# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 18:05:08**

| Metric | Value |
|---|---|
| **Total Value** | **$101,145.51** |
| Cash | $651.65 |
| Holdings Value | $100,493.86 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.26 | $2,499.12 | 85 |
| ADBE | 5 | $385.76 | $391.23 | $1,956.15 | 75 |
| AMD | 18 | $139.86 | $137.20 | $2,469.60 | 85 |
| AMZN | 9 | $228.42 | $220.87 | $1,987.83 | 65 |
| AVGO | 9 | $272.95 | $265.90 | $2,393.10 | 85 |
| AXP | 6 | $315.94 | $323.76 | $1,942.56 | 65 |
| BA | 9 | $215.30 | $210.53 | $1,894.77 | 65 |
| BAC | 51 | $47.30 | $48.30 | $2,463.55 | 85 |
| C | 25 | $84.32 | $86.44 | $2,161.12 | 75 |
| CAT | 5 | $381.20 | $391.82 | $1,959.10 | 65 |
| COST | 2 | $991.47 | $984.99 | $1,969.97 | 75 |
| CRM | 8 | $274.93 | $273.69 | $2,189.48 | 75 |
| CSCO | 27 | $68.84 | $69.18 | $1,867.99 | 65 |
| CVX | 17 | $143.81 | $145.38 | $2,471.46 | 85 |
| DIS | 16 | $122.87 | $123.50 | $1,975.92 | 65 |
| GOOGL | 14 | $175.62 | $175.59 | $2,458.26 | 85 |
| GS | 3 | $706.65 | $706.35 | $2,119.03 | 75 |
| HD | 7 | $369.90 | $374.56 | $2,621.92 | 85 |
| INTC | 82 | $22.23 | $22.96 | $1,882.36 | 65 |
| JNJ | 12 | $151.63 | $155.32 | $1,863.84 | 65 |
| JPM | 7 | $285.02 | $289.88 | $2,029.16 | 65 |
| KO | 26 | $70.42 | $71.67 | $1,863.55 | 65 |
| LLY | 3 | $767.33 | $775.35 | $2,326.05 | 65 |
| MA | 4 | $537.87 | $565.80 | $2,263.20 | 65 |
| META | 3 | $712.71 | $722.34 | $2,167.02 | 90 |
| MRK | 30 | $79.35 | $81.79 | $2,453.70 | 85 |
| MSFT | 4 | $492.89 | $492.96 | $1,971.84 | 65 |
| NFLX | 1 | $1,334.07 | $1,301.48 | $1,301.48 | 85 |
| NKE | 27 | $70.50 | $72.89 | $1,968.03 | 65 |
| NVDA | 16 | $153.32 | $154.66 | $2,474.64 | 85 |
| ORCL | 9 | $219.56 | $219.78 | $1,977.98 | 65 |
| PEP | 16 | $131.60 | $134.97 | $2,159.52 | 75 |
| PFE | 88 | $24.21 | $25.00 | $2,200.27 | 75 |
| PG | 12 | $159.73 | $160.94 | $1,931.28 | 65 |
| PYPL | 32 | $73.86 | $75.59 | $2,418.83 | 85 |
| QCOM | 15 | $159.12 | $160.33 | $2,404.95 | 85 |
| T | 86 | $28.53 | $28.81 | $2,477.66 | 85 |
| TGT | 21 | $98.42 | $103.96 | $2,183.16 | 75 |
| TSLA | 7 | $287.46 | $299.69 | $2,097.80 | 75 |
| UNH | 8 | $306.63 | $322.40 | $2,579.20 | 85 |
| UNP | 11 | $232.22 | $234.97 | $2,584.67 | 85 |
| V | 6 | $344.95 | $356.62 | $2,139.72 | 65 |
| VZ | 50 | $42.73 | $43.70 | $2,184.75 | 75 |
| WFC | 30 | $79.85 | $81.33 | $2,439.90 | 85 |
| WMT | 25 | $97.07 | $98.34 | $2,458.62 | 85 |
| XOM | 21 | $109.38 | $109.03 | $2,289.74 | 75 |

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
| 2025-07-01 18:04:57 | SELL | AMZN | 2 | $219.39 | $-14.77 | 65 |
| 2025-07-01 18:04:57 | SELL | CRM | 1 | $273.68 | $-1.11 | 75 |
| 2025-07-01 18:04:57 | SELL | XOM | 1 | $109.05 | $-0.31 | 75 |
| 2025-07-01 18:04:57 | SELL | PFE | 10 | $25.00 | $7.12 | 75 |
| 2025-07-01 18:04:57 | SELL | NKE | 6 | $72.87 | $11.63 | 65 |
| 2025-07-01 18:04:57 | BUY | NVDA | 4 | $154.66 | N/A | 85 |
| 2025-07-01 18:04:57 | BUY | TSLA | 1 | $299.66 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | AMD | 1 | $137.18 | N/A | 85 |
| 2025-07-01 18:04:57 | BUY | C | 3 | $86.44 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | VZ | 1 | $43.69 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | T | 1 | $28.82 | N/A | 85 |
| 2025-07-01 17:56:28 | SELL | NVDA | 3 | $157.99 | $12.29 | 65 |
| 2025-07-01 17:56:28 | SELL | TSLA | 1 | $317.66 | $27.63 | 65 |
| 2025-07-01 17:56:28 | SELL | C | 2 | $86.39 | $4.32 | 65 |
| 2025-07-01 17:56:28 | BUY | CRM | 1 | $273.90 | N/A | 85 |
| 2025-07-01 17:56:28 | BUY | INTC | 1 | $22.98 | N/A | 65 |
| 2025-07-01 17:56:28 | BUY | XOM | 2 | $109.14 | N/A | 85 |
| 2025-07-01 17:49:44 | SELL | TGT | 2 | $104.10 | $10.37 | 75 |
| 2025-07-01 17:49:44 | BUY | C | 2 | $86.38 | N/A | 75 |
| 2025-07-01 17:40:46 | SELL | XOM | 2 | $109.32 | $-0.11 | 75 |
| 2025-07-01 17:40:46 | SELL | INTC | 1 | $22.98 | $0.75 | 65 |
| 2025-07-01 17:40:46 | SELL | PFE | 1 | $25.00 | $0.69 | 85 |
| 2025-07-01 17:40:46 | SELL | CSCO | 1 | $69.07 | $0.22 | 65 |
| 2025-07-01 17:40:46 | BUY | VZ | 5 | $43.67 | N/A | 75 |
| 2025-07-01 17:40:46 | BUY | TGT | 2 | $104.20 | N/A | 85 |

<!--TRADE_LOG_END--> 
