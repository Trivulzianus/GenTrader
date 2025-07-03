# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 17:25:58**

| Metric | Value |
|---|---|
| **Total Value** | **$101,961.87** |
| Cash | $1,553.04 |
| Holdings Value | $100,408.83 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.55 | $2,349.05 | 75 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 70 |
| AMZN | 11 | $221.66 | $223.41 | $2,457.51 | 85 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 70 |
| AXP | 8 | $324.40 | $328.77 | $2,630.16 | 85 |
| BA | 10 | $212.15 | $215.41 | $2,154.10 | 65 |
| BAC | 54 | $48.71 | $49.02 | $2,647.08 | 85 |
| C | 30 | $86.80 | $88.74 | $2,662.20 | 85 |
| CAT | 5 | $395.95 | $398.93 | $1,994.65 | 65 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $273.33 | $2,186.64 | 65 |
| CSCO | 33 | $68.36 | $69.37 | $2,289.21 | 75 |
| CVX | 16 | $146.52 | $148.85 | $2,381.60 | 75 |
| DIS | 18 | $122.90 | $124.14 | $2,234.61 | 70 |
| GOOGL | 13 | $177.86 | $179.53 | $2,333.89 | 75 |
| GS | 3 | $717.52 | $723.25 | $2,169.75 | 85 |
| HD | 6 | $372.64 | $372.75 | $2,236.47 | 70 |
| INTC | 89 | $22.30 | $22.49 | $2,001.61 | 65 |
| JNJ | 13 | $155.80 | $156.19 | $2,030.47 | 65 |
| JPM | 9 | $292.50 | $296.00 | $2,663.95 | 85 |
| KO | 30 | $71.05 | $71.31 | $2,139.45 | 70 |
| LLY | 2 | $776.66 | $779.36 | $1,558.72 | 65 |
| MA | 3 | $561.03 | $569.52 | $1,708.56 | 70 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 85 |
| MRK | 25 | $82.57 | $81.44 | $2,035.88 | 65 |
| MSFT | 5 | $491.36 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 70 |
| NKE | 34 | $75.88 | $76.53 | $2,602.19 | 85 |
| NVDA | 14 | $155.97 | $159.34 | $2,230.76 | 75 |
| ORCL | 9 | $224.84 | $237.15 | $2,134.35 | 70 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 84 | $25.31 | $25.48 | $2,140.32 | 70 |
| PG | 12 | $160.76 | $160.87 | $1,930.38 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 15 | $161.52 | $162.21 | $2,433.15 | 75 |
| T | 81 | $28.51 | $28.36 | $2,297.57 | 75 |
| TGT | 19 | $105.07 | $104.36 | $1,982.75 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 55 |
| UNH | 7 | $314.75 | $309.75 | $2,168.25 | 65 |
| UNP | 9 | $236.50 | $237.77 | $2,139.93 | 65 |
| V | 6 | $352.90 | $358.87 | $2,153.22 | 75 |
| VZ | 46 | $43.73 | $43.55 | $2,003.30 | 65 |
| WFC | 31 | $82.32 | $83.64 | $2,592.68 | 85 |
| WMT | 21 | $97.29 | $98.28 | $2,063.91 | 70 |
| XOM | 21 | $109.97 | $112.42 | $2,360.92 | 75 |

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
| 2025-07-03 17:25:51 | SELL | CAT | 1 | $398.93 | $2.48 | 65 |
| 2025-07-03 17:25:51 | SELL | CVX | 1 | $148.85 | $2.19 | 75 |
| 2025-07-03 17:25:51 | BUY | KO | 1 | $71.32 | N/A | 70 |
| 2025-07-03 17:25:51 | BUY | PFE | 5 | $25.48 | N/A | 70 |
| 2025-07-03 17:25:51 | BUY | NKE | 6 | $76.54 | N/A | 85 |
| 2025-07-03 17:08:34 | SELL | INTC | 2 | $22.49 | $0.38 | 65 |
| 2025-07-03 17:08:34 | SELL | KO | 1 | $71.30 | $0.25 | 65 |
| 2025-07-03 17:08:34 | SELL | WMT | 2 | $98.32 | $1.88 | 65 |
| 2025-07-03 17:08:34 | SELL | MRK | 2 | $80.95 | $-3.00 | 65 |
| 2025-07-03 17:08:34 | SELL | ORCL | 1 | $237.03 | $10.97 | 65 |
| 2025-07-03 17:08:34 | BUY | AMZN | 1 | $223.41 | N/A | 85 |
| 2025-07-03 17:08:34 | BUY | T | 5 | $28.33 | N/A | 75 |
| 2025-07-03 17:08:34 | BUY | CVX | 1 | $148.35 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
