# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 18:27:22**

| Metric | Value |
|---|---|
| **Total Value** | **$100,743.97** |
| Cash | $1,254.44 |
| Holdings Value | $99,489.53 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.46 | $2,114.60 | 70 |
| ADBE | 5 | $377.60 | $364.72 | $1,823.58 | 65 |
| AMD | 18 | $136.70 | $146.81 | $2,642.58 | 85 |
| AMZN | 11 | $221.97 | $225.99 | $2,485.91 | 75 |
| AVGO | 8 | $275.34 | $274.87 | $2,198.92 | 65 |
| AXP | 7 | $325.34 | $320.07 | $2,240.49 | 70 |
| BA | 11 | $213.84 | $227.46 | $2,502.06 | 85 |
| BAC | 47 | $48.70 | $46.64 | $2,192.08 | 70 |
| C | 30 | $86.68 | $86.67 | $2,600.22 | 85 |
| CAT | 5 | $396.39 | $405.65 | $2,028.26 | 70 |
| COST | 2 | $979.83 | $967.85 | $1,935.70 | 65 |
| CRM | 7 | $268.68 | $259.26 | $1,814.85 | 65 |
| CSCO | 31 | $68.42 | $67.86 | $2,103.82 | 65 |
| CVX | 17 | $147.16 | $155.20 | $2,638.40 | 85 |
| DIS | 17 | $122.96 | $120.27 | $2,044.52 | 65 |
| GOOGL | 13 | $179.61 | $181.21 | $2,355.73 | 75 |
| GS | 3 | $717.52 | $703.14 | $2,109.42 | 70 |
| HD | 6 | $372.64 | $369.54 | $2,217.24 | 70 |
| INTC | 87 | $22.36 | $23.55 | $2,049.28 | 65 |
| JNJ | 13 | $155.89 | $156.96 | $2,040.48 | 65 |
| JPM | 8 | $292.23 | $286.65 | $2,293.20 | 70 |
| KO | 27 | $71.10 | $69.96 | $1,888.92 | 60 |
| LLY | 3 | $781.32 | $785.29 | $2,355.87 | 70 |
| MA | 4 | $563.08 | $546.60 | $2,186.40 | 65 |
| META | 3 | $717.12 | $718.50 | $2,155.50 | 75 |
| MRK | 25 | $82.29 | $83.15 | $2,078.75 | 65 |
| MSFT | 5 | $498.84 | $504.31 | $2,521.55 | 85 |
| NFLX | 1 | $1,279.00 | $1,243.90 | $1,243.90 | 65 |
| NKE | 31 | $75.77 | $72.64 | $2,251.84 | 70 |
| NVDA | 16 | $157.38 | $165.62 | $2,649.84 | 85 |
| ORCL | 9 | $233.26 | $231.32 | $2,081.88 | 65 |
| PEP | 15 | $136.57 | $134.52 | $2,017.86 | 60 |
| PFE | 80 | $25.17 | $25.63 | $2,050.40 | 65 |
| PG | 13 | $160.78 | $156.70 | $2,037.10 | 65 |
| PYPL | 28 | $72.13 | $72.07 | $2,017.96 | 65 |
| QCOM | 13 | $162.18 | $158.50 | $2,060.50 | 65 |
| T | 76 | $27.11 | $26.99 | $2,051.60 | 65 |
| TGT | 20 | $104.91 | $104.08 | $2,081.70 | 65 |
| TSLA | 6 | $288.62 | $312.42 | $1,874.52 | 65 |
| UNH | 7 | $298.51 | $301.03 | $2,107.21 | 65 |
| UNP | 10 | $236.18 | $234.34 | $2,343.40 | 75 |
| V | 6 | $355.85 | $344.99 | $2,069.94 | 65 |
| VZ | 49 | $43.12 | $41.65 | $2,040.85 | 65 |
| WFC | 29 | $82.28 | $82.44 | $2,390.76 | 75 |
| WMT | 22 | $97.25 | $94.44 | $2,077.79 | 65 |
| XOM | 21 | $109.97 | $115.34 | $2,422.14 | 75 |

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
| 2025-07-11 18:27:16 | SELL | JPM | 1 | $286.65 | $-4.96 | 70 |
| 2025-07-11 18:27:16 | SELL | KO | 2 | $70.00 | $-2.06 | 60 |
| 2025-07-11 18:27:16 | SELL | NKE | 1 | $72.65 | $-3.03 | 70 |
| 2025-07-11 18:27:16 | SELL | PFE | 5 | $25.64 | $2.19 | 65 |
| 2025-07-11 18:27:16 | SELL | CSCO | 3 | $67.87 | $-1.50 | 65 |
| 2025-07-11 18:27:16 | BUY | AMD | 3 | $146.78 | N/A | 85 |
| 2025-07-11 18:27:16 | BUY | PYPL | 28 | $72.13 | N/A | 65 |
| 2025-07-11 18:27:16 | BUY | C | 5 | $86.68 | N/A | 85 |
| 2025-07-11 18:27:16 | BUY | BA | 1 | $227.60 | N/A | 85 |
| 2025-07-11 18:27:00 | SELL | PYPL | 31 | $72.18 | $-136.62 | 75 |
| 2025-07-11 18:10:51 | SELL | AMD | 1 | $146.83 | $11.39 | 70 |
| 2025-07-11 18:10:51 | BUY | PFE | 5 | $25.64 | N/A | 70 |
| 2025-07-11 18:10:51 | BUY | CSCO | 3 | $67.85 | N/A | 75 |
| 2025-07-11 17:50:55 | SELL | DIS | 1 | $120.42 | $-2.40 | 65 |
| 2025-07-11 17:50:55 | SELL | PG | 1 | $157.15 | $-3.37 | 65 |
| 2025-07-11 17:50:55 | SELL | CSCO | 2 | $67.79 | $-1.18 | 65 |
| 2025-07-11 17:50:55 | BUY | AMD | 1 | $146.52 | N/A | 75 |
| 2025-07-11 17:50:55 | BUY | NKE | 1 | $72.71 | N/A | 75 |
| 2025-07-11 17:50:55 | BUY | PYPL | 2 | $74.49 | N/A | 75 |
| 2025-07-11 17:39:21 | SELL | PFE | 6 | $25.67 | $2.77 | 65 |
| 2025-07-11 17:39:21 | BUY | AMD | 1 | $146.68 | N/A | 70 |
| 2025-07-11 17:39:21 | BUY | INTC | 1 | $23.49 | N/A | 65 |
| 2025-07-11 17:39:21 | BUY | PG | 1 | $156.99 | N/A | 70 |
| 2025-07-11 17:39:21 | BUY | T | 1 | $26.92 | N/A | 65 |
| 2025-07-11 17:25:53 | SELL | XOM | 2 | $115.33 | $9.80 | 75 |

<!--TRADE_LOG_END--> 
