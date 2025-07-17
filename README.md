# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 19:50:15**

| Metric | Value |
|---|---|
| **Total Value** | **$101,433.04** |
| Cash | $48.69 |
| Holdings Value | $101,384.35 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.66 | $2,106.60 | 65 |
| ADBE | 6 | $375.23 | $366.16 | $2,196.96 | 65 |
| AMD | 14 | $160.03 | $160.06 | $2,240.91 | 75 |
| AMZN | 11 | $221.89 | $224.18 | $2,465.98 | 80 |
| AVGO | 8 | $275.34 | $285.70 | $2,285.60 | 65 |
| AXP | 7 | $309.18 | $315.99 | $2,211.93 | 75 |
| BA | 9 | $232.13 | $231.87 | $2,086.83 | 70 |
| BAC | 47 | $46.28 | $46.93 | $2,205.71 | 70 |
| C | 29 | $86.64 | $92.87 | $2,693.23 | 85 |
| CAT | 6 | $397.74 | $418.24 | $2,509.44 | 70 |
| COST | 2 | $979.83 | $952.33 | $1,904.66 | 65 |
| CRM | 8 | $267.44 | $259.41 | $2,075.28 | 60 |
| CSCO | 34 | $68.56 | $68.39 | $2,325.43 | 75 |
| CVX | 17 | $147.11 | $151.52 | $2,575.84 | 85 |
| DIS | 19 | $122.64 | $121.95 | $2,317.05 | 70 |
| GOOGL | 13 | $179.34 | $183.76 | $2,388.88 | 75 |
| GS | 3 | $717.52 | $706.21 | $2,118.63 | 70 |
| HD | 6 | $354.18 | $359.12 | $2,154.72 | 65 |
| INTC | 84 | $22.34 | $22.78 | $1,913.52 | 60 |
| JNJ | 13 | $155.43 | $163.52 | $2,125.76 | 70 |
| JPM | 9 | $291.90 | $289.71 | $2,607.39 | 85 |
| KO | 30 | $70.97 | $70.58 | $2,117.40 | 65 |
| LLY | 3 | $781.32 | $762.33 | $2,286.98 | 65 |
| MA | 4 | $563.08 | $556.72 | $2,226.88 | 65 |
| META | 3 | $717.12 | $701.82 | $2,105.45 | 70 |
| MRK | 29 | $82.56 | $81.61 | $2,366.69 | 75 |
| MSFT | 5 | $498.84 | $512.00 | $2,560.00 | 85 |
| NFLX | 1 | $1,279.00 | $1,271.82 | $1,271.82 | 70 |
| NKE | 29 | $71.95 | $72.97 | $2,116.13 | 65 |
| NVDA | 15 | $171.80 | $173.28 | $2,599.20 | 85 |
| ORCL | 9 | $232.91 | $249.08 | $2,241.72 | 65 |
| PEP | 16 | $136.49 | $145.47 | $2,327.60 | 75 |
| PFE | 84 | $25.28 | $24.55 | $2,062.62 | 65 |
| PG | 14 | $152.18 | $155.52 | $2,177.28 | 65 |
| PYPL | 32 | $72.34 | $73.97 | $2,367.20 | 75 |
| QCOM | 14 | $153.83 | $152.43 | $2,134.02 | 65 |
| T | 76 | $27.10 | $26.96 | $2,049.34 | 65 |
| TGT | 20 | $104.83 | $103.70 | $2,074.00 | 65 |
| TSLA | 6 | $318.51 | $319.27 | $1,915.62 | 65 |
| UNH | 7 | $298.51 | $287.34 | $2,011.38 | 65 |
| UNP | 9 | $237.31 | $227.55 | $2,047.95 | 65 |
| V | 6 | $355.85 | $350.21 | $2,101.26 | 65 |
| VZ | 50 | $40.87 | $41.01 | $2,050.25 | 65 |
| WFC | 28 | $78.77 | $79.54 | $2,227.12 | 70 |
| WMT | 22 | $97.29 | $94.98 | $2,089.56 | 65 |
| XOM | 21 | $109.99 | $111.74 | $2,346.54 | 75 |

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
| 2025-07-17 19:50:09 | SELL | NKE | 2 | $72.10 | $0.29 | 65 |
| 2025-07-17 19:50:09 | SELL | DIS | 1 | $122.09 | $-0.52 | 70 |
| 2025-07-17 19:50:09 | BUY | AMZN | 1 | $224.27 | N/A | 80 |
| 2025-07-17 19:50:09 | BUY | CSCO | 1 | $68.36 | N/A | 75 |
| 2025-07-17 19:36:48 | SELL | NKE | 1 | $73.03 | $1.04 | 70 |
| 2025-07-17 19:36:48 | SELL | WFC | 1 | $79.74 | $0.93 | 70 |
| 2025-07-17 19:36:48 | BUY | NVDA | 1 | $173.29 | N/A | 85 |
| 2025-07-17 19:36:48 | BUY | BAC | 1 | $47.03 | N/A | 70 |
| 2025-07-17 19:36:48 | BUY | XOM | 2 | $111.86 | N/A | 75 |
| 2025-07-17 19:36:48 | BUY | VZ | 1 | $41.04 | N/A | 65 |
| 2025-07-17 19:36:48 | BUY | CVX | 1 | $151.73 | N/A | 85 |
| 2025-07-17 19:25:18 | SELL | NVDA | 1 | $173.28 | $1.48 | 75 |
| 2025-07-17 19:25:18 | SELL | XOM | 2 | $111.81 | $3.66 | 65 |
| 2025-07-17 19:25:18 | SELL | CSCO | 1 | $68.29 | $-0.27 | 70 |
| 2025-07-17 19:25:18 | BUY | BAC | 2 | $47.01 | N/A | 70 |
| 2025-07-17 19:25:18 | BUY | WFC | 1 | $79.79 | N/A | 75 |
| 2025-07-17 19:25:18 | BUY | VZ | 2 | $41.04 | N/A | 65 |
| 2025-07-17 19:08:19 | SELL | INTC | 5 | $22.80 | $2.13 | 60 |
| 2025-07-17 19:08:19 | SELL | BAC | 2 | $47.15 | $1.78 | 65 |
| 2025-07-17 19:08:19 | SELL | WMT | 1 | $95.40 | $-1.81 | 65 |
| 2025-07-17 19:08:19 | SELL | BA | 1 | $232.16 | $0.04 | 65 |
| 2025-07-17 19:08:19 | SELL | VZ | 3 | $41.06 | $0.58 | 60 |
| 2025-07-17 19:08:19 | BUY | NVDA | 2 | $173.41 | N/A | 85 |
| 2025-07-17 19:08:19 | BUY | NKE | 4 | $73.05 | N/A | 75 |
| 2025-07-17 18:47:04 | SELL | NKE | 4 | $73.06 | $4.28 | 65 |

<!--TRADE_LOG_END--> 
