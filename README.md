# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 18:56:40**

| Metric | Value |
|---|---|
| **Total Value** | **$101,253.13** |
| Cash | $668.85 |
| Holdings Value | $100,584.28 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.02 | $2,496.24 | 85 |
| ADBE | 5 | $385.76 | $390.69 | $1,953.45 | 75 |
| AMD | 15 | $139.15 | $137.10 | $2,056.50 | 75 |
| AMZN | 10 | $227.67 | $221.39 | $2,213.90 | 85 |
| AVGO | 9 | $272.95 | $264.21 | $2,377.89 | 85 |
| AXP | 6 | $315.94 | $323.64 | $1,941.87 | 65 |
| BA | 9 | $215.30 | $210.82 | $1,897.38 | 65 |
| BAC | 50 | $47.28 | $48.41 | $2,420.41 | 85 |
| C | 22 | $84.05 | $86.42 | $1,901.35 | 65 |
| CAT | 5 | $381.20 | $393.33 | $1,966.64 | 65 |
| COST | 2 | $991.47 | $986.63 | $1,973.27 | 65 |
| CRM | 8 | $274.93 | $272.83 | $2,182.64 | 75 |
| CSCO | 27 | $68.84 | $69.11 | $1,866.10 | 65 |
| CVX | 17 | $143.81 | $145.92 | $2,480.64 | 85 |
| DIS | 15 | $122.83 | $123.29 | $1,849.35 | 65 |
| GOOGL | 14 | $175.62 | $175.40 | $2,455.53 | 85 |
| GS | 3 | $706.65 | $707.59 | $2,122.76 | 75 |
| HD | 7 | $369.90 | $374.61 | $2,622.27 | 85 |
| INTC | 81 | $22.22 | $23.00 | $1,863.40 | 65 |
| JNJ | 12 | $151.63 | $155.87 | $1,870.44 | 65 |
| JPM | 7 | $285.02 | $290.26 | $2,031.82 | 75 |
| KO | 26 | $70.42 | $71.82 | $1,867.32 | 65 |
| LLY | 3 | $767.33 | $774.86 | $2,324.57 | 75 |
| MA | 4 | $537.87 | $565.36 | $2,261.44 | 85 |
| META | 3 | $712.71 | $719.14 | $2,157.43 | 85 |
| MRK | 30 | $79.35 | $81.98 | $2,459.40 | 85 |
| MSFT | 4 | $492.89 | $492.61 | $1,970.44 | 85 |
| NFLX | 1 | $1,334.07 | $1,295.50 | $1,295.50 | 85 |
| NKE | 33 | $70.94 | $73.38 | $2,421.54 | 85 |
| NVDA | 16 | $153.32 | $153.72 | $2,459.60 | 85 |
| ORCL | 9 | $219.56 | $218.50 | $1,966.50 | 65 |
| PEP | 16 | $131.60 | $135.51 | $2,168.16 | 75 |
| PFE | 96 | $24.28 | $25.11 | $2,410.08 | 85 |
| PG | 12 | $159.73 | $161.66 | $1,939.92 | 65 |
| PYPL | 32 | $73.86 | $75.52 | $2,416.64 | 85 |
| QCOM | 15 | $159.12 | $160.53 | $2,407.95 | 85 |
| T | 84 | $28.52 | $28.80 | $2,419.62 | 85 |
| TGT | 21 | $98.41 | $104.69 | $2,198.42 | 75 |
| TSLA | 7 | $287.46 | $301.58 | $2,111.05 | 75 |
| UNH | 8 | $306.63 | $324.76 | $2,598.10 | 85 |
| UNP | 11 | $232.22 | $236.05 | $2,596.55 | 85 |
| V | 6 | $344.95 | $356.15 | $2,136.93 | 85 |
| VZ | 49 | $42.72 | $43.63 | $2,137.87 | 75 |
| WFC | 30 | $79.85 | $81.44 | $2,443.26 | 85 |
| WMT | 25 | $97.07 | $98.53 | $2,463.25 | 85 |
| XOM | 22 | $109.37 | $109.50 | $2,408.89 | 85 |

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
| 2025-07-01 18:32:25 | BUY | XOM | 1 | $109.25 | N/A | 85 |
| 2025-07-01 18:32:25 | BUY | C | 2 | $86.29 | N/A | 75 |
| 2025-07-01 18:17:48 | SELL | INTC | 1 | $22.99 | $0.76 | 65 |
| 2025-07-01 18:17:48 | SELL | C | 3 | $86.22 | $5.70 | 65 |
| 2025-07-01 18:17:48 | SELL | T | 1 | $28.81 | $0.28 | 85 |
| 2025-07-01 18:17:48 | BUY | AMZN | 1 | $220.89 | N/A | 85 |
| 2025-07-01 18:17:48 | BUY | NKE | 6 | $72.90 | N/A | 85 |
| 2025-07-01 18:17:48 | BUY | PFE | 8 | $25.05 | N/A | 85 |
| 2025-07-01 18:04:57 | SELL | AMZN | 2 | $219.39 | $-14.77 | 65 |
| 2025-07-01 18:04:57 | SELL | CRM | 1 | $273.68 | $-1.11 | 75 |
| 2025-07-01 18:04:57 | SELL | XOM | 1 | $109.05 | $-0.31 | 75 |
| 2025-07-01 18:04:57 | SELL | PFE | 10 | $25.00 | $7.12 | 75 |
| 2025-07-01 18:04:57 | SELL | NKE | 6 | $72.87 | $11.63 | 65 |

<!--TRADE_LOG_END--> 
