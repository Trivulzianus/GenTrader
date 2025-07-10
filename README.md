# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 18:44:48**

| Metric | Value |
|---|---|
| **Total Value** | **$101,512.57** |
| Cash | $1,843.59 |
| Holdings Value | $99,668.98 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.77 | $2,127.70 | 70 |
| ADBE | 5 | $377.60 | $371.85 | $1,859.25 | 65 |
| AMD | 16 | $135.55 | $143.94 | $2,302.96 | 70 |
| AMZN | 11 | $221.97 | $222.45 | $2,446.95 | 75 |
| AVGO | 8 | $275.34 | $275.13 | $2,201.04 | 75 |
| AXP | 7 | $325.28 | $325.30 | $2,277.10 | 75 |
| BA | 10 | $212.37 | $225.42 | $2,254.20 | 70 |
| BAC | 49 | $48.60 | $46.95 | $2,300.55 | 75 |
| C | 29 | $86.81 | $86.80 | $2,517.20 | 80 |
| CAT | 6 | $397.86 | $409.42 | $2,456.52 | 75 |
| COST | 2 | $979.83 | $977.38 | $1,954.75 | 65 |
| CRM | 7 | $268.68 | $266.06 | $1,862.38 | 65 |
| CSCO | 30 | $68.33 | $68.75 | $2,062.65 | 65 |
| CVX | 17 | $147.15 | $154.10 | $2,619.66 | 80 |
| DIS | 18 | $122.80 | $121.21 | $2,181.78 | 70 |
| GOOGL | 13 | $179.61 | $177.19 | $2,303.47 | 70 |
| GS | 3 | $717.52 | $709.28 | $2,127.84 | 75 |
| HD | 6 | $372.64 | $376.42 | $2,258.52 | 65 |
| INTC | 84 | $22.27 | $23.95 | $2,012.22 | 65 |
| JNJ | 13 | $155.89 | $157.41 | $2,046.33 | 65 |
| JPM | 9 | $291.61 | $288.07 | $2,592.63 | 85 |
| KO | 29 | $71.03 | $69.57 | $2,017.53 | 65 |
| LLY | 2 | $776.66 | $789.89 | $1,579.79 | 65 |
| MA | 4 | $563.08 | $563.98 | $2,255.90 | 65 |
| META | 3 | $717.12 | $724.14 | $2,172.42 | 85 |
| MRK | 28 | $82.46 | $84.44 | $2,364.32 | 75 |
| MSFT | 5 | $498.84 | $501.28 | $2,506.40 | 85 |
| NFLX | 1 | $1,279.00 | $1,250.89 | $1,250.89 | 65 |
| NKE | 29 | $75.82 | $74.89 | $2,171.81 | 70 |
| NVDA | 14 | $156.60 | $163.78 | $2,292.85 | 70 |
| ORCL | 9 | $233.31 | $237.13 | $2,134.17 | 70 |
| PEP | 15 | $136.57 | $136.00 | $2,040.00 | 65 |
| PFE | 84 | $25.17 | $25.84 | $2,170.98 | 70 |
| PG | 13 | $160.78 | $158.85 | $2,065.05 | 65 |
| PYPL | 30 | $76.66 | $75.84 | $2,275.20 | 75 |
| QCOM | 16 | $161.58 | $159.68 | $2,554.88 | 85 |
| T | 73 | $28.55 | $27.64 | $2,018.09 | 65 |
| TGT | 20 | $104.92 | $105.86 | $2,117.20 | 70 |
| TSLA | 6 | $288.62 | $307.18 | $1,843.08 | 60 |
| UNH | 6 | $298.34 | $302.07 | $1,812.42 | 65 |
| UNP | 9 | $236.20 | $238.22 | $2,144.03 | 75 |
| V | 6 | $355.85 | $356.58 | $2,139.48 | 65 |
| VZ | 48 | $43.15 | $42.02 | $2,016.80 | 65 |
| WFC | 31 | $82.31 | $82.34 | $2,552.70 | 80 |
| WMT | 21 | $97.36 | $95.18 | $1,998.69 | 65 |
| XOM | 21 | $109.91 | $114.69 | $2,408.59 | 75 |

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
| 2025-07-10 18:44:41 | SELL | NVDA | 2 | $163.76 | $12.54 | 70 |
| 2025-07-10 18:44:41 | SELL | AMD | 2 | $143.91 | $14.87 | 70 |
| 2025-07-10 18:44:41 | SELL | C | 1 | $86.80 | $-0.01 | 80 |
| 2025-07-10 18:44:41 | SELL | CSCO | 2 | $68.75 | $0.78 | 65 |
| 2025-07-10 18:44:41 | BUY | INTC | 6 | $23.95 | N/A | 65 |
| 2025-07-10 18:44:41 | BUY | PFE | 6 | $25.85 | N/A | 70 |
| 2025-07-10 18:44:41 | BUY | NKE | 2 | $74.89 | N/A | 70 |
| 2025-07-10 18:44:41 | BUY | QCOM | 1 | $159.70 | N/A | 85 |
| 2025-07-10 18:27:27 | SELL | NKE | 2 | $75.06 | $-1.55 | 65 |
| 2025-07-10 18:27:27 | SELL | INTC | 6 | $23.91 | $9.83 | 60 |
| 2025-07-10 18:27:27 | SELL | PFE | 12 | $25.90 | $8.03 | 65 |
| 2025-07-10 18:27:27 | SELL | CSCO | 1 | $68.85 | $0.47 | 70 |
| 2025-07-10 18:27:27 | SELL | QCOM | 1 | $159.75 | $-1.83 | 75 |
| 2025-07-10 18:27:27 | BUY | NVDA | 2 | $163.74 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | PG | 1 | $159.16 | N/A | 70 |
| 2025-07-10 18:27:27 | BUY | WFC | 3 | $82.21 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | CVX | 1 | $153.99 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | TGT | 1 | $106.22 | N/A | 70 |
| 2025-07-10 18:11:08 | SELL | NVDA | 2 | $164.14 | $13.19 | 70 |
| 2025-07-10 18:11:08 | SELL | CRM | 1 | $265.90 | $-2.43 | 60 |
| 2025-07-10 18:11:08 | SELL | CVX | 1 | $154.09 | $6.93 | 80 |
| 2025-07-10 18:11:08 | BUY | AMD | 2 | $144.40 | N/A | 85 |
| 2025-07-10 18:11:08 | BUY | PFE | 7 | $25.56 | N/A | 75 |
| 2025-07-10 18:11:08 | BUY | BA | 1 | $224.96 | N/A | 75 |
| 2025-07-10 18:11:08 | BUY | QCOM | 1 | $159.74 | N/A | 85 |

<!--TRADE_LOG_END--> 
