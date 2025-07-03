# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 14:40:29**

| Metric | Value |
|---|---|
| **Total Value** | **$101,787.10** |
| Cash | $3,025.89 |
| Holdings Value | $98,761.21 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $214.21 | $2,142.10 | 70 |
| ADBE | 5 | $377.60 | $380.63 | $1,903.13 | 65 |
| AMD | 15 | $135.93 | $138.45 | $2,076.69 | 70 |
| AMZN | 10 | $221.48 | $221.90 | $2,219.00 | 70 |
| AVGO | 8 | $269.90 | $274.08 | $2,192.63 | 70 |
| AXP | 8 | $324.40 | $328.38 | $2,627.00 | 80 |
| BA | 10 | $212.15 | $216.34 | $2,163.40 | 70 |
| BAC | 47 | $48.65 | $49.08 | $2,306.76 | 75 |
| C | 30 | $86.80 | $88.31 | $2,649.15 | 85 |
| CAT | 6 | $396.45 | $401.59 | $2,409.54 | 70 |
| COST | 2 | $979.83 | $985.81 | $1,971.62 | 65 |
| CRM | 7 | $267.51 | $272.03 | $1,904.21 | 65 |
| CSCO | 33 | $68.37 | $69.10 | $2,280.38 | 75 |
| CVX | 16 | $146.55 | $148.41 | $2,374.57 | 75 |
| DIS | 18 | $122.90 | $123.51 | $2,223.18 | 75 |
| GOOGL | 13 | $177.82 | $178.59 | $2,321.67 | 70 |
| GS | 3 | $717.52 | $724.12 | $2,172.35 | 85 |
| HD | 6 | $372.64 | $370.77 | $2,224.65 | 70 |
| INTC | 90 | $22.33 | $22.34 | $2,010.15 | 65 |
| JNJ | 13 | $155.80 | $155.79 | $2,025.31 | 65 |
| JPM | 9 | $292.50 | $295.23 | $2,657.07 | 85 |
| KO | 28 | $71.03 | $70.93 | $1,986.04 | 65 |
| LLY | 2 | $776.66 | $776.58 | $1,553.15 | 65 |
| MA | 3 | $561.03 | $567.43 | $1,702.30 | 70 |
| META | 3 | $717.12 | $717.01 | $2,151.03 | 85 |
| MRK | 25 | $82.46 | $81.25 | $2,031.25 | 65 |
| MSFT | 5 | $491.36 | $498.04 | $2,490.18 | 85 |
| NFLX | 1 | $1,279.00 | $1,294.75 | $1,294.75 | 70 |
| NKE | 29 | $75.78 | $75.96 | $2,202.84 | 70 |
| NVDA | 14 | $156.01 | $160.23 | $2,243.22 | 70 |
| ORCL | 9 | $224.73 | $232.43 | $2,091.87 | 70 |
| PEP | 15 | $136.59 | $135.74 | $2,036.10 | 65 |
| PFE | 86 | $25.32 | $25.34 | $2,179.48 | 70 |
| PG | 12 | $160.76 | $160.33 | $1,923.96 | 65 |
| PYPL | 30 | $76.82 | $76.95 | $2,308.65 | 75 |
| QCOM | 14 | $161.41 | $163.16 | $2,284.31 | 70 |
| T | 72 | $28.53 | $28.38 | $2,043.53 | 65 |
| TGT | 20 | $105.04 | $104.36 | $2,087.10 | 65 |
| TSLA | 6 | $313.02 | $315.24 | $1,891.44 | 65 |
| UNH | 7 | $314.75 | $310.14 | $2,170.98 | 65 |
| UNP | 9 | $236.50 | $237.55 | $2,137.93 | 65 |
| V | 6 | $352.90 | $357.81 | $2,146.83 | 70 |
| VZ | 47 | $43.73 | $43.59 | $2,048.50 | 65 |
| WFC | 30 | $82.28 | $83.76 | $2,512.85 | 80 |
| WMT | 22 | $97.34 | $97.89 | $2,153.47 | 70 |
| XOM | 20 | $109.86 | $111.75 | $2,234.90 | 75 |

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
| 2025-07-03 14:40:23 | SELL | NVDA | 2 | $160.31 | $7.52 | 70 |
| 2025-07-03 14:40:23 | SELL | WFC | 1 | $83.73 | $1.41 | 80 |
| 2025-07-03 14:40:23 | BUY | BAC | 2 | $49.05 | N/A | 75 |
| 2025-07-03 14:40:23 | BUY | INTC | 7 | $22.34 | N/A | 65 |
| 2025-07-03 14:40:23 | BUY | WMT | 1 | $97.88 | N/A | 70 |
| 2025-07-03 14:26:03 | SELL | BAC | 8 | $48.94 | $2.14 | 70 |
| 2025-07-03 14:26:03 | BUY | NVDA | 2 | $160.84 | N/A | 85 |
| 2025-07-03 14:26:03 | BUY | PFE | 6 | $25.25 | N/A | 70 |
| 2025-07-03 14:08:35 | SELL | NKE | 5 | $76.23 | $1.92 | 70 |
| 2025-07-03 14:08:35 | SELL | MRK | 2 | $81.92 | $-0.99 | 65 |
| 2025-07-03 14:08:35 | SELL | PFE | 4 | $25.33 | $0.02 | 65 |
| 2025-07-03 14:08:35 | SELL | VZ | 2 | $43.67 | $-0.12 | 65 |
| 2025-07-03 14:08:35 | SELL | T | 5 | $28.35 | $-0.83 | 65 |
| 2025-07-03 14:08:35 | BUY | V | 1 | $356.90 | N/A | 70 |
| 2025-07-03 14:08:35 | BUY | BAC | 6 | $49.19 | N/A | 85 |
| 2025-07-03 13:54:59 | SELL | BAC | 6 | $49.28 | $3.57 | 75 |
| 2025-07-03 13:54:59 | SELL | INTC | 1 | $22.33 | $-0.01 | 60 |
| 2025-07-03 13:54:59 | SELL | WMT | 1 | $97.82 | $0.47 | 65 |
| 2025-07-03 13:54:59 | SELL | MRK | 1 | $81.90 | $-0.50 | 70 |
| 2025-07-03 13:54:59 | SELL | QCOM | 1 | $163.02 | $1.50 | 70 |
| 2025-07-03 13:54:59 | BUY | NKE | 3 | $76.49 | N/A | 85 |
| 2025-07-03 13:54:59 | BUY | DIS | 1 | $123.64 | N/A | 75 |
| 2025-07-03 13:54:59 | BUY | PFE | 4 | $25.41 | N/A | 70 |
| 2025-07-03 13:54:59 | BUY | WFC | 3 | $83.72 | N/A | 85 |
| 2025-07-03 13:54:59 | BUY | CSCO | 1 | $68.79 | N/A | 75 |

<!--TRADE_LOG_END--> 
