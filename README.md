# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 16:32:08**

| Metric | Value |
|---|---|
| **Total Value** | **$101,121.87** |
| Cash | $286.15 |
| Holdings Value | $100,835.72 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.88 | $2,494.62 | 85 |
| ADBE | 5 | $385.76 | $391.75 | $1,958.75 | 65 |
| AMD | 17 | $140.89 | $137.21 | $2,332.57 | 85 |
| AMZN | 11 | $226.78 | $219.19 | $2,411.09 | 85 |
| AVGO | 7 | $274.91 | $267.08 | $1,869.56 | 85 |
| AXP | 6 | $315.94 | $321.88 | $1,931.28 | 65 |
| BA | 9 | $215.30 | $209.92 | $1,889.27 | 65 |
| BAC | 51 | $47.30 | $48.11 | $2,453.67 | 85 |
| C | 22 | $84.08 | $85.73 | $1,886.06 | 65 |
| CAT | 5 | $381.20 | $393.87 | $1,969.35 | 65 |
| COST | 2 | $991.47 | $979.02 | $1,958.04 | 75 |
| CRM | 8 | $274.83 | $273.06 | $2,184.48 | 85 |
| CSCO | 27 | $68.88 | $68.83 | $1,858.54 | 85 |
| CVX | 16 | $143.73 | $146.13 | $2,338.08 | 85 |
| DIS | 16 | $122.90 | $122.83 | $1,965.28 | 65 |
| GOOGL | 14 | $175.62 | $174.40 | $2,441.60 | 85 |
| GS | 3 | $706.65 | $707.39 | $2,122.17 | 75 |
| HD | 7 | $369.90 | $377.96 | $2,645.72 | 85 |
| INTC | 95 | $22.32 | $23.14 | $2,197.83 | 75 |
| JNJ | 12 | $151.63 | $156.35 | $1,876.20 | 65 |
| JPM | 7 | $285.02 | $289.17 | $2,024.19 | 65 |
| KO | 26 | $70.42 | $71.72 | $1,864.59 | 65 |
| LLY | 3 | $767.33 | $782.70 | $2,348.10 | 65 |
| MA | 4 | $537.87 | $561.49 | $2,245.96 | 65 |
| META | 3 | $712.71 | $715.88 | $2,147.64 | 85 |
| MRK | 30 | $79.35 | $82.41 | $2,472.30 | 85 |
| MSFT | 4 | $492.89 | $491.87 | $1,967.48 | 85 |
| NFLX | 1 | $1,334.07 | $1,286.80 | $1,286.80 | 85 |
| NKE | 33 | $70.93 | $73.45 | $2,423.85 | 85 |
| NVDA | 16 | $154.76 | $153.50 | $2,456.08 | 85 |
| ORCL | 9 | $219.56 | $219.17 | $1,972.53 | 65 |
| PEP | 16 | $131.60 | $135.68 | $2,170.88 | 75 |
| PFE | 96 | $24.28 | $25.17 | $2,416.31 | 85 |
| PG | 12 | $159.73 | $161.21 | $1,934.46 | 65 |
| PYPL | 32 | $73.86 | $75.42 | $2,413.60 | 85 |
| QCOM | 15 | $159.12 | $160.99 | $2,414.85 | 85 |
| T | 84 | $28.52 | $28.73 | $2,413.74 | 85 |
| TGT | 21 | $98.42 | $104.98 | $2,204.58 | 75 |
| TSLA | 7 | $290.03 | $303.49 | $2,124.45 | 75 |
| UNH | 8 | $306.63 | $324.51 | $2,596.06 | 85 |
| UNP | 11 | $232.22 | $236.49 | $2,601.39 | 85 |
| V | 6 | $344.95 | $353.83 | $2,122.98 | 65 |
| VZ | 49 | $42.71 | $43.66 | $2,139.59 | 75 |
| WFC | 30 | $79.85 | $81.14 | $2,434.35 | 85 |
| WMT | 25 | $97.07 | $97.92 | $2,448.00 | 85 |
| XOM | 22 | $109.35 | $109.40 | $2,406.80 | 85 |

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
| 2025-07-01 16:32:02 | SELL | JNJ | 1 | $156.45 | $4.44 | 65 |
| 2025-07-01 16:32:02 | SELL | PYPL | 1 | $75.43 | $1.52 | 85 |
| 2025-07-01 16:32:02 | SELL | NKE | 1 | $73.48 | $2.47 | 85 |
| 2025-07-01 16:32:02 | SELL | PFE | 1 | $25.17 | $0.89 | 85 |
| 2025-07-01 16:32:02 | SELL | KO | 3 | $71.72 | $3.51 | 65 |
| 2025-07-01 16:32:02 | SELL | WFC | 1 | $81.15 | $1.26 | 85 |
| 2025-07-01 16:32:02 | SELL | QCOM | 1 | $161.04 | $1.79 | 85 |
| 2025-07-01 16:32:02 | SELL | VZ | 1 | $43.66 | $0.93 | 75 |
| 2025-07-01 16:32:02 | SELL | T | 1 | $28.73 | $0.21 | 85 |
| 2025-07-01 16:32:02 | BUY | TSLA | 1 | $303.60 | N/A | 75 |
| 2025-07-01 16:32:02 | BUY | INTC | 14 | $22.40 | N/A | 75 |
| 2025-07-01 16:17:47 | SELL | AVGO | 2 | $275.65 | $1.15 | 65 |
| 2025-07-01 16:17:47 | BUY | JNJ | 1 | $157.22 | N/A | 75 |
| 2025-07-01 16:17:47 | BUY | AMD | 2 | $136.79 | N/A | 85 |
| 2025-07-01 16:17:47 | BUY | XOM | 2 | $109.36 | N/A | 85 |
| 2025-07-01 16:04:41 | SELL | XOM | 2 | $109.26 | $-0.15 | 75 |
| 2025-07-01 16:04:41 | SELL | C | 1 | $85.52 | $1.38 | 65 |
| 2025-07-01 16:04:41 | BUY | AMD | 1 | $136.23 | N/A | 75 |
| 2025-07-01 16:04:41 | BUY | KO | 3 | $72.08 | N/A | 75 |
| 2025-07-01 15:55:25 | SELL | TSLA | 1 | $317.66 | $25.62 | 65 |
| 2025-07-01 15:55:25 | SELL | AMD | 2 | $141.90 | $0.16 | 65 |
| 2025-07-01 15:55:25 | SELL | KO | 3 | $72.08 | $4.60 | 65 |
| 2025-07-01 15:55:25 | SELL | C | 5 | $85.07 | $3.83 | 65 |
| 2025-07-01 15:55:25 | SELL | CSCO | 1 | $69.38 | $0.48 | 65 |
| 2025-07-01 15:55:25 | BUY | NVDA | 4 | $152.91 | N/A | 85 |

<!--TRADE_LOG_END--> 
