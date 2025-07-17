# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 19:08:24**

| Metric | Value |
|---|---|
| **Total Value** | **$101,498.66** |
| Cash | $349.76 |
| Holdings Value | $101,148.90 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.03 | $2,110.25 | 65 |
| ADBE | 6 | $375.23 | $365.71 | $2,194.26 | 65 |
| AMD | 14 | $160.03 | $159.23 | $2,229.22 | 70 |
| AMZN | 10 | $221.65 | $223.89 | $2,238.90 | 75 |
| AVGO | 8 | $275.34 | $286.37 | $2,290.96 | 65 |
| AXP | 7 | $309.18 | $315.49 | $2,208.43 | 75 |
| BA | 9 | $232.13 | $232.16 | $2,089.49 | 65 |
| BAC | 44 | $46.23 | $47.16 | $2,074.82 | 65 |
| C | 29 | $86.64 | $92.77 | $2,690.33 | 85 |
| CAT | 6 | $397.74 | $419.02 | $2,514.12 | 70 |
| COST | 2 | $979.83 | $952.80 | $1,905.60 | 65 |
| CRM | 8 | $267.44 | $259.15 | $2,073.20 | 65 |
| CSCO | 34 | $68.55 | $68.31 | $2,322.54 | 75 |
| CVX | 16 | $146.82 | $151.47 | $2,423.44 | 75 |
| DIS | 20 | $122.61 | $121.86 | $2,437.20 | 75 |
| GOOGL | 13 | $179.34 | $183.69 | $2,388.03 | 75 |
| GS | 3 | $717.52 | $709.86 | $2,129.57 | 85 |
| HD | 6 | $354.18 | $359.77 | $2,158.62 | 65 |
| INTC | 84 | $22.34 | $22.80 | $1,914.80 | 60 |
| JNJ | 13 | $155.43 | $163.53 | $2,125.95 | 70 |
| JPM | 9 | $291.90 | $290.10 | $2,610.90 | 85 |
| KO | 30 | $70.97 | $70.42 | $2,112.45 | 65 |
| LLY | 3 | $781.32 | $763.63 | $2,290.89 | 65 |
| MA | 4 | $563.08 | $556.40 | $2,225.60 | 65 |
| META | 3 | $717.12 | $702.14 | $2,106.43 | 65 |
| MRK | 29 | $82.56 | $81.70 | $2,369.45 | 75 |
| MSFT | 5 | $498.84 | $511.97 | $2,559.85 | 75 |
| NFLX | 1 | $1,279.00 | $1,274.08 | $1,274.08 | 65 |
| NKE | 32 | $71.99 | $73.05 | $2,337.44 | 75 |
| NVDA | 15 | $171.80 | $173.35 | $2,600.32 | 85 |
| ORCL | 9 | $232.91 | $248.78 | $2,238.97 | 65 |
| PEP | 16 | $136.49 | $145.40 | $2,326.40 | 75 |
| PFE | 84 | $25.28 | $24.58 | $2,064.72 | 65 |
| PG | 14 | $152.18 | $155.30 | $2,174.20 | 65 |
| PYPL | 32 | $72.34 | $74.17 | $2,373.28 | 75 |
| QCOM | 14 | $153.83 | $152.61 | $2,136.54 | 65 |
| T | 76 | $27.10 | $27.02 | $2,053.14 | 65 |
| TGT | 20 | $104.83 | $103.73 | $2,074.70 | 65 |
| TSLA | 6 | $318.51 | $319.07 | $1,914.42 | 65 |
| UNH | 7 | $298.51 | $288.53 | $2,019.71 | 65 |
| UNP | 9 | $237.31 | $227.39 | $2,046.51 | 65 |
| V | 6 | $355.85 | $350.70 | $2,104.20 | 65 |
| VZ | 47 | $40.86 | $41.07 | $1,930.29 | 60 |
| WFC | 28 | $78.77 | $79.94 | $2,238.18 | 70 |
| WMT | 22 | $97.29 | $95.40 | $2,098.80 | 65 |
| XOM | 21 | $109.98 | $111.80 | $2,347.70 | 75 |

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
| 2025-07-17 18:47:04 | BUY | INTC | 5 | $22.82 | N/A | 65 |
| 2025-07-17 18:47:04 | BUY | BAC | 2 | $47.10 | N/A | 70 |
| 2025-07-17 18:47:04 | BUY | WMT | 2 | $95.35 | N/A | 70 |
| 2025-07-17 18:47:04 | BUY | BA | 1 | $232.04 | N/A | 75 |
| 2025-07-17 18:47:04 | BUY | CSCO | 2 | $68.33 | N/A | 75 |
| 2025-07-17 18:28:18 | SELL | NVDA | 2 | $173.20 | $2.86 | 70 |
| 2025-07-17 18:28:18 | SELL | BAC | 1 | $47.17 | $0.91 | 65 |
| 2025-07-17 18:28:18 | SELL | WMT | 1 | $95.37 | $-1.92 | 60 |
| 2025-07-17 18:28:18 | BUY | XOM | 1 | $111.84 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | NKE | 1 | $73.01 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | PYPL | 2 | $73.96 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | BA | 9 | $232.14 | N/A | 70 |
| 2025-07-17 18:28:18 | BUY | CSCO | 1 | $68.31 | N/A | 70 |

<!--TRADE_LOG_END--> 
