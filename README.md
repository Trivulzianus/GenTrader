# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 15:51:55**

| Metric | Value |
|---|---|
| **Total Value** | **$100,792.32** |
| Cash | $1,046.67 |
| Holdings Value | $99,745.65 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.43 | $2,114.25 | 70 |
| ADBE | 6 | $375.23 | $365.49 | $2,192.94 | 65 |
| AMD | 17 | $146.29 | $155.72 | $2,647.23 | 85 |
| AMZN | 10 | $221.60 | $226.97 | $2,269.70 | 75 |
| AVGO | 8 | $275.34 | $281.60 | $2,252.80 | 65 |
| AXP | 7 | $325.34 | $314.12 | $2,198.84 | 65 |
| BA | 11 | $214.40 | $230.76 | $2,538.36 | 80 |
| BAC | 45 | $48.78 | $46.65 | $2,099.03 | 65 |
| C | 30 | $86.78 | $90.38 | $2,711.40 | 85 |
| CAT | 6 | $397.74 | $406.81 | $2,440.83 | 85 |
| COST | 2 | $979.83 | $969.05 | $1,938.10 | 65 |
| CRM | 8 | $267.44 | $259.03 | $2,072.24 | 65 |
| CSCO | 31 | $68.46 | $67.53 | $2,093.43 | 65 |
| CVX | 16 | $146.80 | $151.11 | $2,417.76 | 75 |
| DIS | 17 | $122.96 | $119.35 | $2,028.87 | 65 |
| GOOGL | 14 | $179.71 | $183.72 | $2,572.15 | 85 |
| GS | 3 | $717.52 | $706.98 | $2,120.93 | 75 |
| HD | 6 | $372.64 | $364.31 | $2,185.86 | 65 |
| INTC | 82 | $22.31 | $23.42 | $1,920.44 | 60 |
| JNJ | 13 | $155.95 | $155.19 | $2,017.53 | 65 |
| JPM | 9 | $291.63 | $287.69 | $2,589.21 | 85 |
| KO | 30 | $70.97 | $69.28 | $2,078.25 | 65 |
| LLY | 3 | $781.32 | $775.18 | $2,325.55 | 65 |
| MA | 4 | $563.08 | $550.48 | $2,201.92 | 65 |
| META | 3 | $717.12 | $718.67 | $2,156.01 | 70 |
| MRK | 25 | $82.54 | $81.47 | $2,036.83 | 65 |
| MSFT | 5 | $498.84 | $506.85 | $2,534.24 | 75 |
| NFLX | 1 | $1,279.00 | $1,261.30 | $1,261.30 | 65 |
| NKE | 30 | $72.04 | $72.14 | $2,164.05 | 70 |
| NVDA | 13 | $171.78 | $171.19 | $2,225.53 | 70 |
| ORCL | 9 | $233.27 | $232.09 | $2,088.86 | 65 |
| PEP | 15 | $136.57 | $134.16 | $2,012.40 | 65 |
| PFE | 83 | $25.22 | $24.73 | $2,053.01 | 65 |
| PG | 13 | $152.12 | $152.70 | $1,985.10 | 65 |
| PYPL | 28 | $72.13 | $73.73 | $2,064.57 | 65 |
| QCOM | 14 | $153.83 | $154.87 | $2,168.18 | 70 |
| T | 82 | $27.08 | $26.85 | $2,201.70 | 70 |
| TGT | 20 | $104.94 | $103.45 | $2,069.10 | 65 |
| TSLA | 6 | $318.51 | $313.89 | $1,883.34 | 60 |
| UNH | 7 | $298.51 | $294.76 | $2,063.32 | 65 |
| UNP | 9 | $236.54 | $233.17 | $2,098.53 | 65 |
| V | 6 | $355.85 | $347.89 | $2,087.37 | 65 |
| VZ | 50 | $43.08 | $41.22 | $2,060.75 | 65 |
| WFC | 27 | $78.71 | $78.92 | $2,130.84 | 65 |
| WMT | 21 | $97.38 | $95.19 | $1,998.88 | 65 |
| XOM | 21 | $109.99 | $113.05 | $2,374.12 | 75 |

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
| 2025-07-15 15:51:49 | SELL | BAC | 2 | $46.65 | $-4.09 | 65 |
| 2025-07-15 15:51:49 | SELL | PYPL | 1 | $73.72 | $1.53 | 65 |
| 2025-07-15 15:51:49 | BUY | NKE | 1 | $72.13 | N/A | 70 |
| 2025-07-15 15:51:49 | BUY | BA | 2 | $230.76 | N/A | 80 |
| 2025-07-15 15:51:49 | BUY | T | 5 | $26.86 | N/A | 70 |
| 2025-07-15 15:40:17 | SELL | NVDA | 1 | $171.33 | $-0.42 | 70 |
| 2025-07-15 15:40:17 | SELL | INTC | 6 | $23.37 | $5.90 | 60 |
| 2025-07-15 15:40:17 | SELL | PYPL | 1 | $73.64 | $1.41 | 65 |
| 2025-07-15 15:40:17 | SELL | WFC | 1 | $78.91 | $0.19 | 65 |
| 2025-07-15 15:40:17 | BUY | GOOGL | 1 | $183.45 | N/A | 85 |
| 2025-07-15 15:40:17 | BUY | BAC | 3 | $46.65 | N/A | 70 |
| 2025-07-15 15:26:50 | SELL | GOOGL | 1 | $183.84 | $4.10 | 75 |
| 2025-07-15 15:26:50 | SELL | NKE | 2 | $72.35 | $0.59 | 65 |
| 2025-07-15 15:26:50 | SELL | UNP | 1 | $232.75 | $-3.41 | 65 |
| 2025-07-15 15:26:50 | BUY | INTC | 5 | $23.38 | N/A | 65 |
| 2025-07-15 15:26:50 | BUY | PYPL | 1 | $73.56 | N/A | 70 |
| 2025-07-15 15:26:50 | BUY | WFC | 28 | $78.72 | N/A | 70 |
| 2025-07-15 15:26:26 | SELL | WFC | 27 | $78.75 | $-112.80 | 65 |
| 2025-07-15 15:08:18 | SELL | CVX | 2 | $151.18 | $7.79 | 75 |
| 2025-07-15 15:08:18 | BUY | AMD | 1 | $155.67 | N/A | 85 |
| 2025-07-15 15:08:18 | BUY | C | 3 | $89.11 | N/A | 85 |
| 2025-07-15 15:08:18 | BUY | UNP | 1 | $232.60 | N/A | 75 |
| 2025-07-15 14:52:34 | SELL | NVDA | 1 | $171.28 | $-0.44 | 70 |
| 2025-07-15 14:52:34 | SELL | INTC | 5 | $23.39 | $5.02 | 60 |
| 2025-07-15 14:52:34 | SELL | WFC | 1 | $78.90 | $-3.87 | 65 |

<!--TRADE_LOG_END--> 
