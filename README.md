# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 19:24:34**

| Metric | Value |
|---|---|
| **Total Value** | **$101,468.90** |
| Cash | $2,033.55 |
| Holdings Value | $99,435.35 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.68 | $2,126.80 | 70 |
| ADBE | 5 | $377.60 | $371.83 | $1,859.17 | 65 |
| AMD | 16 | $135.55 | $143.65 | $2,298.40 | 75 |
| AMZN | 11 | $221.97 | $222.03 | $2,442.33 | 75 |
| AVGO | 8 | $275.34 | $275.65 | $2,205.18 | 70 |
| AXP | 7 | $325.28 | $325.50 | $2,278.50 | 75 |
| BA | 10 | $212.37 | $225.53 | $2,255.30 | 70 |
| BAC | 47 | $48.68 | $46.88 | $2,203.12 | 70 |
| C | 27 | $86.80 | $86.83 | $2,344.54 | 75 |
| CAT | 6 | $397.86 | $408.77 | $2,452.62 | 85 |
| COST | 2 | $979.83 | $976.78 | $1,953.56 | 65 |
| CRM | 7 | $268.68 | $264.91 | $1,854.38 | 65 |
| CSCO | 34 | $68.38 | $68.81 | $2,339.37 | 75 |
| CVX | 17 | $147.15 | $153.74 | $2,613.58 | 85 |
| DIS | 18 | $122.80 | $121.10 | $2,179.79 | 70 |
| GOOGL | 13 | $179.61 | $177.76 | $2,310.94 | 75 |
| GS | 3 | $717.52 | $709.42 | $2,128.26 | 75 |
| HD | 6 | $372.64 | $375.98 | $2,255.88 | 65 |
| INTC | 85 | $22.34 | $23.83 | $2,025.55 | 65 |
| JNJ | 13 | $155.89 | $157.66 | $2,049.58 | 65 |
| JPM | 9 | $291.61 | $288.03 | $2,592.24 | 85 |
| KO | 29 | $71.03 | $69.69 | $2,020.87 | 65 |
| LLY | 2 | $776.66 | $793.21 | $1,586.41 | 70 |
| MA | 4 | $563.08 | $564.12 | $2,256.46 | 65 |
| META | 3 | $717.12 | $725.65 | $2,176.95 | 75 |
| MRK | 28 | $82.46 | $84.54 | $2,367.15 | 75 |
| MSFT | 5 | $498.84 | $501.55 | $2,507.75 | 85 |
| NFLX | 1 | $1,279.00 | $1,253.11 | $1,253.11 | 65 |
| NKE | 29 | $75.83 | $74.61 | $2,163.55 | 70 |
| NVDA | 16 | $157.38 | $164.05 | $2,624.80 | 85 |
| ORCL | 9 | $233.31 | $236.17 | $2,125.53 | 70 |
| PEP | 15 | $136.57 | $136.00 | $2,040.00 | 65 |
| PFE | 84 | $25.18 | $25.84 | $2,170.14 | 70 |
| PG | 13 | $160.78 | $158.57 | $2,061.40 | 65 |
| PYPL | 27 | $76.77 | $75.69 | $2,043.63 | 65 |
| QCOM | 15 | $161.72 | $159.29 | $2,389.35 | 75 |
| T | 73 | $28.55 | $27.64 | $2,018.09 | 65 |
| TGT | 20 | $104.92 | $105.75 | $2,115.00 | 65 |
| TSLA | 6 | $288.62 | $309.10 | $1,854.58 | 60 |
| UNH | 6 | $298.34 | $301.18 | $1,807.08 | 65 |
| UNP | 9 | $236.20 | $237.66 | $2,138.94 | 65 |
| V | 6 | $355.85 | $356.62 | $2,139.69 | 65 |
| VZ | 48 | $43.15 | $42.05 | $2,018.16 | 65 |
| WFC | 29 | $82.30 | $82.32 | $2,387.28 | 75 |
| WMT | 21 | $97.36 | $95.08 | $1,996.78 | 65 |
| XOM | 21 | $109.91 | $114.45 | $2,403.55 | 75 |

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
| 2025-07-10 19:24:29 | SELL | BAC | 2 | $46.88 | $-3.46 | 70 |
| 2025-07-10 19:24:29 | SELL | PYPL | 3 | $75.69 | $-2.90 | 65 |
| 2025-07-10 19:24:29 | SELL | C | 3 | $86.83 | $0.10 | 75 |
| 2025-07-10 19:24:29 | BUY | NVDA | 2 | $162.88 | N/A | 85 |
| 2025-07-10 19:24:29 | BUY | INTC | 11 | $23.84 | N/A | 65 |
| 2025-07-10 19:24:29 | BUY | CSCO | 1 | $68.81 | N/A | 75 |
| 2025-07-10 19:07:51 | SELL | INTC | 10 | $23.44 | $11.70 | 55 |
| 2025-07-10 19:07:51 | SELL | WFC | 3 | $82.28 | $-0.06 | 75 |
| 2025-07-10 19:07:51 | BUY | BAC | 2 | $46.89 | N/A | 75 |
| 2025-07-10 19:07:51 | BUY | NKE | 1 | $74.72 | N/A | 70 |
| 2025-07-10 19:07:51 | BUY | PFE | 5 | $25.83 | N/A | 70 |
| 2025-07-10 18:56:32 | SELL | BAC | 2 | $46.85 | $-3.51 | 70 |
| 2025-07-10 18:56:32 | SELL | NKE | 1 | $74.57 | $-1.25 | 65 |
| 2025-07-10 18:56:32 | SELL | PFE | 5 | $25.81 | $3.15 | 65 |
| 2025-07-10 18:56:32 | SELL | QCOM | 1 | $159.48 | $-2.10 | 75 |
| 2025-07-10 18:56:32 | BUY | C | 1 | $86.67 | N/A | 85 |
| 2025-07-10 18:56:32 | BUY | WFC | 1 | $82.15 | N/A | 85 |
| 2025-07-10 18:56:32 | BUY | CSCO | 3 | $68.71 | N/A | 75 |
| 2025-07-10 18:44:41 | SELL | NVDA | 2 | $163.76 | $12.54 | 70 |
| 2025-07-10 18:44:41 | SELL | AMD | 2 | $143.91 | $14.87 | 70 |
| 2025-07-10 18:44:41 | SELL | C | 1 | $86.80 | $-0.01 | 80 |
| 2025-07-10 18:44:41 | SELL | CSCO | 2 | $68.75 | $0.78 | 65 |
| 2025-07-10 18:44:41 | BUY | INTC | 6 | $23.95 | N/A | 65 |
| 2025-07-10 18:44:41 | BUY | PFE | 6 | $25.85 | N/A | 70 |
| 2025-07-10 18:44:41 | BUY | NKE | 2 | $74.89 | N/A | 70 |

<!--TRADE_LOG_END--> 
