# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 22:08:28**

| Metric | Value |
|---|---|
| **Total Value** | **$101,107.90** |
| Cash | $229.16 |
| Holdings Value | $100,878.74 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.18 | $2,111.80 | 70 |
| ADBE | 6 | $375.23 | $365.79 | $2,194.74 | 65 |
| AMD | 14 | $159.84 | $156.99 | $2,197.86 | 65 |
| AMZN | 11 | $221.97 | $226.13 | $2,487.43 | 75 |
| AVGO | 8 | $275.34 | $283.34 | $2,266.72 | 70 |
| AXP | 7 | $309.18 | $307.95 | $2,155.65 | 65 |
| BA | 9 | $232.31 | $229.34 | $2,064.06 | 65 |
| BAC | 47 | $46.26 | $47.32 | $2,224.04 | 70 |
| C | 29 | $86.63 | $93.45 | $2,710.05 | 85 |
| CAT | 6 | $397.74 | $413.71 | $2,482.26 | 65 |
| COST | 2 | $979.83 | $950.95 | $1,901.90 | 65 |
| CRM | 8 | $267.44 | $262.38 | $2,099.04 | 65 |
| CSCO | 31 | $68.62 | $68.05 | $2,109.55 | 65 |
| CVX | 17 | $147.60 | $150.04 | $2,550.68 | 80 |
| DIS | 19 | $122.65 | $121.42 | $2,306.98 | 70 |
| GOOGL | 13 | $179.34 | $185.06 | $2,405.78 | 75 |
| GS | 3 | $717.52 | $708.26 | $2,124.78 | 75 |
| HD | 6 | $354.18 | $359.40 | $2,156.40 | 65 |
| INTC | 89 | $22.38 | $23.10 | $2,055.90 | 65 |
| JNJ | 14 | $155.98 | $163.70 | $2,291.80 | 70 |
| JPM | 8 | $292.14 | $291.27 | $2,330.16 | 75 |
| KO | 30 | $70.96 | $69.85 | $2,095.50 | 65 |
| LLY | 3 | $781.32 | $771.71 | $2,315.13 | 65 |
| MA | 4 | $563.08 | $552.66 | $2,210.64 | 65 |
| META | 3 | $717.12 | $704.28 | $2,112.84 | 70 |
| MRK | 26 | $82.73 | $79.96 | $2,078.96 | 65 |
| MSFT | 5 | $498.84 | $510.05 | $2,550.25 | 85 |
| NFLX | 1 | $1,208.39 | $1,209.24 | $1,209.24 | 65 |
| NKE | 30 | $71.99 | $72.47 | $2,174.10 | 70 |
| NVDA | 15 | $171.82 | $172.41 | $2,586.15 | 85 |
| ORCL | 9 | $232.91 | $245.45 | $2,209.05 | 75 |
| PEP | 15 | $135.89 | $143.24 | $2,148.60 | 70 |
| PFE | 85 | $25.27 | $24.47 | $2,079.95 | 65 |
| PG | 14 | $152.14 | $155.10 | $2,171.40 | 65 |
| PYPL | 32 | $72.39 | $74.17 | $2,373.44 | 75 |
| QCOM | 14 | $153.86 | $154.80 | $2,167.20 | 65 |
| T | 77 | $27.11 | $26.94 | $2,074.38 | 65 |
| TGT | 20 | $104.82 | $103.46 | $2,069.20 | 65 |
| TSLA | 6 | $318.51 | $329.65 | $1,977.90 | 65 |
| UNH | 8 | $283.36 | $282.65 | $2,261.20 | 65 |
| UNP | 9 | $225.02 | $224.87 | $2,023.83 | 65 |
| V | 6 | $355.85 | $349.05 | $2,094.30 | 65 |
| VZ | 51 | $40.87 | $40.84 | $2,082.84 | 65 |
| WFC | 29 | $78.84 | $80.64 | $2,338.56 | 75 |
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
| 2025-07-18 22:08:22 | SELL | CSCO | 1 | $68.05 | $-0.55 | 65 |
| 2025-07-18 22:08:22 | SELL | CVX | 1 | $150.04 | $2.31 | 80 |
| 2025-07-18 22:08:22 | BUY | NKE | 1 | $72.47 | N/A | 70 |
| 2025-07-18 21:50:46 | SELL | BAC | 1 | $47.32 | $1.03 | 70 |
| 2025-07-18 21:50:46 | SELL | BA | 1 | $229.34 | $-2.67 | 65 |
| 2025-07-18 21:50:46 | BUY | INTC | 6 | $23.10 | N/A | 65 |
| 2025-07-18 21:50:46 | BUY | CSCO | 1 | $68.05 | N/A | 70 |
| 2025-07-18 21:37:59 | SELL | GOOGL | 1 | $185.06 | $5.31 | 75 |
| 2025-07-18 21:37:59 | SELL | BAC | 2 | $47.32 | $1.98 | 70 |
| 2025-07-18 21:37:59 | BUY | PYPL | 4 | $74.17 | N/A | 75 |
| 2025-07-18 21:26:21 | SELL | INTC | 6 | $23.10 | $4.35 | 60 |
| 2025-07-18 21:26:21 | BUY | GOOGL | 1 | $185.06 | N/A | 85 |
| 2025-07-18 21:26:21 | BUY | BAC | 2 | $47.32 | N/A | 75 |
| 2025-07-18 21:08:10 | SELL | NKE | 1 | $72.47 | $0.48 | 65 |
| 2025-07-18 21:08:10 | SELL | PYPL | 4 | $74.17 | $7.11 | 65 |
| 2025-07-18 21:08:10 | SELL | T | 1 | $26.94 | $-0.17 | 65 |
| 2025-07-18 21:08:10 | BUY | NVDA | 2 | $172.41 | N/A | 85 |
| 2025-07-18 21:08:10 | BUY | INTC | 6 | $23.10 | N/A | 65 |
| 2025-07-18 21:08:10 | BUY | WFC | 1 | $80.64 | N/A | 75 |
| 2025-07-18 21:08:10 | BUY | QCOM | 1 | $154.80 | N/A | 70 |
| 2025-07-18 20:51:52 | SELL | INTC | 7 | $23.10 | $5.01 | 60 |
| 2025-07-18 20:51:52 | SELL | NVDA | 1 | $172.41 | $0.63 | 70 |
| 2025-07-18 20:51:52 | SELL | PFE | 1 | $24.47 | $-0.79 | 65 |
| 2025-07-18 20:51:52 | SELL | MRK | 1 | $79.96 | $-2.67 | 65 |
| 2025-07-18 20:51:52 | BUY | NKE | 1 | $72.47 | N/A | 70 |

<!--TRADE_LOG_END--> 
