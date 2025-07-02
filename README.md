# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 16:55:57**

| Metric | Value |
|---|---|
| **Total Value** | **$101,044.17** |
| Cash | $3,427.95 |
| Holdings Value | $97,616.22 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $211.03 | $2,110.30 | 70 |
| ADBE | 5 | $377.60 | $374.03 | $1,870.16 | 65 |
| AMD | 16 | $136.11 | $139.13 | $2,226.08 | 70 |
| AMZN | 10 | $221.48 | $220.64 | $2,206.39 | 70 |
| AVGO | 8 | $269.38 | $270.93 | $2,167.44 | 70 |
| AXP | 8 | $324.40 | $325.11 | $2,600.84 | 85 |
| BA | 10 | $212.15 | $212.76 | $2,127.65 | 70 |
| BAC | 54 | $48.67 | $48.55 | $2,621.97 | 85 |
| C | 30 | $86.79 | $86.75 | $2,602.35 | 85 |
| CAT | 6 | $396.45 | $395.94 | $2,375.64 | 85 |
| COST | 2 | $979.83 | $982.31 | $1,964.62 | 65 |
| CRM | 7 | $267.51 | $267.73 | $1,874.08 | 65 |
| CSCO | 34 | $68.37 | $68.61 | $2,332.74 | 75 |
| CVX | 16 | $146.51 | $146.49 | $2,343.84 | 75 |
| DIS | 17 | $122.83 | $122.92 | $2,089.64 | 70 |
| GOOGL | 13 | $177.82 | $178.00 | $2,314.07 | 75 |
| GS | 3 | $717.52 | $716.37 | $2,149.10 | 70 |
| HD | 5 | $372.57 | $371.87 | $1,859.35 | 65 |
| INTC | 92 | $22.34 | $22.07 | $2,030.90 | 65 |
| JNJ | 13 | $155.80 | $155.59 | $2,022.67 | 65 |
| JPM | 9 | $292.49 | $291.92 | $2,627.24 | 75 |
| KO | 28 | $71.03 | $70.89 | $1,985.06 | 65 |
| LLY | 2 | $776.66 | $777.52 | $1,555.04 | 65 |
| MA | 3 | $561.03 | $559.64 | $1,678.93 | 65 |
| META | 3 | $717.12 | $718.17 | $2,154.51 | 75 |
| MRK | 25 | $82.47 | $82.11 | $2,052.75 | 65 |
| MSFT | 4 | $491.43 | $491.30 | $1,965.20 | 75 |
| NFLX | 1 | $1,279.00 | $1,280.54 | $1,280.54 | 65 |
| NKE | 32 | $75.84 | $75.98 | $2,431.52 | 80 |
| NVDA | 14 | $156.49 | $157.28 | $2,201.99 | 70 |
| ORCL | 10 | $224.98 | $225.45 | $2,254.50 | 70 |
| PEP | 15 | $136.59 | $136.47 | $2,047.03 | 65 |
| PFE | 81 | $25.33 | $25.23 | $2,043.23 | 65 |
| PG | 12 | $160.76 | $160.70 | $1,928.40 | 65 |
| PYPL | 30 | $76.82 | $76.39 | $2,291.63 | 75 |
| QCOM | 14 | $161.49 | $161.35 | $2,258.92 | 75 |
| T | 71 | $28.50 | $28.52 | $2,024.57 | 65 |
| TGT | 20 | $105.06 | $104.64 | $2,092.70 | 65 |
| TSLA | 6 | $313.02 | $313.32 | $1,879.92 | 65 |
| UNH | 6 | $315.70 | $313.10 | $1,878.57 | 65 |
| UNP | 9 | $236.50 | $235.63 | $2,120.72 | 65 |
| V | 5 | $352.10 | $352.12 | $1,760.60 | 60 |
| VZ | 49 | $43.74 | $43.68 | $2,140.32 | 70 |
| WFC | 32 | $82.28 | $82.06 | $2,625.76 | 85 |
| WMT | 23 | $97.31 | $97.59 | $2,244.57 | 75 |
| XOM | 20 | $109.91 | $110.11 | $2,202.20 | 70 |

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
| 2025-07-02 16:55:51 | SELL | NVDA | 2 | $157.33 | $1.47 | 70 |
| 2025-07-02 16:55:51 | SELL | MRK | 3 | $82.13 | $-0.91 | 65 |
| 2025-07-02 16:55:51 | SELL | T | 1 | $28.52 | $0.02 | 65 |
| 2025-07-02 16:55:51 | SELL | CVX | 1 | $146.48 | $-0.03 | 75 |
| 2025-07-02 16:55:51 | BUY | WMT | 2 | $97.59 | N/A | 75 |
| 2025-07-02 16:55:51 | BUY | NKE | 1 | $76.05 | N/A | 80 |
| 2025-07-02 16:55:51 | BUY | C | 4 | $86.75 | N/A | 85 |
| 2025-07-02 16:55:51 | BUY | BA | 1 | $212.72 | N/A | 70 |
| 2025-07-02 16:55:51 | BUY | CAT | 1 | $395.95 | N/A | 85 |
| 2025-07-02 16:55:51 | BUY | CSCO | 2 | $68.61 | N/A | 75 |
| 2025-07-02 16:55:51 | BUY | VZ | 3 | $43.69 | N/A | 70 |
| 2025-07-02 16:43:41 | SELL | AAPL | 1 | $210.38 | $-0.98 | 65 |
| 2025-07-02 16:43:41 | SELL | NKE | 3 | $76.15 | $0.86 | 75 |
| 2025-07-02 16:43:41 | SELL | PFE | 5 | $25.24 | $-0.47 | 65 |
| 2025-07-02 16:43:41 | SELL | CSCO | 2 | $68.62 | $0.50 | 70 |
| 2025-07-02 16:43:41 | BUY | INTC | 7 | $22.10 | N/A | 65 |
| 2025-07-02 16:43:41 | BUY | AXP | 1 | $324.77 | N/A | 85 |
| 2025-07-02 16:43:41 | BUY | WFC | 3 | $82.13 | N/A | 85 |
| 2025-07-02 16:43:41 | BUY | CVX | 1 | $146.29 | N/A | 80 |
| 2025-07-02 16:26:58 | SELL | INTC | 6 | $22.21 | $-0.84 | 60 |
| 2025-07-02 16:26:58 | SELL | WMT | 2 | $97.41 | $0.22 | 65 |
| 2025-07-02 16:26:58 | SELL | AXP | 1 | $323.42 | $-0.81 | 70 |
| 2025-07-02 16:26:58 | SELL | WFC | 3 | $82.09 | $-0.55 | 75 |
| 2025-07-02 16:26:58 | SELL | T | 4 | $28.48 | $-0.11 | 65 |
| 2025-07-02 16:26:58 | BUY | NVDA | 2 | $157.13 | N/A | 85 |

<!--TRADE_LOG_END--> 
