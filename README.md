# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 19:36:04**

| Metric | Value |
|---|---|
| **Total Value** | **$100,699.19** |
| Cash | $812.17 |
| Holdings Value | $99,887.03 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.62 | $2,096.15 | 65 |
| ADBE | 5 | $377.60 | $381.36 | $1,906.80 | 65 |
| AMD | 16 | $135.69 | $138.09 | $2,209.52 | 70 |
| AMZN | 10 | $221.61 | $219.65 | $2,196.50 | 70 |
| AVGO | 8 | $275.34 | $272.42 | $2,179.36 | 70 |
| AXP | 8 | $324.24 | $318.60 | $2,548.76 | 85 |
| BA | 10 | $212.43 | $218.67 | $2,186.70 | 70 |
| BAC | 49 | $48.66 | $47.31 | $2,318.43 | 75 |
| C | 30 | $86.59 | $85.96 | $2,578.83 | 85 |
| CAT | 6 | $397.86 | $394.82 | $2,368.92 | 70 |
| COST | 2 | $979.83 | $986.00 | $1,972.00 | 65 |
| CRM | 8 | $268.33 | $273.63 | $2,189.04 | 65 |
| CSCO | 32 | $68.34 | $68.62 | $2,196.00 | 70 |
| CVX | 17 | $147.04 | $152.59 | $2,594.11 | 85 |
| DIS | 17 | $122.85 | $122.11 | $2,075.95 | 65 |
| GOOGL | 12 | $179.60 | $174.05 | $2,088.60 | 65 |
| GS | 3 | $717.52 | $698.01 | $2,094.03 | 75 |
| HD | 6 | $372.64 | $368.20 | $2,209.20 | 70 |
| INTC | 85 | $22.31 | $23.68 | $2,012.38 | 65 |
| JNJ | 13 | $155.89 | $155.50 | $2,021.43 | 65 |
| JPM | 9 | $291.61 | $282.77 | $2,544.97 | 85 |
| KO | 29 | $71.03 | $70.44 | $2,042.76 | 65 |
| LLY | 2 | $776.66 | $779.85 | $1,559.70 | 65 |
| MA | 4 | $563.08 | $561.20 | $2,244.78 | 65 |
| META | 3 | $717.12 | $719.03 | $2,157.11 | 85 |
| MRK | 29 | $82.50 | $81.34 | $2,359.01 | 75 |
| MSFT | 5 | $498.84 | $495.91 | $2,479.55 | 70 |
| NFLX | 1 | $1,279.00 | $1,268.00 | $1,268.00 | 65 |
| NKE | 29 | $75.97 | $74.03 | $2,146.87 | 70 |
| NVDA | 14 | $156.82 | $159.96 | $2,239.44 | 70 |
| ORCL | 9 | $233.41 | $233.88 | $2,104.92 | 65 |
| PEP | 15 | $136.57 | $135.12 | $2,026.80 | 65 |
| PFE | 90 | $25.26 | $25.61 | $2,305.34 | 75 |
| PG | 13 | $160.77 | $157.79 | $2,051.34 | 70 |
| PYPL | 31 | $76.65 | $74.92 | $2,322.67 | 75 |
| QCOM | 15 | $161.62 | $159.91 | $2,398.72 | 75 |
| T | 81 | $28.53 | $28.41 | $2,300.81 | 75 |
| TGT | 20 | $104.90 | $102.31 | $2,046.30 | 65 |
| TSLA | 6 | $288.62 | $294.80 | $1,768.80 | 65 |
| UNH | 7 | $314.75 | $306.36 | $2,144.49 | 65 |
| UNP | 10 | $236.66 | $237.10 | $2,371.05 | 75 |
| V | 6 | $355.95 | $353.93 | $2,123.58 | 65 |
| VZ | 47 | $43.16 | $43.13 | $2,027.11 | 65 |
| WFC | 29 | $82.33 | $81.80 | $2,372.05 | 75 |
| WMT | 21 | $97.35 | $97.36 | $2,044.46 | 65 |
| XOM | 21 | $110.03 | $113.98 | $2,393.68 | 75 |

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
| 2025-07-08 19:35:58 | SELL | NVDA | 3 | $158.24 | $3.51 | 70 |
| 2025-07-08 19:35:58 | SELL | WMT | 2 | $97.36 | $0.01 | 65 |
| 2025-07-08 19:35:58 | BUY | T | 5 | $28.41 | N/A | 75 |
| 2025-07-08 19:24:24 | SELL | BAC | 1 | $47.31 | $-1.33 | 75 |
| 2025-07-08 19:24:24 | SELL | INTC | 1 | $23.54 | $1.22 | 65 |
| 2025-07-08 19:24:24 | SELL | XOM | 2 | $113.85 | $6.97 | 75 |
| 2025-07-08 19:24:24 | SELL | T | 5 | $28.43 | $-0.52 | 70 |
| 2025-07-08 19:24:24 | BUY | PFE | 5 | $25.58 | N/A | 75 |
| 2025-07-08 19:24:24 | BUY | CVX | 1 | $152.33 | N/A | 85 |
| 2025-07-08 19:08:41 | SELL | PFE | 6 | $25.62 | $2.17 | 70 |
| 2025-07-08 19:08:41 | SELL | WFC | 1 | $81.80 | $-0.51 | 75 |
| 2025-07-08 19:08:41 | SELL | CSCO | 2 | $68.71 | $0.69 | 70 |
| 2025-07-08 19:08:41 | BUY | XOM | 2 | $113.96 | N/A | 85 |
| 2025-07-08 19:08:41 | BUY | C | 4 | $86.01 | N/A | 85 |
| 2025-07-08 19:08:41 | BUY | T | 5 | $28.43 | N/A | 75 |
| 2025-07-08 18:57:14 | SELL | XOM | 1 | $114.01 | $3.81 | 75 |
| 2025-07-08 18:57:14 | SELL | C | 2 | $85.92 | $-1.43 | 70 |
| 2025-07-08 18:57:14 | SELL | CVX | 1 | $152.49 | $5.44 | 75 |
| 2025-07-08 18:57:14 | BUY | WFC | 1 | $81.60 | N/A | 80 |
| 2025-07-08 18:57:14 | BUY | CSCO | 2 | $68.67 | N/A | 75 |
| 2025-07-08 18:57:14 | BUY | PFE | 6 | $25.62 | N/A | 75 |
| 2025-07-08 18:57:14 | BUY | T | 4 | $28.41 | N/A | 70 |
| 2025-07-08 18:45:11 | SELL | C | 2 | $85.97 | $-1.22 | 75 |
| 2025-07-08 18:45:11 | BUY | WMT | 2 | $97.38 | N/A | 75 |
| 2025-07-08 18:45:11 | BUY | CVX | 1 | $152.41 | N/A | 85 |

<!--TRADE_LOG_END--> 
