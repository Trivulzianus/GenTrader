# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 18:47:16**

| Metric | Value |
|---|---|
| **Total Value** | **$100,879.26** |
| Cash | $540.00 |
| Holdings Value | $100,339.25 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.32 | $2,093.20 | 65 |
| ADBE | 6 | $375.23 | $366.05 | $2,196.30 | 65 |
| AMD | 16 | $135.48 | $146.50 | $2,343.92 | 75 |
| AMZN | 10 | $221.58 | $225.33 | $2,253.30 | 70 |
| AVGO | 8 | $275.34 | $275.75 | $2,206.00 | 70 |
| AXP | 7 | $325.34 | $320.57 | $2,244.03 | 70 |
| BA | 10 | $212.67 | $230.09 | $2,300.90 | 70 |
| BAC | 47 | $48.71 | $46.97 | $2,207.36 | 70 |
| C | 30 | $86.61 | $87.18 | $2,615.40 | 85 |
| CAT | 6 | $397.74 | $404.93 | $2,429.58 | 75 |
| COST | 2 | $979.83 | $977.47 | $1,954.94 | 65 |
| CRM | 7 | $268.68 | $260.98 | $1,826.86 | 65 |
| CSCO | 30 | $68.50 | $67.77 | $2,033.17 | 65 |
| CVX | 16 | $146.78 | $152.51 | $2,440.16 | 75 |
| DIS | 18 | $122.79 | $120.40 | $2,167.20 | 70 |
| GOOGL | 14 | $179.69 | $181.72 | $2,544.01 | 85 |
| GS | 3 | $717.52 | $711.18 | $2,133.54 | 85 |
| HD | 6 | $372.64 | $369.30 | $2,215.80 | 65 |
| INTC | 80 | $22.30 | $23.36 | $1,868.40 | 60 |
| JNJ | 13 | $155.95 | $156.59 | $2,035.67 | 65 |
| JPM | 9 | $291.63 | $288.20 | $2,593.80 | 85 |
| KO | 29 | $71.03 | $69.45 | $2,014.19 | 65 |
| LLY | 3 | $781.32 | $794.25 | $2,382.76 | 70 |
| MA | 4 | $563.08 | $554.32 | $2,217.26 | 65 |
| META | 3 | $717.12 | $722.94 | $2,168.82 | 85 |
| MRK | 28 | $82.49 | $83.84 | $2,347.52 | 75 |
| MSFT | 5 | $498.84 | $503.11 | $2,515.55 | 80 |
| NFLX | 1 | $1,279.00 | $1,267.45 | $1,267.45 | 65 |
| NKE | 28 | $72.03 | $72.24 | $2,022.72 | 65 |
| NVDA | 16 | $157.66 | $164.79 | $2,636.72 | 85 |
| ORCL | 9 | $233.27 | $229.32 | $2,063.88 | 70 |
| PEP | 15 | $136.57 | $135.61 | $2,034.15 | 65 |
| PFE | 86 | $25.21 | $25.44 | $2,187.84 | 70 |
| PG | 13 | $160.78 | $154.27 | $2,005.54 | 65 |
| PYPL | 31 | $72.25 | $73.75 | $2,286.25 | 75 |
| QCOM | 14 | $153.83 | $154.45 | $2,162.30 | 65 |
| T | 74 | $27.10 | $27.23 | $2,015.39 | 65 |
| TGT | 20 | $104.94 | $104.70 | $2,094.00 | 65 |
| TSLA | 6 | $288.62 | $315.70 | $1,894.20 | 60 |
| UNH | 7 | $298.51 | $300.23 | $2,101.61 | 65 |
| UNP | 10 | $236.29 | $233.69 | $2,336.90 | 75 |
| V | 6 | $355.85 | $351.02 | $2,106.12 | 65 |
| VZ | 49 | $43.12 | $41.69 | $2,042.81 | 65 |
| WFC | 28 | $82.26 | $83.25 | $2,330.86 | 75 |
| WMT | 21 | $97.38 | $95.53 | $2,006.03 | 65 |
| XOM | 21 | $110.01 | $114.04 | $2,394.84 | 80 |

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
| 2025-07-14 18:47:08 | SELL | AMZN | 1 | $225.33 | $3.41 | 70 |
| 2025-07-14 18:47:08 | SELL | INTC | 6 | $23.35 | $5.88 | 60 |
| 2025-07-14 18:47:08 | SELL | NKE | 4 | $72.25 | $0.79 | 65 |
| 2025-07-14 18:47:08 | SELL | MRK | 3 | $83.85 | $3.68 | 75 |
| 2025-07-14 18:47:08 | SELL | CSCO | 1 | $67.78 | $-0.70 | 65 |
| 2025-07-14 18:47:08 | BUY | NVDA | 1 | $164.79 | N/A | 85 |
| 2025-07-14 18:47:08 | BUY | DIS | 1 | $120.40 | N/A | 70 |
| 2025-07-14 18:47:08 | BUY | C | 3 | $87.18 | N/A | 85 |
| 2025-07-14 18:28:00 | SELL | DIS | 1 | $120.43 | $-2.37 | 65 |
| 2025-07-14 18:28:00 | SELL | PFE | 4 | $25.48 | $1.03 | 70 |
| 2025-07-14 18:28:00 | SELL | C | 3 | $87.23 | $1.84 | 75 |
| 2025-07-14 18:28:00 | SELL | CVX | 1 | $152.30 | $5.20 | 75 |
| 2025-07-14 18:28:00 | BUY | NKE | 4 | $72.24 | N/A | 75 |
| 2025-07-14 18:28:00 | BUY | PYPL | 3 | $73.49 | N/A | 75 |
| 2025-07-14 18:28:00 | BUY | MRK | 1 | $83.81 | N/A | 85 |
| 2025-07-14 18:28:00 | BUY | CSCO | 1 | $67.88 | N/A | 70 |
| 2025-07-14 18:11:32 | SELL | MRK | 1 | $83.78 | $1.15 | 80 |
| 2025-07-14 18:11:32 | SELL | ORCL | 1 | $229.99 | $-2.94 | 65 |
| 2025-07-14 18:11:32 | SELL | CSCO | 1 | $67.86 | $-0.61 | 65 |
| 2025-07-14 18:11:32 | BUY | PFE | 6 | $25.49 | N/A | 75 |
| 2025-07-14 18:11:32 | BUY | C | 3 | $87.28 | N/A | 85 |
| 2025-07-14 18:11:32 | BUY | CVX | 1 | $152.13 | N/A | 85 |
| 2025-07-14 17:52:02 | SELL | PYPL | 3 | $73.68 | $4.26 | 65 |
| 2025-07-14 17:52:02 | BUY | NVDA | 1 | $164.99 | N/A | 85 |
| 2025-07-14 17:52:02 | BUY | PFE | 5 | $25.51 | N/A | 70 |

<!--TRADE_LOG_END--> 
