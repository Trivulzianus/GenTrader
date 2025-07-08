# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 19:50:24**

| Metric | Value |
|---|---|
| **Total Value** | **$100,715.41** |
| Cash | $757.02 |
| Holdings Value | $99,958.39 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.75 | $2,097.55 | 65 |
| ADBE | 5 | $377.60 | $381.98 | $1,909.90 | 65 |
| AMD | 16 | $135.69 | $137.80 | $2,204.80 | 70 |
| AMZN | 10 | $221.61 | $219.66 | $2,196.57 | 65 |
| AVGO | 8 | $275.34 | $271.89 | $2,175.12 | 70 |
| AXP | 8 | $324.24 | $318.44 | $2,547.52 | 75 |
| BA | 10 | $212.43 | $218.36 | $2,183.60 | 65 |
| BAC | 49 | $48.66 | $47.28 | $2,316.72 | 75 |
| C | 30 | $86.59 | $85.84 | $2,575.35 | 85 |
| CAT | 6 | $397.86 | $395.33 | $2,372.01 | 70 |
| COST | 2 | $979.83 | $985.65 | $1,971.30 | 65 |
| CRM | 8 | $268.33 | $274.33 | $2,194.64 | 65 |
| CSCO | 33 | $68.35 | $68.67 | $2,266.11 | 75 |
| CVX | 17 | $147.04 | $152.87 | $2,598.79 | 80 |
| DIS | 17 | $122.85 | $122.08 | $2,075.37 | 65 |
| GOOGL | 12 | $179.60 | $174.04 | $2,088.48 | 65 |
| GS | 3 | $717.52 | $697.16 | $2,091.48 | 70 |
| HD | 6 | $372.64 | $367.81 | $2,206.89 | 70 |
| INTC | 85 | $22.31 | $23.75 | $2,018.33 | 65 |
| JNJ | 13 | $155.89 | $155.56 | $2,022.28 | 65 |
| JPM | 9 | $291.61 | $282.47 | $2,542.23 | 85 |
| KO | 29 | $71.03 | $70.42 | $2,042.32 | 65 |
| LLY | 2 | $776.66 | $780.00 | $1,560.00 | 65 |
| MA | 4 | $563.08 | $561.78 | $2,247.12 | 65 |
| META | 3 | $717.12 | $718.83 | $2,156.49 | 85 |
| MRK | 29 | $82.50 | $81.45 | $2,362.05 | 75 |
| MSFT | 5 | $498.84 | $496.71 | $2,483.55 | 75 |
| NFLX | 1 | $1,279.00 | $1,266.89 | $1,266.89 | 65 |
| NKE | 28 | $76.05 | $73.89 | $2,068.92 | 65 |
| NVDA | 14 | $156.82 | $159.90 | $2,238.60 | 75 |
| ORCL | 9 | $233.41 | $234.33 | $2,108.97 | 70 |
| PEP | 15 | $136.57 | $135.24 | $2,028.60 | 65 |
| PFE | 103 | $25.31 | $25.64 | $2,640.92 | 85 |
| PG | 13 | $160.77 | $157.64 | $2,049.32 | 70 |
| PYPL | 31 | $76.65 | $75.03 | $2,325.78 | 75 |
| QCOM | 14 | $161.76 | $159.56 | $2,233.84 | 70 |
| T | 77 | $28.54 | $28.36 | $2,184.04 | 70 |
| TGT | 20 | $104.90 | $102.26 | $2,045.20 | 65 |
| TSLA | 6 | $288.62 | $296.73 | $1,780.39 | 65 |
| UNH | 7 | $314.75 | $307.41 | $2,151.87 | 65 |
| UNP | 10 | $236.66 | $237.15 | $2,371.50 | 75 |
| V | 6 | $355.95 | $354.00 | $2,124.00 | 70 |
| VZ | 47 | $43.16 | $43.15 | $2,027.82 | 65 |
| WFC | 29 | $82.33 | $81.68 | $2,368.72 | 75 |
| WMT | 21 | $97.35 | $97.15 | $2,040.13 | 65 |
| XOM | 21 | $110.03 | $114.11 | $2,396.31 | 75 |

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
| 2025-07-08 19:50:18 | SELL | NKE | 1 | $73.90 | $-2.07 | 65 |
| 2025-07-08 19:50:18 | SELL | QCOM | 1 | $159.56 | $-2.06 | 70 |
| 2025-07-08 19:50:18 | SELL | T | 4 | $28.36 | $-0.67 | 70 |
| 2025-07-08 19:50:18 | BUY | PFE | 13 | $25.65 | N/A | 85 |
| 2025-07-08 19:50:18 | BUY | CSCO | 1 | $68.68 | N/A | 75 |
| 2025-07-08 19:35:58 | SELL | NVDA | 3 | $158.24 | $3.51 | 70 |
| 2025-07-08 19:35:58 | SELL | WMT | 2 | $97.36 | $0.01 | 65 |
| 2025-07-08 19:35:58 | BUY | T | 5 | $28.41 | N/A | 75 |
| 2025-07-08 19:24:24 | SELL | BAC | 1 | $47.31 | $-1.33 | 75 |
| 2025-07-08 19:24:24 | SELL | INTC | 1 | $23.54 | $1.22 | 65 |
| 2025-07-08 19:24:24 | SELL | XOM | 2 | $113.85 | $6.97 | 75 |
| 2025-07-08 19:24:24 | SELL | T | 5 | $28.43 | $-0.52 | 70 |
| 2025-07-08 19:24:24 | BUY | PFE | 5 | $25.58 | N/A | 75 |
| 2025-07-08 19:24:24 | BUY | CVX | 1 | $152.33 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
