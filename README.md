# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 16:43:48**

| Metric | Value |
|---|---|
| **Total Value** | **$101,059.40** |
| Cash | $4,187.12 |
| Holdings Value | $96,872.29 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $210.35 | $2,103.47 | 65 |
| ADBE | 5 | $377.60 | $373.53 | $1,867.65 | 65 |
| AMD | 16 | $136.11 | $139.13 | $2,226.08 | 70 |
| AMZN | 10 | $221.48 | $220.92 | $2,209.20 | 75 |
| AVGO | 8 | $269.38 | $271.56 | $2,172.44 | 70 |
| AXP | 8 | $324.40 | $324.80 | $2,598.36 | 85 |
| BA | 9 | $212.09 | $213.18 | $1,918.61 | 65 |
| BAC | 54 | $48.67 | $48.60 | $2,624.67 | 85 |
| C | 26 | $86.79 | $86.86 | $2,258.49 | 70 |
| CAT | 5 | $396.55 | $396.09 | $1,980.47 | 75 |
| COST | 2 | $979.83 | $982.01 | $1,964.02 | 65 |
| CRM | 7 | $267.51 | $267.97 | $1,875.79 | 65 |
| CSCO | 32 | $68.35 | $68.62 | $2,195.84 | 70 |
| CVX | 17 | $146.51 | $146.28 | $2,486.84 | 80 |
| DIS | 17 | $122.83 | $122.97 | $2,090.49 | 70 |
| GOOGL | 13 | $177.82 | $177.89 | $2,312.57 | 75 |
| GS | 3 | $717.52 | $716.85 | $2,150.55 | 70 |
| HD | 5 | $372.57 | $371.98 | $1,859.91 | 65 |
| INTC | 92 | $22.34 | $22.09 | $2,031.82 | 65 |
| JNJ | 13 | $155.80 | $155.47 | $2,021.11 | 65 |
| JPM | 9 | $292.49 | $292.08 | $2,628.76 | 75 |
| KO | 28 | $71.03 | $70.89 | $1,984.78 | 65 |
| LLY | 2 | $776.66 | $778.00 | $1,556.00 | 65 |
| MA | 3 | $561.03 | $558.04 | $1,674.12 | 65 |
| META | 3 | $717.12 | $718.90 | $2,156.70 | 75 |
| MRK | 28 | $82.43 | $82.14 | $2,299.92 | 75 |
| MSFT | 4 | $491.43 | $491.78 | $1,967.12 | 75 |
| NFLX | 1 | $1,279.00 | $1,280.87 | $1,280.87 | 65 |
| NKE | 31 | $75.84 | $76.13 | $2,360.03 | 75 |
| NVDA | 16 | $156.59 | $157.27 | $2,516.32 | 85 |
| ORCL | 10 | $224.98 | $225.04 | $2,250.40 | 65 |
| PEP | 15 | $136.59 | $136.50 | $2,047.50 | 65 |
| PFE | 81 | $25.33 | $25.23 | $2,044.03 | 65 |
| PG | 12 | $160.76 | $160.70 | $1,928.40 | 65 |
| PYPL | 30 | $76.82 | $76.47 | $2,293.95 | 75 |
| QCOM | 14 | $161.49 | $161.49 | $2,260.86 | 75 |
| T | 72 | $28.50 | $28.55 | $2,055.85 | 65 |
| TGT | 20 | $105.06 | $104.82 | $2,096.40 | 65 |
| TSLA | 6 | $313.02 | $313.29 | $1,879.74 | 65 |
| UNH | 6 | $315.70 | $312.79 | $1,876.71 | 65 |
| UNP | 9 | $236.50 | $235.74 | $2,121.62 | 70 |
| V | 5 | $352.10 | $350.83 | $1,754.15 | 65 |
| VZ | 46 | $43.75 | $43.72 | $2,011.12 | 65 |
| WFC | 32 | $82.28 | $82.13 | $2,628.16 | 85 |
| WMT | 21 | $97.29 | $97.69 | $2,051.49 | 65 |
| XOM | 20 | $109.91 | $109.94 | $2,198.90 | 70 |

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
| 2025-07-02 16:26:58 | BUY | NKE | 1 | $76.31 | N/A | 85 |
| 2025-07-02 16:26:58 | BUY | TGT | 1 | $104.77 | N/A | 70 |
| 2025-07-02 16:09:58 | SELL | C | 1 | $86.82 | $0.02 | 70 |
| 2025-07-02 16:09:58 | SELL | WMT | 1 | $97.34 | $0.04 | 70 |
| 2025-07-02 16:09:58 | BUY | AAPL | 1 | $211.08 | N/A | 75 |
| 2025-07-02 16:09:58 | BUY | BAC | 9 | $48.60 | N/A | 85 |
| 2025-07-02 16:09:58 | BUY | INTC | 7 | $22.17 | N/A | 65 |
| 2025-07-02 16:09:58 | BUY | DIS | 1 | $122.82 | N/A | 70 |
| 2025-07-02 16:09:58 | BUY | PFE | 5 | $25.23 | N/A | 70 |
| 2025-07-02 16:09:58 | BUY | AXP | 2 | $323.87 | N/A | 85 |
| 2025-07-02 16:09:58 | BUY | UNP | 1 | $235.84 | N/A | 70 |

<!--TRADE_LOG_END--> 
