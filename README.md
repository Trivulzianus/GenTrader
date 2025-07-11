# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 14:52:09**

| Metric | Value |
|---|---|
| **Total Value** | **$100,724.75** |
| Cash | $1,169.38 |
| Holdings Value | $99,555.37 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.16 | $2,111.65 | 65 |
| ADBE | 5 | $377.60 | $368.51 | $1,842.55 | 65 |
| AMD | 16 | $135.79 | $144.71 | $2,315.34 | 70 |
| AMZN | 11 | $221.97 | $224.14 | $2,465.54 | 75 |
| AVGO | 8 | $275.34 | $273.36 | $2,186.88 | 70 |
| AXP | 7 | $325.34 | $323.37 | $2,263.59 | 75 |
| BA | 9 | $210.85 | $228.01 | $2,052.09 | 65 |
| BAC | 47 | $48.70 | $46.44 | $2,182.45 | 70 |
| C | 25 | $86.68 | $86.22 | $2,155.50 | 70 |
| CAT | 6 | $397.86 | $404.30 | $2,425.77 | 70 |
| COST | 2 | $979.83 | $971.08 | $1,942.16 | 65 |
| CRM | 7 | $268.68 | $260.07 | $1,820.52 | 65 |
| CSCO | 31 | $68.38 | $68.10 | $2,111.10 | 65 |
| CVX | 17 | $147.16 | $154.62 | $2,628.54 | 85 |
| DIS | 18 | $122.81 | $120.41 | $2,167.38 | 65 |
| GOOGL | 13 | $179.61 | $178.23 | $2,316.99 | 70 |
| GS | 3 | $717.52 | $705.04 | $2,115.13 | 75 |
| HD | 6 | $372.64 | $367.73 | $2,206.38 | 70 |
| INTC | 82 | $22.29 | $23.36 | $1,915.11 | 60 |
| JNJ | 13 | $155.89 | $155.49 | $2,021.36 | 65 |
| JPM | 9 | $291.61 | $286.13 | $2,575.17 | 75 |
| KO | 29 | $71.03 | $69.97 | $2,028.99 | 65 |
| LLY | 3 | $781.32 | $780.85 | $2,342.55 | 70 |
| MA | 4 | $563.08 | $555.50 | $2,221.98 | 65 |
| META | 3 | $717.12 | $714.46 | $2,143.38 | 75 |
| MRK | 25 | $82.30 | $82.48 | $2,062.12 | 65 |
| MSFT | 5 | $498.84 | $501.85 | $2,509.25 | 85 |
| NFLX | 1 | $1,279.00 | $1,248.74 | $1,248.74 | 65 |
| NKE | 31 | $75.76 | $72.78 | $2,256.34 | 70 |
| NVDA | 16 | $157.38 | $167.49 | $2,679.76 | 85 |
| ORCL | 9 | $233.26 | $233.86 | $2,104.74 | 70 |
| PEP | 15 | $136.57 | $134.71 | $2,020.58 | 65 |
| PFE | 87 | $25.20 | $25.45 | $2,214.59 | 70 |
| PG | 14 | $160.52 | $157.09 | $2,199.26 | 65 |
| PYPL | 31 | $76.61 | $74.67 | $2,314.77 | 75 |
| QCOM | 13 | $162.18 | $157.64 | $2,049.32 | 65 |
| T | 76 | $27.10 | $26.90 | $2,044.40 | 65 |
| TGT | 20 | $104.92 | $103.98 | $2,079.60 | 65 |
| TSLA | 6 | $288.62 | $308.89 | $1,853.36 | 65 |
| UNH | 7 | $298.51 | $299.64 | $2,097.51 | 65 |
| UNP | 10 | $236.18 | $235.27 | $2,352.70 | 75 |
| V | 6 | $355.85 | $350.58 | $2,103.48 | 65 |
| VZ | 46 | $43.21 | $41.62 | $1,914.52 | 60 |
| WFC | 29 | $82.28 | $82.16 | $2,382.49 | 75 |
| WMT | 22 | $97.25 | $95.12 | $2,092.64 | 65 |
| XOM | 21 | $109.91 | $115.10 | $2,417.10 | 75 |

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
| 2025-07-11 14:52:03 | SELL | INTC | 6 | $23.35 | $5.94 | 60 |
| 2025-07-11 14:52:03 | SELL | XOM | 2 | $115.08 | $9.45 | 75 |
| 2025-07-11 14:52:03 | SELL | NKE | 1 | $72.81 | $-2.86 | 70 |
| 2025-07-11 14:52:03 | SELL | CSCO | 3 | $68.11 | $-0.75 | 65 |
| 2025-07-11 14:52:03 | SELL | VZ | 3 | $41.62 | $-4.48 | 60 |
| 2025-07-11 14:52:03 | BUY | BAC | 2 | $46.43 | N/A | 70 |
| 2025-07-11 14:52:03 | BUY | PYPL | 2 | $74.69 | N/A | 75 |
| 2025-07-11 14:52:03 | BUY | C | 2 | $86.21 | N/A | 70 |
| 2025-07-11 14:52:03 | BUY | CVX | 1 | $154.60 | N/A | 85 |
| 2025-07-11 14:40:54 | SELL | C | 2 | $86.14 | $-1.05 | 60 |
| 2025-07-11 14:40:54 | SELL | ORCL | 1 | $232.82 | $-0.39 | 65 |
| 2025-07-11 14:40:54 | SELL | CVX | 1 | $154.49 | $7.34 | 75 |
| 2025-07-11 14:40:54 | BUY | INTC | 6 | $23.38 | N/A | 65 |
| 2025-07-11 14:40:54 | BUY | XOM | 2 | $115.05 | N/A | 85 |
| 2025-07-11 14:40:54 | BUY | PFE | 1 | $25.48 | N/A | 70 |
| 2025-07-11 14:40:54 | BUY | CSCO | 2 | $68.32 | N/A | 75 |
| 2025-07-11 14:40:54 | BUY | VZ | 3 | $41.60 | N/A | 65 |
| 2025-07-11 14:25:53 | SELL | BAC | 2 | $46.44 | $-4.51 | 65 |
| 2025-07-11 14:25:53 | SELL | VZ | 3 | $41.69 | $-4.28 | 60 |
| 2025-07-11 14:25:53 | BUY | C | 2 | $86.00 | N/A | 70 |
| 2025-07-11 14:25:53 | BUY | WFC | 1 | $81.96 | N/A | 75 |
| 2025-07-11 14:25:53 | BUY | CSCO | 1 | $68.38 | N/A | 70 |
| 2025-07-11 14:25:53 | BUY | T | 6 | $26.95 | N/A | 65 |
| 2025-07-11 14:09:16 | SELL | INTC | 6 | $23.27 | $5.47 | 60 |
| 2025-07-11 14:09:16 | SELL | XOM | 1 | $114.67 | $4.54 | 75 |

<!--TRADE_LOG_END--> 
