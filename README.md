# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 16:09:20**

| Metric | Value |
|---|---|
| **Total Value** | **$100,627.68** |
| Cash | $622.19 |
| Holdings Value | $100,005.49 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.79 | $2,107.90 | 65 |
| ADBE | 5 | $377.60 | $367.36 | $1,836.81 | 65 |
| AMD | 18 | $136.77 | $145.41 | $2,617.38 | 85 |
| AMZN | 11 | $221.97 | $225.42 | $2,479.62 | 85 |
| AVGO | 8 | $275.34 | $275.69 | $2,205.56 | 70 |
| AXP | 7 | $325.34 | $321.26 | $2,248.86 | 75 |
| BA | 9 | $210.85 | $226.84 | $2,041.61 | 65 |
| BAC | 44 | $48.85 | $46.42 | $2,042.48 | 65 |
| C | 26 | $86.66 | $86.25 | $2,242.50 | 70 |
| CAT | 6 | $397.86 | $404.32 | $2,425.95 | 65 |
| COST | 2 | $979.83 | $966.65 | $1,933.31 | 65 |
| CRM | 7 | $268.68 | $259.67 | $1,817.69 | 65 |
| CSCO | 34 | $68.35 | $67.94 | $2,310.12 | 75 |
| CVX | 17 | $147.16 | $154.96 | $2,634.32 | 85 |
| DIS | 18 | $122.80 | $119.98 | $2,159.64 | 65 |
| GOOGL | 13 | $179.61 | $179.65 | $2,335.45 | 70 |
| GS | 3 | $717.52 | $701.66 | $2,104.99 | 65 |
| HD | 6 | $372.64 | $368.19 | $2,209.17 | 65 |
| INTC | 87 | $22.36 | $23.43 | $2,038.41 | 65 |
| JNJ | 13 | $155.89 | $156.09 | $2,029.11 | 65 |
| JPM | 9 | $291.61 | $285.71 | $2,571.43 | 75 |
| KO | 29 | $71.03 | $69.81 | $2,024.63 | 65 |
| LLY | 3 | $781.32 | $780.49 | $2,341.47 | 70 |
| MA | 4 | $563.08 | $548.37 | $2,193.48 | 65 |
| META | 3 | $717.12 | $719.16 | $2,157.49 | 75 |
| MRK | 25 | $82.29 | $82.84 | $2,071.12 | 65 |
| MSFT | 5 | $498.84 | $504.26 | $2,521.30 | 85 |
| NFLX | 1 | $1,279.00 | $1,237.00 | $1,237.00 | 60 |
| NKE | 32 | $75.67 | $72.63 | $2,324.16 | 75 |
| NVDA | 16 | $157.38 | $166.15 | $2,658.32 | 85 |
| ORCL | 9 | $233.26 | $232.36 | $2,091.24 | 65 |
| PEP | 15 | $136.57 | $133.93 | $2,008.90 | 65 |
| PFE | 85 | $25.20 | $25.56 | $2,172.59 | 70 |
| PG | 13 | $160.80 | $156.66 | $2,036.52 | 65 |
| PYPL | 31 | $76.58 | $74.33 | $2,304.23 | 75 |
| QCOM | 13 | $162.18 | $157.88 | $2,052.39 | 65 |
| T | 76 | $27.10 | $26.65 | $2,025.40 | 65 |
| TGT | 20 | $104.91 | $104.50 | $2,090.00 | 65 |
| TSLA | 6 | $288.62 | $308.90 | $1,853.40 | 65 |
| UNH | 7 | $298.51 | $300.70 | $2,104.90 | 65 |
| UNP | 10 | $236.18 | $234.32 | $2,343.20 | 75 |
| V | 6 | $355.85 | $346.76 | $2,080.59 | 65 |
| VZ | 49 | $43.12 | $41.53 | $2,034.97 | 65 |
| WFC | 29 | $82.28 | $82.03 | $2,378.87 | 75 |
| WMT | 22 | $97.25 | $94.81 | $2,085.71 | 65 |
| XOM | 21 | $109.93 | $115.30 | $2,421.30 | 75 |

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

<!--TRADE_LOG_END--> 
