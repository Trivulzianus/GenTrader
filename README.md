# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 19:50:26**

| Metric | Value |
|---|---|
| **Total Value** | **$101,421.01** |
| Cash | $1,745.84 |
| Holdings Value | $99,675.17 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.35 | $2,123.50 | 70 |
| ADBE | 5 | $377.60 | $371.00 | $1,855.03 | 65 |
| AMD | 15 | $134.98 | $144.13 | $2,161.94 | 65 |
| AMZN | 11 | $221.97 | $222.11 | $2,443.21 | 75 |
| AVGO | 8 | $275.34 | $275.09 | $2,200.72 | 70 |
| AXP | 8 | $325.33 | $325.63 | $2,605.04 | 85 |
| BA | 10 | $212.37 | $226.20 | $2,262.00 | 65 |
| BAC | 50 | $48.57 | $46.86 | $2,343.01 | 75 |
| C | 30 | $86.81 | $86.99 | $2,609.70 | 85 |
| CAT | 6 | $397.86 | $408.26 | $2,449.56 | 75 |
| COST | 2 | $979.83 | $973.50 | $1,947.00 | 65 |
| CRM | 7 | $268.68 | $263.72 | $1,846.04 | 65 |
| CSCO | 32 | $68.35 | $68.86 | $2,203.36 | 70 |
| CVX | 17 | $147.15 | $154.20 | $2,621.40 | 85 |
| DIS | 17 | $122.88 | $121.42 | $2,064.14 | 65 |
| GOOGL | 13 | $179.61 | $177.66 | $2,309.51 | 75 |
| GS | 3 | $717.52 | $709.03 | $2,127.09 | 75 |
| HD | 6 | $372.64 | $374.12 | $2,244.72 | 70 |
| INTC | 85 | $22.34 | $23.84 | $2,026.82 | 65 |
| JNJ | 13 | $155.89 | $157.59 | $2,048.61 | 65 |
| JPM | 9 | $291.61 | $288.00 | $2,592.00 | 85 |
| KO | 29 | $71.03 | $69.81 | $2,024.63 | 65 |
| LLY | 2 | $776.66 | $791.60 | $1,583.20 | 65 |
| MA | 4 | $563.08 | $564.66 | $2,258.66 | 65 |
| META | 3 | $717.12 | $727.10 | $2,181.30 | 80 |
| MRK | 31 | $82.58 | $84.11 | $2,607.41 | 85 |
| MSFT | 5 | $498.84 | $501.35 | $2,506.75 | 70 |
| NFLX | 1 | $1,279.00 | $1,251.58 | $1,251.58 | 65 |
| NKE | 29 | $75.83 | $74.59 | $2,163.11 | 70 |
| NVDA | 14 | $156.42 | $164.00 | $2,296.00 | 70 |
| ORCL | 9 | $233.31 | $235.19 | $2,116.74 | 65 |
| PEP | 15 | $136.57 | $136.17 | $2,042.55 | 65 |
| PFE | 80 | $25.15 | $25.74 | $2,059.20 | 65 |
| PG | 13 | $160.78 | $158.46 | $2,059.93 | 65 |
| PYPL | 31 | $76.64 | $75.68 | $2,346.08 | 75 |
| QCOM | 14 | $161.90 | $159.16 | $2,228.24 | 75 |
| T | 73 | $28.55 | $27.64 | $2,017.36 | 65 |
| TGT | 20 | $104.92 | $105.22 | $2,104.40 | 65 |
| TSLA | 6 | $288.62 | $309.46 | $1,856.75 | 60 |
| UNH | 6 | $298.34 | $300.34 | $1,802.04 | 65 |
| UNP | 9 | $236.20 | $237.35 | $2,136.19 | 70 |
| V | 6 | $355.85 | $356.53 | $2,139.18 | 70 |
| VZ | 48 | $43.15 | $42.03 | $2,017.68 | 65 |
| WFC | 29 | $82.30 | $82.29 | $2,386.41 | 75 |
| WMT | 21 | $97.36 | $94.89 | $1,992.69 | 65 |
| XOM | 21 | $109.91 | $114.89 | $2,412.69 | 75 |

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
| 2025-07-10 19:50:20 | SELL | AMD | 1 | $144.13 | $8.58 | 65 |
| 2025-07-10 19:50:20 | SELL | DIS | 1 | $121.41 | $-1.39 | 65 |
| 2025-07-10 19:50:20 | BUY | BAC | 3 | $46.88 | N/A | 75 |
| 2025-07-10 19:50:20 | BUY | AXP | 1 | $325.68 | N/A | 85 |
| 2025-07-10 19:50:20 | BUY | MRK | 3 | $83.71 | N/A | 85 |
| 2025-07-10 19:36:09 | SELL | NVDA | 2 | $164.12 | $13.47 | 70 |
| 2025-07-10 19:36:09 | SELL | PFE | 4 | $25.76 | $2.34 | 65 |
| 2025-07-10 19:36:09 | SELL | QCOM | 1 | $159.17 | $-2.55 | 70 |
| 2025-07-10 19:36:09 | SELL | CSCO | 2 | $68.87 | $0.98 | 70 |
| 2025-07-10 19:36:09 | BUY | PYPL | 4 | $75.79 | N/A | 75 |
| 2025-07-10 19:36:09 | BUY | C | 3 | $86.94 | N/A | 85 |
| 2025-07-10 19:24:29 | SELL | BAC | 2 | $46.88 | $-3.46 | 70 |
| 2025-07-10 19:24:29 | SELL | PYPL | 3 | $75.69 | $-2.90 | 65 |
| 2025-07-10 19:24:29 | SELL | C | 3 | $86.83 | $0.10 | 75 |
| 2025-07-10 19:24:29 | BUY | NVDA | 2 | $162.88 | N/A | 85 |
| 2025-07-10 19:24:29 | BUY | INTC | 11 | $23.84 | N/A | 65 |
| 2025-07-10 19:24:29 | BUY | CSCO | 1 | $68.81 | N/A | 75 |
| 2025-07-10 19:07:51 | SELL | INTC | 10 | $23.44 | $11.70 | 55 |
| 2025-07-10 19:07:51 | SELL | WFC | 3 | $82.28 | $-0.06 | 75 |
| 2025-07-10 19:07:51 | BUY | BAC | 2 | $46.89 | N/A | 75 |
| 2025-07-10 19:07:51 | BUY | NKE | 1 | $74.72 | N/A | 70 |
| 2025-07-10 19:07:51 | BUY | PFE | 5 | $25.83 | N/A | 70 |
| 2025-07-10 18:56:32 | SELL | BAC | 2 | $46.85 | $-3.51 | 70 |
| 2025-07-10 18:56:32 | SELL | NKE | 1 | $74.57 | $-1.25 | 65 |
| 2025-07-10 18:56:32 | SELL | PFE | 5 | $25.81 | $3.15 | 65 |

<!--TRADE_LOG_END--> 
