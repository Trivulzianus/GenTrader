# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 19:07:43**

| Metric | Value |
|---|---|
| **Total Value** | **$100,653.07** |
| Cash | $1,528.20 |
| Holdings Value | $99,124.87 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.82 | $2,108.20 | 70 |
| ADBE | 5 | $377.60 | $362.98 | $1,814.90 | 65 |
| AMD | 16 | $135.38 | $146.22 | $2,339.52 | 75 |
| AMZN | 11 | $221.97 | $225.33 | $2,478.63 | 75 |
| AVGO | 8 | $275.34 | $273.99 | $2,191.92 | 70 |
| AXP | 7 | $325.34 | $319.55 | $2,236.85 | 75 |
| BA | 10 | $212.57 | $226.63 | $2,266.27 | 70 |
| BAC | 47 | $48.70 | $46.69 | $2,194.43 | 70 |
| C | 27 | $86.66 | $86.72 | $2,341.57 | 75 |
| CAT | 5 | $396.39 | $405.73 | $2,028.62 | 75 |
| COST | 2 | $979.83 | $967.78 | $1,935.56 | 65 |
| CRM | 7 | $268.68 | $258.27 | $1,807.89 | 65 |
| CSCO | 33 | $68.39 | $67.99 | $2,243.67 | 70 |
| CVX | 17 | $147.16 | $155.53 | $2,644.01 | 85 |
| DIS | 17 | $122.96 | $120.15 | $2,042.55 | 65 |
| GOOGL | 13 | $179.61 | $180.57 | $2,347.35 | 75 |
| GS | 3 | $717.52 | $702.98 | $2,108.94 | 70 |
| HD | 6 | $372.64 | $369.77 | $2,218.62 | 65 |
| INTC | 87 | $22.36 | $23.57 | $2,050.59 | 65 |
| JNJ | 13 | $155.89 | $156.86 | $2,039.18 | 65 |
| JPM | 8 | $292.23 | $286.75 | $2,293.96 | 70 |
| KO | 29 | $71.03 | $70.03 | $2,031.01 | 65 |
| LLY | 3 | $781.32 | $784.84 | $2,354.51 | 70 |
| MA | 4 | $563.08 | $547.70 | $2,190.80 | 65 |
| META | 3 | $717.12 | $717.39 | $2,152.18 | 75 |
| MRK | 25 | $82.29 | $83.18 | $2,079.50 | 65 |
| MSFT | 5 | $498.84 | $502.75 | $2,513.75 | 75 |
| NFLX | 1 | $1,279.00 | $1,242.46 | $1,242.46 | 65 |
| NKE | 31 | $75.77 | $72.62 | $2,251.22 | 70 |
| NVDA | 16 | $157.38 | $165.13 | $2,642.08 | 85 |
| ORCL | 9 | $233.26 | $230.29 | $2,072.61 | 70 |
| PEP | 15 | $136.57 | $134.80 | $2,022.00 | 65 |
| PFE | 80 | $25.17 | $25.63 | $2,050.40 | 65 |
| PG | 13 | $160.78 | $157.04 | $2,041.48 | 65 |
| PYPL | 28 | $72.13 | $70.88 | $1,984.50 | 65 |
| QCOM | 13 | $162.18 | $157.91 | $2,052.83 | 65 |
| T | 76 | $27.11 | $27.05 | $2,056.03 | 65 |
| TGT | 20 | $104.91 | $104.39 | $2,087.90 | 65 |
| TSLA | 6 | $288.62 | $310.75 | $1,864.50 | 65 |
| UNH | 7 | $298.51 | $301.45 | $2,110.15 | 65 |
| UNP | 10 | $236.18 | $234.55 | $2,345.50 | 75 |
| V | 6 | $355.85 | $345.65 | $2,073.90 | 65 |
| VZ | 49 | $43.12 | $41.73 | $2,044.53 | 65 |
| WFC | 29 | $82.28 | $82.46 | $2,391.34 | 75 |
| WMT | 22 | $97.25 | $94.45 | $2,078.01 | 65 |
| XOM | 23 | $110.46 | $115.58 | $2,658.45 | 85 |

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
| 2025-07-11 19:07:37 | SELL | PFE | 5 | $25.62 | $2.14 | 65 |
| 2025-07-11 19:07:37 | SELL | BA | 1 | $226.55 | $12.71 | 70 |
| 2025-07-11 19:07:37 | BUY | AMD | 1 | $146.18 | N/A | 75 |
| 2025-07-11 19:07:37 | BUY | C | 1 | $86.73 | N/A | 75 |
| 2025-07-11 18:56:16 | SELL | AMD | 2 | $146.87 | $21.55 | 70 |
| 2025-07-11 18:56:16 | SELL | CSCO | 1 | $68.04 | $-0.34 | 70 |
| 2025-07-11 18:56:16 | SELL | TGT | 1 | $104.61 | $-0.29 | 65 |
| 2025-07-11 18:56:16 | BUY | XOM | 2 | $115.69 | N/A | 85 |
| 2025-07-11 18:56:16 | BUY | PFE | 5 | $25.66 | N/A | 70 |
| 2025-07-11 18:56:16 | BUY | CVX | 1 | $155.79 | N/A | 85 |
| 2025-07-11 18:44:46 | SELL | AMD | 1 | $146.93 | $10.23 | 75 |
| 2025-07-11 18:44:46 | SELL | C | 4 | $86.81 | $0.52 | 70 |
| 2025-07-11 18:44:46 | SELL | CVX | 1 | $155.67 | $8.51 | 75 |
| 2025-07-11 18:44:46 | BUY | KO | 2 | $70.01 | N/A | 65 |
| 2025-07-11 18:44:46 | BUY | CSCO | 3 | $68.04 | N/A | 75 |
| 2025-07-11 18:44:46 | BUY | TGT | 1 | $104.63 | N/A | 70 |
| 2025-07-11 18:27:16 | SELL | JPM | 1 | $286.65 | $-4.96 | 70 |
| 2025-07-11 18:27:16 | SELL | KO | 2 | $70.00 | $-2.06 | 60 |
| 2025-07-11 18:27:16 | SELL | NKE | 1 | $72.65 | $-3.03 | 70 |
| 2025-07-11 18:27:16 | SELL | PFE | 5 | $25.64 | $2.19 | 65 |
| 2025-07-11 18:27:16 | SELL | CSCO | 3 | $67.87 | $-1.50 | 65 |
| 2025-07-11 18:27:16 | BUY | AMD | 3 | $146.78 | N/A | 85 |
| 2025-07-11 18:27:16 | BUY | PYPL | 28 | $72.13 | N/A | 65 |
| 2025-07-11 18:27:16 | BUY | C | 5 | $86.68 | N/A | 85 |
| 2025-07-11 18:27:16 | BUY | BA | 1 | $227.60 | N/A | 85 |

<!--TRADE_LOG_END--> 
