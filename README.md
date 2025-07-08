# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 17:39:44**

| Metric | Value |
|---|---|
| **Total Value** | **$100,724.56** |
| Cash | $823.83 |
| Holdings Value | $99,900.73 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.54 | $2,095.41 | 70 |
| ADBE | 5 | $377.60 | $381.47 | $1,907.35 | 65 |
| AMD | 16 | $135.69 | $137.78 | $2,204.56 | 70 |
| AMZN | 10 | $221.61 | $220.45 | $2,204.50 | 65 |
| AVGO | 8 | $275.34 | $274.51 | $2,196.08 | 70 |
| AXP | 8 | $324.24 | $319.63 | $2,557.04 | 85 |
| BA | 10 | $212.43 | $217.88 | $2,178.75 | 65 |
| BAC | 50 | $48.63 | $47.31 | $2,365.36 | 75 |
| C | 31 | $86.58 | $86.31 | $2,675.46 | 85 |
| CAT | 6 | $397.86 | $394.64 | $2,367.84 | 70 |
| COST | 2 | $979.83 | $989.11 | $1,978.21 | 65 |
| CRM | 8 | $268.33 | $273.28 | $2,186.22 | 65 |
| CSCO | 33 | $68.36 | $68.53 | $2,261.49 | 70 |
| CVX | 16 | $146.71 | $152.46 | $2,439.36 | 75 |
| DIS | 17 | $122.85 | $121.95 | $2,073.15 | 65 |
| GOOGL | 12 | $179.60 | $174.03 | $2,088.36 | 65 |
| GS | 3 | $717.52 | $698.96 | $2,096.87 | 70 |
| HD | 6 | $372.64 | $367.03 | $2,202.18 | 65 |
| INTC | 87 | $22.34 | $23.55 | $2,048.41 | 65 |
| JNJ | 14 | $155.85 | $155.24 | $2,173.36 | 65 |
| JPM | 9 | $291.61 | $282.08 | $2,538.70 | 75 |
| KO | 29 | $71.03 | $70.30 | $2,038.70 | 65 |
| LLY | 2 | $776.66 | $780.98 | $1,561.96 | 65 |
| MA | 4 | $563.08 | $561.87 | $2,247.48 | 65 |
| META | 3 | $717.12 | $719.80 | $2,159.40 | 75 |
| MRK | 28 | $82.54 | $81.12 | $2,271.36 | 70 |
| MSFT | 5 | $498.84 | $495.80 | $2,479.00 | 70 |
| NFLX | 1 | $1,279.00 | $1,277.13 | $1,277.13 | 65 |
| NKE | 30 | $75.91 | $73.78 | $2,213.55 | 70 |
| NVDA | 16 | $156.90 | $159.56 | $2,552.88 | 85 |
| ORCL | 9 | $233.41 | $237.43 | $2,136.87 | 65 |
| PEP | 15 | $136.57 | $134.68 | $2,020.20 | 65 |
| PFE | 87 | $25.25 | $25.49 | $2,217.43 | 70 |
| PG | 13 | $160.77 | $158.11 | $2,055.43 | 65 |
| PYPL | 30 | $76.71 | $74.66 | $2,239.65 | 70 |
| QCOM | 14 | $161.75 | $159.58 | $2,234.12 | 75 |
| T | 72 | $28.54 | $28.41 | $2,045.88 | 65 |
| TGT | 20 | $104.90 | $101.47 | $2,029.50 | 65 |
| TSLA | 6 | $288.62 | $300.74 | $1,804.44 | 65 |
| UNH | 7 | $314.75 | $305.68 | $2,139.76 | 65 |
| UNP | 10 | $236.66 | $236.31 | $2,363.10 | 75 |
| V | 6 | $355.95 | $354.69 | $2,128.14 | 65 |
| VZ | 47 | $43.72 | $43.09 | $2,025.16 | 65 |
| WFC | 29 | $82.34 | $81.70 | $2,369.45 | 75 |
| WMT | 21 | $97.34 | $97.89 | $2,055.69 | 65 |
| XOM | 21 | $110.00 | $114.09 | $2,395.79 | 75 |

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
| 2025-07-08 17:39:36 | SELL | MRK | 1 | $81.13 | $-1.36 | 70 |
| 2025-07-08 17:39:36 | SELL | PYPL | 1 | $74.66 | $-1.98 | 70 |
| 2025-07-08 17:39:36 | SELL | CSCO | 1 | $68.54 | $0.17 | 70 |
| 2025-07-08 17:39:36 | SELL | CVX | 1 | $152.51 | $5.46 | 75 |
| 2025-07-08 17:39:36 | BUY | NVDA | 1 | $159.55 | N/A | 85 |
| 2025-07-08 17:39:36 | BUY | BAC | 1 | $47.31 | N/A | 75 |
| 2025-07-08 17:39:36 | BUY | INTC | 1 | $23.57 | N/A | 65 |
| 2025-07-08 17:39:36 | BUY | NKE | 2 | $73.79 | N/A | 70 |
| 2025-07-08 17:39:36 | BUY | C | 1 | $86.31 | N/A | 85 |
| 2025-07-08 17:25:32 | SELL | NVDA | 1 | $159.57 | $2.66 | 75 |
| 2025-07-08 17:25:32 | SELL | NKE | 2 | $73.86 | $-4.12 | 65 |
| 2025-07-08 17:25:32 | SELL | WMT | 3 | $97.97 | $1.64 | 65 |
| 2025-07-08 17:25:32 | BUY | INTC | 5 | $23.53 | N/A | 65 |
| 2025-07-08 17:25:32 | BUY | C | 4 | $86.25 | N/A | 85 |
| 2025-07-08 17:25:32 | BUY | CVX | 1 | $152.88 | N/A | 85 |
| 2025-07-08 17:08:36 | SELL | INTC | 5 | $23.49 | $5.84 | 60 |
| 2025-07-08 17:08:36 | SELL | C | 5 | $86.33 | $-1.28 | 70 |
| 2025-07-08 17:08:36 | SELL | T | 1 | $28.33 | $-0.22 | 65 |
| 2025-07-08 17:08:36 | BUY | WMT | 3 | $97.67 | N/A | 75 |
| 2025-07-08 17:08:36 | BUY | BA | 1 | $217.69 | N/A | 70 |
| 2025-07-08 17:08:36 | BUY | CSCO | 2 | $68.58 | N/A | 75 |
| 2025-07-08 16:55:22 | SELL | INTC | 1 | $22.00 | $-0.32 | 60 |
| 2025-07-08 16:55:22 | SELL | WMT | 1 | $97.77 | $0.37 | 65 |
| 2025-07-08 16:55:22 | SELL | MRK | 3 | $81.90 | $-1.60 | 75 |
| 2025-07-08 16:55:22 | SELL | T | 5 | $28.30 | $-1.15 | 65 |

<!--TRADE_LOG_END--> 
