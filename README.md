# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 19:37:06**

| Metric | Value |
|---|---|
| **Total Value** | **$100,539.52** |
| Cash | $603.23 |
| Holdings Value | $99,936.29 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.57 | $2,095.70 | 65 |
| ADBE | 6 | $375.23 | $364.67 | $2,188.00 | 65 |
| AMD | 17 | $146.29 | $154.81 | $2,631.77 | 85 |
| AMZN | 10 | $221.65 | $226.69 | $2,266.90 | 75 |
| AVGO | 8 | $275.34 | $280.88 | $2,247.04 | 65 |
| AXP | 7 | $325.34 | $311.52 | $2,180.64 | 65 |
| BA | 10 | $212.88 | $231.03 | $2,310.25 | 70 |
| BAC | 45 | $46.28 | $46.30 | $2,083.72 | 65 |
| C | 30 | $86.78 | $91.61 | $2,748.15 | 85 |
| CAT | 6 | $397.74 | $404.78 | $2,428.68 | 75 |
| COST | 2 | $979.83 | $968.78 | $1,937.56 | 65 |
| CRM | 8 | $267.44 | $258.12 | $2,064.95 | 65 |
| CSCO | 31 | $68.46 | $67.27 | $2,085.37 | 65 |
| CVX | 17 | $147.01 | $150.76 | $2,563.00 | 85 |
| DIS | 18 | $122.77 | $119.30 | $2,147.31 | 65 |
| GOOGL | 14 | $179.71 | $183.37 | $2,567.18 | 85 |
| GS | 3 | $717.52 | $703.37 | $2,110.11 | 65 |
| HD | 6 | $372.64 | $359.76 | $2,158.56 | 65 |
| INTC | 83 | $22.35 | $23.00 | $1,908.59 | 60 |
| JNJ | 13 | $155.95 | $155.25 | $2,018.32 | 65 |
| JPM | 9 | $291.63 | $286.99 | $2,582.91 | 85 |
| KO | 30 | $70.97 | $69.46 | $2,083.80 | 65 |
| LLY | 3 | $781.32 | $769.21 | $2,307.63 | 65 |
| MA | 4 | $563.08 | $552.56 | $2,210.24 | 65 |
| META | 3 | $717.12 | $714.35 | $2,143.05 | 70 |
| MRK | 26 | $82.50 | $81.64 | $2,122.56 | 65 |
| MSFT | 5 | $498.84 | $506.63 | $2,533.17 | 85 |
| NFLX | 1 | $1,279.00 | $1,261.00 | $1,261.00 | 65 |
| NKE | 30 | $72.03 | $71.93 | $2,157.90 | 70 |
| NVDA | 15 | $171.55 | $170.26 | $2,553.89 | 85 |
| ORCL | 9 | $233.15 | $234.85 | $2,113.65 | 65 |
| PEP | 15 | $136.57 | $134.28 | $2,014.20 | 65 |
| PFE | 84 | $25.28 | $24.57 | $2,063.57 | 65 |
| PG | 13 | $152.11 | $152.94 | $1,988.19 | 65 |
| PYPL | 28 | $72.12 | $73.36 | $2,054.00 | 65 |
| QCOM | 14 | $153.83 | $154.44 | $2,162.16 | 65 |
| T | 76 | $27.09 | $27.05 | $2,055.61 | 65 |
| TGT | 20 | $104.94 | $102.89 | $2,057.90 | 65 |
| TSLA | 6 | $318.51 | $310.88 | $1,865.28 | 65 |
| UNH | 7 | $298.51 | $292.09 | $2,044.63 | 65 |
| UNP | 9 | $236.66 | $231.65 | $2,084.85 | 70 |
| V | 6 | $355.85 | $347.76 | $2,086.56 | 65 |
| VZ | 50 | $43.08 | $41.31 | $2,065.71 | 65 |
| WFC | 28 | $78.89 | $78.77 | $2,205.42 | 70 |
| WMT | 21 | $97.38 | $95.52 | $2,005.92 | 65 |
| XOM | 21 | $110.02 | $112.89 | $2,370.69 | 75 |

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
| 2025-07-15 19:36:59 | SELL | INTC | 6 | $23.00 | $3.61 | 60 |
| 2025-07-15 19:36:59 | SELL | PFE | 1 | $24.57 | $-0.71 | 65 |
| 2025-07-15 19:36:59 | BUY | NKE | 1 | $71.93 | N/A | 70 |
| 2025-07-15 19:36:59 | BUY | WFC | 1 | $78.79 | N/A | 70 |
| 2025-07-15 19:36:59 | BUY | CVX | 1 | $150.78 | N/A | 85 |
| 2025-07-15 19:25:11 | SELL | BAC | 3 | $46.37 | $0.24 | 65 |
| 2025-07-15 19:25:11 | SELL | NKE | 1 | $71.90 | $-0.13 | 65 |
| 2025-07-15 19:25:11 | SELL | PFE | 3 | $24.57 | $-2.06 | 65 |
| 2025-07-15 19:25:11 | SELL | CVX | 1 | $150.88 | $3.87 | 75 |
| 2025-07-15 19:25:11 | BUY | NVDA | 2 | $170.14 | N/A | 85 |
| 2025-07-15 19:25:11 | BUY | VZ | 3 | $41.33 | N/A | 65 |
| 2025-07-15 19:08:22 | SELL | AMZN | 1 | $226.20 | $4.14 | 70 |
| 2025-07-15 19:08:22 | SELL | MRK | 1 | $81.50 | $-0.97 | 65 |
| 2025-07-15 19:08:22 | SELL | BA | 1 | $231.14 | $16.60 | 70 |
| 2025-07-15 19:08:22 | SELL | WFC | 1 | $78.33 | $-0.54 | 65 |
| 2025-07-15 19:08:22 | SELL | UNP | 1 | $231.50 | $-4.64 | 65 |
| 2025-07-15 19:08:22 | SELL | VZ | 3 | $41.31 | $-5.29 | 60 |
| 2025-07-15 19:08:22 | BUY | BAC | 3 | $46.24 | N/A | 70 |
| 2025-07-15 19:08:22 | BUY | PFE | 4 | $25.35 | N/A | 70 |
| 2025-07-15 19:08:22 | BUY | CVX | 1 | $150.71 | N/A | 85 |
| 2025-07-15 18:47:03 | SELL | BAC | 2 | $46.28 | $-0.03 | 65 |
| 2025-07-15 18:47:03 | SELL | XOM | 2 | $113.09 | $5.61 | 75 |
| 2025-07-15 18:47:03 | SELL | PFE | 3 | $24.61 | $-1.85 | 65 |
| 2025-07-15 18:47:03 | SELL | PG | 1 | $152.73 | $0.58 | 60 |
| 2025-07-15 18:47:03 | SELL | ORCL | 1 | $234.16 | $0.91 | 65 |

<!--TRADE_LOG_END--> 
