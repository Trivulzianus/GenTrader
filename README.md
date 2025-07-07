# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 18:11:02**

| Metric | Value |
|---|---|
| **Total Value** | **$100,669.08** |
| Cash | $973.67 |
| Holdings Value | $99,695.42 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.93 | $2,099.30 | 75 |
| ADBE | 5 | $377.60 | $376.74 | $1,883.68 | 65 |
| AMD | 15 | $135.73 | $134.93 | $2,023.95 | 65 |
| AMZN | 11 | $221.71 | $223.59 | $2,459.55 | 85 |
| AVGO | 7 | $275.54 | $274.85 | $1,923.95 | 65 |
| AXP | 7 | $324.46 | $322.36 | $2,256.52 | 70 |
| BA | 10 | $212.15 | $216.71 | $2,167.10 | 70 |
| BAC | 53 | $48.71 | $48.66 | $2,578.88 | 85 |
| C | 25 | $86.37 | $87.65 | $2,191.25 | 70 |
| CAT | 6 | $397.86 | $390.13 | $2,340.81 | 75 |
| COST | 2 | $979.83 | $989.20 | $1,978.40 | 65 |
| CRM | 8 | $268.33 | $269.19 | $2,153.52 | 65 |
| CSCO | 32 | $68.35 | $68.80 | $2,201.44 | 70 |
| CVX | 16 | $146.72 | $145.94 | $2,335.04 | 75 |
| DIS | 18 | $122.86 | $123.00 | $2,214.00 | 75 |
| GOOGL | 13 | $179.38 | $176.23 | $2,290.99 | 75 |
| GS | 3 | $717.52 | $712.06 | $2,136.18 | 70 |
| HD | 6 | $372.64 | $366.25 | $2,197.50 | 70 |
| INTC | 90 | $22.26 | $22.05 | $1,984.05 | 65 |
| JNJ | 13 | $155.80 | $155.44 | $2,020.72 | 65 |
| JPM | 9 | $292.50 | $291.84 | $2,626.56 | 85 |
| KO | 28 | $71.03 | $71.08 | $1,990.30 | 65 |
| LLY | 2 | $776.66 | $768.00 | $1,536.01 | 65 |
| MA | 4 | $563.08 | $562.21 | $2,248.84 | 65 |
| META | 3 | $717.12 | $721.45 | $2,164.34 | 85 |
| MRK | 29 | $82.38 | $81.19 | $2,354.37 | 75 |
| MSFT | 5 | $498.84 | $496.70 | $2,483.50 | 85 |
| NFLX | 1 | $1,279.00 | $1,288.65 | $1,288.65 | 65 |
| NKE | 29 | $75.85 | $76.49 | $2,218.27 | 70 |
| NVDA | 16 | $156.45 | $158.42 | $2,534.68 | 85 |
| ORCL | 11 | $227.51 | $234.35 | $2,577.89 | 85 |
| PEP | 15 | $136.58 | $134.63 | $2,019.45 | 65 |
| PFE | 84 | $25.30 | $25.25 | $2,120.73 | 70 |
| PG | 13 | $160.77 | $160.19 | $2,082.47 | 65 |
| PYPL | 29 | $76.84 | $76.06 | $2,205.74 | 70 |
| QCOM | 14 | $161.73 | $158.66 | $2,221.24 | 75 |
| T | 75 | $28.53 | $28.30 | $2,122.76 | 70 |
| TGT | 20 | $104.92 | $101.57 | $2,031.42 | 65 |
| TSLA | 7 | $289.38 | $293.53 | $2,054.71 | 65 |
| UNH | 7 | $314.75 | $302.07 | $2,114.49 | 65 |
| UNP | 10 | $236.56 | $234.96 | $2,349.60 | 75 |
| V | 6 | $355.95 | $355.83 | $2,135.01 | 70 |
| VZ | 47 | $43.72 | $42.83 | $2,012.78 | 65 |
| WFC | 29 | $82.26 | $82.04 | $2,379.16 | 80 |
| WMT | 22 | $97.28 | $98.99 | $2,177.82 | 70 |
| XOM | 20 | $109.93 | $110.39 | $2,207.80 | 70 |

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
| 2025-07-07 18:10:56 | SELL | PYPL | 2 | $76.04 | $-1.49 | 70 |
| 2025-07-07 18:10:56 | SELL | C | 5 | $87.66 | $5.36 | 70 |
| 2025-07-07 18:10:56 | SELL | CSCO | 2 | $68.80 | $0.84 | 70 |
| 2025-07-07 18:10:56 | SELL | XOM | 1 | $110.36 | $0.41 | 70 |
| 2025-07-07 18:10:56 | BUY | NVDA | 2 | $158.41 | N/A | 85 |
| 2025-07-07 18:10:56 | BUY | AMZN | 1 | $223.59 | N/A | 85 |
| 2025-07-07 18:10:56 | BUY | INTC | 6 | $22.03 | N/A | 65 |
| 2025-07-07 18:10:56 | BUY | DIS | 1 | $123.00 | N/A | 75 |
| 2025-07-07 18:10:56 | BUY | PFE | 4 | $25.25 | N/A | 70 |
| 2025-07-07 18:10:56 | BUY | WFC | 1 | $82.03 | N/A | 80 |
| 2025-07-07 18:10:56 | BUY | T | 4 | $28.31 | N/A | 70 |
| 2025-07-07 17:49:54 | SELL | NVDA | 2 | $158.34 | $3.80 | 70 |
| 2025-07-07 17:49:54 | SELL | AMD | 1 | $135.16 | $-0.54 | 65 |
| 2025-07-07 17:49:54 | SELL | INTC | 1 | $22.07 | $-0.20 | 60 |
| 2025-07-07 17:49:54 | SELL | WMT | 1 | $98.86 | $1.51 | 70 |
| 2025-07-07 17:49:54 | SELL | PFE | 6 | $25.38 | $0.45 | 65 |
| 2025-07-07 17:49:54 | SELL | PEP | 1 | $134.62 | $-1.84 | 65 |
| 2025-07-07 17:49:54 | SELL | QCOM | 1 | $158.93 | $-2.62 | 70 |
| 2025-07-07 17:49:54 | SELL | T | 1 | $28.33 | $-0.22 | 65 |
| 2025-07-07 17:49:54 | BUY | ORCL | 2 | $233.65 | N/A | 85 |
| 2025-07-07 17:49:54 | BUY | BAC | 2 | $48.64 | N/A | 85 |
| 2025-07-07 17:25:39 | SELL | AMZN | 1 | $223.02 | $1.36 | 70 |
| 2025-07-07 17:25:39 | SELL | AAPL | 1 | $210.20 | $-0.80 | 65 |
| 2025-07-07 17:25:39 | SELL | BAC | 4 | $48.66 | $-0.18 | 80 |
| 2025-07-07 17:25:39 | SELL | DIS | 1 | $123.16 | $0.30 | 65 |

<!--TRADE_LOG_END--> 
