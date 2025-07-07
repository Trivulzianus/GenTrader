# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 17:50:01**

| Metric | Value |
|---|---|
| **Total Value** | **$100,654.33** |
| Cash | $1,227.15 |
| Holdings Value | $99,427.18 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.94 | $2,099.40 | 70 |
| ADBE | 5 | $377.60 | $376.86 | $1,884.28 | 65 |
| AMD | 15 | $135.73 | $135.13 | $2,026.95 | 65 |
| AMZN | 10 | $221.52 | $223.18 | $2,231.80 | 70 |
| AVGO | 7 | $275.54 | $275.27 | $1,926.92 | 70 |
| AXP | 7 | $324.46 | $322.28 | $2,255.96 | 75 |
| BA | 10 | $212.15 | $215.54 | $2,155.45 | 65 |
| BAC | 53 | $48.71 | $48.65 | $2,578.45 | 85 |
| C | 30 | $86.59 | $87.58 | $2,627.55 | 85 |
| CAT | 6 | $397.86 | $389.85 | $2,339.07 | 75 |
| COST | 2 | $979.83 | $991.49 | $1,982.98 | 65 |
| CRM | 8 | $268.33 | $269.03 | $2,152.24 | 65 |
| CSCO | 34 | $68.38 | $68.83 | $2,340.22 | 75 |
| CVX | 16 | $146.72 | $145.90 | $2,334.47 | 75 |
| DIS | 17 | $122.85 | $123.11 | $2,092.95 | 70 |
| GOOGL | 13 | $179.38 | $176.37 | $2,292.81 | 75 |
| GS | 3 | $717.52 | $711.05 | $2,133.15 | 85 |
| HD | 6 | $372.64 | $366.24 | $2,197.44 | 65 |
| INTC | 84 | $22.27 | $22.06 | $1,853.04 | 60 |
| JNJ | 13 | $155.80 | $155.42 | $2,020.46 | 65 |
| JPM | 9 | $292.50 | $291.39 | $2,622.47 | 85 |
| KO | 28 | $71.03 | $71.08 | $1,990.10 | 65 |
| LLY | 2 | $776.66 | $768.46 | $1,536.91 | 65 |
| MA | 4 | $563.08 | $562.71 | $2,250.85 | 65 |
| META | 3 | $717.12 | $721.75 | $2,165.25 | 70 |
| MRK | 29 | $82.38 | $81.22 | $2,355.24 | 75 |
| MSFT | 5 | $498.84 | $496.37 | $2,481.85 | 85 |
| NFLX | 1 | $1,279.00 | $1,289.60 | $1,289.60 | 65 |
| NKE | 29 | $75.85 | $76.45 | $2,217.05 | 70 |
| NVDA | 14 | $156.17 | $158.37 | $2,217.18 | 70 |
| ORCL | 11 | $227.51 | $234.15 | $2,575.65 | 85 |
| PEP | 15 | $136.58 | $134.61 | $2,019.15 | 65 |
| PFE | 80 | $25.30 | $25.29 | $2,022.80 | 65 |
| PG | 13 | $160.77 | $160.03 | $2,080.39 | 70 |
| PYPL | 31 | $76.78 | $76.09 | $2,358.79 | 75 |
| QCOM | 14 | $161.73 | $158.78 | $2,222.92 | 70 |
| T | 71 | $28.55 | $28.34 | $2,011.79 | 65 |
| TGT | 20 | $104.92 | $101.45 | $2,029.00 | 65 |
| TSLA | 7 | $289.38 | $292.34 | $2,046.38 | 65 |
| UNH | 7 | $314.75 | $303.04 | $2,121.28 | 65 |
| UNP | 10 | $236.56 | $234.81 | $2,348.15 | 75 |
| V | 6 | $355.95 | $355.68 | $2,134.08 | 70 |
| VZ | 47 | $43.72 | $42.83 | $2,012.78 | 65 |
| WFC | 28 | $82.27 | $81.94 | $2,294.46 | 75 |
| WMT | 22 | $97.28 | $98.93 | $2,176.53 | 70 |
| XOM | 21 | $109.95 | $110.52 | $2,320.94 | 75 |

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

<!--TRADE_LOG_END--> 
