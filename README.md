# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-04 12:55:26**

| Metric | Value |
|---|---|
| **Total Value** | **$101,869.82** |
| Cash | $2,089.95 |
| Holdings Value | $99,779.87 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.55 | $2,349.05 | 75 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 70 |
| AMZN | 11 | $221.66 | $223.41 | $2,457.51 | 75 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 70 |
| AXP | 8 | $324.40 | $328.13 | $2,625.04 | 85 |
| BA | 10 | $212.15 | $215.92 | $2,159.20 | 75 |
| BAC | 52 | $48.70 | $48.93 | $2,544.36 | 85 |
| C | 29 | $86.74 | $88.72 | $2,572.88 | 85 |
| CAT | 5 | $395.95 | $397.86 | $1,989.30 | 70 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.15 | $2,177.20 | 65 |
| CSCO | 31 | $68.29 | $69.37 | $2,150.47 | 70 |
| CVX | 17 | $146.63 | $148.37 | $2,522.29 | 85 |
| DIS | 17 | $122.82 | $124.00 | $2,108.00 | 70 |
| GOOGL | 12 | $179.53 | $179.53 | $2,154.36 | 75 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 85 |
| HD | 6 | $372.64 | $371.68 | $2,230.08 | 75 |
| INTC | 81 | $22.28 | $22.49 | $1,821.69 | 60 |
| JNJ | 13 | $155.80 | $156.01 | $2,028.13 | 65 |
| JPM | 9 | $292.50 | $296.00 | $2,664.00 | 85 |
| KO | 28 | $71.03 | $71.35 | $1,997.80 | 65 |
| LLY | 2 | $776.66 | $780.67 | $1,561.34 | 70 |
| MA | 4 | $563.08 | $569.24 | $2,276.96 | 70 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 85 |
| MRK | 25 | $82.57 | $80.93 | $2,023.25 | 65 |
| MSFT | 5 | $491.36 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 70 |
| NKE | 27 | $75.75 | $76.39 | $2,062.53 | 70 |
| NVDA | 16 | $156.39 | $159.34 | $2,549.44 | 85 |
| ORCL | 11 | $227.11 | $237.32 | $2,610.52 | 85 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 78 | $25.31 | $25.38 | $1,979.64 | 65 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 15 | $161.52 | $162.21 | $2,433.15 | 85 |
| T | 70 | $28.54 | $28.36 | $1,985.20 | 65 |
| TGT | 19 | $105.09 | $104.06 | $1,977.14 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 65 |
| UNH | 7 | $314.75 | $308.55 | $2,159.85 | 65 |
| UNP | 9 | $236.50 | $236.28 | $2,126.52 | 75 |
| V | 6 | $352.90 | $358.86 | $2,153.16 | 75 |
| VZ | 46 | $43.73 | $43.55 | $2,003.30 | 65 |
| WFC | 30 | $82.28 | $83.60 | $2,508.00 | 80 |
| WMT | 22 | $97.33 | $98.36 | $2,163.92 | 70 |
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
| 2025-07-04 12:55:21 | SELL | INTC | 1 | $22.49 | $0.21 | 60 |
| 2025-07-04 12:55:21 | SELL | KO | 2 | $71.35 | $0.59 | 65 |
| 2025-07-04 12:55:21 | SELL | PFE | 1 | $25.38 | $0.07 | 65 |
| 2025-07-04 12:55:21 | SELL | WFC | 1 | $83.60 | $1.28 | 80 |
| 2025-07-04 12:55:21 | SELL | T | 1 | $28.36 | $-0.17 | 65 |
| 2025-07-04 12:55:21 | BUY | BAC | 8 | $48.93 | N/A | 85 |
| 2025-07-04 12:55:21 | BUY | QCOM | 1 | $162.21 | N/A | 85 |
| 2025-07-04 12:55:21 | BUY | CVX | 1 | $148.37 | N/A | 85 |
| 2025-07-04 12:31:15 | SELL | PFE | 5 | $25.38 | $0.34 | 65 |
| 2025-07-04 12:31:15 | BUY | ORCL | 1 | $237.32 | N/A | 85 |
| 2025-07-04 12:13:29 | SELL | NKE | 1 | $76.39 | $0.62 | 65 |
| 2025-07-04 12:13:29 | SELL | ORCL | 1 | $237.32 | $10.21 | 75 |
| 2025-07-04 12:13:29 | BUY | PFE | 4 | $25.38 | N/A | 70 |
| 2025-07-04 11:49:54 | SELL | PFE | 4 | $25.38 | $0.27 | 65 |
| 2025-07-04 11:49:54 | BUY | KO | 2 | $71.35 | N/A | 70 |
| 2025-07-04 11:49:54 | BUY | INTC | 1 | $22.49 | N/A | 60 |
| 2025-07-04 11:49:54 | BUY | WMT | 1 | $98.36 | N/A | 70 |
| 2025-07-04 11:36:23 | SELL | KO | 2 | $71.35 | $0.59 | 65 |
| 2025-07-04 11:36:23 | SELL | CSCO | 2 | $69.37 | $2.02 | 70 |
| 2025-07-04 11:36:23 | SELL | T | 5 | $28.36 | $-0.81 | 65 |
| 2025-07-04 11:36:23 | BUY | INTC | 5 | $22.49 | N/A | 60 |
| 2025-07-04 11:36:23 | BUY | NKE | 1 | $76.39 | N/A | 70 |
| 2025-07-04 11:36:23 | BUY | PFE | 5 | $25.38 | N/A | 70 |
| 2025-07-04 11:24:47 | SELL | INTC | 6 | $22.49 | $1.26 | 55 |
| 2025-07-04 11:24:47 | SELL | NKE | 1 | $76.39 | $0.62 | 65 |

<!--TRADE_LOG_END--> 
