# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 17:08:54**

| Metric | Value |
|---|---|
| **Total Value** | **$100,837.10** |
| Cash | $1,882.39 |
| Holdings Value | $98,954.71 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.22 | $2,112.20 | 65 |
| ADBE | 5 | $377.60 | $364.91 | $1,824.55 | 65 |
| AMD | 14 | $133.84 | $146.94 | $2,057.11 | 65 |
| AMZN | 11 | $221.97 | $225.32 | $2,478.52 | 75 |
| AVGO | 8 | $275.34 | $275.74 | $2,205.92 | 70 |
| AXP | 7 | $325.34 | $321.31 | $2,249.17 | 75 |
| BA | 10 | $212.47 | $227.16 | $2,271.61 | 75 |
| BAC | 47 | $48.70 | $46.58 | $2,189.03 | 70 |
| C | 24 | $86.68 | $86.59 | $2,078.21 | 65 |
| CAT | 5 | $396.39 | $405.14 | $2,025.72 | 70 |
| COST | 2 | $979.83 | $969.14 | $1,938.28 | 65 |
| CRM | 7 | $268.68 | $259.53 | $1,816.71 | 65 |
| CSCO | 34 | $68.37 | $67.96 | $2,310.76 | 75 |
| CVX | 17 | $147.16 | $154.99 | $2,634.83 | 85 |
| DIS | 17 | $122.97 | $120.27 | $2,044.59 | 65 |
| GOOGL | 13 | $179.61 | $180.07 | $2,340.91 | 75 |
| GS | 3 | $717.52 | $703.42 | $2,110.27 | 70 |
| HD | 6 | $372.64 | $368.94 | $2,213.64 | 65 |
| INTC | 81 | $22.28 | $23.48 | $1,902.18 | 60 |
| JNJ | 13 | $155.89 | $156.80 | $2,038.40 | 65 |
| JPM | 9 | $291.61 | $286.68 | $2,580.08 | 75 |
| KO | 29 | $71.02 | $69.98 | $2,029.57 | 65 |
| LLY | 3 | $781.32 | $781.14 | $2,343.42 | 70 |
| MA | 4 | $563.08 | $549.64 | $2,198.56 | 60 |
| META | 3 | $717.12 | $721.23 | $2,163.69 | 75 |
| MRK | 25 | $82.29 | $83.02 | $2,075.38 | 65 |
| MSFT | 5 | $498.84 | $504.80 | $2,524.00 | 85 |
| NFLX | 1 | $1,279.00 | $1,237.06 | $1,237.06 | 65 |
| NKE | 31 | $75.77 | $72.67 | $2,252.92 | 70 |
| NVDA | 16 | $157.38 | $166.46 | $2,663.36 | 85 |
| ORCL | 9 | $233.26 | $232.64 | $2,093.76 | 70 |
| PEP | 15 | $136.57 | $134.17 | $2,012.55 | 65 |
| PFE | 86 | $25.20 | $25.61 | $2,202.89 | 70 |
| PG | 13 | $160.80 | $156.84 | $2,038.92 | 65 |
| PYPL | 28 | $76.80 | $74.58 | $2,088.34 | 65 |
| QCOM | 13 | $162.18 | $158.48 | $2,060.23 | 65 |
| T | 70 | $27.13 | $26.95 | $1,886.15 | 60 |
| TGT | 20 | $104.91 | $104.69 | $2,093.80 | 65 |
| TSLA | 6 | $288.62 | $310.78 | $1,864.68 | 65 |
| UNH | 7 | $298.51 | $300.29 | $2,102.00 | 65 |
| UNP | 10 | $236.18 | $234.63 | $2,346.33 | 75 |
| V | 6 | $355.85 | $347.81 | $2,086.89 | 65 |
| VZ | 49 | $43.12 | $41.69 | $2,042.81 | 65 |
| WFC | 29 | $82.28 | $82.36 | $2,388.30 | 75 |
| WMT | 22 | $97.25 | $94.76 | $2,084.65 | 65 |
| XOM | 23 | $110.43 | $115.30 | $2,651.78 | 85 |

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
| 2025-07-11 17:08:48 | SELL | INTC | 5 | $23.48 | $5.67 | 60 |
| 2025-07-11 17:08:48 | SELL | AMD | 4 | $147.03 | $41.02 | 65 |
| 2025-07-11 17:08:48 | SELL | NKE | 1 | $72.68 | $-3.00 | 70 |
| 2025-07-11 17:08:48 | SELL | PYPL | 3 | $74.58 | $-6.01 | 65 |
| 2025-07-11 17:08:48 | SELL | WFC | 1 | $82.36 | $0.07 | 75 |
| 2025-07-11 17:08:48 | SELL | C | 1 | $86.60 | $-0.08 | 65 |
| 2025-07-11 17:08:48 | BUY | XOM | 2 | $115.29 | N/A | 85 |
| 2025-07-11 17:08:48 | BUY | KO | 2 | $69.99 | N/A | 65 |
| 2025-07-11 17:08:48 | BUY | PFE | 1 | $25.61 | N/A | 70 |
| 2025-07-11 17:08:48 | BUY | CSCO | 4 | $67.96 | N/A | 75 |
| 2025-07-11 16:55:43 | SELL | MRK | 1 | $83.01 | $0.69 | 65 |
| 2025-07-11 16:55:43 | SELL | KO | 2 | $70.07 | $-1.93 | 60 |
| 2025-07-11 16:55:43 | SELL | CAT | 1 | $405.21 | $7.35 | 65 |
| 2025-07-11 16:55:43 | SELL | CSCO | 4 | $67.86 | $-2.00 | 65 |
| 2025-07-11 16:55:43 | SELL | T | 1 | $26.86 | $-0.26 | 60 |
| 2025-07-11 16:55:43 | BUY | PYPL | 3 | $74.43 | N/A | 75 |
| 2025-07-11 16:55:43 | BUY | C | 1 | $86.51 | N/A | 70 |
| 2025-07-11 16:43:13 | SELL | XOM | 2 | $114.93 | $9.06 | 75 |
| 2025-07-11 16:43:13 | SELL | DIS | 1 | $119.90 | $-2.89 | 65 |
| 2025-07-11 16:43:13 | SELL | T | 5 | $26.77 | $-1.62 | 60 |
| 2025-07-11 16:43:13 | BUY | BAC | 3 | $46.49 | N/A | 70 |
| 2025-07-11 16:43:13 | BUY | INTC | 5 | $23.38 | N/A | 65 |
| 2025-07-11 16:43:13 | BUY | MRK | 1 | $82.97 | N/A | 70 |
| 2025-07-11 16:43:13 | BUY | WFC | 1 | $82.21 | N/A | 80 |
| 2025-07-11 16:26:51 | SELL | INTC | 6 | $23.36 | $6.00 | 60 |

<!--TRADE_LOG_END--> 
