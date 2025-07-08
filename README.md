# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 17:25:39**

| Metric | Value |
|---|---|
| **Total Value** | **$100,748.92** |
| Cash | $911.30 |
| Holdings Value | $99,837.62 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.76 | $2,097.59 | 70 |
| ADBE | 5 | $377.60 | $380.54 | $1,902.70 | 65 |
| AMD | 16 | $135.69 | $137.82 | $2,205.07 | 70 |
| AMZN | 10 | $221.61 | $220.51 | $2,205.15 | 65 |
| AVGO | 8 | $275.34 | $274.95 | $2,199.64 | 65 |
| AXP | 8 | $324.24 | $319.80 | $2,558.40 | 85 |
| BA | 10 | $212.43 | $218.22 | $2,182.15 | 65 |
| BAC | 49 | $48.66 | $47.31 | $2,318.43 | 75 |
| C | 30 | $86.58 | $86.25 | $2,587.65 | 85 |
| CAT | 6 | $397.86 | $394.74 | $2,368.41 | 70 |
| COST | 2 | $979.83 | $989.45 | $1,978.90 | 65 |
| CRM | 8 | $268.33 | $273.09 | $2,184.72 | 65 |
| CSCO | 34 | $68.36 | $68.49 | $2,328.66 | 75 |
| CVX | 17 | $147.05 | $152.89 | $2,599.13 | 85 |
| DIS | 17 | $122.85 | $122.00 | $2,074.00 | 65 |
| GOOGL | 12 | $179.60 | $174.10 | $2,089.20 | 65 |
| GS | 3 | $717.52 | $698.83 | $2,096.49 | 70 |
| HD | 6 | $372.64 | $367.52 | $2,205.12 | 70 |
| INTC | 86 | $22.32 | $23.52 | $2,022.29 | 65 |
| JNJ | 14 | $155.85 | $155.34 | $2,174.76 | 65 |
| JPM | 9 | $291.61 | $281.52 | $2,533.68 | 75 |
| KO | 29 | $71.03 | $70.35 | $2,040.15 | 65 |
| LLY | 2 | $776.66 | $779.42 | $1,558.85 | 65 |
| MA | 4 | $563.08 | $562.49 | $2,249.96 | 65 |
| META | 3 | $717.12 | $720.40 | $2,161.19 | 85 |
| MRK | 29 | $82.49 | $81.15 | $2,353.35 | 75 |
| MSFT | 5 | $498.84 | $495.77 | $2,478.85 | 75 |
| NFLX | 1 | $1,279.00 | $1,276.21 | $1,276.21 | 65 |
| NKE | 28 | $76.06 | $73.82 | $2,067.09 | 65 |
| NVDA | 15 | $156.72 | $159.58 | $2,393.70 | 75 |
| ORCL | 9 | $233.41 | $236.79 | $2,131.15 | 65 |
| PEP | 15 | $136.57 | $134.79 | $2,021.85 | 65 |
| PFE | 87 | $25.25 | $25.49 | $2,217.20 | 70 |
| PG | 13 | $160.77 | $158.06 | $2,054.78 | 65 |
| PYPL | 31 | $76.64 | $74.67 | $2,314.92 | 75 |
| QCOM | 14 | $161.75 | $159.76 | $2,236.61 | 75 |
| T | 72 | $28.54 | $28.39 | $2,043.72 | 65 |
| TGT | 20 | $104.90 | $101.34 | $2,026.80 | 65 |
| TSLA | 6 | $288.62 | $301.73 | $1,810.39 | 60 |
| UNH | 7 | $314.75 | $305.60 | $2,139.20 | 65 |
| UNP | 10 | $236.66 | $236.37 | $2,363.65 | 75 |
| V | 6 | $355.95 | $355.01 | $2,130.06 | 70 |
| VZ | 47 | $43.72 | $43.08 | $2,024.53 | 65 |
| WFC | 29 | $82.34 | $81.79 | $2,371.91 | 75 |
| WMT | 21 | $97.34 | $97.95 | $2,056.95 | 65 |
| XOM | 21 | $110.00 | $114.40 | $2,402.40 | 75 |

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
| 2025-07-08 16:55:22 | BUY | NVDA | 2 | $159.71 | N/A | 85 |
| 2025-07-08 16:55:22 | BUY | PFE | 7 | $25.24 | N/A | 70 |
| 2025-07-08 16:55:22 | BUY | C | 1 | $86.14 | N/A | 85 |
| 2025-07-08 16:43:31 | SELL | NVDA | 2 | $158.24 | $3.04 | 70 |
| 2025-07-08 16:43:31 | SELL | T | 4 | $28.33 | $-0.74 | 70 |
| 2025-07-08 16:43:31 | SELL | WFC | 1 | $81.65 | $-0.66 | 75 |
| 2025-07-08 16:43:31 | BUY | INTC | 1 | $23.38 | N/A | 65 |
| 2025-07-08 16:43:31 | BUY | BAC | 3 | $47.17 | N/A | 75 |
| 2025-07-08 16:28:46 | SELL | PFE | 12 | $25.68 | $4.43 | 65 |

<!--TRADE_LOG_END--> 
