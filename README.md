# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 15:09:02**

| Metric | Value |
|---|---|
| **Total Value** | **$100,520.37** |
| Cash | $1,551.96 |
| Holdings Value | $98,968.41 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.62 | $2,106.20 | 65 |
| ADBE | 6 | $375.23 | $361.41 | $2,168.46 | 65 |
| AMD | 14 | $144.36 | $154.79 | $2,167.06 | 65 |
| AMZN | 10 | $221.65 | $225.34 | $2,253.45 | 75 |
| AVGO | 8 | $275.34 | $278.62 | $2,228.96 | 70 |
| AXP | 7 | $325.34 | $310.24 | $2,171.68 | 65 |
| BA | 9 | $210.81 | $229.46 | $2,065.14 | 65 |
| BAC | 45 | $46.28 | $45.45 | $2,045.47 | 65 |
| C | 27 | $86.47 | $89.64 | $2,420.14 | 75 |
| CAT | 6 | $397.74 | $407.54 | $2,445.24 | 85 |
| COST | 2 | $979.83 | $960.12 | $1,920.24 | 65 |
| CRM | 8 | $267.44 | $257.13 | $2,057.04 | 65 |
| CSCO | 31 | $68.46 | $67.42 | $2,090.17 | 65 |
| CVX | 16 | $146.76 | $150.02 | $2,400.32 | 75 |
| DIS | 18 | $122.77 | $119.75 | $2,155.55 | 65 |
| GOOGL | 13 | $179.38 | $183.94 | $2,391.22 | 75 |
| GS | 3 | $717.52 | $699.30 | $2,097.90 | 85 |
| HD | 6 | $372.64 | $357.30 | $2,143.80 | 65 |
| INTC | 84 | $22.36 | $22.57 | $1,896.30 | 60 |
| JNJ | 13 | $155.43 | $164.49 | $2,138.37 | 65 |
| JPM | 9 | $291.63 | $285.89 | $2,573.05 | 85 |
| KO | 30 | $70.97 | $69.22 | $2,076.75 | 65 |
| LLY | 3 | $781.32 | $794.83 | $2,384.49 | 70 |
| MA | 4 | $563.08 | $553.70 | $2,214.80 | 65 |
| META | 3 | $717.12 | $707.86 | $2,123.58 | 75 |
| MRK | 29 | $82.47 | $82.47 | $2,391.49 | 75 |
| MSFT | 5 | $498.84 | $504.98 | $2,524.90 | 70 |
| NFLX | 1 | $1,279.00 | $1,263.64 | $1,263.64 | 65 |
| NKE | 29 | $72.03 | $71.88 | $2,084.52 | 65 |
| NVDA | 15 | $171.48 | $170.12 | $2,551.83 | 85 |
| ORCL | 9 | $233.10 | $235.09 | $2,115.76 | 70 |
| PEP | 15 | $136.57 | $134.56 | $2,018.40 | 65 |
| PFE | 83 | $25.29 | $24.86 | $2,063.80 | 65 |
| PG | 14 | $152.15 | $152.98 | $2,141.72 | 65 |
| PYPL | 29 | $72.15 | $72.24 | $2,094.86 | 65 |
| QCOM | 14 | $153.83 | $153.29 | $2,146.08 | 65 |
| T | 77 | $27.09 | $27.00 | $2,079.38 | 65 |
| TGT | 20 | $104.94 | $101.44 | $2,028.80 | 65 |
| TSLA | 6 | $318.51 | $319.61 | $1,917.66 | 65 |
| UNH | 7 | $298.51 | $293.53 | $2,054.71 | 65 |
| UNP | 9 | $236.78 | $231.38 | $2,082.42 | 65 |
| V | 6 | $355.85 | $348.68 | $2,092.05 | 70 |
| VZ | 50 | $43.08 | $41.34 | $2,066.75 | 65 |
| WFC | 26 | $78.81 | $79.08 | $2,056.08 | 65 |
| WMT | 22 | $97.29 | $95.31 | $2,096.82 | 65 |
| XOM | 21 | $109.99 | $112.44 | $2,361.34 | 75 |

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
| 2025-07-16 15:08:56 | SELL | GOOGL | 1 | $184.08 | $4.37 | 75 |
| 2025-07-16 15:08:56 | SELL | C | 3 | $89.61 | $8.46 | 75 |
| 2025-07-16 15:08:56 | BUY | NVDA | 1 | $170.18 | N/A | 85 |
| 2025-07-16 14:52:56 | SELL | ORCL | 1 | $234.96 | $1.68 | 65 |
| 2025-07-16 14:52:56 | BUY | XOM | 1 | $112.65 | N/A | 75 |
| 2025-07-16 14:40:59 | SELL | NVDA | 1 | $170.23 | $-1.26 | 70 |
| 2025-07-16 14:40:59 | BUY | ORCL | 1 | $234.45 | N/A | 75 |
| 2025-07-16 14:26:09 | SELL | XOM | 1 | $112.84 | $2.84 | 70 |
| 2025-07-16 14:26:09 | SELL | NKE | 1 | $72.13 | $0.10 | 65 |
| 2025-07-16 14:26:09 | BUY | NVDA | 1 | $169.74 | N/A | 85 |
| 2025-07-16 14:08:31 | SELL | INTC | 7 | $22.69 | $2.16 | 60 |
| 2025-07-16 14:08:31 | SELL | AMD | 1 | $154.68 | $9.64 | 65 |
| 2025-07-16 14:08:31 | SELL | PFE | 1 | $24.86 | $-0.42 | 65 |
| 2025-07-16 14:08:31 | SELL | WFC | 1 | $79.43 | $0.60 | 65 |
| 2025-07-16 14:08:31 | SELL | UNP | 1 | $230.54 | $-5.61 | 65 |
| 2025-07-16 14:08:31 | BUY | XOM | 1 | $112.48 | N/A | 75 |
| 2025-07-16 14:08:31 | BUY | NKE | 1 | $72.00 | N/A | 70 |
| 2025-07-16 13:50:09 | SELL | NVDA | 1 | $170.74 | $-0.81 | 70 |
| 2025-07-16 13:50:09 | SELL | JNJ | 1 | $161.91 | $6.02 | 65 |
| 2025-07-16 13:50:09 | SELL | XOM | 1 | $112.87 | $2.85 | 70 |
| 2025-07-16 13:50:09 | SELL | PFE | 1 | $24.92 | $-0.36 | 65 |
| 2025-07-16 13:50:09 | SELL | BA | 1 | $230.91 | $18.09 | 65 |
| 2025-07-16 13:50:09 | SELL | WFC | 3 | $79.46 | $1.71 | 65 |
| 2025-07-16 13:50:09 | SELL | CVX | 1 | $150.89 | $3.88 | 75 |
| 2025-07-16 13:50:09 | BUY | INTC | 7 | $22.65 | N/A | 65 |

<!--TRADE_LOG_END--> 
