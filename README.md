# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 20:40:03**

| Metric | Value |
|---|---|
| **Total Value** | **$101,107.90** |
| Cash | $128.31 |
| Holdings Value | $100,979.59 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.18 | $2,111.80 | 65 |
| ADBE | 6 | $375.23 | $365.79 | $2,194.74 | 65 |
| AMD | 14 | $159.84 | $156.99 | $2,197.86 | 65 |
| AMZN | 11 | $221.97 | $226.13 | $2,487.43 | 75 |
| AVGO | 8 | $275.34 | $283.34 | $2,266.72 | 70 |
| AXP | 7 | $309.18 | $307.95 | $2,155.65 | 65 |
| BA | 10 | $232.01 | $229.34 | $2,293.40 | 65 |
| BAC | 48 | $46.29 | $47.32 | $2,271.36 | 70 |
| C | 29 | $86.63 | $93.45 | $2,710.05 | 85 |
| CAT | 6 | $397.74 | $413.71 | $2,482.26 | 70 |
| COST | 2 | $979.83 | $950.95 | $1,901.90 | 65 |
| CRM | 8 | $267.44 | $262.38 | $2,099.04 | 65 |
| CSCO | 31 | $68.62 | $68.05 | $2,109.55 | 65 |
| CVX | 18 | $147.73 | $150.04 | $2,700.72 | 85 |
| DIS | 19 | $122.65 | $121.42 | $2,306.98 | 70 |
| GOOGL | 13 | $179.34 | $185.06 | $2,405.78 | 75 |
| GS | 3 | $717.52 | $708.26 | $2,124.78 | 75 |
| HD | 6 | $354.18 | $359.40 | $2,156.40 | 65 |
| INTC | 90 | $22.38 | $23.10 | $2,079.00 | 65 |
| JNJ | 14 | $155.98 | $163.70 | $2,291.80 | 70 |
| JPM | 8 | $292.14 | $291.27 | $2,330.16 | 75 |
| KO | 30 | $70.96 | $69.85 | $2,095.50 | 65 |
| LLY | 3 | $781.32 | $771.71 | $2,315.13 | 65 |
| MA | 4 | $563.08 | $552.66 | $2,210.64 | 65 |
| META | 3 | $717.12 | $704.28 | $2,112.84 | 70 |
| MRK | 27 | $82.63 | $79.96 | $2,158.92 | 65 |
| MSFT | 5 | $498.84 | $510.05 | $2,550.25 | 85 |
| NFLX | 1 | $1,208.39 | $1,209.24 | $1,209.24 | 65 |
| NKE | 29 | $71.98 | $72.47 | $2,101.63 | 65 |
| NVDA | 14 | $171.78 | $172.41 | $2,413.74 | 70 |
| ORCL | 9 | $232.91 | $245.45 | $2,209.05 | 70 |
| PEP | 15 | $135.89 | $143.24 | $2,148.60 | 65 |
| PFE | 86 | $25.26 | $24.47 | $2,104.42 | 65 |
| PG | 14 | $152.14 | $155.10 | $2,171.40 | 65 |
| PYPL | 32 | $72.39 | $74.17 | $2,373.44 | 75 |
| QCOM | 13 | $153.79 | $154.80 | $2,012.40 | 65 |
| T | 78 | $27.11 | $26.94 | $2,101.32 | 65 |
| TGT | 20 | $104.82 | $103.46 | $2,069.20 | 65 |
| TSLA | 6 | $318.51 | $329.65 | $1,977.90 | 65 |
| UNH | 8 | $283.36 | $282.65 | $2,261.20 | 65 |
| UNP | 9 | $225.02 | $224.87 | $2,023.83 | 65 |
| V | 6 | $355.85 | $349.05 | $2,094.30 | 65 |
| VZ | 51 | $40.87 | $40.84 | $2,082.84 | 65 |
| WFC | 28 | $78.78 | $80.64 | $2,257.92 | 70 |
| WMT | 22 | $97.29 | $95.05 | $2,091.10 | 65 |
| XOM | 20 | $109.72 | $107.77 | $2,155.40 | 65 |

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
| 2025-07-18 20:39:58 | SELL | NKE | 2 | $72.47 | $0.93 | 65 |
| 2025-07-18 20:39:58 | SELL | WFC | 2 | $80.64 | $3.47 | 70 |
| 2025-07-18 20:39:58 | BUY | CVX | 2 | $150.04 | N/A | 85 |
| 2025-07-18 20:26:39 | SELL | MRK | 1 | $79.96 | $-2.57 | 65 |
| 2025-07-18 20:26:39 | SELL | CSCO | 2 | $68.05 | $-1.07 | 65 |
| 2025-07-18 20:26:39 | BUY | INTC | 6 | $23.10 | N/A | 65 |
| 2025-07-18 20:26:39 | BUY | PYPL | 3 | $74.17 | N/A | 75 |
| 2025-07-18 20:26:39 | BUY | NKE | 2 | $72.47 | N/A | 70 |
| 2025-07-18 20:09:26 | SELL | INTC | 6 | $23.10 | $4.30 | 60 |
| 2025-07-18 20:09:26 | SELL | NKE | 2 | $72.49 | $0.95 | 65 |
| 2025-07-18 20:09:26 | BUY | MRK | 2 | $79.98 | N/A | 70 |
| 2025-07-18 20:09:26 | BUY | CVX | 2 | $150.00 | N/A | 75 |
| 2025-07-18 19:51:18 | BUY | NKE | 2 | $72.48 | N/A | 70 |
| 2025-07-18 19:36:26 | SELL | AMZN | 1 | $225.95 | $3.65 | 75 |
| 2025-07-18 19:36:26 | SELL | NVDA | 1 | $171.99 | $0.20 | 70 |
| 2025-07-18 19:36:26 | SELL | PYPL | 3 | $74.15 | $5.29 | 65 |
| 2025-07-18 19:36:26 | BUY | DIS | 1 | $121.18 | N/A | 75 |
| 2025-07-18 19:36:26 | BUY | C | 3 | $93.09 | N/A | 85 |
| 2025-07-18 19:36:26 | BUY | CSCO | 2 | $68.11 | N/A | 70 |
| 2025-07-18 19:24:57 | SELL | C | 3 | $93.17 | $19.60 | 75 |
| 2025-07-18 19:24:57 | BUY | AMZN | 2 | $225.93 | N/A | 85 |
| 2025-07-18 19:24:57 | BUY | NVDA | 1 | $172.15 | N/A | 85 |
| 2025-07-18 19:24:57 | BUY | GOOGL | 1 | $184.87 | N/A | 75 |
| 2025-07-18 19:24:57 | BUY | XOM | 1 | $108.14 | N/A | 70 |
| 2025-07-18 19:09:24 | SELL | NVDA | 2 | $173.00 | $2.16 | 70 |

<!--TRADE_LOG_END--> 
