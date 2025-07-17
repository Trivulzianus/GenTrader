# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 19:25:30**

| Metric | Value |
|---|---|
| **Total Value** | **$101,450.40** |
| Cash | $559.06 |
| Holdings Value | $100,891.35 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.91 | $2,109.15 | 65 |
| ADBE | 6 | $375.23 | $365.81 | $2,194.89 | 65 |
| AMD | 14 | $160.03 | $159.66 | $2,235.23 | 70 |
| AMZN | 10 | $221.65 | $223.77 | $2,237.70 | 75 |
| AVGO | 8 | $275.34 | $286.33 | $2,290.64 | 65 |
| AXP | 7 | $309.18 | $315.39 | $2,207.76 | 75 |
| BA | 9 | $232.13 | $232.32 | $2,090.88 | 70 |
| BAC | 46 | $46.26 | $47.02 | $2,162.92 | 70 |
| C | 29 | $86.64 | $92.84 | $2,692.51 | 85 |
| CAT | 6 | $397.74 | $418.62 | $2,511.72 | 75 |
| COST | 2 | $979.83 | $951.98 | $1,903.95 | 65 |
| CRM | 8 | $267.44 | $259.74 | $2,077.92 | 65 |
| CSCO | 33 | $68.56 | $68.28 | $2,253.40 | 70 |
| CVX | 16 | $146.82 | $151.66 | $2,426.56 | 80 |
| DIS | 20 | $122.61 | $121.77 | $2,435.30 | 75 |
| GOOGL | 13 | $179.34 | $183.90 | $2,390.64 | 75 |
| GS | 3 | $717.52 | $706.81 | $2,120.43 | 80 |
| HD | 6 | $354.18 | $359.17 | $2,155.02 | 65 |
| INTC | 84 | $22.34 | $22.77 | $1,912.26 | 60 |
| JNJ | 13 | $155.43 | $163.42 | $2,124.46 | 70 |
| JPM | 9 | $291.90 | $289.77 | $2,607.93 | 85 |
| KO | 30 | $70.97 | $70.46 | $2,113.80 | 65 |
| LLY | 3 | $781.32 | $761.51 | $2,284.53 | 65 |
| MA | 4 | $563.08 | $557.36 | $2,229.42 | 65 |
| META | 3 | $717.12 | $701.39 | $2,104.17 | 70 |
| MRK | 29 | $82.56 | $81.62 | $2,366.98 | 75 |
| MSFT | 5 | $498.84 | $512.12 | $2,560.60 | 85 |
| NFLX | 1 | $1,279.00 | $1,272.41 | $1,272.41 | 65 |
| NKE | 32 | $71.99 | $73.00 | $2,336.00 | 75 |
| NVDA | 14 | $171.69 | $173.25 | $2,425.53 | 75 |
| ORCL | 9 | $232.91 | $248.99 | $2,240.89 | 75 |
| PEP | 16 | $136.49 | $145.55 | $2,328.80 | 75 |
| PFE | 84 | $25.28 | $24.57 | $2,063.46 | 65 |
| PG | 14 | $152.18 | $155.35 | $2,174.90 | 65 |
| PYPL | 32 | $72.34 | $74.03 | $2,368.80 | 75 |
| QCOM | 14 | $153.83 | $152.52 | $2,135.28 | 65 |
| T | 76 | $27.10 | $27.00 | $2,051.62 | 65 |
| TGT | 20 | $104.83 | $103.48 | $2,069.70 | 65 |
| TSLA | 6 | $318.51 | $318.79 | $1,912.71 | 60 |
| UNH | 7 | $298.51 | $287.70 | $2,013.90 | 65 |
| UNP | 9 | $237.31 | $227.66 | $2,048.94 | 65 |
| V | 6 | $355.85 | $351.00 | $2,106.03 | 65 |
| VZ | 49 | $40.87 | $41.06 | $2,011.94 | 65 |
| WFC | 29 | $78.80 | $79.78 | $2,313.48 | 75 |
| WMT | 22 | $97.29 | $95.09 | $2,092.09 | 65 |
| XOM | 19 | $109.79 | $111.80 | $2,124.11 | 65 |

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
| 2025-07-17 19:25:18 | SELL | NVDA | 1 | $173.28 | $1.48 | 75 |
| 2025-07-17 19:25:18 | SELL | XOM | 2 | $111.81 | $3.66 | 65 |
| 2025-07-17 19:25:18 | SELL | CSCO | 1 | $68.29 | $-0.27 | 70 |
| 2025-07-17 19:25:18 | BUY | BAC | 2 | $47.01 | N/A | 70 |
| 2025-07-17 19:25:18 | BUY | WFC | 1 | $79.79 | N/A | 75 |
| 2025-07-17 19:25:18 | BUY | VZ | 2 | $41.04 | N/A | 65 |
| 2025-07-17 19:08:19 | SELL | INTC | 5 | $22.80 | $2.13 | 60 |
| 2025-07-17 19:08:19 | SELL | BAC | 2 | $47.15 | $1.78 | 65 |
| 2025-07-17 19:08:19 | SELL | WMT | 1 | $95.40 | $-1.81 | 65 |
| 2025-07-17 19:08:19 | SELL | BA | 1 | $232.16 | $0.04 | 65 |
| 2025-07-17 19:08:19 | SELL | VZ | 3 | $41.06 | $0.58 | 60 |
| 2025-07-17 19:08:19 | BUY | NVDA | 2 | $173.41 | N/A | 85 |
| 2025-07-17 19:08:19 | BUY | NKE | 4 | $73.05 | N/A | 75 |
| 2025-07-17 18:47:04 | SELL | NKE | 4 | $73.06 | $4.28 | 65 |
| 2025-07-17 18:47:04 | SELL | PFE | 1 | $24.54 | $-0.73 | 65 |
| 2025-07-17 18:47:04 | SELL | C | 1 | $92.71 | $5.87 | 85 |
| 2025-07-17 18:47:04 | SELL | UNP | 1 | $227.55 | $-8.78 | 65 |
| 2025-07-17 18:47:04 | SELL | T | 1 | $26.98 | $-0.11 | 65 |
| 2025-07-17 18:47:04 | BUY | INTC | 5 | $22.82 | N/A | 65 |
| 2025-07-17 18:47:04 | BUY | BAC | 2 | $47.10 | N/A | 70 |
| 2025-07-17 18:47:04 | BUY | WMT | 2 | $95.35 | N/A | 70 |
| 2025-07-17 18:47:04 | BUY | BA | 1 | $232.04 | N/A | 75 |
| 2025-07-17 18:47:04 | BUY | CSCO | 2 | $68.33 | N/A | 75 |
| 2025-07-17 18:28:18 | SELL | NVDA | 2 | $173.20 | $2.86 | 70 |
| 2025-07-17 18:28:18 | SELL | BAC | 1 | $47.17 | $0.91 | 65 |

<!--TRADE_LOG_END--> 
