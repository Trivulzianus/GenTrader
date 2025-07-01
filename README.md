# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 17:30:10**

| Metric | Value |
|---|---|
| **Total Value** | **$101,117.06** |
| Cash | $136.51 |
| Holdings Value | $100,980.55 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.12 | $2,497.50 | 85 |
| ADBE | 5 | $385.76 | $390.92 | $1,954.58 | 75 |
| AMD | 17 | $140.02 | $137.06 | $2,330.02 | 85 |
| AMZN | 11 | $226.78 | $220.68 | $2,427.45 | 85 |
| AVGO | 9 | $272.95 | $265.96 | $2,393.68 | 85 |
| AXP | 6 | $315.94 | $323.85 | $1,943.10 | 65 |
| BA | 9 | $215.30 | $209.74 | $1,887.66 | 65 |
| BAC | 51 | $47.30 | $48.18 | $2,457.14 | 85 |
| C | 22 | $84.03 | $86.25 | $1,897.39 | 65 |
| CAT | 5 | $381.20 | $391.75 | $1,958.75 | 65 |
| COST | 2 | $991.47 | $984.95 | $1,969.90 | 75 |
| CRM | 8 | $274.90 | $273.31 | $2,186.48 | 75 |
| CSCO | 28 | $68.85 | $69.03 | $1,932.70 | 65 |
| CVX | 17 | $143.81 | $145.45 | $2,472.62 | 85 |
| DIS | 16 | $122.87 | $123.41 | $1,974.56 | 65 |
| GOOGL | 14 | $175.62 | $175.19 | $2,452.73 | 85 |
| GS | 3 | $706.65 | $708.21 | $2,124.64 | 65 |
| HD | 7 | $369.90 | $376.16 | $2,633.12 | 85 |
| INTC | 82 | $22.23 | $23.01 | $1,886.83 | 65 |
| JNJ | 12 | $151.63 | $155.41 | $1,864.87 | 65 |
| JPM | 7 | $285.02 | $289.95 | $2,029.64 | 65 |
| KO | 26 | $70.42 | $71.54 | $1,860.04 | 65 |
| LLY | 3 | $767.33 | $781.08 | $2,343.25 | 65 |
| MA | 4 | $537.87 | $564.37 | $2,257.48 | 65 |
| META | 3 | $712.71 | $720.14 | $2,160.43 | 85 |
| MRK | 30 | $79.35 | $81.92 | $2,457.60 | 85 |
| MSFT | 4 | $492.89 | $493.25 | $1,973.02 | 65 |
| NFLX | 1 | $1,334.07 | $1,296.91 | $1,296.91 | 85 |
| NKE | 33 | $70.93 | $73.09 | $2,411.97 | 85 |
| NVDA | 15 | $153.89 | $154.25 | $2,313.77 | 85 |
| ORCL | 9 | $219.56 | $220.04 | $1,980.33 | 65 |
| PEP | 16 | $131.60 | $134.71 | $2,155.36 | 75 |
| PFE | 99 | $24.30 | $24.98 | $2,472.90 | 85 |
| PG | 12 | $159.73 | $160.73 | $1,928.76 | 65 |
| PYPL | 32 | $73.86 | $75.51 | $2,416.32 | 85 |
| QCOM | 15 | $159.12 | $160.16 | $2,402.40 | 85 |
| T | 85 | $28.52 | $28.80 | $2,448.43 | 85 |
| TGT | 21 | $98.42 | $104.15 | $2,187.15 | 75 |
| TSLA | 7 | $290.03 | $302.15 | $2,115.05 | 65 |
| UNH | 8 | $306.63 | $322.41 | $2,579.28 | 85 |
| UNP | 11 | $232.22 | $235.40 | $2,589.40 | 85 |
| V | 6 | $344.95 | $355.87 | $2,135.22 | 85 |
| VZ | 44 | $42.61 | $43.65 | $1,920.38 | 65 |
| WFC | 30 | $79.85 | $81.36 | $2,440.95 | 85 |
| WMT | 25 | $97.07 | $98.30 | $2,457.38 | 85 |
| XOM | 22 | $109.38 | $109.16 | $2,401.42 | 85 |

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
| 2025-07-01 17:30:00 | SELL | INTC | 1 | $23.02 | $0.79 | 65 |
| 2025-07-01 17:30:00 | SELL | CSCO | 4 | $69.02 | $0.61 | 65 |
| 2025-07-01 17:30:00 | SELL | VZ | 6 | $43.63 | $5.43 | 65 |
| 2025-07-01 17:30:00 | BUY | AMD | 1 | $137.02 | N/A | 85 |
| 2025-07-01 17:30:00 | BUY | AVGO | 2 | $266.08 | N/A | 85 |
| 2025-07-01 17:17:09 | SELL | C | 3 | $86.17 | $5.64 | 65 |
| 2025-07-01 17:17:09 | BUY | XOM | 4 | $108.92 | N/A | 85 |
| 2025-07-01 17:06:51 | SELL | AMD | 1 | $137.57 | $-2.48 | 75 |
| 2025-07-01 17:06:51 | SELL | DIS | 4 | $123.20 | $1.06 | 65 |
| 2025-07-01 17:06:51 | SELL | CSCO | 3 | $68.96 | $0.23 | 75 |
| 2025-07-01 17:06:51 | BUY | NVDA | 3 | $154.74 | N/A | 85 |
| 2025-07-01 17:06:51 | BUY | C | 3 | $85.82 | N/A | 75 |
| 2025-07-01 16:57:52 | SELL | NVDA | 4 | $157.99 | $12.93 | 65 |
| 2025-07-01 16:57:52 | SELL | CRM | 1 | $272.54 | $-2.10 | 75 |
| 2025-07-01 16:57:52 | BUY | AMD | 3 | $137.14 | N/A | 85 |
| 2025-07-01 16:57:52 | BUY | DIS | 4 | $123.06 | N/A | 85 |
| 2025-07-01 16:48:11 | SELL | AMD | 3 | $141.90 | $3.02 | 65 |
| 2025-07-01 16:48:11 | SELL | XOM | 4 | $108.77 | $-2.32 | 65 |
| 2025-07-01 16:48:11 | SELL | INTC | 12 | $22.94 | $7.39 | 65 |
| 2025-07-01 16:48:11 | BUY | CRM | 1 | $273.07 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | PFE | 3 | $25.00 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | CSCO | 8 | $68.88 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | CVX | 1 | $145.12 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | VZ | 1 | $43.67 | N/A | 75 |
| 2025-07-01 16:48:11 | BUY | T | 1 | $28.78 | N/A | 85 |

<!--TRADE_LOG_END--> 
