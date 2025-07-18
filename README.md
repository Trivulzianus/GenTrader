# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 19:36:31**

| Metric | Value |
|---|---|
| **Total Value** | **$101,059.05** |
| Cash | $733.50 |
| Holdings Value | $100,325.55 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.94 | $2,109.45 | 65 |
| ADBE | 6 | $375.23 | $365.65 | $2,193.90 | 65 |
| AMD | 14 | $159.84 | $157.26 | $2,201.64 | 70 |
| AMZN | 11 | $221.97 | $225.99 | $2,485.84 | 75 |
| AVGO | 8 | $275.34 | $283.53 | $2,268.24 | 70 |
| AXP | 7 | $309.18 | $307.74 | $2,154.18 | 65 |
| BA | 10 | $232.01 | $228.83 | $2,288.30 | 65 |
| BAC | 48 | $46.29 | $47.30 | $2,270.40 | 70 |
| C | 29 | $86.63 | $93.08 | $2,699.42 | 85 |
| CAT | 6 | $397.74 | $413.21 | $2,479.26 | 65 |
| COST | 2 | $979.83 | $951.44 | $1,902.88 | 65 |
| CRM | 8 | $267.44 | $262.10 | $2,096.76 | 65 |
| CSCO | 33 | $68.58 | $68.11 | $2,247.79 | 70 |
| CVX | 14 | $147.08 | $148.44 | $2,078.09 | 65 |
| DIS | 19 | $122.65 | $121.23 | $2,303.37 | 75 |
| GOOGL | 13 | $179.34 | $184.71 | $2,401.16 | 75 |
| GS | 3 | $717.52 | $708.32 | $2,124.96 | 85 |
| HD | 6 | $354.18 | $358.60 | $2,151.57 | 65 |
| INTC | 90 | $22.38 | $23.21 | $2,089.35 | 65 |
| JNJ | 14 | $155.98 | $164.01 | $2,296.14 | 70 |
| JPM | 8 | $292.14 | $291.11 | $2,328.84 | 75 |
| KO | 30 | $70.96 | $70.09 | $2,102.85 | 65 |
| LLY | 3 | $781.32 | $773.70 | $2,321.10 | 65 |
| MA | 4 | $563.08 | $551.82 | $2,207.28 | 65 |
| META | 3 | $717.12 | $703.75 | $2,111.25 | 65 |
| MRK | 26 | $82.73 | $80.04 | $2,081.04 | 65 |
| MSFT | 5 | $498.84 | $509.94 | $2,549.70 | 85 |
| NFLX | 1 | $1,208.39 | $1,205.12 | $1,205.12 | 65 |
| NKE | 29 | $71.98 | $72.61 | $2,105.84 | 65 |
| NVDA | 14 | $171.78 | $171.97 | $2,407.58 | 70 |
| ORCL | 9 | $232.91 | $245.81 | $2,212.29 | 75 |
| PEP | 15 | $135.89 | $143.81 | $2,157.15 | 65 |
| PFE | 86 | $25.26 | $24.48 | $2,105.71 | 65 |
| PG | 14 | $152.14 | $155.33 | $2,174.62 | 65 |
| PYPL | 29 | $72.21 | $74.15 | $2,150.35 | 65 |
| QCOM | 13 | $153.79 | $154.47 | $2,008.05 | 65 |
| T | 78 | $27.11 | $26.94 | $2,101.32 | 65 |
| TGT | 20 | $104.82 | $102.88 | $2,057.60 | 65 |
| TSLA | 6 | $318.51 | $328.52 | $1,971.15 | 65 |
| UNH | 8 | $283.36 | $282.34 | $2,258.72 | 65 |
| UNP | 9 | $225.02 | $224.84 | $2,023.56 | 65 |
| V | 6 | $355.85 | $349.00 | $2,093.97 | 65 |
| VZ | 51 | $40.87 | $40.76 | $2,078.51 | 65 |
| WFC | 30 | $78.90 | $80.56 | $2,416.80 | 75 |
| WMT | 22 | $97.29 | $95.13 | $2,092.86 | 65 |
| XOM | 20 | $109.72 | $107.98 | $2,159.60 | 65 |

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
| 2025-07-18 19:36:26 | SELL | AMZN | 1 | $225.95 | $3.65 | 75 |
| 2025-07-18 19:36:26 | SELL | NVDA | 1 | $171.99 | $0.20 | 70 |
| 2025-07-18 19:36:26 | SELL | PYPL | 3 | $74.15 | $5.29 | 65 |
| 2025-07-18 19:36:26 | BUY | DIS | 1 | $121.18 | N/A | 75 |
| 2025-07-18 19:36:26 | BUY | C | 3 | $93.09 | N/A | 85 |
| 2025-07-18 19:36:26 | BUY | CSCO | 2 | $68.11 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
