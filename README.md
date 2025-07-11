# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 18:10:56**

| Metric | Value |
|---|---|
| **Total Value** | **$100,829.24** |
| Cash | $1,306.92 |
| Holdings Value | $99,522.32 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.36 | $2,113.60 | 70 |
| ADBE | 5 | $377.60 | $364.25 | $1,821.23 | 65 |
| AMD | 15 | $134.68 | $146.79 | $2,201.86 | 70 |
| AMZN | 11 | $221.97 | $226.25 | $2,488.79 | 85 |
| AVGO | 8 | $275.34 | $274.82 | $2,198.57 | 65 |
| AXP | 7 | $325.34 | $320.72 | $2,245.04 | 75 |
| BA | 10 | $212.47 | $227.75 | $2,277.50 | 75 |
| BAC | 47 | $48.70 | $46.65 | $2,192.32 | 70 |
| C | 25 | $86.67 | $86.65 | $2,166.25 | 70 |
| CAT | 5 | $396.39 | $405.13 | $2,025.65 | 70 |
| COST | 2 | $979.83 | $967.61 | $1,935.21 | 65 |
| CRM | 7 | $268.68 | $259.14 | $1,814.01 | 65 |
| CSCO | 34 | $68.37 | $67.84 | $2,306.73 | 75 |
| CVX | 17 | $147.16 | $155.28 | $2,639.84 | 85 |
| DIS | 17 | $122.96 | $120.45 | $2,047.65 | 65 |
| GOOGL | 13 | $179.61 | $180.78 | $2,350.09 | 75 |
| GS | 3 | $717.52 | $703.62 | $2,110.86 | 70 |
| HD | 6 | $372.64 | $369.09 | $2,214.54 | 70 |
| INTC | 87 | $22.36 | $23.50 | $2,044.50 | 65 |
| JNJ | 13 | $155.89 | $156.66 | $2,036.58 | 65 |
| JPM | 9 | $291.61 | $287.06 | $2,583.54 | 75 |
| KO | 29 | $71.02 | $69.91 | $2,027.39 | 65 |
| LLY | 3 | $781.32 | $785.23 | $2,355.68 | 70 |
| MA | 4 | $563.08 | $550.27 | $2,201.08 | 65 |
| META | 3 | $717.12 | $719.43 | $2,158.29 | 75 |
| MRK | 25 | $82.29 | $83.05 | $2,076.25 | 65 |
| MSFT | 5 | $498.84 | $504.20 | $2,521.00 | 85 |
| NFLX | 1 | $1,279.00 | $1,241.73 | $1,241.73 | 60 |
| NKE | 32 | $75.67 | $72.66 | $2,325.12 | 75 |
| NVDA | 16 | $157.38 | $165.58 | $2,649.25 | 85 |
| ORCL | 9 | $233.26 | $231.11 | $2,079.99 | 65 |
| PEP | 15 | $136.57 | $134.43 | $2,016.45 | 65 |
| PFE | 85 | $25.20 | $25.65 | $2,180.25 | 70 |
| PG | 13 | $160.78 | $156.66 | $2,036.52 | 65 |
| PYPL | 31 | $76.58 | $74.59 | $2,312.45 | 75 |
| QCOM | 13 | $162.18 | $158.32 | $2,058.16 | 65 |
| T | 76 | $27.11 | $26.95 | $2,047.82 | 65 |
| TGT | 20 | $104.91 | $104.23 | $2,084.60 | 65 |
| TSLA | 6 | $288.62 | $310.59 | $1,863.54 | 65 |
| UNH | 7 | $298.51 | $301.30 | $2,109.07 | 75 |
| UNP | 10 | $236.18 | $234.46 | $2,344.55 | 75 |
| V | 6 | $355.85 | $347.33 | $2,084.01 | 65 |
| VZ | 49 | $43.12 | $41.65 | $2,040.61 | 65 |
| WFC | 29 | $82.28 | $82.44 | $2,390.90 | 75 |
| WMT | 22 | $97.25 | $94.51 | $2,079.22 | 65 |
| XOM | 21 | $109.97 | $115.43 | $2,424.03 | 75 |

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

<!--TRADE_LOG_END--> 
