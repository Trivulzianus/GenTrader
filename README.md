# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 16:27:16**

| Metric | Value |
|---|---|
| **Total Value** | **$100,972.21** |
| Cash | $941.44 |
| Holdings Value | $100,030.77 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.82 | $2,108.20 | 65 |
| ADBE | 6 | $375.23 | $364.83 | $2,189.01 | 65 |
| AMD | 14 | $159.84 | $158.21 | $2,214.94 | 70 |
| AMZN | 10 | $221.57 | $224.62 | $2,246.20 | 75 |
| AVGO | 8 | $275.34 | $282.75 | $2,262.00 | 70 |
| AXP | 7 | $309.18 | $306.44 | $2,145.08 | 65 |
| BA | 10 | $232.01 | $228.72 | $2,287.20 | 65 |
| BAC | 51 | $46.35 | $47.20 | $2,406.95 | 75 |
| C | 29 | $86.64 | $93.42 | $2,709.32 | 85 |
| CAT | 6 | $397.74 | $414.70 | $2,488.20 | 70 |
| COST | 2 | $979.83 | $953.21 | $1,906.42 | 65 |
| CRM | 8 | $267.44 | $259.41 | $2,075.28 | 65 |
| CSCO | 33 | $68.56 | $68.20 | $2,250.52 | 70 |
| CVX | 17 | $147.15 | $149.35 | $2,538.95 | 75 |
| DIS | 18 | $122.74 | $121.14 | $2,180.52 | 65 |
| GOOGL | 13 | $179.34 | $184.87 | $2,403.31 | 70 |
| GS | 3 | $717.52 | $708.28 | $2,124.84 | 75 |
| HD | 6 | $354.18 | $357.03 | $2,142.17 | 65 |
| INTC | 90 | $22.39 | $23.19 | $2,087.10 | 65 |
| JNJ | 14 | $155.97 | $163.98 | $2,295.72 | 70 |
| JPM | 8 | $292.14 | $291.49 | $2,331.88 | 70 |
| KO | 32 | $70.92 | $70.20 | $2,246.40 | 70 |
| LLY | 3 | $781.32 | $770.44 | $2,311.32 | 65 |
| MA | 4 | $563.08 | $551.35 | $2,205.40 | 65 |
| META | 3 | $717.12 | $698.52 | $2,095.56 | 70 |
| MRK | 26 | $82.73 | $80.36 | $2,089.36 | 65 |
| MSFT | 5 | $498.84 | $508.45 | $2,542.25 | 75 |
| NFLX | 1 | $1,208.39 | $1,214.38 | $1,214.38 | 65 |
| NKE | 29 | $71.98 | $72.40 | $2,099.59 | 65 |
| NVDA | 14 | $171.92 | $172.06 | $2,408.84 | 70 |
| ORCL | 9 | $232.91 | $246.09 | $2,214.81 | 70 |
| PEP | 15 | $135.89 | $143.65 | $2,154.75 | 65 |
| PFE | 80 | $25.32 | $24.43 | $1,954.41 | 60 |
| PG | 13 | $151.91 | $154.84 | $2,012.92 | 65 |
| PYPL | 29 | $72.18 | $73.81 | $2,140.63 | 65 |
| QCOM | 14 | $153.83 | $154.12 | $2,157.61 | 65 |
| T | 78 | $27.10 | $27.00 | $2,105.61 | 65 |
| TGT | 20 | $104.82 | $102.19 | $2,043.80 | 65 |
| TSLA | 6 | $318.51 | $327.74 | $1,966.44 | 65 |
| UNH | 7 | $283.57 | $282.88 | $1,980.14 | 65 |
| UNP | 9 | $225.02 | $224.01 | $2,016.09 | 65 |
| V | 6 | $355.85 | $347.82 | $2,086.92 | 65 |
| VZ | 51 | $40.87 | $40.83 | $2,082.09 | 65 |
| WFC | 28 | $78.78 | $80.32 | $2,248.96 | 70 |
| WMT | 22 | $97.29 | $95.19 | $2,094.07 | 65 |
| XOM | 20 | $109.90 | $108.23 | $2,164.60 | 65 |

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
| 2025-07-18 16:27:10 | SELL | NVDA | 1 | $172.01 | $0.08 | 70 |
| 2025-07-18 16:27:10 | SELL | PFE | 5 | $24.42 | $-4.21 | 60 |
| 2025-07-18 16:27:10 | BUY | KO | 2 | $70.18 | N/A | 70 |
| 2025-07-18 16:27:10 | BUY | INTC | 7 | $23.18 | N/A | 65 |
| 2025-07-18 16:27:10 | BUY | WFC | 2 | $80.35 | N/A | 70 |
| 2025-07-18 16:27:10 | BUY | VZ | 3 | $40.83 | N/A | 65 |
| 2025-07-18 16:10:58 | SELL | AMZN | 1 | $225.05 | $3.16 | 70 |
| 2025-07-18 16:10:58 | SELL | NKE | 2 | $72.50 | $0.98 | 65 |
| 2025-07-18 16:10:58 | SELL | WFC | 1 | $80.27 | $1.55 | 65 |
| 2025-07-18 16:10:58 | SELL | VZ | 3 | $40.84 | $-0.08 | 60 |
| 2025-07-18 15:53:05 | SELL | INTC | 7 | $23.44 | $7.19 | 60 |
| 2025-07-18 15:53:05 | SELL | CVX | 1 | $150.71 | $3.36 | 75 |
| 2025-07-18 15:53:05 | BUY | NVDA | 2 | $172.51 | N/A | 85 |
| 2025-07-18 15:53:05 | BUY | UNH | 7 | $283.57 | N/A | 65 |
| 2025-07-18 15:53:05 | BUY | NKE | 2 | $72.36 | N/A | 70 |
| 2025-07-18 15:53:05 | BUY | CSCO | 2 | $68.33 | N/A | 70 |
| 2025-07-18 15:52:44 | SELL | UNH | 7 | $283.57 | $-104.53 | 65 |
| 2025-07-18 15:39:48 | SELL | NKE | 1 | $72.44 | $0.43 | 65 |
| 2025-07-18 15:39:48 | SELL | T | 5 | $26.97 | $-0.65 | 65 |
| 2025-07-18 15:39:48 | SELL | CSCO | 2 | $68.29 | $-0.55 | 65 |
| 2025-07-18 15:39:48 | BUY | BAC | 6 | $47.12 | N/A | 75 |
| 2025-07-18 15:39:48 | BUY | CVX | 1 | $150.86 | N/A | 85 |
| 2025-07-18 15:26:20 | SELL | BAC | 3 | $47.08 | $2.33 | 65 |
| 2025-07-18 15:26:20 | SELL | NKE | 3 | $72.32 | $0.86 | 65 |
| 2025-07-18 15:26:20 | SELL | KO | 4 | $70.38 | $-2.08 | 65 |

<!--TRADE_LOG_END--> 
