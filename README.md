# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 16:27:33**

| Metric | Value |
|---|---|
| **Total Value** | **$100,304.31** |
| Cash | $1,874.71 |
| Holdings Value | $98,429.60 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.63 | $2,096.30 | 65 |
| ADBE | 6 | $375.23 | $360.93 | $2,165.55 | 65 |
| AMD | 15 | $145.06 | $154.44 | $2,316.54 | 70 |
| AMZN | 10 | $221.65 | $223.28 | $2,232.80 | 75 |
| AVGO | 8 | $275.34 | $277.30 | $2,218.40 | 70 |
| AXP | 6 | $308.37 | $309.11 | $1,854.66 | 65 |
| BA | 9 | $210.81 | $228.75 | $2,058.80 | 65 |
| BAC | 46 | $46.27 | $45.41 | $2,088.86 | 65 |
| C | 30 | $86.85 | $89.25 | $2,677.50 | 85 |
| CAT | 6 | $397.74 | $408.12 | $2,448.75 | 70 |
| COST | 2 | $979.83 | $954.55 | $1,909.10 | 65 |
| CRM | 8 | $267.44 | $255.83 | $2,046.62 | 65 |
| CSCO | 31 | $68.46 | $67.23 | $2,084.28 | 65 |
| CVX | 16 | $146.82 | $150.89 | $2,414.24 | 75 |
| DIS | 18 | $122.77 | $119.39 | $2,149.02 | 65 |
| GOOGL | 13 | $179.34 | $183.04 | $2,379.52 | 75 |
| GS | 3 | $717.52 | $701.86 | $2,105.57 | 75 |
| HD | 5 | $353.54 | $355.99 | $1,779.95 | 65 |
| INTC | 85 | $22.36 | $22.48 | $1,910.80 | 60 |
| JNJ | 13 | $155.43 | $164.79 | $2,142.27 | 70 |
| JPM | 8 | $292.60 | $285.63 | $2,285.08 | 75 |
| KO | 30 | $70.97 | $69.14 | $2,074.17 | 65 |
| LLY | 3 | $781.32 | $791.67 | $2,375.01 | 65 |
| MA | 4 | $563.08 | $552.10 | $2,208.38 | 65 |
| META | 3 | $717.12 | $701.66 | $2,104.99 | 75 |
| MRK | 29 | $82.47 | $81.82 | $2,372.72 | 75 |
| MSFT | 5 | $498.84 | $503.78 | $2,518.90 | 75 |
| NFLX | 1 | $1,279.00 | $1,262.65 | $1,262.65 | 65 |
| NKE | 31 | $71.99 | $71.72 | $2,223.32 | 70 |
| NVDA | 15 | $171.45 | $170.34 | $2,555.05 | 85 |
| ORCL | 9 | $232.99 | $236.15 | $2,125.35 | 65 |
| PEP | 15 | $136.57 | $134.54 | $2,018.10 | 65 |
| PFE | 84 | $25.28 | $24.66 | $2,071.44 | 65 |
| PG | 14 | $152.15 | $152.84 | $2,139.77 | 65 |
| PYPL | 29 | $72.15 | $72.29 | $2,096.41 | 65 |
| QCOM | 14 | $153.83 | $152.93 | $2,141.08 | 65 |
| T | 77 | $27.09 | $27.04 | $2,082.08 | 65 |
| TGT | 20 | $104.94 | $100.56 | $2,011.11 | 65 |
| TSLA | 6 | $318.51 | $321.04 | $1,926.24 | 65 |
| UNH | 7 | $298.51 | $292.67 | $2,048.66 | 65 |
| UNP | 9 | $236.78 | $230.54 | $2,074.86 | 65 |
| V | 6 | $355.85 | $348.80 | $2,092.80 | 65 |
| VZ | 50 | $43.08 | $41.31 | $2,065.75 | 65 |
| WFC | 27 | $78.80 | $79.01 | $2,133.27 | 65 |
| WMT | 22 | $97.29 | $94.84 | $2,086.48 | 65 |
| XOM | 20 | $109.85 | $112.82 | $2,256.40 | 70 |

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
| 2025-07-16 16:27:27 | SELL | BAC | 6 | $45.40 | $-4.57 | 65 |
| 2025-07-16 16:27:27 | SELL | XOM | 1 | $112.82 | $2.82 | 70 |
| 2025-07-16 16:27:27 | BUY | GOOGL | 1 | $183.03 | N/A | 75 |
| 2025-07-16 16:27:27 | BUY | NKE | 2 | $71.71 | N/A | 70 |
| 2025-07-16 16:27:27 | BUY | C | 1 | $89.26 | N/A | 85 |
| 2025-07-16 16:10:20 | SELL | GOOGL | 1 | $183.52 | $4.15 | 65 |
| 2025-07-16 16:10:20 | SELL | INTC | 1 | $22.47 | $0.11 | 60 |
| 2025-07-16 16:10:20 | SELL | NKE | 2 | $71.78 | $-0.42 | 65 |
| 2025-07-16 16:10:20 | SELL | WFC | 1 | $78.95 | $0.15 | 65 |
| 2025-07-16 16:10:20 | BUY | NVDA | 2 | $170.34 | N/A | 85 |
| 2025-07-16 16:10:20 | BUY | AMD | 1 | $154.88 | N/A | 75 |
| 2025-07-16 16:10:20 | BUY | BAC | 6 | $45.49 | N/A | 75 |
| 2025-07-16 16:10:20 | BUY | C | 2 | $90.72 | N/A | 85 |
| 2025-07-16 15:52:09 | SELL | NVDA | 3 | $170.08 | $-3.74 | 65 |
| 2025-07-16 15:52:09 | SELL | ORCL | 1 | $235.34 | $2.11 | 65 |
| 2025-07-16 15:52:09 | SELL | CVX | 2 | $150.21 | $6.01 | 75 |
| 2025-07-16 15:52:09 | BUY | NKE | 2 | $71.46 | N/A | 70 |
| 2025-07-16 15:52:09 | BUY | C | 3 | $88.84 | N/A | 75 |
| 2025-07-16 15:52:09 | BUY | WFC | 2 | $78.71 | N/A | 70 |
| 2025-07-16 15:40:59 | SELL | JPM | 1 | $283.89 | $-7.74 | 70 |
| 2025-07-16 15:40:59 | SELL | C | 1 | $88.51 | $2.24 | 65 |
| 2025-07-16 15:40:59 | BUY | NVDA | 2 | $169.67 | N/A | 85 |
| 2025-07-16 15:40:59 | BUY | BAC | 1 | $45.12 | N/A | 65 |
| 2025-07-16 15:40:59 | BUY | INTC | 1 | $22.30 | N/A | 60 |
| 2025-07-16 15:40:59 | BUY | HD | 5 | $353.54 | N/A | 65 |

<!--TRADE_LOG_END--> 
