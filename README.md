# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 01:59:23**

| Metric | Value |
|---|---|
| **Total Value** | **$101,869.82** |
| Cash | $1,477.94 |
| Holdings Value | $100,391.88 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.55 | $2,349.05 | 70 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 65 |
| AMZN | 11 | $221.66 | $223.41 | $2,457.51 | 75 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 70 |
| AXP | 7 | $323.87 | $328.13 | $2,296.91 | 75 |
| BA | 10 | $212.15 | $215.92 | $2,159.20 | 70 |
| BAC | 44 | $48.65 | $48.93 | $2,152.92 | 70 |
| C | 24 | $86.32 | $88.72 | $2,129.28 | 70 |
| CAT | 6 | $397.86 | $397.86 | $2,387.16 | 65 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.15 | $2,177.20 | 65 |
| CSCO | 33 | $68.36 | $69.37 | $2,289.21 | 75 |
| CVX | 16 | $146.52 | $148.37 | $2,373.92 | 80 |
| DIS | 21 | $123.05 | $124.00 | $2,604.00 | 85 |
| GOOGL | 13 | $179.53 | $179.53 | $2,333.89 | 75 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 75 |
| HD | 6 | $372.64 | $371.68 | $2,230.08 | 65 |
| INTC | 90 | $22.30 | $22.49 | $2,024.10 | 65 |
| JNJ | 13 | $155.80 | $156.01 | $2,028.13 | 65 |
| JPM | 9 | $292.50 | $296.00 | $2,664.00 | 85 |
| KO | 28 | $71.03 | $71.35 | $1,997.80 | 65 |
| LLY | 2 | $776.66 | $780.67 | $1,561.34 | 65 |
| MA | 4 | $563.08 | $569.24 | $2,276.96 | 70 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 70 |
| MRK | 25 | $82.57 | $80.93 | $2,023.25 | 65 |
| MSFT | 5 | $498.84 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 65 |
| NKE | 28 | $75.77 | $76.39 | $2,138.92 | 70 |
| NVDA | 16 | $156.39 | $159.34 | $2,549.44 | 85 |
| ORCL | 11 | $227.11 | $237.32 | $2,610.52 | 85 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 86 | $25.31 | $25.38 | $2,182.68 | 70 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 14 | $161.47 | $162.21 | $2,270.94 | 75 |
| T | 71 | $28.53 | $28.36 | $2,013.56 | 65 |
| TGT | 19 | $105.09 | $104.06 | $1,977.14 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 65 |
| UNH | 7 | $314.75 | $308.55 | $2,159.85 | 65 |
| UNP | 10 | $236.48 | $236.28 | $2,362.80 | 75 |
| V | 6 | $352.90 | $358.86 | $2,153.16 | 65 |
| VZ | 47 | $43.73 | $43.55 | $2,046.85 | 65 |
| WFC | 31 | $82.32 | $83.60 | $2,591.60 | 85 |
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
| 2025-07-07 01:59:17 | BUY | BAC | 2 | $48.93 | N/A | 70 |
| 2025-07-07 01:59:17 | BUY | INTC | 6 | $22.49 | N/A | 65 |
| 2025-07-07 01:59:17 | BUY | DIS | 3 | $124.00 | N/A | 85 |
| 2025-07-07 01:59:17 | BUY | WMT | 1 | $98.36 | N/A | 70 |
| 2025-07-07 01:59:17 | BUY | PFE | 6 | $25.38 | N/A | 70 |
| 2025-07-07 01:59:17 | BUY | C | 1 | $88.72 | N/A | 70 |
| 2025-07-07 01:59:17 | BUY | CSCO | 1 | $69.37 | N/A | 75 |
| 2025-07-07 01:13:23 | SELL | BAC | 2 | $48.93 | $0.55 | 65 |
| 2025-07-07 01:13:23 | SELL | C | 2 | $88.72 | $4.60 | 65 |
| 2025-07-07 01:13:23 | SELL | CSCO | 1 | $69.37 | $1.01 | 70 |
| 2025-07-07 01:13:23 | SELL | CVX | 1 | $148.37 | $1.74 | 75 |
| 2025-07-07 01:13:23 | BUY | NKE | 1 | $76.39 | N/A | 70 |
| 2025-07-07 00:36:42 | SELL | WMT | 2 | $98.36 | $1.97 | 65 |
| 2025-07-07 00:36:42 | SELL | NKE | 1 | $76.39 | $0.62 | 65 |
| 2025-07-07 00:36:42 | BUY | CSCO | 1 | $69.37 | N/A | 75 |
| 2025-07-07 00:36:42 | BUY | CVX | 1 | $148.37 | N/A | 85 |
| 2025-07-06 23:50:52 | SELL | INTC | 5 | $22.49 | $0.96 | 60 |
| 2025-07-06 23:50:52 | SELL | VZ | 2 | $43.55 | $-0.34 | 65 |
| 2025-07-06 23:50:52 | SELL | CVX | 1 | $148.37 | $1.74 | 75 |
| 2025-07-06 23:50:52 | BUY | BAC | 2 | $48.93 | N/A | 70 |
| 2025-07-06 23:37:49 | SELL | CSCO | 1 | $69.37 | $1.01 | 70 |
| 2025-07-06 23:37:49 | BUY | UNH | 1 | $308.55 | N/A | 70 |
| 2025-07-06 23:37:49 | BUY | INTC | 6 | $22.49 | N/A | 65 |
| 2025-07-06 23:37:49 | BUY | NKE | 1 | $76.39 | N/A | 70 |
| 2025-07-06 23:37:49 | BUY | VZ | 2 | $43.55 | N/A | 70 |

<!--TRADE_LOG_END--> 
