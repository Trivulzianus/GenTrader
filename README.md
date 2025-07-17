# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 18:47:10**

| Metric | Value |
|---|---|
| **Total Value** | **$101,404.49** |
| Cash | $329.75 |
| Holdings Value | $101,074.74 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.03 | $2,110.25 | 65 |
| ADBE | 6 | $375.23 | $365.43 | $2,192.55 | 65 |
| AMD | 14 | $160.03 | $159.19 | $2,228.66 | 70 |
| AMZN | 10 | $221.65 | $223.84 | $2,238.35 | 75 |
| AVGO | 8 | $275.34 | $285.65 | $2,285.20 | 65 |
| AXP | 7 | $309.18 | $315.31 | $2,207.19 | 75 |
| BA | 10 | $232.13 | $231.93 | $2,319.30 | 75 |
| BAC | 46 | $46.27 | $47.09 | $2,166.14 | 70 |
| C | 29 | $86.64 | $92.72 | $2,688.74 | 85 |
| CAT | 6 | $397.74 | $418.51 | $2,511.06 | 70 |
| COST | 2 | $979.83 | $952.06 | $1,904.12 | 65 |
| CRM | 8 | $267.44 | $258.86 | $2,070.88 | 65 |
| CSCO | 34 | $68.55 | $68.33 | $2,323.05 | 75 |
| CVX | 16 | $146.82 | $151.13 | $2,418.08 | 75 |
| DIS | 20 | $122.61 | $121.59 | $2,431.80 | 75 |
| GOOGL | 13 | $179.34 | $183.60 | $2,386.74 | 75 |
| GS | 3 | $717.52 | $710.82 | $2,132.46 | 85 |
| HD | 6 | $354.18 | $359.29 | $2,155.74 | 65 |
| INTC | 89 | $22.37 | $22.82 | $2,030.54 | 65 |
| JNJ | 13 | $155.43 | $163.72 | $2,128.36 | 65 |
| JPM | 9 | $291.90 | $289.88 | $2,608.97 | 85 |
| KO | 30 | $70.97 | $69.94 | $2,098.20 | 65 |
| LLY | 3 | $781.32 | $763.28 | $2,289.84 | 65 |
| MA | 4 | $563.08 | $554.49 | $2,217.94 | 65 |
| META | 3 | $717.12 | $700.87 | $2,102.61 | 70 |
| MRK | 29 | $82.56 | $81.57 | $2,365.53 | 75 |
| MSFT | 5 | $498.84 | $511.90 | $2,559.50 | 85 |
| NFLX | 1 | $1,279.00 | $1,270.84 | $1,270.84 | 65 |
| NKE | 28 | $71.84 | $73.05 | $2,045.40 | 65 |
| NVDA | 13 | $171.55 | $173.66 | $2,257.58 | 70 |
| ORCL | 9 | $232.91 | $248.01 | $2,232.05 | 75 |
| PEP | 16 | $136.49 | $145.34 | $2,325.40 | 70 |
| PFE | 84 | $25.28 | $24.54 | $2,061.36 | 65 |
| PG | 14 | $152.18 | $155.13 | $2,171.82 | 65 |
| PYPL | 32 | $72.34 | $74.02 | $2,368.48 | 75 |
| QCOM | 14 | $153.83 | $152.81 | $2,139.34 | 65 |
| T | 76 | $27.10 | $26.99 | $2,051.24 | 65 |
| TGT | 20 | $104.83 | $103.59 | $2,071.80 | 65 |
| TSLA | 6 | $318.51 | $319.44 | $1,916.67 | 65 |
| UNH | 7 | $298.51 | $288.15 | $2,017.07 | 65 |
| UNP | 9 | $237.31 | $227.51 | $2,047.59 | 65 |
| V | 6 | $355.85 | $350.00 | $2,100.00 | 70 |
| VZ | 50 | $40.87 | $41.01 | $2,050.25 | 65 |
| WFC | 28 | $78.77 | $79.84 | $2,235.66 | 70 |
| WMT | 23 | $97.21 | $95.34 | $2,192.82 | 70 |
| XOM | 21 | $109.98 | $111.79 | $2,347.59 | 75 |

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
| 2025-07-17 18:47:04 | SELL | NKE | 4 | $73.06 | $4.28 | 65 |
| 2025-07-17 18:47:04 | SELL | PFE | 1 | $24.54 | $-0.73 | 65 |
| 2025-07-17 18:47:04 | SELL | C | 1 | $92.71 | $5.87 | 85 |
| 2025-07-17 18:47:04 | SELL | UNP | 1 | $227.55 | $-8.78 | 65 |
| 2025-07-17 18:47:04 | SELL | T | 1 | $26.98 | $-0.11 | 65 |
| 2025-07-17 18:47:04 | BUY | INTC | 5 | $22.82 | N/A | 65 |
| 2025-07-17 18:47:04 | BUY | BAC | 2 | $47.10 | N/A | 70 |
| 2025-07-17 18:47:04 | BUY | WMT | 2 | $95.35 | N/A | 70 |
| 2025-07-17 18:47:04 | BUY | BA | 1 | $232.04 | N/A | 75 |
| 2025-07-17 18:47:04 | BUY | CSCO | 2 | $68.33 | N/A | 75 |
| 2025-07-17 18:28:18 | SELL | NVDA | 2 | $173.20 | $2.86 | 70 |
| 2025-07-17 18:28:18 | SELL | BAC | 1 | $47.17 | $0.91 | 65 |
| 2025-07-17 18:28:18 | SELL | WMT | 1 | $95.37 | $-1.92 | 60 |
| 2025-07-17 18:28:18 | BUY | XOM | 1 | $111.84 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | NKE | 1 | $73.01 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | PYPL | 2 | $73.96 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | BA | 9 | $232.14 | N/A | 70 |
| 2025-07-17 18:28:18 | BUY | CSCO | 1 | $68.31 | N/A | 70 |
| 2025-07-17 18:27:32 | SELL | BA | 9 | $232.00 | $190.71 | 65 |
| 2025-07-17 18:11:19 | SELL | DIS | 2 | $121.50 | $-2.02 | 75 |
| 2025-07-17 18:11:19 | SELL | NKE | 1 | $72.98 | $0.99 | 70 |
| 2025-07-17 18:11:19 | SELL | CSCO | 2 | $68.28 | $-0.57 | 65 |
| 2025-07-17 18:11:19 | BUY | XOM | 1 | $111.70 | N/A | 70 |
| 2025-07-17 18:11:19 | BUY | PFE | 1 | $24.49 | N/A | 65 |
| 2025-07-17 18:11:19 | BUY | WFC | 2 | $79.68 | N/A | 70 |

<!--TRADE_LOG_END--> 
