# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 23:51:14**

| Metric | Value |
|---|---|
| **Total Value** | **$101,424.08** |
| Cash | $297.48 |
| Holdings Value | $101,126.60 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.17 | $210.02 | $2,310.22 | 75 |
| ADBE | 6 | $375.23 | $366.45 | $2,198.70 | 65 |
| AMD | 14 | $160.03 | $160.41 | $2,245.74 | 75 |
| AMZN | 11 | $221.89 | $223.88 | $2,462.68 | 75 |
| AVGO | 8 | $275.34 | $286.45 | $2,291.60 | 70 |
| AXP | 7 | $309.18 | $315.35 | $2,207.45 | 75 |
| BA | 9 | $232.13 | $231.00 | $2,079.00 | 65 |
| BAC | 47 | $46.28 | $47.02 | $2,209.94 | 70 |
| C | 29 | $86.64 | $93.09 | $2,699.61 | 85 |
| CAT | 6 | $397.74 | $418.07 | $2,508.42 | 85 |
| COST | 2 | $979.83 | $953.91 | $1,907.82 | 65 |
| CRM | 8 | $267.44 | $259.88 | $2,079.04 | 65 |
| CSCO | 33 | $68.56 | $68.30 | $2,253.90 | 70 |
| CVX | 16 | $146.84 | $151.38 | $2,422.08 | 75 |
| DIS | 19 | $122.64 | $122.21 | $2,321.99 | 75 |
| GOOGL | 13 | $179.34 | $183.58 | $2,386.54 | 75 |
| GS | 3 | $717.52 | $705.84 | $2,117.52 | 85 |
| HD | 6 | $354.18 | $359.04 | $2,154.24 | 60 |
| INTC | 90 | $22.37 | $22.80 | $2,052.00 | 65 |
| JNJ | 13 | $155.43 | $162.98 | $2,118.74 | 65 |
| JPM | 9 | $291.90 | $289.90 | $2,609.10 | 85 |
| KO | 30 | $70.97 | $70.59 | $2,117.70 | 65 |
| LLY | 3 | $781.32 | $761.50 | $2,284.50 | 65 |
| MA | 4 | $563.08 | $555.61 | $2,222.44 | 65 |
| META | 3 | $717.12 | $701.41 | $2,104.23 | 65 |
| MRK | 29 | $82.56 | $81.52 | $2,364.08 | 75 |
| MSFT | 5 | $498.84 | $511.70 | $2,558.50 | 75 |
| NFLX | 1 | $1,279.00 | $1,274.17 | $1,274.17 | 65 |
| NKE | 29 | $71.95 | $72.98 | $2,116.42 | 65 |
| NVDA | 15 | $171.80 | $173.00 | $2,595.00 | 85 |
| ORCL | 9 | $232.91 | $248.75 | $2,238.75 | 70 |
| PEP | 16 | $136.49 | $145.44 | $2,327.04 | 75 |
| PFE | 84 | $25.28 | $24.58 | $2,064.72 | 65 |
| PG | 14 | $152.18 | $155.62 | $2,178.68 | 65 |
| PYPL | 31 | $72.29 | $73.86 | $2,289.66 | 75 |
| QCOM | 14 | $153.83 | $152.61 | $2,136.54 | 65 |
| T | 76 | $27.10 | $26.99 | $2,051.24 | 65 |
| TGT | 20 | $104.83 | $103.65 | $2,073.00 | 65 |
| TSLA | 6 | $318.51 | $319.41 | $1,916.46 | 65 |
| UNH | 7 | $298.51 | $288.07 | $2,016.49 | 65 |
| UNP | 9 | $237.31 | $227.49 | $2,047.41 | 65 |
| V | 6 | $355.85 | $349.81 | $2,098.86 | 65 |
| VZ | 50 | $40.87 | $40.95 | $2,047.50 | 65 |
| WFC | 28 | $78.77 | $79.71 | $2,231.88 | 70 |
| WMT | 20 | $97.51 | $95.09 | $1,901.80 | 60 |
| XOM | 20 | $109.90 | $111.66 | $2,233.20 | 70 |

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
| 2025-07-17 23:51:08 | SELL | INTC | 1 | $22.80 | $0.42 | 65 |
| 2025-07-17 23:51:08 | SELL | WMT | 3 | $95.09 | $-6.31 | 60 |
| 2025-07-17 23:51:08 | SELL | T | 1 | $26.99 | $-0.10 | 65 |
| 2025-07-17 23:51:08 | BUY | AAPL | 1 | $210.02 | N/A | 75 |
| 2025-07-17 23:51:08 | BUY | NVDA | 2 | $173.00 | N/A | 85 |
| 2025-07-17 23:51:08 | BUY | PYPL | 2 | $73.86 | N/A | 75 |
| 2025-07-17 23:38:23 | BUY | BAC | 2 | $47.02 | N/A | 70 |
| 2025-07-17 23:38:23 | BUY | INTC | 7 | $22.80 | N/A | 65 |
| 2025-07-17 23:38:23 | BUY | XOM | 1 | $111.66 | N/A | 70 |
| 2025-07-17 23:38:23 | BUY | WMT | 1 | $95.09 | N/A | 70 |
| 2025-07-17 23:38:23 | BUY | WFC | 1 | $79.71 | N/A | 70 |
| 2025-07-17 23:26:09 | SELL | NVDA | 2 | $173.00 | $2.40 | 70 |
| 2025-07-17 23:26:09 | SELL | BAC | 5 | $47.02 | $3.48 | 65 |
| 2025-07-17 23:26:09 | SELL | PYPL | 3 | $73.86 | $4.56 | 65 |
| 2025-07-17 23:26:09 | SELL | BA | 1 | $231.00 | $-1.01 | 65 |
| 2025-07-17 23:09:27 | BUY | PYPL | 2 | $73.86 | N/A | 75 |
| 2025-07-17 23:09:27 | BUY | WFC | 1 | $79.71 | N/A | 70 |
| 2025-07-17 22:52:06 | SELL | WFC | 2 | $79.71 | $1.89 | 65 |
| 2025-07-17 22:52:06 | SELL | CVX | 1 | $151.38 | $4.27 | 75 |
| 2025-07-17 22:52:06 | BUY | NVDA | 2 | $173.00 | N/A | 85 |
| 2025-07-17 22:52:06 | BUY | PYPL | 1 | $73.86 | N/A | 70 |
| 2025-07-17 22:40:48 | SELL | NVDA | 2 | $173.00 | $2.40 | 70 |
| 2025-07-17 22:40:48 | BUY | BAC | 2 | $47.02 | N/A | 75 |
| 2025-07-17 22:26:00 | BUY | PYPL | 1 | $73.86 | N/A | 70 |
| 2025-07-17 22:26:00 | BUY | CVX | 1 | $151.38 | N/A | 85 |

<!--TRADE_LOG_END--> 
