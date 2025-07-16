# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 18:11:31**

| Metric | Value |
|---|---|
| **Total Value** | **$100,570.08** |
| Cash | $1,574.97 |
| Holdings Value | $98,995.11 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.97 | $2,099.70 | 65 |
| ADBE | 6 | $375.23 | $361.09 | $2,166.54 | 65 |
| AMD | 15 | $145.03 | $156.47 | $2,347.12 | 70 |
| AMZN | 10 | $221.65 | $223.06 | $2,230.60 | 75 |
| AVGO | 8 | $275.34 | $278.52 | $2,228.16 | 70 |
| AXP | 6 | $308.37 | $311.11 | $1,866.66 | 65 |
| BA | 9 | $210.81 | $229.00 | $2,061.00 | 65 |
| BAC | 46 | $46.27 | $45.71 | $2,102.66 | 65 |
| C | 30 | $86.85 | $89.72 | $2,691.60 | 85 |
| CAT | 6 | $397.74 | $410.80 | $2,464.78 | 85 |
| COST | 2 | $979.83 | $954.76 | $1,909.52 | 65 |
| CRM | 8 | $267.44 | $256.68 | $2,053.44 | 65 |
| CSCO | 31 | $68.46 | $67.27 | $2,085.37 | 65 |
| CVX | 16 | $146.83 | $151.06 | $2,416.96 | 75 |
| DIS | 18 | $122.77 | $119.51 | $2,151.18 | 70 |
| GOOGL | 13 | $179.34 | $183.71 | $2,388.23 | 75 |
| GS | 3 | $717.52 | $705.00 | $2,115.00 | 70 |
| HD | 5 | $353.54 | $356.96 | $1,784.82 | 65 |
| INTC | 85 | $22.36 | $22.50 | $1,912.92 | 60 |
| JNJ | 13 | $155.43 | $164.60 | $2,139.80 | 70 |
| JPM | 9 | $291.86 | $285.08 | $2,565.72 | 75 |
| KO | 30 | $70.97 | $69.33 | $2,079.90 | 65 |
| LLY | 3 | $781.32 | $789.49 | $2,368.47 | 70 |
| MA | 4 | $563.08 | $553.29 | $2,213.16 | 65 |
| META | 3 | $717.12 | $703.17 | $2,109.51 | 65 |
| MRK | 29 | $82.47 | $82.26 | $2,385.51 | 75 |
| MSFT | 5 | $498.84 | $505.06 | $2,525.30 | 70 |
| NFLX | 1 | $1,279.00 | $1,259.16 | $1,259.16 | 65 |
| NKE | 29 | $71.98 | $72.14 | $2,092.06 | 65 |
| NVDA | 15 | $171.49 | $170.69 | $2,560.35 | 85 |
| ORCL | 9 | $232.99 | $238.98 | $2,150.82 | 70 |
| PEP | 15 | $136.57 | $135.10 | $2,026.50 | 65 |
| PFE | 84 | $25.28 | $24.67 | $2,072.28 | 65 |
| PG | 13 | $152.06 | $153.15 | $1,990.89 | 65 |
| PYPL | 29 | $72.15 | $72.74 | $2,109.46 | 65 |
| QCOM | 14 | $153.83 | $153.29 | $2,146.06 | 65 |
| T | 77 | $27.10 | $26.98 | $2,077.08 | 65 |
| TGT | 20 | $104.94 | $101.41 | $2,028.14 | 65 |
| TSLA | 6 | $318.51 | $319.53 | $1,917.18 | 65 |
| UNH | 7 | $298.51 | $293.86 | $2,057.03 | 65 |
| UNP | 10 | $236.22 | $230.92 | $2,309.23 | 65 |
| V | 6 | $355.85 | $349.69 | $2,098.14 | 65 |
| VZ | 50 | $43.08 | $41.31 | $2,065.75 | 65 |
| WFC | 28 | $78.82 | $79.55 | $2,227.40 | 70 |
| WMT | 22 | $97.29 | $94.83 | $2,086.15 | 65 |
| XOM | 20 | $109.86 | $112.89 | $2,257.80 | 70 |

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
| 2025-07-16 18:11:26 | SELL | AMD | 2 | $156.45 | $20.15 | 70 |
| 2025-07-16 18:11:26 | SELL | NKE | 4 | $72.14 | $0.57 | 65 |
| 2025-07-16 18:11:26 | BUY | NVDA | 1 | $170.68 | N/A | 85 |
| 2025-07-16 18:11:26 | BUY | WFC | 1 | $79.57 | N/A | 70 |
| 2025-07-16 17:52:21 | SELL | INTC | 1 | $22.52 | $0.17 | 60 |
| 2025-07-16 17:52:21 | SELL | XOM | 1 | $112.98 | $2.97 | 70 |
| 2025-07-16 17:52:21 | SELL | PFE | 1 | $24.70 | $-0.57 | 65 |
| 2025-07-16 17:52:21 | BUY | AMD | 3 | $155.94 | N/A | 85 |
| 2025-07-16 17:52:21 | BUY | NKE | 4 | $71.99 | N/A | 75 |
| 2025-07-16 17:41:01 | SELL | T | 1 | $27.04 | $-0.05 | 65 |
| 2025-07-16 17:26:01 | SELL | NVDA | 1 | $171.06 | $-0.45 | 70 |
| 2025-07-16 17:26:01 | SELL | ORCL | 1 | $237.70 | $4.24 | 65 |
| 2025-07-16 17:26:01 | SELL | T | 4 | $27.06 | $-0.15 | 65 |
| 2025-07-16 17:26:01 | BUY | INTC | 1 | $22.62 | N/A | 60 |
| 2025-07-16 17:26:01 | BUY | PFE | 1 | $24.72 | N/A | 65 |
| 2025-07-16 17:26:01 | BUY | CVX | 1 | $150.98 | N/A | 75 |
| 2025-07-16 17:10:45 | SELL | NKE | 1 | $72.04 | $0.04 | 65 |
| 2025-07-16 17:10:45 | SELL | PFE | 1 | $24.70 | $-0.57 | 65 |
| 2025-07-16 17:10:45 | SELL | PG | 1 | $153.29 | $1.14 | 60 |
| 2025-07-16 17:10:45 | BUY | NVDA | 2 | $171.34 | N/A | 85 |
| 2025-07-16 17:10:45 | BUY | XOM | 1 | $113.14 | N/A | 75 |
| 2025-07-16 17:10:45 | BUY | UNP | 1 | $231.21 | N/A | 75 |
| 2025-07-16 17:10:45 | BUY | T | 5 | $27.08 | N/A | 70 |
| 2025-07-16 17:10:45 | BUY | ORCL | 1 | $237.66 | N/A | 75 |
| 2025-07-16 16:57:30 | SELL | NVDA | 1 | $171.12 | $-0.39 | 65 |

<!--TRADE_LOG_END--> 
