# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 17:26:23**

| Metric | Value |
|---|---|
| **Total Value** | **$101,239.20** |
| Cash | $599.75 |
| Holdings Value | $100,639.45 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.97 | $2,109.75 | 65 |
| ADBE | 6 | $375.23 | $365.48 | $2,192.86 | 65 |
| AMD | 14 | $160.03 | $159.24 | $2,229.36 | 70 |
| AMZN | 10 | $221.65 | $223.68 | $2,236.75 | 75 |
| AVGO | 8 | $275.34 | $287.39 | $2,299.16 | 65 |
| AXP | 7 | $309.18 | $313.88 | $2,197.16 | 70 |
| BA | 9 | $210.81 | $228.78 | $2,059.02 | 70 |
| BAC | 45 | $46.25 | $46.78 | $2,105.32 | 65 |
| C | 30 | $86.85 | $92.41 | $2,772.30 | 85 |
| CAT | 6 | $397.74 | $416.82 | $2,500.89 | 75 |
| COST | 2 | $979.83 | $951.41 | $1,902.82 | 65 |
| CRM | 8 | $267.44 | $259.04 | $2,072.28 | 65 |
| CSCO | 33 | $68.56 | $68.18 | $2,249.94 | 70 |
| CVX | 16 | $146.82 | $150.19 | $2,403.04 | 75 |
| DIS | 22 | $122.51 | $121.73 | $2,678.06 | 85 |
| GOOGL | 13 | $179.34 | $182.75 | $2,375.68 | 75 |
| GS | 3 | $717.52 | $707.94 | $2,123.82 | 85 |
| HD | 6 | $354.18 | $357.25 | $2,143.50 | 65 |
| INTC | 84 | $22.34 | $22.92 | $1,925.12 | 60 |
| JNJ | 13 | $155.43 | $163.22 | $2,121.92 | 65 |
| JPM | 9 | $291.90 | $287.40 | $2,586.60 | 80 |
| KO | 30 | $70.97 | $69.77 | $2,092.95 | 65 |
| LLY | 3 | $781.32 | $765.89 | $2,297.67 | 65 |
| MA | 4 | $563.08 | $553.91 | $2,215.64 | 65 |
| META | 3 | $717.12 | $700.86 | $2,102.58 | 70 |
| MRK | 29 | $82.56 | $81.45 | $2,362.05 | 75 |
| MSFT | 5 | $498.84 | $512.65 | $2,563.25 | 85 |
| NFLX | 1 | $1,279.00 | $1,266.15 | $1,266.15 | 65 |
| NKE | 29 | $71.88 | $72.97 | $2,115.99 | 65 |
| NVDA | 13 | $171.56 | $173.70 | $2,258.16 | 70 |
| ORCL | 9 | $232.91 | $247.57 | $2,228.13 | 70 |
| PEP | 16 | $136.49 | $144.71 | $2,315.36 | 70 |
| PFE | 84 | $25.28 | $24.55 | $2,062.62 | 65 |
| PG | 14 | $152.18 | $154.72 | $2,166.08 | 65 |
| PYPL | 28 | $72.12 | $73.56 | $2,059.68 | 65 |
| QCOM | 14 | $153.83 | $152.98 | $2,141.72 | 65 |
| T | 77 | $27.09 | $26.90 | $2,071.12 | 65 |
| TGT | 20 | $104.83 | $103.45 | $2,069.00 | 65 |
| TSLA | 6 | $318.51 | $321.06 | $1,926.37 | 60 |
| UNH | 7 | $298.51 | $288.34 | $2,018.38 | 65 |
| UNP | 10 | $236.33 | $227.88 | $2,278.80 | 65 |
| V | 6 | $355.85 | $349.98 | $2,099.85 | 65 |
| VZ | 50 | $40.87 | $40.92 | $2,046.00 | 65 |
| WFC | 27 | $78.74 | $79.90 | $2,157.30 | 70 |
| WMT | 22 | $97.29 | $95.19 | $2,094.27 | 65 |
| XOM | 21 | $109.97 | $111.67 | $2,344.97 | 75 |

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
| 2025-07-17 17:26:16 | SELL | NKE | 1 | $72.96 | $1.05 | 65 |
| 2025-07-17 17:26:16 | SELL | CSCO | 2 | $68.18 | $-0.70 | 70 |
| 2025-07-17 17:26:16 | SELL | T | 1 | $26.90 | $-0.20 | 65 |
| 2025-07-17 17:26:16 | BUY | XOM | 2 | $111.64 | N/A | 75 |
| 2025-07-17 17:09:24 | SELL | NVDA | 2 | $173.65 | $3.62 | 70 |
| 2025-07-17 17:09:24 | SELL | XOM | 2 | $111.69 | $3.43 | 65 |
| 2025-07-17 17:09:24 | SELL | T | 5 | $26.86 | $-1.09 | 65 |
| 2025-07-17 17:09:24 | BUY | WFC | 1 | $80.10 | N/A | 70 |
| 2025-07-17 17:09:24 | BUY | CSCO | 4 | $68.19 | N/A | 75 |
| 2025-07-17 16:56:39 | SELL | INTC | 6 | $22.99 | $3.60 | 60 |
| 2025-07-17 16:56:39 | SELL | CSCO | 1 | $68.29 | $-0.29 | 65 |
| 2025-07-17 16:56:39 | BUY | NVDA | 2 | $173.66 | N/A | 85 |
| 2025-07-17 16:56:39 | BUY | NKE | 1 | $73.01 | N/A | 70 |
| 2025-07-17 16:56:39 | BUY | VZ | 50 | $40.87 | N/A | 65 |
| 2025-07-17 16:56:39 | BUY | T | 6 | $26.84 | N/A | 70 |
| 2025-07-17 16:56:16 | SELL | VZ | 51 | $40.86 | $-111.01 | 65 |
| 2025-07-17 16:44:33 | SELL | NKE | 2 | $73.14 | $2.38 | 65 |
| 2025-07-17 16:44:33 | SELL | WFC | 2 | $80.17 | $2.74 | 65 |
| 2025-07-17 16:44:33 | BUY | XOM | 2 | $111.66 | N/A | 75 |
| 2025-07-17 16:44:33 | BUY | INTC | 6 | $22.92 | N/A | 65 |
| 2025-07-17 16:27:10 | SELL | NVDA | 2 | $174.01 | $4.26 | 70 |
| 2025-07-17 16:27:10 | SELL | BAC | 3 | $46.61 | $1.01 | 65 |
| 2025-07-17 16:27:10 | SELL | INTC | 6 | $22.94 | $3.32 | 60 |
| 2025-07-17 16:27:10 | SELL | XOM | 2 | $111.70 | $3.44 | 65 |
| 2025-07-17 16:27:10 | SELL | NKE | 1 | $72.97 | $0.98 | 70 |

<!--TRADE_LOG_END--> 
