# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 14:26:02**

| Metric | Value |
|---|---|
| **Total Value** | **$101,126.86** |
| Cash | $658.66 |
| Holdings Value | $100,468.21 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $212.61 | $2,126.10 | 65 |
| ADBE | 5 | $377.60 | $380.19 | $1,900.97 | 65 |
| AMD | 15 | $135.79 | $135.16 | $2,027.36 | 70 |
| AMZN | 11 | $221.66 | $223.99 | $2,463.89 | 85 |
| AVGO | 8 | $269.90 | $276.67 | $2,213.32 | 70 |
| AXP | 8 | $324.34 | $326.44 | $2,611.52 | 85 |
| BA | 10 | $212.15 | $215.62 | $2,156.20 | 70 |
| BAC | 53 | $48.70 | $48.98 | $2,595.94 | 85 |
| C | 24 | $86.36 | $88.24 | $2,117.76 | 70 |
| CAT | 6 | $397.86 | $394.54 | $2,367.24 | 85 |
| COST | 2 | $979.83 | $979.92 | $1,959.84 | 65 |
| CRM | 8 | $268.33 | $273.76 | $2,190.08 | 65 |
| CSCO | 33 | $68.36 | $69.21 | $2,283.93 | 75 |
| CVX | 17 | $146.67 | $147.64 | $2,509.88 | 85 |
| DIS | 20 | $122.97 | $123.81 | $2,476.30 | 85 |
| GOOGL | 13 | $179.40 | $177.75 | $2,310.75 | 75 |
| GS | 3 | $717.52 | $718.39 | $2,155.17 | 75 |
| HD | 6 | $372.64 | $371.09 | $2,226.54 | 65 |
| INTC | 82 | $22.28 | $22.18 | $1,818.76 | 60 |
| JNJ | 13 | $155.80 | $156.07 | $2,028.91 | 65 |
| JPM | 9 | $292.50 | $293.49 | $2,641.41 | 85 |
| KO | 28 | $71.03 | $71.14 | $1,991.92 | 65 |
| LLY | 2 | $776.66 | $765.30 | $1,530.60 | 65 |
| MA | 4 | $563.08 | $565.23 | $2,260.92 | 65 |
| META | 3 | $717.12 | $726.25 | $2,178.76 | 85 |
| MRK | 27 | $82.43 | $81.05 | $2,188.35 | 70 |
| MSFT | 5 | $498.84 | $497.81 | $2,489.07 | 85 |
| NFLX | 1 | $1,279.00 | $1,280.01 | $1,280.01 | 65 |
| NKE | 30 | $75.89 | $76.47 | $2,294.10 | 75 |
| NVDA | 16 | $156.39 | $158.66 | $2,538.48 | 85 |
| ORCL | 10 | $226.66 | $231.67 | $2,316.70 | 75 |
| PEP | 15 | $136.59 | $134.60 | $2,019.07 | 65 |
| PFE | 83 | $25.30 | $25.40 | $2,108.27 | 70 |
| PG | 13 | $160.77 | $160.26 | $2,083.38 | 70 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.85 | 75 |
| QCOM | 14 | $161.69 | $159.12 | $2,227.68 | 75 |
| T | 74 | $28.53 | $28.31 | $2,094.94 | 70 |
| TGT | 19 | $105.09 | $102.86 | $1,954.34 | 65 |
| TSLA | 6 | $288.90 | $294.38 | $1,766.28 | 65 |
| UNH | 7 | $314.75 | $304.17 | $2,129.18 | 65 |
| UNP | 11 | $236.50 | $236.62 | $2,602.88 | 85 |
| V | 6 | $352.90 | $356.14 | $2,136.84 | 70 |
| VZ | 46 | $43.73 | $43.11 | $1,983.06 | 65 |
| WFC | 28 | $82.26 | $82.95 | $2,322.60 | 75 |
| WMT | 23 | $97.34 | $98.05 | $2,255.15 | 75 |
| XOM | 20 | $109.90 | $111.80 | $2,235.90 | 75 |

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
| 2025-07-07 14:25:56 | SELL | INTC | 8 | $22.19 | $-0.68 | 60 |
| 2025-07-07 14:25:56 | SELL | NKE | 2 | $76.39 | $0.95 | 75 |
| 2025-07-07 14:25:56 | SELL | MRK | 2 | $81.06 | $-2.56 | 70 |
| 2025-07-07 14:25:56 | SELL | C | 1 | $88.24 | $1.80 | 70 |
| 2025-07-07 14:25:56 | SELL | WFC | 2 | $82.93 | $1.26 | 75 |
| 2025-07-07 14:25:56 | BUY | WMT | 1 | $98.04 | N/A | 75 |
| 2025-07-07 14:25:56 | BUY | PFE | 4 | $25.41 | N/A | 70 |
| 2025-07-07 14:25:56 | BUY | DIS | 3 | $123.82 | N/A | 85 |
| 2025-07-07 14:25:56 | BUY | T | 3 | $28.31 | N/A | 70 |
| 2025-07-07 14:25:56 | BUY | CVX | 2 | $147.64 | N/A | 85 |
| 2025-07-07 14:09:13 | SELL | MRK | 3 | $81.42 | $-2.49 | 75 |
| 2025-07-07 14:09:13 | SELL | PFE | 11 | $25.48 | $1.80 | 65 |
| 2025-07-07 14:09:13 | SELL | WFC | 1 | $83.07 | $0.74 | 80 |
| 2025-07-07 14:09:13 | SELL | T | 4 | $28.36 | $-0.68 | 65 |
| 2025-07-07 14:09:13 | BUY | WMT | 1 | $97.79 | N/A | 70 |
| 2025-07-07 14:09:13 | BUY | PYPL | 1 | $76.65 | N/A | 75 |
| 2025-07-07 14:09:13 | BUY | NKE | 3 | $76.68 | N/A | 80 |
| 2025-07-07 13:56:10 | SELL | AMD | 1 | $137.91 | $1.99 | 65 |
| 2025-07-07 13:56:10 | SELL | WMT | 1 | $98.00 | $0.68 | 65 |
| 2025-07-07 13:56:10 | BUY | TSLA | 6 | $288.90 | N/A | 65 |
| 2025-07-07 13:56:10 | BUY | NKE | 1 | $76.93 | N/A | 75 |
| 2025-07-07 13:56:10 | BUY | PFE | 10 | $25.44 | N/A | 75 |
| 2025-07-07 13:56:10 | BUY | MRK | 8 | $81.08 | N/A | 85 |
| 2025-07-07 13:56:10 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-07 13:56:10 | BUY | T | 5 | $28.46 | N/A | 70 |

<!--TRADE_LOG_END--> 
