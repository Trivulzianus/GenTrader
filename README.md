# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 19:08:46**

| Metric | Value |
|---|---|
| **Total Value** | **$100,737.02** |
| Cash | $124.30 |
| Holdings Value | $100,612.72 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.72 | $2,097.20 | 70 |
| ADBE | 5 | $377.60 | $381.30 | $1,906.50 | 65 |
| AMD | 16 | $135.69 | $137.63 | $2,202.08 | 70 |
| AMZN | 10 | $221.61 | $219.82 | $2,198.25 | 65 |
| AVGO | 8 | $275.34 | $273.04 | $2,184.32 | 70 |
| AXP | 8 | $324.24 | $318.86 | $2,550.88 | 75 |
| BA | 10 | $212.43 | $218.57 | $2,185.70 | 70 |
| BAC | 50 | $48.63 | $47.39 | $2,369.50 | 75 |
| C | 30 | $86.59 | $86.02 | $2,580.60 | 85 |
| CAT | 6 | $397.86 | $395.31 | $2,371.86 | 70 |
| COST | 2 | $979.83 | $985.16 | $1,970.32 | 65 |
| CRM | 8 | $268.33 | $272.72 | $2,181.76 | 65 |
| CSCO | 32 | $68.34 | $68.72 | $2,198.88 | 70 |
| CVX | 16 | $146.71 | $152.41 | $2,438.64 | 85 |
| DIS | 17 | $122.85 | $122.09 | $2,075.53 | 65 |
| GOOGL | 12 | $179.60 | $173.53 | $2,082.36 | 65 |
| GS | 3 | $717.52 | $698.72 | $2,096.16 | 70 |
| HD | 6 | $372.64 | $367.79 | $2,206.74 | 70 |
| INTC | 86 | $22.32 | $23.60 | $2,029.90 | 65 |
| JNJ | 13 | $155.89 | $155.55 | $2,022.15 | 65 |
| JPM | 9 | $291.61 | $282.98 | $2,546.82 | 85 |
| KO | 29 | $71.03 | $70.42 | $2,042.04 | 65 |
| LLY | 2 | $776.66 | $783.87 | $1,567.74 | 65 |
| MA | 4 | $563.08 | $561.58 | $2,246.32 | 65 |
| META | 3 | $717.12 | $718.32 | $2,154.96 | 75 |
| MRK | 29 | $82.50 | $81.52 | $2,363.93 | 75 |
| MSFT | 5 | $498.84 | $495.77 | $2,478.85 | 75 |
| NFLX | 1 | $1,279.00 | $1,272.26 | $1,272.26 | 65 |
| NKE | 29 | $75.97 | $73.86 | $2,141.94 | 70 |
| NVDA | 17 | $157.07 | $159.59 | $2,713.11 | 85 |
| ORCL | 9 | $233.41 | $234.25 | $2,108.30 | 65 |
| PEP | 15 | $136.57 | $135.11 | $2,026.67 | 65 |
| PFE | 85 | $25.24 | $25.62 | $2,178.12 | 70 |
| PG | 13 | $160.77 | $158.07 | $2,054.91 | 65 |
| PYPL | 31 | $76.65 | $74.74 | $2,316.95 | 75 |
| QCOM | 15 | $161.62 | $160.00 | $2,400.07 | 75 |
| T | 81 | $28.53 | $28.44 | $2,303.64 | 75 |
| TGT | 20 | $104.90 | $102.14 | $2,042.80 | 65 |
| TSLA | 6 | $288.62 | $299.86 | $1,799.16 | 65 |
| UNH | 7 | $314.75 | $306.85 | $2,147.91 | 65 |
| UNP | 10 | $236.66 | $237.29 | $2,372.91 | 75 |
| V | 6 | $355.95 | $353.75 | $2,122.50 | 65 |
| VZ | 47 | $43.16 | $43.10 | $2,025.78 | 65 |
| WFC | 29 | $82.33 | $81.81 | $2,372.35 | 75 |
| WMT | 23 | $97.35 | $97.48 | $2,242.04 | 70 |
| XOM | 23 | $110.36 | $113.97 | $2,621.31 | 85 |

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
| 2025-07-08 19:08:41 | SELL | PFE | 6 | $25.62 | $2.17 | 70 |
| 2025-07-08 19:08:41 | SELL | WFC | 1 | $81.80 | $-0.51 | 75 |
| 2025-07-08 19:08:41 | SELL | CSCO | 2 | $68.71 | $0.69 | 70 |
| 2025-07-08 19:08:41 | BUY | XOM | 2 | $113.96 | N/A | 85 |
| 2025-07-08 19:08:41 | BUY | C | 4 | $86.01 | N/A | 85 |
| 2025-07-08 19:08:41 | BUY | T | 5 | $28.43 | N/A | 75 |
| 2025-07-08 18:57:14 | SELL | XOM | 1 | $114.01 | $3.81 | 75 |
| 2025-07-08 18:57:14 | SELL | C | 2 | $85.92 | $-1.43 | 70 |
| 2025-07-08 18:57:14 | SELL | CVX | 1 | $152.49 | $5.44 | 75 |
| 2025-07-08 18:57:14 | BUY | WFC | 1 | $81.60 | N/A | 80 |
| 2025-07-08 18:57:14 | BUY | CSCO | 2 | $68.67 | N/A | 75 |
| 2025-07-08 18:57:14 | BUY | PFE | 6 | $25.62 | N/A | 75 |
| 2025-07-08 18:57:14 | BUY | T | 4 | $28.41 | N/A | 70 |
| 2025-07-08 18:45:11 | SELL | C | 2 | $85.97 | $-1.22 | 75 |
| 2025-07-08 18:45:11 | BUY | WMT | 2 | $97.38 | N/A | 75 |
| 2025-07-08 18:45:11 | BUY | CVX | 1 | $152.41 | N/A | 85 |
| 2025-07-08 18:27:39 | SELL | WMT | 2 | $97.54 | $0.37 | 65 |
| 2025-07-08 18:27:39 | SELL | XOM | 1 | $114.14 | $3.77 | 80 |
| 2025-07-08 18:27:39 | SELL | MRK | 1 | $81.34 | $-1.12 | 75 |
| 2025-07-08 18:27:39 | SELL | CSCO | 1 | $68.71 | $0.35 | 70 |
| 2025-07-08 18:27:39 | SELL | T | 9 | $28.40 | $-1.18 | 65 |
| 2025-07-08 18:27:39 | BUY | NKE | 1 | $74.00 | N/A | 70 |
| 2025-07-08 18:27:39 | BUY | VZ | 1 | $43.12 | N/A | 65 |
| 2025-07-08 18:10:59 | SELL | JNJ | 1 | $155.35 | $-0.50 | 65 |
| 2025-07-08 18:10:59 | SELL | INTC | 2 | $23.68 | $2.67 | 65 |

<!--TRADE_LOG_END--> 
