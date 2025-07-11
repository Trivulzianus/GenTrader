# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 19:37:09**

| Metric | Value |
|---|---|
| **Total Value** | **$100,827.40** |
| Cash | $1,702.60 |
| Holdings Value | $99,124.79 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.27 | $211.14 | $2,322.54 | 75 |
| ADBE | 5 | $377.60 | $363.60 | $1,818.00 | 65 |
| AMD | 15 | $134.63 | $146.59 | $2,198.85 | 70 |
| AMZN | 11 | $221.97 | $225.43 | $2,479.73 | 85 |
| AVGO | 8 | $275.34 | $274.72 | $2,197.76 | 65 |
| AXP | 7 | $325.34 | $320.25 | $2,241.75 | 75 |
| BA | 11 | $213.85 | $226.65 | $2,493.10 | 85 |
| BAC | 47 | $48.70 | $46.80 | $2,199.37 | 70 |
| C | 24 | $86.64 | $86.86 | $2,084.52 | 65 |
| CAT | 5 | $396.39 | $406.60 | $2,033.00 | 70 |
| COST | 2 | $979.83 | $970.58 | $1,941.16 | 65 |
| CRM | 7 | $268.68 | $257.89 | $1,805.26 | 65 |
| CSCO | 34 | $68.38 | $68.03 | $2,313.02 | 75 |
| CVX | 17 | $147.16 | $155.70 | $2,646.90 | 85 |
| DIS | 18 | $122.80 | $120.26 | $2,164.68 | 70 |
| GOOGL | 13 | $179.61 | $180.27 | $2,343.51 | 75 |
| GS | 3 | $717.52 | $704.74 | $2,114.23 | 70 |
| HD | 6 | $372.64 | $370.38 | $2,222.28 | 65 |
| INTC | 87 | $22.36 | $23.52 | $2,045.81 | 65 |
| JNJ | 13 | $155.89 | $157.03 | $2,041.39 | 65 |
| JPM | 8 | $292.23 | $287.10 | $2,296.80 | 75 |
| KO | 29 | $71.03 | $70.11 | $2,033.33 | 65 |
| LLY | 3 | $781.32 | $787.39 | $2,362.18 | 70 |
| MA | 4 | $563.08 | $549.47 | $2,197.88 | 65 |
| META | 3 | $717.12 | $718.61 | $2,155.83 | 85 |
| MRK | 25 | $82.29 | $83.38 | $2,084.38 | 65 |
| MSFT | 5 | $498.84 | $503.48 | $2,517.40 | 70 |
| NFLX | 1 | $1,279.00 | $1,242.86 | $1,242.86 | 65 |
| NKE | 31 | $75.77 | $72.82 | $2,257.42 | 70 |
| NVDA | 16 | $157.38 | $165.13 | $2,642.10 | 85 |
| ORCL | 9 | $233.26 | $230.66 | $2,075.94 | 65 |
| PEP | 15 | $136.57 | $135.28 | $2,029.12 | 65 |
| PFE | 80 | $25.17 | $25.68 | $2,054.80 | 65 |
| PG | 13 | $160.78 | $157.26 | $2,044.44 | 65 |
| PYPL | 28 | $72.13 | $71.10 | $1,990.80 | 65 |
| QCOM | 13 | $162.18 | $158.12 | $2,055.56 | 65 |
| T | 70 | $27.12 | $27.09 | $1,896.30 | 60 |
| TGT | 20 | $104.91 | $104.72 | $2,094.40 | 65 |
| TSLA | 6 | $288.62 | $313.68 | $1,882.08 | 65 |
| UNH | 7 | $298.51 | $302.60 | $2,118.20 | 65 |
| UNP | 10 | $236.18 | $235.13 | $2,351.30 | 75 |
| V | 6 | $355.85 | $347.47 | $2,084.82 | 70 |
| VZ | 49 | $43.12 | $41.79 | $2,047.54 | 65 |
| WFC | 29 | $82.28 | $82.58 | $2,394.68 | 75 |
| WMT | 22 | $97.25 | $94.62 | $2,081.64 | 65 |
| XOM | 21 | $109.99 | $115.53 | $2,426.13 | 75 |

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
| 2025-07-11 18:56:16 | BUY | CVX | 1 | $155.79 | N/A | 85 |
| 2025-07-11 18:44:46 | SELL | AMD | 1 | $146.93 | $10.23 | 75 |
| 2025-07-11 18:44:46 | SELL | C | 4 | $86.81 | $0.52 | 70 |
| 2025-07-11 18:44:46 | SELL | CVX | 1 | $155.67 | $8.51 | 75 |
| 2025-07-11 18:44:46 | BUY | KO | 2 | $70.01 | N/A | 65 |
| 2025-07-11 18:44:46 | BUY | CSCO | 3 | $68.04 | N/A | 75 |
| 2025-07-11 18:44:46 | BUY | TGT | 1 | $104.63 | N/A | 70 |

<!--TRADE_LOG_END--> 
