# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-06-30 19:56:34**

| Metric | Value |
|---|---|
| **Total Value** | **$100,368.91** |
| Cash | $27.18 |
| Holdings Value | $100,341.73 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $205.59 | $2,467.14 | 85 |
| ADBE | 5 | $385.76 | $387.10 | $1,935.50 | 65 |
| AMD | 14 | $142.83 | $142.00 | $1,987.93 | 65 |
| AMZN | 11 | $226.83 | $219.61 | $2,415.71 | 85 |
| AVGO | 7 | $276.11 | $275.39 | $1,927.73 | 65 |
| AXP | 6 | $315.89 | $319.17 | $1,915.02 | 65 |
| BA | 10 | $214.55 | $209.59 | $2,095.90 | 65 |
| BAC | 52 | $47.22 | $47.24 | $2,456.74 | 85 |
| C | 30 | $84.38 | $85.09 | $2,552.85 | 85 |
| CAT | 5 | $381.20 | $388.30 | $1,941.48 | 65 |
| COST | 2 | $991.47 | $990.14 | $1,980.28 | 65 |
| CRM | 8 | $274.92 | $272.44 | $2,179.52 | 85 |
| CSCO | 28 | $68.92 | $69.42 | $1,943.62 | 65 |
| CVX | 13 | $143.34 | $143.21 | $1,861.73 | 65 |
| DIS | 16 | $122.92 | $124.02 | $1,984.32 | 85 |
| GOOGL | 15 | $178.80 | $176.22 | $2,643.30 | 85 |
| GS | 3 | $706.65 | $708.34 | $2,125.01 | 75 |
| HD | 6 | $370.25 | $367.05 | $2,202.27 | 75 |
| INTC | 86 | $22.36 | $22.43 | $1,929.41 | 65 |
| JNJ | 13 | $151.96 | $152.47 | $1,982.11 | 65 |
| JPM | 7 | $285.02 | $290.07 | $2,030.52 | 65 |
| KO | 28 | $70.48 | $70.69 | $1,979.46 | 65 |
| LLY | 3 | $767.33 | $778.30 | $2,334.90 | 65 |
| MA | 4 | $537.87 | $562.12 | $2,248.49 | 65 |
| META | 3 | $712.71 | $738.60 | $2,215.80 | 85 |
| MRK | 25 | $78.92 | $79.06 | $1,976.38 | 85 |
| MSFT | 4 | $492.89 | $498.70 | $1,994.82 | 65 |
| NFLX | 1 | $1,334.07 | $1,339.25 | $1,339.25 | 65 |
| NKE | 36 | $71.18 | $70.95 | $2,554.20 | 85 |
| NVDA | 16 | $157.81 | $158.20 | $2,531.27 | 85 |
| ORCL | 9 | $219.56 | $219.17 | $1,972.53 | 65 |
| PEP | 17 | $131.85 | $132.06 | $2,244.93 | 75 |
| PFE | 92 | $24.27 | $24.25 | $2,230.54 | 75 |
| PG | 12 | $159.73 | $159.21 | $1,910.52 | 65 |
| PYPL | 34 | $73.92 | $74.36 | $2,528.41 | 85 |
| QCOM | 16 | $159.24 | $159.28 | $2,548.56 | 85 |
| T | 87 | $28.54 | $28.91 | $2,515.61 | 85 |
| TGT | 23 | $98.82 | $98.84 | $2,273.26 | 75 |
| TSLA | 7 | $320.69 | $318.37 | $2,228.60 | 75 |
| UNH | 8 | $306.63 | $311.96 | $2,495.68 | 85 |
| UNP | 11 | $232.22 | $230.13 | $2,531.43 | 85 |
| V | 6 | $344.95 | $355.17 | $2,130.99 | 65 |
| VZ | 45 | $42.64 | $43.26 | $1,946.48 | 65 |
| WFC | 32 | $79.91 | $80.11 | $2,563.68 | 85 |
| WMT | 26 | $97.15 | $97.91 | $2,545.66 | 85 |
| XOM | 18 | $109.40 | $107.90 | $1,942.20 | 65 |

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
| 2025-06-30 19:04:19 | SELL | PFE | 1 | $24.20 | N/A | 75 |
| 2025-06-30 19:04:19 | SELL | C | 1 | $85.21 | N/A | 65 |
| 2025-06-30 19:04:19 | SELL | CAT | 1 | $389.02 | N/A | 65 |
| 2025-06-30 19:04:19 | SELL | T | 1 | $28.65 | N/A | 85 |

<!--TRADE_LOG_END--> 
