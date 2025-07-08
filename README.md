# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 04:44:50**

| Metric | Value |
|---|---|
| **Total Value** | **$100,771.77** |
| Cash | $1,336.73 |
| Holdings Value | $99,435.04 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.95 | $2,099.50 | 65 |
| ADBE | 5 | $377.60 | $376.93 | $1,884.65 | 65 |
| AMD | 16 | $135.68 | $134.80 | $2,156.80 | 70 |
| AMZN | 11 | $221.72 | $223.47 | $2,458.17 | 85 |
| AVGO | 8 | $275.34 | $274.18 | $2,193.44 | 70 |
| AXP | 7 | $324.46 | $322.73 | $2,259.11 | 75 |
| BA | 10 | $212.15 | $218.63 | $2,186.30 | 70 |
| BAC | 54 | $48.70 | $48.66 | $2,627.64 | 85 |
| C | 30 | $86.58 | $87.60 | $2,628.00 | 85 |
| CAT | 6 | $397.86 | $391.51 | $2,349.06 | 75 |
| COST | 2 | $979.83 | $992.18 | $1,984.36 | 65 |
| CRM | 8 | $268.33 | $269.80 | $2,158.40 | 65 |
| CSCO | 34 | $68.39 | $68.93 | $2,343.62 | 75 |
| CVX | 15 | $146.66 | $147.40 | $2,211.00 | 75 |
| DIS | 17 | $122.84 | $123.16 | $2,093.72 | 65 |
| GOOGL | 12 | $179.60 | $176.79 | $2,121.48 | 70 |
| GS | 3 | $717.52 | $710.93 | $2,132.79 | 85 |
| HD | 6 | $372.64 | $367.64 | $2,205.84 | 65 |
| INTC | 91 | $22.26 | $22.00 | $2,002.00 | 65 |
| JNJ | 13 | $155.80 | $155.27 | $2,018.51 | 65 |
| JPM | 9 | $292.50 | $291.97 | $2,627.73 | 85 |
| KO | 29 | $71.03 | $71.01 | $2,059.29 | 65 |
| LLY | 2 | $776.66 | $772.87 | $1,545.74 | 65 |
| MA | 4 | $563.08 | $565.12 | $2,260.48 | 70 |
| META | 3 | $717.12 | $718.35 | $2,155.05 | 85 |
| MRK | 25 | $82.60 | $80.90 | $2,022.50 | 65 |
| MSFT | 5 | $498.84 | $497.72 | $2,488.60 | 70 |
| NFLX | 1 | $1,279.00 | $1,289.62 | $1,289.62 | 70 |
| NKE | 29 | $75.84 | $76.53 | $2,219.37 | 70 |
| NVDA | 14 | $156.23 | $158.24 | $2,215.36 | 70 |
| ORCL | 9 | $233.41 | $232.26 | $2,090.34 | 70 |
| PEP | 15 | $136.57 | $134.45 | $2,016.75 | 65 |
| PFE | 86 | $25.29 | $25.24 | $2,170.64 | 70 |
| PG | 13 | $160.77 | $160.50 | $2,086.50 | 65 |
| PYPL | 27 | $76.85 | $76.18 | $2,056.86 | 65 |
| QCOM | 15 | $161.50 | $158.09 | $2,371.35 | 75 |
| T | 71 | $28.54 | $28.41 | $2,017.11 | 65 |
| TGT | 20 | $104.90 | $101.60 | $2,032.00 | 65 |
| TSLA | 7 | $289.38 | $293.94 | $2,057.58 | 65 |
| UNH | 7 | $314.75 | $303.71 | $2,125.97 | 65 |
| UNP | 10 | $236.53 | $235.35 | $2,353.50 | 75 |
| V | 6 | $355.95 | $356.64 | $2,139.84 | 70 |
| VZ | 47 | $43.72 | $42.80 | $2,011.60 | 65 |
| WFC | 29 | $82.35 | $82.34 | $2,387.86 | 75 |
| WMT | 22 | $97.30 | $99.35 | $2,185.70 | 70 |
| XOM | 21 | $109.97 | $111.11 | $2,333.31 | 75 |

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
| 2025-07-08 04:44:41 | SELL | WMT | 1 | $99.35 | $1.97 | 70 |
| 2025-07-08 04:44:41 | SELL | NKE | 1 | $76.53 | $0.66 | 70 |
| 2025-07-08 04:44:41 | SELL | PYPL | 1 | $76.18 | $-0.65 | 65 |
| 2025-07-08 04:44:41 | SELL | T | 5 | $28.41 | $-0.63 | 65 |
| 2025-07-08 04:44:41 | BUY | INTC | 6 | $22.00 | N/A | 65 |
| 2025-07-08 04:27:48 | SELL | INTC | 6 | $22.00 | $-1.54 | 60 |
| 2025-07-08 04:27:48 | SELL | BAC | 1 | $48.66 | $-0.04 | 85 |
| 2025-07-08 04:27:48 | BUY | AMD | 1 | $134.80 | N/A | 70 |
| 2025-07-08 04:27:48 | BUY | PYPL | 1 | $76.18 | N/A | 70 |
| 2025-07-08 04:02:08 | SELL | AMD | 1 | $134.80 | $-0.88 | 65 |
| 2025-07-08 04:02:08 | SELL | PFE | 1 | $25.24 | $-0.05 | 70 |
| 2025-07-08 04:02:08 | SELL | MRK | 1 | $80.90 | $-1.63 | 65 |
| 2025-07-08 04:02:08 | BUY | INTC | 13 | $22.00 | N/A | 65 |
| 2025-07-08 04:02:08 | BUY | NKE | 1 | $76.53 | N/A | 75 |
| 2025-07-08 04:02:08 | BUY | T | 4 | $28.41 | N/A | 70 |
| 2025-07-08 03:41:52 | SELL | INTC | 8 | $22.00 | $-2.17 | 55 |
| 2025-07-08 03:41:52 | SELL | PYPL | 1 | $76.18 | $-0.65 | 65 |
| 2025-07-08 03:41:52 | SELL | CVX | 1 | $147.40 | $0.70 | 70 |
| 2025-07-08 03:15:15 | SELL | INTC | 7 | $22.00 | $-1.76 | 60 |
| 2025-07-08 03:15:15 | BUY | C | 4 | $87.60 | N/A | 85 |
| 2025-07-08 02:42:11 | SELL | GOOGL | 1 | $176.79 | $-2.59 | 65 |
| 2025-07-08 02:42:11 | SELL | C | 4 | $87.60 | $4.09 | 70 |
| 2025-07-08 02:42:11 | SELL | ORCL | 1 | $232.26 | $-1.03 | 65 |
| 2025-07-08 02:42:11 | BUY | BAC | 1 | $48.66 | N/A | 85 |
| 2025-07-08 02:42:11 | BUY | INTC | 1 | $22.00 | N/A | 65 |

<!--TRADE_LOG_END--> 
