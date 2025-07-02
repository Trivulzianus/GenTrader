# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 17:51:32**

| Metric | Value |
|---|---|
| **Total Value** | **$101,031.07** |
| Cash | $3,819.54 |
| Holdings Value | $97,211.53 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $211.30 | $2,113.00 | 70 |
| ADBE | 5 | $377.60 | $374.72 | $1,873.60 | 65 |
| AMD | 16 | $136.11 | $138.56 | $2,216.96 | 70 |
| AMZN | 10 | $221.48 | $219.91 | $2,199.10 | 70 |
| AVGO | 8 | $269.38 | $271.58 | $2,172.65 | 70 |
| AXP | 8 | $324.40 | $325.41 | $2,603.28 | 85 |
| BA | 10 | $212.15 | $211.67 | $2,116.69 | 70 |
| BAC | 49 | $48.69 | $48.45 | $2,374.05 | 75 |
| C | 26 | $86.80 | $86.39 | $2,246.14 | 70 |
| CAT | 6 | $396.45 | $396.60 | $2,379.57 | 70 |
| COST | 2 | $979.83 | $984.00 | $1,968.00 | 65 |
| CRM | 7 | $267.51 | $267.19 | $1,870.37 | 65 |
| CSCO | 32 | $68.36 | $68.59 | $2,194.73 | 70 |
| CVX | 15 | $146.48 | $146.92 | $2,203.80 | 70 |
| DIS | 17 | $122.83 | $122.64 | $2,084.97 | 65 |
| GOOGL | 14 | $177.86 | $178.46 | $2,498.37 | 85 |
| GS | 3 | $717.52 | $714.40 | $2,143.20 | 85 |
| HD | 5 | $372.57 | $372.58 | $1,862.90 | 65 |
| INTC | 92 | $22.33 | $21.89 | $2,013.67 | 65 |
| JNJ | 13 | $155.80 | $155.59 | $2,022.61 | 65 |
| JPM | 9 | $292.49 | $291.59 | $2,624.31 | 85 |
| KO | 29 | $71.03 | $70.92 | $2,056.54 | 65 |
| LLY | 2 | $776.66 | $777.60 | $1,555.20 | 65 |
| MA | 3 | $561.03 | $560.11 | $1,680.33 | 65 |
| META | 3 | $717.12 | $715.51 | $2,146.55 | 75 |
| MRK | 28 | $82.40 | $82.13 | $2,299.64 | 75 |
| MSFT | 4 | $491.43 | $489.98 | $1,959.92 | 70 |
| NFLX | 1 | $1,279.00 | $1,282.35 | $1,282.35 | 70 |
| NKE | 34 | $75.85 | $76.19 | $2,590.46 | 85 |
| NVDA | 14 | $156.21 | $157.27 | $2,201.78 | 70 |
| ORCL | 9 | $224.91 | $225.57 | $2,030.17 | 65 |
| PEP | 15 | $136.59 | $136.49 | $2,047.31 | 65 |
| PFE | 86 | $25.33 | $25.25 | $2,171.07 | 70 |
| PG | 12 | $160.76 | $160.75 | $1,929.00 | 65 |
| PYPL | 30 | $76.82 | $76.05 | $2,281.50 | 75 |
| QCOM | 15 | $161.52 | $161.91 | $2,428.72 | 80 |
| T | 71 | $28.50 | $28.43 | $2,018.88 | 65 |
| TGT | 20 | $105.06 | $104.76 | $2,095.20 | 65 |
| TSLA | 6 | $313.02 | $314.79 | $1,888.74 | 65 |
| UNH | 6 | $315.70 | $313.67 | $1,882.02 | 65 |
| UNP | 9 | $236.50 | $236.09 | $2,124.76 | 65 |
| V | 5 | $352.10 | $352.46 | $1,762.30 | 65 |
| VZ | 47 | $43.75 | $43.64 | $2,051.08 | 65 |
| WFC | 29 | $82.30 | $81.95 | $2,376.55 | 75 |
| WMT | 23 | $97.33 | $97.73 | $2,247.91 | 75 |
| XOM | 21 | $109.93 | $110.55 | $2,321.59 | 75 |

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
| 2025-07-02 17:51:22 | SELL | NVDA | 2 | $157.23 | $1.77 | 70 |
| 2025-07-02 17:51:22 | SELL | BAC | 5 | $48.47 | $-0.99 | 75 |
| 2025-07-02 17:51:22 | SELL | WFC | 3 | $81.96 | $-0.91 | 75 |
| 2025-07-02 17:51:22 | SELL | ORCL | 1 | $225.57 | $0.60 | 65 |
| 2025-07-02 17:51:22 | SELL | CVX | 1 | $146.91 | $0.40 | 70 |
| 2025-07-02 17:51:22 | BUY | GOOGL | 1 | $178.42 | N/A | 85 |
| 2025-07-02 17:51:22 | BUY | QCOM | 1 | $161.93 | N/A | 80 |
| 2025-07-02 17:39:14 | SELL | KO | 1 | $71.01 | $-0.01 | 65 |
| 2025-07-02 17:39:14 | SELL | CSCO | 2 | $68.53 | $0.33 | 70 |
| 2025-07-02 17:39:14 | BUY | BAC | 9 | $48.46 | N/A | 85 |
| 2025-07-02 17:39:14 | BUY | C | 1 | $86.39 | N/A | 75 |
| 2025-07-02 17:39:14 | BUY | WFC | 3 | $81.89 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
