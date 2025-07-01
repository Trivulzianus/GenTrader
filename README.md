# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 17:17:16**

| Metric | Value |
|---|---|
| **Total Value** | **$101,027.14** |
| Cash | $244.76 |
| Holdings Value | $100,782.38 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.72 | $2,492.64 | 85 |
| ADBE | 5 | $385.76 | $389.85 | $1,949.23 | 65 |
| AMD | 16 | $140.21 | $137.35 | $2,197.60 | 75 |
| AMZN | 11 | $226.78 | $220.50 | $2,425.50 | 85 |
| AVGO | 7 | $274.91 | $267.46 | $1,872.22 | 85 |
| AXP | 6 | $315.94 | $323.47 | $1,940.82 | 65 |
| BA | 9 | $215.30 | $210.35 | $1,893.15 | 65 |
| BAC | 51 | $47.30 | $48.16 | $2,456.41 | 85 |
| C | 22 | $84.03 | $86.19 | $1,896.29 | 65 |
| CAT | 5 | $381.20 | $391.44 | $1,957.20 | 65 |
| COST | 2 | $991.47 | $984.17 | $1,968.35 | 75 |
| CRM | 8 | $274.90 | $272.79 | $2,182.32 | 85 |
| CSCO | 32 | $68.87 | $69.00 | $2,208.00 | 75 |
| CVX | 17 | $143.81 | $145.03 | $2,465.43 | 85 |
| DIS | 16 | $122.87 | $123.22 | $1,971.52 | 65 |
| GOOGL | 14 | $175.62 | $175.21 | $2,452.87 | 85 |
| GS | 3 | $706.65 | $708.61 | $2,125.82 | 75 |
| HD | 7 | $369.90 | $375.49 | $2,628.43 | 85 |
| INTC | 83 | $22.23 | $22.95 | $1,904.73 | 65 |
| JNJ | 12 | $151.63 | $155.12 | $1,861.44 | 65 |
| JPM | 7 | $285.02 | $289.88 | $2,029.12 | 65 |
| KO | 26 | $70.42 | $71.58 | $1,861.08 | 65 |
| LLY | 3 | $767.33 | $779.75 | $2,339.26 | 65 |
| MA | 4 | $537.87 | $563.94 | $2,255.75 | 65 |
| META | 3 | $712.71 | $722.11 | $2,166.33 | 90 |
| MRK | 30 | $79.35 | $81.56 | $2,446.76 | 85 |
| MSFT | 4 | $492.89 | $493.60 | $1,974.40 | 65 |
| NFLX | 1 | $1,334.07 | $1,301.75 | $1,301.75 | 85 |
| NKE | 33 | $70.93 | $72.72 | $2,399.76 | 85 |
| NVDA | 15 | $153.89 | $154.75 | $2,321.27 | 85 |
| ORCL | 9 | $219.56 | $220.28 | $1,982.52 | 65 |
| PEP | 16 | $131.60 | $134.46 | $2,151.36 | 75 |
| PFE | 99 | $24.30 | $24.91 | $2,465.60 | 85 |
| PG | 12 | $159.73 | $160.75 | $1,928.94 | 65 |
| PYPL | 32 | $73.86 | $75.34 | $2,410.83 | 85 |
| QCOM | 15 | $159.12 | $160.15 | $2,402.25 | 85 |
| T | 85 | $28.52 | $28.79 | $2,446.72 | 85 |
| TGT | 21 | $98.42 | $103.62 | $2,176.02 | 75 |
| TSLA | 7 | $290.03 | $302.39 | $2,116.73 | 75 |
| UNH | 8 | $306.63 | $321.68 | $2,573.44 | 85 |
| UNP | 11 | $232.22 | $234.73 | $2,582.03 | 85 |
| V | 6 | $344.95 | $355.52 | $2,133.12 | 65 |
| VZ | 50 | $42.73 | $43.59 | $2,179.75 | 75 |
| WFC | 30 | $79.85 | $81.17 | $2,435.25 | 85 |
| WMT | 25 | $97.07 | $98.25 | $2,456.25 | 85 |
| XOM | 22 | $109.38 | $108.92 | $2,396.13 | 85 |

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
| 2025-07-01 16:32:02 | SELL | JNJ | 1 | $156.45 | $4.44 | 65 |
| 2025-07-01 16:32:02 | SELL | PYPL | 1 | $75.43 | $1.52 | 85 |
| 2025-07-01 16:32:02 | SELL | NKE | 1 | $73.48 | $2.47 | 85 |
| 2025-07-01 16:32:02 | SELL | PFE | 1 | $25.17 | $0.89 | 85 |
| 2025-07-01 16:32:02 | SELL | KO | 3 | $71.72 | $3.51 | 65 |

<!--TRADE_LOG_END--> 
