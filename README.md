# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 14:53:15**

| Metric | Value |
|---|---|
| **Total Value** | **$100,539.54** |
| Cash | $271.39 |
| Holdings Value | $100,268.15 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.50 | $2,085.00 | 65 |
| ADBE | 6 | $375.23 | $364.82 | $2,188.92 | 65 |
| AMD | 14 | $133.89 | $145.02 | $2,030.28 | 65 |
| AMZN | 11 | $221.92 | $226.20 | $2,488.15 | 75 |
| AVGO | 8 | $275.34 | $274.14 | $2,193.12 | 70 |
| AXP | 7 | $325.34 | $318.81 | $2,231.70 | 75 |
| BA | 10 | $212.59 | $228.51 | $2,285.15 | 70 |
| BAC | 47 | $48.70 | $46.69 | $2,194.35 | 70 |
| C | 31 | $86.64 | $86.66 | $2,686.30 | 85 |
| CAT | 6 | $397.74 | $404.48 | $2,426.88 | 85 |
| COST | 2 | $979.83 | $973.98 | $1,947.95 | 70 |
| CRM | 7 | $268.68 | $260.64 | $1,824.48 | 65 |
| CSCO | 30 | $68.48 | $67.40 | $2,022.00 | 65 |
| CVX | 16 | $146.77 | $152.82 | $2,445.12 | 80 |
| DIS | 18 | $122.79 | $119.83 | $2,156.85 | 70 |
| GOOGL | 13 | $179.57 | $180.69 | $2,348.97 | 75 |
| GS | 3 | $717.52 | $707.95 | $2,123.84 | 75 |
| HD | 6 | $372.64 | $367.33 | $2,203.98 | 65 |
| INTC | 88 | $22.38 | $23.10 | $2,032.62 | 65 |
| JNJ | 13 | $155.95 | $155.85 | $2,026.05 | 65 |
| JPM | 9 | $291.63 | $287.35 | $2,586.15 | 75 |
| KO | 29 | $71.03 | $69.59 | $2,018.25 | 65 |
| LLY | 3 | $781.32 | $793.80 | $2,381.40 | 70 |
| MA | 4 | $563.08 | $555.76 | $2,223.06 | 65 |
| META | 3 | $717.12 | $723.40 | $2,170.20 | 70 |
| MRK | 29 | $82.52 | $83.45 | $2,420.20 | 80 |
| MSFT | 5 | $498.84 | $502.66 | $2,513.30 | 85 |
| NFLX | 1 | $1,279.00 | $1,265.00 | $1,265.00 | 65 |
| NKE | 32 | $72.08 | $72.05 | $2,305.60 | 75 |
| NVDA | 16 | $157.68 | $164.18 | $2,626.80 | 85 |
| ORCL | 9 | $233.26 | $227.88 | $2,050.93 | 65 |
| PEP | 15 | $136.57 | $133.97 | $2,009.55 | 65 |
| PFE | 86 | $25.21 | $25.45 | $2,188.27 | 70 |
| PG | 13 | $160.78 | $153.46 | $1,994.98 | 65 |
| PYPL | 31 | $72.27 | $73.94 | $2,292.14 | 75 |
| QCOM | 13 | $153.79 | $153.79 | $1,999.33 | 65 |
| T | 75 | $27.10 | $27.21 | $2,041.12 | 65 |
| TGT | 20 | $104.94 | $103.82 | $2,076.40 | 65 |
| TSLA | 6 | $288.62 | $314.63 | $1,887.81 | 60 |
| UNH | 7 | $298.51 | $299.50 | $2,096.50 | 65 |
| UNP | 10 | $236.18 | $232.65 | $2,326.45 | 75 |
| V | 6 | $355.85 | $351.26 | $2,107.56 | 65 |
| VZ | 49 | $43.12 | $41.66 | $2,041.59 | 65 |
| WFC | 28 | $82.26 | $82.79 | $2,318.12 | 75 |
| WMT | 21 | $97.38 | $94.99 | $1,994.86 | 65 |
| XOM | 21 | $110.01 | $113.85 | $2,390.85 | 75 |

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
| 2025-07-14 14:26:30 | SELL | AMZN | 1 | $225.53 | $3.31 | 75 |
| 2025-07-14 14:26:30 | SELL | JNJ | 1 | $156.57 | $0.58 | 65 |
| 2025-07-14 14:26:30 | SELL | INTC | 7 | $23.03 | $4.61 | 60 |
| 2025-07-14 14:26:30 | SELL | XOM | 1 | $113.52 | $3.35 | 75 |

<!--TRADE_LOG_END--> 
