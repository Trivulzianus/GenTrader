# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-06-30 20:04:18**

| Metric | Value |
|---|---|
| **Total Value** | **$100,321.66** |
| Cash | $178.18 |
| Holdings Value | $100,143.48 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $205.17 | $2,462.04 | 85 |
| ADBE | 5 | $385.76 | $386.88 | $1,934.40 | 65 |
| AMD | 14 | $142.83 | $141.90 | $1,986.60 | 65 |
| AMZN | 9 | $228.48 | $219.39 | $1,974.51 | 65 |
| AVGO | 7 | $276.11 | $275.65 | $1,929.55 | 65 |
| AXP | 6 | $315.89 | $318.92 | $1,913.52 | 65 |
| BA | 10 | $214.55 | $209.51 | $2,095.14 | 65 |
| BAC | 53 | $47.22 | $47.27 | $2,505.57 | 85 |
| C | 27 | $84.30 | $85.10 | $2,297.70 | 75 |
| CAT | 5 | $381.20 | $388.06 | $1,940.28 | 65 |
| COST | 2 | $991.47 | $989.94 | $1,979.88 | 65 |
| CRM | 8 | $274.92 | $272.64 | $2,181.16 | 75 |
| CSCO | 28 | $68.92 | $69.38 | $1,942.64 | 65 |
| CVX | 13 | $143.34 | $143.12 | $1,860.56 | 65 |
| DIS | 20 | $123.12 | $123.95 | $2,479.00 | 85 |
| GOOGL | 15 | $178.80 | $176.23 | $2,643.45 | 85 |
| GS | 3 | $706.65 | $707.75 | $2,123.24 | 85 |
| HD | 6 | $370.25 | $366.60 | $2,199.60 | 75 |
| INTC | 86 | $22.36 | $22.40 | $1,926.40 | 65 |
| JNJ | 13 | $151.96 | $152.68 | $1,984.78 | 65 |
| JPM | 7 | $285.02 | $289.87 | $2,029.09 | 65 |
| KO | 28 | $70.48 | $70.73 | $1,980.58 | 65 |
| LLY | 3 | $767.33 | $779.16 | $2,337.48 | 65 |
| MA | 4 | $537.87 | $562.08 | $2,248.32 | 65 |
| META | 3 | $712.71 | $738.09 | $2,214.27 | 85 |
| MRK | 25 | $78.92 | $79.11 | $1,977.78 | 85 |
| MSFT | 4 | $492.89 | $497.41 | $1,989.64 | 75 |
| NFLX | 1 | $1,334.07 | $1,339.13 | $1,339.13 | 75 |
| NKE | 36 | $71.18 | $71.02 | $2,556.54 | 85 |
| NVDA | 16 | $157.81 | $157.99 | $2,527.84 | 85 |
| ORCL | 9 | $219.56 | $218.63 | $1,967.67 | 65 |
| PEP | 17 | $131.85 | $132.04 | $2,244.68 | 75 |
| PFE | 92 | $24.27 | $24.24 | $2,230.08 | 75 |
| PG | 12 | $159.73 | $159.32 | $1,911.84 | 65 |
| PYPL | 34 | $73.92 | $74.32 | $2,526.88 | 85 |
| QCOM | 16 | $159.24 | $159.26 | $2,548.16 | 85 |
| T | 87 | $28.54 | $28.93 | $2,516.47 | 85 |
| TGT | 23 | $98.82 | $98.65 | $2,268.95 | 75 |
| TSLA | 7 | $320.69 | $317.66 | $2,223.62 | 65 |
| UNH | 8 | $306.63 | $311.78 | $2,494.24 | 85 |
| UNP | 11 | $232.22 | $230.06 | $2,530.61 | 85 |
| V | 6 | $344.95 | $354.74 | $2,128.44 | 65 |
| VZ | 45 | $42.64 | $43.27 | $1,947.15 | 75 |
| WFC | 32 | $79.91 | $80.06 | $2,562.08 | 85 |
| WMT | 26 | $97.15 | $97.77 | $2,541.89 | 85 |
| XOM | 18 | $109.40 | $107.78 | $1,940.04 | 65 |

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
| 2025-06-30 20:04:10 | SELL | AMZN | 2 | $219.39 | $-14.88 | 65 |
| 2025-06-30 20:04:10 | SELL | C | 3 | $85.10 | $2.15 | 75 |
| 2025-06-30 20:04:10 | BUY | BAC | 1 | $47.28 | N/A | 85 |
| 2025-06-30 20:04:10 | BUY | DIS | 4 | $123.95 | N/A | 85 |
| 2025-06-30 19:56:27 | SELL | ADBE | 1 | $387.02 | $1.05 | 65 |
| 2025-06-30 19:56:27 | SELL | INTC | 1 | $22.44 | $0.08 | 65 |
| 2025-06-30 19:56:27 | SELL | PYPL | 1 | $74.38 | $0.44 | 85 |
| 2025-06-30 19:56:27 | SELL | PFE | 1 | $24.19 | $-0.08 | 75 |
| 2025-06-30 19:56:27 | SELL | AXP | 1 | $319.08 | $2.74 | 65 |
| 2025-06-30 19:56:27 | SELL | UNP | 1 | $230.11 | $-1.93 | 85 |
| 2025-06-30 19:56:27 | SELL | CSCO | 1 | $68.65 | $-0.26 | 65 |
| 2025-06-30 19:56:27 | SELL | T | 1 | $28.92 | $0.38 | 85 |
| 2025-06-30 19:56:27 | BUY | AMZN | 2 | $223.30 | N/A | 85 |
| 2025-06-30 19:56:27 | BUY | UNH | 1 | $311.90 | N/A | 85 |
| 2025-06-30 19:56:27 | BUY | BAC | 10 | $47.22 | N/A | 85 |
| 2025-06-30 19:53:35 | SELL | BAC | 12 | $47.21 | N/A | 65 |
| 2025-06-30 19:53:35 | BUY | C | 7 | $85.06 | N/A | 85 |
| 2025-06-30 19:46:44 | SELL | VZ | 1 | $43.18 | N/A | 65 |
| 2025-06-30 19:46:44 | SELL | T | 1 | $28.93 | N/A | 85 |
| 2025-06-30 19:39:40 | SELL | MSFT | 1 | $498.41 | N/A | 65 |
| 2025-06-30 19:39:40 | SELL | UNH | 1 | $311.05 | N/A | 65 |
| 2025-06-30 19:39:40 | BUY | AAPL | 2 | $206.65 | N/A | 85 |
| 2025-06-30 19:39:40 | BUY | BAC | 11 | $47.10 | N/A | 85 |
| 2025-06-30 19:04:19 | SELL | INTC | 1 | $22.44 | N/A | 65 |
| 2025-06-30 19:04:19 | SELL | XOM | 1 | $108.08 | N/A | 65 |

<!--TRADE_LOG_END--> 
