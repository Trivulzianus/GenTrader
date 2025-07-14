# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 19:25:11**

| Metric | Value |
|---|---|
| **Total Value** | **$100,836.59** |
| Cash | $1,112.01 |
| Holdings Value | $99,724.59 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.20 | $2,092.00 | 65 |
| ADBE | 6 | $375.23 | $366.85 | $2,201.10 | 65 |
| AMD | 14 | $133.90 | $146.51 | $2,051.21 | 70 |
| AMZN | 10 | $221.60 | $225.27 | $2,252.70 | 70 |
| AVGO | 8 | $275.34 | $275.88 | $2,207.04 | 70 |
| AXP | 7 | $325.34 | $320.19 | $2,241.33 | 75 |
| BA | 10 | $212.67 | $230.05 | $2,300.51 | 70 |
| BAC | 56 | $48.43 | $46.96 | $2,629.76 | 85 |
| C | 30 | $86.60 | $87.20 | $2,616.15 | 85 |
| CAT | 6 | $397.74 | $405.12 | $2,430.75 | 70 |
| COST | 2 | $979.83 | $977.97 | $1,955.94 | 70 |
| CRM | 7 | $268.68 | $259.99 | $1,819.93 | 65 |
| CSCO | 32 | $68.45 | $67.70 | $2,166.56 | 70 |
| CVX | 16 | $146.79 | $152.24 | $2,435.84 | 75 |
| DIS | 17 | $122.95 | $120.16 | $2,042.72 | 65 |
| GOOGL | 12 | $179.42 | $181.35 | $2,176.26 | 70 |
| GS | 3 | $717.52 | $711.27 | $2,133.81 | 85 |
| HD | 6 | $372.64 | $369.52 | $2,217.12 | 70 |
| INTC | 80 | $22.30 | $23.30 | $1,864.00 | 60 |
| JNJ | 13 | $155.95 | $156.48 | $2,034.24 | 65 |
| JPM | 9 | $291.63 | $288.33 | $2,594.97 | 85 |
| KO | 29 | $71.03 | $69.33 | $2,010.43 | 65 |
| LLY | 3 | $781.32 | $797.41 | $2,392.24 | 70 |
| MA | 4 | $563.08 | $553.05 | $2,212.20 | 65 |
| META | 3 | $717.12 | $721.19 | $2,163.57 | 85 |
| MRK | 28 | $82.50 | $83.75 | $2,345.00 | 75 |
| MSFT | 5 | $498.84 | $503.20 | $2,516.02 | 85 |
| NFLX | 1 | $1,279.00 | $1,265.06 | $1,265.06 | 65 |
| NKE | 28 | $72.03 | $72.27 | $2,023.42 | 65 |
| NVDA | 16 | $157.66 | $164.52 | $2,632.25 | 85 |
| ORCL | 9 | $233.27 | $229.53 | $2,065.77 | 65 |
| PEP | 15 | $136.57 | $135.60 | $2,034.07 | 65 |
| PFE | 86 | $25.21 | $25.41 | $2,185.69 | 70 |
| PG | 13 | $160.78 | $154.19 | $2,004.47 | 65 |
| PYPL | 29 | $72.14 | $73.73 | $2,138.17 | 70 |
| QCOM | 14 | $153.83 | $154.35 | $2,160.90 | 65 |
| T | 75 | $27.10 | $27.23 | $2,041.88 | 65 |
| TGT | 20 | $104.94 | $104.63 | $2,092.60 | 70 |
| TSLA | 6 | $288.62 | $315.93 | $1,895.55 | 65 |
| UNH | 7 | $298.51 | $300.21 | $2,101.47 | 65 |
| UNP | 9 | $236.57 | $233.59 | $2,102.31 | 75 |
| V | 6 | $355.85 | $350.50 | $2,103.00 | 65 |
| VZ | 49 | $43.12 | $41.70 | $2,043.06 | 65 |
| WFC | 28 | $82.26 | $83.24 | $2,330.77 | 75 |
| WMT | 21 | $97.38 | $95.52 | $2,005.82 | 65 |
| XOM | 21 | $110.01 | $114.05 | $2,394.95 | 75 |

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
| 2025-07-14 19:25:06 | SELL | GOOGL | 2 | $181.36 | $3.33 | 70 |
| 2025-07-14 19:25:06 | SELL | AMZN | 1 | $225.28 | $3.35 | 70 |
| 2025-07-14 19:25:06 | SELL | DIS | 1 | $120.17 | $-2.63 | 65 |
| 2025-07-14 19:25:06 | SELL | MRK | 3 | $83.75 | $3.38 | 75 |
| 2025-07-14 19:25:06 | SELL | CVX | 1 | $152.24 | $5.13 | 75 |
| 2025-07-14 19:25:06 | BUY | BAC | 6 | $46.97 | N/A | 85 |
| 2025-07-14 19:25:06 | BUY | PYPL | 1 | $73.72 | N/A | 70 |
| 2025-07-14 19:25:06 | BUY | C | 4 | $87.22 | N/A | 85 |
| 2025-07-14 19:25:06 | BUY | CSCO | 2 | $67.71 | N/A | 70 |
| 2025-07-14 19:08:29 | SELL | AMD | 2 | $146.57 | $22.17 | 65 |
| 2025-07-14 19:08:29 | SELL | PYPL | 3 | $73.81 | $4.67 | 65 |
| 2025-07-14 19:08:29 | SELL | C | 4 | $87.32 | $2.81 | 70 |
| 2025-07-14 19:08:29 | SELL | UNP | 1 | $233.77 | $-2.52 | 65 |
| 2025-07-14 19:08:29 | BUY | AMZN | 1 | $225.41 | N/A | 80 |
| 2025-07-14 19:08:29 | BUY | BAC | 3 | $46.99 | N/A | 75 |
| 2025-07-14 19:08:29 | BUY | MRK | 3 | $83.76 | N/A | 85 |
| 2025-07-14 19:08:29 | BUY | T | 1 | $27.22 | N/A | 65 |
| 2025-07-14 19:08:29 | BUY | CVX | 1 | $152.49 | N/A | 85 |
| 2025-07-14 18:47:08 | SELL | AMZN | 1 | $225.33 | $3.41 | 70 |
| 2025-07-14 18:47:08 | SELL | INTC | 6 | $23.35 | $5.88 | 60 |
| 2025-07-14 18:47:08 | SELL | NKE | 4 | $72.25 | $0.79 | 65 |
| 2025-07-14 18:47:08 | SELL | MRK | 3 | $83.85 | $3.68 | 75 |
| 2025-07-14 18:47:08 | SELL | CSCO | 1 | $67.78 | $-0.70 | 65 |
| 2025-07-14 18:47:08 | BUY | NVDA | 1 | $164.79 | N/A | 85 |
| 2025-07-14 18:47:08 | BUY | DIS | 1 | $120.40 | N/A | 70 |

<!--TRADE_LOG_END--> 
