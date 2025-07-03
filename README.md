# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 00:34:04**

| Metric | Value |
|---|---|
| **Total Value** | **$101,223.79** |
| Cash | $2,216.79 |
| Holdings Value | $99,007.00 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.44 | $2,124.40 | 70 |
| ADBE | 5 | $377.60 | $378.47 | $1,892.35 | 65 |
| AMD | 15 | $135.93 | $138.52 | $2,077.80 | 70 |
| AMZN | 10 | $221.48 | $219.92 | $2,199.20 | 70 |
| AVGO | 7 | $269.90 | $269.90 | $1,889.30 | 70 |
| AXP | 8 | $324.40 | $325.61 | $2,604.88 | 85 |
| BA | 10 | $212.15 | $212.03 | $2,120.30 | 65 |
| BAC | 54 | $48.69 | $48.71 | $2,630.34 | 85 |
| C | 27 | $86.81 | $86.76 | $2,342.52 | 75 |
| CAT | 6 | $396.45 | $398.43 | $2,390.58 | 85 |
| COST | 2 | $979.83 | $982.36 | $1,964.72 | 65 |
| CRM | 7 | $267.51 | $269.21 | $1,884.47 | 65 |
| CSCO | 34 | $68.37 | $68.59 | $2,332.06 | 75 |
| CVX | 16 | $146.54 | $147.98 | $2,367.68 | 75 |
| DIS | 17 | $122.83 | $122.98 | $2,090.66 | 70 |
| GOOGL | 13 | $177.82 | $178.64 | $2,322.32 | 75 |
| GS | 3 | $717.52 | $715.89 | $2,147.67 | 75 |
| HD | 6 | $372.64 | $371.85 | $2,231.10 | 65 |
| INTC | 90 | $22.33 | $21.88 | $1,969.20 | 65 |
| JNJ | 13 | $155.80 | $155.56 | $2,022.28 | 65 |
| JPM | 8 | $292.56 | $292.00 | $2,336.00 | 75 |
| KO | 28 | $71.03 | $70.91 | $1,985.48 | 65 |
| LLY | 2 | $776.66 | $779.28 | $1,558.56 | 65 |
| MA | 3 | $561.03 | $561.52 | $1,684.56 | 65 |
| META | 3 | $717.12 | $713.57 | $2,140.71 | 75 |
| MRK | 28 | $82.40 | $82.39 | $2,306.92 | 75 |
| MSFT | 5 | $491.36 | $491.09 | $2,455.45 | 85 |
| NFLX | 1 | $1,279.00 | $1,284.86 | $1,284.86 | 70 |
| NKE | 34 | $75.86 | $76.39 | $2,597.26 | 85 |
| NVDA | 15 | $156.02 | $157.25 | $2,358.75 | 75 |
| ORCL | 11 | $225.68 | $229.98 | $2,529.78 | 85 |
| PEP | 15 | $136.59 | $136.48 | $2,047.20 | 65 |
| PFE | 84 | $25.33 | $25.32 | $2,126.88 | 70 |
| PG | 12 | $160.76 | $161.20 | $1,934.40 | 65 |
| PYPL | 30 | $76.82 | $76.31 | $2,289.30 | 75 |
| QCOM | 15 | $161.52 | $162.32 | $2,434.80 | 75 |
| T | 76 | $28.52 | $28.31 | $2,151.56 | 70 |
| TGT | 20 | $105.06 | $105.45 | $2,109.00 | 70 |
| TSLA | 6 | $313.02 | $315.65 | $1,893.90 | 65 |
| UNH | 7 | $314.75 | $307.56 | $2,152.92 | 65 |
| UNP | 9 | $236.50 | $237.16 | $2,134.44 | 70 |
| V | 5 | $352.10 | $354.22 | $1,771.10 | 65 |
| VZ | 52 | $43.73 | $43.59 | $2,266.68 | 75 |
| WFC | 30 | $82.28 | $82.36 | $2,470.80 | 80 |
| WMT | 21 | $97.32 | $97.61 | $2,049.81 | 70 |
| XOM | 21 | $109.93 | $111.05 | $2,332.05 | 75 |

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
| 2025-07-03 00:33:57 | SELL | JPM | 1 | $292.00 | $-0.50 | 75 |
| 2025-07-03 00:33:57 | SELL | NVDA | 1 | $157.25 | $1.15 | 75 |
| 2025-07-03 00:33:57 | SELL | MRK | 3 | $82.39 | $-0.02 | 75 |
| 2025-07-03 00:33:57 | SELL | WFC | 1 | $82.36 | $0.08 | 80 |
| 2025-07-03 00:33:57 | SELL | QCOM | 1 | $162.32 | $0.75 | 75 |
| 2025-07-03 00:33:57 | BUY | INTC | 6 | $21.88 | N/A | 65 |
| 2025-07-03 00:33:57 | BUY | ORCL | 1 | $229.98 | N/A | 85 |
| 2025-07-03 00:33:57 | BUY | TGT | 1 | $105.45 | N/A | 70 |
| 2025-07-02 23:50:34 | SELL | C | 1 | $86.76 | $-0.05 | 75 |
| 2025-07-02 23:50:34 | SELL | ORCL | 1 | $229.98 | $4.30 | 70 |
| 2025-07-02 23:50:34 | SELL | T | 4 | $28.31 | $-0.79 | 70 |
| 2025-07-02 23:50:34 | SELL | TGT | 1 | $105.45 | $0.39 | 65 |
| 2025-07-02 23:50:34 | BUY | NKE | 4 | $76.39 | N/A | 85 |
| 2025-07-02 23:50:34 | BUY | MRK | 3 | $82.39 | N/A | 85 |
| 2025-07-02 23:50:34 | BUY | WFC | 3 | $82.36 | N/A | 85 |
| 2025-07-02 23:50:34 | BUY | QCOM | 1 | $162.32 | N/A | 85 |
| 2025-07-02 23:38:01 | SELL | NKE | 4 | $76.39 | $2.14 | 75 |
| 2025-07-02 23:38:01 | SELL | MRK | 3 | $82.39 | $-0.02 | 75 |
| 2025-07-02 23:38:01 | SELL | WFC | 2 | $82.36 | $0.17 | 75 |
| 2025-07-02 23:38:01 | BUY | PFE | 5 | $25.32 | N/A | 70 |
| 2025-07-02 23:38:01 | BUY | C | 1 | $86.76 | N/A | 80 |
| 2025-07-02 23:38:01 | BUY | ORCL | 1 | $229.98 | N/A | 85 |
| 2025-07-02 23:38:01 | BUY | VZ | 6 | $43.59 | N/A | 75 |
| 2025-07-02 23:38:01 | BUY | T | 4 | $28.31 | N/A | 75 |
| 2025-07-02 23:26:07 | SELL | C | 3 | $86.76 | $-0.13 | 75 |

<!--TRADE_LOG_END--> 
