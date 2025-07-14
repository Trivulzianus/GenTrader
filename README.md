# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 15:09:34**

| Metric | Value |
|---|---|
| **Total Value** | **$100,603.91** |
| Cash | $261.77 |
| Holdings Value | $100,342.14 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.49 | $2,084.90 | 65 |
| ADBE | 6 | $375.23 | $364.52 | $2,187.13 | 65 |
| AMD | 14 | $133.89 | $145.41 | $2,035.74 | 65 |
| AMZN | 11 | $221.92 | $226.39 | $2,490.29 | 75 |
| AVGO | 8 | $275.34 | $276.52 | $2,212.16 | 70 |
| AXP | 7 | $325.34 | $319.63 | $2,237.41 | 65 |
| BA | 10 | $212.59 | $228.71 | $2,287.10 | 70 |
| BAC | 44 | $48.83 | $46.76 | $2,057.22 | 65 |
| C | 31 | $86.64 | $86.83 | $2,691.73 | 85 |
| CAT | 6 | $397.74 | $403.61 | $2,421.63 | 70 |
| COST | 2 | $979.83 | $974.11 | $1,948.22 | 70 |
| CRM | 7 | $268.68 | $259.74 | $1,818.18 | 65 |
| CSCO | 32 | $68.45 | $67.41 | $2,157.12 | 70 |
| CVX | 16 | $146.77 | $152.63 | $2,442.08 | 80 |
| DIS | 18 | $122.79 | $119.82 | $2,156.76 | 70 |
| GOOGL | 13 | $179.57 | $180.38 | $2,344.94 | 75 |
| GS | 3 | $717.52 | $709.72 | $2,129.16 | 75 |
| HD | 6 | $372.64 | $367.67 | $2,206.02 | 65 |
| INTC | 82 | $22.33 | $23.12 | $1,896.25 | 60 |
| JNJ | 13 | $155.95 | $155.82 | $2,025.66 | 65 |
| JPM | 9 | $291.63 | $287.60 | $2,588.40 | 85 |
| KO | 29 | $71.03 | $69.59 | $2,018.25 | 65 |
| LLY | 3 | $781.32 | $796.75 | $2,390.25 | 70 |
| MA | 4 | $563.08 | $554.52 | $2,218.08 | 65 |
| META | 3 | $717.12 | $727.18 | $2,181.54 | 75 |
| MRK | 29 | $82.52 | $83.57 | $2,423.57 | 75 |
| MSFT | 5 | $498.84 | $503.39 | $2,516.95 | 75 |
| NFLX | 1 | $1,279.00 | $1,269.20 | $1,269.20 | 65 |
| NKE | 32 | $72.08 | $72.28 | $2,312.96 | 75 |
| NVDA | 16 | $157.68 | $164.83 | $2,637.29 | 85 |
| ORCL | 9 | $233.26 | $228.42 | $2,055.78 | 65 |
| PEP | 15 | $136.57 | $134.13 | $2,011.95 | 65 |
| PFE | 92 | $25.22 | $25.46 | $2,342.32 | 75 |
| PG | 13 | $160.78 | $153.12 | $1,990.56 | 65 |
| PYPL | 31 | $72.27 | $73.63 | $2,282.53 | 75 |
| QCOM | 13 | $153.79 | $153.58 | $1,996.54 | 65 |
| T | 75 | $27.10 | $27.21 | $2,041.12 | 65 |
| TGT | 20 | $104.94 | $104.08 | $2,081.50 | 65 |
| TSLA | 6 | $288.62 | $314.10 | $1,884.60 | 60 |
| UNH | 7 | $298.51 | $299.29 | $2,095.03 | 65 |
| UNP | 10 | $236.18 | $232.03 | $2,320.35 | 75 |
| V | 6 | $355.85 | $350.61 | $2,103.66 | 70 |
| VZ | 49 | $43.12 | $41.62 | $2,039.62 | 65 |
| WFC | 28 | $82.26 | $82.83 | $2,319.38 | 75 |
| WMT | 21 | $97.38 | $95.23 | $1,999.93 | 65 |
| XOM | 21 | $110.01 | $113.86 | $2,391.06 | 75 |

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
| 2025-07-14 15:09:27 | SELL | INTC | 6 | $23.11 | $4.39 | 60 |
| 2025-07-14 15:09:27 | SELL | BAC | 3 | $46.76 | $-5.84 | 65 |
| 2025-07-14 15:09:27 | BUY | PFE | 6 | $25.44 | N/A | 75 |
| 2025-07-14 15:09:27 | BUY | CSCO | 2 | $67.95 | N/A | 70 |
| 2025-07-14 14:53:08 | SELL | GOOGL | 1 | $180.70 | $1.05 | 75 |
| 2025-07-14 14:53:08 | SELL | AMD | 1 | $144.98 | $10.35 | 65 |
| 2025-07-14 14:53:08 | SELL | INTC | 1 | $23.10 | $0.71 | 65 |
| 2025-07-14 14:53:08 | SELL | TGT | 1 | $103.82 | $-1.06 | 65 |
| 2025-07-14 14:53:08 | BUY | NVDA | 3 | $164.12 | N/A | 85 |
| 2025-07-14 14:53:08 | BUY | DIS | 1 | $119.82 | N/A | 70 |
| 2025-07-14 14:53:08 | BUY | PYPL | 1 | $73.98 | N/A | 75 |
| 2025-07-14 14:53:08 | BUY | MRK | 1 | $83.46 | N/A | 80 |
| 2025-07-14 14:53:08 | BUY | NKE | 3 | $72.06 | N/A | 75 |
| 2025-07-14 14:53:08 | BUY | CAT | 1 | $404.48 | N/A | 85 |
| 2025-07-14 14:53:08 | BUY | QCOM | 13 | $153.79 | N/A | 65 |
| 2025-07-14 14:52:53 | SELL | QCOM | 14 | $153.75 | $-116.71 | 65 |
| 2025-07-14 14:41:26 | SELL | NVDA | 2 | $163.70 | $13.00 | 65 |
| 2025-07-14 14:41:26 | SELL | NKE | 1 | $72.14 | $0.06 | 65 |
| 2025-07-14 14:41:26 | SELL | PYPL | 1 | $74.27 | $1.99 | 70 |
| 2025-07-14 14:41:26 | SELL | CVX | 1 | $153.43 | $6.27 | 75 |
| 2025-07-14 14:41:26 | BUY | INTC | 8 | $23.12 | N/A | 65 |
| 2025-07-14 14:41:26 | BUY | PFE | 1 | $25.55 | N/A | 70 |
| 2025-07-14 14:41:26 | BUY | C | 1 | $86.73 | N/A | 85 |
| 2025-07-14 14:41:26 | BUY | VZ | 4 | $41.78 | N/A | 65 |
| 2025-07-14 14:41:26 | BUY | TGT | 1 | $104.26 | N/A | 70 |

<!--TRADE_LOG_END--> 
