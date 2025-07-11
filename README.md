# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 13:46:08**

| Metric | Value |
|---|---|
| **Total Value** | **$100,543.10** |
| Cash | $1,491.13 |
| Holdings Value | $99,051.97 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.01 | $2,100.10 | 65 |
| ADBE | 5 | $377.60 | $368.61 | $1,843.05 | 65 |
| AMD | 16 | $135.79 | $142.40 | $2,278.46 | 70 |
| AMZN | 11 | $221.97 | $223.00 | $2,452.96 | 75 |
| AVGO | 8 | $275.34 | $272.74 | $2,181.92 | 70 |
| AXP | 7 | $325.34 | $322.53 | $2,257.71 | 75 |
| BA | 9 | $210.85 | $226.70 | $2,040.30 | 65 |
| BAC | 45 | $48.80 | $46.38 | $2,087.32 | 65 |
| C | 23 | $86.73 | $85.83 | $1,974.09 | 65 |
| CAT | 6 | $397.86 | $402.60 | $2,415.60 | 70 |
| COST | 2 | $979.83 | $971.86 | $1,943.72 | 65 |
| CRM | 7 | $268.68 | $261.30 | $1,829.10 | 65 |
| CSCO | 32 | $68.35 | $68.10 | $2,179.20 | 70 |
| CVX | 17 | $147.15 | $154.16 | $2,620.72 | 85 |
| DIS | 18 | $122.81 | $119.91 | $2,158.29 | 70 |
| GOOGL | 13 | $179.61 | $176.99 | $2,300.87 | 75 |
| GS | 3 | $717.52 | $701.60 | $2,104.80 | 75 |
| HD | 6 | $372.64 | $368.15 | $2,208.90 | 70 |
| INTC | 88 | $22.36 | $23.19 | $2,040.72 | 65 |
| JNJ | 13 | $155.89 | $156.27 | $2,031.51 | 65 |
| JPM | 9 | $291.61 | $284.15 | $2,557.35 | 75 |
| KO | 29 | $71.03 | $69.53 | $2,016.37 | 65 |
| LLY | 3 | $781.32 | $783.91 | $2,351.73 | 70 |
| MA | 4 | $563.08 | $558.76 | $2,235.04 | 65 |
| META | 3 | $717.12 | $710.92 | $2,132.75 | 75 |
| MRK | 25 | $82.30 | $83.38 | $2,084.57 | 65 |
| MSFT | 5 | $498.84 | $498.77 | $2,493.85 | 85 |
| NFLX | 1 | $1,279.00 | $1,239.31 | $1,239.31 | 65 |
| NKE | 31 | $75.75 | $73.17 | $2,268.12 | 70 |
| NVDA | 16 | $157.38 | $165.45 | $2,647.20 | 85 |
| ORCL | 9 | $233.31 | $230.84 | $2,077.58 | 65 |
| PEP | 15 | $136.57 | $134.59 | $2,018.78 | 65 |
| PFE | 81 | $25.17 | $25.62 | $2,075.62 | 65 |
| PG | 13 | $160.78 | $157.15 | $2,042.95 | 65 |
| PYPL | 30 | $76.67 | $74.44 | $2,233.20 | 70 |
| QCOM | 14 | $161.90 | $158.26 | $2,215.71 | 70 |
| T | 70 | $28.60 | $27.14 | $1,899.80 | 60 |
| TGT | 20 | $104.92 | $103.92 | $2,078.40 | 65 |
| TSLA | 6 | $288.62 | $307.04 | $1,842.21 | 65 |
| UNH | 7 | $298.51 | $299.95 | $2,099.65 | 65 |
| UNP | 10 | $236.18 | $235.64 | $2,356.40 | 75 |
| V | 6 | $355.85 | $351.84 | $2,111.04 | 65 |
| VZ | 49 | $43.12 | $41.82 | $2,049.10 | 65 |
| WFC | 29 | $82.28 | $81.63 | $2,367.20 | 75 |
| WMT | 22 | $97.25 | $95.13 | $2,092.86 | 65 |
| XOM | 21 | $109.91 | $115.04 | $2,415.84 | 75 |

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
| 2025-07-11 13:45:51 | SELL | AAPL | 1 | $209.92 | $-1.24 | 65 |
| 2025-07-11 13:45:51 | SELL | BAC | 4 | $46.38 | $-8.89 | 65 |
| 2025-07-11 13:45:51 | SELL | AMD | 2 | $142.25 | $11.49 | 70 |
| 2025-07-11 13:45:51 | SELL | PFE | 9 | $25.62 | $3.67 | 65 |
| 2025-07-11 13:45:51 | SELL | MRK | 3 | $83.43 | $3.01 | 65 |
| 2025-07-11 13:45:51 | SELL | T | 3 | $27.14 | $-4.20 | 60 |
| 2025-07-11 13:45:51 | BUY | INTC | 4 | $23.20 | N/A | 65 |
| 2025-07-11 13:45:51 | BUY | DIS | 1 | $121.56 | N/A | 70 |
| 2025-07-11 13:45:51 | BUY | WFC | 1 | $81.62 | N/A | 75 |
| 2025-07-11 13:45:51 | BUY | UNP | 1 | $236.01 | N/A | 75 |
| 2025-07-11 13:45:51 | BUY | VZ | 1 | $41.83 | N/A | 65 |
| 2025-07-11 13:28:35 | SELL | CSCO | 1 | $68.76 | $0.40 | 70 |
| 2025-07-11 13:28:35 | BUY | BAC | 2 | $46.97 | N/A | 75 |
| 2025-07-11 13:03:05 | SELL | BAC | 2 | $46.97 | $-3.27 | 70 |
| 2025-07-11 12:31:16 | SELL | WFC | 1 | $82.36 | $0.06 | 75 |
| 2025-07-11 12:31:16 | SELL | C | 1 | $87.08 | $0.34 | 65 |
| 2025-07-11 12:31:16 | SELL | BA | 1 | $226.09 | $13.72 | 65 |
| 2025-07-11 12:31:16 | BUY | LLY | 1 | $790.65 | N/A | 85 |
| 2025-07-11 12:13:20 | BUY | INTC | 5 | $23.82 | N/A | 65 |
| 2025-07-11 11:50:13 | SELL | INTC | 6 | $23.82 | $8.91 | 60 |
| 2025-07-11 11:50:13 | BUY | BAC | 2 | $46.97 | N/A | 75 |
| 2025-07-11 11:50:13 | BUY | NKE | 1 | $74.62 | N/A | 75 |
| 2025-07-11 11:36:46 | SELL | NKE | 1 | $74.62 | $-1.13 | 70 |
| 2025-07-11 11:25:21 | SELL | DIS | 1 | $121.56 | $-1.25 | 65 |
| 2025-07-11 11:25:21 | SELL | WFC | 1 | $82.36 | $0.06 | 75 |

<!--TRADE_LOG_END--> 
