# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 13:56:47**

| Metric | Value |
|---|---|
| **Total Value** | **$100,404.39** |
| Cash | $99.15 |
| Holdings Value | $100,305.24 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.66 | $2,503.98 | 85 |
| ADBE | 5 | $385.76 | $382.62 | $1,913.10 | 65 |
| AMD | 18 | $141.98 | $138.25 | $2,488.41 | 85 |
| AMZN | 11 | $226.76 | $219.76 | $2,417.41 | 85 |
| AVGO | 7 | $276.11 | $271.96 | $1,903.72 | 85 |
| AXP | 7 | $316.33 | $319.06 | $2,233.42 | 65 |
| BA | 10 | $214.55 | $211.38 | $2,113.80 | 65 |
| BAC | 41 | $47.19 | $47.45 | $1,945.65 | 65 |
| C | 23 | $84.14 | $85.19 | $1,959.48 | 65 |
| CAT | 5 | $381.20 | $385.21 | $1,926.07 | 65 |
| COST | 2 | $991.47 | $987.65 | $1,975.30 | 65 |
| CRM | 9 | $274.67 | $271.80 | $2,446.20 | 75 |
| CSCO | 29 | $68.95 | $69.17 | $2,005.79 | 65 |
| CVX | 13 | $143.34 | $143.09 | $1,860.17 | 65 |
| DIS | 16 | $122.90 | $123.45 | $1,975.20 | 65 |
| GOOGL | 15 | $178.80 | $174.92 | $2,623.75 | 85 |
| GS | 3 | $706.65 | $711.63 | $2,134.90 | 65 |
| HD | 6 | $370.25 | $366.94 | $2,201.64 | 85 |
| INTC | 86 | $22.34 | $22.34 | $1,921.09 | 65 |
| JNJ | 13 | $151.96 | $153.69 | $1,997.90 | 65 |
| JPM | 7 | $285.02 | $290.83 | $2,035.84 | 65 |
| KO | 27 | $70.44 | $71.53 | $1,931.18 | 65 |
| LLY | 3 | $767.33 | $781.03 | $2,343.11 | 65 |
| MA | 4 | $537.87 | $560.74 | $2,242.94 | 65 |
| META | 3 | $712.71 | $735.49 | $2,206.45 | 90 |
| MRK | 31 | $79.04 | $79.45 | $2,463.11 | 85 |
| MSFT | 4 | $492.89 | $497.41 | $1,989.64 | 65 |
| NFLX | 1 | $1,334.07 | $1,335.87 | $1,335.87 | 65 |
| NKE | 35 | $71.14 | $73.26 | $2,564.10 | 85 |
| NVDA | 13 | $157.47 | $156.18 | $2,030.34 | 65 |
| ORCL | 9 | $219.56 | $222.65 | $2,003.85 | 65 |
| PEP | 17 | $131.85 | $133.37 | $2,267.29 | 75 |
| PFE | 91 | $24.27 | $24.46 | $2,226.18 | 75 |
| PG | 12 | $159.73 | $160.05 | $1,920.60 | 65 |
| PYPL | 34 | $73.92 | $74.25 | $2,524.50 | 85 |
| QCOM | 16 | $159.24 | $158.43 | $2,534.88 | 85 |
| T | 87 | $28.54 | $28.91 | $2,515.61 | 85 |
| TGT | 23 | $98.82 | $100.61 | $2,314.03 | 75 |
| TSLA | 7 | $294.26 | $301.83 | $2,112.79 | 65 |
| UNH | 8 | $306.63 | $316.38 | $2,531.04 | 85 |
| UNP | 11 | $232.22 | $230.51 | $2,535.61 | 85 |
| V | 6 | $344.95 | $353.13 | $2,118.78 | 65 |
| VZ | 45 | $42.64 | $43.30 | $1,948.72 | 75 |
| WFC | 32 | $79.91 | $80.31 | $2,569.92 | 85 |
| WMT | 26 | $97.15 | $98.49 | $2,560.74 | 85 |
| XOM | 18 | $109.40 | $107.28 | $1,931.13 | 65 |

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
| 2025-07-01 13:56:40 | SELL | NVDA | 3 | $157.99 | $1.26 | 65 |
| 2025-07-01 13:56:40 | SELL | CSCO | 2 | $69.16 | $0.41 | 65 |
| 2025-07-01 13:56:40 | BUY | AMD | 2 | $138.12 | N/A | 85 |
| 2025-07-01 13:56:40 | BUY | MRK | 6 | $79.47 | N/A | 85 |
| 2025-07-01 13:48:54 | SELL | AMD | 1 | $138.81 | $-3.44 | 75 |
| 2025-07-01 13:48:54 | SELL | PFE | 1 | $24.38 | $0.12 | 75 |
| 2025-07-01 13:48:54 | SELL | MRK | 3 | $79.07 | $0.37 | 65 |
| 2025-07-01 13:48:54 | BUY | CSCO | 3 | $69.38 | N/A | 75 |
| 2025-07-01 13:32:56 | SELL | INTC | 14 | $22.52 | $2.16 | 65 |
| 2025-07-01 13:32:56 | SELL | PFE | 1 | $24.32 | $0.05 | 75 |
| 2025-07-01 13:32:56 | SELL | NKE | 1 | $72.47 | $1.29 | 85 |
| 2025-07-01 13:32:56 | SELL | KO | 1 | $71.43 | $0.95 | 65 |
| 2025-07-01 13:32:56 | SELL | C | 3 | $85.26 | $2.96 | 65 |
| 2025-07-01 13:32:56 | SELL | CSCO | 1 | $69.48 | $0.54 | 65 |
| 2025-07-01 13:32:56 | SELL | VZ | 1 | $43.39 | $0.73 | 65 |
| 2025-07-01 13:32:56 | SELL | T | 1 | $29.07 | $0.53 | 85 |
| 2025-07-01 13:32:56 | BUY | NVDA | 3 | $156.71 | N/A | 85 |
| 2025-07-01 13:32:56 | BUY | AMZN | 2 | $219.01 | N/A | 85 |
| 2025-07-01 13:32:56 | BUY | TSLA | 7 | $294.26 | N/A | 75 |
| 2025-07-01 13:32:56 | BUY | AMD | 3 | $139.51 | N/A | 85 |
| 2025-07-01 13:32:31 | SELL | TSLA | 7 | $294.34 | $-184.46 | 65 |
| 2025-07-01 13:17:39 | SELL | V | 1 | $355.05 | $8.66 | 65 |
| 2025-07-01 13:17:39 | SELL | CSCO | 3 | $69.38 | $1.21 | 65 |
| 2025-07-01 13:17:39 | SELL | VZ | 6 | $43.27 | $3.26 | 65 |
| 2025-07-01 13:17:39 | BUY | INTC | 1 | $22.40 | N/A | 75 |

<!--TRADE_LOG_END--> 
