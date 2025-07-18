# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 05:57:23**

| Metric | Value |
|---|---|
| **Total Value** | **$101,424.08** |
| Cash | $812.61 |
| Holdings Value | $100,611.47 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.02 | $2,100.20 | 65 |
| ADBE | 6 | $375.23 | $366.45 | $2,198.70 | 65 |
| AMD | 14 | $160.03 | $160.41 | $2,245.74 | 70 |
| AMZN | 11 | $221.89 | $223.88 | $2,462.68 | 80 |
| AVGO | 8 | $275.34 | $286.45 | $2,291.60 | 65 |
| AXP | 7 | $309.18 | $315.35 | $2,207.45 | 75 |
| BA | 9 | $232.13 | $231.00 | $2,079.00 | 70 |
| BAC | 44 | $46.23 | $47.02 | $2,068.88 | 65 |
| C | 29 | $86.64 | $93.09 | $2,699.61 | 85 |
| CAT | 6 | $397.74 | $418.07 | $2,508.42 | 70 |
| COST | 2 | $979.83 | $953.91 | $1,907.82 | 65 |
| CRM | 8 | $267.44 | $259.88 | $2,079.04 | 65 |
| CSCO | 33 | $68.56 | $68.30 | $2,253.90 | 70 |
| CVX | 16 | $146.84 | $151.38 | $2,422.08 | 75 |
| DIS | 19 | $122.64 | $122.21 | $2,321.99 | 70 |
| GOOGL | 13 | $179.34 | $183.58 | $2,386.54 | 70 |
| GS | 3 | $717.52 | $705.84 | $2,117.52 | 75 |
| HD | 6 | $354.18 | $359.04 | $2,154.24 | 65 |
| INTC | 91 | $22.38 | $22.80 | $2,074.80 | 65 |
| JNJ | 13 | $155.43 | $162.98 | $2,118.74 | 70 |
| JPM | 9 | $291.90 | $289.90 | $2,609.10 | 75 |
| KO | 30 | $70.97 | $70.59 | $2,117.70 | 65 |
| LLY | 3 | $781.32 | $761.50 | $2,284.50 | 65 |
| MA | 4 | $563.08 | $555.61 | $2,222.44 | 65 |
| META | 3 | $717.12 | $701.41 | $2,104.23 | 70 |
| MRK | 29 | $82.56 | $81.52 | $2,364.08 | 75 |
| MSFT | 5 | $498.84 | $511.70 | $2,558.50 | 70 |
| NFLX | 1 | $1,279.00 | $1,274.17 | $1,274.17 | 65 |
| NKE | 29 | $71.95 | $72.98 | $2,116.42 | 65 |
| NVDA | 13 | $171.61 | $173.00 | $2,249.00 | 70 |
| ORCL | 9 | $232.91 | $248.75 | $2,238.75 | 75 |
| PEP | 15 | $135.89 | $145.44 | $2,181.60 | 65 |
| PFE | 85 | $25.27 | $24.58 | $2,089.30 | 65 |
| PG | 13 | $151.91 | $155.62 | $2,023.06 | 65 |
| PYPL | 32 | $72.34 | $73.86 | $2,363.52 | 75 |
| QCOM | 14 | $153.83 | $152.61 | $2,136.54 | 65 |
| T | 77 | $27.09 | $26.99 | $2,078.23 | 65 |
| TGT | 21 | $104.78 | $103.65 | $2,176.65 | 70 |
| TSLA | 6 | $318.51 | $319.41 | $1,916.46 | 65 |
| UNH | 7 | $298.51 | $288.07 | $2,016.49 | 65 |
| UNP | 9 | $237.31 | $227.49 | $2,047.41 | 65 |
| V | 6 | $355.85 | $349.81 | $2,098.86 | 65 |
| VZ | 51 | $40.87 | $40.95 | $2,088.45 | 65 |
| WFC | 28 | $78.77 | $79.71 | $2,231.88 | 70 |
| WMT | 22 | $97.29 | $95.09 | $2,091.98 | 65 |
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
| 2025-07-18 05:57:11 | BUY | INTC | 7 | $22.80 | N/A | 65 |
| 2025-07-18 05:57:11 | BUY | XOM | 1 | $111.66 | N/A | 70 |
| 2025-07-18 05:45:52 | SELL | NVDA | 2 | $173.00 | $2.40 | 70 |
| 2025-07-18 05:45:52 | SELL | CSCO | 2 | $68.30 | $-0.50 | 70 |
| 2025-07-18 05:29:57 | BUY | NVDA | 2 | $173.00 | N/A | 85 |
| 2025-07-18 05:29:57 | BUY | CSCO | 2 | $68.30 | N/A | 75 |
| 2025-07-18 05:13:52 | SELL | AMD | 1 | $160.41 | $0.36 | 70 |
| 2025-07-18 05:13:52 | SELL | CSCO | 2 | $68.30 | $-0.50 | 70 |
| 2025-07-18 05:13:52 | BUY | TGT | 1 | $103.65 | N/A | 70 |
| 2025-07-18 04:50:30 | SELL | NVDA | 1 | $173.00 | $1.29 | 70 |
| 2025-07-18 04:50:30 | SELL | NKE | 1 | $72.98 | $1.00 | 65 |
| 2025-07-18 04:50:30 | BUY | CSCO | 2 | $68.30 | N/A | 75 |
| 2025-07-18 04:29:27 | SELL | NVDA | 1 | $173.00 | $1.20 | 70 |
| 2025-07-18 04:29:27 | SELL | CSCO | 1 | $68.30 | $-0.26 | 70 |
| 2025-07-18 04:29:27 | BUY | AMD | 1 | $160.41 | N/A | 75 |
| 2025-07-18 04:29:27 | BUY | NKE | 1 | $72.98 | N/A | 70 |
| 2025-07-18 04:29:27 | BUY | PFE | 1 | $24.58 | N/A | 65 |
| 2025-07-18 04:29:27 | BUY | WMT | 1 | $95.09 | N/A | 65 |
| 2025-07-18 04:29:27 | BUY | WFC | 1 | $79.71 | N/A | 70 |
| 2025-07-18 04:29:27 | BUY | VZ | 1 | $40.95 | N/A | 65 |
| 2025-07-18 04:06:55 | SELL | INTC | 7 | $22.80 | $2.95 | 60 |
| 2025-07-18 04:06:55 | SELL | NKE | 3 | $72.98 | $2.81 | 65 |
| 2025-07-18 04:06:55 | BUY | AMD | 1 | $160.41 | N/A | 75 |
| 2025-07-18 04:06:55 | BUY | PYPL | 3 | $73.86 | N/A | 75 |
| 2025-07-18 04:06:55 | BUY | WFC | 1 | $79.71 | N/A | 70 |

<!--TRADE_LOG_END--> 
