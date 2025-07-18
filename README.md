# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 16:44:37**

| Metric | Value |
|---|---|
| **Total Value** | **$101,052.95** |
| Cash | $1,090.73 |
| Holdings Value | $99,962.23 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.74 | $2,117.38 | 65 |
| ADBE | 6 | $375.23 | $364.98 | $2,189.88 | 65 |
| AMD | 14 | $159.84 | $158.19 | $2,214.66 | 70 |
| AMZN | 10 | $221.57 | $225.38 | $2,253.80 | 70 |
| AVGO | 8 | $275.34 | $283.34 | $2,266.72 | 65 |
| AXP | 7 | $309.18 | $306.70 | $2,146.93 | 65 |
| BA | 10 | $232.01 | $228.80 | $2,288.00 | 65 |
| BAC | 51 | $46.35 | $47.26 | $2,410.01 | 75 |
| C | 29 | $86.64 | $93.56 | $2,713.24 | 85 |
| CAT | 6 | $397.74 | $415.08 | $2,490.48 | 85 |
| COST | 2 | $979.83 | $954.97 | $1,909.94 | 65 |
| CRM | 8 | $267.44 | $259.58 | $2,076.64 | 65 |
| CSCO | 33 | $68.56 | $68.24 | $2,251.92 | 70 |
| CVX | 15 | $146.92 | $148.85 | $2,232.75 | 65 |
| DIS | 18 | $122.74 | $121.38 | $2,184.84 | 70 |
| GOOGL | 13 | $179.34 | $184.91 | $2,403.83 | 70 |
| GS | 3 | $717.52 | $707.55 | $2,122.65 | 70 |
| HD | 6 | $354.18 | $357.60 | $2,145.60 | 65 |
| INTC | 84 | $22.33 | $23.25 | $1,953.16 | 60 |
| JNJ | 14 | $155.97 | $164.16 | $2,298.17 | 70 |
| JPM | 8 | $292.14 | $291.76 | $2,334.08 | 70 |
| KO | 30 | $70.96 | $70.27 | $2,107.95 | 65 |
| LLY | 3 | $781.32 | $769.61 | $2,308.82 | 65 |
| MA | 4 | $563.08 | $551.77 | $2,207.08 | 70 |
| META | 3 | $717.12 | $699.97 | $2,099.91 | 70 |
| MRK | 26 | $82.73 | $80.33 | $2,088.58 | 65 |
| MSFT | 5 | $498.84 | $509.25 | $2,546.25 | 75 |
| NFLX | 1 | $1,208.39 | $1,210.42 | $1,210.42 | 65 |
| NKE | 31 | $72.02 | $72.54 | $2,248.75 | 70 |
| NVDA | 14 | $171.92 | $172.25 | $2,411.53 | 70 |
| ORCL | 9 | $232.91 | $246.00 | $2,214.00 | 70 |
| PEP | 15 | $135.89 | $143.95 | $2,159.25 | 65 |
| PFE | 85 | $25.27 | $24.47 | $2,079.95 | 65 |
| PG | 13 | $151.91 | $155.03 | $2,015.45 | 65 |
| PYPL | 29 | $72.18 | $74.02 | $2,146.58 | 65 |
| QCOM | 14 | $153.83 | $154.50 | $2,163.00 | 65 |
| T | 78 | $27.10 | $26.96 | $2,103.27 | 65 |
| TGT | 20 | $104.82 | $102.43 | $2,048.60 | 65 |
| TSLA | 6 | $318.51 | $327.17 | $1,963.02 | 65 |
| UNH | 7 | $283.57 | $282.90 | $1,980.33 | 65 |
| UNP | 9 | $225.02 | $224.09 | $2,016.81 | 65 |
| V | 6 | $355.85 | $348.19 | $2,089.14 | 70 |
| VZ | 51 | $40.87 | $40.82 | $2,081.82 | 65 |
| WFC | 30 | $78.90 | $80.48 | $2,414.40 | 75 |
| WMT | 22 | $97.29 | $95.12 | $2,092.64 | 65 |
| XOM | 20 | $109.90 | $108.00 | $2,160.00 | 70 |

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
| 2025-07-18 16:44:31 | SELL | INTC | 6 | $23.25 | $5.17 | 60 |
| 2025-07-18 16:44:31 | SELL | KO | 2 | $70.26 | $-1.31 | 65 |
| 2025-07-18 16:44:31 | SELL | CVX | 2 | $148.85 | $3.40 | 65 |
| 2025-07-18 16:44:31 | BUY | PFE | 5 | $24.48 | N/A | 65 |
| 2025-07-18 16:44:31 | BUY | WFC | 2 | $80.48 | N/A | 75 |
| 2025-07-18 16:44:31 | BUY | NKE | 2 | $72.54 | N/A | 70 |
| 2025-07-18 16:27:10 | SELL | NVDA | 1 | $172.01 | $0.08 | 70 |
| 2025-07-18 16:27:10 | SELL | PFE | 5 | $24.42 | $-4.21 | 60 |
| 2025-07-18 16:27:10 | BUY | KO | 2 | $70.18 | N/A | 70 |
| 2025-07-18 16:27:10 | BUY | INTC | 7 | $23.18 | N/A | 65 |
| 2025-07-18 16:27:10 | BUY | WFC | 2 | $80.35 | N/A | 70 |
| 2025-07-18 16:27:10 | BUY | VZ | 3 | $40.83 | N/A | 65 |
| 2025-07-18 16:10:58 | SELL | AMZN | 1 | $225.05 | $3.16 | 70 |
| 2025-07-18 16:10:58 | SELL | NKE | 2 | $72.50 | $0.98 | 65 |
| 2025-07-18 16:10:58 | SELL | WFC | 1 | $80.27 | $1.55 | 65 |
| 2025-07-18 16:10:58 | SELL | VZ | 3 | $40.84 | $-0.08 | 60 |
| 2025-07-18 15:53:05 | SELL | INTC | 7 | $23.44 | $7.19 | 60 |
| 2025-07-18 15:53:05 | SELL | CVX | 1 | $150.71 | $3.36 | 75 |
| 2025-07-18 15:53:05 | BUY | NVDA | 2 | $172.51 | N/A | 85 |
| 2025-07-18 15:53:05 | BUY | UNH | 7 | $283.57 | N/A | 65 |
| 2025-07-18 15:53:05 | BUY | NKE | 2 | $72.36 | N/A | 70 |
| 2025-07-18 15:53:05 | BUY | CSCO | 2 | $68.33 | N/A | 70 |
| 2025-07-18 15:52:44 | SELL | UNH | 7 | $283.57 | $-104.53 | 65 |
| 2025-07-18 15:39:48 | SELL | NKE | 1 | $72.44 | $0.43 | 65 |
| 2025-07-18 15:39:48 | SELL | T | 5 | $26.97 | $-0.65 | 65 |

<!--TRADE_LOG_END--> 
