# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 15:51:45**

| Metric | Value |
|---|---|
| **Total Value** | **$100,840.72** |
| Cash | $1,088.85 |
| Holdings Value | $99,751.87 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.03 | $2,100.35 | 65 |
| ADBE | 5 | $377.60 | $384.16 | $1,920.80 | 65 |
| AMD | 16 | $135.69 | $137.84 | $2,205.45 | 70 |
| AMZN | 10 | $221.61 | $220.31 | $2,203.08 | 70 |
| AVGO | 8 | $275.34 | $274.49 | $2,195.88 | 70 |
| AXP | 8 | $324.24 | $320.81 | $2,566.50 | 85 |
| BA | 9 | $211.84 | $216.89 | $1,952.01 | 65 |
| BAC | 46 | $48.76 | $47.16 | $2,169.13 | 70 |
| C | 31 | $86.56 | $86.12 | $2,669.72 | 85 |
| CAT | 6 | $397.86 | $393.68 | $2,362.08 | 70 |
| COST | 2 | $979.83 | $988.92 | $1,977.84 | 65 |
| CRM | 8 | $268.33 | $274.57 | $2,196.56 | 65 |
| CSCO | 32 | $68.36 | $68.67 | $2,197.60 | 70 |
| CVX | 16 | $146.69 | $151.43 | $2,422.80 | 75 |
| DIS | 17 | $122.85 | $122.40 | $2,080.81 | 70 |
| GOOGL | 12 | $179.60 | $174.23 | $2,090.76 | 65 |
| GS | 3 | $717.52 | $701.14 | $2,103.42 | 70 |
| HD | 6 | $372.64 | $369.72 | $2,218.32 | 70 |
| INTC | 82 | $22.25 | $23.16 | $1,899.53 | 60 |
| JNJ | 14 | $155.85 | $156.38 | $2,189.39 | 70 |
| JPM | 9 | $291.61 | $282.54 | $2,542.86 | 75 |
| KO | 29 | $71.03 | $70.29 | $2,038.41 | 65 |
| LLY | 2 | $776.66 | $790.38 | $1,580.75 | 65 |
| MA | 4 | $563.08 | $563.49 | $2,253.96 | 65 |
| META | 3 | $717.12 | $719.20 | $2,157.60 | 75 |
| MRK | 29 | $82.43 | $82.06 | $2,379.74 | 75 |
| MSFT | 5 | $498.84 | $495.02 | $2,475.10 | 75 |
| NFLX | 1 | $1,279.00 | $1,272.50 | $1,272.50 | 65 |
| NKE | 30 | $75.91 | $74.34 | $2,230.27 | 70 |
| NVDA | 14 | $156.27 | $159.09 | $2,227.33 | 70 |
| ORCL | 9 | $233.41 | $233.45 | $2,101.05 | 65 |
| PEP | 15 | $136.57 | $135.13 | $2,027.02 | 65 |
| PFE | 86 | $25.28 | $25.79 | $2,217.94 | 70 |
| PG | 13 | $160.77 | $158.81 | $2,064.53 | 65 |
| PYPL | 31 | $76.64 | $75.14 | $2,329.34 | 75 |
| QCOM | 14 | $161.75 | $160.08 | $2,241.12 | 75 |
| T | 72 | $28.54 | $28.36 | $2,042.28 | 65 |
| TGT | 20 | $104.90 | $101.75 | $2,035.00 | 65 |
| TSLA | 6 | $288.62 | $301.77 | $1,810.60 | 65 |
| UNH | 7 | $314.75 | $307.10 | $2,149.66 | 65 |
| UNP | 10 | $236.66 | $237.26 | $2,372.65 | 75 |
| V | 6 | $355.95 | $356.14 | $2,136.84 | 65 |
| VZ | 47 | $43.72 | $43.22 | $2,031.11 | 65 |
| WFC | 29 | $82.34 | $81.53 | $2,364.51 | 75 |
| WMT | 24 | $97.42 | $97.35 | $2,336.47 | 75 |
| XOM | 23 | $110.29 | $113.53 | $2,611.19 | 85 |

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
| 2025-07-08 15:51:38 | SELL | NVDA | 2 | $159.14 | $5.01 | 70 |
| 2025-07-08 15:51:38 | SELL | INTC | 3 | $23.18 | $2.68 | 60 |
| 2025-07-08 15:51:38 | SELL | PFE | 4 | $25.78 | $1.92 | 70 |
| 2025-07-08 15:51:38 | SELL | T | 4 | $28.36 | $-0.66 | 65 |
| 2025-07-08 15:51:38 | BUY | JNJ | 1 | $156.38 | N/A | 70 |
| 2025-07-08 15:51:38 | BUY | WMT | 1 | $97.38 | N/A | 75 |
| 2025-07-08 15:51:38 | BUY | C | 1 | $86.11 | N/A | 85 |
| 2025-07-08 15:39:25 | SELL | BAC | 1 | $47.29 | $-1.43 | 70 |
| 2025-07-08 15:39:25 | SELL | INTC | 3 | $22.00 | $-0.83 | 60 |
| 2025-07-08 15:39:25 | SELL | UNP | 1 | $237.31 | $0.59 | 75 |
| 2025-07-08 15:39:25 | SELL | CSCO | 1 | $68.58 | $0.22 | 70 |
| 2025-07-08 15:39:25 | BUY | XOM | 1 | $113.43 | N/A | 85 |
| 2025-07-08 15:39:25 | BUY | WMT | 2 | $97.29 | N/A | 75 |
| 2025-07-08 15:39:25 | BUY | PFE | 9 | $25.76 | N/A | 75 |
| 2025-07-08 15:39:25 | BUY | C | 2 | $86.16 | N/A | 85 |
| 2025-07-08 15:39:25 | BUY | T | 3 | $28.25 | N/A | 70 |
| 2025-07-08 15:26:24 | SELL | XOM | 1 | $113.18 | $2.90 | 75 |
| 2025-07-08 15:26:24 | SELL | DIS | 1 | $122.26 | $-0.55 | 65 |
| 2025-07-08 15:26:24 | SELL | PFE | 4 | $25.75 | $1.90 | 65 |
| 2025-07-08 15:26:24 | SELL | C | 2 | $86.00 | $-1.14 | 75 |
| 2025-07-08 15:26:24 | SELL | CSCO | 1 | $68.57 | $0.19 | 70 |
| 2025-07-08 15:26:24 | SELL | CVX | 1 | $151.10 | $4.15 | 75 |
| 2025-07-08 15:26:24 | BUY | NVDA | 2 | $159.00 | N/A | 85 |
| 2025-07-08 15:26:24 | BUY | INTC | 1 | $23.26 | N/A | 65 |
| 2025-07-08 15:26:24 | BUY | NKE | 1 | $74.01 | N/A | 70 |

<!--TRADE_LOG_END--> 
