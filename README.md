# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 10:26:33**

| Metric | Value |
|---|---|
| **Total Value** | **$101,424.08** |
| Cash | $714.69 |
| Holdings Value | $100,709.39 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.02 | $2,100.20 | 65 |
| ADBE | 6 | $375.23 | $366.45 | $2,198.70 | 65 |
| AMD | 14 | $160.03 | $160.41 | $2,245.74 | 70 |
| AMZN | 11 | $221.89 | $223.88 | $2,462.68 | 75 |
| AVGO | 8 | $275.34 | $286.45 | $2,291.60 | 65 |
| AXP | 7 | $309.18 | $315.35 | $2,207.45 | 75 |
| BA | 9 | $232.13 | $231.00 | $2,079.00 | 65 |
| BAC | 47 | $46.28 | $47.02 | $2,209.94 | 70 |
| C | 29 | $86.64 | $93.09 | $2,699.61 | 85 |
| CAT | 6 | $397.74 | $418.07 | $2,508.42 | 85 |
| COST | 2 | $979.83 | $953.91 | $1,907.82 | 65 |
| CRM | 8 | $267.44 | $259.88 | $2,079.04 | 65 |
| CSCO | 35 | $68.55 | $68.30 | $2,390.50 | 75 |
| CVX | 16 | $146.84 | $151.38 | $2,422.08 | 75 |
| DIS | 19 | $122.64 | $122.21 | $2,321.99 | 70 |
| GOOGL | 13 | $179.34 | $183.58 | $2,386.54 | 70 |
| GS | 3 | $717.52 | $705.84 | $2,117.52 | 70 |
| HD | 6 | $354.18 | $359.04 | $2,154.24 | 65 |
| INTC | 85 | $22.35 | $22.80 | $1,938.00 | 60 |
| JNJ | 14 | $155.97 | $162.98 | $2,281.72 | 70 |
| JPM | 9 | $291.90 | $289.90 | $2,609.10 | 75 |
| KO | 31 | $70.96 | $70.59 | $2,188.29 | 70 |
| LLY | 3 | $781.32 | $761.50 | $2,284.50 | 65 |
| MA | 4 | $563.08 | $555.61 | $2,222.44 | 65 |
| META | 3 | $717.12 | $701.41 | $2,104.23 | 65 |
| MRK | 26 | $82.68 | $81.52 | $2,119.52 | 65 |
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
| WFC | 29 | $78.80 | $79.71 | $2,311.59 | 70 |
| WMT | 22 | $97.29 | $95.09 | $2,091.98 | 65 |
| XOM | 19 | $109.80 | $111.66 | $2,121.54 | 65 |

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
| 2025-07-18 10:26:27 | SELL | XOM | 1 | $111.66 | $1.76 | 65 |
| 2025-07-18 10:26:27 | SELL | INTC | 6 | $22.80 | $2.53 | 60 |
| 2025-07-18 10:26:27 | SELL | DIS | 3 | $122.21 | $-1.12 | 70 |
| 2025-07-18 10:26:27 | SELL | MRK | 1 | $81.52 | $-1.12 | 65 |
| 2025-07-18 10:26:27 | BUY | BAC | 3 | $47.02 | N/A | 70 |
| 2025-07-18 10:26:27 | BUY | PYPL | 3 | $73.86 | N/A | 75 |
| 2025-07-18 10:26:27 | BUY | KO | 1 | $70.59 | N/A | 70 |
| 2025-07-18 10:26:27 | BUY | VZ | 3 | $40.95 | N/A | 65 |
| 2025-07-18 10:26:27 | BUY | TGT | 1 | $103.65 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
