# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 16:43:22**

| Metric | Value |
|---|---|
| **Total Value** | **$100,681.34** |
| Cash | $762.66 |
| Holdings Value | $99,918.68 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.57 | $2,105.70 | 65 |
| ADBE | 5 | $377.60 | $365.41 | $1,827.05 | 65 |
| AMD | 18 | $136.77 | $145.72 | $2,622.96 | 85 |
| AMZN | 11 | $221.97 | $225.15 | $2,476.62 | 80 |
| AVGO | 8 | $275.34 | $275.29 | $2,202.32 | 70 |
| AXP | 7 | $325.34 | $320.73 | $2,245.12 | 75 |
| BA | 10 | $212.47 | $226.50 | $2,265.00 | 75 |
| BAC | 47 | $48.70 | $46.48 | $2,184.80 | 70 |
| C | 24 | $86.68 | $86.38 | $2,073.12 | 65 |
| CAT | 6 | $397.86 | $404.98 | $2,429.88 | 70 |
| COST | 2 | $979.83 | $967.53 | $1,935.07 | 65 |
| CRM | 7 | $268.68 | $258.90 | $1,812.30 | 65 |
| CSCO | 34 | $68.35 | $67.78 | $2,304.52 | 75 |
| CVX | 17 | $147.16 | $155.05 | $2,635.79 | 80 |
| DIS | 17 | $122.97 | $119.90 | $2,038.30 | 65 |
| GOOGL | 13 | $179.61 | $180.14 | $2,341.82 | 70 |
| GS | 3 | $717.52 | $702.20 | $2,106.60 | 65 |
| HD | 6 | $372.64 | $368.39 | $2,210.34 | 65 |
| INTC | 86 | $22.35 | $23.37 | $2,009.99 | 65 |
| JNJ | 13 | $155.89 | $156.60 | $2,035.86 | 65 |
| JPM | 9 | $291.61 | $286.13 | $2,575.22 | 85 |
| KO | 29 | $71.03 | $69.97 | $2,029.13 | 65 |
| LLY | 3 | $781.32 | $782.09 | $2,346.26 | 75 |
| MA | 4 | $563.08 | $548.94 | $2,195.76 | 65 |
| META | 3 | $717.12 | $719.93 | $2,159.79 | 75 |
| MRK | 26 | $82.32 | $82.99 | $2,157.74 | 70 |
| MSFT | 5 | $498.84 | $504.33 | $2,521.67 | 85 |
| NFLX | 1 | $1,279.00 | $1,236.80 | $1,236.80 | 65 |
| NKE | 32 | $75.67 | $72.58 | $2,322.56 | 75 |
| NVDA | 16 | $157.38 | $166.28 | $2,660.48 | 85 |
| ORCL | 9 | $233.26 | $232.52 | $2,092.68 | 65 |
| PEP | 15 | $136.57 | $134.15 | $2,012.18 | 65 |
| PFE | 85 | $25.20 | $25.62 | $2,177.71 | 70 |
| PG | 13 | $160.80 | $156.67 | $2,036.71 | 65 |
| PYPL | 28 | $76.82 | $74.31 | $2,080.55 | 65 |
| QCOM | 13 | $162.18 | $157.83 | $2,051.79 | 65 |
| T | 71 | $27.12 | $26.77 | $1,901.02 | 60 |
| TGT | 20 | $104.91 | $104.51 | $2,090.20 | 65 |
| TSLA | 6 | $288.62 | $310.10 | $1,860.61 | 65 |
| UNH | 7 | $298.51 | $300.57 | $2,103.99 | 65 |
| UNP | 10 | $236.18 | $234.57 | $2,345.70 | 75 |
| V | 6 | $355.85 | $347.20 | $2,083.20 | 65 |
| VZ | 49 | $43.12 | $41.63 | $2,039.87 | 65 |
| WFC | 30 | $82.28 | $82.21 | $2,466.30 | 80 |
| WMT | 22 | $97.25 | $94.76 | $2,084.72 | 65 |
| XOM | 21 | $109.97 | $115.38 | $2,422.88 | 75 |

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
| 2025-07-11 16:43:13 | SELL | XOM | 2 | $114.93 | $9.06 | 75 |
| 2025-07-11 16:43:13 | SELL | DIS | 1 | $119.90 | $-2.89 | 65 |
| 2025-07-11 16:43:13 | SELL | T | 5 | $26.77 | $-1.62 | 60 |
| 2025-07-11 16:43:13 | BUY | BAC | 3 | $46.49 | N/A | 70 |
| 2025-07-11 16:43:13 | BUY | INTC | 5 | $23.38 | N/A | 65 |
| 2025-07-11 16:43:13 | BUY | MRK | 1 | $82.97 | N/A | 70 |
| 2025-07-11 16:43:13 | BUY | WFC | 1 | $82.21 | N/A | 80 |
| 2025-07-11 16:26:51 | SELL | INTC | 6 | $23.36 | $6.00 | 60 |
| 2025-07-11 16:26:51 | SELL | PYPL | 3 | $74.40 | $-6.56 | 65 |
| 2025-07-11 16:26:51 | SELL | C | 2 | $86.38 | $-0.56 | 65 |
| 2025-07-11 16:26:51 | BUY | XOM | 2 | $115.34 | N/A | 85 |
| 2025-07-11 16:26:51 | BUY | BA | 1 | $227.06 | N/A | 75 |
| 2025-07-11 16:09:13 | SELL | XOM | 1 | $115.30 | $5.13 | 75 |
| 2025-07-11 16:09:13 | SELL | MRK | 1 | $82.85 | $0.53 | 65 |
| 2025-07-11 16:09:13 | BUY | INTC | 1 | $23.44 | N/A | 65 |
| 2025-07-11 16:09:13 | BUY | PYPL | 4 | $74.32 | N/A | 75 |
| 2025-07-11 16:09:13 | BUY | NKE | 1 | $72.62 | N/A | 75 |
| 2025-07-11 15:51:23 | SELL | BAC | 3 | $46.45 | $-6.75 | 65 |
| 2025-07-11 15:51:23 | SELL | INTC | 1 | $23.42 | $1.06 | 65 |
| 2025-07-11 15:51:23 | SELL | PYPL | 1 | $74.56 | $-2.28 | 65 |
| 2025-07-11 15:51:23 | SELL | PFE | 1 | $25.59 | $0.39 | 70 |
| 2025-07-11 15:51:23 | SELL | PG | 1 | $156.91 | $-3.60 | 65 |
| 2025-07-11 15:51:23 | SELL | TGT | 1 | $104.49 | $-0.40 | 65 |
| 2025-07-11 15:51:23 | BUY | DIS | 1 | $120.05 | N/A | 70 |
| 2025-07-11 15:51:23 | BUY | XOM | 1 | $115.55 | N/A | 85 |

<!--TRADE_LOG_END--> 
