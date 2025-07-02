# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 16:10:07**

| Metric | Value |
|---|---|
| **Total Value** | **$101,051.28** |
| Cash | $3,840.69 |
| Holdings Value | $97,210.59 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.36 | $211.11 | $2,322.21 | 75 |
| ADBE | 5 | $377.60 | $375.89 | $1,879.47 | 65 |
| AMD | 16 | $136.11 | $139.14 | $2,226.20 | 70 |
| AMZN | 10 | $221.48 | $221.35 | $2,213.50 | 70 |
| AVGO | 8 | $269.38 | $270.23 | $2,161.84 | 65 |
| AXP | 8 | $324.23 | $323.79 | $2,590.32 | 85 |
| BA | 9 | $212.09 | $212.58 | $1,913.22 | 65 |
| BAC | 54 | $48.67 | $48.60 | $2,624.40 | 85 |
| C | 26 | $86.79 | $86.81 | $2,257.06 | 70 |
| CAT | 5 | $396.55 | $395.94 | $1,979.67 | 75 |
| COST | 2 | $979.83 | $978.84 | $1,957.67 | 65 |
| CRM | 7 | $267.51 | $267.67 | $1,873.69 | 65 |
| CSCO | 34 | $68.37 | $68.45 | $2,327.30 | 75 |
| CVX | 16 | $146.52 | $146.38 | $2,342.08 | 75 |
| DIS | 17 | $122.83 | $122.81 | $2,087.77 | 70 |
| GOOGL | 13 | $177.82 | $178.11 | $2,315.43 | 75 |
| GS | 3 | $717.52 | $716.63 | $2,149.89 | 75 |
| HD | 5 | $372.57 | $371.45 | $1,857.25 | 70 |
| INTC | 91 | $22.35 | $22.18 | $2,018.38 | 65 |
| JNJ | 13 | $155.80 | $155.51 | $2,021.63 | 65 |
| JPM | 9 | $292.49 | $292.41 | $2,631.69 | 85 |
| KO | 28 | $71.03 | $70.91 | $1,985.34 | 65 |
| LLY | 2 | $776.66 | $777.83 | $1,555.66 | 65 |
| MA | 3 | $561.03 | $559.67 | $1,679.01 | 65 |
| META | 3 | $717.12 | $718.47 | $2,155.41 | 75 |
| MRK | 28 | $82.43 | $82.43 | $2,308.04 | 75 |
| MSFT | 4 | $491.43 | $492.32 | $1,969.28 | 70 |
| NFLX | 1 | $1,279.00 | $1,282.89 | $1,282.89 | 65 |
| NKE | 33 | $75.85 | $76.15 | $2,512.95 | 80 |
| NVDA | 14 | $156.51 | $156.92 | $2,196.90 | 70 |
| ORCL | 10 | $224.98 | $224.66 | $2,246.65 | 75 |
| PEP | 15 | $136.59 | $136.29 | $2,044.35 | 65 |
| PFE | 86 | $25.33 | $25.24 | $2,170.47 | 70 |
| PG | 12 | $160.76 | $160.35 | $1,924.24 | 65 |
| PYPL | 30 | $76.82 | $76.64 | $2,299.20 | 75 |
| QCOM | 14 | $161.49 | $161.31 | $2,258.34 | 75 |
| T | 76 | $28.50 | $28.45 | $2,162.20 | 70 |
| TGT | 19 | $105.07 | $104.83 | $1,991.86 | 65 |
| TSLA | 6 | $313.02 | $313.06 | $1,878.35 | 65 |
| UNH | 6 | $315.70 | $313.89 | $1,883.37 | 65 |
| UNP | 9 | $236.50 | $235.84 | $2,122.52 | 70 |
| V | 5 | $352.10 | $351.45 | $1,757.25 | 65 |
| VZ | 46 | $43.75 | $43.66 | $2,008.59 | 65 |
| WFC | 32 | $82.28 | $82.17 | $2,629.28 | 85 |
| WMT | 23 | $97.30 | $97.32 | $2,238.36 | 70 |
| XOM | 20 | $109.91 | $109.97 | $2,199.40 | 70 |

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
| 2025-07-02 15:51:25 | BUY | META | 3 | $717.12 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | JNJ | 13 | $155.80 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | AAPL | 10 | $211.39 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | TSLA | 6 | $313.02 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | JPM | 9 | $292.49 | N/A | 85 |
| 2025-07-02 15:51:25 | BUY | V | 5 | $352.10 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | UNH | 6 | $315.70 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | BAC | 45 | $48.69 | N/A | 70 |

<!--TRADE_LOG_END--> 
