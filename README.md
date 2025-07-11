# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 16:55:51**

| Metric | Value |
|---|---|
| **Total Value** | **$100,793.42** |
| Cash | $1,379.49 |
| Holdings Value | $99,413.93 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.02 | $2,110.19 | 65 |
| ADBE | 5 | $377.60 | $365.40 | $1,827.00 | 65 |
| AMD | 18 | $136.77 | $146.20 | $2,631.61 | 85 |
| AMZN | 11 | $221.97 | $225.38 | $2,479.18 | 85 |
| AVGO | 8 | $275.34 | $275.51 | $2,204.08 | 70 |
| AXP | 7 | $325.34 | $321.18 | $2,248.26 | 75 |
| BA | 10 | $212.47 | $226.94 | $2,269.45 | 75 |
| BAC | 47 | $48.70 | $46.53 | $2,187.14 | 70 |
| C | 25 | $86.68 | $86.53 | $2,163.12 | 70 |
| CAT | 5 | $396.39 | $405.21 | $2,026.05 | 65 |
| COST | 2 | $979.83 | $968.60 | $1,937.19 | 65 |
| CRM | 7 | $268.68 | $259.75 | $1,818.22 | 65 |
| CSCO | 30 | $68.42 | $67.87 | $2,036.05 | 65 |
| CVX | 17 | $147.16 | $155.04 | $2,635.68 | 85 |
| DIS | 17 | $122.97 | $120.13 | $2,042.21 | 65 |
| GOOGL | 13 | $179.61 | $179.75 | $2,336.68 | 75 |
| GS | 3 | $717.52 | $703.16 | $2,109.48 | 80 |
| HD | 6 | $372.64 | $369.21 | $2,215.29 | 65 |
| INTC | 86 | $22.35 | $23.45 | $2,017.13 | 65 |
| JNJ | 13 | $155.89 | $156.76 | $2,037.88 | 65 |
| JPM | 9 | $291.61 | $286.44 | $2,577.96 | 75 |
| KO | 27 | $71.10 | $70.06 | $1,891.62 | 60 |
| LLY | 3 | $781.32 | $781.78 | $2,345.34 | 70 |
| MA | 4 | $563.08 | $549.98 | $2,199.90 | 65 |
| META | 3 | $717.12 | $720.29 | $2,160.87 | 75 |
| MRK | 25 | $82.29 | $83.02 | $2,075.50 | 65 |
| MSFT | 5 | $498.84 | $504.65 | $2,523.25 | 85 |
| NFLX | 1 | $1,279.00 | $1,234.74 | $1,234.74 | 65 |
| NKE | 32 | $75.67 | $72.70 | $2,326.41 | 75 |
| NVDA | 16 | $157.38 | $166.29 | $2,660.59 | 85 |
| ORCL | 9 | $233.26 | $232.65 | $2,093.81 | 70 |
| PEP | 15 | $136.57 | $134.29 | $2,014.35 | 65 |
| PFE | 85 | $25.20 | $25.62 | $2,177.71 | 70 |
| PG | 13 | $160.80 | $156.83 | $2,038.77 | 70 |
| PYPL | 31 | $76.59 | $74.45 | $2,307.95 | 75 |
| QCOM | 13 | $162.18 | $158.24 | $2,057.12 | 65 |
| T | 70 | $27.13 | $26.86 | $1,879.89 | 60 |
| TGT | 20 | $104.91 | $104.72 | $2,094.40 | 65 |
| TSLA | 6 | $288.62 | $310.92 | $1,865.52 | 65 |
| UNH | 7 | $298.51 | $300.22 | $2,101.54 | 65 |
| UNP | 10 | $236.18 | $234.76 | $2,347.60 | 75 |
| V | 6 | $355.85 | $347.44 | $2,084.61 | 65 |
| VZ | 49 | $43.12 | $41.67 | $2,042.07 | 65 |
| WFC | 30 | $82.28 | $82.29 | $2,468.70 | 80 |
| WMT | 22 | $97.25 | $94.89 | $2,087.58 | 65 |
| XOM | 21 | $109.97 | $115.44 | $2,424.24 | 75 |

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

<!--TRADE_LOG_END--> 
