# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 16:27:04**

| Metric | Value |
|---|---|
| **Total Value** | **$101,040.90** |
| Cash | $4,357.04 |
| Holdings Value | $96,683.87 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.36 | $211.04 | $2,321.44 | 70 |
| ADBE | 5 | $377.60 | $375.33 | $1,876.67 | 65 |
| AMD | 16 | $136.11 | $139.60 | $2,233.68 | 70 |
| AMZN | 10 | $221.48 | $220.88 | $2,208.85 | 70 |
| AVGO | 8 | $269.38 | $270.40 | $2,163.20 | 70 |
| AXP | 7 | $324.35 | $323.52 | $2,264.67 | 70 |
| BA | 9 | $212.09 | $212.74 | $1,914.66 | 65 |
| BAC | 54 | $48.67 | $48.62 | $2,625.21 | 85 |
| C | 26 | $86.79 | $86.85 | $2,258.10 | 70 |
| CAT | 5 | $396.55 | $395.77 | $1,978.85 | 70 |
| COST | 2 | $979.83 | $979.86 | $1,959.72 | 65 |
| CRM | 7 | $267.51 | $267.47 | $1,872.29 | 65 |
| CSCO | 34 | $68.37 | $68.58 | $2,331.72 | 75 |
| CVX | 16 | $146.52 | $146.47 | $2,343.52 | 75 |
| DIS | 17 | $122.83 | $122.85 | $2,088.45 | 70 |
| GOOGL | 13 | $177.82 | $177.54 | $2,308.09 | 75 |
| GS | 3 | $717.52 | $716.95 | $2,150.84 | 70 |
| HD | 5 | $372.57 | $371.67 | $1,858.33 | 65 |
| INTC | 85 | $22.36 | $22.23 | $1,889.14 | 60 |
| JNJ | 13 | $155.80 | $155.37 | $2,019.81 | 65 |
| JPM | 9 | $292.49 | $291.92 | $2,627.28 | 85 |
| KO | 28 | $71.03 | $70.84 | $1,983.66 | 65 |
| LLY | 2 | $776.66 | $775.30 | $1,550.60 | 65 |
| MA | 3 | $561.03 | $558.64 | $1,675.92 | 65 |
| META | 3 | $717.12 | $718.04 | $2,154.11 | 75 |
| MRK | 28 | $82.43 | $82.29 | $2,304.12 | 75 |
| MSFT | 4 | $491.43 | $491.81 | $1,967.24 | 75 |
| NFLX | 1 | $1,279.00 | $1,281.50 | $1,281.50 | 65 |
| NKE | 34 | $75.86 | $76.33 | $2,595.39 | 85 |
| NVDA | 16 | $156.59 | $157.01 | $2,512.20 | 85 |
| ORCL | 10 | $224.98 | $225.12 | $2,251.25 | 75 |
| PEP | 15 | $136.59 | $136.45 | $2,046.75 | 65 |
| PFE | 86 | $25.33 | $25.21 | $2,167.66 | 70 |
| PG | 12 | $160.76 | $160.60 | $1,927.20 | 65 |
| PYPL | 30 | $76.82 | $76.53 | $2,295.90 | 75 |
| QCOM | 14 | $161.49 | $161.34 | $2,258.76 | 75 |
| T | 72 | $28.50 | $28.48 | $2,050.20 | 65 |
| TGT | 20 | $105.06 | $104.76 | $2,095.25 | 70 |
| TSLA | 6 | $313.02 | $313.28 | $1,879.68 | 65 |
| UNH | 6 | $315.70 | $313.18 | $1,879.08 | 65 |
| UNP | 9 | $236.50 | $235.92 | $2,123.28 | 70 |
| V | 5 | $352.10 | $350.71 | $1,753.57 | 65 |
| VZ | 46 | $43.75 | $43.65 | $2,007.89 | 65 |
| WFC | 29 | $82.30 | $82.14 | $2,381.91 | 75 |
| WMT | 21 | $97.29 | $97.42 | $2,045.82 | 65 |
| XOM | 20 | $109.91 | $110.02 | $2,200.40 | 70 |

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
| 2025-07-02 16:09:58 | BUY | WFC | 2 | $82.15 | N/A | 85 |
| 2025-07-02 16:09:58 | BUY | ORCL | 1 | $224.76 | N/A | 75 |
| 2025-07-02 16:09:58 | BUY | CSCO | 2 | $68.45 | N/A | 75 |
| 2025-07-02 16:09:58 | BUY | T | 4 | $28.46 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | MSFT | 4 | $491.43 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | GOOGL | 13 | $177.82 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | AMZN | 10 | $221.48 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | NVDA | 14 | $156.51 | N/A | 70 |

<!--TRADE_LOG_END--> 
