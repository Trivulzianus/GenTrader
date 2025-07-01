# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 18:32:31**

| Metric | Value |
|---|---|
| **Total Value** | **$101,162.70** |
| Cash | $138.37 |
| Holdings Value | $101,024.32 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.31 | $2,499.78 | 85 |
| ADBE | 5 | $385.76 | $390.54 | $1,952.70 | 65 |
| AMD | 18 | $139.86 | $137.29 | $2,471.31 | 85 |
| AMZN | 10 | $227.67 | $220.99 | $2,209.90 | 85 |
| AVGO | 9 | $272.95 | $265.54 | $2,389.86 | 85 |
| AXP | 6 | $315.94 | $323.47 | $1,940.82 | 65 |
| BA | 9 | $215.30 | $210.47 | $1,894.23 | 65 |
| BAC | 50 | $47.28 | $48.30 | $2,415.25 | 85 |
| C | 24 | $84.25 | $86.28 | $2,070.84 | 75 |
| CAT | 5 | $381.20 | $392.76 | $1,963.80 | 65 |
| COST | 2 | $991.47 | $984.79 | $1,969.59 | 75 |
| CRM | 8 | $274.93 | $273.06 | $2,184.48 | 85 |
| CSCO | 27 | $68.84 | $69.12 | $1,866.38 | 65 |
| CVX | 17 | $143.81 | $145.55 | $2,474.28 | 85 |
| DIS | 15 | $122.83 | $123.40 | $1,851.00 | 65 |
| GOOGL | 14 | $175.62 | $175.62 | $2,458.75 | 85 |
| GS | 3 | $706.65 | $706.83 | $2,120.49 | 75 |
| HD | 7 | $369.90 | $374.55 | $2,621.85 | 85 |
| INTC | 81 | $22.22 | $23.00 | $1,862.60 | 65 |
| JNJ | 12 | $151.63 | $155.45 | $1,865.40 | 65 |
| JPM | 7 | $285.02 | $289.30 | $2,025.10 | 65 |
| KO | 29 | $70.55 | $71.73 | $2,080.32 | 75 |
| LLY | 3 | $767.33 | $774.45 | $2,323.35 | 65 |
| MA | 4 | $537.87 | $565.39 | $2,261.56 | 85 |
| META | 3 | $712.71 | $721.39 | $2,164.17 | 90 |
| MRK | 30 | $79.35 | $81.89 | $2,456.74 | 85 |
| MSFT | 4 | $492.89 | $492.68 | $1,970.72 | 85 |
| NFLX | 1 | $1,334.07 | $1,300.47 | $1,300.47 | 85 |
| NKE | 33 | $70.94 | $73.16 | $2,414.28 | 85 |
| NVDA | 16 | $153.32 | $154.54 | $2,472.64 | 85 |
| ORCL | 9 | $219.56 | $218.94 | $1,970.46 | 65 |
| PEP | 16 | $131.60 | $135.06 | $2,160.96 | 75 |
| PFE | 96 | $24.28 | $25.05 | $2,404.32 | 85 |
| PG | 12 | $159.73 | $161.15 | $1,933.80 | 65 |
| PYPL | 32 | $73.86 | $75.50 | $2,416.16 | 85 |
| QCOM | 15 | $159.12 | $160.49 | $2,407.28 | 85 |
| T | 74 | $28.48 | $28.80 | $2,130.83 | 75 |
| TGT | 21 | $98.42 | $104.00 | $2,184.11 | 75 |
| TSLA | 7 | $287.46 | $301.90 | $2,113.30 | 65 |
| UNH | 8 | $306.63 | $323.07 | $2,584.60 | 85 |
| UNP | 11 | $232.22 | $235.31 | $2,588.41 | 85 |
| V | 6 | $344.95 | $356.56 | $2,139.39 | 85 |
| VZ | 49 | $42.72 | $43.66 | $2,139.10 | 75 |
| WFC | 30 | $79.85 | $81.22 | $2,436.60 | 85 |
| WMT | 25 | $97.07 | $98.36 | $2,458.88 | 85 |
| XOM | 22 | $109.37 | $109.25 | $2,403.50 | 85 |

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
| 2025-07-01 18:04:57 | SELL | PFE | 10 | $25.00 | $7.12 | 75 |
| 2025-07-01 18:04:57 | SELL | NKE | 6 | $72.87 | $11.63 | 65 |
| 2025-07-01 18:04:57 | BUY | NVDA | 4 | $154.66 | N/A | 85 |
| 2025-07-01 18:04:57 | BUY | TSLA | 1 | $299.66 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | AMD | 1 | $137.18 | N/A | 85 |
| 2025-07-01 18:04:57 | BUY | C | 3 | $86.44 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | VZ | 1 | $43.69 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | T | 1 | $28.82 | N/A | 85 |
| 2025-07-01 17:56:28 | SELL | NVDA | 3 | $157.99 | $12.29 | 65 |

<!--TRADE_LOG_END--> 
