# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 07:38:11**

| Metric | Value |
|---|---|
| **Total Value** | **$100,667.29** |
| Cash | $489.22 |
| Holdings Value | $100,178.07 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.01 | $2,100.10 | 65 |
| ADBE | 5 | $377.60 | $382.24 | $1,911.20 | 65 |
| AMD | 15 | $135.55 | $137.82 | $2,067.30 | 70 |
| AMZN | 10 | $221.61 | $219.36 | $2,193.60 | 70 |
| AVGO | 8 | $275.34 | $271.80 | $2,174.40 | 70 |
| AXP | 7 | $325.28 | $316.98 | $2,218.86 | 75 |
| BA | 10 | $212.43 | $218.52 | $2,185.20 | 70 |
| BAC | 50 | $48.63 | $47.15 | $2,357.50 | 75 |
| C | 30 | $86.59 | $85.57 | $2,567.10 | 85 |
| CAT | 6 | $397.86 | $394.29 | $2,365.74 | 70 |
| COST | 2 | $979.83 | $985.84 | $1,971.68 | 65 |
| CRM | 8 | $268.33 | $273.65 | $2,189.20 | 70 |
| CSCO | 33 | $68.35 | $68.59 | $2,263.47 | 75 |
| CVX | 17 | $147.04 | $153.24 | $2,605.08 | 85 |
| DIS | 17 | $122.85 | $121.82 | $2,070.94 | 70 |
| GOOGL | 12 | $179.60 | $174.36 | $2,092.32 | 70 |
| GS | 3 | $717.52 | $697.28 | $2,091.84 | 75 |
| HD | 6 | $372.64 | $367.50 | $2,205.00 | 65 |
| INTC | 85 | $22.31 | $23.59 | $2,005.15 | 65 |
| JNJ | 13 | $155.89 | $155.79 | $2,025.27 | 65 |
| JPM | 9 | $291.61 | $282.78 | $2,545.02 | 75 |
| KO | 29 | $71.03 | $70.24 | $2,036.96 | 65 |
| LLY | 2 | $776.66 | $777.66 | $1,555.32 | 65 |
| MA | 4 | $563.08 | $562.44 | $2,249.76 | 65 |
| META | 3 | $717.12 | $720.67 | $2,162.01 | 75 |
| MRK | 29 | $82.50 | $81.37 | $2,359.73 | 75 |
| MSFT | 5 | $498.84 | $496.62 | $2,483.10 | 70 |
| NFLX | 1 | $1,279.00 | $1,275.31 | $1,275.31 | 65 |
| NKE | 31 | $75.84 | $73.92 | $2,291.52 | 75 |
| NVDA | 16 | $157.22 | $160.00 | $2,560.00 | 85 |
| ORCL | 9 | $233.41 | $234.50 | $2,110.50 | 70 |
| PEP | 15 | $136.57 | $135.04 | $2,025.60 | 65 |
| PFE | 102 | $25.30 | $25.62 | $2,613.24 | 85 |
| PG | 13 | $160.77 | $157.89 | $2,052.57 | 65 |
| PYPL | 31 | $76.65 | $75.03 | $2,325.93 | 75 |
| QCOM | 15 | $161.61 | $159.45 | $2,391.75 | 75 |
| T | 77 | $28.54 | $28.29 | $2,178.33 | 70 |
| TGT | 20 | $104.90 | $102.01 | $2,040.20 | 65 |
| TSLA | 6 | $288.62 | $297.81 | $1,786.86 | 65 |
| UNH | 7 | $314.75 | $307.70 | $2,153.90 | 70 |
| UNP | 10 | $236.66 | $236.54 | $2,365.40 | 75 |
| V | 6 | $355.95 | $354.55 | $2,127.30 | 65 |
| VZ | 47 | $43.16 | $43.06 | $2,023.82 | 65 |
| WFC | 29 | $82.33 | $81.59 | $2,366.11 | 75 |
| WMT | 21 | $97.35 | $97.09 | $2,038.89 | 65 |
| XOM | 21 | $110.03 | $114.19 | $2,397.99 | 80 |

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
| 2025-07-09 07:38:06 | SELL | WMT | 2 | $97.09 | $-0.47 | 65 |
| 2025-07-09 07:26:07 | BUY | NVDA | 1 | $160.00 | N/A | 85 |
| 2025-07-09 07:26:07 | BUY | NKE | 3 | $73.92 | N/A | 75 |
| 2025-07-09 07:09:48 | SELL | NVDA | 1 | $160.00 | $2.78 | 75 |
| 2025-07-09 07:09:48 | SELL | NKE | 3 | $73.92 | $-5.76 | 65 |
| 2025-07-09 07:09:48 | SELL | WFC | 1 | $81.59 | $-0.72 | 75 |
| 2025-07-09 07:09:48 | SELL | T | 4 | $28.29 | $-0.95 | 70 |
| 2025-07-09 06:46:31 | BUY | NKE | 1 | $73.92 | N/A | 75 |
| 2025-07-09 06:46:31 | BUY | WFC | 1 | $81.59 | N/A | 80 |
| 2025-07-09 06:46:31 | BUY | T | 4 | $28.29 | N/A | 75 |
| 2025-07-09 06:28:18 | SELL | XOM | 2 | $114.19 | $7.60 | 75 |
| 2025-07-09 06:28:18 | SELL | NKE | 1 | $73.92 | $-1.92 | 70 |
| 2025-07-09 06:28:18 | BUY | NVDA | 2 | $160.00 | N/A | 85 |
| 2025-07-09 06:28:18 | BUY | QCOM | 1 | $159.45 | N/A | 80 |
| 2025-07-09 06:28:18 | BUY | CVX | 1 | $153.24 | N/A | 85 |
| 2025-07-09 06:11:41 | SELL | T | 5 | $28.29 | $-1.18 | 70 |
| 2025-07-09 06:11:41 | SELL | CVX | 1 | $153.24 | $6.20 | 75 |
| 2025-07-09 06:11:41 | BUY | NKE | 3 | $73.92 | N/A | 75 |
| 2025-07-09 06:11:41 | BUY | PFE | 5 | $25.62 | N/A | 85 |
| 2025-07-09 05:54:58 | SELL | BAC | 2 | $47.15 | $-2.84 | 75 |
| 2025-07-09 05:54:58 | SELL | PFE | 5 | $25.62 | $1.59 | 80 |
| 2025-07-09 05:54:58 | SELL | NKE | 3 | $73.92 | $-5.76 | 65 |
| 2025-07-09 05:54:58 | BUY | XOM | 2 | $114.19 | N/A | 85 |
| 2025-07-09 05:54:58 | BUY | CSCO | 1 | $68.59 | N/A | 75 |
| 2025-07-09 05:54:58 | BUY | T | 5 | $28.29 | N/A | 75 |

<!--TRADE_LOG_END--> 
