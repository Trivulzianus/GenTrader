# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 15:27:09**

| Metric | Value |
|---|---|
| **Total Value** | **$100,155.85** |
| Cash | $2,187.34 |
| Holdings Value | $97,968.51 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.84 | $2,098.40 | 70 |
| ADBE | 6 | $375.23 | $360.55 | $2,163.30 | 60 |
| AMD | 14 | $144.36 | $154.36 | $2,161.04 | 70 |
| AMZN | 10 | $221.65 | $223.94 | $2,239.40 | 75 |
| AVGO | 8 | $275.34 | $277.29 | $2,218.32 | 75 |
| AXP | 6 | $308.37 | $308.37 | $1,850.22 | 65 |
| BA | 9 | $210.81 | $228.56 | $2,057.04 | 65 |
| BAC | 45 | $46.28 | $45.28 | $2,037.60 | 65 |
| C | 25 | $86.27 | $88.98 | $2,224.50 | 70 |
| CAT | 6 | $397.74 | $406.00 | $2,436.03 | 85 |
| COST | 2 | $979.83 | $955.94 | $1,911.88 | 70 |
| CRM | 8 | $267.44 | $256.02 | $2,048.16 | 65 |
| CSCO | 31 | $68.46 | $67.23 | $2,084.28 | 65 |
| CVX | 16 | $146.76 | $149.84 | $2,397.36 | 75 |
| DIS | 18 | $122.77 | $119.51 | $2,151.18 | 65 |
| GOOGL | 13 | $179.38 | $183.59 | $2,386.67 | 75 |
| GS | 3 | $717.52 | $697.65 | $2,092.95 | 85 |
| HD | 6 | $372.64 | $354.15 | $2,124.90 | 65 |
| INTC | 85 | $22.36 | $22.43 | $1,906.12 | 60 |
| JNJ | 13 | $155.43 | $164.42 | $2,137.41 | 65 |
| JPM | 9 | $291.63 | $284.75 | $2,562.72 | 75 |
| KO | 30 | $70.97 | $68.95 | $2,068.65 | 65 |
| LLY | 3 | $781.32 | $789.16 | $2,367.48 | 70 |
| MA | 4 | $563.08 | $551.67 | $2,206.68 | 65 |
| META | 3 | $717.12 | $703.69 | $2,111.07 | 75 |
| MRK | 29 | $82.47 | $82.00 | $2,378.00 | 75 |
| MSFT | 5 | $498.84 | $503.86 | $2,519.30 | 85 |
| NFLX | 1 | $1,279.00 | $1,264.02 | $1,264.02 | 65 |
| NKE | 29 | $72.03 | $71.55 | $2,074.95 | 65 |
| NVDA | 14 | $171.57 | $170.24 | $2,383.36 | 70 |
| ORCL | 9 | $233.10 | $234.64 | $2,111.76 | 70 |
| PEP | 15 | $136.57 | $134.14 | $2,012.10 | 65 |
| PFE | 83 | $25.29 | $24.74 | $2,053.42 | 65 |
| PG | 14 | $152.15 | $152.63 | $2,136.82 | 65 |
| PYPL | 29 | $72.15 | $71.94 | $2,086.26 | 65 |
| QCOM | 14 | $153.83 | $152.59 | $2,136.26 | 70 |
| T | 77 | $27.09 | $27.02 | $2,080.54 | 65 |
| TGT | 20 | $104.94 | $100.74 | $2,014.80 | 65 |
| TSLA | 6 | $318.51 | $319.38 | $1,916.30 | 55 |
| UNH | 7 | $298.51 | $291.64 | $2,041.48 | 65 |
| UNP | 9 | $236.78 | $230.51 | $2,074.59 | 65 |
| V | 6 | $355.85 | $347.79 | $2,086.74 | 65 |
| VZ | 50 | $43.08 | $41.26 | $2,063.11 | 65 |
| WFC | 26 | $78.81 | $78.69 | $2,045.81 | 65 |
| WMT | 22 | $97.29 | $94.84 | $2,086.59 | 65 |
| XOM | 21 | $109.99 | $112.33 | $2,358.94 | 75 |

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
| 2025-07-16 15:26:58 | SELL | NVDA | 1 | $170.30 | $-1.19 | 70 |
| 2025-07-16 15:26:58 | SELL | C | 2 | $89.00 | $5.06 | 70 |
| 2025-07-16 15:26:58 | BUY | INTC | 1 | $22.42 | N/A | 60 |
| 2025-07-16 15:26:58 | BUY | AXP | 6 | $308.37 | N/A | 65 |
| 2025-07-16 15:26:33 | SELL | AXP | 7 | $308.53 | $-117.64 | 65 |
| 2025-07-16 15:08:56 | SELL | GOOGL | 1 | $184.08 | $4.37 | 75 |
| 2025-07-16 15:08:56 | SELL | C | 3 | $89.61 | $8.46 | 75 |
| 2025-07-16 15:08:56 | BUY | NVDA | 1 | $170.18 | N/A | 85 |
| 2025-07-16 14:52:56 | SELL | ORCL | 1 | $234.96 | $1.68 | 65 |
| 2025-07-16 14:52:56 | BUY | XOM | 1 | $112.65 | N/A | 75 |
| 2025-07-16 14:40:59 | SELL | NVDA | 1 | $170.23 | $-1.26 | 70 |
| 2025-07-16 14:40:59 | BUY | ORCL | 1 | $234.45 | N/A | 75 |
| 2025-07-16 14:26:09 | SELL | XOM | 1 | $112.84 | $2.84 | 70 |
| 2025-07-16 14:26:09 | SELL | NKE | 1 | $72.13 | $0.10 | 65 |
| 2025-07-16 14:26:09 | BUY | NVDA | 1 | $169.74 | N/A | 85 |
| 2025-07-16 14:08:31 | SELL | INTC | 7 | $22.69 | $2.16 | 60 |
| 2025-07-16 14:08:31 | SELL | AMD | 1 | $154.68 | $9.64 | 65 |
| 2025-07-16 14:08:31 | SELL | PFE | 1 | $24.86 | $-0.42 | 65 |
| 2025-07-16 14:08:31 | SELL | WFC | 1 | $79.43 | $0.60 | 65 |
| 2025-07-16 14:08:31 | SELL | UNP | 1 | $230.54 | $-5.61 | 65 |
| 2025-07-16 14:08:31 | BUY | XOM | 1 | $112.48 | N/A | 75 |
| 2025-07-16 14:08:31 | BUY | NKE | 1 | $72.00 | N/A | 70 |
| 2025-07-16 13:50:09 | SELL | NVDA | 1 | $170.74 | $-0.81 | 70 |
| 2025-07-16 13:50:09 | SELL | JNJ | 1 | $161.91 | $6.02 | 65 |
| 2025-07-16 13:50:09 | SELL | XOM | 1 | $112.87 | $2.85 | 70 |

<!--TRADE_LOG_END--> 
