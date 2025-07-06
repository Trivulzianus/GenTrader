# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-06 16:26:41**

| Metric | Value |
|---|---|
| **Total Value** | **$101,869.82** |
| Cash | $2,340.44 |
| Holdings Value | $99,529.38 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $213.55 | $2,135.50 | 75 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 70 |
| AMZN | 11 | $221.66 | $223.41 | $2,457.51 | 80 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 70 |
| AXP | 7 | $323.87 | $328.13 | $2,296.91 | 75 |
| BA | 10 | $212.15 | $215.92 | $2,159.20 | 70 |
| BAC | 53 | $48.70 | $48.93 | $2,593.29 | 85 |
| C | 26 | $86.51 | $88.72 | $2,306.72 | 75 |
| CAT | 5 | $397.86 | $397.86 | $1,989.30 | 70 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.15 | $2,177.20 | 65 |
| CSCO | 31 | $68.29 | $69.37 | $2,150.47 | 70 |
| CVX | 16 | $146.52 | $148.37 | $2,373.92 | 75 |
| DIS | 18 | $122.89 | $124.00 | $2,232.00 | 70 |
| GOOGL | 12 | $179.53 | $179.53 | $2,154.36 | 75 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 85 |
| HD | 6 | $372.64 | $371.68 | $2,230.08 | 65 |
| INTC | 88 | $22.30 | $22.49 | $1,979.12 | 65 |
| JNJ | 13 | $155.80 | $156.01 | $2,028.13 | 70 |
| JPM | 9 | $292.50 | $296.00 | $2,664.00 | 85 |
| KO | 28 | $71.03 | $71.35 | $1,997.80 | 65 |
| LLY | 2 | $776.66 | $780.67 | $1,561.34 | 65 |
| MA | 4 | $563.08 | $569.24 | $2,276.96 | 65 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 85 |
| MRK | 24 | $82.64 | $80.93 | $1,942.32 | 65 |
| MSFT | 5 | $498.84 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 70 |
| NKE | 27 | $75.75 | $76.39 | $2,062.53 | 65 |
| NVDA | 16 | $156.39 | $159.34 | $2,549.44 | 85 |
| ORCL | 11 | $227.11 | $237.32 | $2,610.52 | 85 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 79 | $25.31 | $25.38 | $2,005.02 | 65 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 16 | $161.56 | $162.21 | $2,595.36 | 85 |
| T | 71 | $28.53 | $28.36 | $2,013.56 | 65 |
| TGT | 19 | $105.09 | $104.06 | $1,977.14 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 65 |
| UNH | 6 | $315.79 | $308.55 | $1,851.30 | 65 |
| UNP | 10 | $236.48 | $236.28 | $2,362.80 | 75 |
| V | 6 | $352.90 | $358.86 | $2,153.16 | 65 |
| VZ | 49 | $43.72 | $43.55 | $2,133.95 | 70 |
| WFC | 31 | $82.32 | $83.60 | $2,591.60 | 85 |
| WMT | 23 | $97.38 | $98.36 | $2,262.28 | 75 |
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
| 2025-07-06 16:26:29 | SELL | NKE | 2 | $76.39 | $1.20 | 65 |
| 2025-07-06 16:26:29 | SELL | PFE | 6 | $25.38 | $0.40 | 65 |
| 2025-07-06 16:26:29 | SELL | CSCO | 2 | $69.37 | $2.02 | 70 |
| 2025-07-06 16:26:29 | SELL | CVX | 1 | $148.37 | $1.74 | 75 |
| 2025-07-06 16:26:29 | BUY | INTC | 5 | $22.49 | N/A | 65 |
| 2025-07-06 16:26:29 | BUY | WMT | 2 | $98.36 | N/A | 75 |
| 2025-07-06 16:26:29 | BUY | QCOM | 1 | $162.21 | N/A | 85 |
| 2025-07-06 16:26:29 | BUY | VZ | 2 | $43.55 | N/A | 70 |
| 2025-07-06 16:08:33 | SELL | WMT | 1 | $98.36 | $1.03 | 65 |
| 2025-07-06 16:08:33 | SELL | NKE | 1 | $76.39 | $0.58 | 70 |
| 2025-07-06 16:08:33 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-06 16:08:33 | BUY | PFE | 6 | $25.38 | N/A | 70 |
| 2025-07-06 16:08:33 | BUY | CSCO | 2 | $69.37 | N/A | 75 |
| 2025-07-06 15:50:14 | SELL | WFC | 1 | $83.60 | $1.28 | 80 |
| 2025-07-06 15:50:14 | BUY | BAC | 2 | $48.93 | N/A | 85 |
| 2025-07-06 15:50:14 | BUY | NKE | 3 | $76.39 | N/A | 75 |
| 2025-07-06 15:50:14 | BUY | CSCO | 2 | $69.37 | N/A | 70 |
| 2025-07-06 15:37:19 | SELL | BAC | 3 | $48.93 | $0.67 | 80 |
| 2025-07-06 15:37:19 | SELL | INTC | 6 | $22.49 | $1.16 | 60 |
| 2025-07-06 15:37:19 | SELL | NKE | 1 | $76.39 | $0.62 | 65 |
| 2025-07-06 15:37:19 | SELL | CSCO | 2 | $69.37 | $2.15 | 65 |
| 2025-07-06 15:37:19 | SELL | QCOM | 1 | $162.21 | $0.65 | 75 |
| 2025-07-06 15:37:19 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-06 15:37:19 | BUY | CVX | 1 | $148.37 | N/A | 85 |
| 2025-07-06 15:25:52 | SELL | WFC | 1 | $83.60 | $1.28 | 80 |

<!--TRADE_LOG_END--> 
