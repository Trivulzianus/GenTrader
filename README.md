# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 15:53:11**

| Metric | Value |
|---|---|
| **Total Value** | **$101,193.71** |
| Cash | $660.27 |
| Holdings Value | $100,533.45 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.99 | $2,109.90 | 65 |
| ADBE | 6 | $375.23 | $365.55 | $2,193.27 | 65 |
| AMD | 14 | $159.84 | $158.38 | $2,217.32 | 70 |
| AMZN | 11 | $221.89 | $225.13 | $2,476.47 | 70 |
| AVGO | 8 | $275.34 | $283.25 | $2,266.00 | 70 |
| AXP | 7 | $309.18 | $307.02 | $2,149.14 | 65 |
| BA | 10 | $232.01 | $228.97 | $2,289.65 | 70 |
| BAC | 51 | $46.35 | $47.15 | $2,404.39 | 75 |
| C | 29 | $86.64 | $93.39 | $2,708.16 | 85 |
| CAT | 6 | $397.74 | $415.90 | $2,495.40 | 85 |
| COST | 2 | $979.83 | $954.83 | $1,909.65 | 65 |
| CRM | 8 | $267.44 | $260.39 | $2,083.12 | 65 |
| CSCO | 33 | $68.56 | $68.33 | $2,254.89 | 70 |
| CVX | 17 | $147.15 | $150.66 | $2,561.22 | 75 |
| DIS | 18 | $122.74 | $121.11 | $2,179.98 | 70 |
| GOOGL | 13 | $179.34 | $185.48 | $2,411.24 | 70 |
| GS | 3 | $717.52 | $709.08 | $2,127.24 | 80 |
| HD | 6 | $354.18 | $357.89 | $2,147.36 | 65 |
| INTC | 83 | $22.32 | $23.43 | $1,944.81 | 60 |
| JNJ | 14 | $155.97 | $164.44 | $2,302.09 | 70 |
| JPM | 8 | $292.14 | $291.75 | $2,334.00 | 70 |
| KO | 30 | $70.97 | $70.28 | $2,108.55 | 65 |
| LLY | 3 | $781.32 | $772.92 | $2,318.76 | 65 |
| MA | 4 | $563.08 | $552.45 | $2,209.80 | 65 |
| META | 3 | $717.12 | $700.45 | $2,101.35 | 65 |
| MRK | 26 | $82.73 | $80.86 | $2,102.36 | 65 |
| MSFT | 5 | $498.84 | $509.85 | $2,549.25 | 70 |
| NFLX | 1 | $1,208.39 | $1,213.41 | $1,213.41 | 65 |
| NKE | 31 | $72.02 | $72.47 | $2,246.41 | 70 |
| NVDA | 15 | $171.93 | $172.38 | $2,585.62 | 85 |
| ORCL | 9 | $232.91 | $246.66 | $2,219.99 | 65 |
| PEP | 15 | $135.89 | $144.18 | $2,162.70 | 65 |
| PFE | 85 | $25.27 | $24.53 | $2,085.28 | 65 |
| PG | 13 | $151.91 | $155.21 | $2,017.73 | 65 |
| PYPL | 29 | $72.18 | $73.89 | $2,142.81 | 65 |
| QCOM | 14 | $153.83 | $154.84 | $2,167.76 | 65 |
| T | 78 | $27.10 | $26.95 | $2,101.71 | 65 |
| TGT | 20 | $104.82 | $102.60 | $2,052.00 | 65 |
| TSLA | 6 | $318.51 | $328.17 | $1,969.02 | 65 |
| UNH | 7 | $283.57 | $283.91 | $1,987.36 | 65 |
| UNP | 9 | $225.02 | $223.84 | $2,014.52 | 65 |
| V | 6 | $355.85 | $348.51 | $2,091.06 | 70 |
| VZ | 51 | $40.87 | $40.85 | $2,083.61 | 65 |
| WFC | 27 | $78.72 | $80.22 | $2,165.81 | 65 |
| WMT | 22 | $97.29 | $95.04 | $2,090.88 | 65 |
| XOM | 20 | $109.90 | $109.02 | $2,180.40 | 65 |

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
| 2025-07-18 15:53:05 | SELL | INTC | 7 | $23.44 | $7.19 | 60 |
| 2025-07-18 15:53:05 | SELL | CVX | 1 | $150.71 | $3.36 | 75 |
| 2025-07-18 15:53:05 | BUY | NVDA | 2 | $172.51 | N/A | 85 |
| 2025-07-18 15:53:05 | BUY | UNH | 7 | $283.57 | N/A | 65 |
| 2025-07-18 15:53:05 | BUY | NKE | 2 | $72.36 | N/A | 70 |
| 2025-07-18 15:53:05 | BUY | CSCO | 2 | $68.33 | N/A | 70 |
| 2025-07-18 15:52:44 | SELL | UNH | 7 | $283.57 | $-104.53 | 65 |
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

<!--TRADE_LOG_END--> 
