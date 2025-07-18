# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 19:09:29**

| Metric | Value |
|---|---|
| **Total Value** | **$101,048.54** |
| Cash | $1,287.26 |
| Holdings Value | $99,761.28 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.94 | $2,109.45 | 65 |
| ADBE | 6 | $375.23 | $366.20 | $2,197.20 | 65 |
| AMD | 14 | $159.84 | $157.38 | $2,203.30 | 70 |
| AMZN | 10 | $221.57 | $225.90 | $2,259.00 | 75 |
| AVGO | 8 | $275.34 | $283.07 | $2,264.56 | 65 |
| AXP | 7 | $309.18 | $307.81 | $2,154.67 | 65 |
| BA | 10 | $232.01 | $229.14 | $2,291.40 | 70 |
| BAC | 48 | $46.29 | $47.35 | $2,273.04 | 70 |
| C | 29 | $86.64 | $93.08 | $2,699.46 | 85 |
| CAT | 6 | $397.74 | $413.06 | $2,478.36 | 70 |
| COST | 2 | $979.83 | $949.76 | $1,899.52 | 65 |
| CRM | 8 | $267.44 | $261.75 | $2,094.00 | 65 |
| CSCO | 31 | $68.61 | $68.11 | $2,111.41 | 65 |
| CVX | 14 | $147.08 | $147.56 | $2,065.84 | 65 |
| DIS | 18 | $122.74 | $121.28 | $2,183.04 | 70 |
| GOOGL | 12 | $178.88 | $184.71 | $2,216.52 | 70 |
| GS | 3 | $717.52 | $708.26 | $2,124.78 | 80 |
| HD | 6 | $354.18 | $357.89 | $2,147.36 | 65 |
| INTC | 90 | $22.38 | $23.21 | $2,088.90 | 65 |
| JNJ | 14 | $155.98 | $163.94 | $2,295.16 | 70 |
| JPM | 8 | $292.14 | $291.54 | $2,332.35 | 75 |
| KO | 30 | $70.96 | $70.08 | $2,102.40 | 65 |
| LLY | 3 | $781.32 | $773.29 | $2,319.87 | 65 |
| MA | 4 | $563.08 | $551.65 | $2,206.60 | 65 |
| META | 3 | $717.12 | $701.97 | $2,105.91 | 65 |
| MRK | 26 | $82.73 | $80.22 | $2,085.72 | 65 |
| MSFT | 5 | $498.84 | $511.81 | $2,559.03 | 85 |
| NFLX | 1 | $1,208.39 | $1,208.00 | $1,208.00 | 65 |
| NKE | 29 | $71.98 | $72.45 | $2,101.05 | 65 |
| NVDA | 14 | $171.77 | $172.06 | $2,408.91 | 70 |
| ORCL | 9 | $232.91 | $246.22 | $2,215.98 | 70 |
| PEP | 15 | $135.89 | $143.86 | $2,157.90 | 65 |
| PFE | 86 | $25.26 | $24.48 | $2,104.85 | 65 |
| PG | 14 | $152.14 | $155.10 | $2,171.40 | 65 |
| PYPL | 32 | $72.39 | $74.15 | $2,372.80 | 75 |
| QCOM | 13 | $153.79 | $154.34 | $2,006.42 | 65 |
| T | 78 | $27.11 | $26.89 | $2,097.81 | 65 |
| TGT | 20 | $104.82 | $102.88 | $2,057.60 | 65 |
| TSLA | 6 | $318.51 | $329.87 | $1,979.22 | 65 |
| UNH | 8 | $283.36 | $282.78 | $2,262.24 | 65 |
| UNP | 9 | $225.02 | $224.37 | $2,019.33 | 65 |
| V | 6 | $355.85 | $348.94 | $2,093.61 | 65 |
| VZ | 51 | $40.87 | $40.71 | $2,076.34 | 65 |
| WFC | 30 | $78.90 | $80.58 | $2,417.55 | 75 |
| WMT | 22 | $97.29 | $95.12 | $2,092.65 | 65 |
| XOM | 19 | $109.80 | $107.83 | $2,048.77 | 65 |

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

<!--TRADE_LOG_END--> 
