# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 19:50:58**

| Metric | Value |
|---|---|
| **Total Value** | **$100,518.68** |
| Cash | $622.21 |
| Holdings Value | $99,896.47 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.56 | $2,095.55 | 65 |
| ADBE | 6 | $375.23 | $364.39 | $2,186.34 | 65 |
| AMD | 17 | $146.29 | $155.28 | $2,639.77 | 85 |
| AMZN | 10 | $221.65 | $226.75 | $2,267.50 | 75 |
| AVGO | 8 | $275.34 | $281.55 | $2,252.40 | 70 |
| AXP | 7 | $325.34 | $311.37 | $2,179.59 | 70 |
| BA | 9 | $210.91 | $230.63 | $2,075.67 | 65 |
| BAC | 45 | $46.28 | $46.09 | $2,074.05 | 65 |
| C | 30 | $86.78 | $91.14 | $2,734.05 | 85 |
| CAT | 6 | $397.74 | $404.32 | $2,425.95 | 80 |
| COST | 2 | $979.83 | $968.05 | $1,936.11 | 65 |
| CRM | 8 | $267.44 | $257.68 | $2,061.40 | 65 |
| CSCO | 31 | $68.46 | $67.19 | $2,082.89 | 65 |
| CVX | 17 | $147.01 | $150.78 | $2,563.18 | 85 |
| DIS | 18 | $122.77 | $119.25 | $2,146.41 | 65 |
| GOOGL | 14 | $179.71 | $183.47 | $2,568.58 | 85 |
| GS | 3 | $717.52 | $703.91 | $2,111.73 | 70 |
| HD | 6 | $372.64 | $358.88 | $2,153.25 | 65 |
| INTC | 89 | $22.39 | $22.96 | $2,043.88 | 65 |
| JNJ | 13 | $155.95 | $155.37 | $2,019.81 | 65 |
| JPM | 9 | $291.63 | $286.61 | $2,579.49 | 85 |
| KO | 30 | $70.97 | $69.45 | $2,083.50 | 65 |
| LLY | 3 | $781.32 | $772.74 | $2,318.22 | 65 |
| MA | 4 | $563.08 | $551.00 | $2,204.00 | 65 |
| META | 3 | $717.12 | $712.47 | $2,137.41 | 70 |
| MRK | 26 | $82.50 | $81.67 | $2,123.42 | 65 |
| MSFT | 5 | $498.84 | $506.69 | $2,533.45 | 75 |
| NFLX | 1 | $1,279.00 | $1,261.59 | $1,261.59 | 65 |
| NKE | 30 | $72.03 | $72.05 | $2,161.50 | 70 |
| NVDA | 15 | $171.55 | $170.75 | $2,561.18 | 85 |
| ORCL | 9 | $233.15 | $235.17 | $2,116.53 | 65 |
| PEP | 15 | $136.57 | $134.20 | $2,013.00 | 65 |
| PFE | 84 | $25.28 | $24.61 | $2,066.82 | 65 |
| PG | 13 | $152.11 | $152.85 | $1,987.05 | 65 |
| PYPL | 28 | $72.12 | $73.21 | $2,049.88 | 65 |
| QCOM | 14 | $153.83 | $154.69 | $2,165.66 | 70 |
| T | 76 | $27.09 | $27.02 | $2,053.90 | 65 |
| TGT | 20 | $104.94 | $102.75 | $2,054.90 | 65 |
| TSLA | 6 | $318.51 | $311.76 | $1,870.58 | 65 |
| UNH | 7 | $298.51 | $292.12 | $2,044.86 | 65 |
| UNP | 10 | $236.13 | $231.37 | $2,313.70 | 75 |
| V | 6 | $355.85 | $347.42 | $2,084.52 | 65 |
| VZ | 50 | $43.08 | $41.31 | $2,065.50 | 65 |
| WFC | 26 | $78.90 | $78.78 | $2,048.15 | 65 |
| WMT | 21 | $97.38 | $95.53 | $2,006.23 | 65 |
| XOM | 21 | $110.02 | $113.02 | $2,373.32 | 75 |

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
| 2025-07-15 19:50:51 | SELL | BA | 1 | $230.63 | $17.75 | 65 |
| 2025-07-15 19:50:51 | SELL | WFC | 2 | $78.74 | $-0.30 | 65 |
| 2025-07-15 19:50:51 | BUY | INTC | 6 | $22.96 | N/A | 65 |
| 2025-07-15 19:50:51 | BUY | UNP | 1 | $231.37 | N/A | 75 |
| 2025-07-15 19:36:59 | SELL | INTC | 6 | $23.00 | $3.61 | 60 |
| 2025-07-15 19:36:59 | SELL | PFE | 1 | $24.57 | $-0.71 | 65 |
| 2025-07-15 19:36:59 | BUY | NKE | 1 | $71.93 | N/A | 70 |
| 2025-07-15 19:36:59 | BUY | WFC | 1 | $78.79 | N/A | 70 |
| 2025-07-15 19:36:59 | BUY | CVX | 1 | $150.78 | N/A | 85 |
| 2025-07-15 19:25:11 | SELL | BAC | 3 | $46.37 | $0.24 | 65 |
| 2025-07-15 19:25:11 | SELL | NKE | 1 | $71.90 | $-0.13 | 65 |
| 2025-07-15 19:25:11 | SELL | PFE | 3 | $24.57 | $-2.06 | 65 |
| 2025-07-15 19:25:11 | SELL | CVX | 1 | $150.88 | $3.87 | 75 |
| 2025-07-15 19:25:11 | BUY | NVDA | 2 | $170.14 | N/A | 85 |
| 2025-07-15 19:25:11 | BUY | VZ | 3 | $41.33 | N/A | 65 |
| 2025-07-15 19:08:22 | SELL | AMZN | 1 | $226.20 | $4.14 | 70 |
| 2025-07-15 19:08:22 | SELL | MRK | 1 | $81.50 | $-0.97 | 65 |
| 2025-07-15 19:08:22 | SELL | BA | 1 | $231.14 | $16.60 | 70 |
| 2025-07-15 19:08:22 | SELL | WFC | 1 | $78.33 | $-0.54 | 65 |
| 2025-07-15 19:08:22 | SELL | UNP | 1 | $231.50 | $-4.64 | 65 |
| 2025-07-15 19:08:22 | SELL | VZ | 3 | $41.31 | $-5.29 | 60 |
| 2025-07-15 19:08:22 | BUY | BAC | 3 | $46.24 | N/A | 70 |
| 2025-07-15 19:08:22 | BUY | PFE | 4 | $25.35 | N/A | 70 |
| 2025-07-15 19:08:22 | BUY | CVX | 1 | $150.71 | N/A | 85 |
| 2025-07-15 18:47:03 | SELL | BAC | 2 | $46.28 | $-0.03 | 65 |

<!--TRADE_LOG_END--> 
