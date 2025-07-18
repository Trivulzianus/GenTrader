# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 19:25:04**

| Metric | Value |
|---|---|
| **Total Value** | **$101,106.80** |
| Cash | $649.77 |
| Holdings Value | $100,457.03 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.03 | $2,110.30 | 65 |
| ADBE | 6 | $375.23 | $365.97 | $2,195.82 | 65 |
| AMD | 14 | $159.84 | $157.65 | $2,207.10 | 70 |
| AMZN | 12 | $222.30 | $225.94 | $2,711.22 | 85 |
| AVGO | 8 | $275.34 | $283.62 | $2,268.96 | 70 |
| AXP | 7 | $309.18 | $307.87 | $2,155.09 | 65 |
| BA | 10 | $232.01 | $228.98 | $2,289.80 | 65 |
| BAC | 48 | $46.29 | $47.27 | $2,268.96 | 70 |
| C | 26 | $85.88 | $93.17 | $2,422.42 | 75 |
| CAT | 6 | $397.74 | $413.94 | $2,483.64 | 65 |
| COST | 2 | $979.83 | $950.75 | $1,901.51 | 65 |
| CRM | 8 | $267.44 | $262.38 | $2,099.04 | 65 |
| CSCO | 31 | $68.61 | $68.12 | $2,111.72 | 65 |
| CVX | 14 | $147.08 | $148.18 | $2,074.45 | 65 |
| DIS | 18 | $122.74 | $121.19 | $2,181.42 | 70 |
| GOOGL | 13 | $179.34 | $184.79 | $2,402.27 | 75 |
| GS | 3 | $717.52 | $708.54 | $2,125.62 | 85 |
| HD | 6 | $354.18 | $358.92 | $2,153.52 | 65 |
| INTC | 90 | $22.38 | $23.24 | $2,091.59 | 65 |
| JNJ | 14 | $155.98 | $164.01 | $2,296.14 | 70 |
| JPM | 8 | $292.14 | $291.15 | $2,329.18 | 75 |
| KO | 30 | $70.96 | $70.13 | $2,103.90 | 65 |
| LLY | 3 | $781.32 | $772.65 | $2,317.95 | 65 |
| MA | 4 | $563.08 | $551.71 | $2,206.84 | 65 |
| META | 3 | $717.12 | $703.84 | $2,111.52 | 65 |
| MRK | 26 | $82.73 | $80.09 | $2,082.34 | 65 |
| MSFT | 5 | $498.84 | $511.46 | $2,557.32 | 85 |
| NFLX | 1 | $1,208.39 | $1,206.85 | $1,206.85 | 65 |
| NKE | 29 | $71.98 | $72.60 | $2,105.40 | 65 |
| NVDA | 15 | $171.79 | $172.10 | $2,581.50 | 85 |
| ORCL | 9 | $232.91 | $245.97 | $2,213.68 | 70 |
| PEP | 15 | $135.89 | $143.97 | $2,159.62 | 65 |
| PFE | 86 | $25.26 | $24.50 | $2,107.00 | 65 |
| PG | 14 | $152.14 | $155.23 | $2,173.22 | 65 |
| PYPL | 32 | $72.39 | $74.23 | $2,375.36 | 75 |
| QCOM | 13 | $153.79 | $154.56 | $2,009.28 | 65 |
| T | 78 | $27.11 | $26.93 | $2,100.15 | 65 |
| TGT | 20 | $104.82 | $103.03 | $2,060.60 | 65 |
| TSLA | 6 | $318.51 | $329.39 | $1,976.34 | 65 |
| UNH | 8 | $283.36 | $282.60 | $2,260.78 | 65 |
| UNP | 9 | $225.02 | $224.87 | $2,023.83 | 65 |
| V | 6 | $355.85 | $349.13 | $2,094.80 | 65 |
| VZ | 51 | $40.87 | $40.76 | $2,078.51 | 65 |
| WFC | 30 | $78.90 | $80.49 | $2,414.70 | 75 |
| WMT | 22 | $97.29 | $95.12 | $2,092.75 | 65 |
| XOM | 20 | $109.72 | $108.15 | $2,163.00 | 70 |

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
| 2025-07-18 19:24:57 | SELL | C | 3 | $93.17 | $19.60 | 75 |
| 2025-07-18 19:24:57 | BUY | AMZN | 2 | $225.93 | N/A | 85 |
| 2025-07-18 19:24:57 | BUY | NVDA | 1 | $172.15 | N/A | 85 |
| 2025-07-18 19:24:57 | BUY | GOOGL | 1 | $184.87 | N/A | 75 |
| 2025-07-18 19:24:57 | BUY | XOM | 1 | $108.14 | N/A | 70 |
| 2025-07-18 19:09:24 | SELL | NVDA | 2 | $173.00 | $2.16 | 70 |
| 2025-07-18 19:09:24 | SELL | XOM | 1 | $111.66 | $1.76 | 65 |
| 2025-07-18 19:09:24 | BUY | PYPL | 3 | $74.15 | N/A | 75 |
| 2025-07-18 19:09:24 | BUY | WFC | 2 | $80.58 | N/A | 75 |
| 2025-07-18 18:57:56 | SELL | BAC | 1 | $47.31 | $1.01 | 70 |
| 2025-07-18 18:57:56 | SELL | CVX | 1 | $146.95 | $-0.12 | 60 |
| 2025-07-18 18:57:56 | BUY | NVDA | 2 | $172.08 | N/A | 85 |
| 2025-07-18 18:57:56 | BUY | WFC | 1 | $80.47 | N/A | 70 |
| 2025-07-18 18:45:25 | SELL | BAC | 2 | $47.34 | $1.98 | 70 |
| 2025-07-18 18:45:25 | SELL | WFC | 1 | $80.39 | $1.62 | 65 |
| 2025-07-18 18:45:25 | SELL | CVX | 1 | $146.93 | $-0.13 | 65 |
| 2025-07-18 18:27:27 | BUY | BAC | 3 | $47.28 | N/A | 75 |
| 2025-07-18 18:27:27 | BUY | C | 2 | $93.11 | N/A | 85 |
| 2025-07-18 18:27:27 | BUY | WFC | 1 | $80.35 | N/A | 70 |
| 2025-07-18 18:10:57 | SELL | C | 2 | $93.21 | $13.13 | 75 |
| 2025-07-18 18:10:57 | SELL | CSCO | 4 | $68.07 | $-1.94 | 65 |
| 2025-07-18 18:10:57 | BUY | INTC | 5 | $23.18 | N/A | 65 |
| 2025-07-18 17:53:12 | SELL | NVDA | 1 | $172.46 | $0.53 | 70 |
| 2025-07-18 17:53:12 | SELL | INTC | 5 | $23.22 | $4.15 | 60 |
| 2025-07-18 17:53:12 | SELL | PYPL | 3 | $73.82 | $4.38 | 65 |

<!--TRADE_LOG_END--> 
