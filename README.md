# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 17:10:51**

| Metric | Value |
|---|---|
| **Total Value** | **$100,599.56** |
| Cash | $1,473.62 |
| Holdings Value | $99,125.94 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.74 | $2,107.39 | 65 |
| ADBE | 6 | $375.23 | $361.74 | $2,170.44 | 65 |
| AMD | 14 | $144.32 | $155.46 | $2,176.43 | 70 |
| AMZN | 10 | $221.65 | $223.45 | $2,234.50 | 75 |
| AVGO | 8 | $275.34 | $279.14 | $2,233.14 | 70 |
| AXP | 6 | $308.37 | $310.48 | $1,862.88 | 65 |
| BA | 9 | $210.81 | $228.94 | $2,060.51 | 65 |
| BAC | 46 | $46.27 | $45.64 | $2,099.44 | 65 |
| C | 30 | $86.85 | $89.46 | $2,683.80 | 85 |
| CAT | 6 | $397.74 | $410.36 | $2,462.16 | 85 |
| COST | 2 | $979.83 | $955.72 | $1,911.43 | 65 |
| CRM | 8 | $267.44 | $256.48 | $2,051.84 | 65 |
| CSCO | 31 | $68.46 | $67.45 | $2,090.95 | 65 |
| CVX | 15 | $146.55 | $151.20 | $2,268.00 | 75 |
| DIS | 18 | $122.77 | $119.78 | $2,156.04 | 70 |
| GOOGL | 13 | $179.34 | $183.97 | $2,391.67 | 75 |
| GS | 3 | $717.52 | $705.50 | $2,116.50 | 75 |
| HD | 5 | $353.54 | $356.59 | $1,782.94 | 65 |
| INTC | 85 | $22.36 | $22.64 | $1,923.98 | 60 |
| JNJ | 13 | $155.43 | $164.62 | $2,140.06 | 65 |
| JPM | 9 | $291.86 | $286.26 | $2,576.34 | 75 |
| KO | 30 | $70.97 | $69.24 | $2,077.20 | 65 |
| LLY | 3 | $781.32 | $788.98 | $2,366.93 | 70 |
| MA | 4 | $563.08 | $552.54 | $2,210.16 | 65 |
| META | 3 | $717.12 | $703.35 | $2,110.03 | 70 |
| MRK | 29 | $82.47 | $82.05 | $2,379.45 | 75 |
| MSFT | 5 | $498.84 | $505.32 | $2,526.62 | 70 |
| NFLX | 1 | $1,279.00 | $1,259.56 | $1,259.56 | 65 |
| NKE | 29 | $72.00 | $72.06 | $2,089.60 | 65 |
| NVDA | 15 | $171.51 | $171.29 | $2,569.42 | 85 |
| ORCL | 10 | $233.46 | $237.60 | $2,376.03 | 75 |
| PEP | 15 | $136.57 | $134.87 | $2,023.05 | 65 |
| PFE | 84 | $25.28 | $24.69 | $2,073.96 | 65 |
| PG | 13 | $152.06 | $153.28 | $1,992.64 | 60 |
| PYPL | 29 | $72.15 | $72.70 | $2,108.30 | 65 |
| QCOM | 14 | $153.83 | $153.66 | $2,151.31 | 65 |
| T | 82 | $27.09 | $27.08 | $2,220.96 | 70 |
| TGT | 20 | $104.94 | $101.19 | $2,023.70 | 65 |
| TSLA | 6 | $318.51 | $320.81 | $1,924.86 | 65 |
| UNH | 7 | $298.51 | $293.47 | $2,054.29 | 65 |
| UNP | 10 | $236.22 | $231.25 | $2,312.45 | 75 |
| V | 6 | $355.85 | $349.13 | $2,094.78 | 65 |
| VZ | 50 | $43.08 | $41.38 | $2,069.01 | 65 |
| WFC | 27 | $78.80 | $79.47 | $2,145.69 | 70 |
| WMT | 22 | $97.29 | $94.98 | $2,089.67 | 65 |
| XOM | 21 | $110.01 | $113.14 | $2,375.84 | 75 |

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
| 2025-07-16 16:44:38 | SELL | NVDA | 1 | $170.57 | $-0.88 | 70 |
| 2025-07-16 16:44:38 | BUY | JPM | 1 | $285.90 | N/A | 85 |
| 2025-07-16 16:27:27 | SELL | BAC | 6 | $45.40 | $-4.57 | 65 |
| 2025-07-16 16:27:27 | SELL | XOM | 1 | $112.82 | $2.82 | 70 |
| 2025-07-16 16:27:27 | BUY | GOOGL | 1 | $183.03 | N/A | 75 |
| 2025-07-16 16:27:27 | BUY | NKE | 2 | $71.71 | N/A | 70 |
| 2025-07-16 16:27:27 | BUY | C | 1 | $89.26 | N/A | 85 |
| 2025-07-16 16:10:20 | SELL | GOOGL | 1 | $183.52 | $4.15 | 65 |
| 2025-07-16 16:10:20 | SELL | INTC | 1 | $22.47 | $0.11 | 60 |
| 2025-07-16 16:10:20 | SELL | NKE | 2 | $71.78 | $-0.42 | 65 |
| 2025-07-16 16:10:20 | SELL | WFC | 1 | $78.95 | $0.15 | 65 |
| 2025-07-16 16:10:20 | BUY | NVDA | 2 | $170.34 | N/A | 85 |

<!--TRADE_LOG_END--> 
