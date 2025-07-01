# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 13:33:02**

| Metric | Value |
|---|---|
| **Total Value** | **$100,166.83** |
| Cash | $47.64 |
| Holdings Value | $100,119.19 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $206.41 | $2,476.98 | 85 |
| ADBE | 5 | $385.76 | $383.08 | $1,915.42 | 65 |
| AMD | 17 | $142.25 | $139.62 | $2,373.52 | 85 |
| AMZN | 11 | $226.76 | $219.30 | $2,412.31 | 85 |
| AVGO | 7 | $276.11 | $273.41 | $1,913.87 | 65 |
| AXP | 7 | $316.33 | $317.54 | $2,222.75 | 85 |
| BA | 10 | $214.55 | $209.70 | $2,097.01 | 65 |
| BAC | 41 | $47.19 | $47.31 | $1,939.71 | 65 |
| C | 23 | $84.14 | $85.23 | $1,960.29 | 65 |
| CAT | 5 | $381.20 | $386.85 | $1,934.25 | 65 |
| COST | 2 | $991.47 | $993.00 | $1,986.00 | 65 |
| CRM | 9 | $274.67 | $271.78 | $2,446.02 | 85 |
| CSCO | 28 | $68.92 | $69.51 | $1,946.28 | 65 |
| CVX | 13 | $143.34 | $143.36 | $1,863.68 | 65 |
| DIS | 16 | $122.90 | $123.29 | $1,972.64 | 65 |
| GOOGL | 15 | $178.80 | $174.97 | $2,624.55 | 85 |
| GS | 3 | $706.65 | $708.64 | $2,125.92 | 65 |
| HD | 6 | $370.25 | $364.31 | $2,185.85 | 85 |
| INTC | 86 | $22.34 | $22.54 | $1,938.01 | 65 |
| JNJ | 13 | $151.96 | $153.07 | $1,989.97 | 65 |
| JPM | 7 | $285.02 | $290.25 | $2,031.75 | 65 |
| KO | 27 | $70.44 | $71.36 | $1,926.85 | 65 |
| LLY | 3 | $767.33 | $777.62 | $2,332.86 | 65 |
| MA | 4 | $537.87 | $557.26 | $2,229.04 | 65 |
| META | 3 | $712.71 | $732.40 | $2,197.20 | 90 |
| MRK | 28 | $78.95 | $78.65 | $2,202.20 | 75 |
| MSFT | 4 | $492.89 | $497.21 | $1,988.86 | 65 |
| NFLX | 1 | $1,334.07 | $1,332.18 | $1,332.18 | 65 |
| NKE | 35 | $71.14 | $72.69 | $2,544.15 | 85 |
| NVDA | 16 | $157.57 | $156.87 | $2,509.92 | 85 |
| ORCL | 9 | $219.56 | $220.93 | $1,988.37 | 65 |
| PEP | 17 | $131.85 | $133.00 | $2,261.09 | 75 |
| PFE | 92 | $24.27 | $24.30 | $2,235.60 | 75 |
| PG | 12 | $159.73 | $159.42 | $1,913.04 | 65 |
| PYPL | 34 | $73.92 | $74.06 | $2,518.04 | 85 |
| QCOM | 16 | $159.24 | $158.83 | $2,541.21 | 85 |
| T | 87 | $28.54 | $29.07 | $2,529.09 | 85 |
| TGT | 23 | $98.82 | $99.35 | $2,285.05 | 75 |
| TSLA | 7 | $294.26 | $295.64 | $2,069.48 | 75 |
| UNH | 8 | $306.63 | $312.52 | $2,500.20 | 85 |
| UNP | 11 | $232.22 | $230.00 | $2,530.05 | 85 |
| V | 6 | $344.95 | $351.63 | $2,109.78 | 75 |
| VZ | 45 | $42.64 | $43.41 | $1,953.45 | 65 |
| WFC | 32 | $79.91 | $80.16 | $2,565.12 | 85 |
| WMT | 26 | $97.15 | $98.26 | $2,554.84 | 85 |
| XOM | 18 | $109.40 | $108.04 | $1,944.72 | 65 |

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
| 2025-07-01 13:17:39 | BUY | MRK | 3 | $79.16 | N/A | 75 |
| 2025-07-01 13:17:39 | BUY | C | 3 | $85.12 | N/A | 75 |
| 2025-07-01 12:59:03 | SELL | BAC | 1 | $47.32 | $0.12 | 65 |
| 2025-07-01 12:59:03 | SELL | PFE | 1 | $24.24 | $-0.03 | 75 |
| 2025-07-01 12:59:03 | SELL | MRK | 1 | $79.16 | $0.23 | 65 |
| 2025-07-01 12:59:03 | SELL | VZ | 1 | $43.27 | $0.53 | 75 |
| 2025-07-01 12:59:03 | SELL | T | 1 | $28.94 | $0.39 | 85 |
| 2025-07-01 12:59:03 | BUY | V | 1 | $355.05 | N/A | 85 |

<!--TRADE_LOG_END--> 
