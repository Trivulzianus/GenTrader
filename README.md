# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 18:44:56**

| Metric | Value |
|---|---|
| **Total Value** | **$100,851.11** |
| Cash | $1,455.49 |
| Holdings Value | $99,395.62 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.39 | $2,113.90 | 70 |
| ADBE | 5 | $377.60 | $364.21 | $1,821.05 | 65 |
| AMD | 17 | $136.09 | $146.94 | $2,497.98 | 75 |
| AMZN | 11 | $221.97 | $226.03 | $2,486.33 | 75 |
| AVGO | 8 | $275.34 | $274.85 | $2,198.78 | 70 |
| AXP | 7 | $325.34 | $320.56 | $2,243.95 | 75 |
| BA | 11 | $213.84 | $227.15 | $2,498.65 | 75 |
| BAC | 47 | $48.70 | $46.72 | $2,195.84 | 70 |
| C | 26 | $86.66 | $86.81 | $2,256.93 | 70 |
| CAT | 5 | $396.39 | $406.42 | $2,032.10 | 70 |
| COST | 2 | $979.83 | $967.84 | $1,935.68 | 65 |
| CRM | 7 | $268.68 | $258.74 | $1,811.18 | 65 |
| CSCO | 34 | $68.38 | $68.04 | $2,313.36 | 75 |
| CVX | 16 | $146.63 | $155.70 | $2,491.20 | 75 |
| DIS | 17 | $122.96 | $120.40 | $2,046.80 | 65 |
| GOOGL | 13 | $179.61 | $180.82 | $2,350.66 | 75 |
| GS | 3 | $717.52 | $704.08 | $2,112.25 | 65 |
| HD | 6 | $372.64 | $370.15 | $2,220.90 | 65 |
| INTC | 87 | $22.36 | $23.64 | $2,056.25 | 65 |
| JNJ | 13 | $155.89 | $156.97 | $2,040.61 | 65 |
| JPM | 8 | $292.23 | $286.82 | $2,294.58 | 75 |
| KO | 29 | $71.03 | $70.01 | $2,030.29 | 65 |
| LLY | 3 | $781.32 | $784.94 | $2,354.82 | 65 |
| MA | 4 | $563.08 | $548.85 | $2,195.41 | 65 |
| META | 3 | $717.12 | $719.37 | $2,158.11 | 75 |
| MRK | 25 | $82.29 | $83.23 | $2,080.88 | 65 |
| MSFT | 5 | $498.84 | $504.10 | $2,520.48 | 85 |
| NFLX | 1 | $1,279.00 | $1,243.33 | $1,243.33 | 65 |
| NKE | 31 | $75.77 | $72.78 | $2,256.18 | 70 |
| NVDA | 16 | $157.38 | $165.78 | $2,652.56 | 85 |
| ORCL | 9 | $233.26 | $230.98 | $2,078.82 | 65 |
| PEP | 15 | $136.57 | $134.79 | $2,021.92 | 65 |
| PFE | 80 | $25.17 | $25.65 | $2,052.00 | 65 |
| PG | 13 | $160.78 | $156.81 | $2,038.52 | 65 |
| PYPL | 28 | $72.13 | $72.87 | $2,040.36 | 65 |
| QCOM | 13 | $162.18 | $158.42 | $2,059.41 | 65 |
| T | 76 | $27.11 | $27.02 | $2,053.14 | 65 |
| TGT | 21 | $104.90 | $104.64 | $2,197.34 | 70 |
| TSLA | 6 | $288.62 | $312.18 | $1,873.05 | 65 |
| UNH | 7 | $298.51 | $301.18 | $2,108.24 | 65 |
| UNP | 10 | $236.18 | $234.57 | $2,345.70 | 75 |
| V | 6 | $355.85 | $345.98 | $2,075.85 | 70 |
| VZ | 49 | $43.12 | $41.68 | $2,042.32 | 65 |
| WFC | 29 | $82.28 | $82.50 | $2,392.64 | 75 |
| WMT | 22 | $97.25 | $94.42 | $2,077.24 | 65 |
| XOM | 21 | $109.97 | $115.62 | $2,428.02 | 75 |

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

<!--TRADE_LOG_END--> 
