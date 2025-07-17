# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 20:09:40**

| Metric | Value |
|---|---|
| **Total Value** | **$101,447.24** |
| Cash | $293.77 |
| Holdings Value | $101,153.47 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.02 | $2,100.20 | 65 |
| ADBE | 6 | $375.23 | $366.45 | $2,198.70 | 65 |
| AMD | 14 | $160.03 | $160.41 | $2,245.74 | 70 |
| AMZN | 11 | $221.89 | $223.88 | $2,462.68 | 75 |
| AVGO | 8 | $275.34 | $286.45 | $2,291.60 | 65 |
| AXP | 7 | $309.18 | $315.54 | $2,208.78 | 65 |
| BA | 9 | $232.13 | $231.00 | $2,079.00 | 70 |
| BAC | 50 | $46.32 | $47.05 | $2,352.75 | 75 |
| C | 29 | $86.64 | $93.08 | $2,699.32 | 85 |
| CAT | 6 | $397.74 | $418.09 | $2,508.54 | 75 |
| COST | 2 | $979.83 | $953.91 | $1,907.82 | 65 |
| CRM | 8 | $267.44 | $259.88 | $2,079.04 | 65 |
| CSCO | 33 | $68.56 | $68.30 | $2,253.90 | 70 |
| CVX | 16 | $146.84 | $151.51 | $2,424.16 | 75 |
| DIS | 19 | $122.64 | $122.17 | $2,321.23 | 70 |
| GOOGL | 13 | $179.34 | $183.58 | $2,386.54 | 75 |
| GS | 3 | $717.52 | $706.20 | $2,118.59 | 75 |
| HD | 6 | $354.18 | $359.08 | $2,154.48 | 65 |
| INTC | 90 | $22.37 | $22.80 | $2,052.00 | 65 |
| JNJ | 13 | $155.43 | $163.05 | $2,119.65 | 70 |
| JPM | 9 | $291.90 | $289.87 | $2,608.83 | 85 |
| KO | 30 | $70.97 | $70.62 | $2,118.60 | 65 |
| LLY | 3 | $781.32 | $761.59 | $2,284.76 | 65 |
| MA | 4 | $563.08 | $555.78 | $2,223.12 | 65 |
| META | 3 | $717.12 | $701.41 | $2,104.23 | 70 |
| MRK | 29 | $82.56 | $81.55 | $2,364.95 | 75 |
| MSFT | 5 | $498.84 | $511.70 | $2,558.50 | 75 |
| NFLX | 1 | $1,279.00 | $1,274.17 | $1,274.17 | 65 |
| NKE | 29 | $71.95 | $73.01 | $2,117.21 | 65 |
| NVDA | 15 | $171.80 | $173.00 | $2,595.00 | 85 |
| ORCL | 9 | $232.91 | $248.99 | $2,240.91 | 65 |
| PEP | 16 | $136.49 | $145.44 | $2,327.04 | 75 |
| PFE | 84 | $25.28 | $24.59 | $2,065.98 | 65 |
| PG | 14 | $152.18 | $155.64 | $2,178.96 | 65 |
| PYPL | 32 | $72.34 | $73.86 | $2,363.52 | 75 |
| QCOM | 14 | $153.83 | $152.61 | $2,136.54 | 65 |
| T | 76 | $27.10 | $27.01 | $2,052.76 | 65 |
| TGT | 20 | $104.83 | $103.76 | $2,075.20 | 65 |
| TSLA | 6 | $318.51 | $319.41 | $1,916.46 | 65 |
| UNH | 7 | $298.51 | $288.26 | $2,017.85 | 65 |
| UNP | 9 | $237.31 | $227.26 | $2,045.34 | 65 |
| V | 6 | $355.85 | $350.05 | $2,100.30 | 65 |
| VZ | 50 | $40.87 | $40.98 | $2,049.00 | 65 |
| WFC | 27 | $78.73 | $79.74 | $2,152.98 | 65 |
| WMT | 22 | $97.29 | $95.15 | $2,093.30 | 65 |
| XOM | 19 | $109.80 | $111.75 | $2,123.25 | 65 |

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
| 2025-07-17 20:09:30 | SELL | XOM | 2 | $111.75 | $3.52 | 65 |
| 2025-07-17 20:09:30 | SELL | WFC | 1 | $79.74 | $0.97 | 65 |
| 2025-07-17 20:09:30 | SELL | CSCO | 1 | $68.30 | $-0.26 | 70 |
| 2025-07-17 20:09:30 | SELL | CVX | 1 | $151.51 | $4.40 | 75 |
| 2025-07-17 20:09:30 | BUY | BAC | 3 | $47.06 | N/A | 75 |
| 2025-07-17 20:09:30 | BUY | INTC | 6 | $22.80 | N/A | 65 |
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

<!--TRADE_LOG_END--> 
