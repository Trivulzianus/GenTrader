# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 16:04:51**

| Metric | Value |
|---|---|
| **Total Value** | **$100,996.37** |
| Cash | $141.30 |
| Holdings Value | $100,855.08 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.40 | $2,488.80 | 85 |
| ADBE | 5 | $385.76 | $390.76 | $1,953.80 | 65 |
| AMD | 15 | $141.44 | $136.24 | $2,043.57 | 75 |
| AMZN | 11 | $226.78 | $218.97 | $2,408.66 | 85 |
| AVGO | 9 | $275.08 | $265.26 | $2,387.38 | 85 |
| AXP | 6 | $315.94 | $320.89 | $1,925.34 | 65 |
| BA | 9 | $215.30 | $208.94 | $1,880.42 | 65 |
| BAC | 51 | $47.30 | $47.98 | $2,447.24 | 85 |
| C | 22 | $84.08 | $85.53 | $1,881.69 | 65 |
| CAT | 5 | $381.20 | $392.16 | $1,960.80 | 65 |
| COST | 2 | $991.47 | $981.76 | $1,963.52 | 75 |
| CRM | 8 | $274.83 | $272.17 | $2,177.36 | 75 |
| CSCO | 27 | $68.88 | $68.76 | $1,856.52 | 65 |
| CVX | 16 | $143.73 | $145.77 | $2,332.32 | 85 |
| DIS | 16 | $122.90 | $122.82 | $1,965.12 | 65 |
| GOOGL | 14 | $175.62 | $174.56 | $2,443.77 | 85 |
| GS | 3 | $706.65 | $705.47 | $2,116.41 | 75 |
| HD | 7 | $369.90 | $378.08 | $2,646.56 | 85 |
| INTC | 81 | $22.31 | $22.99 | $1,862.19 | 65 |
| JNJ | 12 | $151.57 | $157.20 | $1,886.40 | 65 |
| JPM | 7 | $285.02 | $288.44 | $2,019.12 | 65 |
| KO | 29 | $70.55 | $72.07 | $2,090.03 | 75 |
| LLY | 3 | $767.33 | $785.25 | $2,355.74 | 65 |
| MA | 4 | $537.87 | $563.23 | $2,252.90 | 65 |
| META | 3 | $712.71 | $717.42 | $2,152.27 | 90 |
| MRK | 30 | $79.35 | $82.43 | $2,472.79 | 85 |
| MSFT | 4 | $492.89 | $491.29 | $1,965.16 | 85 |
| NFLX | 1 | $1,334.07 | $1,285.91 | $1,285.91 | 85 |
| NKE | 34 | $71.01 | $73.50 | $2,499.00 | 85 |
| NVDA | 16 | $154.76 | $152.46 | $2,439.32 | 85 |
| ORCL | 9 | $219.56 | $218.19 | $1,963.71 | 65 |
| PEP | 16 | $131.60 | $136.13 | $2,178.08 | 75 |
| PFE | 97 | $24.29 | $25.23 | $2,447.31 | 85 |
| PG | 12 | $159.73 | $161.84 | $1,942.08 | 65 |
| PYPL | 33 | $73.91 | $75.23 | $2,482.76 | 85 |
| QCOM | 16 | $159.24 | $159.68 | $2,554.83 | 85 |
| T | 85 | $28.52 | $28.86 | $2,453.50 | 85 |
| TGT | 21 | $98.42 | $104.90 | $2,202.90 | 75 |
| TSLA | 6 | $287.77 | $300.49 | $1,802.94 | 65 |
| UNH | 8 | $306.63 | $324.32 | $2,594.56 | 85 |
| UNP | 11 | $232.22 | $236.38 | $2,600.18 | 85 |
| V | 6 | $344.95 | $355.29 | $2,131.74 | 65 |
| VZ | 50 | $42.73 | $43.79 | $2,189.43 | 75 |
| WFC | 31 | $79.89 | $81.00 | $2,511.00 | 85 |
| WMT | 25 | $97.07 | $98.19 | $2,454.69 | 85 |
| XOM | 20 | $109.35 | $109.26 | $2,185.27 | 75 |

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
| 2025-07-01 15:55:25 | BUY | AMZN | 2 | $219.27 | N/A | 85 |
| 2025-07-01 15:55:25 | BUY | CVX | 2 | $145.61 | N/A | 85 |
| 2025-07-01 15:48:26 | SELL | AMZN | 2 | $219.39 | $-14.82 | 65 |
| 2025-07-01 15:48:26 | SELL | NVDA | 4 | $157.99 | $7.85 | 65 |
| 2025-07-01 15:48:26 | SELL | INTC | 1 | $23.09 | $0.77 | 65 |
| 2025-07-01 15:48:26 | SELL | PFE | 1 | $25.22 | $0.92 | 85 |
| 2025-07-01 15:48:26 | BUY | TSLA | 1 | $302.11 | N/A | 75 |
| 2025-07-01 15:48:26 | BUY | KO | 3 | $72.15 | N/A | 75 |
| 2025-07-01 15:48:26 | BUY | C | 6 | $85.11 | N/A | 85 |
| 2025-07-01 15:40:30 | SELL | JNJ | 1 | $156.97 | $4.99 | 65 |
| 2025-07-01 15:40:30 | SELL | C | 3 | $85.23 | $3.01 | 65 |
| 2025-07-01 15:40:30 | BUY | XOM | 4 | $109.07 | N/A | 85 |
| 2025-07-01 15:30:17 | SELL | CRM | 1 | $273.37 | $-1.30 | 75 |
| 2025-07-01 15:30:17 | SELL | AMD | 2 | $136.40 | $-9.64 | 75 |
| 2025-07-01 15:30:17 | SELL | INTC | 2 | $22.86 | $1.05 | 65 |

<!--TRADE_LOG_END--> 
