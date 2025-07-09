# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 19:50:11**

| Metric | Value |
|---|---|
| **Total Value** | **$100,970.27** |
| Cash | $1,712.14 |
| Holdings Value | $99,258.13 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.37 | $2,103.70 | 65 |
| ADBE | 5 | $377.60 | $373.12 | $1,865.60 | 65 |
| AMD | 15 | $135.39 | $138.45 | $2,076.75 | 65 |
| AMZN | 11 | $221.90 | $222.49 | $2,447.39 | 85 |
| AVGO | 8 | $275.34 | $277.85 | $2,222.76 | 70 |
| AXP | 7 | $325.28 | $318.18 | $2,227.26 | 70 |
| BA | 9 | $210.97 | $226.95 | $2,042.53 | 65 |
| BAC | 46 | $48.73 | $46.84 | $2,154.41 | 70 |
| C | 31 | $86.66 | $85.71 | $2,657.01 | 85 |
| CAT | 6 | $397.86 | $402.48 | $2,414.88 | 75 |
| COST | 2 | $979.83 | $979.37 | $1,958.75 | 65 |
| CRM | 8 | $268.33 | $271.34 | $2,170.72 | 65 |
| CSCO | 32 | $68.32 | $69.20 | $2,214.56 | 70 |
| CVX | 17 | $147.07 | $153.31 | $2,606.27 | 85 |
| DIS | 18 | $122.80 | $120.88 | $2,175.84 | 70 |
| GOOGL | 13 | $179.51 | $176.78 | $2,298.14 | 75 |
| GS | 3 | $717.52 | $697.52 | $2,092.57 | 70 |
| HD | 6 | $372.64 | $370.11 | $2,220.63 | 70 |
| INTC | 81 | $22.24 | $23.41 | $1,896.21 | 60 |
| JNJ | 13 | $155.89 | $155.80 | $2,025.40 | 65 |
| JPM | 9 | $291.61 | $283.06 | $2,547.59 | 75 |
| KO | 29 | $71.03 | $69.50 | $2,015.36 | 65 |
| LLY | 2 | $776.66 | $787.00 | $1,574.01 | 65 |
| MA | 4 | $563.08 | $563.75 | $2,255.02 | 65 |
| META | 3 | $717.12 | $734.67 | $2,204.01 | 85 |
| MRK | 28 | $82.45 | $83.87 | $2,348.36 | 75 |
| MSFT | 5 | $498.84 | $503.01 | $2,515.05 | 70 |
| NFLX | 1 | $1,279.00 | $1,283.39 | $1,283.39 | 65 |
| NKE | 29 | $75.94 | $73.67 | $2,136.43 | 70 |
| NVDA | 16 | $157.22 | $162.90 | $2,606.40 | 85 |
| ORCL | 9 | $233.31 | $235.40 | $2,118.64 | 70 |
| PEP | 15 | $136.57 | $134.34 | $2,015.10 | 65 |
| PFE | 86 | $25.22 | $25.50 | $2,193.43 | 70 |
| PG | 13 | $160.75 | $157.04 | $2,041.53 | 65 |
| PYPL | 31 | $76.62 | $74.86 | $2,320.66 | 75 |
| QCOM | 14 | $161.87 | $159.36 | $2,231.04 | 70 |
| T | 72 | $28.56 | $28.11 | $2,023.91 | 65 |
| TGT | 20 | $104.89 | $102.61 | $2,052.20 | 65 |
| TSLA | 6 | $288.62 | $297.34 | $1,784.04 | 65 |
| UNH | 7 | $314.75 | $302.26 | $2,115.82 | 65 |
| UNP | 9 | $236.60 | $237.07 | $2,133.63 | 75 |
| V | 6 | $355.95 | $357.36 | $2,144.13 | 65 |
| VZ | 48 | $43.15 | $42.65 | $2,047.20 | 65 |
| WFC | 29 | $82.30 | $81.72 | $2,369.74 | 75 |
| WMT | 21 | $97.35 | $96.86 | $2,034.06 | 65 |
| XOM | 20 | $109.83 | $113.80 | $2,276.00 | 75 |

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
| 2025-07-09 19:50:04 | SELL | INTC | 6 | $23.43 | $6.69 | 60 |
| 2025-07-09 19:50:04 | SELL | CSCO | 1 | $69.21 | $0.87 | 70 |
| 2025-07-09 19:50:04 | BUY | GOOGL | 1 | $176.74 | N/A | 75 |
| 2025-07-09 19:50:04 | BUY | DIS | 1 | $120.89 | N/A | 70 |
| 2025-07-09 19:50:04 | BUY | PYPL | 1 | $74.86 | N/A | 75 |
| 2025-07-09 19:50:04 | BUY | NKE | 1 | $73.72 | N/A | 70 |
| 2025-07-09 19:36:16 | SELL | GOOGL | 1 | $176.47 | $-3.02 | 65 |
| 2025-07-09 19:36:16 | SELL | NKE | 3 | $73.92 | $-5.69 | 65 |
| 2025-07-09 19:36:16 | BUY | CVX | 1 | $153.36 | N/A | 85 |
| 2025-07-09 19:24:35 | SELL | DIS | 1 | $120.95 | $-1.85 | 65 |
| 2025-07-09 19:24:35 | SELL | PYPL | 1 | $74.80 | $-1.82 | 70 |
| 2025-07-09 19:24:35 | SELL | CVX | 1 | $153.29 | $6.23 | 75 |
| 2025-07-09 19:24:35 | BUY | CSCO | 1 | $69.28 | N/A | 75 |
| 2025-07-09 19:08:38 | SELL | CSCO | 1 | $69.25 | $0.91 | 70 |
| 2025-07-09 19:08:38 | BUY | DIS | 1 | $120.63 | N/A | 70 |
| 2025-07-09 19:08:38 | BUY | NKE | 1 | $73.64 | N/A | 75 |
| 2025-07-09 19:08:38 | BUY | CVX | 1 | $153.20 | N/A | 85 |
| 2025-07-09 18:57:16 | SELL | INTC | 1 | $23.40 | $1.07 | 65 |
| 2025-07-09 18:57:16 | SELL | PFE | 1 | $25.44 | $0.22 | 70 |
| 2025-07-09 18:57:16 | SELL | T | 1 | $28.15 | $-0.40 | 65 |
| 2025-07-09 18:57:16 | BUY | BAC | 2 | $46.92 | N/A | 70 |
| 2025-07-09 18:57:16 | BUY | CSCO | 2 | $69.26 | N/A | 75 |
| 2025-07-09 18:57:16 | BUY | CVX | 1 | $153.03 | N/A | 80 |
| 2025-07-09 18:45:21 | SELL | DIS | 1 | $120.70 | $-2.11 | 65 |
| 2025-07-09 18:45:21 | SELL | WFC | 1 | $81.69 | $-0.59 | 75 |

<!--TRADE_LOG_END--> 
