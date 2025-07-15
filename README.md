# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 23:26:04**

| Metric | Value |
|---|---|
| **Total Value** | **$100,371.17** |
| Cash | $296.80 |
| Holdings Value | $100,074.37 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.11 | $2,091.10 | 65 |
| ADBE | 6 | $375.23 | $364.18 | $2,185.08 | 65 |
| AMD | 15 | $145.04 | $155.61 | $2,334.15 | 75 |
| AMZN | 10 | $221.65 | $226.35 | $2,263.50 | 70 |
| AVGO | 8 | $275.34 | $280.94 | $2,247.52 | 70 |
| AXP | 7 | $325.34 | $310.65 | $2,174.55 | 65 |
| BA | 10 | $212.82 | $230.00 | $2,300.00 | 70 |
| BAC | 45 | $46.28 | $46.15 | $2,076.75 | 65 |
| C | 30 | $86.78 | $90.72 | $2,721.60 | 85 |
| CAT | 6 | $397.74 | $404.64 | $2,427.84 | 70 |
| COST | 2 | $979.83 | $967.68 | $1,935.36 | 65 |
| CRM | 8 | $267.44 | $257.58 | $2,060.64 | 65 |
| CSCO | 31 | $68.46 | $67.18 | $2,082.58 | 65 |
| CVX | 18 | $147.21 | $150.69 | $2,712.42 | 85 |
| DIS | 18 | $122.77 | $118.98 | $2,141.64 | 65 |
| GOOGL | 14 | $179.71 | $182.00 | $2,548.00 | 85 |
| GS | 3 | $717.52 | $702.51 | $2,107.53 | 70 |
| HD | 6 | $372.64 | $358.64 | $2,151.84 | 65 |
| INTC | 84 | $22.36 | $22.92 | $1,925.28 | 60 |
| JNJ | 14 | $155.89 | $155.17 | $2,172.38 | 65 |
| JPM | 9 | $291.63 | $286.55 | $2,578.95 | 85 |
| KO | 30 | $70.97 | $69.36 | $2,080.80 | 65 |
| LLY | 3 | $781.32 | $771.75 | $2,315.25 | 65 |
| MA | 4 | $563.08 | $550.36 | $2,201.44 | 65 |
| META | 3 | $717.12 | $710.39 | $2,131.17 | 70 |
| MRK | 26 | $82.50 | $81.52 | $2,119.52 | 65 |
| MSFT | 5 | $498.84 | $505.82 | $2,529.10 | 75 |
| NFLX | 1 | $1,279.00 | $1,260.27 | $1,260.27 | 65 |
| NKE | 33 | $72.03 | $71.99 | $2,375.67 | 75 |
| NVDA | 13 | $171.69 | $170.70 | $2,219.10 | 70 |
| ORCL | 10 | $233.33 | $234.96 | $2,349.60 | 70 |
| PEP | 15 | $136.57 | $133.81 | $2,007.15 | 65 |
| PFE | 84 | $25.28 | $24.61 | $2,067.24 | 65 |
| PG | 13 | $152.11 | $152.68 | $1,984.84 | 65 |
| PYPL | 28 | $72.12 | $72.96 | $2,042.88 | 65 |
| QCOM | 14 | $153.83 | $154.30 | $2,160.20 | 65 |
| T | 77 | $27.09 | $27.02 | $2,080.54 | 65 |
| TGT | 20 | $104.94 | $102.21 | $2,044.20 | 65 |
| TSLA | 6 | $318.51 | $310.78 | $1,864.68 | 65 |
| UNH | 7 | $298.51 | $291.71 | $2,041.97 | 65 |
| UNP | 10 | $236.13 | $231.14 | $2,311.40 | 75 |
| V | 6 | $355.85 | $347.02 | $2,082.12 | 65 |
| VZ | 50 | $43.08 | $41.26 | $2,063.00 | 65 |
| WFC | 27 | $78.90 | $78.86 | $2,129.22 | 65 |
| WMT | 21 | $97.38 | $95.39 | $2,003.19 | 65 |
| XOM | 21 | $110.02 | $112.91 | $2,371.11 | 75 |

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
| 2025-07-15 23:25:56 | SELL | INTC | 6 | $22.92 | $3.14 | 60 |
| 2025-07-15 23:25:56 | BUY | JPM | 1 | $286.55 | N/A | 85 |
| 2025-07-15 23:08:01 | SELL | JPM | 1 | $286.55 | $-5.08 | 70 |
| 2025-07-15 23:08:01 | BUY | CVX | 2 | $150.69 | N/A | 85 |
| 2025-07-15 22:51:51 | SELL | BAC | 1 | $46.15 | $-0.13 | 65 |
| 2025-07-15 22:51:51 | SELL | WFC | 1 | $78.86 | $-0.04 | 65 |
| 2025-07-15 22:51:51 | SELL | CVX | 2 | $150.69 | $6.96 | 75 |
| 2025-07-15 22:51:51 | BUY | INTC | 6 | $22.92 | N/A | 65 |
| 2025-07-15 22:40:33 | BUY | WFC | 1 | $78.86 | N/A | 70 |
| 2025-07-15 22:26:29 | SELL | BAC | 2 | $46.15 | $-0.24 | 65 |
| 2025-07-15 22:26:29 | SELL | AMD | 1 | $155.61 | $9.91 | 70 |
| 2025-07-15 22:26:29 | SELL | INTC | 5 | $22.92 | $2.64 | 60 |
| 2025-07-15 22:26:29 | BUY | NKE | 1 | $71.99 | N/A | 75 |
| 2025-07-15 22:26:29 | BUY | CVX | 1 | $150.69 | N/A | 85 |
| 2025-07-15 22:26:29 | BUY | T | 1 | $27.02 | N/A | 65 |
| 2025-07-15 22:08:25 | SELL | CSCO | 2 | $67.18 | $-2.40 | 65 |
| 2025-07-15 22:08:25 | SELL | CVX | 1 | $150.69 | $3.48 | 80 |
| 2025-07-15 22:08:25 | BUY | INTC | 5 | $22.92 | N/A | 65 |
| 2025-07-15 22:08:25 | BUY | BAC | 3 | $46.15 | N/A | 70 |
| 2025-07-15 22:08:25 | BUY | NKE | 3 | $71.99 | N/A | 75 |
| 2025-07-15 22:08:25 | BUY | BA | 1 | $230.00 | N/A | 75 |
| 2025-07-15 21:50:36 | SELL | AMD | 1 | $155.61 | $9.32 | 75 |
| 2025-07-15 21:50:36 | SELL | INTC | 5 | $22.92 | $2.64 | 60 |
| 2025-07-15 21:50:36 | SELL | NKE | 1 | $71.99 | $-0.04 | 65 |
| 2025-07-15 21:50:36 | BUY | CSCO | 2 | $67.18 | N/A | 70 |

<!--TRADE_LOG_END--> 
