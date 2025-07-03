# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 17:08:43**

| Metric | Value |
|---|---|
| **Total Value** | **$101,846.87** |
| Cash | $1,663.19 |
| Holdings Value | $100,183.68 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.55 | $2,349.05 | 75 |
| ADBE | 5 | $377.60 | $379.31 | $1,896.55 | 65 |
| AMD | 15 | $135.93 | $137.91 | $2,068.65 | 70 |
| AMZN | 11 | $221.66 | $223.41 | $2,457.51 | 85 |
| AVGO | 8 | $269.90 | $275.18 | $2,201.44 | 65 |
| AXP | 8 | $324.40 | $328.30 | $2,626.40 | 85 |
| BA | 10 | $212.15 | $215.77 | $2,157.70 | 65 |
| BAC | 54 | $48.71 | $48.92 | $2,641.68 | 85 |
| C | 30 | $86.80 | $88.64 | $2,659.20 | 85 |
| CAT | 6 | $396.45 | $398.31 | $2,389.86 | 70 |
| COST | 2 | $979.83 | $987.02 | $1,974.04 | 65 |
| CRM | 8 | $268.33 | $272.23 | $2,177.84 | 65 |
| CSCO | 33 | $68.36 | $69.37 | $2,289.21 | 75 |
| CVX | 17 | $146.66 | $148.35 | $2,521.95 | 85 |
| DIS | 18 | $122.90 | $123.92 | $2,230.56 | 75 |
| GOOGL | 13 | $177.86 | $179.53 | $2,333.89 | 75 |
| GS | 3 | $717.52 | $723.47 | $2,170.41 | 85 |
| HD | 6 | $372.64 | $371.86 | $2,231.13 | 65 |
| INTC | 89 | $22.30 | $22.49 | $2,001.61 | 65 |
| JNJ | 13 | $155.80 | $155.92 | $2,026.96 | 65 |
| JPM | 9 | $292.50 | $295.71 | $2,661.39 | 85 |
| KO | 29 | $71.04 | $71.30 | $2,067.70 | 65 |
| LLY | 2 | $776.66 | $780.45 | $1,560.90 | 65 |
| MA | 3 | $561.03 | $568.45 | $1,705.35 | 65 |
| META | 3 | $717.12 | $719.01 | $2,157.03 | 85 |
| MRK | 25 | $82.57 | $80.95 | $2,023.75 | 65 |
| MSFT | 5 | $491.36 | $498.84 | $2,494.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.18 | $1,297.18 | 70 |
| NKE | 28 | $75.74 | $76.30 | $2,136.40 | 70 |
| NVDA | 14 | $155.97 | $159.34 | $2,230.76 | 75 |
| ORCL | 9 | $224.84 | $237.03 | $2,133.27 | 65 |
| PEP | 15 | $136.59 | $135.38 | $2,030.70 | 65 |
| PFE | 79 | $25.30 | $25.38 | $2,004.62 | 65 |
| PG | 12 | $160.76 | $160.69 | $1,928.34 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 15 | $161.52 | $162.21 | $2,433.15 | 75 |
| T | 81 | $28.51 | $28.34 | $2,295.14 | 75 |
| TGT | 19 | $105.07 | $104.13 | $1,978.47 | 65 |
| TSLA | 6 | $313.02 | $315.35 | $1,892.10 | 65 |
| UNH | 7 | $314.75 | $308.52 | $2,159.64 | 65 |
| UNP | 9 | $236.50 | $236.38 | $2,127.42 | 70 |
| V | 6 | $352.90 | $358.67 | $2,152.02 | 70 |
| VZ | 46 | $43.73 | $43.52 | $2,001.92 | 65 |
| WFC | 31 | $82.32 | $83.51 | $2,588.81 | 85 |
| WMT | 21 | $97.29 | $98.32 | $2,064.72 | 65 |
| XOM | 21 | $109.97 | $112.16 | $2,355.36 | 75 |

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
| 2025-07-03 16:43:14 | BUY | KO | 1 | $71.35 | N/A | 70 |
| 2025-07-03 16:43:14 | BUY | PYPL | 1 | $76.84 | N/A | 75 |
| 2025-07-03 16:43:14 | BUY | NKE | 1 | $76.53 | N/A | 70 |
| 2025-07-03 16:43:14 | BUY | WFC | 2 | $83.61 | N/A | 85 |
| 2025-07-03 16:43:14 | BUY | CSCO | 3 | $69.32 | N/A | 75 |

<!--TRADE_LOG_END--> 
