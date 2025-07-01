# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 12:05:29**

| Metric | Value |
|---|---|
| **Total Value** | **$100,340.42** |
| Cash | $329.05 |
| Holdings Value | $100,011.37 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $205.17 | $2,462.04 | 85 |
| ADBE | 5 | $385.76 | $386.88 | $1,934.40 | 65 |
| AMD | 14 | $142.83 | $141.90 | $1,986.60 | 65 |
| AMZN | 9 | $228.48 | $219.39 | $1,974.51 | 65 |
| AVGO | 7 | $276.11 | $275.65 | $1,929.55 | 65 |
| AXP | 7 | $316.33 | $318.98 | $2,232.86 | 65 |
| BA | 10 | $214.55 | $209.53 | $2,095.30 | 65 |
| BAC | 42 | $47.20 | $47.32 | $1,987.44 | 65 |
| C | 23 | $84.16 | $85.12 | $1,957.76 | 85 |
| CAT | 5 | $381.20 | $388.21 | $1,941.05 | 65 |
| COST | 2 | $991.47 | $989.94 | $1,979.88 | 65 |
| CRM | 9 | $274.67 | $272.69 | $2,454.21 | 85 |
| CSCO | 28 | $68.92 | $69.38 | $1,942.64 | 65 |
| CVX | 13 | $143.34 | $143.19 | $1,861.47 | 65 |
| DIS | 16 | $122.90 | $124.01 | $1,984.16 | 65 |
| GOOGL | 15 | $178.80 | $176.23 | $2,643.45 | 85 |
| GS | 3 | $706.65 | $707.75 | $2,123.25 | 85 |
| HD | 7 | $369.73 | $366.64 | $2,566.48 | 85 |
| INTC | 100 | $22.37 | $22.40 | $2,240.00 | 75 |
| JNJ | 13 | $151.96 | $152.75 | $1,985.75 | 65 |
| JPM | 7 | $285.02 | $289.91 | $2,029.37 | 65 |
| KO | 28 | $70.48 | $70.75 | $1,981.00 | 65 |
| LLY | 3 | $767.33 | $779.53 | $2,338.59 | 65 |
| MA | 4 | $537.87 | $561.94 | $2,247.76 | 65 |
| META | 3 | $712.71 | $738.09 | $2,214.27 | 90 |
| MRK | 25 | $78.92 | $79.16 | $1,979.00 | 65 |
| MSFT | 4 | $492.89 | $497.41 | $1,989.64 | 75 |
| NFLX | 1 | $1,334.07 | $1,339.13 | $1,339.13 | 65 |
| NKE | 36 | $71.18 | $71.04 | $2,557.44 | 85 |
| NVDA | 13 | $157.77 | $157.99 | $2,053.87 | 65 |
| ORCL | 9 | $219.56 | $218.63 | $1,967.67 | 65 |
| PEP | 17 | $131.85 | $132.04 | $2,244.68 | 75 |
| PFE | 93 | $24.27 | $24.24 | $2,254.32 | 75 |
| PG | 12 | $159.73 | $159.32 | $1,911.84 | 65 |
| PYPL | 34 | $73.92 | $74.32 | $2,526.88 | 85 |
| QCOM | 16 | $159.24 | $159.26 | $2,548.16 | 85 |
| T | 88 | $28.54 | $28.94 | $2,546.72 | 85 |
| TGT | 23 | $98.82 | $98.65 | $2,268.95 | 75 |
| TSLA | 7 | $320.69 | $317.66 | $2,223.62 | 65 |
| UNH | 8 | $306.63 | $311.97 | $2,495.76 | 80 |
| UNP | 11 | $232.22 | $230.08 | $2,530.88 | 85 |
| V | 7 | $346.39 | $355.05 | $2,485.35 | 85 |
| VZ | 45 | $42.64 | $43.27 | $1,947.15 | 65 |
| WFC | 32 | $79.91 | $80.12 | $2,563.84 | 85 |
| WMT | 26 | $97.15 | $97.78 | $2,542.28 | 85 |
| XOM | 18 | $109.40 | $107.80 | $1,940.40 | 65 |

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
| 2025-07-01 12:05:23 | SELL | MRK | 3 | $79.16 | $0.64 | 65 |
| 2025-07-01 12:05:23 | SELL | CSCO | 1 | $69.38 | $0.44 | 65 |
| 2025-07-01 12:05:23 | SELL | VZ | 7 | $43.27 | $3.80 | 65 |
| 2025-07-01 12:05:23 | BUY | V | 1 | $355.05 | N/A | 85 |
| 2025-07-01 11:53:49 | SELL | C | 3 | $85.12 | $2.54 | 65 |
| 2025-07-01 11:53:49 | BUY | INTC | 12 | $22.40 | N/A | 75 |
| 2025-07-01 11:44:19 | SELL | BAC | 11 | $47.32 | $1.07 | 65 |
| 2025-07-01 11:44:19 | BUY | C | 3 | $85.12 | N/A | 75 |
| 2025-07-01 11:44:19 | BUY | VZ | 7 | $43.27 | N/A | 75 |
| 2025-07-01 11:35:43 | SELL | C | 4 | $85.12 | $3.26 | 65 |
| 2025-07-01 11:35:43 | SELL | VZ | 7 | $43.27 | $3.80 | 65 |
| 2025-07-01 11:35:43 | SELL | T | 1 | $28.94 | $0.39 | 85 |
| 2025-07-01 11:35:43 | BUY | UNH | 1 | $311.97 | N/A | 85 |
| 2025-07-01 11:35:43 | BUY | BAC | 11 | $47.32 | N/A | 85 |
| 2025-07-01 11:27:17 | SELL | UNH | 1 | $311.97 | $5.34 | 65 |
| 2025-07-01 11:27:17 | SELL | C | 2 | $85.12 | $1.52 | 75 |
| 2025-07-01 11:27:17 | BUY | MRK | 3 | $79.16 | N/A | 75 |
| 2025-07-01 11:27:17 | BUY | BA | 1 | $209.53 | N/A | 75 |
| 2025-07-01 11:27:17 | BUY | VZ | 1 | $43.27 | N/A | 75 |
| 2025-07-01 11:16:37 | SELL | INTC | 13 | $22.40 | $0.42 | 65 |
| 2025-07-01 11:16:37 | SELL | MRK | 3 | $79.16 | $0.64 | 65 |
| 2025-07-01 11:16:37 | SELL | CSCO | 3 | $69.38 | $1.21 | 65 |
| 2025-07-01 11:16:37 | BUY | C | 5 | $85.12 | N/A | 85 |
| 2025-07-01 11:16:37 | BUY | VZ | 6 | $43.27 | N/A | 75 |
| 2025-07-01 11:03:44 | SELL | BAC | 11 | $47.32 | $1.07 | 65 |

<!--TRADE_LOG_END--> 
