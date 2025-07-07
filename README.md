# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 17:25:45**

| Metric | Value |
|---|---|
| **Total Value** | **$100,708.19** |
| Cash | $744.82 |
| Holdings Value | $99,963.37 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.90 | $2,098.95 | 65 |
| ADBE | 5 | $377.60 | $377.05 | $1,885.25 | 65 |
| AMD | 16 | $135.70 | $135.10 | $2,161.60 | 70 |
| AMZN | 10 | $221.52 | $223.04 | $2,230.40 | 70 |
| AVGO | 7 | $275.54 | $275.60 | $1,929.20 | 65 |
| AXP | 7 | $324.46 | $322.71 | $2,258.97 | 75 |
| BA | 10 | $212.15 | $215.51 | $2,155.09 | 70 |
| BAC | 51 | $48.71 | $48.66 | $2,481.91 | 80 |
| C | 30 | $86.59 | $87.58 | $2,627.36 | 85 |
| CAT | 6 | $397.86 | $390.52 | $2,343.12 | 70 |
| COST | 2 | $979.83 | $991.33 | $1,982.66 | 65 |
| CRM | 8 | $268.33 | $269.57 | $2,156.55 | 65 |
| CSCO | 34 | $68.38 | $68.89 | $2,342.37 | 75 |
| CVX | 16 | $146.72 | $145.84 | $2,333.36 | 75 |
| DIS | 17 | $122.85 | $123.16 | $2,093.76 | 65 |
| GOOGL | 13 | $179.38 | $176.15 | $2,289.95 | 75 |
| GS | 3 | $717.52 | $710.89 | $2,132.67 | 85 |
| HD | 6 | $372.64 | $366.88 | $2,201.31 | 65 |
| INTC | 85 | $22.27 | $22.07 | $1,875.53 | 60 |
| JNJ | 13 | $155.80 | $155.64 | $2,023.30 | 65 |
| JPM | 9 | $292.50 | $291.39 | $2,622.50 | 85 |
| KO | 28 | $71.03 | $71.19 | $1,993.18 | 65 |
| LLY | 2 | $776.66 | $768.46 | $1,536.92 | 65 |
| MA | 4 | $563.08 | $563.24 | $2,252.96 | 65 |
| META | 3 | $717.12 | $722.57 | $2,167.71 | 65 |
| MRK | 29 | $82.38 | $81.38 | $2,360.02 | 75 |
| MSFT | 5 | $498.84 | $496.68 | $2,483.38 | 75 |
| NFLX | 1 | $1,279.00 | $1,289.89 | $1,289.89 | 65 |
| NKE | 29 | $75.85 | $76.47 | $2,217.49 | 70 |
| NVDA | 16 | $156.44 | $158.37 | $2,533.92 | 85 |
| ORCL | 9 | $226.15 | $233.56 | $2,102.01 | 70 |
| PEP | 16 | $136.46 | $134.82 | $2,157.12 | 70 |
| PFE | 86 | $25.31 | $25.32 | $2,177.95 | 70 |
| PG | 13 | $160.77 | $160.03 | $2,080.39 | 70 |
| PYPL | 31 | $76.78 | $76.19 | $2,361.89 | 75 |
| QCOM | 15 | $161.55 | $159.13 | $2,386.95 | 75 |
| T | 72 | $28.54 | $28.36 | $2,041.56 | 65 |
| TGT | 20 | $104.92 | $101.66 | $2,033.20 | 65 |
| TSLA | 7 | $289.38 | $291.70 | $2,041.90 | 60 |
| UNH | 7 | $314.75 | $303.33 | $2,123.31 | 65 |
| UNP | 10 | $236.56 | $235.13 | $2,351.27 | 80 |
| V | 6 | $355.95 | $355.78 | $2,134.68 | 70 |
| VZ | 47 | $43.72 | $42.83 | $2,012.78 | 65 |
| WFC | 28 | $82.27 | $82.06 | $2,297.54 | 75 |
| WMT | 23 | $97.35 | $98.88 | $2,274.24 | 75 |
| XOM | 21 | $109.95 | $110.73 | $2,325.33 | 75 |

<!--PORTFOLIO_STATUS_END-->

## How it Works

The agent performs the following steps in a continuous loop:

1.  **News Aggregation:** Fetches the latest financial news from various sources, including MarketAux, RSS feeds (WSJ, MarketWatch, CNBC, Reuters), and Finviz.
2.  **Stock Analysis:** For each stock on its watchlist, it performs:
    *   **Fundamental Analysis:** Synthesizes relevant news articles.
    *   **Sentiment Analysis:** Calculates a sentiment score for the news using `vaderSentiment`.
    *   **Technical Analysis:** Calculates a suite of technical indicators (SMA, RSI, Bollinger Bands, MACD) and identifies candlestick patterns using the `ta` and `yfinance` libraries.
3.  **AI-Powered Decisions:** It feeds all the gathered data into an OpenAI GPT-4 model, which acts as a seasoned trading analyst to provide a detailed trade recommendation (BUY, SELL, or HOLD) with a confidence score and a full justification.
4.  **Trade Execution:** Executes trades based on the AI's decision.
5.  **Portfolio Management:** Tracks cash, holdings, and overall portfolio value.

## Disclaimer

This is an experimental project for educational purposes. It is not financial advice. Trading stocks involves significant risk, and you should not use this agent with real money without fully understanding the risks and the code.

## Trade Log

<!--TRADE_LOG_START-->
| Timestamp | Action | Symbol | Shares | Price | P/L | Confidence |
|---|---|---|---|---|---|---|
| 2025-07-07 17:25:39 | SELL | AMZN | 1 | $223.02 | $1.36 | 70 |
| 2025-07-07 17:25:39 | SELL | AAPL | 1 | $210.20 | $-0.80 | 65 |
| 2025-07-07 17:25:39 | SELL | BAC | 4 | $48.66 | $-0.18 | 80 |
| 2025-07-07 17:25:39 | SELL | DIS | 1 | $123.16 | $0.30 | 65 |
| 2025-07-07 17:25:39 | SELL | PFE | 1 | $25.35 | $0.04 | 70 |
| 2025-07-07 17:25:39 | SELL | T | 1 | $28.35 | $-0.19 | 65 |
| 2025-07-07 17:25:39 | BUY | NVDA | 2 | $158.40 | N/A | 85 |
| 2025-07-07 17:25:39 | BUY | AVGO | 7 | $275.54 | N/A | 65 |
| 2025-07-07 17:08:10 | SELL | AVGO | 8 | $275.33 | $43.44 | 70 |
| 2025-07-07 17:08:10 | SELL | NVDA | 1 | $158.34 | $2.03 | 70 |
| 2025-07-07 17:08:10 | SELL | T | 3 | $28.28 | $-0.74 | 65 |
| 2025-07-07 17:08:10 | BUY | AAPL | 1 | $210.29 | N/A | 75 |
| 2025-07-07 17:08:10 | BUY | TSLA | 1 | $292.27 | N/A | 65 |
| 2025-07-07 17:08:10 | BUY | GOOGL | 1 | $176.22 | N/A | 75 |
| 2025-07-07 17:08:10 | BUY | INTC | 1 | $22.05 | N/A | 60 |
| 2025-07-07 17:08:10 | BUY | BAC | 1 | $48.49 | N/A | 85 |
| 2025-07-07 17:08:10 | BUY | PYPL | 1 | $76.00 | N/A | 75 |
| 2025-07-07 17:08:10 | BUY | PFE | 7 | $25.24 | N/A | 70 |
| 2025-07-07 17:08:10 | BUY | XOM | 1 | $110.76 | N/A | 75 |
| 2025-07-07 17:08:10 | BUY | CSCO | 2 | $68.85 | N/A | 75 |
| 2025-07-07 16:55:21 | SELL | NVDA | 1 | $158.06 | $1.64 | 75 |
| 2025-07-07 16:55:21 | SELL | AAPL | 1 | $213.55 | $2.25 | 65 |
| 2025-07-07 16:55:21 | SELL | PFE | 5 | $25.23 | $-0.39 | 65 |
| 2025-07-07 16:55:21 | SELL | UNP | 1 | $234.91 | $-1.49 | 75 |
| 2025-07-07 16:55:21 | SELL | CSCO | 1 | $68.81 | $0.44 | 70 |

<!--TRADE_LOG_END--> 
