# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 19:50:28**

| Metric | Value |
|---|---|
| **Total Value** | **$100,827.87** |
| Cash | $1,597.87 |
| Holdings Value | $99,230.00 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.27 | $211.13 | $2,322.48 | 70 |
| ADBE | 5 | $377.60 | $362.99 | $1,814.97 | 65 |
| AMD | 15 | $134.63 | $146.81 | $2,202.15 | 70 |
| AMZN | 11 | $221.97 | $225.46 | $2,480.06 | 85 |
| AVGO | 8 | $275.34 | $274.53 | $2,196.24 | 70 |
| AXP | 7 | $325.34 | $320.35 | $2,242.45 | 75 |
| BA | 10 | $212.59 | $226.44 | $2,264.40 | 70 |
| BAC | 47 | $48.70 | $46.77 | $2,197.95 | 70 |
| C | 25 | $86.65 | $86.92 | $2,173.08 | 70 |
| CAT | 5 | $396.39 | $406.61 | $2,033.05 | 70 |
| COST | 2 | $979.83 | $970.58 | $1,941.15 | 65 |
| CRM | 7 | $268.68 | $257.58 | $1,803.06 | 65 |
| CSCO | 33 | $68.40 | $68.00 | $2,244.00 | 70 |
| CVX | 17 | $147.16 | $155.70 | $2,646.90 | 80 |
| DIS | 18 | $122.80 | $120.16 | $2,162.88 | 65 |
| GOOGL | 13 | $179.61 | $180.25 | $2,343.32 | 75 |
| GS | 3 | $717.52 | $704.36 | $2,113.07 | 70 |
| HD | 6 | $372.64 | $370.72 | $2,224.34 | 65 |
| INTC | 87 | $22.36 | $23.46 | $2,041.45 | 65 |
| JNJ | 13 | $155.89 | $156.89 | $2,039.57 | 65 |
| JPM | 8 | $292.23 | $287.09 | $2,296.72 | 70 |
| KO | 29 | $71.03 | $70.06 | $2,031.60 | 65 |
| LLY | 3 | $781.32 | $791.99 | $2,375.97 | 70 |
| MA | 4 | $563.08 | $549.88 | $2,199.53 | 70 |
| META | 3 | $717.12 | $717.50 | $2,152.51 | 75 |
| MRK | 26 | $82.34 | $83.47 | $2,170.22 | 70 |
| MSFT | 5 | $498.84 | $503.57 | $2,517.85 | 85 |
| NFLX | 1 | $1,279.00 | $1,243.55 | $1,243.55 | 65 |
| NKE | 31 | $75.77 | $72.83 | $2,257.73 | 70 |
| NVDA | 16 | $157.38 | $165.00 | $2,640.00 | 85 |
| ORCL | 9 | $233.26 | $230.57 | $2,075.13 | 70 |
| PEP | 15 | $136.57 | $135.28 | $2,029.20 | 65 |
| PFE | 91 | $25.23 | $25.70 | $2,338.24 | 75 |
| PG | 13 | $160.78 | $157.17 | $2,043.21 | 65 |
| PYPL | 28 | $72.13 | $71.67 | $2,006.90 | 65 |
| QCOM | 13 | $162.18 | $157.94 | $2,053.22 | 65 |
| T | 75 | $27.11 | $27.00 | $2,025.00 | 65 |
| TGT | 20 | $104.91 | $104.47 | $2,089.40 | 65 |
| TSLA | 6 | $288.62 | $313.60 | $1,881.60 | 65 |
| UNH | 7 | $298.51 | $303.52 | $2,124.67 | 65 |
| UNP | 10 | $236.18 | $235.31 | $2,353.15 | 75 |
| V | 6 | $355.85 | $347.59 | $2,085.54 | 65 |
| VZ | 49 | $43.12 | $41.66 | $2,041.59 | 65 |
| WFC | 29 | $82.28 | $82.63 | $2,396.27 | 75 |
| WMT | 20 | $97.53 | $94.43 | $1,888.60 | 60 |
| XOM | 21 | $109.99 | $115.53 | $2,426.03 | 75 |

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
| 2025-07-11 19:50:20 | SELL | WMT | 2 | $94.42 | $-5.66 | 60 |
| 2025-07-11 19:50:20 | SELL | BA | 1 | $226.44 | $12.59 | 70 |
| 2025-07-11 19:50:20 | SELL | CSCO | 1 | $68.00 | $-0.38 | 70 |
| 2025-07-11 19:50:20 | BUY | MRK | 1 | $83.46 | N/A | 70 |
| 2025-07-11 19:50:20 | BUY | PFE | 11 | $25.69 | N/A | 75 |
| 2025-07-11 19:50:20 | BUY | C | 1 | $86.91 | N/A | 70 |
| 2025-07-11 19:50:20 | BUY | T | 5 | $27.00 | N/A | 65 |
| 2025-07-11 19:36:57 | SELL | AMD | 1 | $146.60 | $11.22 | 70 |
| 2025-07-11 19:36:57 | SELL | C | 2 | $86.85 | $0.40 | 65 |
| 2025-07-11 19:36:57 | SELL | T | 6 | $27.09 | $-0.17 | 60 |
| 2025-07-11 19:36:57 | BUY | AAPL | 1 | $211.14 | N/A | 75 |
| 2025-07-11 19:36:57 | BUY | BA | 1 | $226.66 | N/A | 85 |
| 2025-07-11 19:24:57 | SELL | XOM | 2 | $115.43 | $9.94 | 75 |
| 2025-07-11 19:24:57 | SELL | C | 1 | $86.78 | $0.12 | 70 |
| 2025-07-11 19:24:57 | BUY | DIS | 1 | $120.19 | N/A | 70 |
| 2025-07-11 19:24:57 | BUY | CSCO | 1 | $68.08 | N/A | 75 |
| 2025-07-11 19:07:37 | SELL | PFE | 5 | $25.62 | $2.14 | 65 |
| 2025-07-11 19:07:37 | SELL | BA | 1 | $226.55 | $12.71 | 70 |
| 2025-07-11 19:07:37 | BUY | AMD | 1 | $146.18 | N/A | 75 |
| 2025-07-11 19:07:37 | BUY | C | 1 | $86.73 | N/A | 75 |
| 2025-07-11 18:56:16 | SELL | AMD | 2 | $146.87 | $21.55 | 70 |
| 2025-07-11 18:56:16 | SELL | CSCO | 1 | $68.04 | $-0.34 | 70 |
| 2025-07-11 18:56:16 | SELL | TGT | 1 | $104.61 | $-0.29 | 65 |
| 2025-07-11 18:56:16 | BUY | XOM | 2 | $115.69 | N/A | 85 |
| 2025-07-11 18:56:16 | BUY | PFE | 5 | $25.66 | N/A | 70 |

<!--TRADE_LOG_END--> 
