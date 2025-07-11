# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 14:09:26**

| Metric | Value |
|---|---|
| **Total Value** | **$100,685.20** |
| Cash | $1,330.09 |
| Holdings Value | $99,355.10 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.35 | $2,113.50 | 70 |
| ADBE | 5 | $377.60 | $368.00 | $1,840.00 | 65 |
| AMD | 16 | $135.79 | $143.15 | $2,290.40 | 70 |
| AMZN | 11 | $221.97 | $224.13 | $2,465.43 | 75 |
| AVGO | 8 | $275.34 | $273.65 | $2,189.20 | 65 |
| AXP | 7 | $325.34 | $323.32 | $2,263.28 | 75 |
| BA | 9 | $210.85 | $228.00 | $2,052.05 | 65 |
| BAC | 47 | $48.70 | $46.42 | $2,181.97 | 70 |
| C | 23 | $86.73 | $85.87 | $1,975.01 | 65 |
| CAT | 6 | $397.86 | $402.38 | $2,414.31 | 70 |
| COST | 2 | $979.83 | $970.50 | $1,941.00 | 65 |
| CRM | 7 | $268.68 | $261.37 | $1,829.57 | 65 |
| CSCO | 31 | $68.36 | $68.22 | $2,114.97 | 65 |
| CVX | 17 | $147.15 | $154.05 | $2,618.85 | 85 |
| DIS | 18 | $122.81 | $120.30 | $2,165.40 | 65 |
| GOOGL | 13 | $179.61 | $176.91 | $2,299.83 | 75 |
| GS | 3 | $717.52 | $702.96 | $2,108.88 | 70 |
| HD | 6 | $372.64 | $368.04 | $2,208.24 | 70 |
| INTC | 82 | $22.29 | $23.26 | $1,907.32 | 60 |
| JNJ | 13 | $155.89 | $156.47 | $2,034.11 | 65 |
| JPM | 9 | $291.61 | $285.11 | $2,565.95 | 75 |
| KO | 29 | $71.03 | $69.72 | $2,022.02 | 65 |
| LLY | 3 | $781.32 | $786.89 | $2,360.66 | 70 |
| MA | 4 | $563.08 | $556.65 | $2,226.60 | 65 |
| META | 3 | $717.12 | $714.82 | $2,144.46 | 75 |
| MRK | 25 | $82.30 | $83.25 | $2,081.12 | 65 |
| MSFT | 5 | $498.84 | $501.05 | $2,505.25 | 75 |
| NFLX | 1 | $1,279.00 | $1,250.13 | $1,250.13 | 65 |
| NKE | 32 | $75.67 | $73.15 | $2,340.84 | 75 |
| NVDA | 16 | $157.38 | $166.00 | $2,656.08 | 85 |
| ORCL | 10 | $233.21 | $232.36 | $2,323.60 | 75 |
| PEP | 15 | $136.57 | $134.35 | $2,015.21 | 65 |
| PFE | 86 | $25.20 | $25.59 | $2,200.31 | 70 |
| PG | 14 | $160.52 | $157.07 | $2,198.98 | 70 |
| PYPL | 29 | $76.75 | $74.72 | $2,166.88 | 70 |
| QCOM | 13 | $162.18 | $157.61 | $2,048.93 | 65 |
| T | 70 | $27.11 | $27.16 | $1,901.20 | 60 |
| TGT | 20 | $104.92 | $103.79 | $2,075.80 | 65 |
| TSLA | 6 | $288.62 | $309.15 | $1,854.93 | 65 |
| UNH | 7 | $298.51 | $299.75 | $2,098.25 | 65 |
| UNP | 10 | $236.18 | $235.38 | $2,353.75 | 75 |
| V | 6 | $355.85 | $350.90 | $2,105.43 | 70 |
| VZ | 49 | $43.12 | $41.77 | $2,046.49 | 65 |
| WFC | 28 | $82.29 | $81.79 | $2,290.12 | 70 |
| WMT | 22 | $97.25 | $95.43 | $2,099.46 | 65 |
| XOM | 21 | $109.91 | $114.73 | $2,409.33 | 75 |

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
| 2025-07-11 14:09:16 | SELL | INTC | 6 | $23.27 | $5.47 | 60 |
| 2025-07-11 14:09:16 | SELL | XOM | 1 | $114.67 | $4.54 | 75 |
| 2025-07-11 14:09:16 | SELL | WFC | 1 | $81.79 | $-0.49 | 70 |
| 2025-07-11 14:09:16 | SELL | T | 5 | $27.16 | $0.20 | 60 |
| 2025-07-11 14:09:16 | BUY | NKE | 1 | $73.15 | N/A | 75 |
| 2025-07-11 14:09:16 | BUY | PYPL | 1 | $74.76 | N/A | 70 |
| 2025-07-11 14:09:16 | BUY | ORCL | 1 | $232.34 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
