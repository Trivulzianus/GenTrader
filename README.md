# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 18:44:38**

| Metric | Value |
|---|---|
| **Total Value** | **$101,116.32** |
| Cash | $3,520.98 |
| Holdings Value | $97,595.33 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $211.53 | $2,115.30 | 70 |
| ADBE | 5 | $377.60 | $376.65 | $1,883.27 | 65 |
| AMD | 16 | $136.11 | $138.65 | $2,218.40 | 70 |
| AMZN | 10 | $221.48 | $220.46 | $2,204.60 | 70 |
| AVGO | 8 | $269.38 | $269.72 | $2,157.74 | 70 |
| AXP | 8 | $324.40 | $325.81 | $2,606.48 | 85 |
| BA | 10 | $212.15 | $210.91 | $2,109.05 | 65 |
| BAC | 49 | $48.69 | $48.56 | $2,379.44 | 75 |
| C | 24 | $86.84 | $86.44 | $2,074.68 | 65 |
| CAT | 6 | $396.45 | $397.73 | $2,386.35 | 75 |
| COST | 2 | $979.83 | $982.66 | $1,965.32 | 65 |
| CRM | 7 | $267.51 | $267.38 | $1,871.62 | 65 |
| CSCO | 34 | $68.37 | $68.42 | $2,326.45 | 75 |
| CVX | 16 | $146.54 | $147.59 | $2,361.52 | 75 |
| DIS | 17 | $122.83 | $123.03 | $2,091.51 | 70 |
| GOOGL | 14 | $177.86 | $178.21 | $2,494.87 | 75 |
| GS | 3 | $717.52 | $712.66 | $2,137.98 | 75 |
| HD | 5 | $372.57 | $373.41 | $1,867.05 | 65 |
| INTC | 92 | $22.33 | $21.98 | $2,021.70 | 65 |
| JNJ | 13 | $155.80 | $155.91 | $2,026.89 | 65 |
| JPM | 9 | $292.49 | $291.12 | $2,620.12 | 85 |
| KO | 29 | $71.03 | $71.05 | $2,060.35 | 65 |
| LLY | 2 | $776.66 | $777.67 | $1,555.34 | 65 |
| MA | 3 | $561.03 | $559.47 | $1,678.41 | 65 |
| META | 3 | $717.12 | $714.20 | $2,142.60 | 75 |
| MRK | 28 | $82.40 | $82.29 | $2,304.12 | 75 |
| MSFT | 4 | $491.43 | $490.20 | $1,960.80 | 75 |
| NFLX | 1 | $1,279.00 | $1,277.67 | $1,277.67 | 65 |
| NKE | 31 | $75.79 | $76.61 | $2,374.91 | 75 |
| NVDA | 14 | $156.24 | $156.81 | $2,195.41 | 70 |
| ORCL | 9 | $224.91 | $224.76 | $2,022.84 | 70 |
| PEP | 15 | $136.59 | $136.90 | $2,053.47 | 65 |
| PFE | 86 | $25.33 | $25.28 | $2,174.08 | 70 |
| PG | 12 | $160.76 | $160.95 | $1,931.40 | 65 |
| PYPL | 30 | $76.82 | $76.13 | $2,283.90 | 75 |
| QCOM | 15 | $161.52 | $162.53 | $2,437.95 | 75 |
| T | 77 | $28.50 | $28.41 | $2,187.95 | 70 |
| TGT | 20 | $105.06 | $105.55 | $2,111.00 | 65 |
| TSLA | 6 | $313.02 | $316.00 | $1,896.00 | 65 |
| UNH | 6 | $315.70 | $311.14 | $1,866.84 | 65 |
| UNP | 9 | $236.50 | $237.04 | $2,133.36 | 65 |
| V | 5 | $352.10 | $352.84 | $1,764.20 | 65 |
| VZ | 47 | $43.74 | $43.73 | $2,055.31 | 65 |
| WFC | 32 | $82.28 | $82.05 | $2,625.44 | 85 |
| WMT | 23 | $97.33 | $97.76 | $2,248.48 | 70 |
| XOM | 21 | $109.93 | $111.10 | $2,333.15 | 75 |

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
| 2025-07-02 17:51:22 | SELL | CVX | 1 | $146.91 | $0.40 | 70 |
| 2025-07-02 17:51:22 | BUY | GOOGL | 1 | $178.42 | N/A | 85 |
| 2025-07-02 17:51:22 | BUY | QCOM | 1 | $161.93 | N/A | 80 |

<!--TRADE_LOG_END--> 
