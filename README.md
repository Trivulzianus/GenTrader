# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 01:13:08**

| Metric | Value |
|---|---|
| **Total Value** | **$100,667.29** |
| Cash | $1,371.73 |
| Holdings Value | $99,295.56 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.01 | $2,100.10 | 65 |
| ADBE | 5 | $377.60 | $382.24 | $1,911.20 | 65 |
| AMD | 16 | $135.69 | $137.82 | $2,205.12 | 70 |
| AMZN | 10 | $221.61 | $219.36 | $2,193.60 | 70 |
| AVGO | 8 | $275.34 | $271.80 | $2,174.40 | 65 |
| AXP | 7 | $325.28 | $316.98 | $2,218.86 | 75 |
| BA | 10 | $212.43 | $218.52 | $2,185.20 | 65 |
| BAC | 50 | $48.63 | $47.15 | $2,357.50 | 75 |
| C | 27 | $86.71 | $85.57 | $2,310.39 | 75 |
| CAT | 6 | $397.86 | $394.29 | $2,365.74 | 65 |
| COST | 2 | $979.83 | $985.84 | $1,971.68 | 65 |
| CRM | 8 | $268.33 | $273.65 | $2,189.20 | 65 |
| CSCO | 34 | $68.36 | $68.59 | $2,332.06 | 75 |
| CVX | 17 | $147.04 | $153.24 | $2,605.08 | 85 |
| DIS | 18 | $122.79 | $121.82 | $2,192.76 | 70 |
| GOOGL | 12 | $179.60 | $174.36 | $2,092.32 | 65 |
| GS | 3 | $717.52 | $697.28 | $2,091.84 | 70 |
| HD | 6 | $372.64 | $367.50 | $2,205.00 | 70 |
| INTC | 87 | $22.34 | $23.59 | $2,052.33 | 65 |
| JNJ | 13 | $155.89 | $155.79 | $2,025.27 | 65 |
| JPM | 9 | $291.61 | $282.78 | $2,545.02 | 75 |
| KO | 29 | $71.03 | $70.24 | $2,036.96 | 65 |
| LLY | 2 | $776.66 | $777.66 | $1,555.32 | 65 |
| MA | 4 | $563.08 | $562.44 | $2,249.76 | 65 |
| META | 3 | $717.12 | $720.67 | $2,162.01 | 85 |
| MRK | 29 | $82.50 | $81.37 | $2,359.73 | 75 |
| MSFT | 5 | $498.84 | $496.62 | $2,483.10 | 70 |
| NFLX | 1 | $1,279.00 | $1,275.31 | $1,275.31 | 65 |
| NKE | 30 | $75.91 | $73.92 | $2,217.60 | 70 |
| NVDA | 14 | $156.82 | $160.00 | $2,240.00 | 75 |
| ORCL | 9 | $233.41 | $234.50 | $2,110.50 | 65 |
| PEP | 15 | $136.57 | $135.04 | $2,025.60 | 65 |
| PFE | 87 | $25.25 | $25.62 | $2,228.94 | 70 |
| PG | 13 | $160.77 | $157.89 | $2,052.57 | 65 |
| PYPL | 30 | $76.70 | $75.03 | $2,250.90 | 70 |
| QCOM | 14 | $161.76 | $159.45 | $2,232.30 | 75 |
| T | 73 | $28.55 | $28.29 | $2,065.17 | 65 |
| TGT | 20 | $104.90 | $102.01 | $2,040.20 | 65 |
| TSLA | 6 | $288.62 | $297.81 | $1,786.86 | 65 |
| UNH | 7 | $314.75 | $307.70 | $2,153.90 | 65 |
| UNP | 10 | $236.66 | $236.54 | $2,365.40 | 75 |
| V | 6 | $355.95 | $354.55 | $2,127.30 | 65 |
| VZ | 48 | $43.16 | $43.06 | $2,066.88 | 65 |
| WFC | 30 | $82.31 | $81.59 | $2,447.70 | 75 |
| WMT | 21 | $97.35 | $97.09 | $2,038.89 | 65 |
| XOM | 21 | $110.03 | $114.19 | $2,397.99 | 75 |

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
| 2025-07-09 01:13:03 | SELL | ORCL | 1 | $234.50 | $0.98 | 65 |
| 2025-07-09 01:13:03 | BUY | DIS | 1 | $121.82 | N/A | 70 |
| 2025-07-09 01:13:03 | BUY | CVX | 1 | $153.24 | N/A | 85 |
| 2025-07-09 00:34:45 | SELL | DIS | 1 | $121.82 | $-0.97 | 65 |
| 2025-07-09 00:34:45 | SELL | CVX | 1 | $153.24 | $6.20 | 75 |
| 2025-07-09 00:34:45 | BUY | BAC | 1 | $47.15 | N/A | 75 |
| 2025-07-09 00:34:45 | BUY | INTC | 1 | $23.59 | N/A | 65 |
| 2025-07-09 00:34:45 | BUY | NKE | 2 | $73.92 | N/A | 70 |
| 2025-07-09 00:34:45 | BUY | PFE | 1 | $25.62 | N/A | 70 |
| 2025-07-09 00:34:45 | BUY | VZ | 1 | $43.06 | N/A | 65 |
| 2025-07-09 00:34:45 | BUY | T | 1 | $28.29 | N/A | 65 |
| 2025-07-08 23:50:27 | SELL | NVDA | 2 | $160.00 | $5.57 | 70 |
| 2025-07-08 23:50:27 | SELL | XOM | 1 | $114.19 | $3.97 | 75 |
| 2025-07-08 23:50:27 | SELL | NKE | 1 | $73.92 | $-2.05 | 65 |
| 2025-07-08 23:50:27 | SELL | WMT | 1 | $97.09 | $-0.25 | 65 |
| 2025-07-08 23:50:27 | SELL | PFE | 6 | $25.62 | $2.11 | 70 |
| 2025-07-08 23:50:27 | SELL | PYPL | 1 | $75.03 | $-1.62 | 70 |
| 2025-07-08 23:50:27 | BUY | DIS | 1 | $121.82 | N/A | 70 |
| 2025-07-08 23:50:27 | BUY | WFC | 1 | $81.59 | N/A | 80 |
| 2025-07-08 23:50:27 | BUY | CVX | 1 | $153.24 | N/A | 85 |
| 2025-07-08 23:37:53 | SELL | XOM | 1 | $114.19 | $3.80 | 80 |
| 2025-07-08 23:37:53 | SELL | PFE | 11 | $25.62 | $3.46 | 75 |
| 2025-07-08 23:37:53 | BUY | BAC | 2 | $47.15 | N/A | 75 |
| 2025-07-08 23:37:53 | BUY | WMT | 1 | $97.09 | N/A | 70 |
| 2025-07-08 23:26:06 | SELL | WMT | 3 | $97.09 | $-0.68 | 65 |

<!--TRADE_LOG_END--> 
