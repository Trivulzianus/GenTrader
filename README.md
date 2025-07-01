# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 15:30:23**

| Metric | Value |
|---|---|
| **Total Value** | **$100,928.36** |
| Cash | $152.44 |
| Holdings Value | $100,775.93 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.97 | $2,495.64 | 85 |
| ADBE | 5 | $385.76 | $390.45 | $1,952.25 | 75 |
| AMD | 16 | $141.82 | $136.44 | $2,183.00 | 75 |
| AMZN | 11 | $226.80 | $219.68 | $2,416.44 | 85 |
| AVGO | 9 | $275.08 | $265.90 | $2,393.10 | 85 |
| AXP | 6 | $315.94 | $320.35 | $1,922.10 | 70 |
| BA | 9 | $215.30 | $208.00 | $1,872.00 | 65 |
| BAC | 51 | $47.30 | $47.72 | $2,433.71 | 85 |
| C | 25 | $84.23 | $85.17 | $2,129.38 | 75 |
| CAT | 5 | $381.20 | $390.61 | $1,953.03 | 65 |
| COST | 2 | $991.47 | $987.21 | $1,974.42 | 65 |
| CRM | 8 | $274.83 | $273.36 | $2,186.84 | 75 |
| CSCO | 28 | $68.90 | $68.83 | $1,927.38 | 85 |
| CVX | 14 | $143.46 | $145.31 | $2,034.34 | 85 |
| DIS | 16 | $122.90 | $123.10 | $1,969.60 | 65 |
| GOOGL | 14 | $175.62 | $174.90 | $2,448.60 | 85 |
| GS | 3 | $706.65 | $704.83 | $2,114.48 | 65 |
| HD | 7 | $369.90 | $377.63 | $2,643.44 | 85 |
| INTC | 82 | $22.32 | $22.84 | $1,873.29 | 65 |
| JNJ | 13 | $151.98 | $157.21 | $2,043.67 | 75 |
| JPM | 7 | $285.02 | $287.93 | $2,015.48 | 65 |
| KO | 26 | $70.37 | $72.18 | $1,876.68 | 65 |
| LLY | 3 | $767.33 | $787.48 | $2,362.44 | 65 |
| MA | 4 | $537.87 | $562.87 | $2,251.46 | 65 |
| META | 3 | $712.71 | $723.06 | $2,169.17 | 90 |
| MRK | 30 | $79.35 | $82.17 | $2,465.10 | 85 |
| MSFT | 4 | $492.89 | $493.90 | $1,975.60 | 65 |
| NFLX | 1 | $1,334.07 | $1,294.58 | $1,294.58 | 85 |
| NKE | 34 | $71.01 | $73.52 | $2,499.68 | 85 |
| NVDA | 16 | $156.03 | $152.77 | $2,444.40 | 85 |
| ORCL | 9 | $219.56 | $218.62 | $1,967.58 | 65 |
| PEP | 16 | $131.60 | $135.66 | $2,170.64 | 75 |
| PFE | 98 | $24.30 | $25.11 | $2,461.27 | 85 |
| PG | 12 | $159.73 | $161.85 | $1,942.20 | 65 |
| PYPL | 33 | $73.91 | $75.10 | $2,478.30 | 85 |
| QCOM | 16 | $159.24 | $159.09 | $2,545.44 | 85 |
| T | 85 | $28.52 | $28.91 | $2,457.78 | 85 |
| TGT | 21 | $98.42 | $104.20 | $2,188.20 | 75 |
| TSLA | 6 | $290.36 | $300.79 | $1,804.74 | 65 |
| UNH | 8 | $306.63 | $325.52 | $2,604.16 | 85 |
| UNP | 11 | $232.22 | $235.26 | $2,587.91 | 85 |
| V | 6 | $344.95 | $355.07 | $2,130.42 | 85 |
| VZ | 50 | $42.73 | $43.70 | $2,185.25 | 75 |
| WFC | 31 | $79.89 | $80.64 | $2,499.68 | 85 |
| WMT | 25 | $97.07 | $98.89 | $2,472.38 | 85 |
| XOM | 18 | $109.40 | $108.82 | $1,958.70 | 65 |

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
| 2025-07-01 15:30:17 | SELL | CRM | 1 | $273.37 | $-1.30 | 75 |
| 2025-07-01 15:30:17 | SELL | AMD | 2 | $136.40 | $-9.64 | 75 |
| 2025-07-01 15:30:17 | SELL | INTC | 2 | $22.86 | $1.05 | 65 |
| 2025-07-01 15:30:17 | SELL | PFE | 1 | $25.12 | $0.81 | 85 |
| 2025-07-01 15:30:17 | SELL | BA | 1 | $207.81 | $-6.74 | 65 |
| 2025-07-01 15:30:17 | BUY | BAC | 11 | $47.72 | N/A | 85 |
| 2025-07-01 15:30:17 | BUY | C | 2 | $85.19 | N/A | 75 |
| 2025-07-01 15:16:59 | SELL | KO | 1 | $72.42 | $1.98 | 65 |
| 2025-07-01 15:16:59 | SELL | PEP | 1 | $135.79 | $3.93 | 75 |
| 2025-07-01 15:16:59 | BUY | JNJ | 1 | $157.42 | N/A | 75 |
| 2025-07-01 15:16:59 | BUY | AMD | 2 | $135.28 | N/A | 85 |
| 2025-07-01 15:16:59 | BUY | CVX | 1 | $145.10 | N/A | 75 |
| 2025-07-01 15:04:07 | SELL | AMD | 2 | $136.43 | $-9.83 | 75 |
| 2025-07-01 15:04:07 | SELL | CSCO | 4 | $69.05 | $0.54 | 65 |
| 2025-07-01 15:04:07 | BUY | NKE | 1 | $71.04 | N/A | 85 |
| 2025-07-01 15:04:07 | BUY | PFE | 10 | $24.85 | N/A | 85 |
| 2025-07-01 14:55:20 | SELL | TSLA | 1 | $317.66 | $23.40 | 65 |
| 2025-07-01 14:55:20 | SELL | PFE | 10 | $24.80 | $4.99 | 75 |
| 2025-07-01 14:55:20 | SELL | CSCO | 4 | $68.99 | $0.27 | 75 |
| 2025-07-01 14:55:20 | BUY | NVDA | 1 | $152.99 | N/A | 85 |
| 2025-07-01 14:55:20 | BUY | INTC | 1 | $22.64 | N/A | 65 |
| 2025-07-01 14:55:20 | BUY | AMD | 2 | $136.55 | N/A | 85 |
| 2025-07-01 14:55:20 | BUY | T | 9 | $28.98 | N/A | 85 |
| 2025-07-01 14:48:45 | SELL | JNJ | 1 | $156.44 | $4.53 | 65 |
| 2025-07-01 14:48:45 | SELL | INTC | 2 | $22.64 | $0.60 | 65 |

<!--TRADE_LOG_END--> 
