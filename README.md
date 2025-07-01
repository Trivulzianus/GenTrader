# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 17:49:55**

| Metric | Value |
|---|---|
| **Total Value** | **$101,131.45** |
| Cash | $80.93 |
| Holdings Value | $101,050.52 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.13 | $2,497.56 | 85 |
| ADBE | 5 | $385.76 | $391.05 | $1,955.25 | 75 |
| AMD | 17 | $140.02 | $137.35 | $2,334.97 | 85 |
| AMZN | 11 | $226.78 | $220.49 | $2,425.39 | 85 |
| AVGO | 9 | $272.95 | $265.81 | $2,392.24 | 85 |
| AXP | 6 | $315.94 | $323.86 | $1,943.16 | 65 |
| BA | 9 | $215.30 | $210.62 | $1,895.58 | 65 |
| BAC | 51 | $47.30 | $48.20 | $2,458.45 | 85 |
| C | 24 | $84.23 | $86.38 | $2,073.12 | 75 |
| CAT | 5 | $381.20 | $392.06 | $1,960.33 | 65 |
| COST | 2 | $991.47 | $986.47 | $1,972.94 | 65 |
| CRM | 8 | $274.90 | $273.37 | $2,186.92 | 75 |
| CSCO | 27 | $68.84 | $69.11 | $1,866.10 | 65 |
| CVX | 17 | $143.81 | $145.57 | $2,474.77 | 85 |
| DIS | 16 | $122.87 | $123.42 | $1,974.79 | 65 |
| GOOGL | 14 | $175.62 | $175.35 | $2,454.90 | 85 |
| GS | 3 | $706.65 | $708.13 | $2,124.39 | 65 |
| HD | 7 | $369.90 | $375.46 | $2,628.22 | 85 |
| INTC | 81 | $22.22 | $22.96 | $1,859.85 | 65 |
| JNJ | 12 | $151.63 | $155.34 | $1,864.14 | 65 |
| JPM | 7 | $285.02 | $290.02 | $2,030.14 | 65 |
| KO | 26 | $70.42 | $71.66 | $1,863.16 | 75 |
| LLY | 3 | $767.33 | $778.90 | $2,336.70 | 65 |
| MA | 4 | $537.87 | $565.61 | $2,262.42 | 65 |
| META | 3 | $712.71 | $721.05 | $2,163.15 | 85 |
| MRK | 30 | $79.35 | $81.85 | $2,455.50 | 85 |
| MSFT | 4 | $492.89 | $492.53 | $1,970.12 | 85 |
| NFLX | 1 | $1,334.07 | $1,297.80 | $1,297.80 | 85 |
| NKE | 33 | $70.93 | $72.97 | $2,408.01 | 85 |
| NVDA | 15 | $153.89 | $154.50 | $2,317.57 | 85 |
| ORCL | 9 | $219.56 | $219.47 | $1,975.23 | 65 |
| PEP | 16 | $131.60 | $134.84 | $2,157.44 | 75 |
| PFE | 98 | $24.29 | $25.00 | $2,450.01 | 85 |
| PG | 12 | $159.73 | $160.87 | $1,930.38 | 65 |
| PYPL | 32 | $73.86 | $75.54 | $2,417.28 | 85 |
| QCOM | 15 | $159.12 | $160.34 | $2,405.10 | 85 |
| T | 85 | $28.52 | $28.82 | $2,450.12 | 85 |
| TGT | 21 | $98.42 | $104.10 | $2,186.10 | 75 |
| TSLA | 7 | $290.03 | $300.68 | $2,104.72 | 75 |
| UNH | 8 | $306.63 | $322.04 | $2,576.32 | 85 |
| UNP | 11 | $232.22 | $235.19 | $2,587.03 | 85 |
| V | 6 | $344.95 | $356.53 | $2,139.18 | 65 |
| VZ | 49 | $42.71 | $43.66 | $2,139.59 | 75 |
| WFC | 30 | $79.85 | $81.38 | $2,441.55 | 85 |
| WMT | 25 | $97.07 | $98.40 | $2,460.00 | 85 |
| XOM | 20 | $109.38 | $109.14 | $2,182.80 | 75 |

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
| 2025-07-01 17:49:44 | SELL | TGT | 2 | $104.10 | $10.37 | 75 |
| 2025-07-01 17:49:44 | BUY | C | 2 | $86.38 | N/A | 75 |
| 2025-07-01 17:40:46 | SELL | XOM | 2 | $109.32 | $-0.11 | 75 |
| 2025-07-01 17:40:46 | SELL | INTC | 1 | $22.98 | $0.75 | 65 |
| 2025-07-01 17:40:46 | SELL | PFE | 1 | $25.00 | $0.69 | 85 |
| 2025-07-01 17:40:46 | SELL | CSCO | 1 | $69.07 | $0.22 | 65 |
| 2025-07-01 17:40:46 | BUY | VZ | 5 | $43.67 | N/A | 75 |
| 2025-07-01 17:40:46 | BUY | TGT | 2 | $104.20 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
