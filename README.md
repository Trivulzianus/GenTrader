# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 16:55:33**

| Metric | Value |
|---|---|
| **Total Value** | **$101,828.11** |
| Cash | $1,464.77 |
| Holdings Value | $100,363.33 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.65 | $2,350.15 | 70 |
| ADBE | 5 | $377.60 | $379.71 | $1,898.57 | 65 |
| AMD | 15 | $135.93 | $137.90 | $2,068.50 | 70 |
| AMZN | 10 | $221.48 | $223.22 | $2,232.20 | 75 |
| AVGO | 8 | $269.90 | $275.05 | $2,200.40 | 75 |
| AXP | 8 | $324.40 | $327.86 | $2,622.88 | 85 |
| BA | 10 | $212.15 | $215.12 | $2,151.20 | 65 |
| BAC | 54 | $48.71 | $48.88 | $2,639.52 | 85 |
| C | 30 | $86.80 | $88.56 | $2,656.80 | 85 |
| CAT | 6 | $396.45 | $398.33 | $2,390.01 | 70 |
| COST | 2 | $979.83 | $985.99 | $1,971.98 | 65 |
| CRM | 8 | $268.33 | $272.27 | $2,178.16 | 65 |
| CSCO | 33 | $68.36 | $69.36 | $2,288.72 | 75 |
| CVX | 16 | $146.55 | $148.61 | $2,377.76 | 75 |
| DIS | 18 | $122.90 | $123.72 | $2,226.96 | 75 |
| GOOGL | 13 | $177.86 | $179.44 | $2,332.72 | 75 |
| GS | 3 | $717.52 | $722.48 | $2,167.44 | 85 |
| HD | 6 | $372.64 | $372.38 | $2,234.28 | 70 |
| INTC | 91 | $22.30 | $22.48 | $2,045.23 | 65 |
| JNJ | 13 | $155.80 | $156.12 | $2,029.50 | 65 |
| JPM | 9 | $292.50 | $295.48 | $2,659.34 | 85 |
| KO | 30 | $71.05 | $71.20 | $2,136.15 | 70 |
| LLY | 2 | $776.66 | $780.17 | $1,560.34 | 65 |
| MA | 3 | $561.03 | $567.41 | $1,702.22 | 70 |
| META | 3 | $717.12 | $719.07 | $2,157.21 | 85 |
| MRK | 27 | $82.45 | $80.99 | $2,186.73 | 75 |
| MSFT | 5 | $491.36 | $498.73 | $2,493.65 | 85 |
| NFLX | 1 | $1,279.00 | $1,294.95 | $1,294.95 | 70 |
| NKE | 28 | $75.74 | $76.47 | $2,141.16 | 70 |
| NVDA | 14 | $155.97 | $158.90 | $2,224.53 | 70 |
| ORCL | 10 | $226.06 | $236.52 | $2,365.20 | 75 |
| PEP | 15 | $136.59 | $135.38 | $2,030.62 | 65 |
| PFE | 79 | $25.30 | $25.43 | $2,008.58 | 65 |
| PG | 12 | $160.76 | $160.25 | $1,922.94 | 65 |
| PYPL | 30 | $76.81 | $76.50 | $2,294.85 | 75 |
| QCOM | 15 | $161.52 | $162.43 | $2,436.47 | 75 |
| T | 76 | $28.52 | $28.32 | $2,152.70 | 70 |
| TGT | 19 | $105.07 | $104.19 | $1,979.70 | 65 |
| TSLA | 6 | $313.02 | $316.08 | $1,896.45 | 60 |
| UNH | 7 | $314.75 | $309.14 | $2,163.98 | 65 |
| UNP | 9 | $236.50 | $237.17 | $2,134.53 | 70 |
| V | 6 | $352.90 | $358.11 | $2,148.66 | 65 |
| VZ | 46 | $43.73 | $43.55 | $2,003.30 | 65 |
| WFC | 31 | $82.32 | $83.39 | $2,585.09 | 85 |
| WMT | 23 | $97.38 | $98.36 | $2,262.39 | 75 |
| XOM | 21 | $109.97 | $112.31 | $2,358.61 | 75 |

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
| 2025-07-03 16:55:24 | SELL | PFE | 1 | $25.42 | $0.12 | 65 |
| 2025-07-03 16:55:24 | SELL | T | 1 | $28.34 | $-0.18 | 70 |
| 2025-07-03 16:55:24 | BUY | INTC | 7 | $21.88 | N/A | 65 |
| 2025-07-03 16:55:24 | BUY | WMT | 2 | $98.40 | N/A | 75 |
| 2025-07-03 16:55:24 | BUY | MRK | 2 | $82.39 | N/A | 75 |
| 2025-07-03 16:43:14 | SELL | INTC | 6 | $22.44 | $0.61 | 60 |
| 2025-07-03 16:43:14 | SELL | WMT | 2 | $98.26 | $1.79 | 65 |
| 2025-07-03 16:43:14 | SELL | QCOM | 1 | $162.53 | $0.95 | 75 |
| 2025-07-03 16:43:14 | SELL | ORCL | 1 | $237.29 | $10.21 | 75 |
| 2025-07-03 16:43:14 | BUY | GOOGL | 1 | $179.18 | N/A | 75 |
| 2025-07-03 16:43:14 | BUY | AAPL | 1 | $212.44 | N/A | 75 |
| 2025-07-03 16:43:14 | BUY | BAC | 7 | $49.03 | N/A | 85 |
| 2025-07-03 16:43:14 | BUY | KO | 1 | $71.35 | N/A | 70 |
| 2025-07-03 16:43:14 | BUY | PYPL | 1 | $76.84 | N/A | 75 |
| 2025-07-03 16:43:14 | BUY | NKE | 1 | $76.53 | N/A | 70 |
| 2025-07-03 16:43:14 | BUY | WFC | 2 | $83.61 | N/A | 85 |
| 2025-07-03 16:43:14 | BUY | CSCO | 3 | $69.32 | N/A | 75 |
| 2025-07-03 16:26:50 | SELL | KO | 1 | $71.25 | $0.20 | 65 |
| 2025-07-03 16:26:50 | SELL | NKE | 6 | $76.33 | $3.05 | 65 |
| 2025-07-03 16:26:50 | SELL | PYPL | 1 | $76.76 | $-0.04 | 70 |
| 2025-07-03 16:26:50 | SELL | CSCO | 2 | $69.36 | $2.06 | 65 |
| 2025-07-03 16:26:50 | SELL | PFE | 11 | $25.50 | $1.91 | 65 |
| 2025-07-03 16:26:50 | BUY | BAC | 2 | $48.98 | N/A | 75 |
| 2025-07-03 16:26:50 | BUY | INTC | 1 | $22.45 | N/A | 65 |
| 2025-07-03 16:26:50 | BUY | WMT | 2 | $98.07 | N/A | 75 |

<!--TRADE_LOG_END--> 
