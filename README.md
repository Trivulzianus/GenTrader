# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 15:39:30**

| Metric | Value |
|---|---|
| **Total Value** | **$100,799.37** |
| Cash | $824.30 |
| Holdings Value | $99,975.08 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.84 | $2,098.35 | 65 |
| ADBE | 5 | $377.60 | $383.55 | $1,917.75 | 65 |
| AMD | 16 | $135.69 | $137.75 | $2,203.92 | 70 |
| AMZN | 10 | $221.61 | $220.20 | $2,202.03 | 70 |
| AVGO | 8 | $275.34 | $274.23 | $2,193.84 | 65 |
| AXP | 8 | $324.24 | $320.56 | $2,564.48 | 85 |
| BA | 9 | $211.84 | $216.48 | $1,948.33 | 65 |
| BAC | 46 | $48.76 | $47.30 | $2,175.57 | 70 |
| C | 30 | $86.58 | $86.14 | $2,584.35 | 85 |
| CAT | 6 | $397.86 | $393.51 | $2,361.08 | 70 |
| COST | 2 | $979.83 | $989.19 | $1,978.39 | 65 |
| CRM | 8 | $268.33 | $274.80 | $2,198.40 | 65 |
| CSCO | 32 | $68.36 | $68.59 | $2,194.88 | 70 |
| CVX | 16 | $146.69 | $151.38 | $2,422.09 | 80 |
| DIS | 17 | $122.85 | $122.36 | $2,080.03 | 70 |
| GOOGL | 12 | $179.60 | $174.10 | $2,089.20 | 65 |
| GS | 3 | $717.52 | $700.92 | $2,102.77 | 70 |
| HD | 6 | $372.64 | $368.99 | $2,213.94 | 70 |
| INTC | 85 | $22.29 | $23.30 | $1,980.08 | 60 |
| JNJ | 13 | $155.81 | $156.22 | $2,030.86 | 70 |
| JPM | 9 | $291.61 | $282.83 | $2,545.47 | 85 |
| KO | 29 | $71.03 | $70.21 | $2,036.09 | 65 |
| LLY | 2 | $776.66 | $789.42 | $1,578.85 | 65 |
| MA | 4 | $563.08 | $563.30 | $2,253.22 | 65 |
| META | 3 | $717.12 | $718.77 | $2,156.31 | 75 |
| MRK | 29 | $82.43 | $81.96 | $2,376.84 | 75 |
| MSFT | 5 | $498.84 | $495.20 | $2,476.00 | 75 |
| NFLX | 1 | $1,279.00 | $1,271.53 | $1,271.53 | 65 |
| NKE | 30 | $75.91 | $74.21 | $2,226.30 | 70 |
| NVDA | 16 | $156.63 | $159.06 | $2,544.94 | 85 |
| ORCL | 9 | $233.41 | $233.76 | $2,103.88 | 75 |
| PEP | 15 | $136.57 | $135.06 | $2,025.97 | 65 |
| PFE | 90 | $25.31 | $25.75 | $2,317.95 | 75 |
| PG | 13 | $160.77 | $158.49 | $2,060.37 | 65 |
| PYPL | 31 | $76.64 | $75.17 | $2,330.27 | 75 |
| QCOM | 14 | $161.75 | $160.69 | $2,249.66 | 75 |
| T | 76 | $28.53 | $28.25 | $2,146.62 | 70 |
| TGT | 20 | $104.90 | $101.41 | $2,028.10 | 65 |
| TSLA | 6 | $288.62 | $302.52 | $1,815.15 | 65 |
| UNH | 7 | $314.75 | $306.45 | $2,145.15 | 65 |
| UNP | 10 | $236.66 | $237.34 | $2,373.40 | 75 |
| V | 6 | $355.95 | $355.99 | $2,135.94 | 65 |
| VZ | 47 | $43.72 | $43.09 | $2,025.00 | 65 |
| WFC | 29 | $82.34 | $81.58 | $2,365.73 | 75 |
| WMT | 23 | $97.42 | $97.28 | $2,237.55 | 75 |
| XOM | 23 | $110.29 | $113.41 | $2,608.43 | 85 |

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
| 2025-07-08 15:39:25 | SELL | BAC | 1 | $47.29 | $-1.43 | 70 |
| 2025-07-08 15:39:25 | SELL | INTC | 3 | $22.00 | $-0.83 | 60 |
| 2025-07-08 15:39:25 | SELL | UNP | 1 | $237.31 | $0.59 | 75 |
| 2025-07-08 15:39:25 | SELL | CSCO | 1 | $68.58 | $0.22 | 70 |
| 2025-07-08 15:39:25 | BUY | XOM | 1 | $113.43 | N/A | 85 |
| 2025-07-08 15:39:25 | BUY | WMT | 2 | $97.29 | N/A | 75 |
| 2025-07-08 15:39:25 | BUY | PFE | 9 | $25.76 | N/A | 75 |
| 2025-07-08 15:39:25 | BUY | C | 2 | $86.16 | N/A | 85 |
| 2025-07-08 15:39:25 | BUY | T | 3 | $28.25 | N/A | 70 |
| 2025-07-08 15:26:24 | SELL | XOM | 1 | $113.18 | $2.90 | 75 |
| 2025-07-08 15:26:24 | SELL | DIS | 1 | $122.26 | $-0.55 | 65 |
| 2025-07-08 15:26:24 | SELL | PFE | 4 | $25.75 | $1.90 | 65 |
| 2025-07-08 15:26:24 | SELL | C | 2 | $86.00 | $-1.14 | 75 |
| 2025-07-08 15:26:24 | SELL | CSCO | 1 | $68.57 | $0.19 | 70 |
| 2025-07-08 15:26:24 | SELL | CVX | 1 | $151.10 | $4.15 | 75 |
| 2025-07-08 15:26:24 | BUY | NVDA | 2 | $159.00 | N/A | 85 |
| 2025-07-08 15:26:24 | BUY | INTC | 1 | $23.26 | N/A | 65 |
| 2025-07-08 15:26:24 | BUY | NKE | 1 | $74.01 | N/A | 70 |
| 2025-07-08 15:08:40 | SELL | BAC | 3 | $47.21 | $-4.29 | 70 |
| 2025-07-08 15:08:40 | SELL | INTC | 1 | $23.42 | $1.15 | 65 |
| 2025-07-08 15:08:40 | SELL | WMT | 1 | $96.97 | $-0.44 | 65 |
| 2025-07-08 15:08:40 | SELL | PFE | 1 | $25.92 | $0.64 | 70 |
| 2025-07-08 15:08:40 | SELL | BA | 2 | $215.10 | $5.32 | 60 |
| 2025-07-08 15:08:40 | BUY | XOM | 2 | $113.91 | N/A | 85 |
| 2025-07-08 15:08:40 | BUY | C | 3 | $85.85 | N/A | 85 |

<!--TRADE_LOG_END--> 
