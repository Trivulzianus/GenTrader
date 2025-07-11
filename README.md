# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 22:26:05**

| Metric | Value |
|---|---|
| **Total Value** | **$100,744.85** |
| Cash | $1,358.44 |
| Holdings Value | $99,386.41 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.27 | $211.16 | $2,322.76 | 70 |
| ADBE | 5 | $377.60 | $363.35 | $1,816.75 | 65 |
| AMD | 15 | $134.63 | $146.42 | $2,196.30 | 70 |
| AMZN | 11 | $221.97 | $225.02 | $2,475.22 | 85 |
| AVGO | 8 | $275.34 | $274.38 | $2,195.04 | 70 |
| AXP | 7 | $325.34 | $319.47 | $2,236.29 | 75 |
| BA | 10 | $212.59 | $226.84 | $2,268.40 | 70 |
| BAC | 47 | $48.70 | $46.73 | $2,196.31 | 70 |
| C | 26 | $86.65 | $86.73 | $2,254.98 | 70 |
| CAT | 6 | $397.98 | $405.92 | $2,435.52 | 70 |
| COST | 2 | $979.83 | $970.33 | $1,940.66 | 65 |
| CRM | 7 | $268.68 | $258.07 | $1,806.49 | 65 |
| CSCO | 32 | $68.41 | $67.95 | $2,174.40 | 70 |
| CVX | 16 | $146.66 | $155.31 | $2,484.96 | 75 |
| DIS | 18 | $122.80 | $119.87 | $2,157.66 | 70 |
| GOOGL | 13 | $179.61 | $180.19 | $2,342.47 | 75 |
| GS | 3 | $717.52 | $704.95 | $2,114.85 | 65 |
| HD | 6 | $372.64 | $370.07 | $2,220.42 | 65 |
| INTC | 81 | $22.29 | $23.43 | $1,897.83 | 60 |
| JNJ | 13 | $155.89 | $156.90 | $2,039.70 | 65 |
| JPM | 8 | $292.23 | $286.86 | $2,294.88 | 75 |
| KO | 29 | $71.03 | $69.87 | $2,026.23 | 65 |
| LLY | 3 | $781.32 | $793.01 | $2,379.03 | 70 |
| MA | 4 | $563.08 | $550.18 | $2,200.72 | 65 |
| META | 3 | $717.12 | $717.51 | $2,152.53 | 75 |
| MRK | 27 | $82.37 | $83.36 | $2,250.72 | 70 |
| MSFT | 5 | $498.84 | $503.32 | $2,516.60 | 85 |
| NFLX | 1 | $1,279.00 | $1,245.11 | $1,245.11 | 65 |
| NKE | 32 | $75.67 | $72.63 | $2,324.16 | 75 |
| NVDA | 16 | $157.38 | $164.92 | $2,638.72 | 85 |
| ORCL | 9 | $233.26 | $230.56 | $2,075.04 | 70 |
| PEP | 15 | $136.57 | $135.26 | $2,028.90 | 65 |
| PFE | 80 | $25.18 | $25.65 | $2,052.00 | 65 |
| PG | 13 | $160.78 | $157.05 | $2,041.65 | 65 |
| PYPL | 28 | $72.13 | $71.36 | $1,998.08 | 65 |
| QCOM | 13 | $162.18 | $157.46 | $2,046.98 | 65 |
| T | 76 | $27.11 | $26.97 | $2,049.72 | 65 |
| TGT | 20 | $104.91 | $104.24 | $2,084.80 | 65 |
| TSLA | 6 | $288.62 | $313.51 | $1,881.06 | 60 |
| UNH | 7 | $298.51 | $304.10 | $2,128.70 | 65 |
| UNP | 10 | $236.18 | $235.10 | $2,351.00 | 75 |
| V | 6 | $355.85 | $347.93 | $2,087.58 | 65 |
| VZ | 49 | $43.12 | $41.62 | $2,039.38 | 65 |
| WFC | 29 | $82.28 | $82.55 | $2,393.95 | 75 |
| WMT | 21 | $97.38 | $94.40 | $1,982.40 | 65 |
| XOM | 22 | $110.24 | $115.43 | $2,539.46 | 80 |

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
| 2025-07-11 22:25:59 | SELL | INTC | 6 | $23.43 | $6.39 | 60 |
| 2025-07-11 22:25:59 | SELL | XOM | 1 | $115.43 | $4.97 | 80 |
| 2025-07-11 22:25:59 | SELL | PFE | 5 | $25.65 | $2.22 | 65 |
| 2025-07-11 22:25:59 | SELL | C | 1 | $86.73 | $0.08 | 70 |
| 2025-07-11 22:25:59 | SELL | CVX | 1 | $155.31 | $8.15 | 75 |
| 2025-07-11 22:25:59 | BUY | CSCO | 2 | $67.95 | N/A | 70 |
| 2025-07-11 22:08:26 | SELL | MRK | 1 | $83.36 | $0.95 | 70 |
| 2025-07-11 22:08:26 | SELL | CSCO | 2 | $67.95 | $-0.92 | 65 |
| 2025-07-11 22:08:26 | BUY | CVX | 1 | $155.31 | N/A | 85 |
| 2025-07-11 21:50:49 | SELL | BAC | 1 | $46.73 | $-1.93 | 70 |
| 2025-07-11 21:50:49 | SELL | PG | 1 | $157.05 | $-3.47 | 65 |
| 2025-07-11 21:50:49 | SELL | T | 1 | $26.97 | $-0.13 | 65 |
| 2025-07-11 21:50:49 | BUY | XOM | 2 | $115.43 | N/A | 85 |
| 2025-07-11 21:50:49 | BUY | MRK | 2 | $83.36 | N/A | 75 |
| 2025-07-11 21:50:49 | BUY | PFE | 4 | $25.65 | N/A | 70 |
| 2025-07-11 21:50:49 | BUY | C | 1 | $86.73 | N/A | 75 |
| 2025-07-11 21:37:21 | SELL | BAC | 2 | $46.73 | $-3.71 | 70 |
| 2025-07-11 21:37:21 | SELL | PFE | 4 | $25.65 | $1.78 | 65 |
| 2025-07-11 21:37:21 | SELL | T | 4 | $26.97 | $-0.51 | 65 |
| 2025-07-11 21:37:21 | SELL | CVX | 1 | $155.31 | $8.15 | 75 |
| 2025-07-11 21:37:21 | BUY | INTC | 1 | $23.43 | N/A | 65 |
| 2025-07-11 21:37:21 | BUY | PG | 1 | $157.05 | N/A | 70 |
| 2025-07-11 21:37:21 | BUY | VZ | 3 | $41.62 | N/A | 65 |
| 2025-07-11 21:26:03 | SELL | C | 4 | $86.73 | $0.27 | 70 |
| 2025-07-11 21:26:03 | SELL | VZ | 3 | $41.62 | $-4.49 | 60 |

<!--TRADE_LOG_END--> 
