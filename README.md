# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 15:09:12**

| Metric | Value |
|---|---|
| **Total Value** | **$100,761.29** |
| Cash | $2,027.74 |
| Holdings Value | $98,733.56 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $207.56 | $2,075.55 | 70 |
| ADBE | 5 | $377.60 | $377.25 | $1,886.22 | 65 |
| AMD | 15 | $135.39 | $137.91 | $2,068.65 | 65 |
| AMZN | 10 | $221.83 | $221.80 | $2,218.00 | 70 |
| AVGO | 8 | $275.34 | $274.69 | $2,197.56 | 70 |
| AXP | 7 | $325.28 | $318.85 | $2,231.95 | 75 |
| BA | 9 | $210.79 | $227.17 | $2,044.53 | 65 |
| BAC | 47 | $48.71 | $46.91 | $2,204.53 | 70 |
| C | 30 | $86.66 | $86.19 | $2,585.70 | 85 |
| CAT | 6 | $397.86 | $398.79 | $2,392.74 | 70 |
| COST | 2 | $979.83 | $977.91 | $1,955.82 | 65 |
| CRM | 8 | $268.33 | $270.77 | $2,166.16 | 65 |
| CSCO | 31 | $68.32 | $68.59 | $2,126.45 | 70 |
| CVX | 15 | $146.26 | $152.91 | $2,293.65 | 75 |
| DIS | 19 | $122.72 | $121.16 | $2,302.04 | 75 |
| GOOGL | 13 | $179.50 | $177.70 | $2,310.10 | 70 |
| GS | 3 | $717.52 | $698.69 | $2,096.07 | 70 |
| HD | 6 | $372.64 | $366.02 | $2,196.15 | 65 |
| INTC | 81 | $22.25 | $23.25 | $1,883.65 | 60 |
| JNJ | 13 | $155.89 | $155.63 | $2,023.15 | 65 |
| JPM | 9 | $291.61 | $284.59 | $2,561.31 | 75 |
| KO | 29 | $71.03 | $69.34 | $2,011.00 | 65 |
| LLY | 2 | $776.66 | $788.44 | $1,576.88 | 65 |
| MA | 4 | $563.08 | $561.96 | $2,247.82 | 65 |
| META | 3 | $717.12 | $732.74 | $2,198.22 | 85 |
| MRK | 29 | $82.50 | $83.48 | $2,420.92 | 75 |
| MSFT | 5 | $498.84 | $501.44 | $2,507.20 | 75 |
| NFLX | 1 | $1,279.00 | $1,279.95 | $1,279.95 | 65 |
| NKE | 29 | $75.97 | $73.84 | $2,141.36 | 70 |
| NVDA | 16 | $157.22 | $163.24 | $2,611.86 | 85 |
| ORCL | 9 | $233.41 | $234.10 | $2,106.90 | 70 |
| PEP | 15 | $136.57 | $133.23 | $1,998.39 | 65 |
| PFE | 86 | $25.22 | $25.46 | $2,189.99 | 70 |
| PG | 13 | $160.77 | $156.59 | $2,035.73 | 65 |
| PYPL | 31 | $76.64 | $74.50 | $2,309.65 | 75 |
| QCOM | 14 | $161.87 | $158.48 | $2,218.75 | 75 |
| T | 72 | $28.56 | $28.20 | $2,030.40 | 65 |
| TGT | 20 | $104.89 | $102.09 | $2,041.90 | 65 |
| TSLA | 6 | $288.62 | $295.00 | $1,770.03 | 65 |
| UNH | 7 | $314.75 | $300.05 | $2,100.35 | 65 |
| UNP | 9 | $236.60 | $236.80 | $2,131.20 | 75 |
| V | 6 | $355.95 | $354.74 | $2,128.41 | 70 |
| VZ | 48 | $43.15 | $42.72 | $2,050.32 | 65 |
| WFC | 29 | $82.27 | $81.98 | $2,377.42 | 75 |
| WMT | 21 | $97.35 | $97.08 | $2,038.58 | 65 |
| XOM | 21 | $110.02 | $113.83 | $2,390.33 | 75 |

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
| 2025-07-09 14:52:38 | BUY | XOM | 1 | $113.65 | N/A | 80 |
| 2025-07-09 14:52:38 | BUY | DIS | 1 | $121.29 | N/A | 75 |
| 2025-07-09 14:52:38 | BUY | PYPL | 1 | $74.64 | N/A | 75 |
| 2025-07-09 14:52:38 | BUY | PFE | 5 | $25.45 | N/A | 70 |
| 2025-07-09 14:40:32 | SELL | PYPL | 1 | $74.77 | $-1.87 | 70 |
| 2025-07-09 14:40:32 | SELL | PFE | 5 | $25.50 | $1.39 | 65 |
| 2025-07-09 14:40:32 | BUY | QCOM | 1 | $159.82 | N/A | 85 |
| 2025-07-09 14:26:02 | SELL | BAC | 3 | $47.10 | $-4.51 | 70 |
| 2025-07-09 14:26:02 | SELL | AMD | 1 | $140.20 | $4.51 | 65 |
| 2025-07-09 14:26:02 | SELL | DIS | 1 | $121.69 | $-1.05 | 70 |
| 2025-07-09 14:26:02 | SELL | WMT | 1 | $97.18 | $-0.17 | 65 |
| 2025-07-09 14:26:02 | SELL | T | 1 | $28.23 | $-0.32 | 65 |
| 2025-07-09 14:26:02 | SELL | CVX | 2 | $152.88 | $11.69 | 70 |
| 2025-07-09 14:26:02 | BUY | NVDA | 2 | $163.39 | N/A | 85 |

<!--TRADE_LOG_END--> 
