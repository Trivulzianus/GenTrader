# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 04:29:29**

| Metric | Value |
|---|---|
| **Total Value** | **$100,865.53** |
| Cash | $1,233.59 |
| Holdings Value | $99,631.94 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.62 | $2,086.20 | 65 |
| ADBE | 6 | $375.23 | $366.99 | $2,201.94 | 65 |
| AMD | 15 | $134.71 | $146.24 | $2,193.60 | 70 |
| AMZN | 11 | $221.97 | $225.69 | $2,482.59 | 85 |
| AVGO | 8 | $275.34 | $275.60 | $2,204.80 | 65 |
| AXP | 7 | $325.34 | $320.92 | $2,246.44 | 75 |
| BA | 9 | $210.69 | $230.51 | $2,074.59 | 70 |
| BAC | 47 | $48.70 | $47.07 | $2,212.29 | 70 |
| C | 28 | $86.54 | $87.50 | $2,450.00 | 75 |
| CAT | 6 | $397.74 | $405.77 | $2,434.62 | 70 |
| COST | 2 | $979.83 | $980.91 | $1,961.82 | 65 |
| CRM | 7 | $268.68 | $259.68 | $1,817.76 | 65 |
| CSCO | 30 | $68.49 | $67.82 | $2,034.60 | 65 |
| CVX | 17 | $147.08 | $151.65 | $2,578.05 | 85 |
| DIS | 18 | $122.79 | $119.97 | $2,159.46 | 70 |
| GOOGL | 14 | $179.74 | $181.56 | $2,541.84 | 85 |
| GS | 3 | $717.52 | $713.30 | $2,139.90 | 70 |
| HD | 6 | $372.64 | $370.11 | $2,220.66 | 65 |
| INTC | 88 | $22.39 | $23.30 | $2,050.40 | 65 |
| JNJ | 13 | $155.95 | $156.82 | $2,038.66 | 65 |
| JPM | 8 | $292.00 | $288.70 | $2,309.60 | 70 |
| KO | 28 | $71.08 | $69.47 | $1,945.16 | 60 |
| LLY | 3 | $781.32 | $799.34 | $2,398.02 | 70 |
| MA | 4 | $563.08 | $553.02 | $2,212.08 | 65 |
| META | 3 | $717.12 | $720.92 | $2,162.76 | 75 |
| MRK | 28 | $82.50 | $83.67 | $2,342.76 | 75 |
| MSFT | 5 | $498.84 | $503.02 | $2,515.10 | 70 |
| NFLX | 1 | $1,279.00 | $1,261.95 | $1,261.95 | 65 |
| NKE | 28 | $72.03 | $72.25 | $2,023.00 | 65 |
| NVDA | 14 | $156.74 | $164.07 | $2,296.98 | 75 |
| ORCL | 9 | $233.27 | $229.28 | $2,063.52 | 70 |
| PEP | 15 | $136.57 | $135.57 | $2,033.55 | 65 |
| PFE | 87 | $25.21 | $25.35 | $2,205.45 | 70 |
| PG | 13 | $160.81 | $153.76 | $1,998.88 | 65 |
| PYPL | 31 | $72.25 | $73.89 | $2,290.59 | 70 |
| QCOM | 13 | $153.79 | $154.29 | $2,005.77 | 65 |
| T | 75 | $27.10 | $27.16 | $2,037.00 | 65 |
| TGT | 20 | $104.94 | $104.87 | $2,097.40 | 65 |
| TSLA | 6 | $288.62 | $316.90 | $1,901.40 | 65 |
| UNH | 7 | $298.51 | $300.58 | $2,104.06 | 65 |
| UNP | 10 | $236.23 | $233.31 | $2,333.10 | 75 |
| V | 6 | $355.85 | $350.50 | $2,103.00 | 65 |
| VZ | 49 | $43.12 | $41.58 | $2,037.42 | 65 |
| WFC | 29 | $82.29 | $83.43 | $2,419.47 | 75 |
| WMT | 21 | $97.38 | $95.78 | $2,011.38 | 65 |
| XOM | 21 | $110.01 | $113.92 | $2,392.32 | 75 |

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
| 2025-07-15 04:29:24 | SELL | KO | 1 | $69.47 | $-1.56 | 60 |
| 2025-07-15 04:29:24 | SELL | C | 2 | $87.50 | $1.80 | 75 |
| 2025-07-15 04:29:24 | SELL | TGT | 1 | $104.87 | $-0.06 | 65 |
| 2025-07-15 04:29:24 | BUY | INTC | 1 | $23.30 | N/A | 65 |
| 2025-07-15 04:29:24 | BUY | PFE | 1 | $25.35 | N/A | 70 |
| 2025-07-15 04:29:24 | BUY | UNP | 1 | $233.31 | N/A | 75 |
| 2025-07-15 04:06:28 | SELL | BAC | 2 | $47.07 | $-3.13 | 70 |
| 2025-07-15 04:06:28 | SELL | WFC | 2 | $83.43 | $2.13 | 75 |
| 2025-07-15 04:06:28 | BUY | DIS | 1 | $119.97 | N/A | 70 |
| 2025-07-15 04:06:28 | BUY | PFE | 5 | $25.35 | N/A | 70 |
| 2025-07-15 04:06:28 | BUY | VZ | 1 | $41.58 | N/A | 65 |
| 2025-07-15 04:06:28 | BUY | T | 1 | $27.16 | N/A | 65 |
| 2025-07-15 04:06:28 | BUY | TGT | 2 | $104.87 | N/A | 70 |
| 2025-07-15 03:36:32 | SELL | PFE | 5 | $25.35 | $0.70 | 65 |
| 2025-07-15 03:36:32 | SELL | UNP | 1 | $233.31 | $-2.92 | 65 |
| 2025-07-15 03:36:32 | BUY | BAC | 2 | $47.07 | N/A | 75 |
| 2025-07-15 03:36:32 | BUY | WFC | 3 | $83.43 | N/A | 85 |
| 2025-07-15 02:49:04 | BUY | PYPL | 3 | $73.89 | N/A | 75 |
| 2025-07-15 02:49:04 | BUY | CVX | 1 | $151.65 | N/A | 85 |
| 2025-07-15 01:59:33 | SELL | BAC | 2 | $47.07 | $-3.13 | 70 |
| 2025-07-15 01:59:33 | SELL | PYPL | 1 | $73.89 | $1.75 | 65 |
| 2025-07-15 01:59:33 | SELL | CVX | 1 | $151.65 | $4.57 | 75 |
| 2025-07-15 01:59:33 | BUY | INTC | 1 | $23.30 | N/A | 65 |
| 2025-07-15 01:59:33 | BUY | PFE | 1 | $25.35 | N/A | 70 |
| 2025-07-15 01:13:07 | SELL | WFC | 3 | $83.43 | $3.19 | 75 |

<!--TRADE_LOG_END--> 
