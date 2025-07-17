# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 13:49:27**

| Metric | Value |
|---|---|
| **Total Value** | **$101,168.82** |
| Cash | $883.56 |
| Holdings Value | $100,285.26 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.13 | $2,101.30 | 65 |
| ADBE | 6 | $375.23 | $361.08 | $2,166.48 | 65 |
| AMD | 14 | $160.08 | $160.20 | $2,242.80 | 70 |
| AMZN | 10 | $221.65 | $224.08 | $2,240.80 | 75 |
| AVGO | 8 | $275.34 | $283.01 | $2,264.12 | 65 |
| AXP | 7 | $309.18 | $314.18 | $2,199.22 | 70 |
| BA | 9 | $210.81 | $230.18 | $2,071.58 | 65 |
| BAC | 45 | $46.26 | $46.11 | $2,074.95 | 65 |
| C | 30 | $86.85 | $91.03 | $2,730.90 | 85 |
| CAT | 6 | $397.74 | $419.22 | $2,515.32 | 85 |
| COST | 2 | $979.83 | $951.52 | $1,903.05 | 60 |
| CRM | 8 | $267.44 | $259.44 | $2,075.52 | 65 |
| CSCO | 32 | $68.45 | $68.22 | $2,182.88 | 70 |
| CVX | 16 | $146.83 | $149.51 | $2,392.16 | 75 |
| DIS | 18 | $122.77 | $121.35 | $2,184.30 | 70 |
| GOOGL | 13 | $179.34 | $180.95 | $2,352.41 | 75 |
| GS | 3 | $717.52 | $715.47 | $2,146.41 | 75 |
| HD | 6 | $354.18 | $358.84 | $2,153.04 | 65 |
| INTC | 91 | $22.37 | $22.68 | $2,063.43 | 65 |
| JNJ | 13 | $155.43 | $163.33 | $2,123.29 | 70 |
| JPM | 9 | $291.90 | $288.13 | $2,593.20 | 75 |
| KO | 30 | $70.97 | $69.73 | $2,091.90 | 65 |
| LLY | 3 | $781.32 | $780.96 | $2,342.88 | 70 |
| MA | 4 | $563.08 | $554.27 | $2,217.08 | 65 |
| META | 3 | $717.12 | $701.75 | $2,105.24 | 75 |
| MRK | 29 | $82.56 | $82.17 | $2,382.93 | 75 |
| MSFT | 5 | $498.84 | $508.97 | $2,544.86 | 75 |
| NFLX | 1 | $1,279.00 | $1,253.20 | $1,253.20 | 65 |
| NKE | 29 | $71.88 | $72.79 | $2,110.91 | 65 |
| NVDA | 13 | $171.54 | $172.13 | $2,237.63 | 70 |
| ORCL | 9 | $232.99 | $246.70 | $2,220.30 | 75 |
| PEP | 16 | $136.49 | $143.25 | $2,292.00 | 75 |
| PFE | 84 | $25.28 | $24.60 | $2,066.40 | 65 |
| PG | 14 | $152.18 | $154.46 | $2,162.44 | 65 |
| PYPL | 28 | $72.12 | $73.36 | $2,054.08 | 65 |
| QCOM | 14 | $153.83 | $152.89 | $2,140.46 | 65 |
| T | 77 | $27.10 | $26.96 | $2,075.91 | 65 |
| TGT | 21 | $104.77 | $102.71 | $2,156.91 | 65 |
| TSLA | 6 | $318.51 | $322.12 | $1,932.69 | 65 |
| UNH | 7 | $298.51 | $290.13 | $2,030.91 | 65 |
| UNP | 9 | $236.91 | $230.08 | $2,070.72 | 65 |
| V | 6 | $355.85 | $350.38 | $2,102.28 | 65 |
| VZ | 50 | $43.08 | $41.20 | $2,060.24 | 65 |
| WFC | 30 | $78.89 | $80.34 | $2,410.20 | 75 |
| WMT | 22 | $97.29 | $95.18 | $2,093.96 | 65 |
| XOM | 21 | $109.98 | $112.00 | $2,352.00 | 75 |

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
| 2025-07-17 13:49:19 | SELL | NKE | 4 | $72.76 | $3.08 | 65 |
| 2025-07-17 13:49:19 | SELL | UNP | 1 | $230.08 | $-6.14 | 65 |
| 2025-07-17 13:49:19 | BUY | INTC | 7 | $22.67 | N/A | 65 |
| 2025-07-17 13:49:19 | BUY | AXP | 1 | $314.02 | N/A | 70 |
| 2025-07-17 13:49:19 | BUY | CSCO | 1 | $68.18 | N/A | 70 |
| 2025-07-17 13:30:02 | SELL | INTC | 6 | $22.69 | $1.93 | 60 |
| 2025-07-17 13:30:02 | BUY | UNP | 1 | $231.18 | N/A | 75 |
| 2025-07-17 13:04:44 | SELL | BAC | 3 | $46.03 | $-0.64 | 65 |
| 2025-07-17 13:04:44 | SELL | UNP | 1 | $231.18 | $-5.04 | 65 |
| 2025-07-17 13:04:44 | BUY | INTC | 5 | $22.69 | N/A | 65 |
| 2025-07-17 13:04:44 | BUY | NKE | 4 | $72.10 | N/A | 75 |
| 2025-07-17 13:04:44 | BUY | VZ | 3 | $41.25 | N/A | 65 |
| 2025-07-17 13:04:44 | BUY | TGT | 1 | $101.34 | N/A | 70 |
| 2025-07-17 12:32:27 | SELL | VZ | 3 | $41.25 | $-5.49 | 60 |
| 2025-07-17 12:14:03 | SELL | T | 5 | $26.95 | $-0.69 | 65 |
| 2025-07-17 12:14:03 | BUY | BAC | 3 | $46.03 | N/A | 70 |
| 2025-07-17 11:50:40 | SELL | INTC | 1 | $22.69 | $0.34 | 60 |
| 2025-07-17 11:50:40 | SELL | BAC | 1 | $46.03 | $-0.22 | 65 |
| 2025-07-17 11:50:40 | BUY | VZ | 3 | $41.25 | N/A | 65 |
| 2025-07-17 11:50:40 | BUY | T | 5 | $26.95 | N/A | 70 |
| 2025-07-17 11:37:41 | SELL | BAC | 5 | $46.03 | $-1.00 | 65 |
| 2025-07-17 11:37:41 | SELL | INTC | 5 | $22.69 | $1.59 | 60 |
| 2025-07-17 11:37:41 | SELL | VZ | 3 | $41.25 | $-5.49 | 60 |
| 2025-07-17 11:37:41 | BUY | AMD | 1 | $160.08 | N/A | 70 |
| 2025-07-17 11:37:41 | BUY | KO | 1 | $69.27 | N/A | 65 |

<!--TRADE_LOG_END--> 
