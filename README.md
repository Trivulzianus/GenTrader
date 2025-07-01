# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 14:29:28**

| Metric | Value |
|---|---|
| **Total Value** | **$100,537.56** |
| Cash | $115.48 |
| Holdings Value | $100,422.08 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $209.54 | $2,514.47 | 85 |
| ADBE | 5 | $385.76 | $386.61 | $1,933.05 | 65 |
| AMD | 14 | $142.76 | $137.20 | $1,920.80 | 65 |
| AMZN | 9 | $228.40 | $219.37 | $1,974.34 | 65 |
| AVGO | 9 | $275.08 | $268.16 | $2,413.44 | 85 |
| AXP | 7 | $316.33 | $318.96 | $2,232.72 | 65 |
| BA | 10 | $214.55 | $209.66 | $2,096.65 | 65 |
| BAC | 41 | $47.19 | $47.56 | $1,949.88 | 65 |
| C | 23 | $84.14 | $85.09 | $1,957.18 | 65 |
| CAT | 5 | $381.20 | $388.24 | $1,941.18 | 65 |
| COST | 2 | $991.47 | $986.45 | $1,972.90 | 65 |
| CRM | 9 | $274.67 | $272.79 | $2,455.11 | 75 |
| CSCO | 37 | $68.92 | $68.90 | $2,549.47 | 85 |
| CVX | 13 | $143.34 | $143.48 | $1,865.27 | 65 |
| DIS | 16 | $122.90 | $123.21 | $1,971.36 | 65 |
| GOOGL | 14 | $175.62 | $175.12 | $2,451.68 | 85 |
| GS | 3 | $706.65 | $707.57 | $2,122.70 | 75 |
| HD | 7 | $369.90 | $370.80 | $2,595.60 | 85 |
| INTC | 88 | $22.34 | $22.43 | $1,974.28 | 65 |
| JNJ | 14 | $152.22 | $155.81 | $2,181.34 | 75 |
| JPM | 7 | $285.02 | $289.55 | $2,026.85 | 65 |
| KO | 27 | $70.44 | $71.64 | $1,934.41 | 65 |
| LLY | 3 | $767.33 | $781.66 | $2,344.97 | 65 |
| MA | 4 | $537.87 | $560.99 | $2,243.96 | 65 |
| META | 3 | $712.71 | $730.22 | $2,190.64 | 90 |
| MRK | 25 | $79.01 | $80.13 | $2,003.25 | 65 |
| MSFT | 4 | $492.89 | $497.14 | $1,988.56 | 65 |
| NFLX | 1 | $1,334.07 | $1,322.86 | $1,322.86 | 65 |
| NKE | 27 | $70.41 | $73.58 | $1,986.76 | 65 |
| NVDA | 16 | $156.91 | $154.47 | $2,471.60 | 85 |
| ORCL | 9 | $219.56 | $218.84 | $1,969.54 | 65 |
| PEP | 17 | $131.85 | $134.26 | $2,282.42 | 75 |
| PFE | 93 | $24.27 | $24.72 | $2,298.96 | 75 |
| PG | 12 | $159.73 | $160.41 | $1,924.86 | 65 |
| PYPL | 34 | $73.92 | $74.47 | $2,531.98 | 85 |
| QCOM | 16 | $159.24 | $158.44 | $2,535.04 | 85 |
| T | 88 | $28.54 | $28.91 | $2,544.52 | 85 |
| TGT | 23 | $98.82 | $102.22 | $2,351.17 | 75 |
| TSLA | 7 | $294.26 | $303.69 | $2,125.81 | 65 |
| UNH | 8 | $306.63 | $319.89 | $2,559.15 | 85 |
| UNP | 11 | $232.22 | $232.25 | $2,554.75 | 85 |
| V | 6 | $344.95 | $353.18 | $2,119.08 | 65 |
| VZ | 45 | $42.64 | $43.45 | $1,955.25 | 65 |
| WFC | 32 | $79.91 | $80.47 | $2,575.04 | 85 |
| WMT | 26 | $97.15 | $98.83 | $2,569.71 | 85 |
| XOM | 18 | $109.40 | $107.64 | $1,937.52 | 65 |

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
| 2025-07-01 14:29:22 | SELL | AMD | 1 | $141.90 | $-0.80 | 65 |
| 2025-07-01 14:29:22 | SELL | NKE | 8 | $73.59 | $19.60 | 65 |
| 2025-07-01 14:29:22 | SELL | MRK | 7 | $79.16 | $0.81 | 65 |
| 2025-07-01 14:29:22 | BUY | NVDA | 3 | $154.47 | N/A | 85 |
| 2025-07-01 14:29:22 | BUY | JNJ | 1 | $155.55 | N/A | 75 |
| 2025-07-01 14:29:22 | BUY | PFE | 1 | $24.24 | N/A | 75 |
| 2025-07-01 14:29:22 | BUY | CSCO | 8 | $68.89 | N/A | 85 |
| 2025-07-01 14:16:46 | SELL | AMZN | 2 | $219.39 | $-14.74 | 65 |
| 2025-07-01 14:16:46 | SELL | AMD | 2 | $138.58 | $-7.27 | 65 |
| 2025-07-01 14:16:46 | SELL | CSCO | 3 | $69.19 | $0.71 | 65 |
| 2025-07-01 14:16:46 | SELL | T | 1 | $28.94 | $0.40 | 85 |
| 2025-07-01 14:16:46 | BUY | GOOGL | 14 | $175.62 | N/A | 85 |
| 2025-07-01 14:04:27 | SELL | GOOGL | 15 | $174.57 | $-63.50 | 85 |
| 2025-07-01 14:04:27 | SELL | AMD | 1 | $137.95 | $-4.03 | 75 |
| 2025-07-01 14:04:27 | BUY | INTC | 2 | $22.39 | N/A | 65 |
| 2025-07-01 14:04:27 | BUY | HD | 1 | $367.84 | N/A | 85 |
| 2025-07-01 14:04:27 | BUY | PFE | 1 | $24.50 | N/A | 75 |
| 2025-07-01 14:04:27 | BUY | MRK | 1 | $79.33 | N/A | 85 |
| 2025-07-01 14:04:27 | BUY | CSCO | 3 | $69.07 | N/A | 75 |
| 2025-07-01 14:04:27 | BUY | AVGO | 2 | $271.46 | N/A | 85 |
| 2025-07-01 14:04:27 | BUY | T | 2 | $28.92 | N/A | 85 |
| 2025-07-01 13:56:40 | SELL | NVDA | 3 | $157.99 | $1.26 | 65 |
| 2025-07-01 13:56:40 | SELL | CSCO | 2 | $69.16 | $0.41 | 65 |
| 2025-07-01 13:56:40 | BUY | AMD | 2 | $138.12 | N/A | 85 |
| 2025-07-01 13:56:40 | BUY | MRK | 6 | $79.47 | N/A | 85 |

<!--TRADE_LOG_END--> 
