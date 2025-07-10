# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 18:27:34**

| Metric | Value |
|---|---|
| **Total Value** | **$101,580.19** |
| Cash | $1,612.26 |
| Holdings Value | $99,967.94 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.94 | $2,129.40 | 70 |
| ADBE | 5 | $377.60 | $372.46 | $1,862.30 | 65 |
| AMD | 18 | $136.48 | $143.98 | $2,591.64 | 85 |
| AMZN | 11 | $221.97 | $222.66 | $2,449.31 | 75 |
| AVGO | 8 | $275.34 | $274.83 | $2,198.64 | 70 |
| AXP | 7 | $325.28 | $325.02 | $2,275.17 | 75 |
| BA | 10 | $212.37 | $225.06 | $2,250.60 | 70 |
| BAC | 49 | $48.60 | $46.94 | $2,299.82 | 75 |
| C | 30 | $86.81 | $86.73 | $2,601.85 | 85 |
| CAT | 6 | $397.86 | $409.75 | $2,458.50 | 85 |
| COST | 2 | $979.83 | $977.94 | $1,955.88 | 65 |
| CRM | 7 | $268.68 | $266.38 | $1,864.68 | 65 |
| CSCO | 32 | $68.36 | $68.85 | $2,203.20 | 70 |
| CVX | 17 | $147.15 | $154.00 | $2,618.00 | 85 |
| DIS | 18 | $122.80 | $121.32 | $2,183.76 | 70 |
| GOOGL | 13 | $179.61 | $177.51 | $2,307.69 | 75 |
| GS | 3 | $717.52 | $708.99 | $2,126.97 | 65 |
| HD | 6 | $372.64 | $377.69 | $2,266.17 | 70 |
| INTC | 78 | $22.14 | $23.91 | $1,864.98 | 60 |
| JNJ | 13 | $155.89 | $157.78 | $2,051.08 | 65 |
| JPM | 9 | $291.61 | $287.52 | $2,587.68 | 85 |
| KO | 29 | $71.03 | $69.63 | $2,019.27 | 65 |
| LLY | 2 | $776.66 | $794.43 | $1,588.86 | 65 |
| MA | 4 | $563.08 | $564.53 | $2,258.12 | 65 |
| META | 3 | $717.12 | $724.83 | $2,174.49 | 85 |
| MRK | 28 | $82.46 | $84.60 | $2,368.80 | 75 |
| MSFT | 5 | $498.84 | $501.47 | $2,507.35 | 85 |
| NFLX | 1 | $1,279.00 | $1,251.02 | $1,251.02 | 60 |
| NKE | 27 | $75.89 | $75.04 | $2,026.08 | 65 |
| NVDA | 16 | $157.49 | $163.75 | $2,620.00 | 85 |
| ORCL | 9 | $233.31 | $237.31 | $2,135.79 | 70 |
| PEP | 15 | $136.57 | $136.31 | $2,044.65 | 65 |
| PFE | 78 | $25.12 | $25.89 | $2,019.81 | 65 |
| PG | 13 | $160.78 | $159.15 | $2,068.95 | 70 |
| PYPL | 30 | $76.66 | $75.97 | $2,279.10 | 75 |
| QCOM | 15 | $161.71 | $159.70 | $2,395.50 | 75 |
| T | 73 | $28.55 | $27.70 | $2,022.46 | 65 |
| TGT | 20 | $104.92 | $106.17 | $2,123.30 | 70 |
| TSLA | 6 | $288.62 | $306.38 | $1,838.27 | 55 |
| UNH | 6 | $298.34 | $302.73 | $1,816.39 | 65 |
| UNP | 9 | $236.20 | $238.21 | $2,143.89 | 75 |
| V | 6 | $355.85 | $356.89 | $2,141.37 | 70 |
| VZ | 48 | $43.15 | $42.08 | $2,019.84 | 65 |
| WFC | 31 | $82.31 | $82.20 | $2,548.36 | 85 |
| WMT | 21 | $97.36 | $95.33 | $2,001.93 | 65 |
| XOM | 21 | $109.91 | $114.62 | $2,407.02 | 75 |

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
| 2025-07-10 18:27:27 | SELL | NKE | 2 | $75.06 | $-1.55 | 65 |
| 2025-07-10 18:27:27 | SELL | INTC | 6 | $23.91 | $9.83 | 60 |
| 2025-07-10 18:27:27 | SELL | PFE | 12 | $25.90 | $8.03 | 65 |
| 2025-07-10 18:27:27 | SELL | CSCO | 1 | $68.85 | $0.47 | 70 |
| 2025-07-10 18:27:27 | SELL | QCOM | 1 | $159.75 | $-1.83 | 75 |
| 2025-07-10 18:27:27 | BUY | NVDA | 2 | $163.74 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | PG | 1 | $159.16 | N/A | 70 |
| 2025-07-10 18:27:27 | BUY | WFC | 3 | $82.21 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | CVX | 1 | $153.99 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | TGT | 1 | $106.22 | N/A | 70 |
| 2025-07-10 18:11:08 | SELL | NVDA | 2 | $164.14 | $13.19 | 70 |
| 2025-07-10 18:11:08 | SELL | CRM | 1 | $265.90 | $-2.43 | 60 |
| 2025-07-10 18:11:08 | SELL | CVX | 1 | $154.09 | $6.93 | 80 |
| 2025-07-10 18:11:08 | BUY | AMD | 2 | $144.40 | N/A | 85 |
| 2025-07-10 18:11:08 | BUY | PFE | 7 | $25.56 | N/A | 75 |
| 2025-07-10 18:11:08 | BUY | BA | 1 | $224.96 | N/A | 75 |
| 2025-07-10 18:11:08 | BUY | QCOM | 1 | $159.74 | N/A | 85 |
| 2025-07-10 17:51:39 | SELL | XOM | 1 | $114.54 | $4.42 | 75 |
| 2025-07-10 17:51:39 | SELL | NKE | 1 | $75.21 | $-0.60 | 70 |
| 2025-07-10 17:51:39 | SELL | QCOM | 1 | $159.84 | $-1.76 | 75 |
| 2025-07-10 17:51:39 | BUY | NVDA | 2 | $164.08 | N/A | 85 |
| 2025-07-10 17:51:39 | BUY | PFE | 5 | $25.88 | N/A | 70 |
| 2025-07-10 17:51:39 | BUY | CSCO | 1 | $68.85 | N/A | 75 |
| 2025-07-10 17:51:39 | BUY | CVX | 1 | $153.77 | N/A | 85 |
| 2025-07-10 17:39:54 | SELL | PFE | 5 | $25.83 | $3.20 | 65 |

<!--TRADE_LOG_END--> 
