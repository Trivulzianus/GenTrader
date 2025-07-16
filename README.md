# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 17:41:08**

| Metric | Value |
|---|---|
| **Total Value** | **$100,560.65** |
| Cash | $1,819.33 |
| Holdings Value | $98,741.32 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.49 | $2,104.90 | 65 |
| ADBE | 6 | $375.23 | $361.52 | $2,169.15 | 65 |
| AMD | 14 | $144.32 | $155.72 | $2,180.08 | 70 |
| AMZN | 10 | $221.65 | $222.88 | $2,228.80 | 75 |
| AVGO | 8 | $275.34 | $279.35 | $2,234.80 | 70 |
| AXP | 6 | $308.37 | $310.23 | $1,861.38 | 65 |
| BA | 9 | $210.81 | $229.25 | $2,063.25 | 65 |
| BAC | 46 | $46.27 | $45.62 | $2,098.29 | 65 |
| C | 30 | $86.85 | $89.53 | $2,686.05 | 85 |
| CAT | 6 | $397.74 | $410.03 | $2,460.18 | 85 |
| COST | 2 | $979.83 | $955.51 | $1,911.02 | 65 |
| CRM | 8 | $267.44 | $256.39 | $2,051.12 | 65 |
| CSCO | 31 | $68.46 | $67.36 | $2,088.16 | 65 |
| CVX | 16 | $146.83 | $151.01 | $2,416.16 | 75 |
| DIS | 18 | $122.77 | $119.57 | $2,152.18 | 65 |
| GOOGL | 13 | $179.34 | $183.99 | $2,391.87 | 75 |
| GS | 3 | $717.52 | $703.22 | $2,109.66 | 70 |
| HD | 5 | $353.54 | $356.97 | $1,784.85 | 65 |
| INTC | 86 | $22.36 | $22.55 | $1,938.89 | 60 |
| JNJ | 13 | $155.43 | $164.74 | $2,141.62 | 65 |
| JPM | 9 | $291.86 | $285.32 | $2,567.88 | 75 |
| KO | 30 | $70.97 | $69.31 | $2,079.15 | 65 |
| LLY | 3 | $781.32 | $791.20 | $2,373.60 | 70 |
| MA | 4 | $563.08 | $552.64 | $2,210.56 | 65 |
| META | 3 | $717.12 | $702.66 | $2,107.98 | 65 |
| MRK | 29 | $82.47 | $82.34 | $2,388.01 | 75 |
| MSFT | 5 | $498.84 | $505.64 | $2,528.18 | 85 |
| NFLX | 1 | $1,279.00 | $1,255.02 | $1,255.02 | 65 |
| NKE | 29 | $72.00 | $71.88 | $2,084.52 | 65 |
| NVDA | 14 | $171.55 | $170.84 | $2,391.69 | 70 |
| ORCL | 9 | $232.99 | $237.98 | $2,141.82 | 70 |
| PEP | 15 | $136.57 | $135.04 | $2,025.60 | 65 |
| PFE | 85 | $25.27 | $24.71 | $2,100.35 | 65 |
| PG | 13 | $152.06 | $153.24 | $1,992.12 | 65 |
| PYPL | 29 | $72.15 | $72.64 | $2,106.68 | 65 |
| QCOM | 14 | $153.83 | $153.47 | $2,148.65 | 65 |
| T | 77 | $27.10 | $27.04 | $2,082.08 | 65 |
| TGT | 20 | $104.94 | $101.22 | $2,024.40 | 65 |
| TSLA | 6 | $318.51 | $320.15 | $1,920.88 | 65 |
| UNH | 7 | $298.51 | $294.30 | $2,060.10 | 65 |
| UNP | 10 | $236.22 | $231.22 | $2,312.15 | 65 |
| V | 6 | $355.85 | $349.25 | $2,095.50 | 70 |
| VZ | 50 | $43.08 | $41.35 | $2,067.75 | 65 |
| WFC | 27 | $78.80 | $79.50 | $2,146.50 | 65 |
| WMT | 22 | $97.29 | $94.89 | $2,087.47 | 65 |
| XOM | 21 | $110.01 | $112.87 | $2,370.27 | 75 |

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
| 2025-07-16 17:41:01 | SELL | T | 1 | $27.04 | $-0.05 | 65 |
| 2025-07-16 17:26:01 | SELL | NVDA | 1 | $171.06 | $-0.45 | 70 |
| 2025-07-16 17:26:01 | SELL | ORCL | 1 | $237.70 | $4.24 | 65 |
| 2025-07-16 17:26:01 | SELL | T | 4 | $27.06 | $-0.15 | 65 |
| 2025-07-16 17:26:01 | BUY | INTC | 1 | $22.62 | N/A | 60 |
| 2025-07-16 17:26:01 | BUY | PFE | 1 | $24.72 | N/A | 65 |
| 2025-07-16 17:26:01 | BUY | CVX | 1 | $150.98 | N/A | 75 |
| 2025-07-16 17:10:45 | SELL | NKE | 1 | $72.04 | $0.04 | 65 |
| 2025-07-16 17:10:45 | SELL | PFE | 1 | $24.70 | $-0.57 | 65 |
| 2025-07-16 17:10:45 | SELL | PG | 1 | $153.29 | $1.14 | 60 |
| 2025-07-16 17:10:45 | BUY | NVDA | 2 | $171.34 | N/A | 85 |
| 2025-07-16 17:10:45 | BUY | XOM | 1 | $113.14 | N/A | 75 |
| 2025-07-16 17:10:45 | BUY | UNP | 1 | $231.21 | N/A | 75 |
| 2025-07-16 17:10:45 | BUY | T | 5 | $27.08 | N/A | 70 |
| 2025-07-16 17:10:45 | BUY | ORCL | 1 | $237.66 | N/A | 75 |
| 2025-07-16 16:57:30 | SELL | NVDA | 1 | $171.12 | $-0.39 | 65 |
| 2025-07-16 16:57:30 | SELL | AMD | 1 | $155.31 | $10.25 | 65 |
| 2025-07-16 16:57:30 | SELL | NKE | 1 | $71.62 | $-0.37 | 65 |
| 2025-07-16 16:57:30 | SELL | CVX | 1 | $150.95 | $4.13 | 70 |
| 2025-07-16 16:57:30 | BUY | PFE | 1 | $24.68 | N/A | 65 |
| 2025-07-16 16:44:38 | SELL | NVDA | 1 | $170.57 | $-0.88 | 70 |
| 2025-07-16 16:44:38 | BUY | JPM | 1 | $285.90 | N/A | 85 |
| 2025-07-16 16:27:27 | SELL | BAC | 6 | $45.40 | $-4.57 | 65 |
| 2025-07-16 16:27:27 | SELL | XOM | 1 | $112.82 | $2.82 | 70 |
| 2025-07-16 16:27:27 | BUY | GOOGL | 1 | $183.03 | N/A | 75 |

<!--TRADE_LOG_END--> 
