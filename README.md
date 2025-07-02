# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 17:25:57**

| Metric | Value |
|---|---|
| **Total Value** | **$101,015.79** |
| Cash | $3,544.79 |
| Holdings Value | $97,470.99 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $210.80 | $2,108.00 | 70 |
| ADBE | 5 | $377.60 | $373.55 | $1,867.73 | 65 |
| AMD | 16 | $136.11 | $138.84 | $2,221.44 | 70 |
| AMZN | 10 | $221.48 | $220.53 | $2,205.30 | 70 |
| AVGO | 8 | $269.38 | $270.82 | $2,166.56 | 70 |
| AXP | 8 | $324.40 | $324.90 | $2,599.20 | 80 |
| BA | 10 | $212.15 | $212.05 | $2,120.50 | 70 |
| BAC | 45 | $48.72 | $48.44 | $2,179.58 | 70 |
| C | 25 | $86.81 | $86.55 | $2,163.62 | 70 |
| CAT | 6 | $396.45 | $396.06 | $2,376.36 | 75 |
| COST | 2 | $979.83 | $983.86 | $1,967.72 | 65 |
| CRM | 7 | $267.51 | $267.07 | $1,869.49 | 65 |
| CSCO | 34 | $68.37 | $68.53 | $2,330.02 | 75 |
| CVX | 16 | $146.51 | $146.65 | $2,346.43 | 75 |
| DIS | 17 | $122.83 | $122.68 | $2,085.63 | 70 |
| GOOGL | 13 | $177.82 | $178.75 | $2,323.75 | 75 |
| GS | 3 | $717.52 | $714.97 | $2,144.89 | 70 |
| HD | 5 | $372.57 | $372.23 | $1,861.12 | 65 |
| INTC | 92 | $22.33 | $21.91 | $2,015.26 | 65 |
| JNJ | 13 | $155.80 | $155.71 | $2,024.22 | 65 |
| JPM | 9 | $292.49 | $291.70 | $2,625.30 | 85 |
| KO | 30 | $71.03 | $71.03 | $2,130.75 | 70 |
| LLY | 2 | $776.66 | $777.29 | $1,554.59 | 70 |
| MA | 3 | $561.03 | $559.89 | $1,679.67 | 65 |
| META | 3 | $717.12 | $716.39 | $2,149.17 | 75 |
| MRK | 28 | $82.40 | $82.10 | $2,298.80 | 75 |
| MSFT | 4 | $491.43 | $490.33 | $1,961.32 | 70 |
| NFLX | 1 | $1,279.00 | $1,273.44 | $1,273.44 | 65 |
| NKE | 34 | $75.85 | $76.13 | $2,588.48 | 85 |
| NVDA | 16 | $156.34 | $157.24 | $2,515.84 | 85 |
| ORCL | 10 | $224.98 | $225.82 | $2,258.24 | 70 |
| PEP | 15 | $136.59 | $136.61 | $2,049.15 | 65 |
| PFE | 86 | $25.33 | $25.27 | $2,173.65 | 70 |
| PG | 12 | $160.76 | $160.92 | $1,931.04 | 65 |
| PYPL | 30 | $76.82 | $76.11 | $2,283.45 | 75 |
| QCOM | 14 | $161.49 | $161.68 | $2,263.52 | 75 |
| T | 71 | $28.50 | $28.45 | $2,019.95 | 65 |
| TGT | 20 | $105.06 | $104.42 | $2,088.40 | 65 |
| TSLA | 6 | $313.02 | $315.45 | $1,892.70 | 65 |
| UNH | 6 | $315.70 | $313.10 | $1,878.57 | 65 |
| UNP | 9 | $236.50 | $235.92 | $2,123.28 | 65 |
| V | 5 | $352.10 | $352.27 | $1,761.35 | 65 |
| VZ | 47 | $43.75 | $43.66 | $2,051.78 | 65 |
| WFC | 29 | $82.31 | $82.00 | $2,377.86 | 75 |
| WMT | 23 | $97.33 | $97.71 | $2,247.33 | 75 |
| XOM | 21 | $109.93 | $110.31 | $2,316.53 | 75 |

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
| 2025-07-02 17:25:50 | SELL | BAC | 9 | $48.44 | $-2.07 | 70 |
| 2025-07-02 17:25:50 | SELL | WFC | 3 | $82.00 | $-0.83 | 75 |
| 2025-07-02 17:25:50 | BUY | NVDA | 1 | $157.29 | N/A | 85 |
| 2025-07-02 17:25:50 | BUY | INTC | 7 | $21.91 | N/A | 65 |
| 2025-07-02 17:25:50 | BUY | KO | 2 | $71.03 | N/A | 70 |
| 2025-07-02 17:25:50 | BUY | XOM | 1 | $110.32 | N/A | 75 |
| 2025-07-02 17:25:50 | BUY | WMT | 2 | $97.74 | N/A | 75 |
| 2025-07-02 17:25:50 | BUY | C | 1 | $86.56 | N/A | 70 |
| 2025-07-02 17:08:18 | SELL | INTC | 7 | $22.10 | $-1.65 | 60 |
| 2025-07-02 17:08:18 | SELL | WMT | 2 | $97.50 | $0.36 | 65 |
| 2025-07-02 17:08:18 | SELL | C | 6 | $86.64 | $-0.86 | 65 |
| 2025-07-02 17:08:18 | SELL | VZ | 2 | $43.60 | $-0.29 | 65 |
| 2025-07-02 17:08:18 | BUY | NVDA | 1 | $153.30 | N/A | 75 |
| 2025-07-02 17:08:18 | BUY | NKE | 2 | $76.04 | N/A | 85 |
| 2025-07-02 17:08:18 | BUY | PFE | 5 | $25.22 | N/A | 70 |
| 2025-07-02 17:08:18 | BUY | MRK | 3 | $81.81 | N/A | 75 |
| 2025-07-02 16:55:51 | SELL | NVDA | 2 | $157.33 | $1.47 | 70 |
| 2025-07-02 16:55:51 | SELL | MRK | 3 | $82.13 | $-0.91 | 65 |
| 2025-07-02 16:55:51 | SELL | T | 1 | $28.52 | $0.02 | 65 |
| 2025-07-02 16:55:51 | SELL | CVX | 1 | $146.48 | $-0.03 | 75 |
| 2025-07-02 16:55:51 | BUY | WMT | 2 | $97.59 | N/A | 75 |
| 2025-07-02 16:55:51 | BUY | NKE | 1 | $76.05 | N/A | 80 |
| 2025-07-02 16:55:51 | BUY | C | 4 | $86.75 | N/A | 85 |
| 2025-07-02 16:55:51 | BUY | BA | 1 | $212.72 | N/A | 70 |
| 2025-07-02 16:55:51 | BUY | CAT | 1 | $395.95 | N/A | 85 |

<!--TRADE_LOG_END--> 
