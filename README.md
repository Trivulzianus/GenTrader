# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 20:51:43**

| Metric | Value |
|---|---|
| **Total Value** | **$100,771.77** |
| Cash | $1,282.15 |
| Holdings Value | $99,489.62 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.95 | $2,099.50 | 70 |
| ADBE | 5 | $377.60 | $376.93 | $1,884.65 | 65 |
| AMD | 16 | $135.68 | $134.80 | $2,156.80 | 70 |
| AMZN | 11 | $221.72 | $223.47 | $2,458.17 | 85 |
| AVGO | 8 | $275.34 | $274.18 | $2,193.44 | 65 |
| AXP | 7 | $324.46 | $322.73 | $2,259.11 | 70 |
| BA | 10 | $212.15 | $218.63 | $2,186.30 | 70 |
| BAC | 54 | $48.70 | $48.66 | $2,627.64 | 85 |
| C | 25 | $86.37 | $87.60 | $2,190.00 | 70 |
| CAT | 6 | $397.86 | $391.51 | $2,349.06 | 85 |
| COST | 2 | $979.83 | $992.18 | $1,984.36 | 65 |
| CRM | 8 | $268.33 | $269.80 | $2,158.40 | 65 |
| CSCO | 32 | $68.36 | $68.93 | $2,205.76 | 70 |
| CVX | 16 | $146.70 | $147.40 | $2,358.40 | 75 |
| DIS | 17 | $122.84 | $123.16 | $2,093.72 | 65 |
| GOOGL | 13 | $179.38 | $176.79 | $2,298.27 | 70 |
| GS | 3 | $717.52 | $710.93 | $2,132.79 | 70 |
| HD | 6 | $372.64 | $367.64 | $2,205.84 | 65 |
| INTC | 85 | $22.27 | $22.00 | $1,870.00 | 60 |
| JNJ | 13 | $155.80 | $155.27 | $2,018.51 | 65 |
| JPM | 9 | $292.50 | $291.97 | $2,627.73 | 85 |
| KO | 29 | $71.03 | $71.01 | $2,059.29 | 65 |
| LLY | 2 | $776.66 | $772.87 | $1,545.74 | 65 |
| MA | 4 | $563.08 | $565.12 | $2,260.48 | 65 |
| META | 3 | $717.12 | $718.35 | $2,155.05 | 85 |
| MRK | 26 | $82.53 | $80.90 | $2,103.40 | 70 |
| MSFT | 5 | $498.84 | $497.72 | $2,488.60 | 70 |
| NFLX | 1 | $1,279.00 | $1,289.62 | $1,289.62 | 65 |
| NKE | 32 | $75.91 | $76.53 | $2,448.96 | 80 |
| NVDA | 14 | $156.23 | $158.24 | $2,215.36 | 70 |
| ORCL | 9 | $233.41 | $232.26 | $2,090.34 | 70 |
| PEP | 15 | $136.57 | $134.45 | $2,016.75 | 65 |
| PFE | 86 | $25.29 | $25.24 | $2,170.64 | 70 |
| PG | 13 | $160.77 | $160.50 | $2,086.50 | 65 |
| PYPL | 27 | $76.85 | $76.18 | $2,056.86 | 65 |
| QCOM | 15 | $161.50 | $158.09 | $2,371.35 | 75 |
| T | 72 | $28.54 | $28.41 | $2,045.52 | 65 |
| TGT | 20 | $104.90 | $101.60 | $2,032.00 | 65 |
| TSLA | 7 | $289.38 | $293.94 | $2,057.58 | 65 |
| UNH | 7 | $314.75 | $303.71 | $2,125.97 | 65 |
| UNP | 10 | $236.53 | $235.35 | $2,353.50 | 75 |
| V | 6 | $355.95 | $356.64 | $2,139.84 | 70 |
| VZ | 47 | $43.72 | $42.80 | $2,011.60 | 65 |
| WFC | 29 | $82.35 | $82.34 | $2,387.86 | 75 |
| WMT | 23 | $97.38 | $99.35 | $2,285.05 | 75 |
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
| 2025-07-07 20:51:37 | SELL | UNP | 1 | $235.35 | $-1.08 | 75 |
| 2025-07-07 20:51:37 | SELL | CSCO | 1 | $68.93 | $0.56 | 70 |
| 2025-07-07 20:51:37 | BUY | NKE | 2 | $76.53 | N/A | 80 |
| 2025-07-07 20:51:37 | BUY | MRK | 1 | $80.90 | N/A | 70 |
| 2025-07-07 20:51:37 | BUY | VZ | 3 | $42.80 | N/A | 65 |
| 2025-07-07 20:39:48 | SELL | AAPL | 1 | $209.95 | $-1.02 | 65 |
| 2025-07-07 20:39:48 | SELL | ORCL | 1 | $232.26 | $-1.03 | 65 |
| 2025-07-07 20:39:48 | SELL | VZ | 3 | $42.80 | $-2.75 | 60 |
| 2025-07-07 20:39:48 | SELL | C | 5 | $87.60 | $5.11 | 70 |
| 2025-07-07 20:39:48 | SELL | T | 4 | $28.41 | $-0.50 | 65 |
| 2025-07-07 20:39:48 | BUY | AMD | 1 | $134.80 | N/A | 70 |
| 2025-07-07 20:39:48 | BUY | XOM | 1 | $111.11 | N/A | 75 |
| 2025-07-07 20:39:48 | BUY | PFE | 1 | $25.24 | N/A | 70 |
| 2025-07-07 20:39:48 | BUY | CSCO | 1 | $68.93 | N/A | 75 |
| 2025-07-07 20:26:21 | SELL | MRK | 3 | $80.90 | $-4.55 | 65 |
| 2025-07-07 20:26:21 | SELL | PYPL | 2 | $76.18 | $-1.26 | 65 |
| 2025-07-07 20:26:21 | BUY | NKE | 1 | $76.53 | N/A | 75 |
| 2025-07-07 20:26:21 | BUY | UNP | 1 | $235.35 | N/A | 85 |
| 2025-07-07 20:26:21 | BUY | T | 5 | $28.41 | N/A | 70 |
| 2025-07-07 20:09:18 | SELL | DIS | 1 | $123.18 | $0.32 | 65 |
| 2025-07-07 20:09:18 | SELL | NKE | 5 | $76.56 | $3.04 | 70 |
| 2025-07-07 20:09:18 | SELL | PYPL | 2 | $76.18 | $-1.17 | 70 |
| 2025-07-07 20:09:18 | SELL | WFC | 2 | $82.33 | $-0.04 | 75 |
| 2025-07-07 20:09:18 | SELL | UNP | 1 | $235.35 | $-1.08 | 75 |
| 2025-07-07 20:09:18 | BUY | AAPL | 1 | $209.95 | N/A | 75 |

<!--TRADE_LOG_END--> 
