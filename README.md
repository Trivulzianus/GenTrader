# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 20:04:08**

| Metric | Value |
|---|---|
| **Total Value** | **$101,078.52** |
| Cash | $192.89 |
| Holdings Value | $100,885.63 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.82 | $2,493.84 | 85 |
| ADBE | 5 | $385.76 | $392.10 | $1,960.50 | 75 |
| AMD | 14 | $139.36 | $136.11 | $1,905.54 | 65 |
| AMZN | 11 | $227.14 | $220.46 | $2,425.06 | 85 |
| AVGO | 9 | $272.95 | $264.74 | $2,382.66 | 85 |
| AXP | 6 | $315.94 | $322.48 | $1,934.88 | 65 |
| BA | 9 | $215.30 | $209.76 | $1,887.84 | 65 |
| BAC | 50 | $47.28 | $48.16 | $2,408.00 | 85 |
| C | 22 | $84.05 | $86.27 | $1,897.94 | 65 |
| CAT | 5 | $381.20 | $390.96 | $1,954.80 | 65 |
| COST | 2 | $991.47 | $985.96 | $1,971.92 | 65 |
| CRM | 8 | $274.93 | $272.01 | $2,176.08 | 75 |
| CSCO | 31 | $68.87 | $69.10 | $2,142.10 | 75 |
| CVX | 16 | $143.71 | $145.59 | $2,329.44 | 85 |
| DIS | 15 | $122.83 | $123.47 | $1,851.98 | 65 |
| GOOGL | 14 | $175.62 | $175.84 | $2,461.76 | 85 |
| GS | 3 | $706.65 | $706.51 | $2,119.53 | 65 |
| HD | 7 | $369.90 | $373.21 | $2,612.47 | 85 |
| INTC | 82 | $22.23 | $22.85 | $1,873.70 | 65 |
| JNJ | 12 | $151.64 | $155.90 | $1,870.80 | 65 |
| JPM | 7 | $285.02 | $290.34 | $2,032.38 | 65 |
| KO | 26 | $70.43 | $71.68 | $1,863.68 | 65 |
| LLY | 3 | $767.33 | $775.90 | $2,327.70 | 65 |
| MA | 4 | $537.87 | $564.62 | $2,258.48 | 65 |
| META | 3 | $712.71 | $719.22 | $2,157.66 | 90 |
| MRK | 30 | $79.35 | $81.81 | $2,454.30 | 85 |
| MSFT | 4 | $492.89 | $492.05 | $1,968.20 | 85 |
| NFLX | 1 | $1,334.07 | $1,293.60 | $1,293.60 | 85 |
| NKE | 33 | $70.99 | $73.39 | $2,421.71 | 85 |
| NVDA | 16 | $153.32 | $153.30 | $2,452.80 | 85 |
| ORCL | 9 | $219.56 | $218.97 | $1,970.73 | 65 |
| PEP | 16 | $131.60 | $135.26 | $2,164.16 | 75 |
| PFE | 97 | $24.29 | $25.04 | $2,428.88 | 85 |
| PG | 12 | $159.73 | $161.24 | $1,934.82 | 65 |
| PYPL | 32 | $73.86 | $75.30 | $2,409.44 | 85 |
| QCOM | 15 | $159.12 | $159.40 | $2,391.00 | 85 |
| T | 84 | $28.52 | $28.87 | $2,425.08 | 85 |
| TGT | 23 | $98.93 | $103.88 | $2,389.24 | 85 |
| TSLA | 7 | $287.46 | $300.71 | $2,104.97 | 65 |
| UNH | 8 | $306.63 | $326.02 | $2,608.16 | 85 |
| UNP | 11 | $232.22 | $235.58 | $2,591.38 | 85 |
| V | 6 | $344.95 | $355.52 | $2,133.12 | 85 |
| VZ | 49 | $42.72 | $43.66 | $2,139.34 | 75 |
| WFC | 30 | $79.85 | $81.47 | $2,444.25 | 85 |
| WMT | 25 | $97.07 | $98.24 | $2,456.00 | 85 |
| XOM | 22 | $109.37 | $109.26 | $2,403.72 | 85 |

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
| 2025-07-01 20:04:01 | SELL | AMD | 3 | $136.11 | $-8.04 | 65 |
| 2025-07-01 20:04:01 | SELL | C | 2 | $86.27 | $4.06 | 65 |
| 2025-07-01 20:04:01 | BUY | CSCO | 4 | $69.10 | N/A | 75 |
| 2025-07-01 20:04:01 | BUY | CVX | 1 | $145.59 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
