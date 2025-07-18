# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 10:09:19**

| Metric | Value |
|---|---|
| **Total Value** | **$101,424.08** |
| Cash | $677.81 |
| Holdings Value | $100,746.27 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.02 | $2,100.20 | 65 |
| ADBE | 6 | $375.23 | $366.45 | $2,198.70 | 65 |
| AMD | 14 | $160.03 | $160.41 | $2,245.74 | 70 |
| AMZN | 11 | $221.89 | $223.88 | $2,462.68 | 75 |
| AVGO | 8 | $275.34 | $286.45 | $2,291.60 | 65 |
| AXP | 7 | $309.18 | $315.35 | $2,207.45 | 75 |
| BA | 9 | $232.13 | $231.00 | $2,079.00 | 70 |
| BAC | 44 | $46.23 | $47.02 | $2,068.88 | 65 |
| C | 29 | $86.64 | $93.09 | $2,699.61 | 85 |
| CAT | 6 | $397.74 | $418.07 | $2,508.42 | 70 |
| COST | 2 | $979.83 | $953.91 | $1,907.82 | 65 |
| CRM | 8 | $267.44 | $259.88 | $2,079.04 | 65 |
| CSCO | 35 | $68.55 | $68.30 | $2,390.50 | 75 |
| CVX | 16 | $146.84 | $151.38 | $2,422.08 | 75 |
| DIS | 22 | $122.58 | $122.21 | $2,688.62 | 85 |
| GOOGL | 13 | $179.34 | $183.58 | $2,386.54 | 70 |
| GS | 3 | $717.52 | $705.84 | $2,117.52 | 75 |
| HD | 6 | $354.18 | $359.04 | $2,154.24 | 65 |
| INTC | 91 | $22.38 | $22.80 | $2,074.80 | 65 |
| JNJ | 14 | $155.97 | $162.98 | $2,281.72 | 70 |
| JPM | 9 | $291.90 | $289.90 | $2,609.10 | 75 |
| KO | 30 | $70.97 | $70.59 | $2,117.70 | 65 |
| LLY | 3 | $781.32 | $761.50 | $2,284.50 | 65 |
| MA | 4 | $563.08 | $555.61 | $2,222.44 | 65 |
| META | 3 | $717.12 | $701.41 | $2,104.23 | 65 |
| MRK | 27 | $82.64 | $81.52 | $2,201.04 | 70 |
| MSFT | 5 | $498.84 | $511.70 | $2,558.50 | 70 |
| NFLX | 1 | $1,279.00 | $1,274.17 | $1,274.17 | 65 |
| NKE | 29 | $71.95 | $72.98 | $2,116.42 | 65 |
| NVDA | 13 | $171.61 | $173.00 | $2,249.00 | 70 |
| ORCL | 9 | $232.91 | $248.75 | $2,238.75 | 70 |
| PEP | 15 | $135.89 | $145.44 | $2,181.60 | 70 |
| PFE | 85 | $25.27 | $24.58 | $2,089.30 | 65 |
| PG | 13 | $151.91 | $155.62 | $2,023.06 | 65 |
| PYPL | 29 | $72.18 | $73.86 | $2,141.94 | 65 |
| QCOM | 14 | $153.83 | $152.61 | $2,136.54 | 65 |
| T | 77 | $27.09 | $26.99 | $2,078.23 | 65 |
| TGT | 20 | $104.83 | $103.65 | $2,073.00 | 65 |
| TSLA | 6 | $318.51 | $319.41 | $1,916.46 | 65 |
| UNH | 7 | $298.51 | $288.07 | $2,016.49 | 65 |
| UNP | 9 | $237.31 | $227.49 | $2,047.41 | 65 |
| V | 6 | $355.85 | $349.81 | $2,098.86 | 65 |
| VZ | 48 | $40.87 | $40.95 | $1,965.60 | 60 |
| WFC | 29 | $78.80 | $79.71 | $2,311.59 | 70 |
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
| 2025-07-18 10:09:11 | SELL | NKE | 4 | $72.98 | $3.63 | 65 |
| 2025-07-18 10:09:11 | SELL | PYPL | 3 | $73.86 | $4.56 | 65 |
| 2025-07-18 10:09:11 | SELL | WFC | 1 | $79.71 | $0.88 | 70 |
| 2025-07-18 10:09:11 | SELL | VZ | 3 | $40.95 | $0.24 | 60 |
| 2025-07-18 10:09:11 | BUY | XOM | 1 | $111.66 | N/A | 70 |
| 2025-07-18 10:09:11 | BUY | DIS | 3 | $122.21 | N/A | 85 |
| 2025-07-18 10:09:11 | BUY | MRK | 1 | $81.52 | N/A | 70 |
| 2025-07-18 10:09:11 | BUY | CSCO | 2 | $68.30 | N/A | 75 |
| 2025-07-18 09:53:39 | SELL | CSCO | 2 | $68.30 | $-0.50 | 70 |
| 2025-07-18 09:53:39 | BUY | INTC | 6 | $22.80 | N/A | 65 |
| 2025-07-18 09:53:39 | BUY | NKE | 4 | $72.98 | N/A | 75 |
| 2025-07-18 09:53:39 | BUY | WFC | 2 | $79.71 | N/A | 75 |
| 2025-07-18 09:42:19 | SELL | XOM | 1 | $111.66 | $1.76 | 65 |
| 2025-07-18 09:42:19 | SELL | MRK | 3 | $81.52 | $-3.12 | 65 |
| 2025-07-18 09:42:19 | BUY | WFC | 1 | $79.71 | N/A | 70 |
| 2025-07-18 09:42:19 | BUY | CSCO | 2 | $68.30 | N/A | 75 |
| 2025-07-18 09:28:28 | SELL | INTC | 1 | $22.80 | $0.45 | 60 |
| 2025-07-18 09:28:28 | SELL | CSCO | 2 | $68.30 | $-0.50 | 70 |
| 2025-07-18 09:28:28 | BUY | JNJ | 1 | $162.98 | N/A | 75 |
| 2025-07-18 09:28:28 | BUY | MRK | 3 | $81.52 | N/A | 75 |
| 2025-07-18 09:12:21 | SELL | INTC | 5 | $22.80 | $2.11 | 60 |
| 2025-07-18 09:12:21 | SELL | WFC | 2 | $79.71 | $1.82 | 65 |
| 2025-07-18 09:12:21 | SELL | MRK | 3 | $81.52 | $-3.12 | 65 |
| 2025-07-18 08:57:35 | BUY | XOM | 1 | $111.66 | N/A | 70 |
| 2025-07-18 08:44:19 | SELL | XOM | 1 | $111.66 | $1.76 | 65 |

<!--TRADE_LOG_END--> 
