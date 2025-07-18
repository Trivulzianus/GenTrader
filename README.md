# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 15:39:54**

| Metric | Value |
|---|---|
| **Total Value** | **$101,147.19** |
| Cash | $971.90 |
| Holdings Value | $100,175.29 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.90 | $2,108.95 | 65 |
| ADBE | 6 | $375.23 | $365.03 | $2,190.18 | 65 |
| AMD | 14 | $159.84 | $157.88 | $2,210.32 | 70 |
| AMZN | 11 | $221.89 | $224.79 | $2,472.70 | 75 |
| AVGO | 8 | $275.34 | $282.12 | $2,256.96 | 70 |
| AXP | 7 | $309.18 | $306.60 | $2,146.20 | 65 |
| BA | 10 | $232.01 | $229.15 | $2,291.50 | 70 |
| BAC | 51 | $46.35 | $47.12 | $2,403.12 | 75 |
| C | 29 | $86.64 | $93.32 | $2,706.31 | 85 |
| CAT | 6 | $397.74 | $414.82 | $2,488.92 | 65 |
| COST | 2 | $979.83 | $956.65 | $1,913.30 | 65 |
| CRM | 8 | $267.44 | $259.74 | $2,077.88 | 65 |
| CSCO | 31 | $68.58 | $68.28 | $2,116.84 | 65 |
| CVX | 18 | $147.35 | $150.89 | $2,716.02 | 85 |
| DIS | 18 | $122.74 | $120.95 | $2,177.10 | 65 |
| GOOGL | 13 | $179.34 | $185.10 | $2,406.30 | 70 |
| GS | 3 | $717.52 | $708.42 | $2,125.26 | 85 |
| HD | 6 | $354.18 | $357.81 | $2,146.86 | 65 |
| INTC | 90 | $22.41 | $23.43 | $2,108.25 | 65 |
| JNJ | 14 | $155.97 | $164.74 | $2,306.36 | 70 |
| JPM | 8 | $292.14 | $291.38 | $2,331.00 | 70 |
| KO | 30 | $70.97 | $70.41 | $2,112.15 | 65 |
| LLY | 3 | $781.32 | $773.29 | $2,319.87 | 65 |
| MA | 4 | $563.08 | $552.78 | $2,211.12 | 65 |
| META | 3 | $717.12 | $698.32 | $2,094.96 | 70 |
| MRK | 26 | $82.73 | $80.92 | $2,103.92 | 65 |
| MSFT | 5 | $498.84 | $510.62 | $2,553.09 | 85 |
| NFLX | 1 | $1,208.39 | $1,216.58 | $1,216.58 | 65 |
| NKE | 29 | $71.99 | $72.42 | $2,100.32 | 65 |
| NVDA | 13 | $171.84 | $172.26 | $2,239.38 | 70 |
| ORCL | 9 | $232.91 | $246.18 | $2,215.62 | 70 |
| PEP | 15 | $135.89 | $144.32 | $2,164.80 | 65 |
| PFE | 85 | $25.27 | $24.51 | $2,083.35 | 65 |
| PG | 13 | $151.91 | $155.46 | $2,020.98 | 65 |
| PYPL | 29 | $72.18 | $73.82 | $2,140.78 | 65 |
| QCOM | 14 | $153.83 | $154.71 | $2,165.87 | 65 |
| T | 78 | $27.10 | $26.96 | $2,103.27 | 65 |
| TGT | 20 | $104.82 | $102.58 | $2,051.60 | 65 |
| TSLA | 6 | $318.51 | $328.09 | $1,968.54 | 65 |
| UNH | 7 | $298.51 | $283.61 | $1,985.27 | 65 |
| UNP | 9 | $225.02 | $223.31 | $2,009.79 | 65 |
| V | 6 | $355.85 | $348.79 | $2,092.74 | 70 |
| VZ | 51 | $40.87 | $40.88 | $2,084.88 | 65 |
| WFC | 27 | $78.72 | $80.13 | $2,163.51 | 65 |
| WMT | 22 | $97.29 | $95.23 | $2,095.17 | 65 |
| XOM | 20 | $109.90 | $108.87 | $2,177.40 | 65 |

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
| 2025-07-18 15:39:48 | SELL | NKE | 1 | $72.44 | $0.43 | 65 |
| 2025-07-18 15:39:48 | SELL | T | 5 | $26.97 | $-0.65 | 65 |
| 2025-07-18 15:39:48 | SELL | CSCO | 2 | $68.29 | $-0.55 | 65 |
| 2025-07-18 15:39:48 | BUY | BAC | 6 | $47.12 | N/A | 75 |
| 2025-07-18 15:39:48 | BUY | CVX | 1 | $150.86 | N/A | 85 |
| 2025-07-18 15:26:20 | SELL | BAC | 3 | $47.08 | $2.33 | 65 |
| 2025-07-18 15:26:20 | SELL | NKE | 3 | $72.32 | $0.86 | 65 |
| 2025-07-18 15:26:20 | SELL | KO | 4 | $70.38 | $-2.08 | 65 |
| 2025-07-18 15:26:20 | BUY | T | 5 | $26.98 | N/A | 70 |
| 2025-07-18 15:08:54 | SELL | WFC | 1 | $80.03 | $1.26 | 65 |
| 2025-07-18 15:08:54 | SELL | CVX | 1 | $150.64 | $3.31 | 75 |
| 2025-07-18 15:08:54 | BUY | BAC | 1 | $47.13 | N/A | 70 |
| 2025-07-18 15:08:54 | BUY | INTC | 1 | $23.39 | N/A | 65 |
| 2025-07-18 15:08:54 | BUY | KO | 4 | $70.37 | N/A | 75 |
| 2025-07-18 15:08:54 | BUY | NKE | 4 | $72.42 | N/A | 75 |
| 2025-07-18 14:53:25 | SELL | NVDA | 1 | $172.34 | $0.46 | 70 |
| 2025-07-18 14:53:25 | SELL | CSCO | 2 | $68.38 | $-0.35 | 70 |
| 2025-07-18 14:53:25 | BUY | BAC | 2 | $47.15 | N/A | 70 |
| 2025-07-18 14:53:25 | BUY | INTC | 5 | $23.30 | N/A | 65 |
| 2025-07-18 14:53:25 | BUY | WFC | 1 | $79.94 | N/A | 70 |
| 2025-07-18 14:40:53 | SELL | NVDA | 1 | $172.07 | $0.18 | 70 |
| 2025-07-18 14:40:53 | SELL | BAC | 3 | $47.08 | $2.34 | 65 |
| 2025-07-18 14:40:53 | SELL | KO | 1 | $70.44 | $-0.51 | 65 |
| 2025-07-18 14:40:53 | SELL | MRK | 3 | $81.06 | $-4.49 | 65 |
| 2025-07-18 14:40:53 | BUY | AMD | 1 | $157.83 | N/A | 70 |

<!--TRADE_LOG_END--> 
