# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 18:27:27**

| Metric | Value |
|---|---|
| **Total Value** | **$100,577.62** |
| Cash | $1,693.15 |
| Holdings Value | $98,884.47 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.04 | $2,100.45 | 70 |
| ADBE | 6 | $375.23 | $361.27 | $2,167.62 | 65 |
| AMD | 15 | $145.03 | $157.10 | $2,356.50 | 70 |
| AMZN | 10 | $221.65 | $223.07 | $2,230.70 | 75 |
| AVGO | 8 | $275.34 | $279.35 | $2,234.80 | 70 |
| AXP | 6 | $308.37 | $311.19 | $1,867.17 | 65 |
| BA | 9 | $210.81 | $229.10 | $2,061.91 | 65 |
| BAC | 49 | $46.24 | $45.85 | $2,246.89 | 70 |
| C | 30 | $86.85 | $89.87 | $2,696.10 | 85 |
| CAT | 6 | $397.74 | $410.93 | $2,465.58 | 85 |
| COST | 2 | $979.83 | $953.20 | $1,906.40 | 65 |
| CRM | 8 | $267.44 | $256.97 | $2,055.75 | 65 |
| CSCO | 31 | $68.46 | $67.28 | $2,085.84 | 65 |
| CVX | 16 | $146.83 | $150.80 | $2,412.82 | 75 |
| DIS | 18 | $122.77 | $119.52 | $2,151.36 | 65 |
| GOOGL | 13 | $179.34 | $183.95 | $2,391.35 | 75 |
| GS | 3 | $717.52 | $705.54 | $2,116.63 | 70 |
| HD | 5 | $353.54 | $357.26 | $1,786.30 | 65 |
| INTC | 86 | $22.36 | $22.49 | $1,934.14 | 60 |
| JNJ | 13 | $155.43 | $163.94 | $2,131.28 | 65 |
| JPM | 9 | $291.86 | $285.18 | $2,566.62 | 75 |
| KO | 30 | $70.97 | $69.28 | $2,078.25 | 65 |
| LLY | 3 | $781.32 | $788.99 | $2,366.97 | 70 |
| MA | 4 | $563.08 | $553.04 | $2,212.18 | 60 |
| META | 3 | $717.12 | $703.20 | $2,109.59 | 65 |
| MRK | 26 | $82.58 | $82.17 | $2,136.42 | 65 |
| MSFT | 5 | $498.84 | $505.60 | $2,528.00 | 70 |
| NFLX | 1 | $1,279.00 | $1,259.68 | $1,259.68 | 65 |
| NKE | 29 | $71.98 | $72.08 | $2,090.46 | 65 |
| NVDA | 14 | $171.52 | $170.99 | $2,393.83 | 70 |
| ORCL | 9 | $232.99 | $239.53 | $2,155.73 | 65 |
| PEP | 15 | $136.57 | $134.84 | $2,022.67 | 65 |
| PFE | 85 | $25.27 | $24.62 | $2,093.12 | 65 |
| PG | 13 | $152.06 | $153.10 | $1,990.30 | 65 |
| PYPL | 29 | $72.15 | $72.82 | $2,111.78 | 65 |
| QCOM | 14 | $153.83 | $153.31 | $2,146.34 | 65 |
| T | 77 | $27.10 | $26.92 | $2,072.52 | 65 |
| TGT | 20 | $104.94 | $101.42 | $2,028.42 | 65 |
| TSLA | 6 | $318.51 | $319.38 | $1,916.28 | 65 |
| UNH | 7 | $298.51 | $293.48 | $2,054.36 | 65 |
| UNP | 10 | $236.22 | $230.91 | $2,309.13 | 65 |
| V | 6 | $355.85 | $349.58 | $2,097.51 | 65 |
| VZ | 50 | $43.08 | $41.23 | $2,061.75 | 65 |
| WFC | 28 | $78.82 | $79.64 | $2,229.78 | 70 |
| WMT | 22 | $97.29 | $94.82 | $2,086.04 | 65 |
| XOM | 21 | $109.99 | $112.72 | $2,367.12 | 75 |

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
| 2025-07-16 18:27:21 | SELL | NVDA | 1 | $170.99 | $-0.49 | 70 |
| 2025-07-16 18:27:21 | SELL | MRK | 3 | $81.52 | $-2.86 | 65 |
| 2025-07-16 18:27:21 | BUY | BAC | 3 | $45.85 | N/A | 70 |
| 2025-07-16 18:27:21 | BUY | INTC | 1 | $22.50 | N/A | 60 |
| 2025-07-16 18:27:21 | BUY | XOM | 1 | $112.69 | N/A | 75 |
| 2025-07-16 18:27:21 | BUY | PFE | 1 | $24.62 | N/A | 65 |
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

<!--TRADE_LOG_END--> 
