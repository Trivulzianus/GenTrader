# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 07:38:53**

| Metric | Value |
|---|---|
| **Total Value** | **$101,396.34** |
| Cash | $1,610.97 |
| Holdings Value | $99,785.37 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.16 | $212.41 | $2,336.51 | 70 |
| ADBE | 5 | $377.60 | $371.43 | $1,857.15 | 65 |
| AMD | 16 | $135.55 | $144.16 | $2,306.56 | 75 |
| AMZN | 11 | $221.97 | $222.26 | $2,444.86 | 75 |
| AVGO | 8 | $275.34 | $275.40 | $2,203.20 | 70 |
| AXP | 7 | $325.34 | $325.24 | $2,276.68 | 70 |
| BA | 10 | $212.37 | $226.09 | $2,260.90 | 70 |
| BAC | 47 | $48.67 | $46.97 | $2,207.59 | 70 |
| C | 24 | $86.74 | $87.08 | $2,089.92 | 65 |
| CAT | 6 | $397.86 | $408.33 | $2,449.98 | 70 |
| COST | 2 | $979.83 | $970.17 | $1,940.34 | 65 |
| CRM | 7 | $268.68 | $263.97 | $1,847.79 | 65 |
| CSCO | 34 | $68.37 | $68.76 | $2,337.84 | 75 |
| CVX | 17 | $147.15 | $154.17 | $2,620.89 | 80 |
| DIS | 17 | $122.88 | $121.56 | $2,066.52 | 70 |
| GOOGL | 13 | $179.61 | $177.62 | $2,309.06 | 75 |
| GS | 3 | $717.52 | $709.12 | $2,127.36 | 85 |
| HD | 6 | $372.64 | $373.30 | $2,239.80 | 65 |
| INTC | 85 | $22.34 | $23.82 | $2,024.70 | 65 |
| JNJ | 13 | $155.89 | $157.69 | $2,049.97 | 65 |
| JPM | 9 | $291.61 | $288.19 | $2,593.71 | 85 |
| KO | 29 | $71.03 | $69.77 | $2,023.33 | 65 |
| LLY | 2 | $776.66 | $790.65 | $1,581.30 | 65 |
| MA | 4 | $563.08 | $563.52 | $2,254.08 | 65 |
| META | 3 | $717.12 | $727.24 | $2,181.72 | 75 |
| MRK | 28 | $82.42 | $84.02 | $2,352.56 | 75 |
| MSFT | 5 | $498.84 | $501.48 | $2,507.40 | 85 |
| NFLX | 1 | $1,279.00 | $1,250.59 | $1,250.59 | 65 |
| NKE | 32 | $75.71 | $74.62 | $2,387.84 | 75 |
| NVDA | 16 | $157.38 | $164.10 | $2,625.60 | 85 |
| ORCL | 9 | $233.31 | $235.00 | $2,115.00 | 65 |
| PEP | 15 | $136.57 | $136.08 | $2,041.20 | 65 |
| PFE | 90 | $25.22 | $25.78 | $2,320.20 | 75 |
| PG | 13 | $160.78 | $158.49 | $2,060.37 | 65 |
| PYPL | 30 | $76.67 | $75.70 | $2,271.00 | 75 |
| QCOM | 14 | $161.90 | $159.09 | $2,227.26 | 70 |
| T | 73 | $28.54 | $27.62 | $2,016.26 | 65 |
| TGT | 20 | $104.92 | $104.74 | $2,094.80 | 65 |
| TSLA | 6 | $288.62 | $309.87 | $1,859.22 | 65 |
| UNH | 6 | $298.34 | $299.51 | $1,797.06 | 65 |
| UNP | 9 | $236.20 | $237.00 | $2,133.00 | 65 |
| V | 6 | $355.85 | $355.88 | $2,135.28 | 70 |
| VZ | 48 | $43.15 | $42.03 | $2,017.44 | 65 |
| WFC | 28 | $82.30 | $82.36 | $2,306.08 | 75 |
| WMT | 21 | $97.36 | $94.86 | $1,992.06 | 65 |
| XOM | 23 | $110.35 | $114.93 | $2,643.39 | 85 |

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
| 2025-07-11 07:38:49 | SELL | BAC | 2 | $46.97 | $-3.27 | 70 |
| 2025-07-11 07:38:49 | SELL | C | 3 | $87.08 | $0.90 | 65 |
| 2025-07-11 07:38:49 | BUY | INTC | 1 | $23.82 | N/A | 65 |
| 2025-07-11 07:38:49 | BUY | XOM | 2 | $114.93 | N/A | 85 |
| 2025-07-11 07:38:49 | BUY | CSCO | 1 | $68.76 | N/A | 75 |
| 2025-07-11 07:25:57 | SELL | C | 3 | $87.08 | $0.81 | 75 |
| 2025-07-11 07:25:57 | BUY | BA | 1 | $226.09 | N/A | 75 |
| 2025-07-11 07:09:46 | BUY | C | 3 | $87.08 | N/A | 85 |
| 2025-07-11 06:46:52 | BUY | AMD | 1 | $144.16 | N/A | 75 |
| 2025-07-11 06:46:52 | BUY | CVX | 1 | $154.17 | N/A | 85 |
| 2025-07-11 06:28:20 | SELL | CVX | 1 | $154.17 | $7.02 | 75 |
| 2025-07-11 06:28:20 | BUY | BAC | 2 | $46.97 | N/A | 75 |
| 2025-07-11 06:28:20 | BUY | INTC | 5 | $23.82 | N/A | 65 |
| 2025-07-11 06:28:20 | BUY | CSCO | 1 | $68.76 | N/A | 75 |
| 2025-07-11 06:11:59 | SELL | INTC | 6 | $23.82 | $8.91 | 60 |
| 2025-07-11 06:11:59 | SELL | C | 3 | $87.08 | $0.81 | 75 |
| 2025-07-11 05:52:40 | SELL | BAC | 2 | $46.97 | $-3.27 | 70 |
| 2025-07-11 05:52:40 | SELL | NKE | 3 | $74.62 | $-3.00 | 75 |
| 2025-07-11 05:52:40 | SELL | CSCO | 1 | $68.76 | $0.40 | 70 |
| 2025-07-11 05:52:40 | BUY | CVX | 1 | $154.17 | N/A | 85 |
| 2025-07-11 05:41:56 | SELL | CVX | 1 | $154.17 | $7.02 | 75 |
| 2025-07-11 05:41:56 | BUY | BAC | 2 | $46.97 | N/A | 75 |
| 2025-07-11 05:41:56 | BUY | PYPL | 1 | $75.70 | N/A | 75 |
| 2025-07-11 05:41:56 | BUY | NKE | 4 | $74.62 | N/A | 85 |
| 2025-07-11 05:41:56 | BUY | CSCO | 1 | $68.76 | N/A | 75 |

<!--TRADE_LOG_END--> 
