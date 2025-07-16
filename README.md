# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 13:50:16**

| Metric | Value |
|---|---|
| **Total Value** | **$100,507.84** |
| Cash | $732.06 |
| Holdings Value | $99,775.77 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.44 | $2,104.45 | 65 |
| ADBE | 6 | $375.23 | $361.55 | $2,169.27 | 65 |
| AMD | 15 | $145.04 | $154.57 | $2,318.55 | 70 |
| AMZN | 10 | $221.65 | $224.88 | $2,248.85 | 70 |
| AVGO | 8 | $275.34 | $277.86 | $2,222.84 | 70 |
| AXP | 7 | $325.34 | $310.45 | $2,173.15 | 65 |
| BA | 9 | $210.81 | $231.13 | $2,080.17 | 65 |
| BAC | 45 | $46.28 | $46.19 | $2,078.33 | 65 |
| C | 30 | $86.78 | $89.84 | $2,695.20 | 85 |
| CAT | 6 | $397.74 | $404.64 | $2,427.84 | 70 |
| COST | 2 | $979.83 | $963.56 | $1,927.12 | 65 |
| CRM | 8 | $267.44 | $257.31 | $2,058.48 | 65 |
| CSCO | 31 | $68.46 | $67.25 | $2,084.60 | 65 |
| CVX | 16 | $146.76 | $150.85 | $2,413.68 | 75 |
| DIS | 18 | $122.77 | $120.05 | $2,160.90 | 70 |
| GOOGL | 14 | $179.71 | $182.91 | $2,560.67 | 75 |
| GS | 3 | $717.52 | $695.10 | $2,085.30 | 85 |
| HD | 6 | $372.64 | $358.16 | $2,148.96 | 65 |
| INTC | 91 | $22.38 | $22.61 | $2,057.05 | 65 |
| JNJ | 13 | $155.43 | $161.99 | $2,105.87 | 65 |
| JPM | 9 | $291.63 | $287.32 | $2,585.88 | 80 |
| KO | 30 | $70.97 | $69.40 | $2,082.00 | 65 |
| LLY | 3 | $781.32 | $780.80 | $2,342.40 | 65 |
| MA | 4 | $563.08 | $551.90 | $2,207.60 | 65 |
| META | 3 | $717.12 | $707.40 | $2,122.20 | 75 |
| MRK | 29 | $82.47 | $82.21 | $2,384.09 | 75 |
| MSFT | 5 | $498.84 | $503.68 | $2,518.40 | 85 |
| NFLX | 1 | $1,279.00 | $1,255.56 | $1,255.56 | 65 |
| NKE | 29 | $72.03 | $72.31 | $2,096.85 | 65 |
| NVDA | 14 | $171.61 | $170.77 | $2,390.78 | 70 |
| ORCL | 9 | $233.15 | $233.72 | $2,103.43 | 70 |
| PEP | 15 | $136.57 | $134.50 | $2,017.50 | 65 |
| PFE | 84 | $25.28 | $24.93 | $2,093.70 | 65 |
| PG | 14 | $152.15 | $153.41 | $2,147.81 | 65 |
| PYPL | 29 | $72.15 | $72.58 | $2,104.68 | 65 |
| QCOM | 14 | $153.83 | $153.43 | $2,148.06 | 65 |
| T | 77 | $27.09 | $26.99 | $2,077.87 | 65 |
| TGT | 20 | $104.94 | $102.17 | $2,043.40 | 65 |
| TSLA | 6 | $318.51 | $317.05 | $1,902.30 | 60 |
| UNH | 7 | $298.51 | $295.18 | $2,066.28 | 70 |
| UNP | 10 | $236.15 | $231.23 | $2,312.30 | 75 |
| V | 6 | $355.85 | $347.22 | $2,083.32 | 65 |
| VZ | 50 | $43.08 | $41.38 | $2,069.25 | 65 |
| WFC | 27 | $78.83 | $79.47 | $2,145.82 | 65 |
| WMT | 22 | $97.29 | $95.31 | $2,096.82 | 65 |
| XOM | 20 | $109.88 | $112.81 | $2,256.20 | 70 |

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
| 2025-07-16 13:50:09 | SELL | NVDA | 1 | $170.74 | $-0.81 | 70 |
| 2025-07-16 13:50:09 | SELL | JNJ | 1 | $161.91 | $6.02 | 65 |
| 2025-07-16 13:50:09 | SELL | XOM | 1 | $112.87 | $2.85 | 70 |
| 2025-07-16 13:50:09 | SELL | PFE | 1 | $24.92 | $-0.36 | 65 |
| 2025-07-16 13:50:09 | SELL | BA | 1 | $230.91 | $18.09 | 65 |
| 2025-07-16 13:50:09 | SELL | WFC | 3 | $79.46 | $1.71 | 65 |
| 2025-07-16 13:50:09 | SELL | CVX | 1 | $150.89 | $3.88 | 75 |
| 2025-07-16 13:50:09 | BUY | INTC | 7 | $22.65 | N/A | 65 |
| 2025-07-16 13:50:09 | BUY | MRK | 3 | $82.21 | N/A | 75 |
| 2025-07-16 13:50:09 | BUY | UNP | 1 | $231.38 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
