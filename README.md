# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 15:55:32**

| Metric | Value |
|---|---|
| **Total Value** | **$100,968.66** |
| Cash | $189.73 |
| Holdings Value | $100,778.93 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.40 | $2,488.80 | 85 |
| ADBE | 5 | $385.76 | $391.10 | $1,955.48 | 75 |
| AMD | 14 | $141.81 | $136.24 | $1,907.38 | 65 |
| AMZN | 11 | $226.78 | $219.22 | $2,411.42 | 85 |
| AVGO | 9 | $275.08 | $265.43 | $2,388.87 | 85 |
| AXP | 6 | $315.94 | $319.95 | $1,919.73 | 65 |
| BA | 9 | $215.30 | $208.55 | $1,876.95 | 65 |
| BAC | 51 | $47.30 | $47.80 | $2,437.55 | 85 |
| C | 23 | $84.14 | $85.08 | $1,956.73 | 65 |
| CAT | 5 | $381.20 | $391.83 | $1,959.15 | 65 |
| COST | 2 | $991.47 | $983.65 | $1,967.31 | 75 |
| CRM | 8 | $274.83 | $272.05 | $2,176.40 | 75 |
| CSCO | 27 | $68.88 | $68.67 | $1,853.96 | 65 |
| CVX | 16 | $143.73 | $145.63 | $2,330.08 | 85 |
| DIS | 16 | $122.90 | $122.45 | $1,959.28 | 65 |
| GOOGL | 14 | $175.62 | $174.97 | $2,449.61 | 85 |
| GS | 3 | $706.65 | $702.99 | $2,108.95 | 65 |
| HD | 7 | $369.90 | $378.74 | $2,651.18 | 85 |
| INTC | 81 | $22.31 | $23.09 | $1,870.69 | 65 |
| JNJ | 12 | $151.57 | $157.12 | $1,885.44 | 65 |
| JPM | 7 | $285.02 | $287.05 | $2,009.35 | 65 |
| KO | 26 | $70.37 | $72.08 | $1,874.08 | 65 |
| LLY | 3 | $767.33 | $788.20 | $2,364.59 | 65 |
| MA | 4 | $537.87 | $562.88 | $2,251.53 | 65 |
| META | 3 | $712.71 | $719.07 | $2,157.21 | 88 |
| MRK | 30 | $79.35 | $82.55 | $2,476.50 | 85 |
| MSFT | 4 | $492.89 | $492.47 | $1,969.88 | 85 |
| NFLX | 1 | $1,334.07 | $1,285.76 | $1,285.76 | 85 |
| NKE | 34 | $71.01 | $73.69 | $2,505.63 | 85 |
| NVDA | 16 | $154.76 | $152.86 | $2,445.76 | 85 |
| ORCL | 9 | $219.56 | $218.18 | $1,963.62 | 65 |
| PEP | 16 | $131.60 | $135.93 | $2,174.88 | 75 |
| PFE | 97 | $24.29 | $25.25 | $2,448.76 | 85 |
| PG | 12 | $159.73 | $161.93 | $1,943.16 | 65 |
| PYPL | 33 | $73.91 | $75.00 | $2,474.84 | 85 |
| QCOM | 16 | $159.24 | $159.89 | $2,558.24 | 85 |
| T | 85 | $28.52 | $28.82 | $2,449.70 | 85 |
| TGT | 21 | $98.42 | $104.74 | $2,199.54 | 75 |
| TSLA | 6 | $287.77 | $302.19 | $1,813.12 | 65 |
| UNH | 8 | $306.63 | $323.74 | $2,589.92 | 85 |
| UNP | 11 | $232.22 | $236.02 | $2,596.22 | 85 |
| V | 6 | $344.95 | $354.98 | $2,129.88 | 85 |
| VZ | 50 | $42.73 | $43.70 | $2,184.75 | 75 |
| WFC | 31 | $79.89 | $80.58 | $2,497.98 | 85 |
| WMT | 25 | $97.07 | $98.28 | $2,457.12 | 85 |
| XOM | 22 | $109.34 | $109.18 | $2,401.96 | 85 |

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
| 2025-07-01 15:55:25 | SELL | TSLA | 1 | $317.66 | $25.62 | 65 |
| 2025-07-01 15:55:25 | SELL | AMD | 2 | $141.90 | $0.16 | 65 |
| 2025-07-01 15:55:25 | SELL | KO | 3 | $72.08 | $4.60 | 65 |
| 2025-07-01 15:55:25 | SELL | C | 5 | $85.07 | $3.83 | 65 |
| 2025-07-01 15:55:25 | SELL | CSCO | 1 | $69.38 | $0.48 | 65 |
| 2025-07-01 15:55:25 | BUY | NVDA | 4 | $152.91 | N/A | 85 |
| 2025-07-01 15:55:25 | BUY | AMZN | 2 | $219.27 | N/A | 85 |
| 2025-07-01 15:55:25 | BUY | CVX | 2 | $145.61 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
