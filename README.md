# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 01:13:07**

| Metric | Value |
|---|---|
| **Total Value** | **$101,396.34** |
| Cash | $2,049.47 |
| Holdings Value | $99,346.87 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.16 | $212.41 | $2,336.51 | 70 |
| ADBE | 5 | $377.60 | $371.43 | $1,857.15 | 65 |
| AMD | 15 | $134.98 | $144.16 | $2,162.40 | 70 |
| AMZN | 11 | $221.97 | $222.26 | $2,444.86 | 75 |
| AVGO | 8 | $275.34 | $275.40 | $2,203.20 | 70 |
| AXP | 8 | $325.33 | $325.24 | $2,601.92 | 75 |
| BA | 9 | $210.85 | $226.09 | $2,034.81 | 65 |
| BAC | 46 | $48.71 | $46.97 | $2,160.62 | 70 |
| C | 26 | $86.77 | $87.08 | $2,264.08 | 70 |
| CAT | 6 | $397.86 | $408.33 | $2,449.98 | 85 |
| COST | 2 | $979.83 | $970.17 | $1,940.34 | 65 |
| CRM | 7 | $268.68 | $263.97 | $1,847.79 | 65 |
| CSCO | 34 | $68.37 | $68.76 | $2,337.84 | 75 |
| CVX | 16 | $146.71 | $154.17 | $2,466.72 | 80 |
| DIS | 17 | $122.88 | $121.56 | $2,066.52 | 65 |
| GOOGL | 13 | $179.61 | $177.62 | $2,309.06 | 75 |
| GS | 3 | $717.52 | $709.12 | $2,127.36 | 85 |
| HD | 6 | $372.64 | $373.30 | $2,239.80 | 65 |
| INTC | 85 | $22.34 | $23.82 | $2,024.70 | 65 |
| JNJ | 13 | $155.89 | $157.69 | $2,049.97 | 65 |
| JPM | 8 | $292.04 | $288.19 | $2,305.52 | 70 |
| KO | 29 | $71.03 | $69.77 | $2,023.33 | 65 |
| LLY | 2 | $776.66 | $790.65 | $1,581.30 | 65 |
| MA | 4 | $563.08 | $563.52 | $2,254.08 | 65 |
| META | 3 | $717.12 | $727.24 | $2,181.72 | 85 |
| MRK | 28 | $82.42 | $84.02 | $2,352.56 | 75 |
| MSFT | 5 | $498.84 | $501.48 | $2,507.40 | 85 |
| NFLX | 1 | $1,279.00 | $1,250.59 | $1,250.59 | 65 |
| NKE | 35 | $75.62 | $74.62 | $2,611.70 | 85 |
| NVDA | 16 | $157.38 | $164.10 | $2,625.60 | 85 |
| ORCL | 9 | $233.31 | $235.00 | $2,115.00 | 65 |
| PEP | 15 | $136.57 | $136.08 | $2,041.20 | 65 |
| PFE | 84 | $25.18 | $25.78 | $2,165.52 | 70 |
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
| WFC | 29 | $82.30 | $82.36 | $2,388.44 | 75 |
| WMT | 21 | $97.36 | $94.86 | $1,992.06 | 65 |
| XOM | 21 | $109.91 | $114.93 | $2,413.53 | 75 |

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
| 2025-07-11 01:13:02 | SELL | C | 1 | $87.08 | $0.30 | 70 |
| 2025-07-11 01:13:02 | SELL | BA | 1 | $226.09 | $13.72 | 65 |
| 2025-07-11 01:13:02 | BUY | BAC | 2 | $46.97 | N/A | 70 |
| 2025-07-11 01:13:02 | BUY | PYPL | 3 | $75.70 | N/A | 75 |
| 2025-07-11 00:34:49 | SELL | BAC | 2 | $46.97 | $-3.48 | 65 |
| 2025-07-11 00:34:49 | SELL | C | 3 | $87.08 | $0.81 | 75 |
| 2025-07-11 00:34:49 | SELL | WFC | 2 | $82.36 | $0.11 | 75 |
| 2025-07-11 00:34:49 | SELL | PYPL | 3 | $75.70 | $-2.92 | 65 |
| 2025-07-11 00:34:49 | SELL | CVX | 1 | $154.17 | $7.02 | 75 |
| 2025-07-11 00:34:49 | BUY | NVDA | 2 | $164.10 | N/A | 85 |
| 2025-07-10 23:50:25 | SELL | WFC | 1 | $82.36 | $0.05 | 80 |
| 2025-07-10 23:50:25 | SELL | TGT | 1 | $104.74 | $-0.17 | 65 |
| 2025-07-10 23:50:25 | BUY | BAC | 3 | $46.97 | N/A | 70 |
| 2025-07-10 23:50:25 | BUY | INTC | 5 | $23.82 | N/A | 65 |
| 2025-07-10 23:50:25 | BUY | PYPL | 1 | $75.70 | N/A | 75 |
| 2025-07-10 23:50:25 | BUY | PFE | 4 | $25.78 | N/A | 70 |
| 2025-07-10 23:37:47 | SELL | INTC | 5 | $23.82 | $7.42 | 60 |
| 2025-07-10 23:37:47 | SELL | PFE | 5 | $25.78 | $2.98 | 65 |
| 2025-07-10 23:37:47 | BUY | NKE | 3 | $74.62 | N/A | 85 |
| 2025-07-10 23:37:47 | BUY | WFC | 3 | $82.36 | N/A | 85 |
| 2025-07-10 23:37:47 | BUY | TGT | 1 | $104.74 | N/A | 70 |
| 2025-07-10 23:25:56 | SELL | BAC | 1 | $46.97 | $-1.82 | 65 |
| 2025-07-10 23:25:56 | SELL | PYPL | 2 | $75.70 | $-1.88 | 70 |
| 2025-07-10 23:08:22 | SELL | BAC | 2 | $46.97 | $-3.48 | 65 |
| 2025-07-10 23:08:22 | SELL | NKE | 3 | $74.62 | $-3.00 | 75 |

<!--TRADE_LOG_END--> 
