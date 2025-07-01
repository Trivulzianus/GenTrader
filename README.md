# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 19:26:13**

| Metric | Value |
|---|---|
| **Total Value** | **$101,190.32** |
| Cash | $106.75 |
| Holdings Value | $101,083.57 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.83 | $2,493.96 | 85 |
| ADBE | 5 | $385.76 | $391.23 | $1,956.14 | 75 |
| AMD | 16 | $138.97 | $136.84 | $2,189.44 | 75 |
| AMZN | 11 | $227.14 | $221.64 | $2,438.01 | 85 |
| AVGO | 9 | $272.95 | $263.99 | $2,375.91 | 85 |
| AXP | 6 | $315.94 | $323.06 | $1,938.36 | 65 |
| BA | 9 | $215.30 | $210.09 | $1,890.81 | 65 |
| BAC | 50 | $47.28 | $48.23 | $2,411.50 | 85 |
| C | 22 | $84.05 | $86.17 | $1,895.63 | 65 |
| CAT | 5 | $381.20 | $392.87 | $1,964.33 | 65 |
| COST | 2 | $991.47 | $984.51 | $1,969.02 | 65 |
| CRM | 8 | $274.93 | $272.71 | $2,181.71 | 75 |
| CSCO | 27 | $68.84 | $69.17 | $1,867.71 | 65 |
| CVX | 17 | $143.81 | $146.06 | $2,483.02 | 85 |
| DIS | 15 | $122.83 | $123.38 | $1,850.62 | 65 |
| GOOGL | 14 | $175.62 | $175.81 | $2,461.34 | 85 |
| GS | 3 | $706.65 | $707.26 | $2,121.78 | 75 |
| HD | 7 | $369.90 | $374.20 | $2,619.43 | 85 |
| INTC | 81 | $22.22 | $22.94 | $1,858.53 | 65 |
| JNJ | 13 | $151.97 | $155.93 | $2,027.03 | 65 |
| JPM | 7 | $285.02 | $290.30 | $2,032.07 | 65 |
| KO | 27 | $70.48 | $71.72 | $1,936.57 | 65 |
| LLY | 3 | $767.33 | $776.47 | $2,329.39 | 65 |
| MA | 4 | $537.87 | $565.86 | $2,263.44 | 65 |
| META | 3 | $712.71 | $719.20 | $2,157.60 | 85 |
| MRK | 30 | $79.35 | $81.99 | $2,459.70 | 85 |
| MSFT | 4 | $492.89 | $492.24 | $1,968.96 | 85 |
| NFLX | 1 | $1,334.07 | $1,295.32 | $1,295.32 | 85 |
| NKE | 33 | $70.99 | $73.44 | $2,423.68 | 85 |
| NVDA | 16 | $153.32 | $153.59 | $2,457.47 | 85 |
| ORCL | 9 | $219.56 | $218.84 | $1,969.52 | 65 |
| PEP | 16 | $131.60 | $135.29 | $2,164.64 | 75 |
| PFE | 97 | $24.29 | $25.05 | $2,430.34 | 85 |
| PG | 12 | $159.73 | $161.55 | $1,938.60 | 65 |
| PYPL | 32 | $73.86 | $75.47 | $2,414.88 | 85 |
| QCOM | 15 | $159.12 | $159.78 | $2,396.70 | 85 |
| T | 75 | $28.48 | $28.84 | $2,162.62 | 75 |
| TGT | 23 | $98.93 | $104.06 | $2,393.40 | 85 |
| TSLA | 7 | $287.46 | $302.45 | $2,117.15 | 75 |
| UNH | 8 | $306.63 | $324.10 | $2,592.80 | 85 |
| UNP | 11 | $232.22 | $235.89 | $2,594.79 | 85 |
| V | 6 | $344.95 | $356.77 | $2,140.65 | 65 |
| VZ | 49 | $42.72 | $43.69 | $2,140.57 | 75 |
| WFC | 30 | $79.85 | $81.33 | $2,439.75 | 85 |
| WMT | 25 | $97.07 | $98.30 | $2,457.38 | 85 |
| XOM | 22 | $109.37 | $109.61 | $2,411.31 | 85 |

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
| 2025-07-01 19:26:02 | SELL | AMD | 1 | $136.80 | $-2.04 | 75 |
| 2025-07-01 19:26:02 | SELL | KO | 2 | $71.71 | $2.28 | 65 |
| 2025-07-01 19:26:02 | SELL | C | 2 | $86.16 | $3.86 | 65 |
| 2025-07-01 19:26:02 | SELL | T | 9 | $28.85 | $2.95 | 75 |
| 2025-07-01 19:26:02 | BUY | AMZN | 1 | $221.83 | N/A | 85 |
| 2025-07-01 19:26:02 | BUY | NKE | 7 | $73.47 | N/A | 85 |
| 2025-07-01 19:26:02 | BUY | PFE | 1 | $25.07 | N/A | 85 |
| 2025-07-01 19:16:27 | SELL | NKE | 7 | $73.24 | $16.12 | 65 |
| 2025-07-01 19:16:27 | BUY | JNJ | 1 | $156.04 | N/A | 75 |
| 2025-07-01 19:16:27 | BUY | AMD | 2 | $136.57 | N/A | 85 |
| 2025-07-01 19:16:27 | BUY | KO | 3 | $71.83 | N/A | 75 |
| 2025-07-01 19:03:44 | BUY | C | 2 | $86.18 | N/A | 75 |
| 2025-07-01 19:03:44 | BUY | TGT | 2 | $104.35 | N/A | 85 |
| 2025-07-01 18:56:35 | SELL | C | 2 | $86.43 | $4.36 | 65 |
| 2025-07-01 18:56:35 | SELL | TGT | 2 | $104.57 | $11.24 | 75 |
| 2025-07-01 18:56:35 | BUY | AMD | 1 | $137.29 | N/A | 75 |
| 2025-07-01 18:48:11 | SELL | AMD | 4 | $141.90 | $8.15 | 65 |
| 2025-07-01 18:48:11 | SELL | KO | 3 | $71.69 | $3.43 | 65 |
| 2025-07-01 18:48:11 | BUY | T | 10 | $28.80 | N/A | 85 |
| 2025-07-01 18:48:11 | BUY | TGT | 2 | $104.46 | N/A | 85 |
| 2025-07-01 18:32:25 | SELL | BAC | 1 | $48.29 | $1.00 | 85 |
| 2025-07-01 18:32:25 | SELL | DIS | 1 | $123.40 | $0.53 | 65 |
| 2025-07-01 18:32:25 | SELL | VZ | 1 | $43.65 | $0.92 | 75 |
| 2025-07-01 18:32:25 | SELL | T | 11 | $28.78 | $2.88 | 75 |
| 2025-07-01 18:32:25 | BUY | KO | 3 | $71.73 | N/A | 75 |

<!--TRADE_LOG_END--> 
