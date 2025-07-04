# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-04 01:12:59**

| Metric | Value |
|---|---|
| **Total Value** | **$101,869.82** |
| Cash | $1,901.91 |
| Holdings Value | $99,967.91 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.55 | $2,349.05 | 75 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 65 |
| AMZN | 11 | $221.66 | $223.41 | $2,457.51 | 75 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 65 |
| AXP | 8 | $324.40 | $328.13 | $2,625.04 | 85 |
| BA | 10 | $212.15 | $215.92 | $2,159.20 | 70 |
| BAC | 47 | $48.67 | $48.93 | $2,299.71 | 75 |
| C | 30 | $86.80 | $88.72 | $2,661.60 | 85 |
| CAT | 5 | $395.95 | $397.86 | $1,989.30 | 70 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.15 | $2,177.20 | 65 |
| CSCO | 33 | $68.36 | $69.37 | $2,289.21 | 75 |
| CVX | 16 | $146.52 | $148.37 | $2,373.92 | 75 |
| DIS | 17 | $122.82 | $124.00 | $2,108.00 | 70 |
| GOOGL | 12 | $179.53 | $179.53 | $2,154.36 | 75 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 85 |
| HD | 6 | $372.64 | $371.68 | $2,230.08 | 75 |
| INTC | 82 | $22.28 | $22.49 | $1,844.18 | 60 |
| JNJ | 13 | $155.80 | $156.01 | $2,028.13 | 65 |
| JPM | 9 | $292.50 | $296.00 | $2,664.00 | 85 |
| KO | 28 | $71.03 | $71.35 | $1,997.80 | 65 |
| LLY | 2 | $776.66 | $780.67 | $1,561.34 | 65 |
| MA | 4 | $563.08 | $569.24 | $2,276.96 | 70 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 85 |
| MRK | 25 | $82.57 | $80.93 | $2,023.25 | 65 |
| MSFT | 5 | $491.36 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 70 |
| NKE | 28 | $75.77 | $76.39 | $2,138.92 | 70 |
| NVDA | 16 | $156.39 | $159.34 | $2,549.44 | 85 |
| ORCL | 10 | $226.09 | $237.32 | $2,373.20 | 85 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 85 | $25.31 | $25.38 | $2,157.30 | 70 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 15 | $161.52 | $162.21 | $2,433.15 | 75 |
| T | 71 | $28.53 | $28.36 | $2,013.56 | 65 |
| TGT | 20 | $105.04 | $104.06 | $2,081.20 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 65 |
| UNH | 7 | $314.75 | $308.55 | $2,159.85 | 70 |
| UNP | 9 | $236.50 | $236.28 | $2,126.52 | 70 |
| V | 6 | $352.90 | $358.86 | $2,153.16 | 75 |
| VZ | 46 | $43.73 | $43.55 | $2,003.30 | 65 |
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
| 2025-07-04 01:12:54 | SELL | BAC | 6 | $48.93 | $1.37 | 75 |
| 2025-07-04 01:12:54 | SELL | INTC | 6 | $22.49 | $1.17 | 60 |
| 2025-07-04 01:12:54 | SELL | MRK | 1 | $80.93 | $-1.58 | 65 |
| 2025-07-04 01:12:54 | SELL | T | 5 | $28.36 | $-0.81 | 65 |
| 2025-07-04 00:33:38 | SELL | PFE | 5 | $25.38 | $0.32 | 70 |
| 2025-07-04 00:33:38 | SELL | QCOM | 1 | $162.21 | $0.65 | 75 |
| 2025-07-04 00:33:38 | BUY | NVDA | 2 | $159.34 | N/A | 85 |
| 2025-07-04 00:33:38 | BUY | BAC | 6 | $48.93 | N/A | 85 |
| 2025-07-04 00:33:38 | BUY | INTC | 6 | $22.49 | N/A | 65 |
| 2025-07-04 00:33:38 | BUY | MRK | 1 | $80.93 | N/A | 70 |
| 2025-07-04 00:33:38 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-04 00:33:38 | BUY | CSCO | 3 | $69.37 | N/A | 75 |
| 2025-07-03 23:50:42 | SELL | INTC | 6 | $22.49 | $1.17 | 60 |
| 2025-07-03 23:50:42 | SELL | WFC | 1 | $83.60 | $1.28 | 80 |
| 2025-07-03 23:50:42 | SELL | CVX | 1 | $148.37 | $1.74 | 75 |
| 2025-07-03 23:50:42 | BUY | WMT | 1 | $98.36 | N/A | 75 |
| 2025-07-03 23:50:42 | BUY | CSCO | 1 | $69.37 | N/A | 70 |
| 2025-07-03 23:37:49 | SELL | WMT | 1 | $98.36 | $0.98 | 70 |
| 2025-07-03 23:37:49 | SELL | ORCL | 1 | $237.32 | $10.21 | 75 |
| 2025-07-03 23:37:49 | SELL | VZ | 3 | $43.55 | $-0.51 | 65 |
| 2025-07-03 23:37:49 | BUY | BAC | 3 | $48.93 | N/A | 75 |
| 2025-07-03 23:37:49 | BUY | CVX | 1 | $148.37 | N/A | 85 |
| 2025-07-03 23:37:49 | BUY | QCOM | 2 | $162.21 | N/A | 85 |
| 2025-07-03 23:25:38 | SELL | V | 1 | $358.86 | $5.11 | 65 |
| 2025-07-03 23:25:38 | SELL | BAC | 4 | $48.93 | $1.01 | 70 |

<!--TRADE_LOG_END--> 
