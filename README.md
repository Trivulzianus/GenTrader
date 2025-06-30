# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-06-30 19:51:24**

| Metric | Value |
|---|---|
| **Total Value** | **$100,404.82** |
| Cash | $132.00 |
| Holdings Value | $100,272.82 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $206.17 | $2,474.04 | 85 |
| ADBE | 6 | $385.97 | $387.10 | $2,322.60 | 65 |
| AMD | 14 | $142.83 | $141.89 | $1,986.46 | 65 |
| AMZN | 9 | $227.61 | $219.47 | $1,975.23 | 65 |
| AVGO | 7 | $276.11 | $274.78 | $1,923.46 | 65 |
| AXP | 7 | $316.34 | $318.85 | $2,231.91 | 65 |
| BA | 10 | $214.55 | $209.37 | $2,093.70 | 65 |
| BAC | 54 | $47.22 | $47.20 | $2,549.07 | 85 |
| C | 23 | $84.18 | $85.03 | $1,955.80 | 85 |
| CAT | 5 | $381.20 | $388.52 | $1,942.60 | 65 |
| COST | 2 | $991.47 | $989.60 | $1,979.19 | 65 |
| CRM | 8 | $274.92 | $272.28 | $2,178.24 | 75 |
| CSCO | 29 | $68.91 | $69.28 | $2,009.26 | 65 |
| CVX | 13 | $143.34 | $143.20 | $1,861.60 | 65 |
| DIS | 16 | $122.92 | $124.08 | $1,985.28 | 65 |
| GOOGL | 15 | $178.80 | $176.41 | $2,646.15 | 85 |
| GS | 3 | $706.65 | $708.43 | $2,125.29 | 85 |
| HD | 6 | $370.25 | $367.01 | $2,202.09 | 75 |
| INTC | 87 | $22.36 | $22.50 | $1,957.93 | 65 |
| JNJ | 13 | $151.96 | $152.66 | $1,984.58 | 65 |
| JPM | 7 | $285.02 | $289.96 | $2,029.72 | 65 |
| KO | 28 | $70.48 | $70.70 | $1,979.60 | 65 |
| LLY | 3 | $767.33 | $778.81 | $2,336.43 | 65 |
| MA | 4 | $537.87 | $561.96 | $2,247.82 | 65 |
| META | 3 | $712.71 | $738.66 | $2,215.98 | 85 |
| MRK | 25 | $78.92 | $79.21 | $1,980.25 | 65 |
| MSFT | 4 | $492.89 | $499.44 | $1,997.76 | 65 |
| NFLX | 1 | $1,334.07 | $1,335.54 | $1,335.54 | 65 |
| NKE | 36 | $71.18 | $70.98 | $2,555.46 | 85 |
| NVDA | 16 | $157.81 | $158.40 | $2,534.40 | 85 |
| ORCL | 9 | $219.56 | $219.42 | $1,974.78 | 65 |
| PEP | 17 | $131.85 | $132.22 | $2,247.66 | 75 |
| PFE | 93 | $24.27 | $24.30 | $2,259.90 | 75 |
| PG | 12 | $159.73 | $159.47 | $1,913.64 | 65 |
| PYPL | 35 | $73.94 | $74.33 | $2,601.55 | 85 |
| QCOM | 16 | $159.24 | $159.15 | $2,546.40 | 85 |
| T | 88 | $28.54 | $28.95 | $2,548.04 | 85 |
| TGT | 23 | $98.82 | $99.01 | $2,277.23 | 75 |
| TSLA | 7 | $320.69 | $318.21 | $2,227.45 | 65 |
| UNH | 7 | $305.88 | $311.82 | $2,182.74 | 65 |
| UNP | 12 | $232.04 | $230.32 | $2,763.84 | 85 |
| V | 6 | $344.95 | $355.05 | $2,130.30 | 65 |
| VZ | 45 | $42.64 | $43.23 | $1,945.12 | 65 |
| WFC | 32 | $79.91 | $80.17 | $2,565.60 | 85 |
| WMT | 26 | $97.15 | $98.01 | $2,548.26 | 85 |
| XOM | 18 | $109.40 | $107.94 | $1,942.84 | 65 |

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
| Timestamp | Action | Symbol | Shares | Price | Total | Confidence |
|---|---|---|---|---|---|---|
| 2025-06-30 19:46:44 | SELL | VZ | 1 | $43.18 | $43.18 | 65 |
| 2025-06-30 19:46:44 | SELL | T | 1 | $28.93 | $28.93 | 85 |
| 2025-06-30 19:39:40 | SELL | MSFT | 1 | $498.41 | $498.41 | 65 |
| 2025-06-30 19:39:40 | SELL | UNH | 1 | $311.05 | $311.05 | 65 |
| 2025-06-30 19:39:40 | BUY | AAPL | 2 | $206.65 | $413.31 | 85 |
| 2025-06-30 19:39:40 | BUY | BAC | 11 | $47.10 | $518.15 | 85 |
| 2025-06-30 19:04:19 | SELL | INTC | 1 | $22.44 | $22.44 | 65 |
| 2025-06-30 19:04:19 | SELL | XOM | 1 | $108.08 | $108.08 | 65 |
| 2025-06-30 19:04:19 | SELL | PFE | 1 | $24.20 | $24.20 | 75 |
| 2025-06-30 19:04:19 | SELL | C | 1 | $85.21 | $85.21 | 65 |
| 2025-06-30 19:04:19 | SELL | CAT | 1 | $389.02 | $389.02 | 65 |
| 2025-06-30 19:04:19 | SELL | T | 1 | $28.65 | $28.65 | 85 |
| 2025-06-30 19:04:19 | BUY | MSFT | 1 | $498.74 | $498.74 | 85 |
| 2025-06-30 18:48:29 | SELL | BAC | 11 | $47.17 | $518.87 | 65 |
| 2025-06-30 18:48:29 | SELL | XOM | 4 | $108.18 | $432.72 | 65 |
| 2025-06-30 18:48:29 | BUY | AMD | 1 | $141.62 | $141.62 | 65 |
| 2025-06-30 18:48:29 | BUY | PYPL | 4 | $74.01 | $296.04 | 85 |
| 2025-06-30 18:48:29 | BUY | T | 80 | $28.60 | $2,288.40 | 85 |
| 2025-06-30 18:32:58 | SELL | AMZN | 2 | $219.42 | $438.84 | 65 |
| 2025-06-30 18:32:58 | SELL | AAPL | 1 | $200.24 | $200.24 | 65 |
| 2025-06-30 18:32:58 | SELL | PYPL | 4 | $74.05 | $296.20 | 75 |
| 2025-06-30 18:32:58 | SELL | COST | 1 | $984.27 | $984.27 | 65 |
| 2025-06-30 18:32:58 | BUY | NVDA | 3 | $157.37 | $472.10 | 85 |
| 2025-06-30 18:32:58 | BUY | XOM | 4 | $109.38 | $437.52 | 85 |
| 2025-06-30 18:17:46 | SELL | NVDA | 3 | $157.63 | $472.88 | 65 |

<!--TRADE_LOG_END--> 
