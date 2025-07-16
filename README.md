# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 17:52:28**

| Metric | Value |
|---|---|
| **Total Value** | **$100,572.90** |
| Cash | $1,223.76 |
| Holdings Value | $99,349.14 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.25 | $2,102.50 | 65 |
| ADBE | 6 | $375.23 | $361.71 | $2,170.26 | 65 |
| AMD | 17 | $146.37 | $155.94 | $2,650.89 | 85 |
| AMZN | 10 | $221.65 | $222.89 | $2,228.90 | 75 |
| AVGO | 8 | $275.34 | $278.90 | $2,231.20 | 70 |
| AXP | 6 | $308.37 | $310.54 | $1,863.24 | 65 |
| BA | 9 | $210.81 | $229.61 | $2,066.49 | 70 |
| BAC | 46 | $46.27 | $45.63 | $2,099.21 | 65 |
| C | 30 | $86.85 | $89.75 | $2,692.35 | 85 |
| CAT | 6 | $397.74 | $410.41 | $2,462.46 | 85 |
| COST | 2 | $979.83 | $955.57 | $1,911.14 | 65 |
| CRM | 8 | $267.44 | $256.58 | $2,052.68 | 65 |
| CSCO | 31 | $68.46 | $67.31 | $2,086.46 | 65 |
| CVX | 16 | $146.83 | $151.09 | $2,417.52 | 80 |
| DIS | 18 | $122.77 | $119.56 | $2,152.08 | 65 |
| GOOGL | 13 | $179.34 | $183.88 | $2,390.44 | 75 |
| GS | 3 | $717.52 | $703.31 | $2,109.94 | 70 |
| HD | 5 | $353.54 | $356.60 | $1,783.02 | 65 |
| INTC | 85 | $22.36 | $22.52 | $1,913.90 | 60 |
| JNJ | 13 | $155.43 | $164.58 | $2,139.54 | 70 |
| JPM | 9 | $291.86 | $285.38 | $2,568.42 | 85 |
| KO | 30 | $70.97 | $69.32 | $2,079.60 | 65 |
| LLY | 3 | $781.32 | $790.48 | $2,371.44 | 70 |
| MA | 4 | $563.08 | $553.08 | $2,212.32 | 65 |
| META | 3 | $717.12 | $704.86 | $2,114.58 | 65 |
| MRK | 29 | $82.47 | $82.33 | $2,387.71 | 75 |
| MSFT | 5 | $498.84 | $505.19 | $2,525.95 | 70 |
| NFLX | 1 | $1,279.00 | $1,255.62 | $1,255.62 | 60 |
| NKE | 33 | $72.00 | $71.94 | $2,374.18 | 75 |
| NVDA | 14 | $171.55 | $170.79 | $2,391.06 | 70 |
| ORCL | 9 | $232.99 | $238.35 | $2,145.15 | 65 |
| PEP | 15 | $136.57 | $134.95 | $2,024.25 | 65 |
| PFE | 84 | $25.28 | $24.71 | $2,075.37 | 65 |
| PG | 13 | $152.06 | $153.08 | $1,990.04 | 65 |
| PYPL | 29 | $72.15 | $72.69 | $2,108.01 | 65 |
| QCOM | 14 | $153.83 | $153.41 | $2,147.74 | 65 |
| T | 77 | $27.10 | $27.00 | $2,079.38 | 65 |
| TGT | 20 | $104.94 | $101.25 | $2,025.00 | 65 |
| TSLA | 6 | $318.51 | $320.64 | $1,923.84 | 65 |
| UNH | 7 | $298.51 | $294.04 | $2,058.28 | 65 |
| UNP | 10 | $236.22 | $231.12 | $2,311.25 | 75 |
| V | 6 | $355.85 | $349.35 | $2,096.10 | 65 |
| VZ | 50 | $43.08 | $41.31 | $2,065.75 | 65 |
| WFC | 27 | $78.80 | $79.51 | $2,146.77 | 70 |
| WMT | 22 | $97.29 | $94.88 | $2,087.36 | 65 |
| XOM | 20 | $109.86 | $112.99 | $2,259.73 | 70 |

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
| 2025-07-16 16:57:30 | SELL | AMD | 1 | $155.31 | $10.25 | 65 |
| 2025-07-16 16:57:30 | SELL | NKE | 1 | $71.62 | $-0.37 | 65 |
| 2025-07-16 16:57:30 | SELL | CVX | 1 | $150.95 | $4.13 | 70 |
| 2025-07-16 16:57:30 | BUY | PFE | 1 | $24.68 | N/A | 65 |

<!--TRADE_LOG_END--> 
