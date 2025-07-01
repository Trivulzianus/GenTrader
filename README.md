# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 19:03:51**

| Metric | Value |
|---|---|
| **Total Value** | **$101,087.91** |
| Cash | $287.79 |
| Holdings Value | $100,800.12 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.65 | $2,491.80 | 85 |
| ADBE | 5 | $385.76 | $390.25 | $1,951.25 | 75 |
| AMD | 15 | $139.15 | $136.38 | $2,045.70 | 75 |
| AMZN | 10 | $227.67 | $220.67 | $2,206.73 | 85 |
| AVGO | 9 | $272.95 | $263.22 | $2,368.98 | 85 |
| AXP | 6 | $315.94 | $322.60 | $1,935.57 | 65 |
| BA | 9 | $215.30 | $210.20 | $1,891.80 | 65 |
| BAC | 50 | $47.28 | $48.28 | $2,414.25 | 85 |
| C | 24 | $84.23 | $86.22 | $2,069.28 | 75 |
| CAT | 5 | $381.20 | $392.33 | $1,961.65 | 65 |
| COST | 2 | $991.47 | $985.84 | $1,971.68 | 65 |
| CRM | 8 | $274.93 | $272.36 | $2,178.88 | 75 |
| CSCO | 27 | $68.84 | $69.03 | $1,863.92 | 65 |
| CVX | 17 | $143.81 | $145.93 | $2,480.81 | 85 |
| DIS | 15 | $122.83 | $123.04 | $1,845.60 | 65 |
| GOOGL | 14 | $175.62 | $174.96 | $2,449.37 | 85 |
| GS | 3 | $706.65 | $706.20 | $2,118.59 | 65 |
| HD | 7 | $369.90 | $373.70 | $2,615.90 | 85 |
| INTC | 81 | $22.22 | $22.91 | $1,855.70 | 65 |
| JNJ | 12 | $151.63 | $155.96 | $1,871.52 | 65 |
| JPM | 7 | $285.02 | $289.70 | $2,027.90 | 65 |
| KO | 26 | $70.42 | $71.83 | $1,867.45 | 65 |
| LLY | 3 | $767.33 | $774.43 | $2,323.29 | 65 |
| MA | 4 | $537.87 | $565.14 | $2,260.56 | 85 |
| META | 3 | $712.71 | $717.76 | $2,153.30 | 85 |
| MRK | 30 | $79.35 | $82.00 | $2,460.00 | 85 |
| MSFT | 4 | $492.89 | $491.66 | $1,966.64 | 85 |
| NFLX | 1 | $1,334.07 | $1,293.44 | $1,293.44 | 85 |
| NKE | 33 | $70.94 | $73.15 | $2,413.95 | 85 |
| NVDA | 16 | $153.32 | $153.26 | $2,452.24 | 85 |
| ORCL | 9 | $219.56 | $218.06 | $1,962.59 | 65 |
| PEP | 16 | $131.60 | $135.53 | $2,168.48 | 75 |
| PFE | 96 | $24.28 | $25.08 | $2,408.00 | 85 |
| PG | 12 | $159.73 | $161.69 | $1,940.28 | 65 |
| PYPL | 32 | $73.86 | $75.45 | $2,414.56 | 85 |
| QCOM | 15 | $159.12 | $160.16 | $2,402.40 | 85 |
| T | 84 | $28.52 | $28.80 | $2,419.62 | 85 |
| TGT | 23 | $98.93 | $104.39 | $2,400.97 | 85 |
| TSLA | 7 | $287.46 | $300.60 | $2,104.20 | 75 |
| UNH | 8 | $306.63 | $324.16 | $2,593.28 | 85 |
| UNP | 11 | $232.22 | $235.80 | $2,593.80 | 85 |
| V | 6 | $344.95 | $356.26 | $2,137.56 | 85 |
| VZ | 49 | $42.72 | $43.67 | $2,139.83 | 75 |
| WFC | 30 | $79.85 | $81.28 | $2,438.26 | 85 |
| WMT | 25 | $97.07 | $98.36 | $2,459.00 | 85 |
| XOM | 22 | $109.37 | $109.53 | $2,409.55 | 85 |

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
| 2025-07-01 18:17:48 | BUY | PFE | 8 | $25.05 | N/A | 85 |
| 2025-07-01 18:04:57 | SELL | AMZN | 2 | $219.39 | $-14.77 | 65 |
| 2025-07-01 18:04:57 | SELL | CRM | 1 | $273.68 | $-1.11 | 75 |
| 2025-07-01 18:04:57 | SELL | XOM | 1 | $109.05 | $-0.31 | 75 |

<!--TRADE_LOG_END--> 
