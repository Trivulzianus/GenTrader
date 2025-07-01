# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 18:48:21**

| Metric | Value |
|---|---|
| **Total Value** | **$101,206.62** |
| Cash | $424.14 |
| Holdings Value | $100,782.49 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.04 | $2,496.48 | 85 |
| ADBE | 5 | $385.76 | $390.58 | $1,952.90 | 65 |
| AMD | 14 | $139.28 | $137.22 | $1,921.15 | 65 |
| AMZN | 10 | $227.67 | $221.18 | $2,211.75 | 85 |
| AVGO | 9 | $272.95 | $264.56 | $2,381.04 | 85 |
| AXP | 6 | $315.94 | $323.58 | $1,941.48 | 65 |
| BA | 9 | $215.30 | $210.79 | $1,897.11 | 65 |
| BAC | 50 | $47.28 | $48.35 | $2,417.51 | 85 |
| C | 24 | $84.25 | $86.39 | $2,073.48 | 75 |
| CAT | 5 | $381.20 | $392.92 | $1,964.60 | 65 |
| COST | 2 | $991.47 | $986.78 | $1,973.56 | 65 |
| CRM | 8 | $274.93 | $272.97 | $2,183.76 | 85 |
| CSCO | 27 | $68.84 | $69.08 | $1,865.16 | 65 |
| CVX | 17 | $143.81 | $145.64 | $2,475.88 | 85 |
| DIS | 15 | $122.83 | $123.31 | $1,849.65 | 65 |
| GOOGL | 14 | $175.62 | $175.23 | $2,453.22 | 85 |
| GS | 3 | $706.65 | $707.49 | $2,122.47 | 75 |
| HD | 7 | $369.90 | $374.50 | $2,621.50 | 85 |
| INTC | 81 | $22.22 | $22.98 | $1,861.78 | 65 |
| JNJ | 12 | $151.63 | $155.61 | $1,867.32 | 65 |
| JPM | 7 | $285.02 | $290.09 | $2,030.63 | 65 |
| KO | 26 | $70.42 | $71.69 | $1,864.07 | 65 |
| LLY | 3 | $767.33 | $775.95 | $2,327.84 | 65 |
| MA | 4 | $537.87 | $565.20 | $2,260.80 | 85 |
| META | 3 | $712.71 | $719.85 | $2,159.55 | 85 |
| MRK | 30 | $79.35 | $81.93 | $2,458.00 | 85 |
| MSFT | 4 | $492.89 | $492.45 | $1,969.80 | 85 |
| NFLX | 1 | $1,334.07 | $1,297.65 | $1,297.65 | 85 |
| NKE | 33 | $70.94 | $73.27 | $2,417.84 | 85 |
| NVDA | 16 | $153.32 | $154.44 | $2,470.96 | 85 |
| ORCL | 9 | $219.56 | $219.07 | $1,971.63 | 65 |
| PEP | 16 | $131.60 | $135.08 | $2,161.28 | 75 |
| PFE | 96 | $24.28 | $25.07 | $2,407.20 | 85 |
| PG | 12 | $159.73 | $161.32 | $1,935.90 | 65 |
| PYPL | 32 | $73.86 | $75.47 | $2,415.20 | 85 |
| QCOM | 15 | $159.12 | $160.41 | $2,406.15 | 85 |
| T | 84 | $28.52 | $28.80 | $2,419.20 | 85 |
| TGT | 23 | $98.95 | $104.46 | $2,402.58 | 85 |
| TSLA | 7 | $287.46 | $302.56 | $2,117.92 | 65 |
| UNH | 8 | $306.63 | $323.25 | $2,586.00 | 85 |
| UNP | 11 | $232.22 | $235.49 | $2,590.39 | 85 |
| V | 6 | $344.95 | $356.32 | $2,137.93 | 85 |
| VZ | 49 | $42.72 | $43.59 | $2,135.66 | 75 |
| WFC | 30 | $79.85 | $81.28 | $2,438.55 | 85 |
| WMT | 25 | $97.07 | $98.53 | $2,463.12 | 85 |
| XOM | 22 | $109.37 | $109.31 | $2,404.82 | 85 |

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
| 2025-07-01 18:04:57 | BUY | NVDA | 4 | $154.66 | N/A | 85 |
| 2025-07-01 18:04:57 | BUY | TSLA | 1 | $299.66 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | AMD | 1 | $137.18 | N/A | 85 |

<!--TRADE_LOG_END--> 
