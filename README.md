# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 14:26:36**

| Metric | Value |
|---|---|
| **Total Value** | **$100,566.17** |
| Cash | $997.24 |
| Holdings Value | $99,568.93 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.24 | $2,082.35 | 65 |
| ADBE | 6 | $375.23 | $364.27 | $2,185.65 | 65 |
| AMD | 15 | $134.63 | $144.16 | $2,162.32 | 70 |
| AMZN | 11 | $221.92 | $225.32 | $2,478.52 | 75 |
| AVGO | 8 | $275.34 | $274.21 | $2,193.72 | 70 |
| AXP | 7 | $325.34 | $319.62 | $2,237.34 | 75 |
| BA | 10 | $212.59 | $228.95 | $2,289.50 | 70 |
| BAC | 47 | $48.70 | $46.67 | $2,193.72 | 70 |
| C | 30 | $86.64 | $86.65 | $2,599.50 | 85 |
| CAT | 5 | $396.39 | $405.42 | $2,027.10 | 70 |
| COST | 2 | $979.83 | $976.38 | $1,952.76 | 65 |
| CRM | 7 | $268.68 | $261.18 | $1,828.23 | 65 |
| CSCO | 30 | $68.48 | $67.63 | $2,028.90 | 65 |
| CVX | 17 | $147.16 | $152.38 | $2,590.55 | 85 |
| DIS | 17 | $122.97 | $120.05 | $2,040.85 | 65 |
| GOOGL | 14 | $179.65 | $180.54 | $2,527.56 | 85 |
| GS | 3 | $717.52 | $708.08 | $2,124.24 | 85 |
| HD | 6 | $372.64 | $368.85 | $2,213.10 | 70 |
| INTC | 81 | $22.32 | $23.04 | $1,865.84 | 60 |
| JNJ | 13 | $155.95 | $156.61 | $2,035.93 | 65 |
| JPM | 9 | $291.63 | $287.37 | $2,586.33 | 85 |
| KO | 29 | $71.03 | $69.70 | $2,021.44 | 65 |
| LLY | 3 | $781.32 | $795.82 | $2,387.45 | 70 |
| MA | 4 | $563.08 | $557.33 | $2,229.32 | 65 |
| META | 3 | $717.12 | $721.54 | $2,164.62 | 70 |
| MRK | 28 | $82.49 | $83.55 | $2,339.40 | 75 |
| MSFT | 5 | $498.84 | $502.22 | $2,511.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,265.40 | $1,265.40 | 65 |
| NKE | 30 | $72.08 | $71.88 | $2,156.40 | 70 |
| NVDA | 15 | $157.20 | $163.85 | $2,457.75 | 80 |
| ORCL | 9 | $233.26 | $226.23 | $2,036.07 | 70 |
| PEP | 15 | $136.57 | $134.16 | $2,012.33 | 65 |
| PFE | 85 | $25.21 | $25.46 | $2,164.53 | 70 |
| PG | 13 | $160.78 | $153.82 | $1,999.66 | 65 |
| PYPL | 31 | $72.28 | $74.17 | $2,299.27 | 75 |
| QCOM | 14 | $162.09 | $154.15 | $2,158.03 | 65 |
| T | 75 | $27.10 | $27.28 | $2,046.14 | 65 |
| TGT | 20 | $104.91 | $103.39 | $2,067.80 | 65 |
| TSLA | 6 | $288.62 | $313.71 | $1,882.26 | 65 |
| UNH | 7 | $298.51 | $300.37 | $2,102.59 | 65 |
| UNP | 10 | $236.18 | $233.54 | $2,335.45 | 70 |
| V | 6 | $355.85 | $351.77 | $2,110.62 | 65 |
| VZ | 45 | $43.24 | $41.77 | $1,879.42 | 60 |
| WFC | 28 | $82.26 | $82.72 | $2,316.02 | 75 |
| WMT | 21 | $97.38 | $95.10 | $1,997.10 | 65 |
| XOM | 21 | $110.01 | $113.56 | $2,384.76 | 75 |

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
| 2025-07-14 14:26:30 | SELL | AMZN | 1 | $225.53 | $3.31 | 75 |
| 2025-07-14 14:26:30 | SELL | JNJ | 1 | $156.57 | $0.58 | 65 |
| 2025-07-14 14:26:30 | SELL | INTC | 7 | $23.03 | $4.61 | 60 |
| 2025-07-14 14:26:30 | SELL | XOM | 1 | $113.52 | $3.35 | 75 |
| 2025-07-14 14:26:30 | SELL | DIS | 1 | $120.04 | $-2.77 | 65 |
| 2025-07-14 14:26:30 | SELL | PFE | 1 | $25.65 | $0.44 | 70 |
| 2025-07-14 14:26:30 | SELL | CSCO | 3 | $67.64 | $-2.30 | 65 |
| 2025-07-14 14:26:30 | SELL | VZ | 1 | $41.76 | $-1.45 | 60 |
| 2025-07-14 14:26:30 | BUY | NVDA | 2 | $163.91 | N/A | 80 |
| 2025-07-14 14:26:30 | BUY | PYPL | 3 | $74.12 | N/A | 75 |
| 2025-07-14 14:26:30 | BUY | NKE | 2 | $71.85 | N/A | 70 |
| 2025-07-14 14:26:30 | BUY | C | 3 | $86.65 | N/A | 85 |
| 2025-07-14 14:09:17 | SELL | PYPL | 4 | $73.70 | $5.64 | 65 |
| 2025-07-14 14:09:17 | SELL | VZ | 3 | $41.74 | $-4.11 | 60 |
| 2025-07-14 14:09:17 | SELL | T | 1 | $27.40 | $0.29 | 65 |
| 2025-07-14 14:09:17 | BUY | XOM | 1 | $114.01 | N/A | 80 |
| 2025-07-14 14:09:17 | BUY | C | 1 | $86.29 | N/A | 75 |
| 2025-07-14 14:09:17 | BUY | WFC | 1 | $82.58 | N/A | 75 |
| 2025-07-14 13:48:21 | SELL | NVDA | 3 | $162.65 | $15.79 | 65 |
| 2025-07-14 13:48:21 | SELL | WFC | 1 | $82.75 | $0.48 | 70 |
| 2025-07-14 13:48:21 | SELL | CSCO | 1 | $67.74 | $-0.64 | 70 |
| 2025-07-14 13:48:21 | SELL | QCOM | 1 | $154.02 | $-7.52 | 65 |
| 2025-07-14 13:48:21 | BUY | JNJ | 1 | $157.31 | N/A | 70 |
| 2025-07-14 13:48:21 | BUY | AMZN | 1 | $225.02 | N/A | 85 |
| 2025-07-14 13:48:21 | BUY | INTC | 1 | $23.43 | N/A | 65 |

<!--TRADE_LOG_END--> 
