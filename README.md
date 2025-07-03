# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 20:08:17**

| Metric | Value |
|---|---|
| **Total Value** | **$101,869.82** |
| Cash | $2,055.66 |
| Holdings Value | $99,814.16 |

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
| BAC | 48 | $48.68 | $48.93 | $2,348.64 | 75 |
| C | 30 | $86.80 | $88.72 | $2,661.60 | 85 |
| CAT | 5 | $395.95 | $397.86 | $1,989.30 | 70 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.15 | $2,177.20 | 65 |
| CSCO | 33 | $68.36 | $69.37 | $2,289.21 | 75 |
| CVX | 16 | $146.52 | $148.37 | $2,373.92 | 75 |
| DIS | 17 | $122.82 | $124.00 | $2,108.00 | 70 |
| GOOGL | 12 | $177.72 | $179.53 | $2,154.36 | 70 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 85 |
| HD | 6 | $372.64 | $371.68 | $2,230.08 | 65 |
| INTC | 88 | $22.30 | $22.49 | $1,979.12 | 65 |
| JNJ | 13 | $155.80 | $156.01 | $2,028.13 | 65 |
| JPM | 9 | $292.50 | $296.00 | $2,664.00 | 85 |
| KO | 29 | $71.04 | $71.35 | $2,069.15 | 65 |
| LLY | 2 | $776.66 | $780.67 | $1,561.34 | 65 |
| MA | 3 | $561.03 | $569.24 | $1,707.72 | 70 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 75 |
| MRK | 26 | $82.51 | $80.93 | $2,104.18 | 70 |
| MSFT | 5 | $491.36 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 75 |
| NKE | 28 | $75.77 | $76.39 | $2,138.92 | 70 |
| NVDA | 14 | $155.97 | $159.34 | $2,230.76 | 75 |
| ORCL | 11 | $227.11 | $237.32 | $2,610.52 | 85 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 84 | $25.31 | $25.38 | $2,131.92 | 70 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 14 | $161.47 | $162.21 | $2,270.94 | 70 |
| T | 76 | $28.52 | $28.36 | $2,155.36 | 70 |
| TGT | 20 | $105.04 | $104.06 | $2,081.20 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 60 |
| UNH | 7 | $314.75 | $308.55 | $2,159.85 | 65 |
| UNP | 9 | $236.50 | $236.28 | $2,126.52 | 70 |
| V | 6 | $352.90 | $358.86 | $2,153.16 | 70 |
| VZ | 53 | $43.71 | $43.55 | $2,308.15 | 75 |
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
| 2025-07-03 20:08:10 | SELL | GOOGL | 1 | $179.53 | $1.67 | 70 |
| 2025-07-03 20:08:10 | SELL | BAC | 5 | $48.93 | $1.14 | 75 |
| 2025-07-03 20:08:10 | BUY | INTC | 5 | $22.49 | N/A | 65 |
| 2025-07-03 20:08:10 | BUY | PFE | 4 | $25.38 | N/A | 70 |
| 2025-07-03 20:08:10 | BUY | MRK | 1 | $80.93 | N/A | 70 |
| 2025-07-03 20:08:10 | BUY | VZ | 4 | $43.55 | N/A | 75 |
| 2025-07-03 19:50:00 | SELL | INTC | 6 | $22.49 | $1.16 | 60 |
| 2025-07-03 19:50:00 | SELL | WMT | 1 | $98.36 | $0.98 | 70 |
| 2025-07-03 19:50:00 | SELL | PFE | 5 | $25.38 | $0.34 | 65 |
| 2025-07-03 19:50:00 | BUY | WFC | 3 | $83.60 | N/A | 85 |
| 2025-07-03 19:50:00 | BUY | ORCL | 1 | $237.32 | N/A | 85 |
| 2025-07-03 19:50:00 | BUY | VZ | 3 | $43.55 | N/A | 70 |
| 2025-07-03 19:35:40 | SELL | KO | 1 | $71.35 | $0.30 | 65 |
| 2025-07-03 19:35:40 | SELL | WFC | 3 | $83.60 | $3.83 | 75 |
| 2025-07-03 19:35:40 | SELL | ORCL | 1 | $237.32 | $10.21 | 70 |
| 2025-07-03 19:35:40 | BUY | BAC | 5 | $48.93 | N/A | 85 |
| 2025-07-03 19:35:40 | BUY | WMT | 1 | $98.36 | N/A | 75 |
| 2025-07-03 19:35:40 | BUY | CSCO | 1 | $69.37 | N/A | 75 |
| 2025-07-03 19:23:53 | SELL | BAC | 6 | $48.93 | $1.35 | 75 |
| 2025-07-03 19:23:53 | SELL | CSCO | 1 | $69.37 | $1.01 | 70 |
| 2025-07-03 19:23:53 | BUY | INTC | 1 | $22.49 | N/A | 65 |
| 2025-07-03 19:07:20 | SELL | V | 1 | $358.86 | $5.11 | 65 |
| 2025-07-03 19:07:20 | SELL | PFE | 5 | $25.38 | $0.32 | 70 |
| 2025-07-03 19:07:20 | BUY | INTC | 6 | $22.49 | N/A | 65 |
| 2025-07-03 19:07:20 | BUY | NKE | 2 | $76.39 | N/A | 70 |

<!--TRADE_LOG_END--> 
