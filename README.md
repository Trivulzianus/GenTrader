# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 18:56:23**

| Metric | Value |
|---|---|
| **Total Value** | **$101,111.55** |
| Cash | $3,358.82 |
| Holdings Value | $97,752.72 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.17 | $2,121.72 | 70 |
| ADBE | 5 | $377.60 | $376.52 | $1,882.62 | 65 |
| AMD | 15 | $135.93 | $138.77 | $2,081.55 | 65 |
| AMZN | 10 | $221.48 | $220.24 | $2,202.41 | 70 |
| AVGO | 8 | $269.38 | $269.55 | $2,156.40 | 75 |
| AXP | 8 | $324.40 | $325.97 | $2,607.76 | 85 |
| BA | 10 | $212.15 | $210.92 | $2,109.20 | 65 |
| BAC | 49 | $48.69 | $48.59 | $2,380.66 | 75 |
| C | 24 | $86.84 | $86.44 | $2,074.68 | 65 |
| CAT | 6 | $396.45 | $397.60 | $2,385.60 | 70 |
| COST | 2 | $979.83 | $981.31 | $1,962.62 | 65 |
| CRM | 7 | $267.51 | $268.00 | $1,876.00 | 65 |
| CSCO | 34 | $68.37 | $68.44 | $2,327.13 | 75 |
| CVX | 17 | $146.61 | $147.58 | $2,508.86 | 85 |
| DIS | 17 | $122.83 | $123.01 | $2,091.17 | 70 |
| GOOGL | 14 | $177.86 | $178.40 | $2,497.60 | 85 |
| GS | 3 | $717.52 | $712.13 | $2,136.40 | 70 |
| HD | 5 | $372.57 | $373.53 | $1,867.65 | 65 |
| INTC | 92 | $22.33 | $21.97 | $2,021.23 | 65 |
| JNJ | 13 | $155.80 | $155.79 | $2,025.33 | 65 |
| JPM | 9 | $292.49 | $291.10 | $2,619.90 | 85 |
| KO | 29 | $71.03 | $71.01 | $2,059.29 | 65 |
| LLY | 2 | $776.66 | $777.28 | $1,554.56 | 65 |
| MA | 3 | $561.03 | $559.70 | $1,679.10 | 65 |
| META | 3 | $717.12 | $714.61 | $2,143.83 | 70 |
| MRK | 28 | $82.40 | $82.24 | $2,302.72 | 75 |
| MSFT | 4 | $491.43 | $490.10 | $1,960.42 | 70 |
| NFLX | 1 | $1,279.00 | $1,279.80 | $1,279.80 | 65 |
| NKE | 31 | $75.79 | $76.52 | $2,371.97 | 75 |
| NVDA | 15 | $156.05 | $156.76 | $2,351.42 | 75 |
| ORCL | 9 | $224.91 | $225.68 | $2,031.12 | 65 |
| PEP | 15 | $136.59 | $136.49 | $2,047.28 | 65 |
| PFE | 86 | $25.33 | $25.30 | $2,175.37 | 70 |
| PG | 12 | $160.76 | $160.91 | $1,930.92 | 65 |
| PYPL | 30 | $76.82 | $76.18 | $2,285.40 | 75 |
| QCOM | 15 | $161.52 | $162.46 | $2,436.94 | 75 |
| T | 77 | $28.50 | $28.41 | $2,187.95 | 70 |
| TGT | 20 | $105.06 | $105.41 | $2,108.20 | 65 |
| TSLA | 6 | $313.02 | $315.31 | $1,891.89 | 65 |
| UNH | 6 | $315.70 | $310.58 | $1,863.48 | 65 |
| UNP | 9 | $236.50 | $237.06 | $2,133.59 | 65 |
| V | 5 | $352.10 | $352.78 | $1,763.90 | 65 |
| VZ | 47 | $43.74 | $43.69 | $2,053.43 | 65 |
| WFC | 32 | $82.28 | $82.06 | $2,625.76 | 85 |
| WMT | 23 | $97.33 | $97.64 | $2,245.84 | 75 |
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
| 2025-07-02 18:56:13 | SELL | AMD | 1 | $138.74 | $2.63 | 65 |
| 2025-07-02 18:56:13 | BUY | NVDA | 1 | $153.30 | N/A | 75 |
| 2025-07-02 18:56:13 | BUY | CVX | 1 | $147.60 | N/A | 85 |
| 2025-07-02 18:44:32 | SELL | NVDA | 2 | $156.80 | $0.97 | 70 |
| 2025-07-02 18:44:32 | SELL | BAC | 5 | $48.55 | $-0.62 | 75 |
| 2025-07-02 18:44:32 | SELL | NKE | 3 | $76.62 | $2.27 | 75 |
| 2025-07-02 18:44:32 | SELL | VZ | 6 | $43.73 | $-0.08 | 65 |
| 2025-07-02 18:44:32 | BUY | PFE | 6 | $25.29 | N/A | 70 |
| 2025-07-02 18:44:32 | BUY | WFC | 3 | $82.04 | N/A | 85 |
| 2025-07-02 18:44:32 | BUY | T | 6 | $28.41 | N/A | 70 |
| 2025-07-02 18:27:27 | SELL | PFE | 6 | $25.32 | $-0.02 | 65 |
| 2025-07-02 18:27:27 | BUY | INTC | 6 | $21.93 | N/A | 65 |
| 2025-07-02 18:27:27 | BUY | NKE | 5 | $76.44 | N/A | 85 |
| 2025-07-02 18:27:27 | BUY | VZ | 6 | $43.68 | N/A | 75 |
| 2025-07-02 18:27:27 | BUY | CSCO | 2 | $68.47 | N/A | 75 |
| 2025-07-02 18:27:27 | BUY | CVX | 1 | $147.50 | N/A | 80 |
| 2025-07-02 18:11:25 | SELL | INTC | 6 | $21.93 | $-2.37 | 60 |
| 2025-07-02 18:11:25 | SELL | NKE | 5 | $76.38 | $2.60 | 70 |
| 2025-07-02 18:11:25 | SELL | C | 2 | $86.29 | $-1.00 | 65 |
| 2025-07-02 18:11:25 | BUY | NVDA | 2 | $157.03 | N/A | 85 |
| 2025-07-02 18:11:25 | BUY | BAC | 5 | $48.49 | N/A | 85 |
| 2025-07-02 17:51:22 | SELL | NVDA | 2 | $157.23 | $1.77 | 70 |
| 2025-07-02 17:51:22 | SELL | BAC | 5 | $48.47 | $-0.99 | 75 |
| 2025-07-02 17:51:22 | SELL | WFC | 3 | $81.96 | $-0.91 | 75 |
| 2025-07-02 17:51:22 | SELL | ORCL | 1 | $225.57 | $0.60 | 65 |

<!--TRADE_LOG_END--> 
