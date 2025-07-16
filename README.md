# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 17:26:06**

| Metric | Value |
|---|---|
| **Total Value** | **$100,611.01** |
| Cash | $1,792.29 |
| Holdings Value | $98,818.73 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.51 | $2,105.10 | 65 |
| ADBE | 6 | $375.23 | $361.92 | $2,171.52 | 65 |
| AMD | 14 | $144.32 | $155.84 | $2,181.76 | 65 |
| AMZN | 10 | $221.65 | $223.05 | $2,230.50 | 75 |
| AVGO | 8 | $275.34 | $279.73 | $2,237.82 | 65 |
| AXP | 6 | $308.37 | $310.33 | $1,861.98 | 65 |
| BA | 9 | $210.81 | $229.44 | $2,064.91 | 65 |
| BAC | 46 | $46.27 | $45.67 | $2,100.82 | 65 |
| C | 30 | $86.85 | $89.57 | $2,687.24 | 85 |
| CAT | 6 | $397.74 | $411.01 | $2,466.09 | 75 |
| COST | 2 | $979.83 | $955.40 | $1,910.80 | 65 |
| CRM | 8 | $267.44 | $256.35 | $2,050.80 | 65 |
| CSCO | 31 | $68.46 | $67.42 | $2,090.17 | 65 |
| CVX | 16 | $146.83 | $150.99 | $2,415.76 | 75 |
| DIS | 18 | $122.77 | $119.72 | $2,154.96 | 65 |
| GOOGL | 13 | $179.34 | $184.05 | $2,392.65 | 75 |
| GS | 3 | $717.52 | $704.99 | $2,114.95 | 70 |
| HD | 5 | $353.54 | $356.65 | $1,783.25 | 65 |
| INTC | 86 | $22.36 | $22.62 | $1,945.32 | 60 |
| JNJ | 13 | $155.43 | $164.56 | $2,139.28 | 65 |
| JPM | 9 | $291.86 | $285.95 | $2,573.59 | 85 |
| KO | 30 | $70.97 | $69.25 | $2,077.35 | 65 |
| LLY | 3 | $781.32 | $791.58 | $2,374.74 | 70 |
| MA | 4 | $563.08 | $552.50 | $2,210.02 | 65 |
| META | 3 | $717.12 | $702.22 | $2,106.66 | 65 |
| MRK | 29 | $82.47 | $82.35 | $2,388.15 | 75 |
| MSFT | 5 | $498.84 | $505.54 | $2,527.70 | 70 |
| NFLX | 1 | $1,279.00 | $1,259.74 | $1,259.74 | 65 |
| NKE | 29 | $72.00 | $71.86 | $2,083.80 | 65 |
| NVDA | 14 | $171.55 | $171.07 | $2,395.05 | 70 |
| ORCL | 9 | $232.99 | $237.69 | $2,139.26 | 65 |
| PEP | 15 | $136.57 | $134.97 | $2,024.48 | 65 |
| PFE | 85 | $25.27 | $24.73 | $2,102.05 | 65 |
| PG | 13 | $152.06 | $153.09 | $1,990.23 | 65 |
| PYPL | 29 | $72.15 | $72.71 | $2,108.59 | 65 |
| QCOM | 14 | $153.83 | $153.57 | $2,149.98 | 65 |
| T | 78 | $27.09 | $27.05 | $2,109.90 | 65 |
| TGT | 20 | $104.94 | $101.30 | $2,026.00 | 65 |
| TSLA | 6 | $318.51 | $321.11 | $1,926.64 | 65 |
| UNH | 7 | $298.51 | $293.91 | $2,057.37 | 65 |
| UNP | 10 | $236.22 | $231.22 | $2,312.25 | 65 |
| V | 6 | $355.85 | $349.19 | $2,095.11 | 65 |
| VZ | 50 | $43.08 | $41.38 | $2,068.75 | 65 |
| WFC | 27 | $78.80 | $79.55 | $2,147.72 | 65 |
| WMT | 22 | $97.29 | $94.85 | $2,086.70 | 65 |
| XOM | 21 | $110.01 | $112.92 | $2,371.22 | 70 |

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
| 2025-07-16 16:44:38 | SELL | NVDA | 1 | $170.57 | $-0.88 | 70 |
| 2025-07-16 16:44:38 | BUY | JPM | 1 | $285.90 | N/A | 85 |
| 2025-07-16 16:27:27 | SELL | BAC | 6 | $45.40 | $-4.57 | 65 |
| 2025-07-16 16:27:27 | SELL | XOM | 1 | $112.82 | $2.82 | 70 |
| 2025-07-16 16:27:27 | BUY | GOOGL | 1 | $183.03 | N/A | 75 |
| 2025-07-16 16:27:27 | BUY | NKE | 2 | $71.71 | N/A | 70 |

<!--TRADE_LOG_END--> 
