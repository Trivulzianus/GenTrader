# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 14:08:23**

| Metric | Value |
|---|---|
| **Total Value** | **$101,142.15** |
| Cash | $1,449.37 |
| Holdings Value | $99,692.78 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.32 | $2,103.20 | 65 |
| ADBE | 5 | $377.60 | $382.47 | $1,912.35 | 65 |
| AMD | 16 | $135.69 | $140.09 | $2,241.36 | 70 |
| AMZN | 10 | $221.61 | $223.87 | $2,238.70 | 75 |
| AVGO | 8 | $275.34 | $276.65 | $2,213.20 | 70 |
| AXP | 7 | $325.28 | $319.27 | $2,234.89 | 75 |
| BA | 10 | $212.43 | $224.71 | $2,247.05 | 65 |
| BAC | 50 | $48.61 | $47.06 | $2,353.25 | 75 |
| C | 27 | $86.71 | $86.11 | $2,324.97 | 75 |
| CAT | 6 | $397.86 | $400.43 | $2,402.58 | 70 |
| COST | 2 | $979.83 | $978.14 | $1,956.28 | 65 |
| CRM | 8 | $268.33 | $273.64 | $2,189.12 | 65 |
| CSCO | 34 | $68.35 | $68.85 | $2,340.90 | 75 |
| CVX | 17 | $147.04 | $153.35 | $2,606.95 | 85 |
| DIS | 19 | $122.74 | $121.59 | $2,310.21 | 70 |
| GOOGL | 13 | $179.50 | $178.34 | $2,318.42 | 75 |
| GS | 3 | $717.52 | $698.98 | $2,096.94 | 65 |
| HD | 6 | $372.64 | $367.46 | $2,204.76 | 65 |
| INTC | 87 | $22.33 | $23.34 | $2,031.01 | 65 |
| JNJ | 13 | $155.89 | $155.67 | $2,023.71 | 65 |
| JPM | 9 | $291.61 | $283.54 | $2,551.82 | 75 |
| KO | 29 | $71.03 | $69.58 | $2,017.68 | 65 |
| LLY | 2 | $776.66 | $791.85 | $1,583.70 | 70 |
| MA | 4 | $563.08 | $562.75 | $2,250.98 | 65 |
| META | 3 | $717.12 | $734.01 | $2,202.03 | 85 |
| MRK | 29 | $82.50 | $83.37 | $2,417.73 | 75 |
| MSFT | 5 | $498.84 | $504.31 | $2,521.55 | 70 |
| NFLX | 1 | $1,279.00 | $1,276.33 | $1,276.33 | 65 |
| NKE | 29 | $75.97 | $74.60 | $2,163.40 | 70 |
| NVDA | 14 | $156.34 | $163.37 | $2,287.16 | 70 |
| ORCL | 9 | $233.41 | $232.88 | $2,095.92 | 65 |
| PEP | 15 | $136.57 | $134.97 | $2,024.55 | 65 |
| PFE | 81 | $25.20 | $25.61 | $2,074.79 | 65 |
| PG | 13 | $160.77 | $157.51 | $2,047.63 | 65 |
| PYPL | 29 | $76.72 | $75.65 | $2,193.85 | 70 |
| QCOM | 15 | $161.64 | $160.52 | $2,407.80 | 75 |
| T | 73 | $28.55 | $28.07 | $2,049.11 | 65 |
| TGT | 20 | $104.89 | $103.14 | $2,062.80 | 65 |
| TSLA | 6 | $288.62 | $297.95 | $1,787.73 | 65 |
| UNH | 7 | $314.75 | $301.26 | $2,108.83 | 65 |
| UNP | 9 | $236.60 | $238.04 | $2,142.36 | 75 |
| V | 6 | $355.95 | $355.85 | $2,135.10 | 70 |
| VZ | 48 | $43.15 | $42.69 | $2,049.12 | 65 |
| WFC | 29 | $82.27 | $81.87 | $2,374.23 | 75 |
| WMT | 22 | $97.35 | $96.85 | $2,130.70 | 65 |
| XOM | 21 | $110.03 | $113.62 | $2,386.02 | 75 |

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
| 2025-07-09 14:08:18 | SELL | NVDA | 2 | $163.34 | $12.24 | 70 |
| 2025-07-09 14:08:18 | SELL | XOM | 1 | $113.63 | $3.43 | 75 |
| 2025-07-09 14:08:18 | SELL | QCOM | 1 | $160.52 | $-1.05 | 75 |
| 2025-07-09 14:08:18 | SELL | TGT | 1 | $103.17 | $-1.64 | 65 |
| 2025-07-09 14:08:18 | BUY | GOOGL | 1 | $178.32 | N/A | 75 |
| 2025-07-09 14:08:18 | BUY | INTC | 6 | $23.33 | N/A | 65 |
| 2025-07-09 14:08:18 | BUY | AMD | 1 | $137.82 | N/A | 70 |
| 2025-07-09 14:08:18 | BUY | BAC | 6 | $47.10 | N/A | 75 |
| 2025-07-09 14:08:18 | BUY | PYPL | 1 | $75.67 | N/A | 70 |
| 2025-07-09 14:08:18 | BUY | CSCO | 1 | $68.59 | N/A | 75 |
| 2025-07-09 14:08:18 | BUY | VZ | 1 | $42.69 | N/A | 65 |
| 2025-07-09 13:46:32 | SELL | BAC | 6 | $47.26 | $-8.24 | 65 |
| 2025-07-09 13:46:32 | SELL | INTC | 5 | $23.45 | $5.64 | 60 |
| 2025-07-09 13:46:32 | SELL | PYPL | 3 | $75.58 | $-3.20 | 65 |
| 2025-07-09 13:46:32 | SELL | WMT | 2 | $96.98 | $-0.67 | 65 |
| 2025-07-09 13:46:32 | SELL | PFE | 22 | $25.68 | $8.25 | 65 |
| 2025-07-09 13:46:32 | SELL | WFC | 3 | $82.17 | $-0.28 | 75 |
| 2025-07-09 13:46:32 | SELL | UNP | 1 | $237.24 | $0.58 | 65 |
| 2025-07-09 13:46:32 | SELL | CSCO | 1 | $68.85 | $0.49 | 70 |
| 2025-07-09 13:46:32 | BUY | NVDA | 1 | $160.00 | N/A | 85 |
| 2025-07-09 13:46:32 | BUY | XOM | 1 | $113.72 | N/A | 80 |
| 2025-07-09 13:46:32 | BUY | QCOM | 1 | $160.97 | N/A | 85 |
| 2025-07-09 13:46:32 | BUY | T | 1 | $28.16 | N/A | 65 |
| 2025-07-09 13:46:32 | BUY | TGT | 1 | $102.87 | N/A | 70 |
| 2025-07-09 13:28:47 | SELL | XOM | 2 | $114.19 | $7.60 | 75 |

<!--TRADE_LOG_END--> 
