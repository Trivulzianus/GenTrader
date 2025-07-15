# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 18:28:16**

| Metric | Value |
|---|---|
| **Total Value** | **$100,695.06** |
| Cash | $159.71 |
| Holdings Value | $100,535.35 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.35 | $2,113.50 | 65 |
| ADBE | 6 | $375.23 | $365.13 | $2,190.78 | 65 |
| AMD | 17 | $146.29 | $155.46 | $2,642.74 | 85 |
| AMZN | 11 | $222.06 | $226.87 | $2,495.57 | 85 |
| AVGO | 8 | $275.34 | $282.09 | $2,256.72 | 70 |
| AXP | 7 | $325.34 | $312.00 | $2,184.00 | 65 |
| BA | 10 | $212.82 | $232.99 | $2,329.90 | 75 |
| BAC | 47 | $46.29 | $46.35 | $2,178.68 | 70 |
| C | 30 | $86.78 | $91.50 | $2,745.00 | 85 |
| CAT | 6 | $397.74 | $405.31 | $2,431.89 | 70 |
| COST | 2 | $979.83 | $968.83 | $1,937.66 | 65 |
| CRM | 8 | $267.44 | $258.22 | $2,065.76 | 65 |
| CSCO | 31 | $68.46 | $67.44 | $2,090.79 | 65 |
| CVX | 16 | $146.78 | $151.39 | $2,422.24 | 75 |
| DIS | 18 | $122.77 | $119.33 | $2,148.03 | 65 |
| GOOGL | 14 | $179.71 | $183.85 | $2,573.90 | 85 |
| GS | 3 | $717.52 | $703.48 | $2,110.45 | 70 |
| HD | 6 | $372.64 | $360.28 | $2,161.68 | 65 |
| INTC | 89 | $22.39 | $23.25 | $2,069.69 | 65 |
| JNJ | 13 | $155.95 | $155.15 | $2,016.89 | 65 |
| JPM | 9 | $291.63 | $286.51 | $2,578.60 | 85 |
| KO | 30 | $70.97 | $69.32 | $2,079.60 | 65 |
| LLY | 3 | $781.32 | $772.50 | $2,317.50 | 65 |
| MA | 4 | $563.08 | $552.66 | $2,210.66 | 65 |
| META | 3 | $717.12 | $716.76 | $2,150.28 | 70 |
| MRK | 25 | $82.54 | $81.40 | $2,035.09 | 65 |
| MSFT | 5 | $498.84 | $507.98 | $2,539.90 | 75 |
| NFLX | 1 | $1,279.00 | $1,257.00 | $1,257.00 | 65 |
| NKE | 29 | $72.04 | $71.78 | $2,081.48 | 65 |
| NVDA | 13 | $171.77 | $170.91 | $2,221.76 | 70 |
| ORCL | 10 | $233.25 | $233.76 | $2,337.65 | 75 |
| PEP | 15 | $136.57 | $134.07 | $2,011.05 | 65 |
| PFE | 87 | $25.23 | $24.59 | $2,138.89 | 70 |
| PG | 14 | $152.15 | $152.58 | $2,136.12 | 65 |
| PYPL | 28 | $72.12 | $73.80 | $2,066.40 | 65 |
| QCOM | 14 | $153.83 | $155.34 | $2,174.70 | 65 |
| T | 77 | $27.09 | $27.05 | $2,082.47 | 65 |
| TGT | 20 | $104.94 | $102.44 | $2,048.90 | 65 |
| TSLA | 6 | $318.51 | $314.98 | $1,889.91 | 60 |
| UNH | 7 | $298.51 | $292.09 | $2,044.63 | 65 |
| UNP | 9 | $236.60 | $232.14 | $2,089.26 | 65 |
| V | 6 | $355.85 | $348.16 | $2,088.96 | 65 |
| VZ | 50 | $43.08 | $41.30 | $2,064.75 | 65 |
| WFC | 27 | $78.89 | $78.19 | $2,111.26 | 65 |
| WMT | 21 | $97.38 | $95.50 | $2,005.61 | 65 |
| XOM | 23 | $110.29 | $113.35 | $2,607.05 | 85 |

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
| 2025-07-15 18:28:07 | SELL | NKE | 2 | $71.78 | $-0.49 | 65 |
| 2025-07-15 18:28:07 | SELL | CVX | 1 | $151.40 | $4.35 | 75 |
| 2025-07-15 18:28:07 | BUY | BAC | 3 | $47.07 | N/A | 70 |
| 2025-07-15 18:28:07 | BUY | XOM | 2 | $113.38 | N/A | 85 |
| 2025-07-15 18:28:07 | BUY | PFE | 4 | $25.35 | N/A | 70 |
| 2025-07-15 18:11:30 | BUY | CVX | 1 | $151.10 | N/A | 85 |
| 2025-07-15 17:51:39 | SELL | WFC | 1 | $78.10 | $-0.77 | 65 |
| 2025-07-15 17:51:39 | SELL | UNP | 1 | $231.92 | $-4.21 | 65 |
| 2025-07-15 17:51:39 | SELL | CVX | 1 | $150.41 | $3.40 | 75 |
| 2025-07-15 17:51:39 | BUY | BAC | 44 | $46.24 | N/A | 65 |
| 2025-07-15 17:51:39 | BUY | NKE | 1 | $71.61 | N/A | 70 |
| 2025-07-15 17:51:17 | SELL | BAC | 45 | $46.24 | $-115.05 | 65 |
| 2025-07-15 17:40:07 | SELL | NVDA | 2 | $170.66 | $-1.93 | 70 |
| 2025-07-15 17:40:07 | SELL | PYPL | 1 | $73.84 | $1.66 | 65 |
| 2025-07-15 17:40:07 | BUY | AMZN | 1 | $226.36 | N/A | 85 |
| 2025-07-15 17:40:07 | BUY | NKE | 1 | $71.86 | N/A | 70 |
| 2025-07-15 17:40:07 | BUY | WFC | 1 | $78.48 | N/A | 70 |
| 2025-07-15 17:40:07 | BUY | UNP | 1 | $232.34 | N/A | 75 |
| 2025-07-15 17:40:07 | BUY | ORCL | 1 | $233.15 | N/A | 75 |
| 2025-07-15 17:40:07 | BUY | CVX | 1 | $150.49 | N/A | 85 |
| 2025-07-15 17:25:36 | SELL | BAC | 3 | $46.31 | $-6.97 | 65 |
| 2025-07-15 17:25:36 | SELL | UNP | 1 | $232.23 | $-3.89 | 65 |
| 2025-07-15 17:25:36 | SELL | CVX | 2 | $150.52 | $6.62 | 75 |
| 2025-07-15 17:25:36 | BUY | NVDA | 2 | $170.62 | N/A | 85 |
| 2025-07-15 17:25:36 | BUY | INTC | 6 | $23.20 | N/A | 65 |

<!--TRADE_LOG_END--> 
