# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 14:26:18**

| Metric | Value |
|---|---|
| **Total Value** | **$101,069.58** |
| Cash | $1,315.43 |
| Holdings Value | $99,754.16 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.96 | $2,099.60 | 65 |
| ADBE | 6 | $375.23 | $364.11 | $2,184.63 | 65 |
| AMD | 13 | $160.00 | $157.15 | $2,042.95 | 65 |
| AMZN | 11 | $221.89 | $223.34 | $2,456.74 | 75 |
| AVGO | 8 | $275.34 | $282.91 | $2,263.28 | 70 |
| AXP | 7 | $309.18 | $303.43 | $2,124.01 | 65 |
| BA | 10 | $232.01 | $229.63 | $2,296.30 | 65 |
| BAC | 48 | $46.30 | $46.98 | $2,255.28 | 70 |
| C | 29 | $86.64 | $92.79 | $2,690.77 | 85 |
| CAT | 6 | $397.74 | $415.68 | $2,494.08 | 85 |
| COST | 2 | $979.83 | $959.40 | $1,918.80 | 70 |
| CRM | 8 | $267.44 | $259.74 | $2,077.92 | 65 |
| CSCO | 31 | $68.57 | $68.44 | $2,121.49 | 65 |
| CVX | 16 | $146.84 | $152.22 | $2,435.52 | 75 |
| DIS | 18 | $122.74 | $120.86 | $2,175.48 | 70 |
| GOOGL | 13 | $179.34 | $184.22 | $2,394.80 | 70 |
| GS | 3 | $717.52 | $701.26 | $2,103.78 | 70 |
| HD | 6 | $354.18 | $358.01 | $2,148.06 | 65 |
| INTC | 84 | $22.34 | $22.91 | $1,924.86 | 60 |
| JNJ | 14 | $155.97 | $164.83 | $2,307.62 | 70 |
| JPM | 8 | $292.14 | $289.86 | $2,318.88 | 70 |
| KO | 31 | $70.95 | $70.67 | $2,190.62 | 70 |
| LLY | 3 | $781.32 | $773.43 | $2,320.29 | 65 |
| MA | 4 | $563.08 | $552.59 | $2,210.34 | 65 |
| META | 3 | $717.12 | $693.20 | $2,079.60 | 75 |
| MRK | 29 | $82.56 | $81.26 | $2,356.54 | 75 |
| MSFT | 5 | $498.84 | $510.57 | $2,552.85 | 85 |
| NFLX | 1 | $1,208.39 | $1,212.25 | $1,212.25 | 65 |
| NKE | 29 | $71.98 | $72.25 | $2,095.39 | 65 |
| NVDA | 15 | $171.89 | $172.13 | $2,581.95 | 85 |
| ORCL | 9 | $232.91 | $247.09 | $2,223.86 | 70 |
| PEP | 15 | $135.89 | $145.25 | $2,178.74 | 65 |
| PFE | 79 | $25.32 | $24.57 | $1,940.65 | 60 |
| PG | 13 | $151.91 | $155.37 | $2,019.81 | 65 |
| PYPL | 29 | $72.18 | $73.32 | $2,126.28 | 65 |
| QCOM | 14 | $153.83 | $152.97 | $2,141.51 | 65 |
| T | 78 | $27.10 | $27.00 | $2,106.37 | 65 |
| TGT | 20 | $104.82 | $103.62 | $2,072.40 | 65 |
| TSLA | 6 | $318.51 | $326.90 | $1,961.40 | 65 |
| UNH | 7 | $298.51 | $283.89 | $1,987.26 | 65 |
| UNP | 9 | $225.02 | $224.58 | $2,021.22 | 65 |
| V | 6 | $355.85 | $348.55 | $2,091.27 | 65 |
| VZ | 51 | $40.87 | $41.07 | $2,094.57 | 65 |
| WFC | 27 | $78.73 | $79.70 | $2,151.90 | 65 |
| WMT | 22 | $97.29 | $95.42 | $2,099.13 | 65 |
| XOM | 19 | $109.80 | $110.69 | $2,103.11 | 65 |

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
| 2025-07-18 14:26:10 | SELL | NKE | 1 | $72.27 | $0.28 | 65 |
| 2025-07-18 14:26:10 | SELL | PFE | 6 | $24.58 | $-4.18 | 60 |
| 2025-07-18 14:26:10 | BUY | NVDA | 1 | $173.00 | N/A | 85 |
| 2025-07-18 14:26:10 | BUY | KO | 1 | $70.65 | N/A | 70 |
| 2025-07-18 14:09:21 | SELL | NVDA | 1 | $173.35 | $1.44 | 70 |
| 2025-07-18 14:09:21 | SELL | KO | 1 | $70.61 | $-0.35 | 65 |
| 2025-07-18 14:09:21 | SELL | DIS | 1 | $120.96 | $-1.68 | 65 |
| 2025-07-18 14:09:21 | SELL | NKE | 3 | $72.34 | $0.95 | 65 |
| 2025-07-18 14:09:21 | SELL | CSCO | 2 | $68.51 | $-0.11 | 65 |
| 2025-07-18 14:09:21 | BUY | NFLX | 1 | $1,208.39 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | PFE | 1 | $24.62 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | UNP | 9 | $225.02 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | TGT | 1 | $103.78 | N/A | 65 |
| 2025-07-18 14:08:57 | SELL | UNP | 9 | $225.04 | $-110.44 | 65 |
| 2025-07-18 14:08:51 | SELL | NFLX | 1 | $1,207.30 | $-71.70 | 65 |
| 2025-07-18 13:49:22 | SELL | WFC | 2 | $79.81 | $2.01 | 65 |
| 2025-07-18 13:49:22 | SELL | T | 5 | $26.84 | $-1.21 | 65 |
| 2025-07-18 13:49:22 | SELL | TGT | 1 | $103.98 | $-0.85 | 60 |
| 2025-07-18 13:49:22 | BUY | NVDA | 2 | $173.85 | N/A | 85 |
| 2025-07-18 13:49:22 | BUY | KO | 1 | $70.39 | N/A | 70 |
| 2025-07-18 13:49:22 | BUY | MRK | 1 | $81.42 | N/A | 75 |
| 2025-07-18 13:49:22 | BUY | NKE | 4 | $72.58 | N/A | 75 |
| 2025-07-18 13:29:45 | SELL | JPM | 1 | $289.90 | $-2.00 | 70 |
| 2025-07-18 13:29:45 | SELL | KO | 2 | $70.59 | $-0.71 | 65 |
| 2025-07-18 13:29:45 | SELL | PYPL | 3 | $73.86 | $4.56 | 65 |

<!--TRADE_LOG_END--> 
