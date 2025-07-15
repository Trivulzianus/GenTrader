# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 14:41:38**

| Metric | Value |
|---|---|
| **Total Value** | **$100,750.05** |
| Cash | $1,708.25 |
| Holdings Value | $99,041.80 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.59 | $2,095.90 | 70 |
| ADBE | 6 | $375.23 | $364.64 | $2,187.84 | 65 |
| AMD | 15 | $145.66 | $156.51 | $2,347.65 | 70 |
| AMZN | 10 | $221.60 | $226.14 | $2,261.40 | 70 |
| AVGO | 8 | $275.34 | $282.84 | $2,262.72 | 70 |
| AXP | 7 | $325.34 | $313.31 | $2,193.14 | 65 |
| BA | 9 | $210.77 | $230.50 | $2,074.50 | 65 |
| BAC | 44 | $48.83 | $46.62 | $2,051.50 | 65 |
| C | 30 | $86.79 | $89.21 | $2,676.20 | 85 |
| CAT | 6 | $397.74 | $407.29 | $2,443.74 | 85 |
| COST | 2 | $979.83 | $969.37 | $1,938.74 | 65 |
| CRM | 7 | $268.68 | $258.65 | $1,810.55 | 65 |
| CSCO | 31 | $68.46 | $67.47 | $2,091.41 | 65 |
| CVX | 16 | $146.80 | $151.37 | $2,421.92 | 75 |
| DIS | 17 | $122.96 | $119.11 | $2,024.95 | 65 |
| GOOGL | 14 | $179.74 | $183.14 | $2,563.96 | 85 |
| GS | 3 | $717.52 | $707.78 | $2,123.34 | 80 |
| HD | 6 | $372.64 | $364.66 | $2,187.96 | 65 |
| INTC | 88 | $22.39 | $23.41 | $2,060.52 | 65 |
| JNJ | 13 | $155.95 | $155.13 | $2,016.75 | 65 |
| JPM | 9 | $291.63 | $287.51 | $2,587.63 | 85 |
| KO | 29 | $71.03 | $69.27 | $2,008.83 | 65 |
| LLY | 3 | $781.32 | $782.35 | $2,347.05 | 65 |
| MA | 4 | $563.08 | $550.00 | $2,200.02 | 65 |
| META | 3 | $717.12 | $715.00 | $2,145.00 | 65 |
| MRK | 25 | $82.54 | $82.13 | $2,053.25 | 65 |
| MSFT | 5 | $498.84 | $505.08 | $2,525.40 | 85 |
| NFLX | 1 | $1,279.00 | $1,263.35 | $1,263.35 | 65 |
| NKE | 30 | $72.05 | $72.12 | $2,163.60 | 70 |
| NVDA | 15 | $171.71 | $172.03 | $2,580.45 | 85 |
| ORCL | 9 | $233.27 | $232.57 | $2,093.13 | 65 |
| PEP | 15 | $136.57 | $134.34 | $2,015.10 | 65 |
| PFE | 83 | $25.22 | $24.93 | $2,069.19 | 65 |
| PG | 13 | $152.12 | $152.10 | $1,977.36 | 65 |
| PYPL | 29 | $72.19 | $73.43 | $2,129.47 | 65 |
| QCOM | 14 | $153.83 | $154.85 | $2,167.90 | 65 |
| T | 76 | $27.10 | $26.88 | $2,042.71 | 65 |
| TGT | 20 | $104.94 | $103.49 | $2,069.80 | 65 |
| TSLA | 6 | $318.51 | $314.58 | $1,887.50 | 60 |
| UNH | 7 | $298.51 | $294.50 | $2,061.50 | 65 |
| UNP | 9 | $236.56 | $231.97 | $2,087.78 | 65 |
| V | 6 | $355.85 | $347.86 | $2,087.16 | 65 |
| VZ | 50 | $43.08 | $41.20 | $2,059.75 | 65 |
| WFC | 28 | $82.78 | $79.01 | $2,212.28 | 70 |
| WMT | 21 | $97.38 | $94.98 | $1,994.58 | 65 |
| XOM | 21 | $109.99 | $113.20 | $2,377.30 | 75 |

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
| 2025-07-15 14:41:32 | SELL | AMZN | 1 | $226.26 | $4.24 | 70 |
| 2025-07-15 14:41:32 | SELL | PYPL | 3 | $73.44 | $3.40 | 65 |
| 2025-07-15 14:41:32 | SELL | BA | 2 | $230.57 | $32.40 | 65 |
| 2025-07-15 14:41:32 | SELL | CVX | 1 | $151.29 | $4.23 | 75 |
| 2025-07-15 14:41:32 | BUY | NVDA | 15 | $171.71 | N/A | 85 |
| 2025-07-15 14:41:32 | BUY | INTC | 7 | $23.40 | N/A | 65 |
| 2025-07-15 14:41:32 | BUY | XOM | 1 | $113.19 | N/A | 75 |
| 2025-07-15 14:41:32 | BUY | WFC | 2 | $79.06 | N/A | 70 |
| 2025-07-15 14:41:32 | BUY | PG | 13 | $152.12 | N/A | 65 |
| 2025-07-15 14:41:32 | BUY | VZ | 1 | $41.19 | N/A | 65 |
| 2025-07-15 14:40:44 | SELL | PG | 14 | $152.10 | $-114.93 | 65 |
| 2025-07-15 14:40:39 | SELL | NVDA | 13 | $171.71 | $210.41 | 70 |
| 2025-07-15 14:26:51 | SELL | NVDA | 2 | $171.32 | $27.40 | 70 |
| 2025-07-15 14:26:51 | SELL | PFE | 3 | $25.00 | $-0.62 | 65 |
| 2025-07-15 14:26:51 | SELL | MRK | 4 | $82.50 | $-0.13 | 65 |
| 2025-07-15 14:26:51 | BUY | AMZN | 1 | $226.68 | N/A | 85 |
| 2025-07-15 14:26:51 | BUY | PYPL | 4 | $73.54 | N/A | 75 |
| 2025-07-15 14:26:51 | BUY | BA | 1 | $230.60 | N/A | 85 |
| 2025-07-15 14:26:51 | BUY | T | 1 | $26.88 | N/A | 65 |
| 2025-07-15 14:09:14 | SELL | BAC | 3 | $46.58 | $-6.33 | 65 |
| 2025-07-15 14:09:14 | SELL | AMD | 1 | $154.88 | $8.64 | 70 |
| 2025-07-15 14:09:14 | SELL | INTC | 6 | $23.41 | $6.18 | 60 |
| 2025-07-15 14:09:14 | SELL | WFC | 6 | $79.52 | $-17.28 | 65 |
| 2025-07-15 14:09:14 | SELL | CSCO | 1 | $67.51 | $-0.92 | 65 |
| 2025-07-15 14:09:14 | BUY | NVDA | 2 | $170.47 | N/A | 85 |

<!--TRADE_LOG_END--> 
