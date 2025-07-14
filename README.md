# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 16:10:06**

| Metric | Value |
|---|---|
| **Total Value** | **$100,782.12** |
| Cash | $536.00 |
| Holdings Value | $100,246.12 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.16 | $2,091.60 | 65 |
| ADBE | 6 | $375.23 | $365.02 | $2,190.12 | 65 |
| AMD | 15 | $134.72 | $146.53 | $2,197.91 | 70 |
| AMZN | 11 | $221.92 | $225.76 | $2,483.31 | 75 |
| AVGO | 8 | $275.34 | $275.48 | $2,203.84 | 65 |
| AXP | 7 | $325.34 | $321.63 | $2,251.41 | 70 |
| BA | 11 | $214.23 | $230.09 | $2,530.99 | 75 |
| BAC | 47 | $48.71 | $46.94 | $2,205.95 | 70 |
| C | 31 | $86.64 | $87.16 | $2,701.96 | 85 |
| CAT | 6 | $397.74 | $404.15 | $2,424.90 | 70 |
| COST | 2 | $979.83 | $971.55 | $1,943.10 | 70 |
| CRM | 7 | $268.68 | $261.19 | $1,828.31 | 65 |
| CSCO | 31 | $68.48 | $67.43 | $2,090.33 | 65 |
| CVX | 16 | $146.79 | $152.02 | $2,432.32 | 75 |
| DIS | 18 | $122.80 | $120.31 | $2,165.67 | 70 |
| GOOGL | 13 | $179.57 | $180.84 | $2,350.86 | 75 |
| GS | 3 | $717.52 | $712.05 | $2,136.15 | 75 |
| HD | 6 | $372.64 | $367.87 | $2,207.22 | 65 |
| INTC | 87 | $22.38 | $23.18 | $2,016.23 | 65 |
| JNJ | 13 | $155.95 | $155.90 | $2,026.70 | 65 |
| JPM | 9 | $291.63 | $288.27 | $2,594.47 | 85 |
| KO | 29 | $71.03 | $69.66 | $2,020.00 | 65 |
| LLY | 3 | $781.32 | $796.00 | $2,388.00 | 70 |
| MA | 4 | $563.08 | $555.55 | $2,222.20 | 65 |
| META | 3 | $717.12 | $724.77 | $2,174.32 | 75 |
| MRK | 26 | $82.41 | $83.48 | $2,170.60 | 70 |
| MSFT | 5 | $498.84 | $503.31 | $2,516.55 | 75 |
| NFLX | 1 | $1,279.00 | $1,264.57 | $1,264.57 | 65 |
| NKE | 29 | $72.05 | $72.37 | $2,098.73 | 65 |
| NVDA | 16 | $157.68 | $165.08 | $2,641.25 | 85 |
| ORCL | 9 | $233.26 | $230.21 | $2,071.88 | 65 |
| PEP | 15 | $136.57 | $135.32 | $2,029.80 | 65 |
| PFE | 86 | $25.21 | $25.51 | $2,193.58 | 70 |
| PG | 13 | $160.78 | $153.52 | $1,995.76 | 65 |
| PYPL | 28 | $72.13 | $73.54 | $2,059.12 | 65 |
| QCOM | 13 | $153.79 | $153.97 | $2,001.61 | 65 |
| T | 75 | $27.10 | $27.16 | $2,036.62 | 65 |
| TGT | 20 | $104.94 | $104.94 | $2,098.70 | 65 |
| TSLA | 6 | $288.62 | $315.23 | $1,891.38 | 65 |
| UNH | 7 | $298.51 | $299.79 | $2,098.53 | 65 |
| UNP | 10 | $236.27 | $233.34 | $2,333.35 | 75 |
| V | 6 | $355.85 | $351.58 | $2,109.51 | 65 |
| VZ | 49 | $43.12 | $41.59 | $2,038.15 | 65 |
| WFC | 28 | $82.26 | $83.31 | $2,332.82 | 75 |
| WMT | 21 | $97.38 | $95.25 | $2,000.14 | 65 |
| XOM | 21 | $110.01 | $113.60 | $2,385.60 | 75 |

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
| 2025-07-14 16:09:59 | SELL | PYPL | 2 | $73.56 | $2.66 | 65 |
| 2025-07-14 16:09:59 | SELL | NKE | 2 | $72.37 | $0.60 | 65 |
| 2025-07-14 16:09:59 | SELL | CVX | 1 | $152.08 | $4.98 | 75 |
| 2025-07-14 16:09:59 | BUY | BAC | 1 | $46.73 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | AMD | 1 | $146.40 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | DIS | 1 | $120.31 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | MRK | 1 | $83.47 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | UNP | 1 | $233.26 | N/A | 75 |
| 2025-07-14 15:52:17 | SELL | DIS | 1 | $120.24 | $-2.56 | 65 |
| 2025-07-14 15:52:17 | SELL | MRK | 3 | $83.36 | $2.65 | 65 |
| 2025-07-14 15:52:17 | SELL | PYPL | 1 | $73.48 | $1.21 | 70 |
| 2025-07-14 15:52:17 | BUY | BAC | 2 | $46.85 | N/A | 70 |
| 2025-07-14 15:52:17 | BUY | BA | 1 | $230.60 | N/A | 85 |
| 2025-07-14 15:40:20 | SELL | BAC | 2 | $46.81 | $-3.88 | 65 |
| 2025-07-14 15:40:20 | SELL | NKE | 1 | $72.42 | $0.34 | 70 |
| 2025-07-14 15:40:20 | SELL | MRK | 1 | $83.70 | $1.18 | 75 |
| 2025-07-14 15:40:20 | SELL | PFE | 1 | $25.53 | $0.31 | 70 |
| 2025-07-14 15:40:20 | BUY | INTC | 5 | $23.11 | N/A | 65 |
| 2025-07-14 15:40:20 | BUY | PYPL | 1 | $73.52 | N/A | 75 |
| 2025-07-14 15:26:28 | SELL | PYPL | 1 | $73.74 | $1.46 | 70 |
| 2025-07-14 15:26:28 | SELL | PFE | 5 | $25.46 | $1.18 | 70 |
| 2025-07-14 15:26:28 | SELL | UNP | 1 | $232.40 | $-3.78 | 65 |
| 2025-07-14 15:26:28 | SELL | CSCO | 1 | $67.31 | $-1.14 | 65 |
| 2025-07-14 15:26:28 | BUY | BAC | 2 | $46.81 | N/A | 70 |
| 2025-07-14 15:26:28 | BUY | CVX | 1 | $152.33 | N/A | 85 |

<!--TRADE_LOG_END--> 
