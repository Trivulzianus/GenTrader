# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 19:51:24**

| Metric | Value |
|---|---|
| **Total Value** | **$101,093.64** |
| Cash | $588.54 |
| Holdings Value | $100,505.10 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.20 | $2,112.02 | 65 |
| ADBE | 6 | $375.23 | $365.33 | $2,191.98 | 65 |
| AMD | 14 | $159.84 | $157.20 | $2,200.80 | 70 |
| AMZN | 11 | $221.97 | $226.10 | $2,487.15 | 75 |
| AVGO | 8 | $275.34 | $283.80 | $2,270.40 | 70 |
| AXP | 7 | $309.18 | $308.10 | $2,156.71 | 65 |
| BA | 10 | $232.01 | $228.72 | $2,287.15 | 65 |
| BAC | 48 | $46.29 | $47.32 | $2,271.45 | 70 |
| C | 29 | $86.63 | $93.34 | $2,707.01 | 85 |
| CAT | 6 | $397.74 | $413.79 | $2,482.74 | 75 |
| COST | 2 | $979.83 | $950.85 | $1,901.70 | 65 |
| CRM | 8 | $267.44 | $262.57 | $2,100.56 | 65 |
| CSCO | 33 | $68.58 | $68.13 | $2,248.29 | 70 |
| CVX | 14 | $147.08 | $148.65 | $2,081.03 | 65 |
| DIS | 19 | $122.65 | $121.16 | $2,301.95 | 70 |
| GOOGL | 13 | $179.34 | $184.97 | $2,404.61 | 75 |
| GS | 3 | $717.52 | $708.14 | $2,124.43 | 75 |
| HD | 6 | $354.18 | $359.19 | $2,155.14 | 65 |
| INTC | 90 | $22.38 | $23.20 | $2,088.45 | 65 |
| JNJ | 14 | $155.98 | $163.69 | $2,291.66 | 70 |
| JPM | 8 | $292.14 | $291.48 | $2,331.84 | 75 |
| KO | 30 | $70.96 | $69.94 | $2,098.05 | 65 |
| LLY | 3 | $781.32 | $775.01 | $2,325.05 | 65 |
| MA | 4 | $563.08 | $552.75 | $2,211.00 | 65 |
| META | 3 | $717.12 | $703.25 | $2,109.75 | 65 |
| MRK | 26 | $82.73 | $80.05 | $2,081.30 | 65 |
| MSFT | 5 | $498.84 | $510.16 | $2,550.80 | 85 |
| NFLX | 1 | $1,208.39 | $1,208.96 | $1,208.96 | 65 |
| NKE | 31 | $72.01 | $72.48 | $2,246.73 | 70 |
| NVDA | 14 | $171.78 | $172.09 | $2,409.19 | 70 |
| ORCL | 9 | $232.91 | $245.92 | $2,213.28 | 70 |
| PEP | 15 | $135.89 | $143.60 | $2,154.00 | 65 |
| PFE | 86 | $25.26 | $24.47 | $2,104.42 | 65 |
| PG | 14 | $152.14 | $155.37 | $2,175.13 | 65 |
| PYPL | 29 | $72.21 | $74.16 | $2,150.49 | 65 |
| QCOM | 13 | $153.79 | $154.59 | $2,009.67 | 65 |
| T | 78 | $27.11 | $26.92 | $2,100.09 | 65 |
| TGT | 20 | $104.82 | $103.15 | $2,063.00 | 65 |
| TSLA | 6 | $318.51 | $329.17 | $1,975.02 | 65 |
| UNH | 8 | $283.36 | $282.11 | $2,256.86 | 65 |
| UNP | 9 | $225.02 | $224.93 | $2,024.33 | 65 |
| V | 6 | $355.85 | $349.00 | $2,094.03 | 65 |
| VZ | 51 | $40.87 | $40.77 | $2,079.01 | 65 |
| WFC | 30 | $78.90 | $80.64 | $2,419.35 | 75 |
| WMT | 22 | $97.29 | $95.06 | $2,091.43 | 65 |
| XOM | 20 | $109.72 | $107.86 | $2,157.10 | 65 |

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
| 2025-07-18 19:51:18 | BUY | NKE | 2 | $72.48 | N/A | 70 |
| 2025-07-18 19:36:26 | SELL | AMZN | 1 | $225.95 | $3.65 | 75 |
| 2025-07-18 19:36:26 | SELL | NVDA | 1 | $171.99 | $0.20 | 70 |
| 2025-07-18 19:36:26 | SELL | PYPL | 3 | $74.15 | $5.29 | 65 |
| 2025-07-18 19:36:26 | BUY | DIS | 1 | $121.18 | N/A | 75 |
| 2025-07-18 19:36:26 | BUY | C | 3 | $93.09 | N/A | 85 |
| 2025-07-18 19:36:26 | BUY | CSCO | 2 | $68.11 | N/A | 70 |
| 2025-07-18 19:24:57 | SELL | C | 3 | $93.17 | $19.60 | 75 |
| 2025-07-18 19:24:57 | BUY | AMZN | 2 | $225.93 | N/A | 85 |
| 2025-07-18 19:24:57 | BUY | NVDA | 1 | $172.15 | N/A | 85 |
| 2025-07-18 19:24:57 | BUY | GOOGL | 1 | $184.87 | N/A | 75 |
| 2025-07-18 19:24:57 | BUY | XOM | 1 | $108.14 | N/A | 70 |
| 2025-07-18 19:09:24 | SELL | NVDA | 2 | $173.00 | $2.16 | 70 |
| 2025-07-18 19:09:24 | SELL | XOM | 1 | $111.66 | $1.76 | 65 |
| 2025-07-18 19:09:24 | BUY | PYPL | 3 | $74.15 | N/A | 75 |
| 2025-07-18 19:09:24 | BUY | WFC | 2 | $80.58 | N/A | 75 |
| 2025-07-18 18:57:56 | SELL | BAC | 1 | $47.31 | $1.01 | 70 |
| 2025-07-18 18:57:56 | SELL | CVX | 1 | $146.95 | $-0.12 | 60 |
| 2025-07-18 18:57:56 | BUY | NVDA | 2 | $172.08 | N/A | 85 |
| 2025-07-18 18:57:56 | BUY | WFC | 1 | $80.47 | N/A | 70 |
| 2025-07-18 18:45:25 | SELL | BAC | 2 | $47.34 | $1.98 | 70 |
| 2025-07-18 18:45:25 | SELL | WFC | 1 | $80.39 | $1.62 | 65 |
| 2025-07-18 18:45:25 | SELL | CVX | 1 | $146.93 | $-0.13 | 65 |
| 2025-07-18 18:27:27 | BUY | BAC | 3 | $47.28 | N/A | 75 |
| 2025-07-18 18:27:27 | BUY | C | 2 | $93.11 | N/A | 85 |

<!--TRADE_LOG_END--> 
