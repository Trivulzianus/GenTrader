# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 11:25:05**

| Metric | Value |
|---|---|
| **Total Value** | **$101,869.82** |
| Cash | $1,423.63 |
| Holdings Value | $100,446.19 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $213.55 | $2,135.50 | 70 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 65 |
| AMZN | 11 | $221.66 | $223.41 | $2,457.51 | 85 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 70 |
| AXP | 7 | $323.87 | $328.13 | $2,296.91 | 85 |
| BA | 10 | $212.15 | $215.92 | $2,159.20 | 70 |
| BAC | 53 | $48.70 | $48.93 | $2,593.29 | 85 |
| C | 29 | $86.74 | $88.72 | $2,572.88 | 85 |
| CAT | 6 | $397.86 | $397.86 | $2,387.16 | 70 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.15 | $2,177.20 | 65 |
| CSCO | 31 | $68.29 | $69.37 | $2,150.47 | 70 |
| CVX | 16 | $146.52 | $148.37 | $2,373.92 | 75 |
| DIS | 17 | $122.82 | $124.00 | $2,108.00 | 70 |
| GOOGL | 12 | $179.53 | $179.53 | $2,154.36 | 75 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 85 |
| HD | 6 | $372.64 | $371.68 | $2,230.08 | 65 |
| INTC | 75 | $22.26 | $22.49 | $1,686.75 | 55 |
| JNJ | 13 | $155.80 | $156.01 | $2,028.13 | 65 |
| JPM | 9 | $292.50 | $296.00 | $2,664.00 | 85 |
| KO | 28 | $71.03 | $71.35 | $1,997.80 | 65 |
| LLY | 2 | $776.66 | $780.67 | $1,561.34 | 65 |
| MA | 4 | $563.08 | $569.24 | $2,276.96 | 70 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 85 |
| MRK | 25 | $82.57 | $80.93 | $2,023.25 | 65 |
| MSFT | 5 | $498.84 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 65 |
| NKE | 29 | $75.79 | $76.39 | $2,215.31 | 70 |
| NVDA | 16 | $156.39 | $159.34 | $2,549.44 | 85 |
| ORCL | 11 | $227.11 | $237.32 | $2,610.52 | 85 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 84 | $25.31 | $25.38 | $2,131.92 | 70 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 16 | $161.56 | $162.21 | $2,595.36 | 85 |
| T | 71 | $28.53 | $28.36 | $2,013.56 | 65 |
| TGT | 19 | $105.09 | $104.06 | $1,977.14 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 60 |
| UNH | 7 | $314.75 | $308.55 | $2,159.85 | 65 |
| UNP | 10 | $236.48 | $236.28 | $2,362.80 | 75 |
| V | 6 | $352.90 | $358.86 | $2,153.16 | 70 |
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
| 2025-07-07 11:24:59 | SELL | INTC | 7 | $22.49 | $1.46 | 55 |
| 2025-07-07 11:24:59 | SELL | CSCO | 2 | $69.37 | $2.02 | 70 |
| 2025-07-07 11:24:59 | BUY | WMT | 2 | $98.36 | N/A | 75 |
| 2025-07-07 11:24:59 | BUY | PFE | 5 | $25.38 | N/A | 70 |
| 2025-07-07 11:24:59 | BUY | QCOM | 2 | $162.21 | N/A | 85 |
| 2025-07-07 11:24:59 | BUY | VZ | 3 | $43.55 | N/A | 70 |
| 2025-07-07 11:08:00 | SELL | INTC | 1 | $22.49 | $0.21 | 60 |
| 2025-07-07 11:08:00 | SELL | PFE | 6 | $25.38 | $0.40 | 65 |
| 2025-07-07 11:08:00 | SELL | VZ | 1 | $43.55 | $-0.18 | 65 |
| 2025-07-07 11:08:00 | SELL | CVX | 1 | $148.37 | $1.74 | 75 |
| 2025-07-07 11:08:00 | SELL | T | 5 | $28.36 | $-0.81 | 65 |
| 2025-07-07 11:08:00 | BUY | CSCO | 2 | $69.37 | N/A | 75 |
| 2025-07-07 10:53:32 | SELL | INTC | 5 | $22.49 | $0.97 | 60 |
| 2025-07-07 10:53:32 | SELL | VZ | 2 | $43.55 | $-0.34 | 65 |
| 2025-07-07 10:53:32 | BUY | PFE | 6 | $25.38 | N/A | 70 |
| 2025-07-07 10:53:32 | BUY | CVX | 1 | $148.37 | N/A | 85 |
| 2025-07-07 10:42:16 | SELL | WMT | 2 | $98.36 | $1.97 | 65 |
| 2025-07-07 10:42:16 | SELL | QCOM | 1 | $162.21 | $0.69 | 70 |
| 2025-07-07 10:42:16 | SELL | CVX | 1 | $148.37 | $1.74 | 75 |
| 2025-07-07 10:42:16 | BUY | VZ | 3 | $43.55 | N/A | 70 |
| 2025-07-07 10:26:41 | SELL | AAPL | 1 | $213.55 | $2.00 | 70 |
| 2025-07-07 10:26:41 | SELL | PFE | 6 | $25.38 | $0.40 | 65 |
| 2025-07-07 10:26:41 | SELL | T | 1 | $28.36 | $-0.16 | 70 |
| 2025-07-07 10:26:41 | SELL | VZ | 7 | $43.55 | $-1.11 | 65 |
| 2025-07-07 10:26:41 | BUY | INTC | 6 | $22.49 | N/A | 65 |

<!--TRADE_LOG_END--> 
