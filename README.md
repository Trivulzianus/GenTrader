# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 18:27:33**

| Metric | Value |
|---|---|
| **Total Value** | **$101,074.64** |
| Cash | $3,040.75 |
| Holdings Value | $98,033.89 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $211.68 | $2,116.80 | 65 |
| ADBE | 5 | $377.60 | $375.75 | $1,878.72 | 65 |
| AMD | 16 | $136.11 | $138.57 | $2,217.12 | 70 |
| AMZN | 10 | $221.48 | $220.32 | $2,203.20 | 70 |
| AVGO | 8 | $269.38 | $270.67 | $2,165.38 | 75 |
| AXP | 8 | $324.40 | $325.71 | $2,605.68 | 85 |
| BA | 10 | $212.15 | $211.21 | $2,112.10 | 70 |
| BAC | 54 | $48.67 | $48.50 | $2,619.00 | 85 |
| C | 24 | $86.84 | $86.36 | $2,072.76 | 65 |
| CAT | 6 | $396.45 | $397.41 | $2,384.46 | 70 |
| COST | 2 | $979.83 | $982.39 | $1,964.79 | 65 |
| CRM | 7 | $267.51 | $267.43 | $1,871.98 | 65 |
| CSCO | 34 | $68.37 | $68.47 | $2,328.15 | 75 |
| CVX | 16 | $146.54 | $147.48 | $2,359.68 | 80 |
| DIS | 17 | $122.83 | $122.81 | $2,087.77 | 70 |
| GOOGL | 14 | $177.86 | $178.09 | $2,493.26 | 75 |
| GS | 3 | $717.52 | $712.49 | $2,137.47 | 70 |
| HD | 5 | $372.57 | $373.02 | $1,865.12 | 70 |
| INTC | 92 | $22.33 | $21.93 | $2,017.10 | 65 |
| JNJ | 13 | $155.80 | $155.82 | $2,025.66 | 65 |
| JPM | 9 | $292.49 | $290.93 | $2,618.37 | 85 |
| KO | 29 | $71.03 | $70.94 | $2,057.12 | 65 |
| LLY | 2 | $776.66 | $777.38 | $1,554.76 | 65 |
| MA | 3 | $561.03 | $558.72 | $1,676.16 | 65 |
| META | 3 | $717.12 | $715.77 | $2,147.31 | 70 |
| MRK | 28 | $82.40 | $82.27 | $2,303.56 | 75 |
| MSFT | 4 | $491.43 | $490.20 | $1,960.80 | 70 |
| NFLX | 1 | $1,279.00 | $1,279.17 | $1,279.17 | 65 |
| NKE | 34 | $75.86 | $76.43 | $2,598.62 | 85 |
| NVDA | 16 | $156.31 | $156.90 | $2,510.43 | 85 |
| ORCL | 9 | $224.91 | $223.60 | $2,012.44 | 65 |
| PEP | 15 | $136.59 | $136.84 | $2,052.53 | 65 |
| PFE | 80 | $25.33 | $25.32 | $2,026.00 | 65 |
| PG | 12 | $160.76 | $160.88 | $1,930.56 | 65 |
| PYPL | 30 | $76.82 | $76.14 | $2,284.20 | 75 |
| QCOM | 15 | $161.52 | $162.22 | $2,433.30 | 75 |
| T | 71 | $28.50 | $28.41 | $2,017.11 | 65 |
| TGT | 20 | $105.06 | $105.39 | $2,107.80 | 65 |
| TSLA | 6 | $313.02 | $316.07 | $1,896.42 | 65 |
| UNH | 6 | $315.70 | $312.80 | $1,876.80 | 65 |
| UNP | 9 | $236.50 | $236.57 | $2,129.13 | 70 |
| V | 5 | $352.10 | $352.39 | $1,761.95 | 65 |
| VZ | 53 | $43.74 | $43.71 | $2,316.53 | 75 |
| WFC | 29 | $82.30 | $81.97 | $2,377.27 | 75 |
| WMT | 23 | $97.33 | $97.75 | $2,248.14 | 75 |
| XOM | 21 | $109.93 | $111.01 | $2,331.21 | 75 |

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

<!--TRADE_LOG_END--> 
