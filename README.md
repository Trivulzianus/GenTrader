# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 17:56:34**

| Metric | Value |
|---|---|
| **Total Value** | **$101,214.05** |
| Cash | $530.18 |
| Holdings Value | $100,683.87 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.12 | $2,497.41 | 85 |
| ADBE | 5 | $385.76 | $391.43 | $1,957.15 | 65 |
| AMD | 17 | $140.02 | $137.39 | $2,335.63 | 85 |
| AMZN | 11 | $226.78 | $220.78 | $2,428.59 | 85 |
| AVGO | 9 | $272.95 | $266.10 | $2,394.93 | 85 |
| AXP | 6 | $315.94 | $324.27 | $1,945.62 | 65 |
| BA | 9 | $215.30 | $210.71 | $1,896.39 | 65 |
| BAC | 51 | $47.30 | $48.20 | $2,457.95 | 85 |
| C | 22 | $84.03 | $86.41 | $1,900.91 | 65 |
| CAT | 5 | $381.20 | $392.03 | $1,960.15 | 65 |
| COST | 2 | $991.47 | $986.96 | $1,973.92 | 65 |
| CRM | 9 | $274.79 | $273.92 | $2,465.24 | 85 |
| CSCO | 27 | $68.84 | $69.19 | $1,868.00 | 65 |
| CVX | 17 | $143.81 | $145.59 | $2,475.03 | 85 |
| DIS | 16 | $122.87 | $123.53 | $1,976.40 | 65 |
| GOOGL | 14 | $175.62 | $175.54 | $2,457.56 | 85 |
| GS | 3 | $706.65 | $707.74 | $2,123.20 | 65 |
| HD | 7 | $369.90 | $375.75 | $2,630.25 | 85 |
| INTC | 82 | $22.23 | $22.96 | $1,883.13 | 65 |
| JNJ | 12 | $151.63 | $155.53 | $1,866.36 | 65 |
| JPM | 7 | $285.02 | $290.12 | $2,030.88 | 65 |
| KO | 26 | $70.42 | $71.69 | $1,863.81 | 65 |
| LLY | 3 | $767.33 | $778.80 | $2,336.40 | 65 |
| MA | 4 | $537.87 | $566.06 | $2,264.24 | 75 |
| META | 3 | $712.71 | $721.56 | $2,164.68 | 85 |
| MRK | 30 | $79.35 | $81.98 | $2,459.40 | 85 |
| MSFT | 4 | $492.89 | $493.24 | $1,972.95 | 65 |
| NFLX | 1 | $1,334.07 | $1,299.38 | $1,299.38 | 85 |
| NKE | 33 | $70.93 | $73.06 | $2,411.14 | 85 |
| NVDA | 12 | $152.87 | $154.54 | $1,854.48 | 65 |
| ORCL | 9 | $219.56 | $219.87 | $1,978.83 | 65 |
| PEP | 16 | $131.60 | $134.97 | $2,159.44 | 75 |
| PFE | 98 | $24.29 | $25.02 | $2,452.45 | 85 |
| PG | 12 | $159.73 | $160.89 | $1,930.68 | 65 |
| PYPL | 32 | $73.86 | $75.66 | $2,420.96 | 85 |
| QCOM | 15 | $159.12 | $160.12 | $2,401.80 | 85 |
| T | 85 | $28.52 | $28.86 | $2,453.53 | 85 |
| TGT | 21 | $98.42 | $104.09 | $2,185.89 | 75 |
| TSLA | 6 | $285.42 | $298.90 | $1,793.38 | 65 |
| UNH | 8 | $306.63 | $322.55 | $2,580.40 | 85 |
| UNP | 11 | $232.22 | $235.19 | $2,587.12 | 85 |
| V | 6 | $344.95 | $356.94 | $2,141.64 | 85 |
| VZ | 49 | $42.71 | $43.73 | $2,143.01 | 75 |
| WFC | 30 | $79.85 | $81.38 | $2,441.40 | 85 |
| WMT | 25 | $97.07 | $98.41 | $2,460.32 | 85 |
| XOM | 22 | $109.36 | $109.17 | $2,401.85 | 85 |

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
| 2025-07-01 17:56:28 | SELL | NVDA | 3 | $157.99 | $12.29 | 65 |
| 2025-07-01 17:56:28 | SELL | TSLA | 1 | $317.66 | $27.63 | 65 |
| 2025-07-01 17:56:28 | SELL | C | 2 | $86.39 | $4.32 | 65 |
| 2025-07-01 17:56:28 | BUY | CRM | 1 | $273.90 | N/A | 85 |
| 2025-07-01 17:56:28 | BUY | INTC | 1 | $22.98 | N/A | 65 |
| 2025-07-01 17:56:28 | BUY | XOM | 2 | $109.14 | N/A | 85 |
| 2025-07-01 17:49:44 | SELL | TGT | 2 | $104.10 | $10.37 | 75 |
| 2025-07-01 17:49:44 | BUY | C | 2 | $86.38 | N/A | 75 |
| 2025-07-01 17:40:46 | SELL | XOM | 2 | $109.32 | $-0.11 | 75 |
| 2025-07-01 17:40:46 | SELL | INTC | 1 | $22.98 | $0.75 | 65 |
| 2025-07-01 17:40:46 | SELL | PFE | 1 | $25.00 | $0.69 | 85 |
| 2025-07-01 17:40:46 | SELL | CSCO | 1 | $69.07 | $0.22 | 65 |
| 2025-07-01 17:40:46 | BUY | VZ | 5 | $43.67 | N/A | 75 |
| 2025-07-01 17:40:46 | BUY | TGT | 2 | $104.20 | N/A | 85 |
| 2025-07-01 17:30:00 | SELL | INTC | 1 | $23.02 | $0.79 | 65 |
| 2025-07-01 17:30:00 | SELL | CSCO | 4 | $69.02 | $0.61 | 65 |
| 2025-07-01 17:30:00 | SELL | VZ | 6 | $43.63 | $5.43 | 65 |
| 2025-07-01 17:30:00 | BUY | AMD | 1 | $137.02 | N/A | 85 |
| 2025-07-01 17:30:00 | BUY | AVGO | 2 | $266.08 | N/A | 85 |
| 2025-07-01 17:17:09 | SELL | C | 3 | $86.17 | $5.64 | 65 |
| 2025-07-01 17:17:09 | BUY | XOM | 4 | $108.92 | N/A | 85 |
| 2025-07-01 17:06:51 | SELL | AMD | 1 | $137.57 | $-2.48 | 75 |
| 2025-07-01 17:06:51 | SELL | DIS | 4 | $123.20 | $1.06 | 65 |
| 2025-07-01 17:06:51 | SELL | CSCO | 3 | $68.96 | $0.23 | 75 |
| 2025-07-01 17:06:51 | BUY | NVDA | 3 | $154.74 | N/A | 85 |

<!--TRADE_LOG_END--> 
