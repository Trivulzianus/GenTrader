# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 17:40:56**

| Metric | Value |
|---|---|
| **Total Value** | **$101,136.30** |
| Cash | $45.48 |
| Holdings Value | $101,090.82 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.01 | $2,496.12 | 85 |
| ADBE | 5 | $385.76 | $391.22 | $1,956.10 | 75 |
| AMD | 17 | $140.02 | $137.05 | $2,329.90 | 85 |
| AMZN | 11 | $226.78 | $220.69 | $2,427.59 | 85 |
| AVGO | 9 | $272.95 | $265.67 | $2,390.99 | 85 |
| AXP | 6 | $315.94 | $323.96 | $1,943.76 | 65 |
| BA | 9 | $215.30 | $210.22 | $1,891.98 | 65 |
| BAC | 51 | $47.30 | $48.19 | $2,457.69 | 85 |
| C | 22 | $84.03 | $86.36 | $1,899.81 | 65 |
| CAT | 5 | $381.20 | $391.89 | $1,959.45 | 65 |
| COST | 2 | $991.47 | $985.17 | $1,970.34 | 65 |
| CRM | 8 | $274.90 | $273.59 | $2,188.72 | 85 |
| CSCO | 27 | $68.84 | $69.08 | $1,865.16 | 65 |
| CVX | 17 | $143.81 | $145.75 | $2,477.75 | 85 |
| DIS | 16 | $122.87 | $123.53 | $1,976.48 | 65 |
| GOOGL | 14 | $175.62 | $175.31 | $2,454.36 | 85 |
| GS | 3 | $706.65 | $708.07 | $2,124.21 | 65 |
| HD | 7 | $369.90 | $375.76 | $2,630.32 | 85 |
| INTC | 81 | $22.22 | $22.95 | $1,859.35 | 65 |
| JNJ | 12 | $151.63 | $155.39 | $1,864.68 | 65 |
| JPM | 7 | $285.02 | $290.02 | $2,030.17 | 65 |
| KO | 26 | $70.42 | $71.61 | $1,861.99 | 65 |
| LLY | 3 | $767.33 | $779.49 | $2,338.46 | 65 |
| MA | 4 | $537.87 | $565.05 | $2,260.20 | 75 |
| META | 3 | $712.71 | $720.36 | $2,161.08 | 90 |
| MRK | 30 | $79.35 | $81.88 | $2,456.25 | 85 |
| MSFT | 4 | $492.89 | $492.73 | $1,970.92 | 85 |
| NFLX | 1 | $1,334.07 | $1,296.81 | $1,296.81 | 85 |
| NKE | 33 | $70.93 | $73.09 | $2,412.13 | 85 |
| NVDA | 15 | $153.89 | $154.34 | $2,315.18 | 85 |
| ORCL | 9 | $219.56 | $219.68 | $1,977.12 | 65 |
| PEP | 16 | $131.60 | $134.75 | $2,156.00 | 75 |
| PFE | 98 | $24.29 | $25.01 | $2,450.51 | 85 |
| PG | 12 | $159.73 | $160.84 | $1,930.14 | 65 |
| PYPL | 32 | $73.86 | $75.52 | $2,416.64 | 85 |
| QCOM | 15 | $159.12 | $160.21 | $2,403.15 | 85 |
| T | 85 | $28.52 | $28.81 | $2,448.84 | 85 |
| TGT | 23 | $98.92 | $104.23 | $2,397.29 | 85 |
| TSLA | 7 | $290.03 | $301.50 | $2,110.47 | 75 |
| UNH | 8 | $306.63 | $322.44 | $2,579.48 | 85 |
| UNP | 11 | $232.22 | $235.47 | $2,590.22 | 85 |
| V | 6 | $344.95 | $356.15 | $2,136.90 | 65 |
| VZ | 49 | $42.71 | $43.66 | $2,139.59 | 75 |
| WFC | 30 | $79.85 | $81.40 | $2,442.00 | 85 |
| WMT | 25 | $97.07 | $98.30 | $2,457.62 | 85 |
| XOM | 20 | $109.38 | $109.34 | $2,186.90 | 75 |

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
| 2025-07-01 17:40:46 | SELL | XOM | 2 | $109.32 | $-0.11 | 75 |
| 2025-07-01 17:40:46 | SELL | INTC | 1 | $22.98 | $0.75 | 65 |
| 2025-07-01 17:40:46 | SELL | PFE | 1 | $25.00 | $0.69 | 85 |
| 2025-07-01 17:40:46 | SELL | CSCO | 1 | $69.07 | $0.22 | 65 |
| 2025-07-01 17:40:46 | BUY | VZ | 5 | $43.67 | N/A | 75 |
| 2025-07-01 17:40:46 | BUY | TGT | 2 | $104.20 | N/A | 85 |
| 2025-07-01 17:30:00 | SELL | INTC | 1 | $23.02 | $0.79 | 65 |
| 2025-07-01 17:30:00 | SELL | CSCO | 4 | $69.02 | $0.61 | 65 |
| 2025-07-01 17:30:00 | SELL | VZ | 6 | $43.63 | $5.43 | 65 |
| 2025-07-01 17:30:00 | BUY | AMD | 1 | $137.02 | N/A | 85 |
| 2025-07-01 17:30:00 | BUY | AVGO | 2 | $266.08 | N/A | 85 |
| 2025-07-01 17:17:09 | SELL | C | 3 | $86.17 | $5.64 | 65 |
| 2025-07-01 17:17:09 | BUY | XOM | 4 | $108.92 | N/A | 85 |
| 2025-07-01 17:06:51 | SELL | AMD | 1 | $137.57 | $-2.48 | 75 |
| 2025-07-01 17:06:51 | SELL | DIS | 4 | $123.20 | $1.06 | 65 |
| 2025-07-01 17:06:51 | SELL | CSCO | 3 | $68.96 | $0.23 | 75 |
| 2025-07-01 17:06:51 | BUY | NVDA | 3 | $154.74 | N/A | 85 |
| 2025-07-01 17:06:51 | BUY | C | 3 | $85.82 | N/A | 75 |
| 2025-07-01 16:57:52 | SELL | NVDA | 4 | $157.99 | $12.93 | 65 |
| 2025-07-01 16:57:52 | SELL | CRM | 1 | $272.54 | $-2.10 | 75 |
| 2025-07-01 16:57:52 | BUY | AMD | 3 | $137.14 | N/A | 85 |
| 2025-07-01 16:57:52 | BUY | DIS | 4 | $123.06 | N/A | 85 |
| 2025-07-01 16:48:11 | SELL | AMD | 3 | $141.90 | $3.02 | 65 |
| 2025-07-01 16:48:11 | SELL | XOM | 4 | $108.77 | $-2.32 | 65 |
| 2025-07-01 16:48:11 | SELL | INTC | 12 | $22.94 | $7.39 | 65 |

<!--TRADE_LOG_END--> 
