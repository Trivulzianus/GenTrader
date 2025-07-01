# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 19:16:38**

| Metric | Value |
|---|---|
| **Total Value** | **$101,137.63** |
| Cash | $155.78 |
| Holdings Value | $100,981.85 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.98 | $2,495.76 | 85 |
| ADBE | 5 | $385.76 | $391.20 | $1,956.00 | 75 |
| AMD | 17 | $138.84 | $136.59 | $2,322.03 | 85 |
| AMZN | 10 | $227.67 | $221.13 | $2,211.30 | 85 |
| AVGO | 9 | $272.95 | $263.45 | $2,371.05 | 85 |
| AXP | 6 | $315.94 | $322.78 | $1,936.68 | 65 |
| BA | 9 | $215.30 | $210.20 | $1,891.80 | 65 |
| BAC | 50 | $47.28 | $48.23 | $2,411.75 | 85 |
| C | 24 | $84.23 | $86.18 | $2,068.32 | 75 |
| CAT | 5 | $381.20 | $392.72 | $1,963.60 | 65 |
| COST | 2 | $991.47 | $985.26 | $1,970.52 | 65 |
| CRM | 8 | $274.93 | $272.63 | $2,181.08 | 75 |
| CSCO | 27 | $68.84 | $69.06 | $1,864.75 | 65 |
| CVX | 17 | $143.81 | $146.01 | $2,482.17 | 85 |
| DIS | 15 | $122.83 | $123.26 | $1,848.90 | 65 |
| GOOGL | 14 | $175.62 | $175.35 | $2,454.90 | 85 |
| GS | 3 | $706.65 | $706.53 | $2,119.61 | 75 |
| HD | 7 | $369.90 | $374.27 | $2,619.89 | 85 |
| INTC | 81 | $22.22 | $22.89 | $1,854.49 | 65 |
| JNJ | 13 | $151.97 | $156.00 | $2,028.00 | 75 |
| JPM | 7 | $285.02 | $290.00 | $2,029.97 | 65 |
| KO | 29 | $70.57 | $71.83 | $2,082.93 | 75 |
| LLY | 3 | $767.33 | $775.66 | $2,326.98 | 65 |
| MA | 4 | $537.87 | $565.35 | $2,261.40 | 85 |
| META | 3 | $712.71 | $718.22 | $2,154.66 | 88 |
| MRK | 30 | $79.35 | $81.98 | $2,459.55 | 85 |
| MSFT | 4 | $492.89 | $492.19 | $1,968.76 | 85 |
| NFLX | 1 | $1,334.07 | $1,294.94 | $1,294.94 | 85 |
| NKE | 26 | $70.32 | $73.25 | $1,904.50 | 65 |
| NVDA | 16 | $153.32 | $153.23 | $2,451.61 | 85 |
| ORCL | 9 | $219.56 | $218.32 | $1,964.92 | 65 |
| PEP | 16 | $131.60 | $135.47 | $2,167.60 | 75 |
| PFE | 96 | $24.28 | $25.04 | $2,403.36 | 85 |
| PG | 12 | $159.73 | $161.70 | $1,940.40 | 65 |
| PYPL | 32 | $73.86 | $75.47 | $2,414.88 | 85 |
| QCOM | 15 | $159.12 | $159.96 | $2,399.40 | 85 |
| T | 84 | $28.52 | $28.80 | $2,419.62 | 85 |
| TGT | 23 | $98.93 | $104.27 | $2,398.21 | 85 |
| TSLA | 7 | $287.46 | $301.62 | $2,111.31 | 65 |
| UNH | 8 | $306.63 | $324.21 | $2,593.68 | 85 |
| UNP | 11 | $232.22 | $235.81 | $2,593.97 | 85 |
| V | 6 | $344.95 | $356.62 | $2,139.75 | 65 |
| VZ | 49 | $42.72 | $43.67 | $2,139.83 | 75 |
| WFC | 30 | $79.85 | $81.25 | $2,437.35 | 85 |
| WMT | 25 | $97.07 | $98.38 | $2,459.38 | 85 |
| XOM | 22 | $109.37 | $109.56 | $2,410.30 | 85 |

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
| 2025-07-01 19:16:27 | SELL | NKE | 7 | $73.24 | $16.12 | 65 |
| 2025-07-01 19:16:27 | BUY | JNJ | 1 | $156.04 | N/A | 75 |
| 2025-07-01 19:16:27 | BUY | AMD | 2 | $136.57 | N/A | 85 |
| 2025-07-01 19:16:27 | BUY | KO | 3 | $71.83 | N/A | 75 |
| 2025-07-01 19:03:44 | BUY | C | 2 | $86.18 | N/A | 75 |
| 2025-07-01 19:03:44 | BUY | TGT | 2 | $104.35 | N/A | 85 |
| 2025-07-01 18:56:35 | SELL | C | 2 | $86.43 | $4.36 | 65 |
| 2025-07-01 18:56:35 | SELL | TGT | 2 | $104.57 | $11.24 | 75 |
| 2025-07-01 18:56:35 | BUY | AMD | 1 | $137.29 | N/A | 75 |
| 2025-07-01 18:48:11 | SELL | AMD | 4 | $141.90 | $8.15 | 65 |
| 2025-07-01 18:48:11 | SELL | KO | 3 | $71.69 | $3.43 | 65 |
| 2025-07-01 18:48:11 | BUY | T | 10 | $28.80 | N/A | 85 |
| 2025-07-01 18:48:11 | BUY | TGT | 2 | $104.46 | N/A | 85 |
| 2025-07-01 18:32:25 | SELL | BAC | 1 | $48.29 | $1.00 | 85 |
| 2025-07-01 18:32:25 | SELL | DIS | 1 | $123.40 | $0.53 | 65 |
| 2025-07-01 18:32:25 | SELL | VZ | 1 | $43.65 | $0.92 | 75 |
| 2025-07-01 18:32:25 | SELL | T | 11 | $28.78 | $2.88 | 75 |
| 2025-07-01 18:32:25 | BUY | KO | 3 | $71.73 | N/A | 75 |
| 2025-07-01 18:32:25 | BUY | XOM | 1 | $109.25 | N/A | 85 |
| 2025-07-01 18:32:25 | BUY | C | 2 | $86.29 | N/A | 75 |
| 2025-07-01 18:17:48 | SELL | INTC | 1 | $22.99 | $0.76 | 65 |
| 2025-07-01 18:17:48 | SELL | C | 3 | $86.22 | $5.70 | 65 |
| 2025-07-01 18:17:48 | SELL | T | 1 | $28.81 | $0.28 | 85 |
| 2025-07-01 18:17:48 | BUY | AMZN | 1 | $220.89 | N/A | 85 |
| 2025-07-01 18:17:48 | BUY | NKE | 6 | $72.90 | N/A | 85 |

<!--TRADE_LOG_END--> 
