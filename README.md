# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 15:40:33**

| Metric | Value |
|---|---|
| **Total Value** | **$100,767.31** |
| Cash | $2,057.39 |
| Holdings Value | $98,709.92 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $207.65 | $2,076.45 | 70 |
| ADBE | 5 | $377.60 | $376.45 | $1,882.27 | 65 |
| AMD | 15 | $135.39 | $138.12 | $2,071.80 | 70 |
| AMZN | 10 | $221.83 | $222.67 | $2,226.70 | 75 |
| AVGO | 8 | $275.34 | $274.90 | $2,199.20 | 70 |
| AXP | 7 | $325.28 | $318.76 | $2,231.32 | 70 |
| BA | 9 | $210.79 | $227.51 | $2,047.59 | 65 |
| BAC | 44 | $48.83 | $46.88 | $2,062.76 | 65 |
| C | 26 | $86.78 | $86.03 | $2,236.65 | 70 |
| CAT | 6 | $397.86 | $399.17 | $2,394.99 | 65 |
| COST | 2 | $979.83 | $977.17 | $1,954.33 | 65 |
| CRM | 8 | $268.33 | $271.06 | $2,168.48 | 65 |
| CSCO | 34 | $68.35 | $68.69 | $2,335.63 | 75 |
| CVX | 16 | $146.66 | $152.64 | $2,442.24 | 75 |
| DIS | 19 | $122.72 | $121.16 | $2,302.04 | 70 |
| GOOGL | 13 | $179.50 | $177.97 | $2,313.55 | 75 |
| GS | 3 | $717.52 | $698.14 | $2,094.43 | 75 |
| HD | 6 | $372.64 | $366.05 | $2,196.30 | 65 |
| INTC | 87 | $22.34 | $23.25 | $2,023.18 | 65 |
| JNJ | 13 | $155.89 | $155.44 | $2,020.72 | 65 |
| JPM | 9 | $291.61 | $284.14 | $2,557.26 | 75 |
| KO | 29 | $71.03 | $69.17 | $2,005.84 | 65 |
| LLY | 2 | $776.66 | $785.07 | $1,570.14 | 70 |
| MA | 4 | $563.08 | $562.14 | $2,248.58 | 70 |
| META | 3 | $717.12 | $734.38 | $2,203.14 | 85 |
| MRK | 29 | $82.50 | $83.41 | $2,418.74 | 75 |
| MSFT | 5 | $498.84 | $500.96 | $2,504.82 | 85 |
| NFLX | 1 | $1,279.00 | $1,282.02 | $1,282.02 | 65 |
| NKE | 29 | $75.98 | $73.84 | $2,141.51 | 70 |
| NVDA | 16 | $157.22 | $163.28 | $2,612.40 | 85 |
| ORCL | 9 | $233.41 | $233.42 | $2,100.78 | 65 |
| PEP | 15 | $136.57 | $133.60 | $2,004.00 | 65 |
| PFE | 81 | $25.21 | $25.39 | $2,056.60 | 65 |
| PG | 13 | $160.75 | $156.91 | $2,039.89 | 65 |
| PYPL | 31 | $76.64 | $74.80 | $2,318.80 | 75 |
| QCOM | 14 | $161.87 | $158.93 | $2,225.02 | 75 |
| T | 72 | $28.56 | $28.12 | $2,025.00 | 65 |
| TGT | 20 | $104.89 | $102.30 | $2,046.00 | 65 |
| TSLA | 6 | $288.62 | $295.95 | $1,775.70 | 65 |
| UNH | 7 | $314.75 | $300.04 | $2,100.28 | 65 |
| UNP | 9 | $236.60 | $237.29 | $2,135.61 | 70 |
| V | 6 | $355.95 | $354.72 | $2,128.32 | 70 |
| VZ | 48 | $43.15 | $42.62 | $2,045.52 | 65 |
| WFC | 30 | $82.26 | $81.84 | $2,455.35 | 80 |
| WMT | 21 | $97.35 | $97.11 | $2,039.41 | 65 |
| XOM | 21 | $110.02 | $113.74 | $2,388.54 | 75 |

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
| 2025-07-09 15:40:22 | SELL | BAC | 3 | $46.88 | $-5.46 | 65 |
| 2025-07-09 15:40:22 | SELL | PFE | 5 | $25.40 | $0.87 | 65 |
| 2025-07-09 15:40:22 | SELL | PG | 1 | $156.94 | $-3.54 | 65 |
| 2025-07-09 15:40:22 | SELL | CVX | 1 | $152.64 | $5.63 | 75 |
| 2025-07-09 15:40:22 | BUY | INTC | 1 | $23.25 | N/A | 65 |
| 2025-07-09 15:40:22 | BUY | NKE | 1 | $73.84 | N/A | 70 |
| 2025-07-09 15:40:22 | BUY | WFC | 1 | $81.85 | N/A | 80 |
| 2025-07-09 15:40:22 | BUY | CSCO | 2 | $68.68 | N/A | 75 |
| 2025-07-09 15:26:48 | SELL | NKE | 1 | $73.75 | $-2.22 | 65 |
| 2025-07-09 15:26:48 | SELL | C | 4 | $85.93 | $-2.92 | 70 |
| 2025-07-09 15:26:48 | BUY | INTC | 5 | $23.59 | N/A | 65 |
| 2025-07-09 15:26:48 | BUY | PG | 1 | $156.78 | N/A | 70 |
| 2025-07-09 15:26:48 | BUY | CSCO | 1 | $68.65 | N/A | 70 |
| 2025-07-09 15:26:48 | BUY | CVX | 2 | $152.68 | N/A | 85 |
| 2025-07-09 15:09:06 | SELL | AMZN | 1 | $219.36 | $-2.25 | 70 |
| 2025-07-09 15:09:06 | SELL | XOM | 1 | $113.82 | $3.62 | 75 |
| 2025-07-09 15:09:06 | SELL | BA | 1 | $227.19 | $14.76 | 65 |
| 2025-07-09 15:09:06 | BUY | PFE | 1 | $25.47 | N/A | 70 |
| 2025-07-09 15:09:06 | BUY | C | 4 | $86.19 | N/A | 85 |
| 2025-07-09 15:09:06 | BUY | CSCO | 1 | $68.60 | N/A | 70 |
| 2025-07-09 14:52:38 | SELL | INTC | 6 | $23.30 | $5.84 | 60 |
| 2025-07-09 14:52:38 | SELL | C | 1 | $85.94 | $-0.77 | 70 |
| 2025-07-09 14:52:38 | SELL | QCOM | 2 | $159.13 | $-4.79 | 70 |
| 2025-07-09 14:52:38 | SELL | CSCO | 4 | $68.63 | $1.11 | 65 |
| 2025-07-09 14:52:38 | BUY | AMZN | 1 | $221.62 | N/A | 85 |

<!--TRADE_LOG_END--> 
