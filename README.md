# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 18:28:06**

| Metric | Value |
|---|---|
| **Total Value** | **$100,846.77** |
| Cash | $112.97 |
| Holdings Value | $100,733.80 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.07 | $2,090.75 | 65 |
| ADBE | 6 | $375.23 | $365.35 | $2,192.10 | 65 |
| AMD | 16 | $135.48 | $146.56 | $2,344.96 | 75 |
| AMZN | 11 | $221.92 | $225.46 | $2,480.01 | 75 |
| AVGO | 8 | $275.34 | $276.22 | $2,209.76 | 70 |
| AXP | 7 | $325.34 | $320.56 | $2,243.90 | 70 |
| BA | 10 | $212.67 | $229.84 | $2,298.38 | 70 |
| BAC | 47 | $48.71 | $46.95 | $2,206.65 | 70 |
| C | 27 | $86.55 | $87.23 | $2,355.21 | 75 |
| CAT | 6 | $397.74 | $405.17 | $2,431.04 | 75 |
| COST | 2 | $979.83 | $975.62 | $1,951.23 | 65 |
| CRM | 7 | $268.68 | $260.61 | $1,824.27 | 65 |
| CSCO | 31 | $68.48 | $67.89 | $2,104.45 | 70 |
| CVX | 16 | $146.78 | $152.30 | $2,436.80 | 75 |
| DIS | 17 | $122.93 | $120.43 | $2,047.31 | 65 |
| GOOGL | 14 | $179.69 | $181.88 | $2,546.25 | 85 |
| GS | 3 | $717.52 | $711.61 | $2,134.82 | 75 |
| HD | 6 | $372.64 | $368.75 | $2,212.50 | 65 |
| INTC | 86 | $22.37 | $23.34 | $2,006.81 | 65 |
| JNJ | 13 | $155.95 | $156.37 | $2,032.81 | 65 |
| JPM | 9 | $291.63 | $288.34 | $2,595.06 | 85 |
| KO | 29 | $71.03 | $69.47 | $2,014.77 | 65 |
| LLY | 3 | $781.32 | $795.36 | $2,386.07 | 85 |
| MA | 4 | $563.08 | $553.99 | $2,215.96 | 65 |
| META | 3 | $717.12 | $724.19 | $2,172.57 | 85 |
| MRK | 31 | $82.62 | $83.83 | $2,598.73 | 85 |
| MSFT | 5 | $498.84 | $502.84 | $2,514.20 | 75 |
| NFLX | 1 | $1,279.00 | $1,268.44 | $1,268.44 | 65 |
| NKE | 32 | $72.06 | $72.23 | $2,311.36 | 75 |
| NVDA | 15 | $157.18 | $164.87 | $2,473.05 | 85 |
| ORCL | 9 | $233.27 | $229.59 | $2,066.36 | 65 |
| PEP | 15 | $136.57 | $135.68 | $2,035.20 | 65 |
| PFE | 86 | $25.21 | $25.48 | $2,191.71 | 70 |
| PG | 13 | $160.78 | $154.10 | $2,003.30 | 65 |
| PYPL | 31 | $72.25 | $73.48 | $2,278.03 | 75 |
| QCOM | 14 | $153.83 | $154.54 | $2,163.56 | 65 |
| T | 74 | $27.10 | $27.16 | $2,010.21 | 65 |
| TGT | 20 | $104.94 | $104.55 | $2,091.00 | 65 |
| TSLA | 6 | $288.62 | $314.85 | $1,889.10 | 60 |
| UNH | 7 | $298.51 | $300.37 | $2,102.59 | 65 |
| UNP | 10 | $236.29 | $233.33 | $2,333.30 | 75 |
| V | 6 | $355.85 | $350.95 | $2,105.73 | 65 |
| VZ | 49 | $43.12 | $41.65 | $2,040.61 | 65 |
| WFC | 28 | $82.26 | $83.28 | $2,331.70 | 75 |
| WMT | 21 | $97.38 | $95.33 | $2,001.83 | 65 |
| XOM | 21 | $110.01 | $113.78 | $2,389.38 | 75 |

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
| 2025-07-14 18:28:00 | SELL | DIS | 1 | $120.43 | $-2.37 | 65 |
| 2025-07-14 18:28:00 | SELL | PFE | 4 | $25.48 | $1.03 | 70 |
| 2025-07-14 18:28:00 | SELL | C | 3 | $87.23 | $1.84 | 75 |
| 2025-07-14 18:28:00 | SELL | CVX | 1 | $152.30 | $5.20 | 75 |
| 2025-07-14 18:28:00 | BUY | NKE | 4 | $72.24 | N/A | 75 |
| 2025-07-14 18:28:00 | BUY | PYPL | 3 | $73.49 | N/A | 75 |
| 2025-07-14 18:28:00 | BUY | MRK | 1 | $83.81 | N/A | 85 |
| 2025-07-14 18:28:00 | BUY | CSCO | 1 | $67.88 | N/A | 70 |
| 2025-07-14 18:11:32 | SELL | MRK | 1 | $83.78 | $1.15 | 80 |
| 2025-07-14 18:11:32 | SELL | ORCL | 1 | $229.99 | $-2.94 | 65 |
| 2025-07-14 18:11:32 | SELL | CSCO | 1 | $67.86 | $-0.61 | 65 |
| 2025-07-14 18:11:32 | BUY | PFE | 6 | $25.49 | N/A | 75 |
| 2025-07-14 18:11:32 | BUY | C | 3 | $87.28 | N/A | 85 |
| 2025-07-14 18:11:32 | BUY | CVX | 1 | $152.13 | N/A | 85 |
| 2025-07-14 17:52:02 | SELL | PYPL | 3 | $73.68 | $4.26 | 65 |
| 2025-07-14 17:52:02 | BUY | NVDA | 1 | $164.99 | N/A | 85 |
| 2025-07-14 17:52:02 | BUY | PFE | 5 | $25.51 | N/A | 70 |
| 2025-07-14 17:52:02 | BUY | MRK | 3 | $83.83 | N/A | 85 |
| 2025-07-14 17:52:02 | BUY | CSCO | 1 | $67.91 | N/A | 70 |
| 2025-07-14 17:40:02 | SELL | NKE | 1 | $72.27 | $0.23 | 65 |
| 2025-07-14 17:40:02 | SELL | PFE | 7 | $25.48 | $1.89 | 65 |
| 2025-07-14 17:40:02 | SELL | C | 4 | $87.31 | $2.67 | 75 |
| 2025-07-14 17:40:02 | SELL | CSCO | 2 | $67.84 | $-1.23 | 65 |
| 2025-07-14 17:40:02 | SELL | T | 1 | $27.16 | $0.05 | 65 |
| 2025-07-14 17:40:02 | BUY | GOOGL | 1 | $181.31 | N/A | 85 |

<!--TRADE_LOG_END--> 
