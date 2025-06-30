# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-06-30 19:04:25**

| Metric | Value |
|---|---|
| **Total Value** | **$100,194.46** |
| Cash | $181.88 |
| Holdings Value | $100,012.58 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $200.21 | $202.82 | $2,028.15 | 85 |
| ADBE | 6 | $385.97 | $387.02 | $2,322.12 | 65 |
| AMD | 14 | $142.83 | $141.88 | $1,986.32 | 65 |
| AMZN | 9 | $227.61 | $219.91 | $1,979.19 | 85 |
| AVGO | 7 | $276.11 | $274.27 | $1,919.92 | 65 |
| AXP | 7 | $316.34 | $318.88 | $2,232.16 | 65 |
| BA | 10 | $214.55 | $208.81 | $2,088.10 | 65 |
| BAC | 43 | $47.25 | $47.23 | $2,031.11 | 85 |
| C | 23 | $84.18 | $85.19 | $1,959.37 | 65 |
| CAT | 5 | $381.20 | $389.02 | $1,945.12 | 65 |
| COST | 2 | $991.47 | $986.31 | $1,972.62 | 65 |
| CRM | 8 | $274.92 | $271.69 | $2,173.52 | 65 |
| CSCO | 29 | $68.91 | $69.08 | $2,003.18 | 65 |
| CVX | 13 | $143.34 | $142.99 | $1,858.87 | 65 |
| DIS | 16 | $122.92 | $123.89 | $1,982.24 | 65 |
| GOOGL | 15 | $178.80 | $176.56 | $2,648.47 | 85 |
| GS | 3 | $706.65 | $706.26 | $2,118.78 | 75 |
| HD | 6 | $370.25 | $366.43 | $2,198.58 | 85 |
| INTC | 87 | $22.36 | $22.44 | $1,952.28 | 65 |
| JNJ | 13 | $151.96 | $151.84 | $1,973.92 | 65 |
| JPM | 7 | $285.02 | $290.22 | $2,031.54 | 65 |
| KO | 28 | $70.48 | $70.47 | $1,973.02 | 65 |
| LLY | 3 | $767.33 | $778.14 | $2,334.42 | 65 |
| MA | 4 | $537.87 | $560.58 | $2,242.32 | 65 |
| META | 3 | $712.71 | $737.14 | $2,211.42 | 85 |
| MRK | 25 | $78.92 | $79.04 | $1,976.00 | 65 |
| MSFT | 5 | $494.00 | $498.71 | $2,493.55 | 85 |
| NFLX | 1 | $1,334.07 | $1,341.00 | $1,341.00 | 65 |
| NKE | 36 | $71.18 | $70.64 | $2,543.04 | 85 |
| NVDA | 16 | $157.81 | $157.89 | $2,526.22 | 85 |
| ORCL | 9 | $219.56 | $220.80 | $1,987.24 | 65 |
| PEP | 17 | $131.85 | $131.78 | $2,240.29 | 75 |
| PFE | 93 | $24.27 | $24.20 | $2,250.60 | 75 |
| PG | 12 | $159.73 | $158.71 | $1,904.52 | 65 |
| PYPL | 35 | $73.94 | $74.11 | $2,594.02 | 85 |
| QCOM | 16 | $159.24 | $158.95 | $2,543.20 | 85 |
| T | 89 | $28.55 | $28.65 | $2,549.71 | 85 |
| TGT | 23 | $98.82 | $98.59 | $2,267.57 | 75 |
| TSLA | 7 | $320.69 | $319.15 | $2,234.05 | 65 |
| UNH | 8 | $306.52 | $310.99 | $2,487.88 | 85 |
| UNP | 12 | $232.04 | $230.34 | $2,764.14 | 85 |
| V | 6 | $344.95 | $353.94 | $2,123.64 | 65 |
| VZ | 46 | $42.65 | $42.90 | $1,973.17 | 65 |
| WFC | 32 | $79.91 | $80.24 | $2,567.68 | 85 |
| WMT | 26 | $97.15 | $97.42 | $2,533.05 | 85 |
| XOM | 18 | $109.40 | $108.07 | $1,945.26 | 65 |

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
| 2025-06-30 18:17:46 | SELL | C | 6 | $84.86 | $509.13 | 65 |
| 2025-06-30 18:17:46 | BUY | AAPL | 2 | $200.51 | $401.02 | 75 |
| 2025-06-30 18:17:46 | BUY | NKE | 1 | $70.78 | $70.78 | 85 |
| 2025-06-30 18:17:46 | BUY | PFE | 13 | $24.17 | $314.21 | 75 |
| 2025-06-30 18:04:47 | SELL | PFE | 13 | $24.17 | $314.15 | 65 |
| 2025-06-30 18:04:47 | BUY | WMT | 2 | $96.88 | $193.75 | 85 |

<!--TRADE_LOG_END--> 
