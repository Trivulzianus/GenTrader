# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 19:24:42**

| Metric | Value |
|---|---|
| **Total Value** | **$100,943.59** |
| Cash | $1,703.67 |
| Holdings Value | $99,239.93 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.80 | $2,098.00 | 70 |
| ADBE | 5 | $377.60 | $373.92 | $1,869.60 | 65 |
| AMD | 15 | $135.39 | $138.83 | $2,082.45 | 65 |
| AMZN | 11 | $221.90 | $222.62 | $2,448.82 | 85 |
| AVGO | 8 | $275.34 | $277.56 | $2,220.44 | 70 |
| AXP | 7 | $325.28 | $317.81 | $2,224.67 | 75 |
| BA | 9 | $210.97 | $226.55 | $2,038.95 | 65 |
| BAC | 46 | $48.73 | $46.83 | $2,154.18 | 70 |
| C | 31 | $86.66 | $85.72 | $2,657.38 | 85 |
| CAT | 6 | $397.86 | $402.00 | $2,412.00 | 75 |
| COST | 2 | $979.83 | $978.26 | $1,956.52 | 65 |
| CRM | 8 | $268.33 | $271.01 | $2,168.05 | 65 |
| CSCO | 33 | $68.35 | $69.28 | $2,286.08 | 75 |
| CVX | 16 | $146.68 | $153.28 | $2,452.56 | 75 |
| DIS | 17 | $122.91 | $120.93 | $2,055.81 | 65 |
| GOOGL | 13 | $179.49 | $176.31 | $2,292.04 | 75 |
| GS | 3 | $717.52 | $697.22 | $2,091.66 | 70 |
| HD | 6 | $372.64 | $369.59 | $2,217.54 | 70 |
| INTC | 87 | $22.32 | $23.43 | $2,038.42 | 65 |
| JNJ | 13 | $155.89 | $155.70 | $2,024.13 | 65 |
| JPM | 9 | $291.61 | $282.78 | $2,544.99 | 75 |
| KO | 29 | $71.03 | $69.50 | $2,015.64 | 65 |
| LLY | 2 | $776.66 | $787.59 | $1,575.17 | 65 |
| MA | 4 | $563.08 | $563.37 | $2,253.48 | 65 |
| META | 3 | $717.12 | $735.32 | $2,205.96 | 85 |
| MRK | 28 | $82.45 | $83.86 | $2,348.16 | 75 |
| MSFT | 5 | $498.84 | $502.44 | $2,512.18 | 85 |
| NFLX | 1 | $1,279.00 | $1,285.56 | $1,285.56 | 65 |
| NKE | 31 | $75.82 | $73.72 | $2,285.47 | 75 |
| NVDA | 16 | $157.22 | $163.14 | $2,610.22 | 85 |
| ORCL | 9 | $233.31 | $234.55 | $2,110.95 | 75 |
| PEP | 15 | $136.57 | $134.36 | $2,015.40 | 65 |
| PFE | 86 | $25.22 | $25.46 | $2,189.81 | 70 |
| PG | 13 | $160.75 | $156.96 | $2,040.48 | 65 |
| PYPL | 30 | $76.68 | $74.79 | $2,243.72 | 70 |
| QCOM | 14 | $161.87 | $159.13 | $2,227.82 | 75 |
| T | 72 | $28.56 | $28.16 | $2,027.52 | 65 |
| TGT | 20 | $104.89 | $102.47 | $2,049.40 | 65 |
| TSLA | 6 | $288.62 | $297.37 | $1,784.22 | 65 |
| UNH | 7 | $314.75 | $302.70 | $2,118.90 | 65 |
| UNP | 9 | $236.60 | $237.55 | $2,137.95 | 75 |
| V | 6 | $355.95 | $356.55 | $2,139.30 | 65 |
| VZ | 48 | $43.15 | $42.69 | $2,048.88 | 65 |
| WFC | 29 | $82.30 | $81.75 | $2,370.89 | 75 |
| WMT | 21 | $97.35 | $96.86 | $2,034.06 | 65 |
| XOM | 20 | $109.83 | $113.72 | $2,274.50 | 75 |

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
| 2025-07-09 18:45:21 | SELL | BA | 1 | $226.55 | $14.02 | 65 |
| 2025-07-09 18:45:21 | BUY | AMZN | 1 | $222.52 | N/A | 85 |
| 2025-07-09 18:45:21 | BUY | GOOGL | 1 | $176.15 | N/A | 75 |
| 2025-07-09 18:45:21 | BUY | PYPL | 2 | $74.62 | N/A | 75 |
| 2025-07-09 18:45:21 | BUY | CSCO | 1 | $69.21 | N/A | 70 |
| 2025-07-09 18:27:27 | SELL | GOOGL | 1 | $176.27 | $-3.23 | 65 |
| 2025-07-09 18:27:27 | SELL | BAC | 3 | $46.96 | $-5.20 | 65 |
| 2025-07-09 18:27:27 | SELL | WFC | 2 | $81.72 | $-1.05 | 75 |
| 2025-07-09 18:27:27 | SELL | CSCO | 4 | $69.18 | $3.26 | 65 |

<!--TRADE_LOG_END--> 
