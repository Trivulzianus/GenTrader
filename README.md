# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 20:09:22**

| Metric | Value |
|---|---|
| **Total Value** | **$100,667.98** |
| Cash | $1,430.16 |
| Holdings Value | $99,237.82 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.01 | $2,100.10 | 65 |
| ADBE | 5 | $377.60 | $382.24 | $1,911.20 | 65 |
| AMD | 16 | $135.69 | $137.82 | $2,205.12 | 70 |
| AMZN | 10 | $221.61 | $219.36 | $2,193.60 | 70 |
| AVGO | 8 | $275.34 | $271.80 | $2,174.40 | 65 |
| AXP | 8 | $324.24 | $317.07 | $2,536.56 | 85 |
| BA | 10 | $212.43 | $218.50 | $2,185.00 | 65 |
| BAC | 49 | $48.66 | $47.15 | $2,310.11 | 75 |
| C | 26 | $86.75 | $85.57 | $2,224.82 | 70 |
| CAT | 6 | $397.86 | $394.47 | $2,366.82 | 70 |
| COST | 2 | $979.83 | $985.84 | $1,971.68 | 65 |
| CRM | 8 | $268.33 | $273.67 | $2,189.36 | 65 |
| CSCO | 32 | $68.34 | $68.59 | $2,194.88 | 70 |
| CVX | 17 | $147.04 | $153.21 | $2,604.49 | 85 |
| DIS | 17 | $122.85 | $121.84 | $2,071.36 | 65 |
| GOOGL | 12 | $179.60 | $174.36 | $2,092.32 | 65 |
| GS | 3 | $717.52 | $697.11 | $2,091.33 | 75 |
| HD | 6 | $372.64 | $367.52 | $2,205.15 | 70 |
| INTC | 86 | $22.32 | $23.59 | $2,028.74 | 65 |
| JNJ | 13 | $155.89 | $155.79 | $2,025.27 | 65 |
| JPM | 9 | $291.61 | $282.66 | $2,543.94 | 85 |
| KO | 29 | $71.03 | $70.27 | $2,037.68 | 65 |
| LLY | 2 | $776.66 | $778.32 | $1,556.64 | 65 |
| MA | 4 | $563.08 | $562.40 | $2,249.60 | 65 |
| META | 3 | $717.12 | $720.67 | $2,162.01 | 75 |
| MRK | 29 | $82.50 | $81.38 | $2,360.02 | 75 |
| MSFT | 5 | $498.84 | $496.62 | $2,483.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,275.31 | $1,275.31 | 65 |
| NKE | 28 | $76.05 | $73.96 | $2,070.79 | 65 |
| NVDA | 14 | $156.82 | $160.00 | $2,240.00 | 70 |
| ORCL | 9 | $233.41 | $234.41 | $2,109.69 | 75 |
| PEP | 15 | $136.57 | $135.04 | $2,025.60 | 65 |
| PFE | 86 | $25.24 | $25.62 | $2,203.75 | 70 |
| PG | 13 | $160.77 | $157.86 | $2,052.18 | 65 |
| PYPL | 31 | $76.65 | $75.03 | $2,325.93 | 75 |
| QCOM | 14 | $161.76 | $159.45 | $2,232.30 | 75 |
| T | 72 | $28.56 | $28.30 | $2,037.60 | 65 |
| TGT | 20 | $104.90 | $101.99 | $2,039.80 | 65 |
| TSLA | 6 | $288.62 | $297.81 | $1,786.86 | 65 |
| UNH | 7 | $314.75 | $307.64 | $2,153.46 | 65 |
| UNP | 10 | $236.66 | $236.58 | $2,365.80 | 75 |
| V | 6 | $355.95 | $354.11 | $2,124.63 | 70 |
| VZ | 47 | $43.16 | $43.06 | $2,024.05 | 65 |
| WFC | 29 | $82.33 | $81.60 | $2,366.40 | 75 |
| WMT | 24 | $97.32 | $97.09 | $2,330.16 | 75 |
| XOM | 21 | $110.03 | $114.20 | $2,398.20 | 75 |

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
| 2025-07-08 20:09:14 | SELL | PFE | 17 | $25.62 | $5.42 | 70 |
| 2025-07-08 20:09:14 | SELL | C | 4 | $85.57 | $-4.09 | 70 |
| 2025-07-08 20:09:14 | SELL | CSCO | 1 | $68.59 | $0.24 | 70 |
| 2025-07-08 20:09:14 | SELL | T | 5 | $28.30 | $-1.21 | 65 |
| 2025-07-08 20:09:14 | BUY | INTC | 1 | $23.59 | N/A | 65 |
| 2025-07-08 20:09:14 | BUY | WMT | 3 | $97.09 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
