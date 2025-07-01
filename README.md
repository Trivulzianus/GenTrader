# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 14:04:34**

| Metric | Value |
|---|---|
| **Total Value** | **$100,372.19** |
| Cash | $1,531.23 |
| Holdings Value | $98,840.96 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $209.10 | $2,509.15 | 85 |
| ADBE | 5 | $385.76 | $381.76 | $1,908.80 | 65 |
| AMD | 17 | $142.22 | $137.95 | $2,345.15 | 75 |
| AMZN | 11 | $226.76 | $219.12 | $2,410.38 | 85 |
| AVGO | 9 | $275.08 | $271.62 | $2,444.53 | 85 |
| AXP | 7 | $316.33 | $319.28 | $2,234.96 | 65 |
| BA | 10 | $214.55 | $210.88 | $2,108.85 | 65 |
| BAC | 41 | $47.19 | $47.53 | $1,948.73 | 65 |
| C | 23 | $84.14 | $85.16 | $1,958.57 | 65 |
| CAT | 5 | $381.20 | $386.05 | $1,930.25 | 65 |
| COST | 2 | $991.47 | $985.11 | $1,970.22 | 65 |
| CRM | 9 | $274.67 | $273.21 | $2,458.89 | 85 |
| CSCO | 32 | $68.96 | $69.03 | $2,209.12 | 75 |
| CVX | 13 | $143.34 | $143.10 | $1,860.36 | 65 |
| DIS | 16 | $122.90 | $123.34 | $1,973.44 | 65 |
| GS | 3 | $706.65 | $708.81 | $2,126.43 | 75 |
| HD | 7 | $369.90 | $367.79 | $2,574.53 | 85 |
| INTC | 88 | $22.34 | $22.41 | $1,971.64 | 65 |
| JNJ | 13 | $151.96 | $153.63 | $1,997.23 | 65 |
| JPM | 7 | $285.02 | $290.54 | $2,033.78 | 65 |
| KO | 27 | $70.44 | $71.41 | $1,927.93 | 65 |
| LLY | 3 | $767.33 | $781.98 | $2,345.94 | 75 |
| MA | 4 | $537.87 | $561.08 | $2,244.32 | 65 |
| META | 3 | $712.71 | $733.35 | $2,200.05 | 90 |
| MRK | 32 | $79.04 | $79.36 | $2,539.52 | 85 |
| MSFT | 4 | $492.89 | $496.51 | $1,986.04 | 65 |
| NFLX | 1 | $1,334.07 | $1,333.22 | $1,333.22 | 65 |
| NKE | 35 | $71.14 | $73.11 | $2,558.68 | 85 |
| NVDA | 13 | $157.47 | $155.91 | $2,026.83 | 65 |
| ORCL | 9 | $219.56 | $222.04 | $1,998.36 | 65 |
| PEP | 17 | $131.85 | $133.12 | $2,263.04 | 75 |
| PFE | 92 | $24.27 | $24.49 | $2,253.08 | 75 |
| PG | 12 | $159.73 | $159.80 | $1,917.57 | 65 |
| PYPL | 34 | $73.92 | $74.20 | $2,522.80 | 85 |
| QCOM | 16 | $159.24 | $158.19 | $2,530.96 | 85 |
| T | 89 | $28.54 | $28.92 | $2,573.88 | 85 |
| TGT | 23 | $98.82 | $100.42 | $2,309.78 | 75 |
| TSLA | 7 | $294.26 | $304.16 | $2,129.11 | 75 |
| UNH | 8 | $306.63 | $316.11 | $2,528.84 | 85 |
| UNP | 11 | $232.22 | $230.96 | $2,540.54 | 85 |
| V | 6 | $344.95 | $353.24 | $2,119.41 | 65 |
| VZ | 45 | $42.64 | $43.33 | $1,949.63 | 65 |
| WFC | 32 | $79.91 | $80.44 | $2,573.92 | 85 |
| WMT | 26 | $97.15 | $98.44 | $2,559.31 | 85 |
| XOM | 18 | $109.40 | $107.40 | $1,933.20 | 65 |

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
| 2025-07-01 13:32:56 | SELL | KO | 1 | $71.43 | $0.95 | 65 |
| 2025-07-01 13:32:56 | SELL | C | 3 | $85.26 | $2.96 | 65 |
| 2025-07-01 13:32:56 | SELL | CSCO | 1 | $69.48 | $0.54 | 65 |
| 2025-07-01 13:32:56 | SELL | VZ | 1 | $43.39 | $0.73 | 65 |
| 2025-07-01 13:32:56 | SELL | T | 1 | $29.07 | $0.53 | 85 |

<!--TRADE_LOG_END--> 
