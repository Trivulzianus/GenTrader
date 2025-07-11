# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 15:51:29**

| Metric | Value |
|---|---|
| **Total Value** | **$100,730.13** |
| Cash | $817.36 |
| Holdings Value | $99,912.77 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.46 | $2,104.60 | 70 |
| ADBE | 5 | $377.60 | $366.70 | $1,833.52 | 70 |
| AMD | 18 | $136.77 | $145.42 | $2,617.56 | 85 |
| AMZN | 11 | $221.97 | $225.50 | $2,480.50 | 85 |
| AVGO | 8 | $275.34 | $275.14 | $2,201.16 | 70 |
| AXP | 7 | $325.34 | $321.74 | $2,252.18 | 75 |
| BA | 9 | $210.85 | $227.28 | $2,045.52 | 65 |
| BAC | 44 | $48.85 | $46.45 | $2,043.58 | 65 |
| C | 26 | $86.66 | $86.33 | $2,244.45 | 75 |
| CAT | 6 | $397.86 | $404.77 | $2,428.62 | 75 |
| COST | 2 | $979.83 | $968.72 | $1,937.44 | 65 |
| CRM | 7 | $268.68 | $259.53 | $1,816.72 | 65 |
| CSCO | 34 | $68.35 | $68.03 | $2,313.19 | 75 |
| CVX | 17 | $147.16 | $155.36 | $2,641.12 | 85 |
| DIS | 18 | $122.80 | $120.02 | $2,160.36 | 70 |
| GOOGL | 13 | $179.61 | $180.02 | $2,340.24 | 75 |
| GS | 3 | $717.52 | $703.00 | $2,109.00 | 65 |
| HD | 6 | $372.64 | $368.95 | $2,213.70 | 65 |
| INTC | 86 | $22.35 | $23.41 | $2,013.69 | 65 |
| JNJ | 13 | $155.89 | $156.15 | $2,029.95 | 65 |
| JPM | 9 | $291.61 | $286.06 | $2,574.49 | 75 |
| KO | 29 | $71.03 | $69.94 | $2,028.26 | 65 |
| LLY | 3 | $781.32 | $782.00 | $2,346.00 | 70 |
| MA | 4 | $563.08 | $550.78 | $2,203.12 | 65 |
| META | 3 | $717.12 | $717.82 | $2,153.46 | 75 |
| MRK | 26 | $82.31 | $82.72 | $2,150.59 | 70 |
| MSFT | 5 | $498.84 | $503.78 | $2,518.90 | 85 |
| NFLX | 1 | $1,279.00 | $1,239.93 | $1,239.93 | 65 |
| NKE | 31 | $75.77 | $72.59 | $2,250.29 | 75 |
| NVDA | 16 | $157.38 | $166.63 | $2,666.09 | 85 |
| ORCL | 9 | $233.26 | $232.25 | $2,090.30 | 65 |
| PEP | 15 | $136.57 | $134.14 | $2,012.10 | 65 |
| PFE | 85 | $25.20 | $25.60 | $2,176.00 | 70 |
| PG | 13 | $160.80 | $156.94 | $2,040.22 | 65 |
| PYPL | 27 | $76.92 | $74.56 | $2,012.99 | 65 |
| QCOM | 13 | $162.18 | $158.03 | $2,054.39 | 70 |
| T | 76 | $27.10 | $26.73 | $2,031.86 | 65 |
| TGT | 20 | $104.91 | $104.49 | $2,089.80 | 65 |
| TSLA | 6 | $288.62 | $308.56 | $1,851.36 | 65 |
| UNH | 7 | $298.51 | $301.20 | $2,108.40 | 65 |
| UNP | 10 | $236.18 | $234.88 | $2,348.80 | 75 |
| V | 6 | $355.85 | $348.10 | $2,088.60 | 70 |
| VZ | 49 | $43.12 | $41.59 | $2,037.66 | 65 |
| WFC | 29 | $82.28 | $82.09 | $2,380.61 | 75 |
| WMT | 22 | $97.25 | $94.98 | $2,089.56 | 65 |
| XOM | 22 | $110.17 | $115.54 | $2,541.88 | 85 |

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
| 2025-07-11 15:51:23 | SELL | BAC | 3 | $46.45 | $-6.75 | 65 |
| 2025-07-11 15:51:23 | SELL | INTC | 1 | $23.42 | $1.06 | 65 |
| 2025-07-11 15:51:23 | SELL | PYPL | 1 | $74.56 | $-2.28 | 65 |
| 2025-07-11 15:51:23 | SELL | PFE | 1 | $25.59 | $0.39 | 70 |
| 2025-07-11 15:51:23 | SELL | PG | 1 | $156.91 | $-3.60 | 65 |
| 2025-07-11 15:51:23 | SELL | TGT | 1 | $104.49 | $-0.40 | 65 |
| 2025-07-11 15:51:23 | BUY | DIS | 1 | $120.05 | N/A | 70 |
| 2025-07-11 15:51:23 | BUY | XOM | 1 | $115.55 | N/A | 85 |
| 2025-07-11 15:51:23 | BUY | NKE | 2 | $72.60 | N/A | 75 |
| 2025-07-11 15:51:23 | BUY | MRK | 1 | $82.71 | N/A | 70 |
| 2025-07-11 15:51:23 | BUY | C | 2 | $86.34 | N/A | 75 |
| 2025-07-11 15:51:23 | BUY | CSCO | 3 | $68.04 | N/A | 75 |
| 2025-07-11 15:39:50 | SELL | NKE | 1 | $72.61 | $-3.27 | 65 |
| 2025-07-11 15:39:50 | SELL | PYPL | 1 | $74.61 | $-2.15 | 65 |
| 2025-07-11 15:39:50 | SELL | C | 1 | $86.40 | $-0.27 | 65 |
| 2025-07-11 15:39:50 | SELL | CSCO | 1 | $68.04 | $-0.34 | 65 |
| 2025-07-11 15:39:50 | BUY | BAC | 3 | $46.50 | N/A | 70 |
| 2025-07-11 15:39:50 | BUY | INTC | 6 | $23.40 | N/A | 65 |
| 2025-07-11 15:39:50 | BUY | AMD | 1 | $145.68 | N/A | 85 |
| 2025-07-11 15:39:50 | BUY | KO | 1 | $69.83 | N/A | 65 |
| 2025-07-11 15:39:50 | BUY | PFE | 5 | $25.58 | N/A | 70 |
| 2025-07-11 15:39:50 | BUY | TGT | 1 | $104.45 | N/A | 70 |
| 2025-07-11 15:26:26 | SELL | AMD | 1 | $144.69 | $7.97 | 75 |
| 2025-07-11 15:26:26 | SELL | INTC | 6 | $23.31 | $5.73 | 60 |
| 2025-07-11 15:26:26 | SELL | KO | 1 | $69.85 | $-1.19 | 60 |

<!--TRADE_LOG_END--> 
