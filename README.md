# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 20:09:33**

| Metric | Value |
|---|---|
| **Total Value** | **$101,096.82** |
| Cash | $412.16 |
| Holdings Value | $100,684.66 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.18 | $2,111.80 | 65 |
| ADBE | 6 | $375.23 | $365.79 | $2,194.74 | 65 |
| AMD | 14 | $159.84 | $156.99 | $2,197.86 | 65 |
| AMZN | 11 | $221.97 | $226.13 | $2,487.43 | 75 |
| AVGO | 8 | $275.34 | $283.34 | $2,266.72 | 65 |
| AXP | 7 | $309.18 | $308.09 | $2,156.63 | 65 |
| BA | 10 | $232.01 | $229.36 | $2,293.61 | 70 |
| BAC | 48 | $46.29 | $47.30 | $2,270.64 | 70 |
| C | 29 | $86.63 | $93.41 | $2,708.89 | 85 |
| CAT | 6 | $397.74 | $413.77 | $2,482.62 | 70 |
| COST | 2 | $979.83 | $950.95 | $1,901.90 | 65 |
| CRM | 8 | $267.44 | $262.34 | $2,098.72 | 65 |
| CSCO | 33 | $68.58 | $68.05 | $2,245.65 | 70 |
| CVX | 16 | $147.44 | $150.00 | $2,399.93 | 75 |
| DIS | 19 | $122.65 | $121.39 | $2,306.51 | 70 |
| GOOGL | 13 | $179.34 | $185.06 | $2,405.78 | 75 |
| GS | 3 | $717.52 | $708.50 | $2,125.50 | 80 |
| HD | 6 | $354.18 | $359.33 | $2,156.01 | 65 |
| INTC | 84 | $22.33 | $23.10 | $1,940.40 | 60 |
| JNJ | 14 | $155.98 | $163.67 | $2,291.38 | 70 |
| JPM | 8 | $292.14 | $291.17 | $2,329.32 | 70 |
| KO | 30 | $70.96 | $69.84 | $2,095.20 | 65 |
| LLY | 3 | $781.32 | $771.91 | $2,315.73 | 65 |
| MA | 4 | $563.08 | $552.20 | $2,208.80 | 65 |
| META | 3 | $717.12 | $704.28 | $2,112.84 | 70 |
| MRK | 28 | $82.53 | $79.98 | $2,239.44 | 70 |
| MSFT | 5 | $498.84 | $510.05 | $2,550.25 | 85 |
| NFLX | 1 | $1,208.39 | $1,209.24 | $1,209.24 | 65 |
| NKE | 29 | $71.98 | $72.48 | $2,102.07 | 65 |
| NVDA | 14 | $171.78 | $172.41 | $2,413.74 | 70 |
| ORCL | 9 | $232.91 | $245.31 | $2,207.79 | 70 |
| PEP | 15 | $135.89 | $143.24 | $2,148.60 | 65 |
| PFE | 86 | $25.26 | $24.46 | $2,103.56 | 65 |
| PG | 14 | $152.14 | $155.07 | $2,170.98 | 65 |
| PYPL | 29 | $72.21 | $74.17 | $2,150.93 | 65 |
| QCOM | 13 | $153.79 | $154.80 | $2,012.40 | 65 |
| T | 78 | $27.11 | $26.93 | $2,100.15 | 65 |
| TGT | 20 | $104.82 | $103.45 | $2,069.00 | 65 |
| TSLA | 6 | $318.51 | $329.65 | $1,977.90 | 65 |
| UNH | 8 | $283.36 | $282.57 | $2,260.56 | 65 |
| UNP | 9 | $225.02 | $224.77 | $2,022.93 | 65 |
| V | 6 | $355.85 | $349.07 | $2,094.42 | 65 |
| VZ | 51 | $40.87 | $40.80 | $2,080.80 | 65 |
| WFC | 30 | $78.90 | $80.63 | $2,418.90 | 75 |
| WMT | 22 | $97.29 | $95.05 | $2,091.10 | 65 |
| XOM | 20 | $109.72 | $107.77 | $2,155.30 | 65 |

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
| 2025-07-18 19:09:24 | SELL | XOM | 1 | $111.66 | $1.76 | 65 |
| 2025-07-18 19:09:24 | BUY | PYPL | 3 | $74.15 | N/A | 75 |
| 2025-07-18 19:09:24 | BUY | WFC | 2 | $80.58 | N/A | 75 |
| 2025-07-18 18:57:56 | SELL | BAC | 1 | $47.31 | $1.01 | 70 |
| 2025-07-18 18:57:56 | SELL | CVX | 1 | $146.95 | $-0.12 | 60 |
| 2025-07-18 18:57:56 | BUY | NVDA | 2 | $172.08 | N/A | 85 |
| 2025-07-18 18:57:56 | BUY | WFC | 1 | $80.47 | N/A | 70 |
| 2025-07-18 18:45:25 | SELL | BAC | 2 | $47.34 | $1.98 | 70 |

<!--TRADE_LOG_END--> 
