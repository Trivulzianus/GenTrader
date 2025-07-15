# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 14:09:21**

| Metric | Value |
|---|---|
| **Total Value** | **$101,026.53** |
| Cash | $1,347.90 |
| Holdings Value | $99,678.63 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.76 | $2,097.60 | 65 |
| ADBE | 6 | $375.23 | $367.86 | $2,207.16 | 65 |
| AMD | 15 | $145.66 | $155.38 | $2,330.70 | 70 |
| AMZN | 10 | $221.56 | $226.96 | $2,269.60 | 75 |
| AVGO | 8 | $275.34 | $280.50 | $2,244.00 | 70 |
| AXP | 7 | $325.34 | $314.64 | $2,202.48 | 70 |
| BA | 10 | $212.74 | $229.59 | $2,295.91 | 70 |
| BAC | 44 | $48.83 | $46.59 | $2,049.90 | 65 |
| C | 30 | $86.79 | $88.25 | $2,647.35 | 85 |
| CAT | 6 | $397.74 | $406.29 | $2,437.74 | 85 |
| COST | 2 | $979.83 | $971.63 | $1,943.26 | 65 |
| CRM | 7 | $268.68 | $259.84 | $1,818.88 | 65 |
| CSCO | 31 | $68.46 | $67.53 | $2,093.28 | 65 |
| CVX | 17 | $147.06 | $151.43 | $2,574.31 | 85 |
| DIS | 17 | $122.96 | $119.49 | $2,031.33 | 65 |
| GOOGL | 14 | $179.74 | $182.31 | $2,552.41 | 85 |
| GS | 3 | $717.52 | $706.94 | $2,120.82 | 75 |
| HD | 6 | $372.64 | $365.99 | $2,195.94 | 65 |
| INTC | 81 | $22.30 | $23.42 | $1,897.02 | 60 |
| JNJ | 13 | $155.95 | $156.38 | $2,033.00 | 65 |
| JPM | 9 | $291.63 | $286.35 | $2,577.15 | 85 |
| KO | 29 | $71.03 | $69.45 | $2,014.19 | 65 |
| LLY | 3 | $781.32 | $797.76 | $2,393.28 | 85 |
| MA | 4 | $563.08 | $552.20 | $2,208.78 | 65 |
| META | 3 | $717.12 | $716.70 | $2,150.10 | 65 |
| MRK | 29 | $82.54 | $83.47 | $2,420.49 | 75 |
| MSFT | 5 | $498.84 | $505.05 | $2,525.25 | 75 |
| NFLX | 1 | $1,279.00 | $1,263.27 | $1,263.27 | 65 |
| NKE | 30 | $72.05 | $72.61 | $2,178.15 | 70 |
| NVDA | 15 | $157.63 | $170.51 | $2,557.59 | 85 |
| ORCL | 9 | $233.27 | $231.20 | $2,080.80 | 65 |
| PEP | 15 | $136.57 | $135.16 | $2,027.40 | 65 |
| PFE | 86 | $25.21 | $25.35 | $2,180.10 | 70 |
| PG | 14 | $160.31 | $153.47 | $2,148.65 | 65 |
| PYPL | 28 | $72.13 | $73.64 | $2,061.89 | 65 |
| QCOM | 14 | $153.83 | $155.64 | $2,178.99 | 70 |
| T | 75 | $27.10 | $27.02 | $2,026.12 | 65 |
| TGT | 20 | $104.94 | $104.61 | $2,092.16 | 65 |
| TSLA | 6 | $318.51 | $318.91 | $1,913.46 | 65 |
| UNH | 7 | $298.51 | $297.23 | $2,080.58 | 65 |
| UNP | 9 | $236.56 | $233.05 | $2,097.45 | 65 |
| V | 6 | $355.85 | $349.40 | $2,096.40 | 65 |
| VZ | 49 | $43.12 | $41.38 | $2,027.62 | 65 |
| WFC | 26 | $83.07 | $79.50 | $2,067.13 | 65 |
| WMT | 21 | $97.38 | $95.32 | $2,001.72 | 65 |
| XOM | 20 | $109.83 | $113.36 | $2,267.20 | 75 |

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
| 2025-07-15 14:09:14 | SELL | BAC | 3 | $46.58 | $-6.33 | 65 |
| 2025-07-15 14:09:14 | SELL | AMD | 1 | $154.88 | $8.64 | 70 |
| 2025-07-15 14:09:14 | SELL | INTC | 6 | $23.41 | $6.18 | 60 |
| 2025-07-15 14:09:14 | SELL | WFC | 6 | $79.52 | $-17.28 | 65 |
| 2025-07-15 14:09:14 | SELL | CSCO | 1 | $67.51 | $-0.92 | 65 |
| 2025-07-15 14:09:14 | BUY | NVDA | 2 | $170.47 | N/A | 85 |
| 2025-07-15 14:09:14 | BUY | CVX | 1 | $151.40 | N/A | 85 |
| 2025-07-15 13:49:01 | SELL | AMZN | 1 | $226.07 | $4.10 | 70 |
| 2025-07-15 13:49:01 | SELL | XOM | 1 | $113.65 | $3.64 | 70 |
| 2025-07-15 13:49:01 | SELL | PYPL | 3 | $73.38 | $3.39 | 65 |
| 2025-07-15 13:49:01 | SELL | NVDA | 1 | $170.90 | $14.16 | 70 |
| 2025-07-15 13:49:01 | SELL | MRK | 2 | $83.67 | $2.12 | 75 |
| 2025-07-15 13:49:01 | SELL | BA | 1 | $229.75 | $15.46 | 70 |
| 2025-07-15 13:49:01 | SELL | CVX | 1 | $151.68 | $4.60 | 75 |
| 2025-07-15 13:49:01 | BUY | TSLA | 6 | $318.51 | N/A | 65 |
| 2025-07-15 13:49:01 | BUY | AMD | 16 | $146.24 | N/A | 75 |
| 2025-07-15 13:49:01 | BUY | BAC | 1 | $46.42 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | NKE | 2 | $72.33 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | PFE | 5 | $25.38 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | C | 5 | $88.64 | N/A | 85 |
| 2025-07-15 13:49:01 | BUY | WFC | 4 | $83.43 | N/A | 85 |
| 2025-07-15 13:49:01 | BUY | CSCO | 2 | $67.42 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | T | 1 | $27.01 | N/A | 65 |
| 2025-07-15 13:48:44 | SELL | TSLA | 6 | $318.64 | $180.11 | 60 |
| 2025-07-15 13:48:38 | SELL | AMD | 15 | $158.18 | $351.98 | 70 |

<!--TRADE_LOG_END--> 
