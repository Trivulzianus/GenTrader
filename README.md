# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 12:59:13**

| Metric | Value |
|---|---|
| **Total Value** | **$100,340.42** |
| Cash | $185.00 |
| Holdings Value | $100,155.42 |

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
| BAC | 41 | $47.19 | $47.32 | $1,940.12 | 65 |
| C | 23 | $84.16 | $85.12 | $1,957.76 | 85 |
| CAT | 5 | $381.20 | $388.21 | $1,941.05 | 65 |
| COST | 2 | $991.47 | $989.94 | $1,979.88 | 65 |
| CRM | 9 | $274.67 | $272.69 | $2,454.21 | 75 |
| CSCO | 32 | $68.98 | $69.38 | $2,220.16 | 75 |
| CVX | 13 | $143.34 | $143.19 | $1,861.47 | 65 |
| DIS | 16 | $122.90 | $124.01 | $1,984.16 | 65 |
| GOOGL | 15 | $178.80 | $176.23 | $2,643.45 | 85 |
| GS | 3 | $706.65 | $707.75 | $2,123.25 | 75 |
| HD | 6 | $370.25 | $366.64 | $2,199.84 | 85 |
| INTC | 99 | $22.37 | $22.40 | $2,217.60 | 75 |
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
| UNH | 8 | $306.63 | $311.97 | $2,495.76 | 85 |
| UNP | 11 | $232.22 | $230.08 | $2,530.88 | 85 |
| V | 7 | $346.39 | $355.05 | $2,485.35 | 85 |
| VZ | 52 | $42.73 | $43.27 | $2,250.04 | 75 |
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
| 2025-07-01 12:59:03 | SELL | BAC | 1 | $47.32 | $0.12 | 65 |
| 2025-07-01 12:59:03 | SELL | PFE | 1 | $24.24 | $-0.03 | 75 |
| 2025-07-01 12:59:03 | SELL | MRK | 1 | $79.16 | $0.23 | 65 |
| 2025-07-01 12:59:03 | SELL | VZ | 1 | $43.27 | $0.53 | 75 |
| 2025-07-01 12:59:03 | SELL | T | 1 | $28.94 | $0.39 | 85 |
| 2025-07-01 12:59:03 | BUY | V | 1 | $355.05 | N/A | 85 |
| 2025-07-01 12:59:03 | BUY | INTC | 11 | $22.40 | N/A | 75 |
| 2025-07-01 12:59:03 | BUY | CSCO | 4 | $69.38 | N/A | 75 |
| 2025-07-01 12:34:29 | SELL | V | 1 | $355.05 | $8.66 | 65 |
| 2025-07-01 12:34:29 | SELL | HD | 1 | $366.64 | $-3.09 | 65 |
| 2025-07-01 12:34:29 | SELL | MRK | 6 | $79.16 | $1.12 | 65 |
| 2025-07-01 12:34:29 | BUY | INTC | 1 | $22.40 | N/A | 65 |
| 2025-07-01 12:34:29 | BUY | PFE | 1 | $24.24 | N/A | 75 |
| 2025-07-01 12:34:29 | BUY | T | 1 | $28.94 | N/A | 85 |
| 2025-07-01 12:34:29 | BUY | VZ | 8 | $43.27 | N/A | 75 |
| 2025-07-01 12:18:24 | SELL | INTC | 13 | $22.40 | $0.43 | 65 |
| 2025-07-01 12:18:24 | BUY | MRK | 7 | $79.16 | N/A | 85 |
| 2025-07-01 12:05:23 | SELL | MRK | 3 | $79.16 | $0.64 | 65 |
| 2025-07-01 12:05:23 | SELL | CSCO | 1 | $69.38 | $0.44 | 65 |
| 2025-07-01 12:05:23 | SELL | VZ | 7 | $43.27 | $3.80 | 65 |
| 2025-07-01 12:05:23 | BUY | V | 1 | $355.05 | N/A | 85 |
| 2025-07-01 11:53:49 | SELL | C | 3 | $85.12 | $2.54 | 65 |
| 2025-07-01 11:53:49 | BUY | INTC | 12 | $22.40 | N/A | 75 |
| 2025-07-01 11:44:19 | SELL | BAC | 11 | $47.32 | $1.07 | 65 |
| 2025-07-01 11:44:19 | BUY | C | 3 | $85.12 | N/A | 75 |

<!--TRADE_LOG_END--> 
