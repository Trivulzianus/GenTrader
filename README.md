# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 13:44:36**

| Metric | Value |
|---|---|
| **Total Value** | **$101,651.35** |
| Cash | $3,076.95 |
| Holdings Value | $98,574.40 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.58 | $2,125.80 | 70 |
| ADBE | 5 | $377.60 | $381.59 | $1,907.95 | 65 |
| AMD | 15 | $135.93 | $137.85 | $2,067.82 | 70 |
| AMZN | 10 | $221.48 | $222.53 | $2,225.30 | 75 |
| AVGO | 8 | $269.90 | $271.94 | $2,175.48 | 70 |
| AXP | 8 | $324.40 | $326.75 | $2,614.00 | 85 |
| BA | 10 | $212.15 | $215.14 | $2,151.40 | 70 |
| BAC | 53 | $48.69 | $49.11 | $2,602.83 | 85 |
| C | 30 | $86.80 | $87.78 | $2,633.55 | 85 |
| CAT | 6 | $396.45 | $401.13 | $2,406.78 | 65 |
| COST | 2 | $979.83 | $983.61 | $1,967.22 | 65 |
| CRM | 7 | $267.51 | $273.62 | $1,915.31 | 65 |
| CSCO | 32 | $68.35 | $68.66 | $2,196.97 | 70 |
| CVX | 16 | $146.55 | $147.83 | $2,365.28 | 75 |
| DIS | 17 | $122.86 | $123.52 | $2,099.84 | 70 |
| GOOGL | 13 | $177.82 | $177.61 | $2,308.93 | 70 |
| GS | 3 | $717.52 | $718.82 | $2,156.46 | 85 |
| HD | 6 | $372.64 | $369.35 | $2,216.10 | 70 |
| INTC | 84 | $22.33 | $22.32 | $1,875.30 | 60 |
| JNJ | 13 | $155.80 | $155.42 | $2,020.46 | 65 |
| JPM | 9 | $292.50 | $293.74 | $2,643.66 | 85 |
| KO | 28 | $71.03 | $70.67 | $1,978.62 | 65 |
| LLY | 2 | $776.66 | $778.55 | $1,557.10 | 70 |
| MA | 3 | $561.03 | $564.82 | $1,694.45 | 70 |
| META | 3 | $717.12 | $723.50 | $2,170.50 | 85 |
| MRK | 28 | $82.40 | $81.66 | $2,286.48 | 75 |
| MSFT | 5 | $491.36 | $494.56 | $2,472.80 | 85 |
| NFLX | 1 | $1,279.00 | $1,286.78 | $1,286.78 | 65 |
| NKE | 31 | $75.79 | $76.73 | $2,378.61 | 75 |
| NVDA | 14 | $155.93 | $158.14 | $2,213.96 | 75 |
| ORCL | 9 | $224.73 | $233.81 | $2,104.34 | 75 |
| PEP | 15 | $136.59 | $136.21 | $2,043.15 | 65 |
| PFE | 80 | $25.33 | $25.32 | $2,025.78 | 65 |
| PG | 12 | $160.76 | $161.21 | $1,934.51 | 65 |
| PYPL | 30 | $76.82 | $77.06 | $2,311.80 | 75 |
| QCOM | 15 | $161.52 | $163.30 | $2,449.50 | 80 |
| T | 77 | $28.52 | $28.29 | $2,178.34 | 70 |
| TGT | 20 | $105.04 | $105.15 | $2,103.00 | 70 |
| TSLA | 6 | $313.02 | $315.25 | $1,891.50 | 55 |
| UNH | 7 | $314.75 | $310.38 | $2,172.66 | 65 |
| UNP | 9 | $236.50 | $238.10 | $2,142.94 | 75 |
| V | 5 | $352.10 | $355.93 | $1,779.64 | 65 |
| VZ | 46 | $43.73 | $43.73 | $2,011.49 | 65 |
| WFC | 28 | $82.17 | $83.28 | $2,331.70 | 75 |
| WMT | 22 | $97.34 | $97.78 | $2,151.14 | 70 |
| XOM | 20 | $109.86 | $111.36 | $2,227.20 | 70 |

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
| 2025-07-03 13:44:30 | SELL | XOM | 1 | $111.39 | $1.46 | 70 |
| 2025-07-03 13:44:30 | SELL | INTC | 6 | $22.29 | $-0.22 | 60 |
| 2025-07-03 13:44:30 | SELL | PFE | 3 | $25.31 | $-0.06 | 65 |
| 2025-07-03 13:44:30 | SELL | NKE | 2 | $76.68 | $1.68 | 75 |
| 2025-07-03 13:44:30 | SELL | WFC | 3 | $83.26 | $2.94 | 75 |
| 2025-07-03 13:44:30 | SELL | CSCO | 1 | $68.65 | $0.29 | 70 |
| 2025-07-03 13:44:30 | SELL | VZ | 5 | $43.72 | $-0.05 | 65 |
| 2025-07-03 13:44:30 | SELL | T | 3 | $28.29 | $-0.65 | 70 |
| 2025-07-03 13:44:30 | SELL | CVX | 1 | $147.80 | $1.18 | 75 |
| 2025-07-03 13:44:30 | BUY | DIS | 1 | $123.52 | N/A | 70 |
| 2025-07-03 13:44:30 | BUY | WMT | 1 | $97.80 | N/A | 70 |
| 2025-07-03 13:44:30 | BUY | TGT | 1 | $105.13 | N/A | 70 |
| 2025-07-03 13:28:20 | SELL | DIS | 1 | $122.98 | $0.15 | 65 |
| 2025-07-03 13:28:20 | SELL | PFE | 1 | $25.32 | $-0.01 | 70 |
| 2025-07-03 13:28:20 | SELL | CSCO | 1 | $68.59 | $0.22 | 75 |
| 2025-07-03 13:28:20 | SELL | T | 1 | $28.31 | $-0.20 | 75 |
| 2025-07-03 13:28:20 | BUY | VZ | 5 | $43.59 | N/A | 75 |
| 2025-07-03 13:28:20 | BUY | CVX | 1 | $147.98 | N/A | 85 |
| 2025-07-03 13:01:59 | SELL | BAC | 1 | $48.71 | $0.02 | 85 |
| 2025-07-03 13:01:59 | SELL | PFE | 1 | $25.32 | $-0.01 | 70 |
| 2025-07-03 13:01:59 | SELL | TGT | 1 | $105.45 | $0.39 | 65 |
| 2025-07-03 13:01:59 | SELL | CVX | 1 | $147.98 | $1.36 | 75 |
| 2025-07-03 13:01:59 | SELL | VZ | 6 | $43.59 | $-0.83 | 65 |
| 2025-07-03 13:01:59 | BUY | NKE | 1 | $76.39 | N/A | 85 |
| 2025-07-03 13:01:59 | BUY | WFC | 2 | $82.36 | N/A | 85 |

<!--TRADE_LOG_END--> 
