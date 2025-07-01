# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 16:17:53**

| Metric | Value |
|---|---|
| **Total Value** | **$101,144.47** |
| Cash | $43.09 |
| Holdings Value | $101,101.38 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.66 | $2,491.92 | 85 |
| ADBE | 5 | $385.76 | $391.68 | $1,958.40 | 75 |
| AMD | 17 | $140.89 | $136.77 | $2,325.09 | 85 |
| AMZN | 11 | $226.78 | $218.89 | $2,407.79 | 85 |
| AVGO | 7 | $274.91 | $266.63 | $1,866.44 | 65 |
| AXP | 6 | $315.94 | $321.30 | $1,927.77 | 65 |
| BA | 9 | $215.30 | $209.28 | $1,883.57 | 65 |
| BAC | 51 | $47.30 | $48.05 | $2,450.55 | 85 |
| C | 22 | $84.08 | $85.61 | $1,883.31 | 65 |
| CAT | 5 | $381.20 | $393.19 | $1,965.92 | 65 |
| COST | 2 | $991.47 | $979.04 | $1,958.09 | 75 |
| CRM | 8 | $274.83 | $273.57 | $2,188.56 | 75 |
| CSCO | 27 | $68.88 | $68.82 | $1,858.14 | 65 |
| CVX | 16 | $143.73 | $146.03 | $2,336.48 | 85 |
| DIS | 16 | $122.90 | $123.01 | $1,968.16 | 65 |
| GOOGL | 14 | $175.62 | $174.25 | $2,439.50 | 85 |
| GS | 3 | $706.65 | $704.62 | $2,113.85 | 65 |
| HD | 7 | $369.90 | $379.25 | $2,654.75 | 85 |
| INTC | 81 | $22.31 | $23.10 | $1,871.16 | 65 |
| JNJ | 13 | $152.00 | $157.10 | $2,042.30 | 75 |
| JPM | 7 | $285.02 | $288.12 | $2,016.84 | 65 |
| KO | 29 | $70.55 | $71.99 | $2,087.76 | 75 |
| LLY | 3 | $767.33 | $786.15 | $2,358.45 | 65 |
| MA | 4 | $537.87 | $563.05 | $2,252.20 | 65 |
| META | 3 | $712.71 | $716.59 | $2,149.77 | 90 |
| MRK | 30 | $79.35 | $82.84 | $2,485.20 | 85 |
| MSFT | 4 | $492.89 | $492.00 | $1,968.00 | 85 |
| NFLX | 1 | $1,334.07 | $1,285.61 | $1,285.61 | 85 |
| NKE | 34 | $71.01 | $73.49 | $2,498.66 | 85 |
| NVDA | 16 | $154.76 | $152.97 | $2,447.60 | 85 |
| ORCL | 9 | $219.56 | $218.66 | $1,967.94 | 65 |
| PEP | 16 | $131.60 | $136.09 | $2,177.43 | 75 |
| PFE | 97 | $24.29 | $25.30 | $2,454.59 | 85 |
| PG | 12 | $159.73 | $161.78 | $1,941.36 | 65 |
| PYPL | 33 | $73.91 | $75.37 | $2,487.21 | 85 |
| QCOM | 16 | $159.24 | $161.34 | $2,581.36 | 85 |
| T | 85 | $28.52 | $28.82 | $2,449.28 | 85 |
| TGT | 21 | $98.42 | $104.95 | $2,203.95 | 85 |
| TSLA | 6 | $287.77 | $302.50 | $1,815.00 | 65 |
| UNH | 8 | $306.63 | $324.54 | $2,596.34 | 85 |
| UNP | 11 | $232.22 | $236.94 | $2,606.34 | 85 |
| V | 6 | $344.95 | $354.80 | $2,128.80 | 65 |
| VZ | 50 | $42.73 | $43.80 | $2,189.75 | 75 |
| WFC | 31 | $79.89 | $80.97 | $2,510.22 | 85 |
| WMT | 25 | $97.07 | $97.81 | $2,445.38 | 85 |
| XOM | 22 | $109.35 | $109.30 | $2,404.60 | 85 |

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

<!--TRADE_LOG_END--> 
