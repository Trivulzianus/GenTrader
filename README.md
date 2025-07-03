# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 14:26:10**

| Metric | Value |
|---|---|
| **Total Value** | **$101,737.39** |
| Cash | $2,973.89 |
| Holdings Value | $98,763.50 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $213.59 | $2,135.90 | 70 |
| ADBE | 5 | $377.60 | $380.53 | $1,902.65 | 60 |
| AMD | 15 | $135.93 | $139.00 | $2,085.00 | 65 |
| AMZN | 10 | $221.48 | $221.51 | $2,215.15 | 70 |
| AVGO | 8 | $269.90 | $275.28 | $2,202.24 | 70 |
| AXP | 8 | $324.40 | $327.83 | $2,622.68 | 85 |
| BA | 10 | $212.15 | $217.00 | $2,170.00 | 70 |
| BAC | 45 | $48.63 | $48.98 | $2,203.89 | 70 |
| C | 30 | $86.80 | $88.08 | $2,642.40 | 85 |
| CAT | 6 | $396.45 | $401.67 | $2,410.02 | 70 |
| COST | 2 | $979.83 | $985.67 | $1,971.34 | 65 |
| CRM | 7 | $267.51 | $273.19 | $1,912.33 | 65 |
| CSCO | 33 | $68.37 | $68.95 | $2,275.35 | 75 |
| CVX | 16 | $146.55 | $147.65 | $2,362.40 | 75 |
| DIS | 18 | $122.90 | $123.58 | $2,224.44 | 75 |
| GOOGL | 13 | $177.82 | $178.23 | $2,316.99 | 75 |
| GS | 3 | $717.52 | $725.34 | $2,176.01 | 85 |
| HD | 6 | $372.64 | $369.60 | $2,217.60 | 65 |
| INTC | 83 | $22.33 | $22.38 | $1,857.12 | 60 |
| JNJ | 13 | $155.80 | $155.07 | $2,015.88 | 65 |
| JPM | 9 | $292.50 | $294.62 | $2,651.61 | 85 |
| KO | 28 | $71.03 | $70.77 | $1,981.42 | 65 |
| LLY | 2 | $776.66 | $778.97 | $1,557.94 | 65 |
| MA | 3 | $561.03 | $566.61 | $1,699.83 | 65 |
| META | 3 | $717.12 | $716.12 | $2,148.38 | 85 |
| MRK | 25 | $82.46 | $81.10 | $2,027.50 | 65 |
| MSFT | 5 | $491.36 | $498.06 | $2,490.30 | 85 |
| NFLX | 1 | $1,279.00 | $1,294.42 | $1,294.42 | 70 |
| NKE | 29 | $75.78 | $75.86 | $2,199.94 | 70 |
| NVDA | 16 | $156.55 | $160.82 | $2,573.20 | 85 |
| ORCL | 9 | $224.73 | $233.00 | $2,097.00 | 65 |
| PEP | 15 | $136.59 | $135.61 | $2,034.12 | 65 |
| PFE | 86 | $25.32 | $25.26 | $2,171.95 | 70 |
| PG | 12 | $160.76 | $160.34 | $1,924.14 | 65 |
| PYPL | 30 | $76.82 | $76.92 | $2,307.75 | 75 |
| QCOM | 14 | $161.41 | $163.68 | $2,291.45 | 70 |
| T | 72 | $28.53 | $28.32 | $2,039.40 | 65 |
| TGT | 20 | $105.04 | $104.63 | $2,092.60 | 65 |
| TSLA | 6 | $313.02 | $313.40 | $1,880.41 | 65 |
| UNH | 7 | $314.75 | $311.64 | $2,181.48 | 65 |
| UNP | 9 | $236.50 | $237.54 | $2,137.86 | 75 |
| V | 6 | $352.90 | $357.12 | $2,142.72 | 75 |
| VZ | 47 | $43.73 | $43.51 | $2,044.81 | 65 |
| WFC | 31 | $82.32 | $83.64 | $2,592.84 | 85 |
| WMT | 21 | $97.32 | $97.55 | $2,048.45 | 65 |
| XOM | 20 | $109.86 | $111.63 | $2,232.60 | 75 |

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
| 2025-07-03 14:26:03 | SELL | BAC | 8 | $48.94 | $2.14 | 70 |
| 2025-07-03 14:26:03 | BUY | NVDA | 2 | $160.84 | N/A | 85 |
| 2025-07-03 14:26:03 | BUY | PFE | 6 | $25.25 | N/A | 70 |
| 2025-07-03 14:08:35 | SELL | NKE | 5 | $76.23 | $1.92 | 70 |
| 2025-07-03 14:08:35 | SELL | MRK | 2 | $81.92 | $-0.99 | 65 |
| 2025-07-03 14:08:35 | SELL | PFE | 4 | $25.33 | $0.02 | 65 |
| 2025-07-03 14:08:35 | SELL | VZ | 2 | $43.67 | $-0.12 | 65 |
| 2025-07-03 14:08:35 | SELL | T | 5 | $28.35 | $-0.83 | 65 |
| 2025-07-03 14:08:35 | BUY | V | 1 | $356.90 | N/A | 70 |
| 2025-07-03 14:08:35 | BUY | BAC | 6 | $49.19 | N/A | 85 |
| 2025-07-03 13:54:59 | SELL | BAC | 6 | $49.28 | $3.57 | 75 |
| 2025-07-03 13:54:59 | SELL | INTC | 1 | $22.33 | $-0.01 | 60 |
| 2025-07-03 13:54:59 | SELL | WMT | 1 | $97.82 | $0.47 | 65 |
| 2025-07-03 13:54:59 | SELL | MRK | 1 | $81.90 | $-0.50 | 70 |
| 2025-07-03 13:54:59 | SELL | QCOM | 1 | $163.02 | $1.50 | 70 |
| 2025-07-03 13:54:59 | BUY | NKE | 3 | $76.49 | N/A | 85 |
| 2025-07-03 13:54:59 | BUY | DIS | 1 | $123.64 | N/A | 75 |
| 2025-07-03 13:54:59 | BUY | PFE | 4 | $25.41 | N/A | 70 |
| 2025-07-03 13:54:59 | BUY | WFC | 3 | $83.72 | N/A | 85 |
| 2025-07-03 13:54:59 | BUY | CSCO | 1 | $68.79 | N/A | 75 |
| 2025-07-03 13:54:59 | BUY | VZ | 3 | $43.63 | N/A | 70 |
| 2025-07-03 13:44:30 | SELL | XOM | 1 | $111.39 | $1.46 | 70 |
| 2025-07-03 13:44:30 | SELL | INTC | 6 | $22.29 | $-0.22 | 60 |
| 2025-07-03 13:44:30 | SELL | PFE | 3 | $25.31 | $-0.06 | 65 |
| 2025-07-03 13:44:30 | SELL | NKE | 2 | $76.68 | $1.68 | 75 |

<!--TRADE_LOG_END--> 
