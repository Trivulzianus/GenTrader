# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 15:39:56**

| Metric | Value |
|---|---|
| **Total Value** | **$100,761.00** |
| Cash | $1,133.33 |
| Holdings Value | $99,627.68 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.85 | $2,108.50 | 65 |
| ADBE | 5 | $377.60 | $367.40 | $1,837.00 | 65 |
| AMD | 18 | $136.77 | $145.65 | $2,621.70 | 85 |
| AMZN | 11 | $221.97 | $225.15 | $2,476.65 | 75 |
| AVGO | 8 | $275.34 | $275.06 | $2,200.44 | 70 |
| AXP | 7 | $325.34 | $322.74 | $2,259.14 | 75 |
| BA | 9 | $210.85 | $228.11 | $2,052.97 | 65 |
| BAC | 47 | $48.70 | $46.48 | $2,184.80 | 70 |
| C | 24 | $86.69 | $86.39 | $2,073.36 | 65 |
| CAT | 6 | $397.86 | $405.70 | $2,434.20 | 65 |
| COST | 2 | $979.83 | $967.82 | $1,935.64 | 65 |
| CRM | 7 | $268.68 | $259.83 | $1,818.81 | 65 |
| CSCO | 31 | $68.38 | $68.03 | $2,109.09 | 65 |
| CVX | 17 | $147.16 | $155.23 | $2,638.91 | 85 |
| DIS | 17 | $122.96 | $120.09 | $2,041.53 | 65 |
| GOOGL | 13 | $179.61 | $179.91 | $2,338.83 | 75 |
| GS | 3 | $717.52 | $703.71 | $2,111.13 | 70 |
| HD | 6 | $372.64 | $368.89 | $2,213.37 | 70 |
| INTC | 87 | $22.36 | $23.41 | $2,036.24 | 65 |
| JNJ | 13 | $155.89 | $156.06 | $2,028.78 | 65 |
| JPM | 9 | $291.61 | $286.56 | $2,579.04 | 75 |
| KO | 29 | $71.03 | $69.83 | $2,024.93 | 65 |
| LLY | 3 | $781.32 | $782.63 | $2,347.90 | 70 |
| MA | 4 | $563.08 | $552.05 | $2,208.22 | 65 |
| META | 3 | $717.12 | $716.93 | $2,150.80 | 75 |
| MRK | 25 | $82.30 | $82.72 | $2,067.88 | 65 |
| MSFT | 5 | $498.84 | $503.15 | $2,515.77 | 85 |
| NFLX | 1 | $1,279.00 | $1,239.01 | $1,239.01 | 65 |
| NKE | 29 | $75.99 | $72.58 | $2,104.96 | 65 |
| NVDA | 16 | $157.38 | $166.94 | $2,670.96 | 85 |
| ORCL | 9 | $233.26 | $232.43 | $2,091.87 | 70 |
| PEP | 15 | $136.57 | $134.01 | $2,010.14 | 65 |
| PFE | 86 | $25.20 | $25.58 | $2,199.60 | 70 |
| PG | 14 | $160.52 | $156.90 | $2,196.60 | 65 |
| PYPL | 28 | $76.84 | $74.62 | $2,089.36 | 65 |
| QCOM | 13 | $162.18 | $158.12 | $2,055.56 | 65 |
| T | 76 | $27.10 | $26.75 | $2,033.38 | 65 |
| TGT | 21 | $104.89 | $104.45 | $2,193.45 | 70 |
| TSLA | 6 | $288.62 | $308.48 | $1,850.88 | 65 |
| UNH | 7 | $298.51 | $300.41 | $2,102.87 | 65 |
| UNP | 10 | $236.18 | $235.06 | $2,350.55 | 75 |
| V | 6 | $355.85 | $348.92 | $2,093.49 | 65 |
| VZ | 49 | $43.12 | $41.58 | $2,037.18 | 65 |
| WFC | 29 | $82.28 | $82.25 | $2,385.25 | 75 |
| WMT | 22 | $97.25 | $94.79 | $2,085.34 | 65 |
| XOM | 21 | $109.92 | $115.31 | $2,421.61 | 75 |

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
| 2025-07-11 15:26:26 | SELL | XOM | 2 | $115.29 | $9.81 | 75 |
| 2025-07-11 15:26:26 | SELL | MRK | 1 | $82.43 | $0.13 | 65 |
| 2025-07-11 15:26:26 | BUY | PYPL | 1 | $74.56 | N/A | 70 |
| 2025-07-11 15:26:26 | BUY | NKE | 1 | $72.74 | N/A | 70 |
| 2025-07-11 15:26:26 | BUY | C | 1 | $86.32 | N/A | 70 |
| 2025-07-11 15:08:26 | SELL | BAC | 3 | $46.47 | $-6.67 | 65 |
| 2025-07-11 15:08:26 | SELL | DIS | 1 | $120.31 | $-2.50 | 65 |
| 2025-07-11 15:08:26 | SELL | PFE | 6 | $25.45 | $1.54 | 65 |
| 2025-07-11 15:08:26 | SELL | PYPL | 3 | $74.53 | $-6.25 | 65 |
| 2025-07-11 15:08:26 | SELL | NKE | 2 | $72.54 | $-6.44 | 65 |
| 2025-07-11 15:08:26 | SELL | C | 1 | $86.31 | $-0.37 | 65 |
| 2025-07-11 15:08:26 | BUY | AMD | 2 | $144.16 | N/A | 85 |

<!--TRADE_LOG_END--> 
