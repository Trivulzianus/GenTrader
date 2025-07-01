# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 15:40:44**

| Metric | Value |
|---|---|
| **Total Value** | **$100,848.33** |
| Cash | $128.82 |
| Holdings Value | $100,719.51 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.36 | $2,488.31 | 85 |
| ADBE | 5 | $385.76 | $389.27 | $1,946.35 | 65 |
| AMD | 16 | $141.82 | $136.45 | $2,183.20 | 75 |
| AMZN | 11 | $226.80 | $219.44 | $2,413.78 | 85 |
| AVGO | 9 | $275.08 | $264.67 | $2,382.03 | 85 |
| AXP | 6 | $315.94 | $320.00 | $1,920.00 | 65 |
| BA | 9 | $215.30 | $208.32 | $1,874.88 | 65 |
| BAC | 51 | $47.30 | $47.76 | $2,435.51 | 85 |
| C | 22 | $84.09 | $85.20 | $1,874.40 | 65 |
| CAT | 5 | $381.20 | $391.38 | $1,956.90 | 65 |
| COST | 2 | $991.47 | $984.01 | $1,968.02 | 75 |
| CRM | 8 | $274.83 | $271.90 | $2,175.20 | 75 |
| CSCO | 28 | $68.90 | $68.69 | $1,923.32 | 65 |
| CVX | 14 | $143.46 | $145.52 | $2,037.28 | 85 |
| DIS | 16 | $122.90 | $122.67 | $1,962.72 | 65 |
| GOOGL | 14 | $175.62 | $174.78 | $2,446.92 | 85 |
| GS | 3 | $706.65 | $703.73 | $2,111.20 | 65 |
| HD | 7 | $369.90 | $378.17 | $2,647.19 | 85 |
| INTC | 82 | $22.32 | $22.94 | $1,881.14 | 65 |
| JNJ | 12 | $151.57 | $156.97 | $1,883.64 | 65 |
| JPM | 7 | $285.02 | $287.61 | $2,013.24 | 65 |
| KO | 26 | $70.37 | $72.08 | $1,874.08 | 65 |
| LLY | 3 | $767.33 | $784.17 | $2,352.51 | 65 |
| MA | 4 | $537.87 | $562.43 | $2,249.72 | 65 |
| META | 3 | $712.71 | $719.95 | $2,159.84 | 90 |
| MRK | 30 | $79.35 | $82.42 | $2,472.60 | 85 |
| MSFT | 4 | $492.89 | $492.88 | $1,971.52 | 85 |
| NFLX | 1 | $1,334.07 | $1,287.91 | $1,287.91 | 85 |
| NKE | 34 | $71.01 | $73.59 | $2,502.06 | 85 |
| NVDA | 16 | $156.03 | $152.62 | $2,441.92 | 85 |
| ORCL | 9 | $219.56 | $217.62 | $1,958.58 | 65 |
| PEP | 16 | $131.60 | $135.80 | $2,172.80 | 75 |
| PFE | 98 | $24.30 | $25.16 | $2,465.67 | 85 |
| PG | 12 | $159.73 | $161.87 | $1,942.44 | 65 |
| PYPL | 33 | $73.91 | $75.03 | $2,475.83 | 85 |
| QCOM | 16 | $159.24 | $159.21 | $2,547.36 | 85 |
| T | 85 | $28.52 | $28.85 | $2,452.25 | 85 |
| TGT | 21 | $98.42 | $104.17 | $2,187.47 | 75 |
| TSLA | 6 | $290.36 | $302.22 | $1,813.32 | 65 |
| UNH | 8 | $306.63 | $324.40 | $2,595.16 | 85 |
| UNP | 11 | $232.22 | $235.55 | $2,591.05 | 85 |
| V | 6 | $344.95 | $354.79 | $2,128.74 | 85 |
| VZ | 50 | $42.73 | $43.66 | $2,182.88 | 75 |
| WFC | 31 | $79.89 | $80.72 | $2,502.47 | 85 |
| WMT | 25 | $97.07 | $98.63 | $2,465.80 | 85 |
| XOM | 22 | $109.34 | $109.11 | $2,400.31 | 85 |

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
| 2025-07-01 15:40:30 | SELL | JNJ | 1 | $156.97 | $4.99 | 65 |
| 2025-07-01 15:40:30 | SELL | C | 3 | $85.23 | $3.01 | 65 |
| 2025-07-01 15:40:30 | BUY | XOM | 4 | $109.07 | N/A | 85 |
| 2025-07-01 15:30:17 | SELL | CRM | 1 | $273.37 | $-1.30 | 75 |
| 2025-07-01 15:30:17 | SELL | AMD | 2 | $136.40 | $-9.64 | 75 |
| 2025-07-01 15:30:17 | SELL | INTC | 2 | $22.86 | $1.05 | 65 |
| 2025-07-01 15:30:17 | SELL | PFE | 1 | $25.12 | $0.81 | 85 |
| 2025-07-01 15:30:17 | SELL | BA | 1 | $207.81 | $-6.74 | 65 |
| 2025-07-01 15:30:17 | BUY | BAC | 11 | $47.72 | N/A | 85 |
| 2025-07-01 15:30:17 | BUY | C | 2 | $85.19 | N/A | 75 |
| 2025-07-01 15:16:59 | SELL | KO | 1 | $72.42 | $1.98 | 65 |
| 2025-07-01 15:16:59 | SELL | PEP | 1 | $135.79 | $3.93 | 75 |
| 2025-07-01 15:16:59 | BUY | JNJ | 1 | $157.42 | N/A | 75 |
| 2025-07-01 15:16:59 | BUY | AMD | 2 | $135.28 | N/A | 85 |
| 2025-07-01 15:16:59 | BUY | CVX | 1 | $145.10 | N/A | 75 |
| 2025-07-01 15:04:07 | SELL | AMD | 2 | $136.43 | $-9.83 | 75 |
| 2025-07-01 15:04:07 | SELL | CSCO | 4 | $69.05 | $0.54 | 65 |
| 2025-07-01 15:04:07 | BUY | NKE | 1 | $71.04 | N/A | 85 |
| 2025-07-01 15:04:07 | BUY | PFE | 10 | $24.85 | N/A | 85 |
| 2025-07-01 14:55:20 | SELL | TSLA | 1 | $317.66 | $23.40 | 65 |
| 2025-07-01 14:55:20 | SELL | PFE | 10 | $24.80 | $4.99 | 75 |
| 2025-07-01 14:55:20 | SELL | CSCO | 4 | $68.99 | $0.27 | 75 |
| 2025-07-01 14:55:20 | BUY | NVDA | 1 | $152.99 | N/A | 85 |
| 2025-07-01 14:55:20 | BUY | INTC | 1 | $22.64 | N/A | 65 |
| 2025-07-01 14:55:20 | BUY | AMD | 2 | $136.55 | N/A | 85 |

<!--TRADE_LOG_END--> 
