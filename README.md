# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-04 06:46:24**

| Metric | Value |
|---|---|
| **Total Value** | **$101,869.82** |
| Cash | $2,123.70 |
| Holdings Value | $99,746.12 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.55 | $2,349.05 | 75 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 70 |
| AMZN | 10 | $221.48 | $223.41 | $2,234.10 | 75 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 70 |
| AXP | 8 | $324.40 | $328.13 | $2,625.04 | 85 |
| BA | 10 | $212.15 | $215.92 | $2,159.20 | 70 |
| BAC | 44 | $48.65 | $48.93 | $2,152.92 | 70 |
| C | 30 | $86.80 | $88.72 | $2,661.60 | 85 |
| CAT | 5 | $395.95 | $397.86 | $1,989.30 | 70 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.15 | $2,177.20 | 65 |
| CSCO | 31 | $68.29 | $69.37 | $2,150.47 | 70 |
| CVX | 16 | $146.52 | $148.37 | $2,373.92 | 75 |
| DIS | 17 | $122.82 | $124.00 | $2,108.00 | 70 |
| GOOGL | 12 | $179.53 | $179.53 | $2,154.36 | 75 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 70 |
| HD | 6 | $372.64 | $371.68 | $2,230.08 | 70 |
| INTC | 82 | $22.28 | $22.49 | $1,844.18 | 60 |
| JNJ | 13 | $155.80 | $156.01 | $2,028.13 | 65 |
| JPM | 9 | $292.50 | $296.00 | $2,664.00 | 85 |
| KO | 30 | $71.05 | $71.35 | $2,140.50 | 70 |
| LLY | 2 | $776.66 | $780.67 | $1,561.34 | 70 |
| MA | 4 | $563.08 | $569.24 | $2,276.96 | 70 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 85 |
| MRK | 25 | $82.57 | $80.93 | $2,023.25 | 65 |
| MSFT | 5 | $491.36 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 65 |
| NKE | 28 | $75.77 | $76.39 | $2,138.92 | 70 |
| NVDA | 16 | $156.39 | $159.34 | $2,549.44 | 85 |
| ORCL | 11 | $227.11 | $237.32 | $2,610.52 | 85 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 79 | $25.31 | $25.38 | $2,005.02 | 65 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 60 |
| PYPL | 31 | $76.80 | $76.59 | $2,374.29 | 75 |
| QCOM | 15 | $161.52 | $162.21 | $2,433.15 | 80 |
| T | 81 | $28.51 | $28.36 | $2,297.16 | 75 |
| TGT | 19 | $105.09 | $104.06 | $1,977.14 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 65 |
| UNH | 7 | $314.75 | $308.55 | $2,159.85 | 70 |
| UNP | 9 | $236.50 | $236.28 | $2,126.52 | 75 |
| V | 6 | $352.90 | $358.86 | $2,153.16 | 70 |
| VZ | 46 | $43.73 | $43.55 | $2,003.30 | 65 |
| WFC | 31 | $82.32 | $83.60 | $2,591.60 | 85 |
| WMT | 21 | $97.28 | $98.36 | $2,065.56 | 70 |
| XOM | 20 | $109.86 | $112.20 | $2,244.00 | 75 |

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
| 2025-07-04 06:46:19 | SELL | INTC | 6 | $22.49 | $1.17 | 60 |
| 2025-07-04 06:28:19 | SELL | PFE | 5 | $25.38 | $0.34 | 65 |
| 2025-07-04 06:28:19 | SELL | CVX | 1 | $148.37 | $1.74 | 75 |
| 2025-07-04 06:28:19 | BUY | INTC | 6 | $22.49 | N/A | 65 |
| 2025-07-04 06:28:19 | BUY | KO | 2 | $71.35 | N/A | 70 |
| 2025-07-04 06:28:19 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-04 06:11:47 | SELL | BAC | 3 | $48.93 | $0.77 | 70 |
| 2025-07-04 06:11:47 | SELL | KO | 2 | $71.35 | $0.59 | 65 |
| 2025-07-04 06:11:47 | SELL | WFC | 1 | $83.60 | $1.28 | 80 |
| 2025-07-04 06:11:47 | SELL | CSCO | 2 | $69.37 | $2.02 | 70 |
| 2025-07-04 06:11:47 | BUY | PFE | 5 | $25.38 | N/A | 70 |
| 2025-07-04 06:11:47 | BUY | QCOM | 1 | $162.21 | N/A | 80 |
| 2025-07-04 05:52:18 | SELL | AMZN | 1 | $223.41 | $1.75 | 70 |
| 2025-07-04 05:52:18 | SELL | QCOM | 2 | $162.21 | $1.29 | 70 |
| 2025-07-04 05:52:18 | BUY | BAC | 4 | $48.93 | N/A | 75 |
| 2025-07-04 05:52:18 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-04 05:52:18 | BUY | CSCO | 2 | $69.37 | N/A | 75 |
| 2025-07-04 05:41:21 | SELL | WFC | 1 | $83.60 | $1.28 | 80 |
| 2025-07-04 05:41:21 | BUY | BAC | 2 | $48.93 | N/A | 70 |
| 2025-07-04 05:41:21 | BUY | QCOM | 2 | $162.21 | N/A | 85 |
| 2025-07-04 05:26:24 | SELL | BAC | 3 | $48.93 | $0.83 | 65 |
| 2025-07-04 05:26:24 | SELL | PYPL | 1 | $76.59 | $-0.20 | 75 |
| 2025-07-04 05:26:24 | BUY | ORCL | 1 | $237.32 | N/A | 85 |
| 2025-07-04 05:11:18 | SELL | INTC | 7 | $22.49 | $1.35 | 60 |
| 2025-07-04 05:11:18 | SELL | PFE | 5 | $25.38 | $0.34 | 65 |

<!--TRADE_LOG_END--> 
