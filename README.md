# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 19:33:52**

| Metric | Value |
|---|---|
| **Total Value** | **$101,168.18** |
| Cash | $81.82 |
| Holdings Value | $101,086.36 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.01 | $2,496.12 | 85 |
| ADBE | 5 | $385.76 | $390.69 | $1,953.45 | 75 |
| AMD | 16 | $138.97 | $136.79 | $2,188.64 | 85 |
| AMZN | 11 | $227.14 | $221.53 | $2,436.83 | 85 |
| AVGO | 9 | $272.95 | $263.99 | $2,375.91 | 85 |
| AXP | 6 | $315.94 | $322.75 | $1,936.50 | 75 |
| BA | 9 | $215.30 | $210.07 | $1,890.67 | 65 |
| BAC | 50 | $47.28 | $48.17 | $2,408.61 | 85 |
| C | 22 | $84.05 | $86.13 | $1,894.97 | 65 |
| CAT | 5 | $381.20 | $392.61 | $1,963.05 | 65 |
| COST | 2 | $991.47 | $984.18 | $1,968.36 | 65 |
| CRM | 8 | $274.93 | $272.53 | $2,180.24 | 75 |
| CSCO | 27 | $68.84 | $69.08 | $1,865.29 | 65 |
| CVX | 17 | $143.81 | $146.03 | $2,482.51 | 85 |
| DIS | 15 | $122.83 | $123.37 | $1,850.55 | 65 |
| GOOGL | 14 | $175.62 | $175.81 | $2,461.34 | 85 |
| GS | 3 | $706.65 | $706.44 | $2,119.32 | 75 |
| HD | 7 | $369.90 | $374.34 | $2,620.38 | 85 |
| INTC | 92 | $22.30 | $22.96 | $2,112.32 | 75 |
| JNJ | 12 | $151.64 | $155.96 | $1,871.52 | 65 |
| JPM | 7 | $285.02 | $289.88 | $2,029.19 | 65 |
| KO | 26 | $70.43 | $71.69 | $1,864.07 | 65 |
| LLY | 3 | $767.33 | $776.62 | $2,329.86 | 65 |
| MA | 4 | $537.87 | $565.07 | $2,260.26 | 75 |
| META | 3 | $712.71 | $719.18 | $2,157.54 | 85 |
| MRK | 30 | $79.35 | $81.91 | $2,457.30 | 85 |
| MSFT | 4 | $492.89 | $492.19 | $1,968.76 | 85 |
| NFLX | 1 | $1,334.07 | $1,292.71 | $1,292.71 | 85 |
| NKE | 33 | $70.99 | $73.33 | $2,420.05 | 85 |
| NVDA | 16 | $153.32 | $153.62 | $2,457.92 | 85 |
| ORCL | 9 | $219.56 | $218.81 | $1,969.25 | 65 |
| PEP | 16 | $131.60 | $135.38 | $2,166.00 | 75 |
| PFE | 97 | $24.29 | $25.07 | $2,432.28 | 85 |
| PG | 12 | $159.73 | $161.60 | $1,939.20 | 65 |
| PYPL | 32 | $73.86 | $75.42 | $2,413.60 | 85 |
| QCOM | 15 | $159.12 | $159.79 | $2,396.85 | 85 |
| T | 75 | $28.48 | $28.84 | $2,162.99 | 85 |
| TGT | 23 | $98.93 | $103.98 | $2,391.62 | 85 |
| TSLA | 7 | $287.46 | $303.38 | $2,123.66 | 70 |
| UNH | 8 | $306.63 | $324.56 | $2,596.46 | 85 |
| UNP | 11 | $232.22 | $235.94 | $2,595.39 | 85 |
| V | 6 | $344.95 | $356.37 | $2,138.24 | 65 |
| VZ | 49 | $42.72 | $43.69 | $2,140.81 | 75 |
| WFC | 30 | $79.85 | $81.31 | $2,439.45 | 85 |
| WMT | 25 | $97.07 | $98.28 | $2,456.88 | 85 |
| XOM | 22 | $109.37 | $109.52 | $2,409.44 | 85 |

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
| 2025-07-01 18:48:11 | BUY | TGT | 2 | $104.46 | N/A | 85 |
| 2025-07-01 18:32:25 | SELL | BAC | 1 | $48.29 | $1.00 | 85 |
| 2025-07-01 18:32:25 | SELL | DIS | 1 | $123.40 | $0.53 | 65 |

<!--TRADE_LOG_END--> 
