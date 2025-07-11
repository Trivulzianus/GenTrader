# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 19:25:02**

| Metric | Value |
|---|---|
| **Total Value** | **$100,795.11** |
| Cash | $1,657.58 |
| Holdings Value | $99,137.53 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.25 | $2,112.50 | 70 |
| ADBE | 5 | $377.60 | $363.62 | $1,818.10 | 65 |
| AMD | 16 | $135.38 | $146.43 | $2,342.88 | 75 |
| AMZN | 11 | $221.97 | $225.94 | $2,485.28 | 75 |
| AVGO | 8 | $275.34 | $274.71 | $2,197.68 | 70 |
| AXP | 7 | $325.34 | $320.23 | $2,241.61 | 75 |
| BA | 10 | $212.57 | $226.74 | $2,267.40 | 75 |
| BAC | 47 | $48.70 | $46.73 | $2,196.55 | 70 |
| C | 26 | $86.65 | $86.78 | $2,256.15 | 70 |
| CAT | 5 | $396.39 | $406.46 | $2,032.30 | 70 |
| COST | 2 | $979.83 | $969.12 | $1,938.24 | 65 |
| CRM | 7 | $268.68 | $258.24 | $1,807.68 | 65 |
| CSCO | 34 | $68.38 | $68.08 | $2,314.72 | 75 |
| CVX | 17 | $147.16 | $155.60 | $2,645.20 | 85 |
| DIS | 18 | $122.80 | $120.18 | $2,163.24 | 70 |
| GOOGL | 13 | $179.61 | $180.54 | $2,347.02 | 75 |
| GS | 3 | $717.52 | $704.73 | $2,114.19 | 70 |
| HD | 6 | $372.64 | $370.38 | $2,222.31 | 65 |
| INTC | 87 | $22.36 | $23.52 | $2,045.81 | 65 |
| JNJ | 13 | $155.89 | $157.05 | $2,041.65 | 65 |
| JPM | 8 | $292.23 | $286.89 | $2,295.13 | 75 |
| KO | 29 | $71.03 | $70.08 | $2,032.46 | 65 |
| LLY | 3 | $781.32 | $786.24 | $2,358.72 | 70 |
| MA | 4 | $563.08 | $549.27 | $2,197.10 | 65 |
| META | 3 | $717.12 | $719.30 | $2,157.90 | 75 |
| MRK | 25 | $82.29 | $83.26 | $2,081.50 | 65 |
| MSFT | 5 | $498.84 | $503.69 | $2,518.47 | 85 |
| NFLX | 1 | $1,279.00 | $1,243.81 | $1,243.81 | 65 |
| NKE | 31 | $75.77 | $72.81 | $2,257.13 | 70 |
| NVDA | 16 | $157.38 | $165.11 | $2,641.83 | 85 |
| ORCL | 9 | $233.26 | $230.98 | $2,078.82 | 65 |
| PEP | 15 | $136.57 | $135.14 | $2,027.10 | 65 |
| PFE | 80 | $25.17 | $25.65 | $2,052.34 | 65 |
| PG | 13 | $160.78 | $157.20 | $2,043.60 | 65 |
| PYPL | 28 | $72.13 | $71.11 | $1,991.08 | 65 |
| QCOM | 13 | $162.18 | $158.16 | $2,056.08 | 65 |
| T | 76 | $27.11 | $27.05 | $2,055.42 | 65 |
| TGT | 20 | $104.91 | $104.64 | $2,092.90 | 65 |
| TSLA | 6 | $288.62 | $313.23 | $1,879.38 | 65 |
| UNH | 7 | $298.51 | $302.13 | $2,114.90 | 65 |
| UNP | 10 | $236.18 | $234.67 | $2,346.70 | 75 |
| V | 6 | $355.85 | $347.06 | $2,082.36 | 70 |
| VZ | 49 | $43.12 | $41.73 | $2,044.53 | 65 |
| WFC | 29 | $82.28 | $82.53 | $2,393.37 | 75 |
| WMT | 22 | $97.25 | $94.57 | $2,080.54 | 65 |
| XOM | 21 | $109.99 | $115.42 | $2,423.85 | 75 |

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
| 2025-07-11 19:24:57 | SELL | XOM | 2 | $115.43 | $9.94 | 75 |
| 2025-07-11 19:24:57 | SELL | C | 1 | $86.78 | $0.12 | 70 |
| 2025-07-11 19:24:57 | BUY | DIS | 1 | $120.19 | N/A | 70 |
| 2025-07-11 19:24:57 | BUY | CSCO | 1 | $68.08 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
