# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 14:26:57**

| Metric | Value |
|---|---|
| **Total Value** | **$100,880.56** |
| Cash | $1,317.27 |
| Holdings Value | $99,563.29 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.09 | $2,100.90 | 65 |
| ADBE | 6 | $375.23 | $365.99 | $2,195.91 | 65 |
| AMD | 15 | $145.66 | $156.38 | $2,345.70 | 70 |
| AMZN | 11 | $222.02 | $226.69 | $2,493.59 | 85 |
| AVGO | 8 | $275.34 | $282.81 | $2,262.48 | 65 |
| AXP | 7 | $325.34 | $314.68 | $2,202.76 | 70 |
| BA | 11 | $214.37 | $230.58 | $2,536.38 | 85 |
| BAC | 44 | $48.83 | $46.72 | $2,055.68 | 65 |
| C | 30 | $86.79 | $89.22 | $2,676.60 | 85 |
| CAT | 6 | $397.74 | $407.54 | $2,445.24 | 85 |
| COST | 2 | $979.83 | $968.99 | $1,937.98 | 65 |
| CRM | 7 | $268.68 | $259.04 | $1,813.25 | 65 |
| CSCO | 31 | $68.46 | $67.42 | $2,089.87 | 65 |
| CVX | 17 | $147.06 | $151.16 | $2,569.72 | 80 |
| DIS | 17 | $122.96 | $119.40 | $2,029.76 | 65 |
| GOOGL | 14 | $179.74 | $182.49 | $2,554.85 | 85 |
| GS | 3 | $717.52 | $710.58 | $2,131.74 | 85 |
| HD | 6 | $372.64 | $365.02 | $2,190.12 | 65 |
| INTC | 81 | $22.30 | $23.48 | $1,902.28 | 60 |
| JNJ | 13 | $155.95 | $155.51 | $2,021.63 | 65 |
| JPM | 9 | $291.63 | $288.49 | $2,596.38 | 85 |
| KO | 29 | $71.03 | $69.31 | $2,010.13 | 65 |
| LLY | 3 | $781.32 | $787.71 | $2,363.12 | 70 |
| MA | 4 | $563.08 | $549.99 | $2,199.96 | 65 |
| META | 3 | $717.12 | $716.40 | $2,149.20 | 65 |
| MRK | 25 | $82.54 | $82.52 | $2,062.92 | 65 |
| MSFT | 5 | $498.84 | $505.37 | $2,526.85 | 75 |
| NFLX | 1 | $1,279.00 | $1,264.16 | $1,264.16 | 65 |
| NKE | 30 | $72.05 | $72.41 | $2,172.26 | 70 |
| NVDA | 13 | $155.52 | $171.41 | $2,228.26 | 70 |
| ORCL | 9 | $233.27 | $232.45 | $2,092.05 | 65 |
| PEP | 15 | $136.57 | $134.30 | $2,014.50 | 65 |
| PFE | 83 | $25.22 | $25.02 | $2,076.24 | 65 |
| PG | 14 | $160.31 | $152.52 | $2,135.28 | 65 |
| PYPL | 32 | $72.31 | $73.52 | $2,352.64 | 75 |
| QCOM | 14 | $153.83 | $155.19 | $2,172.66 | 65 |
| T | 76 | $27.10 | $26.84 | $2,039.46 | 65 |
| TGT | 20 | $104.94 | $103.76 | $2,075.20 | 65 |
| TSLA | 6 | $318.51 | $317.38 | $1,904.28 | 65 |
| UNH | 7 | $298.51 | $294.77 | $2,063.39 | 65 |
| UNP | 9 | $236.56 | $231.99 | $2,087.91 | 65 |
| V | 6 | $355.85 | $347.96 | $2,087.76 | 65 |
| VZ | 49 | $43.12 | $41.10 | $2,013.90 | 65 |
| WFC | 26 | $83.07 | $79.28 | $2,061.22 | 65 |
| WMT | 21 | $97.38 | $94.97 | $1,994.47 | 65 |
| XOM | 20 | $109.83 | $113.13 | $2,262.63 | 75 |

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
| 2025-07-15 14:26:51 | SELL | NVDA | 2 | $171.32 | $27.40 | 70 |
| 2025-07-15 14:26:51 | SELL | PFE | 3 | $25.00 | $-0.62 | 65 |
| 2025-07-15 14:26:51 | SELL | MRK | 4 | $82.50 | $-0.13 | 65 |
| 2025-07-15 14:26:51 | BUY | AMZN | 1 | $226.68 | N/A | 85 |
| 2025-07-15 14:26:51 | BUY | PYPL | 4 | $73.54 | N/A | 75 |
| 2025-07-15 14:26:51 | BUY | BA | 1 | $230.60 | N/A | 85 |
| 2025-07-15 14:26:51 | BUY | T | 1 | $26.88 | N/A | 65 |
| 2025-07-15 14:09:14 | SELL | BAC | 3 | $46.58 | $-6.33 | 65 |
| 2025-07-15 14:09:14 | SELL | AMD | 1 | $154.88 | $8.64 | 70 |
| 2025-07-15 14:09:14 | SELL | INTC | 6 | $23.41 | $6.18 | 60 |
| 2025-07-15 14:09:14 | SELL | WFC | 6 | $79.52 | $-17.28 | 65 |
| 2025-07-15 14:09:14 | SELL | CSCO | 1 | $67.51 | $-0.92 | 65 |
| 2025-07-15 14:09:14 | BUY | NVDA | 2 | $170.47 | N/A | 85 |
| 2025-07-15 14:09:14 | BUY | CVX | 1 | $151.40 | N/A | 85 |
| 2025-07-15 13:49:01 | SELL | AMZN | 1 | $226.07 | $4.10 | 70 |
| 2025-07-15 13:49:01 | SELL | XOM | 1 | $113.65 | $3.64 | 70 |
| 2025-07-15 13:49:01 | SELL | PYPL | 3 | $73.38 | $3.39 | 65 |
| 2025-07-15 13:49:01 | SELL | NVDA | 1 | $170.90 | $14.16 | 70 |
| 2025-07-15 13:49:01 | SELL | MRK | 2 | $83.67 | $2.12 | 75 |
| 2025-07-15 13:49:01 | SELL | BA | 1 | $229.75 | $15.46 | 70 |
| 2025-07-15 13:49:01 | SELL | CVX | 1 | $151.68 | $4.60 | 75 |
| 2025-07-15 13:49:01 | BUY | TSLA | 6 | $318.51 | N/A | 65 |
| 2025-07-15 13:49:01 | BUY | AMD | 16 | $146.24 | N/A | 75 |
| 2025-07-15 13:49:01 | BUY | BAC | 1 | $46.42 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | NKE | 2 | $72.33 | N/A | 70 |

<!--TRADE_LOG_END--> 
