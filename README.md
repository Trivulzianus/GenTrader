# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 17:39:26**

| Metric | Value |
|---|---|
| **Total Value** | **$100,787.84** |
| Cash | $1,446.90 |
| Holdings Value | $99,340.93 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.97 | $2,109.70 | 70 |
| ADBE | 5 | $377.60 | $364.64 | $1,823.20 | 65 |
| AMD | 15 | $134.70 | $146.61 | $2,199.15 | 70 |
| AMZN | 11 | $221.97 | $225.02 | $2,475.22 | 80 |
| AVGO | 8 | $275.34 | $272.76 | $2,182.08 | 65 |
| AXP | 7 | $325.34 | $320.86 | $2,246.02 | 75 |
| BA | 10 | $212.47 | $227.56 | $2,275.60 | 70 |
| BAC | 47 | $48.70 | $46.52 | $2,186.44 | 70 |
| C | 25 | $86.67 | $86.53 | $2,163.25 | 70 |
| CAT | 5 | $396.39 | $405.13 | $2,025.65 | 65 |
| COST | 2 | $979.83 | $967.66 | $1,935.32 | 65 |
| CRM | 7 | $268.68 | $259.32 | $1,815.27 | 65 |
| CSCO | 33 | $68.38 | $67.72 | $2,234.76 | 70 |
| CVX | 17 | $147.16 | $155.33 | $2,640.61 | 85 |
| DIS | 18 | $122.82 | $120.22 | $2,163.96 | 65 |
| GOOGL | 13 | $179.61 | $180.34 | $2,344.42 | 75 |
| GS | 3 | $717.52 | $702.79 | $2,108.37 | 85 |
| HD | 6 | $372.64 | $369.75 | $2,218.50 | 65 |
| INTC | 87 | $22.36 | $23.48 | $2,043.18 | 65 |
| JNJ | 13 | $155.89 | $156.92 | $2,039.96 | 65 |
| JPM | 9 | $291.61 | $286.49 | $2,578.37 | 75 |
| KO | 29 | $71.02 | $70.07 | $2,032.03 | 65 |
| LLY | 3 | $781.32 | $783.15 | $2,349.45 | 70 |
| MA | 4 | $563.08 | $548.86 | $2,195.45 | 60 |
| META | 3 | $717.12 | $718.58 | $2,155.74 | 75 |
| MRK | 25 | $82.29 | $83.19 | $2,079.75 | 65 |
| MSFT | 5 | $498.84 | $503.45 | $2,517.25 | 85 |
| NFLX | 1 | $1,279.00 | $1,234.73 | $1,234.73 | 65 |
| NKE | 31 | $75.77 | $72.74 | $2,254.94 | 70 |
| NVDA | 16 | $157.38 | $165.91 | $2,654.64 | 85 |
| ORCL | 9 | $233.26 | $231.46 | $2,083.14 | 65 |
| PEP | 15 | $136.57 | $134.59 | $2,018.85 | 65 |
| PFE | 80 | $25.17 | $25.66 | $2,053.20 | 65 |
| PG | 14 | $160.52 | $157.02 | $2,198.28 | 70 |
| PYPL | 29 | $76.73 | $74.56 | $2,162.24 | 70 |
| QCOM | 13 | $162.18 | $158.31 | $2,058.04 | 65 |
| T | 76 | $27.11 | $26.92 | $2,045.92 | 65 |
| TGT | 20 | $104.91 | $104.80 | $2,096.00 | 65 |
| TSLA | 6 | $288.62 | $310.12 | $1,860.69 | 65 |
| UNH | 7 | $298.51 | $302.50 | $2,117.50 | 65 |
| UNP | 10 | $236.18 | $234.77 | $2,347.70 | 75 |
| V | 6 | $355.85 | $346.82 | $2,080.95 | 65 |
| VZ | 49 | $43.12 | $41.75 | $2,045.66 | 65 |
| WFC | 29 | $82.28 | $82.25 | $2,385.39 | 75 |
| WMT | 22 | $97.25 | $94.57 | $2,080.54 | 65 |
| XOM | 21 | $109.97 | $115.42 | $2,423.82 | 75 |

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
| 2025-07-11 17:39:21 | SELL | PFE | 6 | $25.67 | $2.77 | 65 |
| 2025-07-11 17:39:21 | BUY | AMD | 1 | $146.68 | N/A | 70 |
| 2025-07-11 17:39:21 | BUY | INTC | 1 | $23.49 | N/A | 65 |
| 2025-07-11 17:39:21 | BUY | PG | 1 | $156.99 | N/A | 70 |
| 2025-07-11 17:39:21 | BUY | T | 1 | $26.92 | N/A | 65 |
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

<!--TRADE_LOG_END--> 
