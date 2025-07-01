# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 15:48:33**

| Metric | Value |
|---|---|
| **Total Value** | **$100,923.65** |
| Cash | $218.66 |
| Holdings Value | $100,704.98 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.29 | $2,487.44 | 85 |
| ADBE | 5 | $385.76 | $391.06 | $1,955.31 | 65 |
| AMD | 16 | $141.82 | $136.33 | $2,181.28 | 75 |
| AMZN | 9 | $228.45 | $219.12 | $1,972.12 | 65 |
| AVGO | 9 | $275.08 | $265.18 | $2,386.62 | 85 |
| AXP | 6 | $315.94 | $319.51 | $1,917.06 | 75 |
| BA | 9 | $215.30 | $208.21 | $1,873.90 | 65 |
| BAC | 51 | $47.30 | $47.74 | $2,434.99 | 85 |
| C | 28 | $84.31 | $85.08 | $2,382.24 | 85 |
| CAT | 5 | $381.20 | $391.96 | $1,959.80 | 65 |
| COST | 2 | $991.47 | $983.59 | $1,967.17 | 75 |
| CRM | 8 | $274.83 | $271.64 | $2,173.12 | 75 |
| CSCO | 28 | $68.90 | $68.70 | $1,923.74 | 65 |
| CVX | 14 | $143.46 | $145.63 | $2,038.82 | 85 |
| DIS | 16 | $122.90 | $122.61 | $1,961.76 | 65 |
| GOOGL | 14 | $175.62 | $174.96 | $2,449.44 | 85 |
| GS | 3 | $706.65 | $701.79 | $2,105.38 | 65 |
| HD | 7 | $369.90 | $378.72 | $2,651.04 | 85 |
| INTC | 81 | $22.31 | $23.09 | $1,870.29 | 65 |
| JNJ | 12 | $151.57 | $157.29 | $1,887.48 | 65 |
| JPM | 7 | $285.02 | $286.81 | $2,007.70 | 65 |
| KO | 29 | $70.55 | $72.16 | $2,092.64 | 75 |
| LLY | 3 | $767.33 | $786.91 | $2,360.73 | 65 |
| MA | 4 | $537.87 | $562.84 | $2,251.34 | 65 |
| META | 3 | $712.71 | $719.50 | $2,158.49 | 90 |
| MRK | 30 | $79.35 | $82.67 | $2,479.95 | 85 |
| MSFT | 4 | $492.89 | $492.48 | $1,969.92 | 85 |
| NFLX | 1 | $1,334.07 | $1,286.89 | $1,286.89 | 85 |
| NKE | 34 | $71.01 | $73.70 | $2,505.69 | 85 |
| NVDA | 12 | $155.37 | $152.25 | $1,827.00 | 65 |
| ORCL | 9 | $219.56 | $217.84 | $1,960.56 | 65 |
| PEP | 16 | $131.60 | $136.08 | $2,177.28 | 75 |
| PFE | 97 | $24.29 | $25.23 | $2,447.49 | 85 |
| PG | 12 | $159.73 | $162.05 | $1,944.60 | 65 |
| PYPL | 33 | $73.91 | $75.05 | $2,476.65 | 85 |
| QCOM | 16 | $159.24 | $159.57 | $2,553.20 | 85 |
| T | 85 | $28.52 | $28.86 | $2,452.98 | 85 |
| TGT | 21 | $98.42 | $104.59 | $2,196.49 | 75 |
| TSLA | 7 | $292.04 | $302.12 | $2,114.88 | 75 |
| UNH | 8 | $306.63 | $324.26 | $2,594.08 | 85 |
| UNP | 11 | $232.22 | $236.07 | $2,596.82 | 85 |
| V | 6 | $344.95 | $355.13 | $2,130.78 | 85 |
| VZ | 50 | $42.73 | $43.69 | $2,184.50 | 75 |
| WFC | 31 | $79.89 | $80.52 | $2,496.12 | 85 |
| WMT | 25 | $97.07 | $98.30 | $2,457.42 | 85 |
| XOM | 22 | $109.34 | $109.17 | $2,401.74 | 80 |

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
| 2025-07-01 15:48:26 | SELL | AMZN | 2 | $219.39 | $-14.82 | 65 |
| 2025-07-01 15:48:26 | SELL | NVDA | 4 | $157.99 | $7.85 | 65 |
| 2025-07-01 15:48:26 | SELL | INTC | 1 | $23.09 | $0.77 | 65 |
| 2025-07-01 15:48:26 | SELL | PFE | 1 | $25.22 | $0.92 | 85 |
| 2025-07-01 15:48:26 | BUY | TSLA | 1 | $302.11 | N/A | 75 |
| 2025-07-01 15:48:26 | BUY | KO | 3 | $72.15 | N/A | 75 |
| 2025-07-01 15:48:26 | BUY | C | 6 | $85.11 | N/A | 85 |
| 2025-07-01 15:40:30 | SELL | JNJ | 1 | $156.97 | $4.99 | 65 |
| 2025-07-01 15:40:30 | SELL | C | 3 | $85.23 | $3.01 | 65 |
| 2025-07-01 15:40:30 | BUY | XOM | 4 | $109.07 | N/A | 85 |
| 2025-07-01 15:30:17 | SELL | CRM | 1 | $273.37 | $-1.30 | 75 |
| 2025-07-01 15:30:17 | SELL | AMD | 2 | $136.40 | $-9.64 | 75 |
| 2025-07-01 15:30:17 | SELL | INTC | 2 | $22.86 | $1.05 | 65 |
| 2025-07-01 15:30:17 | SELL | PFE | 1 | $25.12 | $0.81 | 85 |
| 2025-07-01 15:30:17 | SELL | BA | 1 | $207.81 | $-6.74 | 65 |
| 2025-07-01 15:30:17 | BUY | BAC | 11 | $47.72 | N/A | 85 |
| 2025-07-01 15:30:17 | BUY | C | 2 | $85.19 | N/A | 75 |
| 2025-07-01 15:16:59 | SELL | KO | 1 | $72.42 | $1.98 | 65 |
| 2025-07-01 15:16:59 | SELL | PEP | 1 | $135.79 | $3.93 | 75 |
| 2025-07-01 15:16:59 | BUY | JNJ | 1 | $157.42 | N/A | 75 |
| 2025-07-01 15:16:59 | BUY | AMD | 2 | $135.28 | N/A | 85 |
| 2025-07-01 15:16:59 | BUY | CVX | 1 | $145.10 | N/A | 75 |
| 2025-07-01 15:04:07 | SELL | AMD | 2 | $136.43 | $-9.83 | 75 |
| 2025-07-01 15:04:07 | SELL | CSCO | 4 | $69.05 | $0.54 | 65 |
| 2025-07-01 15:04:07 | BUY | NKE | 1 | $71.04 | N/A | 85 |

<!--TRADE_LOG_END--> 
