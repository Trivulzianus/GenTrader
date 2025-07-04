# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-04 13:43:03**

| Metric | Value |
|---|---|
| **Total Value** | **$101,869.82** |
| Cash | $1,938.49 |
| Holdings Value | $99,931.33 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.55 | $2,349.05 | 75 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 70 |
| AMZN | 11 | $221.66 | $223.41 | $2,457.51 | 75 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 70 |
| AXP | 8 | $324.40 | $328.13 | $2,625.04 | 85 |
| BA | 10 | $212.15 | $215.92 | $2,159.20 | 70 |
| BAC | 45 | $48.66 | $48.93 | $2,201.85 | 70 |
| C | 27 | $86.59 | $88.72 | $2,395.44 | 75 |
| CAT | 5 | $395.95 | $397.86 | $1,989.30 | 70 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.15 | $2,177.20 | 65 |
| CSCO | 33 | $68.36 | $69.37 | $2,289.21 | 75 |
| CVX | 16 | $146.52 | $148.37 | $2,373.92 | 75 |
| DIS | 21 | $123.05 | $124.00 | $2,604.00 | 85 |
| GOOGL | 12 | $179.53 | $179.53 | $2,154.36 | 75 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 85 |
| HD | 6 | $372.64 | $371.68 | $2,230.08 | 65 |
| INTC | 82 | $22.28 | $22.49 | $1,844.18 | 60 |
| JNJ | 13 | $155.80 | $156.01 | $2,028.13 | 65 |
| JPM | 9 | $292.50 | $296.00 | $2,664.00 | 85 |
| KO | 30 | $71.05 | $71.35 | $2,140.50 | 70 |
| LLY | 2 | $776.66 | $780.67 | $1,561.34 | 65 |
| MA | 4 | $563.08 | $569.24 | $2,276.96 | 70 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 85 |
| MRK | 25 | $82.57 | $80.93 | $2,023.25 | 65 |
| MSFT | 5 | $491.36 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 70 |
| NKE | 28 | $75.77 | $76.39 | $2,138.92 | 70 |
| NVDA | 16 | $156.39 | $159.34 | $2,549.44 | 85 |
| ORCL | 10 | $226.09 | $237.32 | $2,373.20 | 75 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 79 | $25.31 | $25.38 | $2,005.02 | 65 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 15 | $161.52 | $162.21 | $2,433.15 | 75 |
| T | 76 | $28.52 | $28.36 | $2,155.36 | 70 |
| TGT | 19 | $105.09 | $104.06 | $1,977.14 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 65 |
| UNH | 7 | $314.75 | $308.55 | $2,159.85 | 65 |
| UNP | 9 | $236.50 | $236.28 | $2,126.52 | 75 |
| V | 6 | $352.90 | $358.86 | $2,153.16 | 65 |
| VZ | 46 | $43.73 | $43.55 | $2,003.30 | 65 |
| WFC | 31 | $82.32 | $83.60 | $2,591.60 | 85 |
| WMT | 21 | $97.28 | $98.36 | $2,065.56 | 65 |
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
| 2025-07-04 13:42:57 | SELL | BAC | 2 | $48.93 | $0.52 | 70 |
| 2025-07-04 13:42:57 | SELL | WMT | 1 | $98.36 | $1.03 | 65 |
| 2025-07-04 13:42:57 | SELL | PFE | 4 | $25.38 | $0.28 | 65 |
| 2025-07-04 13:42:57 | SELL | C | 2 | $88.72 | $3.96 | 75 |
| 2025-07-04 13:42:57 | SELL | ORCL | 1 | $237.32 | $10.21 | 75 |
| 2025-07-04 13:42:57 | SELL | CVX | 1 | $148.37 | $1.74 | 75 |
| 2025-07-04 13:42:57 | BUY | INTC | 1 | $22.49 | N/A | 60 |
| 2025-07-04 13:42:57 | BUY | KO | 1 | $71.35 | N/A | 70 |
| 2025-07-04 13:42:57 | BUY | DIS | 2 | $124.00 | N/A | 85 |
| 2025-07-04 13:42:57 | BUY | NKE | 1 | $76.39 | N/A | 70 |
| 2025-07-04 13:42:57 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-04 13:42:57 | BUY | CSCO | 2 | $69.37 | N/A | 75 |
| 2025-07-04 13:42:57 | BUY | T | 2 | $28.36 | N/A | 70 |
| 2025-07-04 13:16:48 | SELL | BAC | 5 | $48.93 | $1.17 | 75 |
| 2025-07-04 13:16:48 | BUY | KO | 1 | $71.35 | N/A | 70 |
| 2025-07-04 13:16:48 | BUY | DIS | 2 | $124.00 | N/A | 80 |
| 2025-07-04 13:16:48 | BUY | PFE | 5 | $25.38 | N/A | 70 |
| 2025-07-04 13:16:48 | BUY | T | 4 | $28.36 | N/A | 70 |
| 2025-07-04 12:55:21 | SELL | INTC | 1 | $22.49 | $0.21 | 60 |
| 2025-07-04 12:55:21 | SELL | KO | 2 | $71.35 | $0.59 | 65 |
| 2025-07-04 12:55:21 | SELL | PFE | 1 | $25.38 | $0.07 | 65 |
| 2025-07-04 12:55:21 | SELL | WFC | 1 | $83.60 | $1.28 | 80 |
| 2025-07-04 12:55:21 | SELL | T | 1 | $28.36 | $-0.17 | 65 |
| 2025-07-04 12:55:21 | BUY | BAC | 8 | $48.93 | N/A | 85 |
| 2025-07-04 12:55:21 | BUY | QCOM | 1 | $162.21 | N/A | 85 |

<!--TRADE_LOG_END--> 
