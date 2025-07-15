# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 17:40:14**

| Metric | Value |
|---|---|
| **Total Value** | **$100,682.07** |
| Cash | $50.16 |
| Holdings Value | $100,631.92 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.07 | $2,110.70 | 70 |
| ADBE | 6 | $375.23 | $365.36 | $2,192.16 | 65 |
| AMD | 17 | $146.29 | $155.77 | $2,648.04 | 85 |
| AMZN | 11 | $222.06 | $226.33 | $2,489.63 | 85 |
| AVGO | 8 | $275.34 | $280.80 | $2,246.38 | 65 |
| AXP | 7 | $325.34 | $312.10 | $2,184.66 | 65 |
| BA | 10 | $212.82 | $230.12 | $2,301.25 | 70 |
| BAC | 45 | $48.79 | $46.38 | $2,086.88 | 65 |
| C | 30 | $86.78 | $90.33 | $2,709.90 | 85 |
| CAT | 6 | $397.74 | $404.20 | $2,425.23 | 70 |
| COST | 2 | $979.83 | $970.35 | $1,940.70 | 65 |
| CRM | 8 | $267.44 | $258.99 | $2,071.92 | 65 |
| CSCO | 31 | $68.46 | $67.38 | $2,088.62 | 65 |
| CVX | 17 | $147.01 | $150.51 | $2,558.67 | 85 |
| DIS | 18 | $122.77 | $119.35 | $2,148.30 | 70 |
| GOOGL | 14 | $179.71 | $183.76 | $2,572.64 | 85 |
| GS | 3 | $717.52 | $703.10 | $2,109.30 | 70 |
| HD | 6 | $372.64 | $362.27 | $2,173.65 | 65 |
| INTC | 89 | $22.39 | $23.27 | $2,070.59 | 65 |
| JNJ | 13 | $155.95 | $155.59 | $2,022.73 | 65 |
| JPM | 9 | $291.63 | $287.09 | $2,583.81 | 85 |
| KO | 30 | $70.97 | $69.40 | $2,081.97 | 65 |
| LLY | 3 | $781.32 | $778.59 | $2,335.77 | 65 |
| MA | 4 | $563.08 | $553.07 | $2,212.28 | 65 |
| META | 3 | $717.12 | $715.84 | $2,147.51 | 65 |
| MRK | 25 | $82.54 | $81.70 | $2,042.58 | 65 |
| MSFT | 5 | $498.84 | $507.42 | $2,537.08 | 70 |
| NFLX | 1 | $1,279.00 | $1,257.85 | $1,257.85 | 65 |
| NKE | 30 | $72.03 | $71.86 | $2,155.69 | 70 |
| NVDA | 13 | $171.77 | $170.60 | $2,217.80 | 70 |
| ORCL | 10 | $233.25 | $233.12 | $2,331.20 | 75 |
| PEP | 15 | $136.57 | $134.10 | $2,011.50 | 65 |
| PFE | 83 | $25.22 | $24.79 | $2,057.77 | 65 |
| PG | 14 | $152.15 | $152.69 | $2,137.61 | 65 |
| PYPL | 28 | $72.12 | $73.84 | $2,067.52 | 65 |
| QCOM | 14 | $153.83 | $154.92 | $2,168.88 | 65 |
| T | 77 | $27.09 | $26.93 | $2,073.61 | 65 |
| TGT | 20 | $104.94 | $102.75 | $2,055.00 | 65 |
| TSLA | 6 | $318.51 | $314.86 | $1,889.13 | 65 |
| UNH | 7 | $298.51 | $294.75 | $2,063.23 | 65 |
| UNP | 10 | $236.13 | $232.34 | $2,323.40 | 75 |
| V | 6 | $355.85 | $348.13 | $2,088.78 | 65 |
| VZ | 50 | $43.08 | $41.23 | $2,061.75 | 65 |
| WFC | 28 | $78.86 | $78.48 | $2,197.44 | 70 |
| WMT | 21 | $97.38 | $95.69 | $2,009.49 | 65 |
| XOM | 21 | $109.99 | $112.92 | $2,371.32 | 75 |

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
| 2025-07-15 17:40:07 | SELL | NVDA | 2 | $170.66 | $-1.93 | 70 |
| 2025-07-15 17:40:07 | SELL | PYPL | 1 | $73.84 | $1.66 | 65 |
| 2025-07-15 17:40:07 | BUY | AMZN | 1 | $226.36 | N/A | 85 |
| 2025-07-15 17:40:07 | BUY | NKE | 1 | $71.86 | N/A | 70 |
| 2025-07-15 17:40:07 | BUY | WFC | 1 | $78.48 | N/A | 70 |
| 2025-07-15 17:40:07 | BUY | UNP | 1 | $232.34 | N/A | 75 |
| 2025-07-15 17:40:07 | BUY | ORCL | 1 | $233.15 | N/A | 75 |
| 2025-07-15 17:40:07 | BUY | CVX | 1 | $150.49 | N/A | 85 |
| 2025-07-15 17:25:36 | SELL | BAC | 3 | $46.31 | $-6.97 | 65 |
| 2025-07-15 17:25:36 | SELL | UNP | 1 | $232.23 | $-3.89 | 65 |
| 2025-07-15 17:25:36 | SELL | CVX | 2 | $150.52 | $6.62 | 75 |
| 2025-07-15 17:25:36 | BUY | NVDA | 2 | $170.62 | N/A | 85 |
| 2025-07-15 17:25:36 | BUY | INTC | 6 | $23.20 | N/A | 65 |
| 2025-07-15 17:09:19 | SELL | INTC | 6 | $23.23 | $4.98 | 60 |
| 2025-07-15 17:09:19 | BUY | PG | 1 | $152.54 | N/A | 70 |
| 2025-07-15 17:09:19 | BUY | UNP | 1 | $232.19 | N/A | 75 |
| 2025-07-15 17:09:19 | BUY | CVX | 2 | $150.43 | N/A | 85 |
| 2025-07-15 16:57:02 | SELL | NKE | 1 | $71.99 | $-0.05 | 65 |
| 2025-07-15 16:57:02 | SELL | WFC | 1 | $78.58 | $-0.28 | 65 |
| 2025-07-15 16:57:02 | SELL | BA | 1 | $230.25 | $15.84 | 70 |
| 2025-07-15 16:57:02 | SELL | CVX | 1 | $150.56 | $3.53 | 75 |
| 2025-07-15 16:57:02 | BUY | BAC | 4 | $46.47 | N/A | 70 |
| 2025-07-15 16:57:02 | BUY | INTC | 1 | $23.25 | N/A | 65 |
| 2025-07-15 16:57:02 | BUY | DIS | 1 | $119.46 | N/A | 70 |
| 2025-07-15 16:44:17 | SELL | AMZN | 1 | $226.16 | $4.11 | 70 |

<!--TRADE_LOG_END--> 
