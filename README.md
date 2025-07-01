# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 13:49:03**

| Metric | Value |
|---|---|
| **Total Value** | **$100,309.66** |
| Cash | $239.91 |
| Holdings Value | $100,069.75 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.42 | $2,501.04 | 85 |
| ADBE | 5 | $385.76 | $382.20 | $1,911.02 | 65 |
| AMD | 16 | $142.46 | $139.09 | $2,225.44 | 75 |
| AMZN | 11 | $226.76 | $219.62 | $2,415.77 | 85 |
| AVGO | 7 | $276.11 | $271.34 | $1,899.38 | 85 |
| AXP | 7 | $316.33 | $319.20 | $2,234.40 | 65 |
| BA | 10 | $214.55 | $211.44 | $2,114.40 | 65 |
| BAC | 41 | $47.19 | $47.47 | $1,946.07 | 85 |
| C | 23 | $84.14 | $85.23 | $1,960.40 | 65 |
| CAT | 5 | $381.20 | $384.42 | $1,922.10 | 65 |
| COST | 2 | $991.47 | $990.86 | $1,981.71 | 65 |
| CRM | 9 | $274.67 | $270.90 | $2,438.10 | 75 |
| CSCO | 31 | $68.96 | $69.16 | $2,143.80 | 75 |
| CVX | 13 | $143.34 | $142.94 | $1,858.22 | 65 |
| DIS | 16 | $122.90 | $123.71 | $1,979.40 | 65 |
| GOOGL | 15 | $178.80 | $174.50 | $2,617.50 | 85 |
| GS | 3 | $706.65 | $711.22 | $2,133.66 | 75 |
| HD | 6 | $370.25 | $367.02 | $2,202.15 | 85 |
| INTC | 86 | $22.34 | $22.39 | $1,925.11 | 65 |
| JNJ | 13 | $151.96 | $153.42 | $1,994.46 | 65 |
| JPM | 7 | $285.02 | $290.38 | $2,032.69 | 65 |
| KO | 27 | $70.44 | $71.53 | $1,931.31 | 65 |
| LLY | 3 | $767.33 | $781.39 | $2,344.18 | 65 |
| MA | 4 | $537.87 | $560.22 | $2,240.88 | 65 |
| META | 3 | $712.71 | $733.69 | $2,201.07 | 90 |
| MRK | 25 | $78.93 | $79.08 | $1,977.00 | 65 |
| MSFT | 4 | $492.89 | $497.24 | $1,988.96 | 65 |
| NFLX | 1 | $1,334.07 | $1,333.08 | $1,333.08 | 65 |
| NKE | 35 | $71.14 | $73.06 | $2,557.10 | 85 |
| NVDA | 16 | $157.57 | $156.17 | $2,498.75 | 85 |
| ORCL | 9 | $219.56 | $221.31 | $1,991.79 | 65 |
| PEP | 17 | $131.85 | $133.44 | $2,268.48 | 75 |
| PFE | 91 | $24.27 | $24.39 | $2,219.91 | 75 |
| PG | 12 | $159.73 | $160.03 | $1,920.36 | 65 |
| PYPL | 34 | $73.92 | $74.19 | $2,522.46 | 85 |
| QCOM | 16 | $159.24 | $158.18 | $2,530.88 | 85 |
| T | 87 | $28.54 | $28.94 | $2,517.77 | 85 |
| TGT | 23 | $98.82 | $100.54 | $2,312.42 | 75 |
| TSLA | 7 | $294.26 | $298.58 | $2,090.06 | 65 |
| UNH | 8 | $306.63 | $314.93 | $2,519.40 | 85 |
| UNP | 11 | $232.22 | $230.71 | $2,537.76 | 85 |
| V | 6 | $344.95 | $352.74 | $2,116.44 | 75 |
| VZ | 45 | $42.64 | $43.27 | $1,947.38 | 65 |
| WFC | 32 | $79.91 | $80.35 | $2,571.20 | 85 |
| WMT | 26 | $97.15 | $98.51 | $2,561.26 | 85 |
| XOM | 18 | $109.40 | $107.39 | $1,933.02 | 65 |

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
| 2025-07-01 13:17:39 | BUY | MRK | 3 | $79.16 | N/A | 75 |
| 2025-07-01 13:17:39 | BUY | C | 3 | $85.12 | N/A | 75 |
| 2025-07-01 12:59:03 | SELL | BAC | 1 | $47.32 | $0.12 | 65 |
| 2025-07-01 12:59:03 | SELL | PFE | 1 | $24.24 | $-0.03 | 75 |

<!--TRADE_LOG_END--> 
