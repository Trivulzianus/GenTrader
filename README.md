# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 17:10:54**

| Metric | Value |
|---|---|
| **Total Value** | **$101,510.99** |
| Cash | $2,002.23 |
| Holdings Value | $99,508.76 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.13 | $2,121.30 | 70 |
| ADBE | 5 | $377.60 | $372.45 | $1,862.23 | 65 |
| AMD | 16 | $135.52 | $144.29 | $2,308.58 | 75 |
| AMZN | 10 | $221.91 | $222.40 | $2,224.00 | 75 |
| AVGO | 8 | $275.34 | $274.36 | $2,194.88 | 70 |
| AXP | 7 | $325.28 | $323.78 | $2,266.46 | 75 |
| BA | 9 | $210.97 | $225.10 | $2,025.94 | 70 |
| BAC | 46 | $48.71 | $47.09 | $2,166.37 | 70 |
| C | 27 | $86.81 | $86.82 | $2,344.09 | 75 |
| CAT | 6 | $397.86 | $409.82 | $2,458.95 | 70 |
| COST | 2 | $979.83 | $975.59 | $1,951.18 | 65 |
| CRM | 8 | $268.33 | $266.64 | $2,133.16 | 65 |
| CSCO | 34 | $68.39 | $68.81 | $2,339.71 | 75 |
| CVX | 17 | $147.16 | $153.72 | $2,613.24 | 85 |
| DIS | 18 | $122.80 | $121.41 | $2,185.38 | 70 |
| GOOGL | 13 | $179.61 | $177.23 | $2,303.99 | 75 |
| GS | 3 | $717.52 | $707.87 | $2,123.61 | 75 |
| HD | 6 | $372.64 | $376.40 | $2,258.40 | 70 |
| INTC | 79 | $22.17 | $23.70 | $1,872.13 | 60 |
| JNJ | 13 | $155.89 | $157.70 | $2,050.10 | 65 |
| JPM | 9 | $291.61 | $287.97 | $2,591.73 | 85 |
| KO | 29 | $71.03 | $69.56 | $2,017.10 | 65 |
| LLY | 2 | $776.66 | $792.15 | $1,584.31 | 70 |
| MA | 4 | $563.08 | $563.70 | $2,254.80 | 70 |
| META | 3 | $717.12 | $725.43 | $2,176.29 | 85 |
| MRK | 28 | $82.46 | $84.59 | $2,368.66 | 75 |
| MSFT | 5 | $498.84 | $500.54 | $2,502.69 | 85 |
| NFLX | 1 | $1,279.00 | $1,254.43 | $1,254.43 | 65 |
| NKE | 29 | $75.83 | $75.32 | $2,184.28 | 70 |
| NVDA | 16 | $157.45 | $163.36 | $2,613.76 | 85 |
| ORCL | 9 | $233.31 | $236.47 | $2,128.18 | 70 |
| PEP | 15 | $136.57 | $136.22 | $2,043.30 | 65 |
| PFE | 78 | $25.15 | $25.88 | $2,018.64 | 65 |
| PG | 13 | $160.77 | $159.54 | $2,074.09 | 65 |
| PYPL | 31 | $76.64 | $76.09 | $2,358.79 | 75 |
| QCOM | 15 | $161.71 | $159.76 | $2,396.40 | 75 |
| T | 73 | $28.55 | $27.60 | $2,014.80 | 65 |
| TGT | 19 | $104.85 | $105.95 | $2,013.14 | 65 |
| TSLA | 6 | $288.62 | $302.66 | $1,815.96 | 65 |
| UNH | 6 | $298.34 | $302.76 | $1,816.56 | 65 |
| UNP | 9 | $236.20 | $238.61 | $2,147.49 | 65 |
| V | 6 | $355.85 | $356.69 | $2,140.11 | 70 |
| VZ | 48 | $43.15 | $41.99 | $2,015.76 | 65 |
| WFC | 32 | $82.33 | $82.64 | $2,644.64 | 85 |
| WMT | 21 | $97.36 | $95.80 | $2,011.80 | 65 |
| XOM | 22 | $110.12 | $114.42 | $2,517.35 | 85 |

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
| 2025-07-10 17:10:42 | SELL | INTC | 5 | $23.69 | $7.15 | 60 |
| 2025-07-10 17:10:42 | SELL | PFE | 5 | $25.88 | $3.42 | 65 |
| 2025-07-10 17:10:42 | SELL | C | 3 | $86.82 | $0.04 | 75 |
| 2025-07-10 17:10:42 | BUY | NVDA | 2 | $163.36 | N/A | 85 |
| 2025-07-10 17:10:42 | BUY | AMD | 1 | $144.26 | N/A | 75 |
| 2025-07-10 16:57:22 | SELL | NKE | 1 | $75.32 | $-0.49 | 70 |
| 2025-07-10 16:57:22 | SELL | TGT | 1 | $105.94 | $1.03 | 65 |
| 2025-07-10 16:57:22 | BUY | INTC | 5 | $23.72 | N/A | 65 |
| 2025-07-10 16:57:22 | BUY | XOM | 1 | $114.52 | N/A | 85 |
| 2025-07-10 16:57:22 | BUY | PFE | 5 | $25.81 | N/A | 70 |
| 2025-07-10 16:57:22 | BUY | C | 4 | $86.77 | N/A | 85 |
| 2025-07-10 16:44:03 | SELL | NVDA | 1 | $163.45 | $6.38 | 70 |
| 2025-07-10 16:44:03 | SELL | INTC | 4 | $23.73 | $5.91 | 60 |
| 2025-07-10 16:44:03 | SELL | XOM | 2 | $114.51 | $8.41 | 75 |
| 2025-07-10 16:44:03 | SELL | C | 4 | $86.78 | $-0.13 | 70 |
| 2025-07-10 16:44:03 | SELL | QCOM | 1 | $159.93 | $-1.67 | 75 |
| 2025-07-10 16:44:03 | BUY | PFE | 1 | $25.82 | N/A | 65 |
| 2025-07-10 16:27:11 | SELL | BAC | 1 | $47.10 | $-1.58 | 70 |
| 2025-07-10 16:27:11 | SELL | PFE | 2 | $25.82 | $1.31 | 65 |
| 2025-07-10 16:27:11 | SELL | MRK | 3 | $84.41 | $5.29 | 75 |
| 2025-07-10 16:27:11 | SELL | VZ | 1 | $41.99 | $-1.13 | 65 |
| 2025-07-10 16:27:11 | SELL | T | 1 | $27.58 | $-0.96 | 65 |
| 2025-07-10 16:27:11 | BUY | NVDA | 1 | $163.26 | N/A | 85 |
| 2025-07-10 16:27:11 | BUY | INTC | 3 | $23.72 | N/A | 65 |
| 2025-07-10 16:27:11 | BUY | NKE | 1 | $75.41 | N/A | 75 |

<!--TRADE_LOG_END--> 
