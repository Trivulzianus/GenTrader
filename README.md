# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 17:26:00**

| Metric | Value |
|---|---|
| **Total Value** | **$100,841.35** |
| Cash | $1,646.99 |
| Holdings Value | $99,194.36 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.08 | $2,110.80 | 70 |
| ADBE | 5 | $377.60 | $364.78 | $1,823.90 | 65 |
| AMD | 14 | $133.84 | $147.07 | $2,058.96 | 70 |
| AMZN | 11 | $221.97 | $225.44 | $2,479.84 | 75 |
| AVGO | 8 | $275.34 | $274.07 | $2,192.56 | 70 |
| AXP | 7 | $325.34 | $320.96 | $2,246.72 | 75 |
| BA | 10 | $212.47 | $227.60 | $2,276.05 | 75 |
| BAC | 47 | $48.70 | $46.53 | $2,187.14 | 70 |
| C | 25 | $86.67 | $86.53 | $2,163.25 | 70 |
| CAT | 5 | $396.39 | $405.27 | $2,026.38 | 70 |
| COST | 2 | $979.83 | $969.39 | $1,938.78 | 65 |
| CRM | 7 | $268.68 | $259.59 | $1,817.13 | 65 |
| CSCO | 33 | $68.38 | $67.89 | $2,240.21 | 70 |
| CVX | 17 | $147.16 | $155.15 | $2,637.55 | 85 |
| DIS | 18 | $122.82 | $120.27 | $2,164.80 | 70 |
| GOOGL | 13 | $179.61 | $180.60 | $2,347.80 | 75 |
| GS | 3 | $717.52 | $703.28 | $2,109.84 | 85 |
| HD | 6 | $372.64 | $369.60 | $2,217.60 | 70 |
| INTC | 86 | $22.35 | $23.55 | $2,025.71 | 65 |
| JNJ | 13 | $155.89 | $156.82 | $2,038.62 | 65 |
| JPM | 9 | $291.61 | $286.67 | $2,580.01 | 75 |
| KO | 29 | $71.02 | $70.07 | $2,031.93 | 65 |
| LLY | 3 | $781.32 | $781.57 | $2,344.70 | 70 |
| MA | 4 | $563.08 | $548.27 | $2,193.10 | 65 |
| META | 3 | $717.12 | $721.17 | $2,163.52 | 75 |
| MRK | 25 | $82.29 | $83.03 | $2,075.75 | 65 |
| MSFT | 5 | $498.84 | $504.52 | $2,522.60 | 85 |
| NFLX | 1 | $1,279.00 | $1,236.60 | $1,236.60 | 65 |
| NKE | 31 | $75.77 | $72.67 | $2,252.92 | 70 |
| NVDA | 16 | $157.38 | $166.27 | $2,660.32 | 85 |
| ORCL | 9 | $233.26 | $232.37 | $2,091.33 | 70 |
| PEP | 15 | $136.57 | $134.19 | $2,012.85 | 65 |
| PFE | 86 | $25.20 | $25.63 | $2,203.76 | 70 |
| PG | 13 | $160.80 | $156.83 | $2,038.79 | 65 |
| PYPL | 29 | $76.73 | $74.61 | $2,163.84 | 70 |
| QCOM | 13 | $162.18 | $158.45 | $2,059.85 | 65 |
| T | 75 | $27.12 | $26.95 | $2,021.25 | 65 |
| TGT | 20 | $104.91 | $104.89 | $2,097.70 | 70 |
| TSLA | 6 | $288.62 | $311.08 | $1,866.48 | 65 |
| UNH | 7 | $298.51 | $300.83 | $2,105.84 | 65 |
| UNP | 10 | $236.18 | $234.73 | $2,347.28 | 70 |
| V | 6 | $355.85 | $347.14 | $2,082.84 | 65 |
| VZ | 49 | $43.12 | $41.74 | $2,045.50 | 65 |
| WFC | 29 | $82.28 | $82.29 | $2,386.41 | 75 |
| WMT | 22 | $97.25 | $94.71 | $2,083.62 | 65 |
| XOM | 21 | $109.97 | $115.33 | $2,421.93 | 75 |

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
| 2025-07-11 17:25:53 | SELL | XOM | 2 | $115.33 | $9.80 | 75 |
| 2025-07-11 17:25:53 | SELL | CSCO | 1 | $67.88 | $-0.49 | 70 |
| 2025-07-11 17:25:53 | BUY | INTC | 5 | $23.55 | N/A | 65 |
| 2025-07-11 17:25:53 | BUY | DIS | 1 | $120.27 | N/A | 70 |
| 2025-07-11 17:25:53 | BUY | PYPL | 1 | $74.60 | N/A | 70 |
| 2025-07-11 17:25:53 | BUY | C | 1 | $86.52 | N/A | 70 |
| 2025-07-11 17:25:53 | BUY | T | 5 | $26.97 | N/A | 65 |
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

<!--TRADE_LOG_END--> 
