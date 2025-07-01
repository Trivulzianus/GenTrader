# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 19:52:58**

| Metric | Value |
|---|---|
| **Total Value** | **$101,173.11** |
| Cash | $34.01 |
| Holdings Value | $101,139.10 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.91 | $2,494.86 | 85 |
| ADBE | 5 | $385.76 | $392.13 | $1,960.65 | 75 |
| AMD | 17 | $138.79 | $136.60 | $2,322.20 | 85 |
| AMZN | 11 | $227.14 | $221.17 | $2,432.87 | 85 |
| AVGO | 9 | $272.95 | $265.12 | $2,386.08 | 85 |
| AXP | 6 | $315.94 | $322.62 | $1,935.69 | 65 |
| BA | 9 | $215.30 | $210.05 | $1,890.43 | 65 |
| BAC | 50 | $47.28 | $48.17 | $2,408.51 | 85 |
| C | 24 | $84.24 | $86.28 | $2,070.60 | 75 |
| CAT | 5 | $381.20 | $391.13 | $1,955.65 | 65 |
| COST | 2 | $991.47 | $985.57 | $1,971.14 | 65 |
| CRM | 8 | $274.93 | $272.08 | $2,176.64 | 75 |
| CSCO | 27 | $68.84 | $69.10 | $1,865.70 | 65 |
| CVX | 15 | $143.58 | $145.51 | $2,182.72 | 75 |
| DIS | 15 | $122.83 | $123.49 | $1,852.35 | 65 |
| GOOGL | 14 | $175.62 | $175.65 | $2,459.10 | 85 |
| GS | 3 | $706.65 | $706.87 | $2,120.61 | 75 |
| HD | 7 | $369.90 | $373.90 | $2,617.30 | 85 |
| INTC | 82 | $22.23 | $22.91 | $1,879.03 | 65 |
| JNJ | 12 | $151.64 | $155.80 | $1,869.60 | 65 |
| JPM | 7 | $285.02 | $290.26 | $2,031.86 | 65 |
| KO | 26 | $70.43 | $71.72 | $1,864.59 | 75 |
| LLY | 3 | $767.33 | $778.19 | $2,334.57 | 65 |
| MA | 4 | $537.87 | $565.16 | $2,260.66 | 65 |
| META | 3 | $712.71 | $719.61 | $2,158.83 | 85 |
| MRK | 30 | $79.35 | $81.64 | $2,449.05 | 85 |
| MSFT | 4 | $492.89 | $492.78 | $1,971.12 | 85 |
| NFLX | 1 | $1,334.07 | $1,295.99 | $1,295.99 | 85 |
| NKE | 33 | $70.99 | $73.35 | $2,420.40 | 85 |
| NVDA | 16 | $153.32 | $153.88 | $2,462.00 | 85 |
| ORCL | 9 | $219.56 | $219.26 | $1,973.36 | 65 |
| PEP | 16 | $131.60 | $135.38 | $2,166.08 | 75 |
| PFE | 97 | $24.29 | $25.07 | $2,431.31 | 85 |
| PG | 12 | $159.73 | $161.44 | $1,937.28 | 65 |
| PYPL | 32 | $73.86 | $75.50 | $2,416.16 | 85 |
| QCOM | 15 | $159.12 | $159.70 | $2,395.50 | 85 |
| T | 84 | $28.52 | $28.89 | $2,426.76 | 85 |
| TGT | 23 | $98.93 | $104.16 | $2,395.68 | 85 |
| TSLA | 7 | $287.46 | $303.41 | $2,123.86 | 70 |
| UNH | 8 | $306.63 | $324.99 | $2,599.92 | 85 |
| UNP | 11 | $232.22 | $235.80 | $2,593.80 | 85 |
| V | 6 | $344.95 | $356.04 | $2,136.24 | 65 |
| VZ | 49 | $42.72 | $43.70 | $2,141.55 | 75 |
| WFC | 30 | $79.85 | $81.36 | $2,440.80 | 85 |
| WMT | 25 | $97.07 | $98.27 | $2,456.62 | 85 |
| XOM | 22 | $109.37 | $109.25 | $2,403.39 | 85 |

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
| 2025-07-01 19:52:52 | SELL | CVX | 2 | $145.52 | $3.42 | 75 |
| 2025-07-01 19:52:52 | BUY | AMD | 3 | $136.47 | N/A | 85 |
| 2025-07-01 19:52:52 | BUY | C | 2 | $86.29 | N/A | 75 |
| 2025-07-01 19:43:14 | SELL | AMD | 2 | $136.76 | $-4.42 | 65 |
| 2025-07-01 19:43:14 | SELL | INTC | 10 | $22.93 | $6.30 | 65 |
| 2025-07-01 19:43:14 | BUY | T | 9 | $28.86 | N/A | 85 |
| 2025-07-01 19:33:41 | SELL | JNJ | 1 | $155.95 | $3.97 | 65 |
| 2025-07-01 19:33:41 | SELL | KO | 1 | $71.68 | $1.20 | 65 |
| 2025-07-01 19:33:41 | BUY | INTC | 11 | $22.96 | N/A | 75 |
| 2025-07-01 19:26:02 | SELL | AMD | 1 | $136.80 | $-2.04 | 75 |
| 2025-07-01 19:26:02 | SELL | KO | 2 | $71.71 | $2.28 | 65 |
| 2025-07-01 19:26:02 | SELL | C | 2 | $86.16 | $3.86 | 65 |
| 2025-07-01 19:26:02 | SELL | T | 9 | $28.85 | $2.95 | 75 |
| 2025-07-01 19:26:02 | BUY | AMZN | 1 | $221.83 | N/A | 85 |
| 2025-07-01 19:26:02 | BUY | NKE | 7 | $73.47 | N/A | 85 |
| 2025-07-01 19:26:02 | BUY | PFE | 1 | $25.07 | N/A | 85 |
| 2025-07-01 19:16:27 | SELL | NKE | 7 | $73.24 | $16.12 | 65 |
| 2025-07-01 19:16:27 | BUY | JNJ | 1 | $156.04 | N/A | 75 |
| 2025-07-01 19:16:27 | BUY | AMD | 2 | $136.57 | N/A | 85 |
| 2025-07-01 19:16:27 | BUY | KO | 3 | $71.83 | N/A | 75 |
| 2025-07-01 19:03:44 | BUY | C | 2 | $86.18 | N/A | 75 |
| 2025-07-01 19:03:44 | BUY | TGT | 2 | $104.35 | N/A | 85 |
| 2025-07-01 18:56:35 | SELL | C | 2 | $86.43 | $4.36 | 65 |
| 2025-07-01 18:56:35 | SELL | TGT | 2 | $104.57 | $11.24 | 75 |
| 2025-07-01 18:56:35 | BUY | AMD | 1 | $137.29 | N/A | 75 |

<!--TRADE_LOG_END--> 
