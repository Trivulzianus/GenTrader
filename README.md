# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-06-30 19:53:49**

| Metric | Value |
|---|---|
| **Total Value** | **$100,439.72** |
| Cash | $103.13 |
| Holdings Value | $100,336.59 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $206.44 | $2,477.29 | 85 |
| ADBE | 6 | $385.97 | $387.05 | $2,322.30 | 65 |
| AMD | 14 | $142.83 | $142.03 | $1,988.42 | 65 |
| AMZN | 9 | $227.61 | $219.34 | $1,974.08 | 65 |
| AVGO | 7 | $276.11 | $274.86 | $1,924.02 | 65 |
| AXP | 7 | $316.34 | $319.09 | $2,233.63 | 65 |
| BA | 10 | $214.55 | $209.36 | $2,093.60 | 65 |
| BAC | 42 | $47.22 | $47.27 | $1,985.34 | 65 |
| C | 30 | $84.38 | $85.09 | $2,552.70 | 85 |
| CAT | 5 | $381.20 | $388.62 | $1,943.08 | 65 |
| COST | 2 | $991.47 | $990.74 | $1,981.47 | 65 |
| CRM | 8 | $274.92 | $272.39 | $2,179.12 | 75 |
| CSCO | 29 | $68.91 | $69.33 | $2,010.43 | 65 |
| CVX | 13 | $143.34 | $143.22 | $1,861.86 | 65 |
| DIS | 16 | $122.92 | $124.14 | $1,986.16 | 65 |
| GOOGL | 15 | $178.80 | $176.16 | $2,642.40 | 85 |
| GS | 3 | $706.65 | $708.15 | $2,124.45 | 75 |
| HD | 6 | $370.25 | $367.02 | $2,202.12 | 75 |
| INTC | 87 | $22.36 | $22.49 | $1,956.63 | 65 |
| JNJ | 13 | $151.96 | $152.74 | $1,985.62 | 65 |
| JPM | 7 | $285.02 | $290.00 | $2,030.00 | 65 |
| KO | 28 | $70.48 | $70.76 | $1,981.28 | 65 |
| LLY | 3 | $767.33 | $779.38 | $2,338.15 | 65 |
| MA | 4 | $537.87 | $562.23 | $2,248.92 | 75 |
| META | 3 | $712.71 | $739.37 | $2,218.11 | 85 |
| MRK | 25 | $78.92 | $79.22 | $1,980.50 | 65 |
| MSFT | 4 | $492.89 | $499.83 | $1,999.34 | 75 |
| NFLX | 1 | $1,334.07 | $1,337.32 | $1,337.32 | 65 |
| NKE | 36 | $71.18 | $70.98 | $2,555.28 | 85 |
| NVDA | 16 | $157.81 | $158.42 | $2,534.72 | 85 |
| ORCL | 9 | $219.56 | $219.21 | $1,972.89 | 65 |
| PEP | 17 | $131.85 | $132.23 | $2,247.91 | 75 |
| PFE | 93 | $24.27 | $24.30 | $2,260.36 | 75 |
| PG | 12 | $159.73 | $159.55 | $1,914.60 | 65 |
| PYPL | 35 | $73.94 | $74.36 | $2,602.60 | 85 |
| QCOM | 16 | $159.24 | $159.32 | $2,549.12 | 85 |
| T | 88 | $28.54 | $29.01 | $2,552.88 | 85 |
| TGT | 23 | $98.82 | $99.01 | $2,277.23 | 75 |
| TSLA | 7 | $320.69 | $318.46 | $2,229.25 | 75 |
| UNH | 7 | $305.88 | $311.30 | $2,179.07 | 75 |
| UNP | 12 | $232.04 | $230.28 | $2,763.30 | 85 |
| V | 6 | $344.95 | $355.24 | $2,131.44 | 65 |
| VZ | 45 | $42.64 | $43.30 | $1,948.72 | 65 |
| WFC | 32 | $79.91 | $80.19 | $2,566.24 | 85 |
| WMT | 26 | $97.15 | $98.09 | $2,550.34 | 85 |
| XOM | 18 | $109.40 | $107.91 | $1,942.29 | 65 |

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
| 2025-06-30 19:53:35 | SELL | BAC | 12 | $47.21 | $566.52 | 65 |
| 2025-06-30 19:53:35 | BUY | C | 7 | $85.06 | $595.39 | 85 |
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

<!--TRADE_LOG_END--> 
