# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 13:29:07**

| Metric | Value |
|---|---|
| **Total Value** | **$100,771.77** |
| Cash | $1,860.37 |
| Holdings Value | $98,911.40 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.95 | $2,099.50 | 70 |
| ADBE | 5 | $377.60 | $376.93 | $1,884.65 | 65 |
| AMD | 16 | $135.68 | $134.80 | $2,156.80 | 70 |
| AMZN | 11 | $221.72 | $223.47 | $2,458.17 | 85 |
| AVGO | 8 | $275.34 | $274.18 | $2,193.44 | 70 |
| AXP | 8 | $324.24 | $322.73 | $2,581.84 | 85 |
| BA | 10 | $212.15 | $218.63 | $2,186.30 | 65 |
| BAC | 48 | $48.71 | $48.66 | $2,335.68 | 75 |
| C | 30 | $86.58 | $87.60 | $2,628.00 | 85 |
| CAT | 6 | $397.86 | $391.51 | $2,349.06 | 70 |
| COST | 2 | $979.83 | $992.18 | $1,984.36 | 65 |
| CRM | 8 | $268.33 | $269.80 | $2,158.40 | 65 |
| CSCO | 34 | $68.39 | $68.93 | $2,343.62 | 75 |
| CVX | 16 | $146.70 | $147.40 | $2,358.40 | 75 |
| DIS | 17 | $122.84 | $123.16 | $2,093.72 | 65 |
| GOOGL | 12 | $179.60 | $176.79 | $2,121.48 | 70 |
| GS | 3 | $717.52 | $710.93 | $2,132.79 | 85 |
| HD | 6 | $372.64 | $367.64 | $2,205.84 | 70 |
| INTC | 86 | $22.27 | $22.00 | $1,892.00 | 60 |
| JNJ | 13 | $155.80 | $155.27 | $2,018.51 | 65 |
| JPM | 8 | $292.56 | $291.97 | $2,335.76 | 75 |
| KO | 29 | $71.03 | $71.01 | $2,059.29 | 65 |
| LLY | 2 | $776.66 | $772.87 | $1,545.74 | 65 |
| MA | 4 | $563.08 | $565.12 | $2,260.48 | 65 |
| META | 3 | $717.12 | $718.35 | $2,155.05 | 70 |
| MRK | 26 | $82.53 | $80.90 | $2,103.40 | 65 |
| MSFT | 5 | $498.84 | $497.72 | $2,488.60 | 70 |
| NFLX | 1 | $1,279.00 | $1,289.62 | $1,289.62 | 65 |
| NKE | 30 | $75.87 | $76.53 | $2,295.90 | 75 |
| NVDA | 13 | $156.08 | $158.24 | $2,057.12 | 70 |
| ORCL | 9 | $233.41 | $232.26 | $2,090.34 | 70 |
| PEP | 15 | $136.57 | $134.45 | $2,016.75 | 65 |
| PFE | 87 | $25.29 | $25.24 | $2,195.88 | 70 |
| PG | 13 | $160.77 | $160.50 | $2,086.50 | 65 |
| PYPL | 27 | $76.85 | $76.18 | $2,056.86 | 65 |
| QCOM | 14 | $161.75 | $158.09 | $2,213.26 | 75 |
| T | 72 | $28.54 | $28.41 | $2,045.52 | 65 |
| TGT | 20 | $104.90 | $101.60 | $2,032.00 | 65 |
| TSLA | 6 | $288.62 | $293.94 | $1,763.64 | 65 |
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
| 2025-07-08 13:29:02 | SELL | TGT | 1 | $101.60 | $-3.15 | 65 |
| 2025-07-08 13:29:02 | SELL | T | 5 | $28.41 | $-0.62 | 65 |
| 2025-07-08 13:29:02 | BUY | BAC | 2 | $48.66 | N/A | 75 |
| 2025-07-08 13:29:02 | BUY | NKE | 1 | $76.53 | N/A | 75 |
| 2025-07-08 13:03:18 | SELL | BAC | 3 | $48.66 | $-0.14 | 70 |
| 2025-07-08 13:03:18 | SELL | NKE | 1 | $76.53 | $0.66 | 70 |
| 2025-07-08 13:03:18 | SELL | QCOM | 1 | $158.09 | $-3.41 | 70 |
| 2025-07-08 13:03:18 | BUY | BA | 1 | $218.63 | N/A | 70 |
| 2025-07-08 13:03:18 | BUY | T | 5 | $28.41 | N/A | 70 |
| 2025-07-08 12:32:02 | SELL | BA | 1 | $218.63 | $6.48 | 60 |
| 2025-07-08 12:32:02 | SELL | T | 5 | $28.41 | $-0.62 | 65 |
| 2025-07-08 12:32:02 | BUY | NKE | 1 | $76.53 | N/A | 75 |
| 2025-07-08 12:13:58 | SELL | PYPL | 1 | $76.18 | $-0.65 | 65 |
| 2025-07-08 12:13:58 | SELL | MRK | 1 | $80.90 | $-1.57 | 65 |
| 2025-07-08 12:13:58 | BUY | C | 4 | $87.60 | N/A | 85 |
| 2025-07-08 11:50:06 | SELL | BAC | 2 | $48.66 | $-0.09 | 75 |
| 2025-07-08 11:50:06 | SELL | C | 3 | $87.60 | $3.17 | 70 |
| 2025-07-08 11:50:06 | SELL | WFC | 1 | $82.34 | $-0.01 | 75 |
| 2025-07-08 11:50:06 | BUY | MRK | 2 | $80.90 | N/A | 70 |
| 2025-07-08 11:50:06 | BUY | PYPL | 3 | $76.18 | N/A | 70 |
| 2025-07-08 11:50:06 | BUY | TGT | 1 | $101.60 | N/A | 70 |
| 2025-07-08 11:37:02 | SELL | PYPL | 3 | $76.18 | $-1.95 | 60 |
| 2025-07-08 11:37:02 | SELL | NKE | 1 | $76.53 | $0.66 | 70 |
| 2025-07-08 11:37:02 | SELL | C | 1 | $87.60 | $1.02 | 80 |
| 2025-07-08 11:37:02 | BUY | BAC | 3 | $48.66 | N/A | 80 |

<!--TRADE_LOG_END--> 
