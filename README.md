# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 19:36:54**

| Metric | Value |
|---|---|
| **Total Value** | **$101,473.93** |
| Cash | $75.02 |
| Holdings Value | $101,398.91 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.91 | $2,109.05 | 65 |
| ADBE | 6 | $375.23 | $366.36 | $2,198.16 | 65 |
| AMD | 14 | $160.03 | $159.84 | $2,237.76 | 70 |
| AMZN | 10 | $221.65 | $224.39 | $2,243.90 | 75 |
| AVGO | 8 | $275.34 | $286.00 | $2,288.04 | 65 |
| AXP | 7 | $309.18 | $315.48 | $2,208.36 | 75 |
| BA | 9 | $232.13 | $231.94 | $2,087.46 | 70 |
| BAC | 47 | $46.28 | $47.02 | $2,210.17 | 70 |
| C | 29 | $86.64 | $92.81 | $2,691.63 | 85 |
| CAT | 6 | $397.74 | $418.28 | $2,509.68 | 75 |
| COST | 2 | $979.83 | $951.75 | $1,903.50 | 65 |
| CRM | 8 | $267.44 | $259.51 | $2,076.08 | 65 |
| CSCO | 33 | $68.56 | $68.33 | $2,255.05 | 70 |
| CVX | 17 | $147.11 | $151.74 | $2,579.58 | 85 |
| DIS | 20 | $122.61 | $122.04 | $2,440.80 | 75 |
| GOOGL | 13 | $179.34 | $183.94 | $2,391.16 | 75 |
| GS | 3 | $717.52 | $706.34 | $2,119.01 | 75 |
| HD | 6 | $354.18 | $359.35 | $2,156.07 | 65 |
| INTC | 84 | $22.34 | $22.79 | $1,913.94 | 60 |
| JNJ | 13 | $155.43 | $163.71 | $2,128.23 | 65 |
| JPM | 9 | $291.90 | $289.74 | $2,607.63 | 85 |
| KO | 30 | $70.97 | $70.44 | $2,113.35 | 65 |
| LLY | 3 | $781.32 | $763.42 | $2,290.27 | 65 |
| MA | 4 | $563.08 | $556.87 | $2,227.48 | 65 |
| META | 3 | $717.12 | $701.51 | $2,104.53 | 70 |
| MRK | 29 | $82.56 | $81.71 | $2,369.59 | 75 |
| MSFT | 5 | $498.84 | $512.14 | $2,560.70 | 70 |
| NFLX | 1 | $1,279.00 | $1,273.90 | $1,273.90 | 65 |
| NKE | 31 | $71.96 | $73.02 | $2,263.62 | 70 |
| NVDA | 15 | $171.80 | $173.32 | $2,599.88 | 85 |
| ORCL | 9 | $232.91 | $249.22 | $2,242.98 | 65 |
| PEP | 16 | $136.49 | $145.50 | $2,328.00 | 70 |
| PFE | 84 | $25.28 | $24.57 | $2,064.30 | 65 |
| PG | 14 | $152.18 | $155.44 | $2,176.16 | 65 |
| PYPL | 32 | $72.34 | $73.96 | $2,366.72 | 75 |
| QCOM | 14 | $153.83 | $152.39 | $2,133.46 | 65 |
| T | 76 | $27.10 | $27.00 | $2,051.62 | 65 |
| TGT | 20 | $104.83 | $103.62 | $2,072.40 | 65 |
| TSLA | 6 | $318.51 | $319.10 | $1,914.60 | 65 |
| UNH | 7 | $298.51 | $287.48 | $2,012.36 | 65 |
| UNP | 9 | $237.31 | $227.73 | $2,049.57 | 65 |
| V | 6 | $355.85 | $350.52 | $2,103.12 | 65 |
| VZ | 50 | $40.87 | $41.05 | $2,052.25 | 65 |
| WFC | 28 | $78.77 | $79.70 | $2,231.74 | 70 |
| WMT | 22 | $97.29 | $95.09 | $2,092.09 | 65 |
| XOM | 21 | $109.99 | $111.86 | $2,348.95 | 75 |

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
| 2025-07-17 19:36:48 | SELL | NKE | 1 | $73.03 | $1.04 | 70 |
| 2025-07-17 19:36:48 | SELL | WFC | 1 | $79.74 | $0.93 | 70 |
| 2025-07-17 19:36:48 | BUY | NVDA | 1 | $173.29 | N/A | 85 |
| 2025-07-17 19:36:48 | BUY | BAC | 1 | $47.03 | N/A | 70 |
| 2025-07-17 19:36:48 | BUY | XOM | 2 | $111.86 | N/A | 75 |
| 2025-07-17 19:36:48 | BUY | VZ | 1 | $41.04 | N/A | 65 |
| 2025-07-17 19:36:48 | BUY | CVX | 1 | $151.73 | N/A | 85 |
| 2025-07-17 19:25:18 | SELL | NVDA | 1 | $173.28 | $1.48 | 75 |
| 2025-07-17 19:25:18 | SELL | XOM | 2 | $111.81 | $3.66 | 65 |
| 2025-07-17 19:25:18 | SELL | CSCO | 1 | $68.29 | $-0.27 | 70 |
| 2025-07-17 19:25:18 | BUY | BAC | 2 | $47.01 | N/A | 70 |
| 2025-07-17 19:25:18 | BUY | WFC | 1 | $79.79 | N/A | 75 |
| 2025-07-17 19:25:18 | BUY | VZ | 2 | $41.04 | N/A | 65 |
| 2025-07-17 19:08:19 | SELL | INTC | 5 | $22.80 | $2.13 | 60 |
| 2025-07-17 19:08:19 | SELL | BAC | 2 | $47.15 | $1.78 | 65 |
| 2025-07-17 19:08:19 | SELL | WMT | 1 | $95.40 | $-1.81 | 65 |
| 2025-07-17 19:08:19 | SELL | BA | 1 | $232.16 | $0.04 | 65 |
| 2025-07-17 19:08:19 | SELL | VZ | 3 | $41.06 | $0.58 | 60 |
| 2025-07-17 19:08:19 | BUY | NVDA | 2 | $173.41 | N/A | 85 |
| 2025-07-17 19:08:19 | BUY | NKE | 4 | $73.05 | N/A | 75 |
| 2025-07-17 18:47:04 | SELL | NKE | 4 | $73.06 | $4.28 | 65 |
| 2025-07-17 18:47:04 | SELL | PFE | 1 | $24.54 | $-0.73 | 65 |
| 2025-07-17 18:47:04 | SELL | C | 1 | $92.71 | $5.87 | 85 |
| 2025-07-17 18:47:04 | SELL | UNP | 1 | $227.55 | $-8.78 | 65 |
| 2025-07-17 18:47:04 | SELL | T | 1 | $26.98 | $-0.11 | 65 |

<!--TRADE_LOG_END--> 
