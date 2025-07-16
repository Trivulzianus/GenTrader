# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 13:30:10**

| Metric | Value |
|---|---|
| **Total Value** | **$100,558.48** |
| Cash | $277.93 |
| Holdings Value | $100,280.55 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.29 | $2,102.90 | 70 |
| ADBE | 6 | $375.23 | $364.57 | $2,187.42 | 70 |
| AMD | 15 | $145.04 | $155.61 | $2,334.15 | 70 |
| AMZN | 10 | $221.65 | $225.88 | $2,258.75 | 75 |
| AVGO | 8 | $275.34 | $280.11 | $2,240.88 | 70 |
| AXP | 7 | $325.34 | $312.00 | $2,184.00 | 65 |
| BA | 10 | $212.82 | $232.23 | $2,322.32 | 65 |
| BAC | 45 | $46.28 | $46.19 | $2,078.55 | 65 |
| C | 30 | $86.78 | $91.53 | $2,745.90 | 85 |
| CAT | 6 | $397.74 | $405.50 | $2,433.00 | 70 |
| COST | 2 | $979.83 | $967.68 | $1,935.36 | 70 |
| CRM | 8 | $267.44 | $258.97 | $2,071.76 | 65 |
| CSCO | 31 | $68.46 | $67.18 | $2,082.58 | 65 |
| CVX | 17 | $147.01 | $150.69 | $2,561.73 | 85 |
| DIS | 18 | $122.77 | $118.98 | $2,141.64 | 70 |
| GOOGL | 14 | $179.71 | $183.25 | $2,565.50 | 75 |
| GS | 3 | $717.52 | $702.51 | $2,107.53 | 65 |
| HD | 6 | $372.64 | $359.86 | $2,159.13 | 65 |
| INTC | 84 | $22.36 | $22.99 | $1,931.16 | 60 |
| JNJ | 14 | $155.89 | $155.17 | $2,172.38 | 65 |
| JPM | 9 | $291.63 | $286.55 | $2,578.95 | 85 |
| KO | 30 | $70.97 | $69.36 | $2,080.80 | 65 |
| LLY | 3 | $781.32 | $771.75 | $2,315.25 | 65 |
| MA | 4 | $563.08 | $550.36 | $2,201.44 | 65 |
| META | 3 | $717.12 | $713.37 | $2,140.11 | 65 |
| MRK | 26 | $82.50 | $81.45 | $2,117.83 | 65 |
| MSFT | 5 | $498.84 | $505.82 | $2,529.10 | 75 |
| NFLX | 1 | $1,279.00 | $1,260.27 | $1,260.27 | 65 |
| NKE | 29 | $72.03 | $72.25 | $2,095.39 | 65 |
| NVDA | 15 | $171.55 | $171.03 | $2,565.45 | 85 |
| ORCL | 9 | $233.15 | $235.55 | $2,119.95 | 65 |
| PEP | 15 | $136.57 | $133.97 | $2,009.62 | 65 |
| PFE | 85 | $25.28 | $24.68 | $2,097.38 | 65 |
| PG | 14 | $152.15 | $152.69 | $2,137.66 | 65 |
| PYPL | 29 | $72.15 | $72.96 | $2,115.84 | 65 |
| QCOM | 14 | $153.83 | $154.30 | $2,160.20 | 65 |
| T | 77 | $27.09 | $27.00 | $2,079.38 | 65 |
| TGT | 20 | $104.94 | $102.55 | $2,050.90 | 65 |
| TSLA | 6 | $318.51 | $312.88 | $1,877.28 | 65 |
| UNH | 7 | $298.51 | $293.10 | $2,051.70 | 65 |
| UNP | 9 | $236.68 | $232.77 | $2,094.93 | 65 |
| V | 6 | $355.85 | $347.38 | $2,084.28 | 65 |
| VZ | 50 | $43.08 | $41.25 | $2,062.50 | 65 |
| WFC | 30 | $78.89 | $78.86 | $2,365.80 | 75 |
| WMT | 22 | $97.29 | $95.49 | $2,100.78 | 65 |
| XOM | 21 | $110.02 | $112.91 | $2,371.11 | 75 |

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
| 2025-07-16 13:30:02 | SELL | BAC | 3 | $46.15 | $-0.37 | 65 |
| 2025-07-16 13:30:02 | BUY | NVDA | 1 | $170.70 | N/A | 85 |
| 2025-07-16 13:30:02 | BUY | WFC | 2 | $78.86 | N/A | 75 |
| 2025-07-16 13:04:56 | SELL | UNP | 1 | $231.14 | $-4.99 | 65 |
| 2025-07-16 13:04:56 | SELL | T | 1 | $27.02 | $-0.07 | 65 |
| 2025-07-16 13:04:56 | BUY | WFC | 1 | $78.86 | N/A | 70 |
| 2025-07-16 13:04:56 | BUY | BA | 1 | $230.00 | N/A | 75 |
| 2025-07-16 12:32:59 | SELL | CVX | 1 | $150.69 | $3.48 | 75 |
| 2025-07-16 12:32:59 | BUY | BAC | 2 | $46.15 | N/A | 70 |
| 2025-07-16 12:14:16 | SELL | WFC | 3 | $78.86 | $-0.10 | 65 |
| 2025-07-16 12:14:16 | SELL | T | 4 | $27.02 | $-0.28 | 65 |
| 2025-07-16 12:14:16 | BUY | JPM | 1 | $286.55 | N/A | 85 |
| 2025-07-16 12:14:16 | BUY | AMD | 1 | $155.61 | N/A | 75 |
| 2025-07-16 12:14:16 | BUY | CVX | 2 | $150.69 | N/A | 85 |
| 2025-07-16 11:50:24 | SELL | CVX | 2 | $150.69 | $6.96 | 75 |
| 2025-07-16 11:50:24 | BUY | WFC | 2 | $78.86 | N/A | 75 |
| 2025-07-16 11:50:24 | BUY | T | 5 | $27.02 | N/A | 70 |
| 2025-07-16 11:37:29 | SELL | GOOGL | 1 | $182.00 | $2.13 | 75 |
| 2025-07-16 11:37:29 | SELL | BAC | 2 | $46.15 | $-0.24 | 65 |
| 2025-07-16 11:37:29 | SELL | PFE | 6 | $24.61 | $-3.74 | 65 |
| 2025-07-16 11:37:29 | BUY | WFC | 1 | $78.86 | N/A | 70 |
| 2025-07-16 11:37:29 | BUY | CVX | 1 | $150.69 | N/A | 85 |
| 2025-07-16 11:25:47 | SELL | NVDA | 1 | $170.70 | $-0.85 | 70 |
| 2025-07-16 11:25:47 | SELL | INTC | 6 | $22.92 | $3.14 | 60 |
| 2025-07-16 11:25:47 | BUY | CVX | 1 | $150.69 | N/A | 85 |

<!--TRADE_LOG_END--> 
