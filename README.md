# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 14:52:16**

| Metric | Value |
|---|---|
| **Total Value** | **$101,843.42** |
| Cash | $2,707.09 |
| Holdings Value | $99,136.33 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $213.24 | $2,132.40 | 70 |
| ADBE | 5 | $377.60 | $381.08 | $1,905.41 | 65 |
| AMD | 15 | $135.93 | $137.93 | $2,068.96 | 65 |
| AMZN | 10 | $221.48 | $222.06 | $2,220.60 | 75 |
| AVGO | 8 | $269.90 | $273.41 | $2,187.28 | 70 |
| AXP | 8 | $324.40 | $328.57 | $2,628.56 | 75 |
| BA | 10 | $212.15 | $216.89 | $2,168.90 | 70 |
| BAC | 47 | $48.65 | $49.01 | $2,303.47 | 75 |
| C | 30 | $86.80 | $88.29 | $2,648.70 | 85 |
| CAT | 6 | $396.45 | $401.50 | $2,408.97 | 65 |
| COST | 2 | $979.83 | $986.51 | $1,973.02 | 65 |
| CRM | 7 | $267.51 | $272.89 | $1,910.23 | 65 |
| CSCO | 33 | $68.37 | $69.17 | $2,282.45 | 75 |
| CVX | 16 | $146.55 | $148.77 | $2,380.32 | 75 |
| DIS | 18 | $122.90 | $123.57 | $2,224.26 | 70 |
| GOOGL | 13 | $177.82 | $178.49 | $2,320.31 | 75 |
| GS | 3 | $717.52 | $724.36 | $2,173.08 | 70 |
| HD | 6 | $372.64 | $371.49 | $2,228.94 | 65 |
| INTC | 84 | $22.33 | $22.36 | $1,878.25 | 60 |
| JNJ | 13 | $155.80 | $155.96 | $2,027.48 | 65 |
| JPM | 9 | $292.50 | $295.40 | $2,658.60 | 85 |
| KO | 28 | $71.03 | $71.09 | $1,990.66 | 65 |
| LLY | 2 | $776.66 | $778.54 | $1,557.09 | 65 |
| MA | 3 | $561.03 | $567.92 | $1,703.76 | 65 |
| META | 3 | $717.12 | $716.29 | $2,148.88 | 85 |
| MRK | 25 | $82.46 | $81.39 | $2,034.88 | 65 |
| MSFT | 5 | $491.36 | $498.18 | $2,490.90 | 85 |
| NFLX | 1 | $1,279.00 | $1,294.55 | $1,294.55 | 70 |
| NKE | 34 | $75.82 | $76.00 | $2,584.17 | 85 |
| NVDA | 14 | $156.01 | $159.43 | $2,232.02 | 70 |
| ORCL | 9 | $224.73 | $232.77 | $2,094.92 | 70 |
| PEP | 15 | $136.59 | $135.73 | $2,035.89 | 65 |
| PFE | 80 | $25.32 | $25.45 | $2,036.40 | 65 |
| PG | 12 | $160.76 | $160.68 | $1,928.16 | 65 |
| PYPL | 30 | $76.82 | $77.01 | $2,310.30 | 75 |
| QCOM | 14 | $161.41 | $163.23 | $2,285.22 | 75 |
| T | 77 | $28.52 | $28.38 | $2,185.26 | 70 |
| TGT | 20 | $105.04 | $104.48 | $2,089.70 | 70 |
| TSLA | 6 | $313.02 | $315.23 | $1,891.38 | 60 |
| UNH | 7 | $314.75 | $311.31 | $2,179.17 | 65 |
| UNP | 9 | $236.50 | $238.15 | $2,143.35 | 70 |
| V | 6 | $352.90 | $358.17 | $2,148.99 | 70 |
| VZ | 47 | $43.73 | $43.59 | $2,048.49 | 65 |
| WFC | 31 | $82.32 | $83.66 | $2,593.46 | 85 |
| WMT | 22 | $97.34 | $98.08 | $2,157.65 | 70 |
| XOM | 20 | $109.86 | $112.05 | $2,240.90 | 75 |

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
| 2025-07-03 14:52:10 | SELL | INTC | 6 | $22.36 | $0.16 | 60 |
| 2025-07-03 14:52:10 | SELL | PFE | 6 | $25.45 | $0.77 | 65 |
| 2025-07-03 14:52:10 | BUY | NKE | 5 | $76.02 | N/A | 85 |
| 2025-07-03 14:52:10 | BUY | WFC | 1 | $83.65 | N/A | 85 |
| 2025-07-03 14:52:10 | BUY | T | 5 | $28.39 | N/A | 70 |
| 2025-07-03 14:40:23 | SELL | NVDA | 2 | $160.31 | $7.52 | 70 |
| 2025-07-03 14:40:23 | SELL | WFC | 1 | $83.73 | $1.41 | 80 |
| 2025-07-03 14:40:23 | BUY | BAC | 2 | $49.05 | N/A | 75 |
| 2025-07-03 14:40:23 | BUY | INTC | 7 | $22.34 | N/A | 65 |
| 2025-07-03 14:40:23 | BUY | WMT | 1 | $97.88 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
