# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 03:51:03**

| Metric | Value |
|---|---|
| **Total Value** | **$100,667.29** |
| Cash | $1,158.50 |
| Holdings Value | $99,508.79 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.01 | $2,100.10 | 65 |
| ADBE | 5 | $377.60 | $382.24 | $1,911.20 | 65 |
| AMD | 16 | $135.69 | $137.82 | $2,205.12 | 70 |
| AMZN | 10 | $221.61 | $219.36 | $2,193.60 | 70 |
| AVGO | 8 | $275.34 | $271.80 | $2,174.40 | 70 |
| AXP | 7 | $325.28 | $316.98 | $2,218.86 | 75 |
| BA | 10 | $212.43 | $218.52 | $2,185.20 | 65 |
| BAC | 47 | $48.72 | $47.15 | $2,216.05 | 70 |
| C | 26 | $86.75 | $85.57 | $2,224.82 | 70 |
| CAT | 6 | $397.86 | $394.29 | $2,365.74 | 70 |
| COST | 2 | $979.83 | $985.84 | $1,971.68 | 65 |
| CRM | 8 | $268.33 | $273.65 | $2,189.20 | 65 |
| CSCO | 34 | $68.36 | $68.59 | $2,332.06 | 75 |
| CVX | 17 | $147.04 | $153.24 | $2,605.08 | 85 |
| DIS | 17 | $122.85 | $121.82 | $2,070.94 | 65 |
| GOOGL | 12 | $179.60 | $174.36 | $2,092.32 | 65 |
| GS | 3 | $717.52 | $697.28 | $2,091.84 | 75 |
| HD | 6 | $372.64 | $367.50 | $2,205.00 | 70 |
| INTC | 86 | $22.32 | $23.59 | $2,028.74 | 65 |
| JNJ | 13 | $155.89 | $155.79 | $2,025.27 | 70 |
| JPM | 9 | $291.61 | $282.78 | $2,545.02 | 85 |
| KO | 30 | $71.00 | $70.24 | $2,107.20 | 70 |
| LLY | 2 | $776.66 | $777.66 | $1,555.32 | 65 |
| MA | 4 | $563.08 | $562.44 | $2,249.76 | 65 |
| META | 3 | $717.12 | $720.67 | $2,162.01 | 85 |
| MRK | 29 | $82.50 | $81.37 | $2,359.73 | 75 |
| MSFT | 5 | $498.84 | $496.62 | $2,483.10 | 75 |
| NFLX | 1 | $1,279.00 | $1,275.31 | $1,275.31 | 65 |
| NKE | 29 | $75.97 | $73.92 | $2,143.68 | 70 |
| NVDA | 16 | $157.22 | $160.00 | $2,560.00 | 85 |
| ORCL | 9 | $233.41 | $234.50 | $2,110.50 | 70 |
| PEP | 15 | $136.57 | $135.04 | $2,025.60 | 65 |
| PFE | 91 | $25.26 | $25.62 | $2,331.42 | 75 |
| PG | 13 | $160.77 | $157.89 | $2,052.57 | 65 |
| PYPL | 31 | $76.65 | $75.03 | $2,325.93 | 75 |
| QCOM | 14 | $161.76 | $159.45 | $2,232.30 | 75 |
| T | 72 | $28.56 | $28.29 | $2,036.88 | 65 |
| TGT | 20 | $104.90 | $102.01 | $2,040.20 | 65 |
| TSLA | 6 | $288.62 | $297.81 | $1,786.86 | 65 |
| UNH | 7 | $314.75 | $307.70 | $2,153.90 | 65 |
| UNP | 10 | $236.66 | $236.54 | $2,365.40 | 75 |
| V | 6 | $355.95 | $354.55 | $2,127.30 | 65 |
| VZ | 47 | $43.16 | $43.06 | $2,023.82 | 65 |
| WFC | 32 | $82.26 | $81.59 | $2,610.88 | 85 |
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
| 2025-07-09 03:50:57 | SELL | INTC | 1 | $23.59 | $1.25 | 65 |
| 2025-07-09 03:50:57 | SELL | PFE | 2 | $25.62 | $0.70 | 75 |
| 2025-07-09 03:50:57 | SELL | VZ | 1 | $43.06 | $-0.10 | 65 |
| 2025-07-09 03:50:57 | SELL | T | 1 | $28.29 | $-0.26 | 65 |
| 2025-07-09 03:50:57 | BUY | NVDA | 1 | $160.00 | N/A | 85 |
| 2025-07-09 03:50:57 | BUY | KO | 1 | $70.24 | N/A | 70 |
| 2025-07-09 03:50:57 | BUY | NKE | 1 | $73.92 | N/A | 70 |
| 2025-07-09 03:50:57 | BUY | WFC | 2 | $81.59 | N/A | 85 |
| 2025-07-09 03:50:57 | BUY | CVX | 1 | $153.24 | N/A | 85 |
| 2025-07-09 03:17:32 | SELL | NVDA | 1 | $160.00 | $2.78 | 75 |
| 2025-07-09 03:17:32 | SELL | XOM | 2 | $114.19 | $7.60 | 75 |
| 2025-07-09 03:17:32 | SELL | NKE | 2 | $73.92 | $-3.97 | 65 |
| 2025-07-09 03:17:32 | BUY | WFC | 1 | $81.59 | N/A | 80 |
| 2025-07-09 02:43:32 | SELL | PFE | 11 | $25.62 | $3.43 | 75 |
| 2025-07-09 02:43:32 | SELL | CVX | 1 | $153.24 | $6.20 | 75 |
| 2025-07-09 02:43:32 | BUY | XOM | 2 | $114.19 | N/A | 85 |
| 2025-07-09 02:43:32 | BUY | PYPL | 1 | $75.03 | N/A | 75 |
| 2025-07-09 01:59:40 | SELL | BAC | 3 | $47.15 | $-4.43 | 70 |
| 2025-07-09 01:59:40 | SELL | DIS | 1 | $121.82 | $-0.97 | 65 |
| 2025-07-09 01:59:40 | SELL | C | 1 | $85.57 | $-1.14 | 70 |
| 2025-07-09 01:59:40 | SELL | WFC | 1 | $81.59 | $-0.72 | 75 |
| 2025-07-09 01:59:40 | BUY | NVDA | 2 | $160.00 | N/A | 85 |
| 2025-07-09 01:59:40 | BUY | PFE | 17 | $25.62 | N/A | 85 |
| 2025-07-09 01:13:03 | SELL | ORCL | 1 | $234.50 | $0.98 | 65 |
| 2025-07-09 01:13:03 | BUY | DIS | 1 | $121.82 | N/A | 70 |

<!--TRADE_LOG_END--> 
