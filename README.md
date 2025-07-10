# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 21:08:23**

| Metric | Value |
|---|---|
| **Total Value** | **$101,396.34** |
| Cash | $1,550.03 |
| Holdings Value | $99,846.31 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.16 | $212.41 | $2,336.51 | 75 |
| ADBE | 5 | $377.60 | $371.43 | $1,857.15 | 65 |
| AMD | 15 | $134.98 | $144.16 | $2,162.40 | 70 |
| AMZN | 11 | $221.97 | $222.26 | $2,444.86 | 75 |
| AVGO | 8 | $275.34 | $275.40 | $2,203.20 | 70 |
| AXP | 8 | $325.33 | $325.24 | $2,601.92 | 75 |
| BA | 10 | $212.37 | $226.09 | $2,260.90 | 75 |
| BAC | 50 | $48.57 | $46.97 | $2,348.50 | 75 |
| C | 30 | $86.81 | $87.08 | $2,612.40 | 85 |
| CAT | 6 | $397.86 | $408.33 | $2,449.98 | 85 |
| COST | 2 | $979.83 | $970.17 | $1,940.34 | 65 |
| CRM | 7 | $268.68 | $263.97 | $1,847.79 | 65 |
| CSCO | 34 | $68.37 | $68.76 | $2,337.84 | 75 |
| CVX | 16 | $146.71 | $154.17 | $2,466.72 | 75 |
| DIS | 18 | $122.81 | $121.56 | $2,188.08 | 70 |
| GOOGL | 13 | $179.61 | $177.62 | $2,309.06 | 75 |
| GS | 3 | $717.52 | $709.12 | $2,127.36 | 75 |
| HD | 6 | $372.64 | $373.30 | $2,239.80 | 65 |
| INTC | 85 | $22.34 | $23.82 | $2,024.70 | 65 |
| JNJ | 13 | $155.89 | $157.69 | $2,049.97 | 65 |
| JPM | 9 | $291.61 | $288.19 | $2,593.71 | 75 |
| KO | 29 | $71.03 | $69.77 | $2,023.33 | 65 |
| LLY | 2 | $776.66 | $790.65 | $1,581.30 | 65 |
| MA | 4 | $563.08 | $563.52 | $2,254.08 | 65 |
| META | 3 | $717.12 | $727.24 | $2,181.72 | 85 |
| MRK | 28 | $82.42 | $84.02 | $2,352.56 | 75 |
| MSFT | 5 | $498.84 | $501.48 | $2,507.40 | 85 |
| NFLX | 1 | $1,279.00 | $1,250.59 | $1,250.59 | 65 |
| NKE | 29 | $75.83 | $74.62 | $2,163.98 | 70 |
| NVDA | 14 | $156.42 | $164.10 | $2,297.40 | 70 |
| ORCL | 9 | $233.31 | $235.00 | $2,115.00 | 65 |
| PEP | 15 | $136.57 | $136.08 | $2,041.20 | 65 |
| PFE | 84 | $25.18 | $25.78 | $2,165.52 | 70 |
| PG | 13 | $160.78 | $158.49 | $2,060.37 | 65 |
| PYPL | 31 | $76.64 | $75.70 | $2,346.70 | 75 |
| QCOM | 14 | $161.90 | $159.09 | $2,227.26 | 75 |
| T | 74 | $28.53 | $27.62 | $2,043.88 | 65 |
| TGT | 20 | $104.92 | $104.74 | $2,094.80 | 65 |
| TSLA | 6 | $288.62 | $309.87 | $1,859.22 | 65 |
| UNH | 6 | $298.34 | $299.51 | $1,797.06 | 65 |
| UNP | 9 | $236.20 | $237.00 | $2,133.00 | 70 |
| V | 6 | $355.85 | $355.88 | $2,135.28 | 65 |
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
| 2025-07-10 21:08:16 | SELL | T | 5 | $27.62 | $-4.27 | 65 |
| 2025-07-10 21:08:16 | SELL | CVX | 1 | $154.17 | $7.02 | 75 |
| 2025-07-10 21:08:16 | BUY | PFE | 5 | $25.78 | N/A | 70 |
| 2025-07-10 20:51:49 | BUY | T | 5 | $27.62 | N/A | 70 |
| 2025-07-10 20:39:46 | SELL | PFE | 1 | $25.78 | $0.63 | 65 |
| 2025-07-10 20:39:46 | BUY | NKE | 1 | $74.62 | N/A | 70 |
| 2025-07-10 20:26:26 | SELL | NKE | 1 | $74.62 | $-1.21 | 65 |
| 2025-07-10 20:26:26 | SELL | PFE | 4 | $25.78 | $2.41 | 65 |
| 2025-07-10 20:26:26 | SELL | T | 4 | $27.62 | $-3.46 | 65 |
| 2025-07-10 20:26:26 | BUY | AAPL | 1 | $212.41 | N/A | 75 |
| 2025-07-10 20:26:26 | BUY | DIS | 1 | $121.56 | N/A | 70 |
| 2025-07-10 20:26:26 | BUY | CSCO | 1 | $68.76 | N/A | 75 |
| 2025-07-10 20:09:09 | SELL | MRK | 3 | $84.06 | $4.43 | 75 |
| 2025-07-10 20:09:09 | BUY | PFE | 4 | $25.78 | N/A | 70 |
| 2025-07-10 20:09:09 | BUY | CSCO | 1 | $68.76 | N/A | 75 |
| 2025-07-10 20:09:09 | BUY | T | 5 | $27.60 | N/A | 70 |
| 2025-07-10 19:50:20 | SELL | AMD | 1 | $144.13 | $8.58 | 65 |
| 2025-07-10 19:50:20 | SELL | DIS | 1 | $121.41 | $-1.39 | 65 |
| 2025-07-10 19:50:20 | BUY | BAC | 3 | $46.88 | N/A | 75 |
| 2025-07-10 19:50:20 | BUY | AXP | 1 | $325.68 | N/A | 85 |
| 2025-07-10 19:50:20 | BUY | MRK | 3 | $83.71 | N/A | 85 |
| 2025-07-10 19:36:09 | SELL | NVDA | 2 | $164.12 | $13.47 | 70 |
| 2025-07-10 19:36:09 | SELL | PFE | 4 | $25.76 | $2.34 | 65 |
| 2025-07-10 19:36:09 | SELL | QCOM | 1 | $159.17 | $-2.55 | 70 |
| 2025-07-10 19:36:09 | SELL | CSCO | 2 | $68.87 | $0.98 | 70 |

<!--TRADE_LOG_END--> 
