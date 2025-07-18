# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 17:53:18**

| Metric | Value |
|---|---|
| **Total Value** | **$101,030.02** |
| Cash | $1,187.24 |
| Holdings Value | $99,842.78 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.15 | $2,111.51 | 65 |
| ADBE | 6 | $375.23 | $365.67 | $2,194.02 | 65 |
| AMD | 14 | $159.84 | $157.38 | $2,203.32 | 70 |
| AMZN | 10 | $221.57 | $225.54 | $2,255.40 | 75 |
| AVGO | 8 | $275.34 | $283.42 | $2,267.36 | 65 |
| AXP | 7 | $309.18 | $307.67 | $2,153.69 | 65 |
| BA | 10 | $232.01 | $227.97 | $2,279.66 | 65 |
| BAC | 48 | $46.29 | $47.31 | $2,270.88 | 70 |
| C | 29 | $86.64 | $93.17 | $2,702.07 | 85 |
| CAT | 6 | $397.74 | $412.97 | $2,477.82 | 70 |
| COST | 2 | $979.83 | $952.12 | $1,904.24 | 65 |
| CRM | 8 | $267.44 | $260.04 | $2,080.32 | 65 |
| CSCO | 35 | $68.55 | $68.14 | $2,384.85 | 75 |
| CVX | 16 | $147.06 | $149.70 | $2,395.20 | 75 |
| DIS | 18 | $122.74 | $121.42 | $2,185.65 | 70 |
| GOOGL | 12 | $178.88 | $185.02 | $2,220.29 | 70 |
| GS | 3 | $717.52 | $707.52 | $2,122.56 | 75 |
| HD | 6 | $354.18 | $357.41 | $2,144.46 | 65 |
| INTC | 85 | $22.34 | $23.22 | $1,973.69 | 60 |
| JNJ | 14 | $155.98 | $164.31 | $2,300.34 | 70 |
| JPM | 8 | $292.14 | $291.35 | $2,330.80 | 70 |
| KO | 30 | $70.96 | $70.25 | $2,107.65 | 65 |
| LLY | 3 | $781.32 | $775.00 | $2,325.00 | 65 |
| MA | 4 | $563.08 | $552.38 | $2,209.52 | 65 |
| META | 3 | $717.12 | $698.69 | $2,096.07 | 70 |
| MRK | 26 | $82.73 | $80.28 | $2,087.28 | 65 |
| MSFT | 5 | $498.84 | $510.73 | $2,553.65 | 75 |
| NFLX | 1 | $1,208.39 | $1,216.00 | $1,216.00 | 65 |
| NKE | 29 | $71.98 | $72.53 | $2,103.23 | 65 |
| NVDA | 14 | $171.90 | $172.47 | $2,414.65 | 70 |
| ORCL | 9 | $232.91 | $246.29 | $2,216.65 | 65 |
| PEP | 15 | $135.89 | $143.46 | $2,151.90 | 65 |
| PFE | 86 | $25.26 | $24.45 | $2,102.27 | 65 |
| PG | 14 | $152.14 | $155.11 | $2,171.54 | 65 |
| PYPL | 29 | $72.21 | $73.81 | $2,140.49 | 65 |
| QCOM | 13 | $153.79 | $154.21 | $2,004.73 | 65 |
| T | 78 | $27.11 | $26.93 | $2,100.93 | 65 |
| TGT | 20 | $104.82 | $102.34 | $2,046.80 | 65 |
| TSLA | 6 | $318.51 | $327.94 | $1,967.64 | 65 |
| UNH | 8 | $283.36 | $282.93 | $2,263.44 | 65 |
| UNP | 9 | $225.02 | $222.80 | $2,005.20 | 65 |
| V | 6 | $355.85 | $348.82 | $2,092.92 | 70 |
| VZ | 51 | $40.87 | $40.78 | $2,080.03 | 65 |
| WFC | 27 | $78.72 | $80.47 | $2,172.82 | 65 |
| WMT | 22 | $97.29 | $95.05 | $2,091.02 | 65 |
| XOM | 20 | $109.90 | $108.16 | $2,163.20 | 65 |

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
| 2025-07-18 17:53:12 | SELL | NVDA | 1 | $172.46 | $0.53 | 70 |
| 2025-07-18 17:53:12 | SELL | INTC | 5 | $23.22 | $4.15 | 60 |
| 2025-07-18 17:53:12 | SELL | PYPL | 3 | $73.82 | $4.38 | 65 |
| 2025-07-18 17:53:12 | SELL | WFC | 2 | $80.47 | $3.26 | 65 |
| 2025-07-18 17:53:12 | BUY | PFE | 1 | $24.44 | N/A | 65 |
| 2025-07-18 17:53:12 | BUY | CSCO | 3 | $68.14 | N/A | 75 |
| 2025-07-18 17:40:48 | SELL | KO | 2 | $70.23 | $-1.37 | 65 |
| 2025-07-18 17:40:48 | SELL | PFE | 1 | $24.44 | $-0.82 | 65 |
| 2025-07-18 17:40:48 | SELL | CVX | 1 | $149.87 | $2.64 | 75 |
| 2025-07-18 17:40:48 | SELL | INTC | 1 | $23.29 | $0.90 | 65 |
| 2025-07-18 17:40:48 | SELL | T | 1 | $26.93 | $-0.17 | 65 |
| 2025-07-18 17:40:48 | SELL | VZ | 1 | $40.81 | $-0.05 | 65 |
| 2025-07-18 17:40:48 | BUY | UNH | 1 | $281.89 | N/A | 75 |
| 2025-07-18 17:40:48 | BUY | PYPL | 3 | $74.08 | N/A | 75 |
| 2025-07-18 17:40:48 | BUY | WFC | 1 | $80.50 | N/A | 75 |
| 2025-07-18 17:40:48 | BUY | PG | 1 | $155.14 | N/A | 70 |
| 2025-07-18 17:40:48 | BUY | C | 2 | $93.21 | N/A | 85 |
| 2025-07-18 17:40:48 | BUY | CSCO | 1 | $68.12 | N/A | 70 |
| 2025-07-18 17:26:26 | SELL | JNJ | 1 | $164.11 | $7.59 | 70 |
| 2025-07-18 17:26:26 | SELL | C | 2 | $93.24 | $13.19 | 75 |
| 2025-07-18 17:26:26 | SELL | T | 4 | $26.88 | $-0.88 | 65 |
| 2025-07-18 17:26:26 | BUY | INTC | 8 | $23.20 | N/A | 65 |
| 2025-07-18 17:26:26 | BUY | PFE | 1 | $24.58 | N/A | 65 |
| 2025-07-18 17:26:26 | BUY | KO | 1 | $70.11 | N/A | 70 |
| 2025-07-18 17:26:26 | BUY | CVX | 1 | $149.60 | N/A | 80 |

<!--TRADE_LOG_END--> 
