# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 05:55:31**

| Metric | Value |
|---|---|
| **Total Value** | **$100,371.17** |
| Cash | $654.97 |
| Holdings Value | $99,716.20 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.11 | $2,091.10 | 70 |
| ADBE | 6 | $375.23 | $364.18 | $2,185.08 | 65 |
| AMD | 14 | $144.29 | $155.61 | $2,178.54 | 70 |
| AMZN | 10 | $221.65 | $226.35 | $2,263.50 | 70 |
| AVGO | 8 | $275.34 | $280.94 | $2,247.52 | 70 |
| AXP | 7 | $325.34 | $310.65 | $2,174.55 | 65 |
| BA | 9 | $210.91 | $230.00 | $2,070.00 | 65 |
| BAC | 45 | $46.28 | $46.15 | $2,076.75 | 65 |
| C | 30 | $86.78 | $90.72 | $2,721.60 | 85 |
| CAT | 6 | $397.74 | $404.64 | $2,427.84 | 70 |
| COST | 2 | $979.83 | $967.68 | $1,935.36 | 65 |
| CRM | 8 | $267.44 | $257.58 | $2,060.64 | 65 |
| CSCO | 31 | $68.46 | $67.18 | $2,082.58 | 65 |
| CVX | 16 | $146.78 | $150.69 | $2,411.04 | 75 |
| DIS | 18 | $122.77 | $118.98 | $2,141.64 | 65 |
| GOOGL | 15 | $179.87 | $182.00 | $2,730.00 | 85 |
| GS | 3 | $717.52 | $702.51 | $2,107.53 | 70 |
| HD | 6 | $372.64 | $358.64 | $2,151.84 | 65 |
| INTC | 84 | $22.36 | $22.92 | $1,925.28 | 60 |
| JNJ | 14 | $155.89 | $155.17 | $2,172.38 | 65 |
| JPM | 8 | $292.27 | $286.55 | $2,292.40 | 75 |
| KO | 30 | $70.97 | $69.36 | $2,080.80 | 65 |
| LLY | 3 | $781.32 | $771.75 | $2,315.25 | 65 |
| MA | 4 | $563.08 | $550.36 | $2,201.44 | 65 |
| META | 3 | $717.12 | $710.39 | $2,131.17 | 70 |
| MRK | 26 | $82.50 | $81.52 | $2,119.52 | 65 |
| MSFT | 5 | $498.84 | $505.82 | $2,529.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,260.27 | $1,260.27 | 65 |
| NKE | 33 | $72.03 | $71.99 | $2,375.67 | 75 |
| NVDA | 15 | $171.55 | $170.70 | $2,560.50 | 85 |
| ORCL | 9 | $233.15 | $234.96 | $2,114.64 | 65 |
| PEP | 15 | $136.57 | $133.81 | $2,007.15 | 65 |
| PFE | 84 | $25.28 | $24.61 | $2,067.24 | 65 |
| PG | 14 | $152.15 | $152.68 | $2,137.52 | 65 |
| PYPL | 28 | $72.12 | $72.96 | $2,042.88 | 65 |
| QCOM | 14 | $153.83 | $154.30 | $2,160.20 | 70 |
| T | 77 | $27.09 | $27.02 | $2,080.54 | 65 |
| TGT | 20 | $104.94 | $102.21 | $2,044.20 | 65 |
| TSLA | 6 | $318.51 | $310.78 | $1,864.68 | 65 |
| UNH | 7 | $298.51 | $291.71 | $2,041.97 | 65 |
| UNP | 10 | $236.13 | $231.14 | $2,311.40 | 75 |
| V | 6 | $355.85 | $347.02 | $2,082.12 | 65 |
| VZ | 50 | $43.08 | $41.26 | $2,063.00 | 65 |
| WFC | 28 | $78.90 | $78.86 | $2,208.08 | 70 |
| WMT | 22 | $97.29 | $95.39 | $2,098.58 | 65 |
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
| 2025-07-16 05:55:27 | SELL | WMT | 1 | $95.39 | $-1.82 | 65 |
| 2025-07-16 05:55:27 | SELL | PFE | 1 | $24.61 | $-0.67 | 65 |
| 2025-07-16 05:55:27 | SELL | CVX | 2 | $150.69 | $6.96 | 75 |
| 2025-07-16 05:55:27 | BUY | WFC | 1 | $78.86 | N/A | 70 |
| 2025-07-16 05:44:43 | SELL | PFE | 5 | $24.61 | $-3.15 | 65 |
| 2025-07-16 05:44:43 | SELL | WFC | 1 | $78.86 | $-0.04 | 65 |
| 2025-07-16 05:44:43 | BUY | WMT | 2 | $95.39 | N/A | 70 |
| 2025-07-16 05:44:43 | BUY | CVX | 1 | $150.69 | N/A | 85 |
| 2025-07-16 05:28:50 | SELL | JPM | 1 | $286.55 | $-5.08 | 70 |
| 2025-07-16 05:28:50 | BUY | PFE | 5 | $24.61 | N/A | 70 |
| 2025-07-16 05:28:50 | BUY | PG | 1 | $152.68 | N/A | 70 |
| 2025-07-16 05:28:50 | BUY | CVX | 1 | $150.69 | N/A | 85 |
| 2025-07-16 05:12:47 | SELL | MRK | 1 | $81.52 | $-0.95 | 65 |
| 2025-07-16 05:12:47 | SELL | CSCO | 1 | $67.18 | $-1.24 | 65 |
| 2025-07-16 05:12:47 | SELL | CVX | 2 | $150.69 | $6.96 | 75 |
| 2025-07-16 05:12:47 | BUY | NVDA | 1 | $170.70 | N/A | 85 |
| 2025-07-16 05:12:47 | BUY | NKE | 3 | $71.99 | N/A | 75 |
| 2025-07-16 05:12:47 | BUY | WFC | 1 | $78.86 | N/A | 70 |
| 2025-07-16 04:49:39 | SELL | AMD | 1 | $155.61 | $10.57 | 65 |
| 2025-07-16 04:49:39 | SELL | WFC | 1 | $78.86 | $-0.04 | 65 |
| 2025-07-16 04:49:39 | BUY | MRK | 1 | $81.52 | N/A | 70 |
| 2025-07-16 04:49:39 | BUY | PFE | 1 | $24.61 | N/A | 65 |
| 2025-07-16 04:49:39 | BUY | CVX | 1 | $150.69 | N/A | 85 |
| 2025-07-16 04:29:39 | SELL | NVDA | 1 | $170.70 | $-0.85 | 70 |
| 2025-07-16 04:29:39 | SELL | NKE | 2 | $71.99 | $-0.08 | 65 |

<!--TRADE_LOG_END--> 
