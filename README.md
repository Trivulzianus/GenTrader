# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 19:08:49**

| Metric | Value |
|---|---|
| **Total Value** | **$100,868.33** |
| Cash | $840.19 |
| Holdings Value | $100,028.15 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.98 | $2,089.80 | 65 |
| ADBE | 6 | $375.23 | $366.78 | $2,200.68 | 65 |
| AMD | 14 | $133.90 | $146.57 | $2,051.98 | 65 |
| AMZN | 11 | $221.93 | $225.37 | $2,479.07 | 80 |
| AVGO | 8 | $275.34 | $275.70 | $2,205.60 | 65 |
| AXP | 7 | $325.34 | $320.81 | $2,245.67 | 75 |
| BA | 10 | $212.67 | $230.16 | $2,301.60 | 70 |
| BAC | 50 | $48.60 | $47.00 | $2,349.80 | 75 |
| C | 26 | $86.50 | $87.31 | $2,270.06 | 70 |
| CAT | 6 | $397.74 | $405.24 | $2,431.41 | 70 |
| COST | 2 | $979.83 | $978.35 | $1,956.70 | 65 |
| CRM | 7 | $268.68 | $260.76 | $1,825.32 | 65 |
| CSCO | 30 | $68.50 | $67.74 | $2,032.30 | 65 |
| CVX | 17 | $147.11 | $152.42 | $2,591.14 | 85 |
| DIS | 18 | $122.79 | $120.23 | $2,164.14 | 65 |
| GOOGL | 14 | $179.69 | $181.25 | $2,537.43 | 85 |
| GS | 3 | $717.52 | $711.87 | $2,135.61 | 85 |
| HD | 6 | $372.64 | $369.42 | $2,216.52 | 70 |
| INTC | 80 | $22.30 | $23.30 | $1,864.19 | 60 |
| JNJ | 13 | $155.95 | $156.34 | $2,032.42 | 65 |
| JPM | 9 | $291.63 | $288.38 | $2,595.47 | 85 |
| KO | 29 | $71.03 | $69.42 | $2,013.04 | 65 |
| LLY | 3 | $781.32 | $795.00 | $2,385.00 | 70 |
| MA | 4 | $563.08 | $553.98 | $2,215.92 | 60 |
| META | 3 | $717.12 | $721.46 | $2,164.38 | 70 |
| MRK | 31 | $82.62 | $83.76 | $2,596.56 | 85 |
| MSFT | 5 | $498.84 | $503.03 | $2,515.14 | 75 |
| NFLX | 1 | $1,279.00 | $1,267.10 | $1,267.10 | 65 |
| NKE | 28 | $72.03 | $72.24 | $2,022.72 | 65 |
| NVDA | 16 | $157.66 | $164.66 | $2,634.64 | 85 |
| ORCL | 9 | $233.27 | $229.05 | $2,061.45 | 70 |
| PEP | 15 | $136.57 | $135.66 | $2,034.90 | 65 |
| PFE | 86 | $25.21 | $25.43 | $2,187.41 | 70 |
| PG | 13 | $160.78 | $154.29 | $2,005.77 | 65 |
| PYPL | 28 | $72.08 | $73.78 | $2,065.98 | 65 |
| QCOM | 14 | $153.83 | $154.25 | $2,159.50 | 65 |
| T | 75 | $27.10 | $27.23 | $2,041.88 | 65 |
| TGT | 20 | $104.94 | $104.63 | $2,092.60 | 65 |
| TSLA | 6 | $288.62 | $316.25 | $1,897.50 | 65 |
| UNH | 7 | $298.51 | $300.23 | $2,101.61 | 65 |
| UNP | 9 | $236.57 | $233.82 | $2,104.42 | 65 |
| V | 6 | $355.85 | $351.34 | $2,108.03 | 65 |
| VZ | 49 | $43.12 | $41.72 | $2,044.04 | 65 |
| WFC | 28 | $82.26 | $83.33 | $2,333.10 | 75 |
| WMT | 21 | $97.38 | $95.50 | $2,005.50 | 65 |
| XOM | 21 | $110.01 | $113.95 | $2,393.05 | 75 |

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
| 2025-07-14 19:08:29 | SELL | AMD | 2 | $146.57 | $22.17 | 65 |
| 2025-07-14 19:08:29 | SELL | PYPL | 3 | $73.81 | $4.67 | 65 |
| 2025-07-14 19:08:29 | SELL | C | 4 | $87.32 | $2.81 | 70 |
| 2025-07-14 19:08:29 | SELL | UNP | 1 | $233.77 | $-2.52 | 65 |
| 2025-07-14 19:08:29 | BUY | AMZN | 1 | $225.41 | N/A | 80 |
| 2025-07-14 19:08:29 | BUY | BAC | 3 | $46.99 | N/A | 75 |
| 2025-07-14 19:08:29 | BUY | MRK | 3 | $83.76 | N/A | 85 |
| 2025-07-14 19:08:29 | BUY | T | 1 | $27.22 | N/A | 65 |
| 2025-07-14 19:08:29 | BUY | CVX | 1 | $152.49 | N/A | 85 |
| 2025-07-14 18:47:08 | SELL | AMZN | 1 | $225.33 | $3.41 | 70 |
| 2025-07-14 18:47:08 | SELL | INTC | 6 | $23.35 | $5.88 | 60 |
| 2025-07-14 18:47:08 | SELL | NKE | 4 | $72.25 | $0.79 | 65 |
| 2025-07-14 18:47:08 | SELL | MRK | 3 | $83.85 | $3.68 | 75 |
| 2025-07-14 18:47:08 | SELL | CSCO | 1 | $67.78 | $-0.70 | 65 |
| 2025-07-14 18:47:08 | BUY | NVDA | 1 | $164.79 | N/A | 85 |
| 2025-07-14 18:47:08 | BUY | DIS | 1 | $120.40 | N/A | 70 |
| 2025-07-14 18:47:08 | BUY | C | 3 | $87.18 | N/A | 85 |
| 2025-07-14 18:28:00 | SELL | DIS | 1 | $120.43 | $-2.37 | 65 |
| 2025-07-14 18:28:00 | SELL | PFE | 4 | $25.48 | $1.03 | 70 |
| 2025-07-14 18:28:00 | SELL | C | 3 | $87.23 | $1.84 | 75 |
| 2025-07-14 18:28:00 | SELL | CVX | 1 | $152.30 | $5.20 | 75 |
| 2025-07-14 18:28:00 | BUY | NKE | 4 | $72.24 | N/A | 75 |
| 2025-07-14 18:28:00 | BUY | PYPL | 3 | $73.49 | N/A | 75 |
| 2025-07-14 18:28:00 | BUY | MRK | 1 | $83.81 | N/A | 85 |
| 2025-07-14 18:28:00 | BUY | CSCO | 1 | $67.88 | N/A | 70 |

<!--TRADE_LOG_END--> 
