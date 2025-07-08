# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 16:43:39**

| Metric | Value |
|---|---|
| **Total Value** | **$100,883.39** |
| Cash | $1,071.36 |
| Holdings Value | $99,812.03 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.64 | $2,106.40 | 65 |
| ADBE | 5 | $377.60 | $383.67 | $1,918.35 | 65 |
| AMD | 16 | $135.69 | $138.00 | $2,208.00 | 70 |
| AMZN | 10 | $221.61 | $220.61 | $2,206.13 | 70 |
| AVGO | 8 | $275.34 | $275.00 | $2,200.00 | 70 |
| AXP | 8 | $324.24 | $320.29 | $2,562.32 | 85 |
| BA | 9 | $211.84 | $217.60 | $1,958.44 | 65 |
| BAC | 49 | $48.66 | $47.15 | $2,310.35 | 75 |
| C | 30 | $86.60 | $86.13 | $2,583.90 | 85 |
| CAT | 6 | $397.86 | $393.68 | $2,362.08 | 75 |
| COST | 2 | $979.83 | $989.47 | $1,978.94 | 65 |
| CRM | 8 | $268.33 | $275.05 | $2,200.40 | 65 |
| CSCO | 32 | $68.35 | $68.76 | $2,200.38 | 70 |
| CVX | 16 | $146.69 | $152.11 | $2,433.71 | 75 |
| DIS | 17 | $122.85 | $122.30 | $2,079.10 | 70 |
| GOOGL | 12 | $179.60 | $174.14 | $2,089.68 | 65 |
| GS | 3 | $717.52 | $698.75 | $2,096.25 | 70 |
| HD | 6 | $372.64 | $369.42 | $2,216.51 | 65 |
| INTC | 87 | $22.32 | $23.39 | $2,034.84 | 65 |
| JNJ | 14 | $155.85 | $156.12 | $2,185.68 | 65 |
| JPM | 9 | $291.61 | $281.38 | $2,532.42 | 75 |
| KO | 29 | $71.03 | $70.17 | $2,034.79 | 65 |
| LLY | 2 | $776.66 | $791.43 | $1,582.86 | 65 |
| MA | 4 | $563.08 | $562.45 | $2,249.80 | 65 |
| META | 3 | $717.12 | $719.78 | $2,159.34 | 75 |
| MRK | 32 | $82.44 | $82.24 | $2,631.68 | 85 |
| MSFT | 5 | $498.84 | $495.55 | $2,477.75 | 75 |
| NFLX | 1 | $1,279.00 | $1,274.51 | $1,274.51 | 65 |
| NKE | 30 | $75.91 | $74.11 | $2,223.15 | 70 |
| NVDA | 14 | $156.50 | $159.58 | $2,234.12 | 70 |
| ORCL | 9 | $233.41 | $236.66 | $2,129.96 | 65 |
| PEP | 15 | $136.57 | $134.99 | $2,024.91 | 65 |
| PFE | 80 | $25.25 | $25.68 | $2,054.00 | 65 |
| PG | 13 | $160.77 | $158.57 | $2,061.41 | 65 |
| PYPL | 31 | $76.64 | $74.85 | $2,320.37 | 75 |
| QCOM | 14 | $161.75 | $160.58 | $2,248.12 | 75 |
| T | 78 | $28.53 | $28.34 | $2,210.13 | 70 |
| TGT | 20 | $104.90 | $101.94 | $2,038.70 | 65 |
| TSLA | 6 | $288.62 | $302.00 | $1,812.00 | 60 |
| UNH | 7 | $314.75 | $306.47 | $2,145.29 | 65 |
| UNP | 10 | $236.66 | $237.26 | $2,372.65 | 80 |
| V | 6 | $355.95 | $354.92 | $2,129.52 | 70 |
| VZ | 47 | $43.72 | $43.08 | $2,024.98 | 65 |
| WFC | 29 | $82.34 | $81.69 | $2,369.01 | 75 |
| WMT | 22 | $97.40 | $97.60 | $2,147.20 | 70 |
| XOM | 21 | $110.00 | $113.90 | $2,391.90 | 75 |

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
| 2025-07-08 16:43:31 | SELL | NVDA | 2 | $158.24 | $3.04 | 70 |
| 2025-07-08 16:43:31 | SELL | T | 4 | $28.33 | $-0.74 | 70 |
| 2025-07-08 16:43:31 | SELL | WFC | 1 | $81.65 | $-0.66 | 75 |
| 2025-07-08 16:43:31 | BUY | INTC | 1 | $23.38 | N/A | 65 |
| 2025-07-08 16:43:31 | BUY | BAC | 3 | $47.17 | N/A | 75 |
| 2025-07-08 16:28:46 | SELL | PFE | 12 | $25.68 | $4.43 | 65 |
| 2025-07-08 16:28:46 | SELL | CSCO | 2 | $68.78 | $0.81 | 70 |
| 2025-07-08 16:28:46 | BUY | NVDA | 2 | $159.84 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | INTC | 4 | $23.38 | N/A | 65 |
| 2025-07-08 16:28:46 | BUY | WMT | 1 | $97.81 | N/A | 70 |
| 2025-07-08 16:28:46 | BUY | MRK | 5 | $82.31 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | WFC | 1 | $81.61 | N/A | 80 |
| 2025-07-08 16:28:46 | BUY | C | 2 | $86.18 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | T | 5 | $28.36 | N/A | 75 |
| 2025-07-08 16:09:53 | SELL | XOM | 2 | $113.31 | $6.04 | 75 |
| 2025-07-08 16:09:53 | SELL | WMT | 3 | $97.66 | $0.72 | 65 |
| 2025-07-08 16:09:53 | SELL | MRK | 2 | $81.93 | $-0.99 | 70 |
| 2025-07-08 16:09:53 | SELL | C | 3 | $85.91 | $-1.96 | 75 |
| 2025-07-08 16:09:53 | BUY | PFE | 6 | $25.62 | N/A | 75 |
| 2025-07-08 16:09:53 | BUY | CSCO | 2 | $68.56 | N/A | 75 |
| 2025-07-08 16:09:53 | BUY | T | 5 | $28.33 | N/A | 70 |
| 2025-07-08 15:51:38 | SELL | NVDA | 2 | $159.14 | $5.01 | 70 |
| 2025-07-08 15:51:38 | SELL | INTC | 3 | $23.18 | $2.68 | 60 |
| 2025-07-08 15:51:38 | SELL | PFE | 4 | $25.78 | $1.92 | 70 |
| 2025-07-08 15:51:38 | SELL | T | 4 | $28.36 | $-0.66 | 65 |

<!--TRADE_LOG_END--> 
