# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 16:27:18**

| Metric | Value |
|---|---|
| **Total Value** | **$101,463.88** |
| Cash | $1,524.25 |
| Holdings Value | $99,939.63 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.02 | $2,120.20 | 70 |
| ADBE | 5 | $377.60 | $371.56 | $1,857.78 | 65 |
| AMD | 15 | $134.94 | $143.88 | $2,158.20 | 70 |
| AMZN | 10 | $221.91 | $222.14 | $2,221.37 | 75 |
| AVGO | 8 | $275.34 | $274.29 | $2,194.28 | 70 |
| AXP | 7 | $325.28 | $323.92 | $2,267.44 | 75 |
| BA | 9 | $210.97 | $224.37 | $2,019.33 | 65 |
| BAC | 46 | $48.71 | $47.09 | $2,166.37 | 70 |
| C | 30 | $86.81 | $86.89 | $2,606.85 | 85 |
| CAT | 6 | $397.86 | $410.27 | $2,461.62 | 85 |
| COST | 2 | $979.83 | $973.95 | $1,947.91 | 65 |
| CRM | 8 | $268.33 | $266.86 | $2,134.88 | 65 |
| CSCO | 34 | $68.39 | $68.91 | $2,342.77 | 75 |
| CVX | 17 | $147.16 | $153.66 | $2,612.14 | 85 |
| DIS | 18 | $122.80 | $121.39 | $2,185.02 | 70 |
| GOOGL | 13 | $179.61 | $176.72 | $2,297.41 | 75 |
| GS | 3 | $717.52 | $707.60 | $2,122.80 | 75 |
| HD | 6 | $372.64 | $376.13 | $2,256.81 | 70 |
| INTC | 83 | $22.25 | $23.71 | $1,968.35 | 65 |
| JNJ | 13 | $155.89 | $157.82 | $2,051.66 | 65 |
| JPM | 9 | $291.61 | $287.52 | $2,587.68 | 85 |
| KO | 29 | $71.03 | $69.53 | $2,016.51 | 65 |
| LLY | 2 | $776.66 | $794.25 | $1,588.50 | 65 |
| MA | 4 | $563.08 | $562.94 | $2,251.76 | 70 |
| META | 3 | $717.12 | $726.65 | $2,179.95 | 85 |
| MRK | 28 | $82.46 | $84.41 | $2,363.61 | 75 |
| MSFT | 5 | $498.84 | $500.10 | $2,500.50 | 85 |
| NFLX | 1 | $1,279.00 | $1,263.82 | $1,263.82 | 65 |
| NKE | 30 | $75.81 | $75.42 | $2,262.45 | 75 |
| NVDA | 15 | $157.07 | $163.24 | $2,448.53 | 85 |
| ORCL | 9 | $233.31 | $235.57 | $2,120.13 | 70 |
| PEP | 15 | $136.57 | $136.29 | $2,044.35 | 65 |
| PFE | 77 | $25.15 | $25.82 | $1,988.14 | 65 |
| PG | 13 | $160.77 | $159.01 | $2,067.13 | 65 |
| PYPL | 31 | $76.64 | $75.98 | $2,355.38 | 75 |
| QCOM | 16 | $161.60 | $159.72 | $2,555.52 | 85 |
| T | 73 | $28.55 | $27.58 | $2,013.33 | 65 |
| TGT | 20 | $104.91 | $105.65 | $2,113.00 | 70 |
| TSLA | 6 | $288.62 | $303.94 | $1,823.67 | 65 |
| UNH | 6 | $298.34 | $301.91 | $1,811.47 | 65 |
| UNP | 9 | $236.20 | $238.65 | $2,147.85 | 70 |
| V | 6 | $355.85 | $355.82 | $2,134.95 | 65 |
| VZ | 48 | $43.15 | $41.99 | $2,015.76 | 65 |
| WFC | 32 | $82.33 | $82.68 | $2,645.76 | 85 |
| WMT | 21 | $97.36 | $95.73 | $2,010.43 | 65 |
| XOM | 23 | $110.31 | $114.62 | $2,636.26 | 85 |

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
| 2025-07-10 16:27:11 | SELL | BAC | 1 | $47.10 | $-1.58 | 70 |
| 2025-07-10 16:27:11 | SELL | PFE | 2 | $25.82 | $1.31 | 65 |
| 2025-07-10 16:27:11 | SELL | MRK | 3 | $84.41 | $5.29 | 75 |
| 2025-07-10 16:27:11 | SELL | VZ | 1 | $41.99 | $-1.13 | 65 |
| 2025-07-10 16:27:11 | SELL | T | 1 | $27.58 | $-0.96 | 65 |
| 2025-07-10 16:27:11 | BUY | NVDA | 1 | $163.26 | N/A | 85 |
| 2025-07-10 16:27:11 | BUY | INTC | 3 | $23.72 | N/A | 65 |
| 2025-07-10 16:27:11 | BUY | NKE | 1 | $75.41 | N/A | 75 |
| 2025-07-10 16:27:11 | BUY | QCOM | 1 | $159.70 | N/A | 85 |
| 2025-07-10 16:09:41 | SELL | NVDA | 2 | $162.90 | $10.99 | 70 |
| 2025-07-10 16:09:41 | SELL | INTC | 6 | $23.75 | $8.66 | 60 |
| 2025-07-10 16:09:41 | BUY | MRK | 3 | $84.54 | N/A | 85 |
| 2025-07-10 16:09:41 | BUY | WFC | 3 | $82.56 | N/A | 85 |
| 2025-07-10 16:09:41 | BUY | CSCO | 1 | $68.98 | N/A | 75 |
| 2025-07-10 15:52:49 | SELL | AMZN | 1 | $221.79 | $-0.11 | 70 |
| 2025-07-10 15:52:49 | SELL | AMD | 1 | $144.29 | $8.77 | 65 |
| 2025-07-10 15:52:49 | SELL | BAC | 2 | $47.06 | $-3.10 | 70 |
| 2025-07-10 15:52:49 | SELL | PFE | 5 | $25.83 | $3.11 | 65 |
| 2025-07-10 15:52:49 | SELL | QCOM | 1 | $159.69 | $-1.91 | 75 |
| 2025-07-10 15:52:49 | BUY | NKE | 2 | $75.04 | N/A | 70 |
| 2025-07-10 15:52:49 | BUY | CSCO | 1 | $68.96 | N/A | 75 |
| 2025-07-10 15:40:57 | SELL | MRK | 1 | $84.34 | $1.83 | 75 |
| 2025-07-10 15:40:57 | SELL | NKE | 1 | $75.13 | $-0.73 | 65 |
| 2025-07-10 15:40:57 | SELL | CSCO | 1 | $68.93 | $0.55 | 70 |
| 2025-07-10 15:40:57 | SELL | T | 1 | $27.53 | $-0.98 | 65 |

<!--TRADE_LOG_END--> 
