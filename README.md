# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 22:26:32**

| Metric | Value |
|---|---|
| **Total Value** | **$100,667.29** |
| Cash | $846.08 |
| Holdings Value | $99,821.21 |

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
| BAC | 50 | $48.63 | $47.15 | $2,357.50 | 75 |
| C | 27 | $86.71 | $85.57 | $2,310.39 | 75 |
| CAT | 6 | $397.86 | $394.29 | $2,365.74 | 70 |
| COST | 2 | $979.83 | $985.84 | $1,971.68 | 65 |
| CRM | 8 | $268.33 | $273.65 | $2,189.20 | 65 |
| CSCO | 34 | $68.36 | $68.59 | $2,332.06 | 75 |
| CVX | 16 | $146.65 | $153.24 | $2,451.84 | 75 |
| DIS | 17 | $122.85 | $121.82 | $2,070.94 | 65 |
| GOOGL | 12 | $179.60 | $174.36 | $2,092.32 | 65 |
| GS | 3 | $717.52 | $697.28 | $2,091.84 | 70 |
| HD | 6 | $372.64 | $367.50 | $2,205.00 | 65 |
| INTC | 86 | $22.32 | $23.59 | $2,028.74 | 65 |
| JNJ | 13 | $155.89 | $155.79 | $2,025.27 | 65 |
| JPM | 9 | $291.61 | $282.78 | $2,545.02 | 85 |
| KO | 29 | $71.03 | $70.24 | $2,036.96 | 65 |
| LLY | 2 | $776.66 | $777.66 | $1,555.32 | 65 |
| MA | 4 | $563.08 | $562.44 | $2,249.76 | 65 |
| META | 3 | $717.12 | $720.67 | $2,162.01 | 75 |
| MRK | 29 | $82.50 | $81.37 | $2,359.73 | 75 |
| MSFT | 5 | $498.84 | $496.62 | $2,483.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,275.31 | $1,275.31 | 65 |
| NKE | 28 | $76.05 | $73.92 | $2,069.76 | 65 |
| NVDA | 16 | $157.22 | $160.00 | $2,560.00 | 85 |
| ORCL | 10 | $233.52 | $234.50 | $2,345.00 | 70 |
| PEP | 16 | $136.47 | $135.04 | $2,160.64 | 65 |
| PFE | 104 | $25.31 | $25.62 | $2,664.48 | 85 |
| PG | 13 | $160.77 | $157.89 | $2,052.57 | 65 |
| PYPL | 30 | $76.70 | $75.03 | $2,250.90 | 70 |
| QCOM | 14 | $161.76 | $159.45 | $2,232.30 | 70 |
| T | 72 | $28.56 | $28.29 | $2,036.88 | 65 |
| TGT | 20 | $104.90 | $102.01 | $2,040.20 | 65 |
| TSLA | 6 | $288.62 | $297.81 | $1,786.86 | 65 |
| UNH | 7 | $314.75 | $307.70 | $2,153.90 | 65 |
| UNP | 10 | $236.66 | $236.54 | $2,365.40 | 75 |
| V | 6 | $355.95 | $354.55 | $2,127.30 | 65 |
| VZ | 47 | $43.16 | $43.06 | $2,023.82 | 65 |
| WFC | 29 | $82.33 | $81.59 | $2,366.11 | 75 |
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
| 2025-07-08 22:26:01 | SELL | PYPL | 1 | $75.03 | $-1.62 | 70 |
| 2025-07-08 22:26:01 | SELL | NKE | 1 | $73.92 | $-2.05 | 65 |
| 2025-07-08 22:26:01 | BUY | NVDA | 2 | $160.00 | N/A | 85 |
| 2025-07-08 22:26:01 | BUY | PFE | 1 | $25.62 | N/A | 85 |
| 2025-07-08 22:08:11 | SELL | WMT | 3 | $97.09 | $-0.68 | 65 |
| 2025-07-08 22:08:11 | SELL | TGT | 1 | $102.01 | $-2.76 | 65 |
| 2025-07-08 22:08:11 | BUY | PFE | 11 | $25.62 | N/A | 85 |
| 2025-07-08 22:08:11 | BUY | C | 1 | $85.57 | N/A | 75 |
| 2025-07-08 21:50:11 | SELL | XOM | 2 | $114.19 | $7.60 | 75 |
| 2025-07-08 21:50:11 | SELL | PFE | 7 | $25.62 | $2.29 | 75 |
| 2025-07-08 21:50:11 | SELL | WFC | 1 | $81.59 | $-0.72 | 75 |
| 2025-07-08 21:50:11 | BUY | NKE | 1 | $73.92 | N/A | 70 |
| 2025-07-08 21:50:11 | BUY | PEP | 1 | $135.04 | N/A | 70 |
| 2025-07-08 21:50:11 | BUY | ORCL | 1 | $234.50 | N/A | 75 |
| 2025-07-08 21:50:11 | BUY | TGT | 1 | $102.01 | N/A | 70 |
| 2025-07-08 21:37:39 | SELL | PFE | 4 | $25.62 | $1.26 | 80 |
| 2025-07-08 21:37:39 | SELL | AXP | 1 | $316.98 | $-7.26 | 70 |
| 2025-07-08 21:37:39 | SELL | NKE | 1 | $73.92 | $-2.05 | 65 |
| 2025-07-08 21:37:39 | SELL | C | 1 | $85.57 | $-1.14 | 70 |
| 2025-07-08 21:37:39 | BUY | BAC | 3 | $47.15 | N/A | 75 |
| 2025-07-08 21:37:39 | BUY | XOM | 2 | $114.19 | N/A | 85 |
| 2025-07-08 21:37:39 | BUY | WFC | 1 | $81.59 | N/A | 80 |
| 2025-07-08 21:37:39 | BUY | WMT | 3 | $97.09 | N/A | 75 |
| 2025-07-08 21:25:50 | SELL | NVDA | 1 | $160.00 | $2.97 | 70 |
| 2025-07-08 21:25:50 | SELL | XOM | 2 | $114.19 | $7.60 | 75 |

<!--TRADE_LOG_END--> 
