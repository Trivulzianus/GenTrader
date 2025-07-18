# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 18:58:01**

| Metric | Value |
|---|---|
| **Total Value** | **$101,012.12** |
| Cash | $1,213.22 |
| Holdings Value | $99,798.90 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.94 | $2,109.35 | 65 |
| ADBE | 6 | $375.23 | $366.00 | $2,196.03 | 65 |
| AMD | 14 | $159.84 | $157.31 | $2,202.34 | 70 |
| AMZN | 10 | $221.57 | $225.79 | $2,257.95 | 75 |
| AVGO | 8 | $275.34 | $282.96 | $2,263.68 | 70 |
| AXP | 7 | $309.18 | $307.97 | $2,155.79 | 65 |
| BA | 10 | $232.01 | $229.15 | $2,291.50 | 65 |
| BAC | 48 | $46.29 | $47.31 | $2,271.12 | 70 |
| C | 29 | $86.64 | $93.01 | $2,697.29 | 85 |
| CAT | 6 | $397.74 | $412.98 | $2,477.88 | 70 |
| COST | 2 | $979.83 | $950.74 | $1,901.48 | 65 |
| CRM | 8 | $267.44 | $261.48 | $2,091.84 | 65 |
| CSCO | 31 | $68.61 | $68.08 | $2,110.33 | 65 |
| CVX | 14 | $147.08 | $147.01 | $2,058.14 | 60 |
| DIS | 18 | $122.74 | $121.22 | $2,181.96 | 70 |
| GOOGL | 12 | $178.88 | $184.66 | $2,215.92 | 70 |
| GS | 3 | $717.52 | $708.23 | $2,124.69 | 70 |
| HD | 6 | $354.18 | $358.07 | $2,148.42 | 65 |
| INTC | 90 | $22.38 | $23.18 | $2,085.75 | 65 |
| JNJ | 14 | $155.98 | $163.77 | $2,292.78 | 70 |
| JPM | 8 | $292.14 | $291.46 | $2,331.68 | 75 |
| KO | 30 | $70.96 | $70.15 | $2,104.50 | 65 |
| LLY | 3 | $781.32 | $773.74 | $2,321.22 | 65 |
| MA | 4 | $563.08 | $552.00 | $2,208.00 | 65 |
| META | 3 | $717.12 | $700.98 | $2,102.94 | 75 |
| MRK | 26 | $82.73 | $80.25 | $2,086.63 | 65 |
| MSFT | 5 | $498.84 | $511.48 | $2,557.40 | 75 |
| NFLX | 1 | $1,208.39 | $1,208.91 | $1,208.91 | 65 |
| NKE | 29 | $71.98 | $72.51 | $2,102.83 | 65 |
| NVDA | 16 | $171.92 | $172.09 | $2,753.36 | 85 |
| ORCL | 9 | $232.91 | $246.31 | $2,216.79 | 75 |
| PEP | 15 | $135.89 | $143.67 | $2,155.05 | 65 |
| PFE | 86 | $25.26 | $24.44 | $2,101.84 | 65 |
| PG | 14 | $152.14 | $155.09 | $2,171.19 | 65 |
| PYPL | 29 | $72.21 | $74.00 | $2,145.86 | 65 |
| QCOM | 13 | $153.79 | $154.07 | $2,002.91 | 65 |
| T | 78 | $27.11 | $26.93 | $2,100.93 | 65 |
| TGT | 20 | $104.82 | $102.78 | $2,055.60 | 65 |
| TSLA | 6 | $318.51 | $330.17 | $1,981.02 | 65 |
| UNH | 8 | $283.36 | $282.91 | $2,263.28 | 65 |
| UNP | 9 | $225.02 | $224.17 | $2,017.53 | 60 |
| V | 6 | $355.85 | $349.30 | $2,095.80 | 65 |
| VZ | 51 | $40.87 | $40.76 | $2,078.51 | 65 |
| WFC | 28 | $78.78 | $80.47 | $2,253.30 | 70 |
| WMT | 22 | $97.29 | $95.14 | $2,093.19 | 65 |
| XOM | 20 | $109.90 | $107.72 | $2,154.40 | 65 |

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
| 2025-07-18 18:57:56 | SELL | BAC | 1 | $47.31 | $1.01 | 70 |
| 2025-07-18 18:57:56 | SELL | CVX | 1 | $146.95 | $-0.12 | 60 |
| 2025-07-18 18:57:56 | BUY | NVDA | 2 | $172.08 | N/A | 85 |
| 2025-07-18 18:57:56 | BUY | WFC | 1 | $80.47 | N/A | 70 |
| 2025-07-18 18:45:25 | SELL | BAC | 2 | $47.34 | $1.98 | 70 |
| 2025-07-18 18:45:25 | SELL | WFC | 1 | $80.39 | $1.62 | 65 |
| 2025-07-18 18:45:25 | SELL | CVX | 1 | $146.93 | $-0.13 | 65 |
| 2025-07-18 18:27:27 | BUY | BAC | 3 | $47.28 | N/A | 75 |
| 2025-07-18 18:27:27 | BUY | C | 2 | $93.11 | N/A | 85 |
| 2025-07-18 18:27:27 | BUY | WFC | 1 | $80.35 | N/A | 70 |
| 2025-07-18 18:10:57 | SELL | C | 2 | $93.21 | $13.13 | 75 |
| 2025-07-18 18:10:57 | SELL | CSCO | 4 | $68.07 | $-1.94 | 65 |
| 2025-07-18 18:10:57 | BUY | INTC | 5 | $23.18 | N/A | 65 |
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

<!--TRADE_LOG_END--> 
