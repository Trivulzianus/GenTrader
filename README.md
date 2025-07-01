# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 19:43:20**

| Metric | Value |
|---|---|
| **Total Value** | **$101,160.73** |
| Cash | $324.95 |
| Holdings Value | $100,835.78 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.60 | $2,491.20 | 85 |
| ADBE | 5 | $385.76 | $391.20 | $1,956.02 | 75 |
| AMD | 14 | $139.29 | $136.75 | $1,914.50 | 65 |
| AMZN | 11 | $227.14 | $221.04 | $2,431.49 | 85 |
| AVGO | 9 | $272.95 | $263.79 | $2,374.11 | 85 |
| AXP | 6 | $315.94 | $323.12 | $1,938.69 | 65 |
| BA | 9 | $215.30 | $209.68 | $1,887.12 | 65 |
| BAC | 50 | $47.28 | $48.16 | $2,407.75 | 85 |
| C | 22 | $84.05 | $86.22 | $1,896.73 | 65 |
| CAT | 5 | $381.20 | $392.41 | $1,962.05 | 65 |
| COST | 2 | $991.47 | $984.74 | $1,969.48 | 65 |
| CRM | 8 | $274.93 | $272.18 | $2,177.40 | 75 |
| CSCO | 27 | $68.84 | $69.06 | $1,864.49 | 65 |
| CVX | 17 | $143.81 | $146.12 | $2,483.95 | 85 |
| DIS | 15 | $122.83 | $123.35 | $1,850.25 | 65 |
| GOOGL | 14 | $175.62 | $175.84 | $2,461.76 | 85 |
| GS | 3 | $706.65 | $707.25 | $2,121.75 | 65 |
| HD | 7 | $369.90 | $374.04 | $2,618.25 | 85 |
| INTC | 82 | $22.23 | $22.94 | $1,881.08 | 65 |
| JNJ | 12 | $151.64 | $155.91 | $1,870.92 | 65 |
| JPM | 7 | $285.02 | $290.31 | $2,032.20 | 65 |
| KO | 26 | $70.43 | $71.72 | $1,864.78 | 65 |
| LLY | 3 | $767.33 | $776.06 | $2,328.18 | 65 |
| MA | 4 | $537.87 | $565.20 | $2,260.80 | 75 |
| META | 3 | $712.71 | $718.54 | $2,155.62 | 85 |
| MRK | 30 | $79.35 | $81.80 | $2,454.00 | 85 |
| MSFT | 4 | $492.89 | $492.01 | $1,968.04 | 85 |
| NFLX | 1 | $1,334.07 | $1,292.48 | $1,292.48 | 85 |
| NKE | 33 | $70.99 | $73.36 | $2,421.04 | 85 |
| NVDA | 16 | $153.32 | $153.41 | $2,454.64 | 85 |
| ORCL | 9 | $219.56 | $219.09 | $1,971.77 | 65 |
| PEP | 16 | $131.60 | $135.44 | $2,166.96 | 75 |
| PFE | 97 | $24.29 | $25.07 | $2,431.79 | 85 |
| PG | 12 | $159.73 | $161.61 | $1,939.32 | 65 |
| PYPL | 32 | $73.86 | $75.39 | $2,412.48 | 85 |
| QCOM | 15 | $159.12 | $159.69 | $2,395.35 | 85 |
| T | 84 | $28.52 | $28.86 | $2,423.82 | 85 |
| TGT | 23 | $98.93 | $104.17 | $2,395.91 | 85 |
| TSLA | 7 | $287.46 | $303.90 | $2,127.30 | 75 |
| UNH | 8 | $306.63 | $325.00 | $2,600.00 | 85 |
| UNP | 11 | $232.22 | $235.84 | $2,594.30 | 85 |
| V | 6 | $344.95 | $356.14 | $2,136.84 | 65 |
| VZ | 49 | $42.72 | $43.73 | $2,142.53 | 75 |
| WFC | 30 | $79.85 | $81.37 | $2,441.10 | 85 |
| WMT | 25 | $97.07 | $98.23 | $2,455.88 | 85 |
| XOM | 22 | $109.37 | $109.53 | $2,409.66 | 85 |

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
| 2025-07-01 18:48:11 | SELL | AMD | 4 | $141.90 | $8.15 | 65 |
| 2025-07-01 18:48:11 | SELL | KO | 3 | $71.69 | $3.43 | 65 |
| 2025-07-01 18:48:11 | BUY | T | 10 | $28.80 | N/A | 85 |

<!--TRADE_LOG_END--> 
