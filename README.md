# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 13:56:07**

| Metric | Value |
|---|---|
| **Total Value** | **$100,693.12** |
| Cash | $1,238.50 |
| Holdings Value | $99,454.62 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.69 | $2,106.95 | 65 |
| ADBE | 5 | $377.60 | $368.59 | $1,842.95 | 65 |
| AMD | 16 | $135.79 | $143.27 | $2,292.32 | 75 |
| AMZN | 11 | $221.97 | $224.13 | $2,465.48 | 75 |
| AVGO | 8 | $275.34 | $273.22 | $2,185.76 | 65 |
| AXP | 7 | $325.34 | $323.16 | $2,262.12 | 65 |
| BA | 9 | $210.85 | $228.19 | $2,053.71 | 65 |
| BAC | 47 | $48.70 | $46.40 | $2,180.58 | 70 |
| C | 23 | $86.73 | $85.89 | $1,975.47 | 65 |
| CAT | 6 | $397.86 | $402.91 | $2,417.46 | 70 |
| COST | 2 | $979.83 | $972.90 | $1,945.80 | 65 |
| CRM | 7 | $268.68 | $261.60 | $1,831.18 | 65 |
| CSCO | 31 | $68.36 | $68.20 | $2,114.20 | 65 |
| CVX | 17 | $147.15 | $153.66 | $2,612.30 | 85 |
| DIS | 18 | $122.81 | $120.38 | $2,166.84 | 65 |
| GOOGL | 13 | $179.61 | $177.48 | $2,307.23 | 75 |
| GS | 3 | $717.52 | $702.00 | $2,106.01 | 70 |
| HD | 6 | $372.64 | $368.79 | $2,212.74 | 70 |
| INTC | 88 | $22.36 | $23.30 | $2,049.96 | 65 |
| JNJ | 13 | $155.89 | $156.28 | $2,031.70 | 65 |
| JPM | 9 | $291.61 | $284.86 | $2,563.74 | 75 |
| KO | 29 | $71.03 | $69.48 | $2,015.07 | 65 |
| LLY | 3 | $781.32 | $785.38 | $2,356.14 | 70 |
| MA | 4 | $563.08 | $558.16 | $2,232.64 | 65 |
| META | 3 | $717.12 | $711.99 | $2,135.97 | 75 |
| MRK | 25 | $82.30 | $83.15 | $2,078.75 | 65 |
| MSFT | 5 | $498.84 | $500.70 | $2,503.50 | 85 |
| NFLX | 1 | $1,279.00 | $1,245.00 | $1,245.00 | 65 |
| NKE | 31 | $75.75 | $73.29 | $2,271.99 | 70 |
| NVDA | 16 | $157.38 | $166.09 | $2,657.36 | 85 |
| ORCL | 9 | $233.31 | $232.06 | $2,088.54 | 70 |
| PEP | 15 | $136.57 | $134.64 | $2,019.60 | 65 |
| PFE | 86 | $25.20 | $25.58 | $2,199.88 | 70 |
| PG | 14 | $160.52 | $157.17 | $2,200.41 | 70 |
| PYPL | 28 | $76.82 | $74.62 | $2,089.36 | 65 |
| QCOM | 13 | $162.18 | $158.36 | $2,058.68 | 65 |
| T | 75 | $27.11 | $27.11 | $2,033.62 | 65 |
| TGT | 20 | $104.92 | $104.05 | $2,081.00 | 65 |
| TSLA | 6 | $288.62 | $310.05 | $1,860.30 | 65 |
| UNH | 7 | $298.51 | $299.33 | $2,095.31 | 65 |
| UNP | 10 | $236.18 | $235.91 | $2,359.15 | 75 |
| V | 6 | $355.85 | $352.06 | $2,112.33 | 65 |
| VZ | 49 | $43.12 | $41.74 | $2,045.26 | 65 |
| WFC | 29 | $82.28 | $81.77 | $2,371.33 | 75 |
| WMT | 22 | $97.25 | $95.25 | $2,095.50 | 65 |
| XOM | 22 | $110.13 | $114.70 | $2,523.40 | 80 |

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
| 2025-07-11 13:55:56 | SELL | PYPL | 2 | $74.62 | $-4.10 | 65 |
| 2025-07-11 13:55:56 | SELL | QCOM | 1 | $158.34 | $-3.56 | 65 |
| 2025-07-11 13:55:56 | SELL | CSCO | 1 | $68.18 | $-0.17 | 65 |
| 2025-07-11 13:55:56 | BUY | BAC | 2 | $46.38 | N/A | 70 |
| 2025-07-11 13:55:56 | BUY | XOM | 1 | $114.69 | N/A | 80 |
| 2025-07-11 13:55:56 | BUY | PFE | 5 | $25.57 | N/A | 70 |
| 2025-07-11 13:55:56 | BUY | PG | 1 | $157.15 | N/A | 70 |
| 2025-07-11 13:55:56 | BUY | T | 75 | $27.11 | N/A | 65 |
| 2025-07-11 13:55:42 | SELL | T | 70 | $27.11 | $-104.64 | 60 |
| 2025-07-11 13:45:51 | SELL | AAPL | 1 | $209.92 | $-1.24 | 65 |
| 2025-07-11 13:45:51 | SELL | BAC | 4 | $46.38 | $-8.89 | 65 |
| 2025-07-11 13:45:51 | SELL | AMD | 2 | $142.25 | $11.49 | 70 |
| 2025-07-11 13:45:51 | SELL | PFE | 9 | $25.62 | $3.67 | 65 |
| 2025-07-11 13:45:51 | SELL | MRK | 3 | $83.43 | $3.01 | 65 |
| 2025-07-11 13:45:51 | SELL | T | 3 | $27.14 | $-4.20 | 60 |
| 2025-07-11 13:45:51 | BUY | INTC | 4 | $23.20 | N/A | 65 |
| 2025-07-11 13:45:51 | BUY | DIS | 1 | $121.56 | N/A | 70 |
| 2025-07-11 13:45:51 | BUY | WFC | 1 | $81.62 | N/A | 75 |
| 2025-07-11 13:45:51 | BUY | UNP | 1 | $236.01 | N/A | 75 |
| 2025-07-11 13:45:51 | BUY | VZ | 1 | $41.83 | N/A | 65 |
| 2025-07-11 13:28:35 | SELL | CSCO | 1 | $68.76 | $0.40 | 70 |
| 2025-07-11 13:28:35 | BUY | BAC | 2 | $46.97 | N/A | 75 |
| 2025-07-11 13:03:05 | SELL | BAC | 2 | $46.97 | $-3.27 | 70 |
| 2025-07-11 12:31:16 | SELL | WFC | 1 | $82.36 | $0.06 | 75 |
| 2025-07-11 12:31:16 | SELL | C | 1 | $87.08 | $0.34 | 65 |

<!--TRADE_LOG_END--> 
