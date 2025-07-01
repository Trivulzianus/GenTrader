# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 14:16:52**

| Metric | Value |
|---|---|
| **Total Value** | **$100,555.94** |
| Cash | $25.02 |
| Holdings Value | $100,530.93 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $209.62 | $2,515.44 | 85 |
| ADBE | 5 | $385.76 | $385.35 | $1,926.75 | 65 |
| AMD | 15 | $142.70 | $138.72 | $2,080.80 | 65 |
| AMZN | 9 | $228.40 | $220.45 | $1,984.05 | 65 |
| AVGO | 9 | $275.08 | $271.02 | $2,439.18 | 85 |
| AXP | 7 | $316.33 | $319.87 | $2,239.06 | 75 |
| BA | 10 | $214.55 | $210.54 | $2,105.40 | 65 |
| BAC | 41 | $47.19 | $47.55 | $1,949.35 | 65 |
| C | 23 | $84.14 | $85.38 | $1,963.62 | 75 |
| CAT | 5 | $381.20 | $388.30 | $1,941.50 | 65 |
| COST | 2 | $991.47 | $985.83 | $1,971.65 | 65 |
| CRM | 9 | $274.67 | $273.58 | $2,462.26 | 85 |
| CSCO | 29 | $68.93 | $69.17 | $2,006.07 | 65 |
| CVX | 13 | $143.34 | $143.40 | $1,864.14 | 65 |
| DIS | 16 | $122.90 | $123.44 | $1,975.04 | 65 |
| GOOGL | 14 | $175.62 | $175.49 | $2,456.86 | 85 |
| GS | 3 | $706.65 | $709.89 | $2,129.68 | 65 |
| HD | 7 | $369.90 | $368.83 | $2,581.81 | 85 |
| INTC | 88 | $22.34 | $22.47 | $1,977.26 | 75 |
| JNJ | 13 | $151.96 | $153.88 | $2,000.44 | 65 |
| JPM | 7 | $285.02 | $289.93 | $2,029.51 | 65 |
| KO | 27 | $70.44 | $71.44 | $1,928.75 | 65 |
| LLY | 3 | $767.33 | $780.48 | $2,341.44 | 65 |
| MA | 4 | $537.87 | $559.86 | $2,239.44 | 65 |
| META | 3 | $712.71 | $735.75 | $2,207.24 | 88 |
| MRK | 32 | $79.04 | $79.59 | $2,546.96 | 85 |
| MSFT | 4 | $492.89 | $497.71 | $1,990.84 | 65 |
| NFLX | 1 | $1,334.07 | $1,330.52 | $1,330.52 | 65 |
| NKE | 35 | $71.14 | $73.71 | $2,579.85 | 85 |
| NVDA | 13 | $157.47 | $156.24 | $2,031.14 | 65 |
| ORCL | 9 | $219.56 | $220.18 | $1,981.58 | 65 |
| PEP | 17 | $131.85 | $133.25 | $2,265.25 | 75 |
| PFE | 92 | $24.27 | $24.54 | $2,257.82 | 85 |
| PG | 12 | $159.73 | $160.05 | $1,920.60 | 65 |
| PYPL | 34 | $73.92 | $74.43 | $2,530.58 | 85 |
| QCOM | 16 | $159.24 | $158.85 | $2,541.60 | 85 |
| T | 88 | $28.54 | $28.88 | $2,541.00 | 85 |
| TGT | 23 | $98.82 | $101.61 | $2,337.03 | 75 |
| TSLA | 7 | $294.26 | $304.13 | $2,128.91 | 65 |
| UNH | 8 | $306.63 | $318.90 | $2,551.20 | 85 |
| UNP | 11 | $232.22 | $231.12 | $2,542.32 | 85 |
| V | 6 | $344.95 | $352.86 | $2,117.16 | 65 |
| VZ | 45 | $42.64 | $43.27 | $1,946.92 | 65 |
| WFC | 32 | $79.91 | $80.46 | $2,574.72 | 85 |
| WMT | 26 | $97.15 | $98.61 | $2,563.73 | 85 |
| XOM | 18 | $109.40 | $107.47 | $1,934.46 | 65 |

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
| 2025-07-01 14:16:46 | SELL | AMZN | 2 | $219.39 | $-14.74 | 65 |
| 2025-07-01 14:16:46 | SELL | AMD | 2 | $138.58 | $-7.27 | 65 |
| 2025-07-01 14:16:46 | SELL | CSCO | 3 | $69.19 | $0.71 | 65 |
| 2025-07-01 14:16:46 | SELL | T | 1 | $28.94 | $0.40 | 85 |
| 2025-07-01 14:16:46 | BUY | GOOGL | 14 | $175.62 | N/A | 85 |
| 2025-07-01 14:04:27 | SELL | GOOGL | 15 | $174.57 | $-63.50 | 85 |
| 2025-07-01 14:04:27 | SELL | AMD | 1 | $137.95 | $-4.03 | 75 |
| 2025-07-01 14:04:27 | BUY | INTC | 2 | $22.39 | N/A | 65 |
| 2025-07-01 14:04:27 | BUY | HD | 1 | $367.84 | N/A | 85 |
| 2025-07-01 14:04:27 | BUY | PFE | 1 | $24.50 | N/A | 75 |
| 2025-07-01 14:04:27 | BUY | MRK | 1 | $79.33 | N/A | 85 |
| 2025-07-01 14:04:27 | BUY | CSCO | 3 | $69.07 | N/A | 75 |
| 2025-07-01 14:04:27 | BUY | AVGO | 2 | $271.46 | N/A | 85 |
| 2025-07-01 14:04:27 | BUY | T | 2 | $28.92 | N/A | 85 |
| 2025-07-01 13:56:40 | SELL | NVDA | 3 | $157.99 | $1.26 | 65 |
| 2025-07-01 13:56:40 | SELL | CSCO | 2 | $69.16 | $0.41 | 65 |
| 2025-07-01 13:56:40 | BUY | AMD | 2 | $138.12 | N/A | 85 |
| 2025-07-01 13:56:40 | BUY | MRK | 6 | $79.47 | N/A | 85 |
| 2025-07-01 13:48:54 | SELL | AMD | 1 | $138.81 | $-3.44 | 75 |
| 2025-07-01 13:48:54 | SELL | PFE | 1 | $24.38 | $0.12 | 75 |
| 2025-07-01 13:48:54 | SELL | MRK | 3 | $79.07 | $0.37 | 65 |
| 2025-07-01 13:48:54 | BUY | CSCO | 3 | $69.38 | N/A | 75 |
| 2025-07-01 13:32:56 | SELL | INTC | 14 | $22.52 | $2.16 | 65 |
| 2025-07-01 13:32:56 | SELL | PFE | 1 | $24.32 | $0.05 | 75 |
| 2025-07-01 13:32:56 | SELL | NKE | 1 | $72.47 | $1.29 | 85 |

<!--TRADE_LOG_END--> 
