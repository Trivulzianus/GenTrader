# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 22:26:22**

| Metric | Value |
|---|---|
| **Total Value** | **$100,778.09** |
| Cash | $2,432.52 |
| Holdings Value | $98,345.57 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.16 | $2,101.60 | 65 |
| ADBE | 6 | $375.23 | $361.77 | $2,170.62 | 65 |
| AMD | 13 | $160.08 | $160.08 | $2,081.04 | 70 |
| AMZN | 10 | $221.65 | $223.19 | $2,231.90 | 75 |
| AVGO | 8 | $275.34 | $280.81 | $2,246.48 | 70 |
| AXP | 6 | $308.37 | $311.90 | $1,871.40 | 65 |
| BA | 9 | $210.81 | $229.90 | $2,069.10 | 60 |
| BAC | 45 | $46.26 | $46.03 | $2,071.35 | 65 |
| C | 30 | $86.85 | $90.02 | $2,700.60 | 85 |
| CAT | 6 | $397.74 | $412.88 | $2,477.28 | 85 |
| COST | 2 | $979.83 | $951.37 | $1,902.74 | 65 |
| CRM | 8 | $267.44 | $257.95 | $2,063.60 | 65 |
| CSCO | 31 | $68.46 | $67.37 | $2,088.47 | 65 |
| CVX | 16 | $146.83 | $149.92 | $2,398.72 | 75 |
| DIS | 18 | $122.77 | $119.82 | $2,156.76 | 65 |
| GOOGL | 13 | $179.34 | $182.97 | $2,378.61 | 70 |
| GS | 3 | $717.52 | $708.82 | $2,126.46 | 85 |
| HD | 5 | $353.54 | $357.40 | $1,787.00 | 65 |
| INTC | 84 | $22.35 | $22.69 | $1,905.96 | 60 |
| JNJ | 13 | $155.43 | $164.78 | $2,142.14 | 70 |
| JPM | 8 | $292.65 | $285.82 | $2,286.56 | 75 |
| KO | 30 | $70.97 | $69.27 | $2,078.10 | 65 |
| LLY | 3 | $781.32 | $789.80 | $2,369.40 | 85 |
| MA | 4 | $563.08 | $555.52 | $2,222.08 | 65 |
| META | 3 | $717.12 | $702.91 | $2,108.73 | 65 |
| MRK | 29 | $82.56 | $82.43 | $2,390.47 | 75 |
| MSFT | 5 | $498.84 | $505.62 | $2,528.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,250.31 | $1,250.31 | 65 |
| NKE | 30 | $71.98 | $72.10 | $2,163.00 | 70 |
| NVDA | 13 | $171.54 | $171.37 | $2,227.81 | 70 |
| ORCL | 9 | $232.99 | $241.30 | $2,171.70 | 65 |
| PEP | 15 | $136.57 | $135.35 | $2,030.25 | 65 |
| PFE | 84 | $25.28 | $24.61 | $2,067.24 | 65 |
| PG | 13 | $152.06 | $153.73 | $1,998.49 | 65 |
| PYPL | 29 | $72.15 | $72.97 | $2,116.13 | 65 |
| QCOM | 14 | $153.83 | $154.07 | $2,156.98 | 65 |
| T | 77 | $27.10 | $26.95 | $2,075.15 | 65 |
| TGT | 20 | $104.94 | $101.34 | $2,026.80 | 65 |
| TSLA | 6 | $318.51 | $321.67 | $1,930.02 | 65 |
| UNH | 7 | $298.51 | $292.49 | $2,047.43 | 65 |
| UNP | 10 | $236.22 | $231.18 | $2,311.80 | 75 |
| V | 6 | $355.85 | $349.90 | $2,099.40 | 70 |
| VZ | 50 | $43.08 | $41.25 | $2,062.50 | 65 |
| WFC | 29 | $78.86 | $79.91 | $2,317.39 | 75 |
| WMT | 22 | $97.29 | $95.15 | $2,093.30 | 65 |
| XOM | 20 | $109.87 | $112.23 | $2,244.60 | 70 |

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
| 2025-07-16 22:26:12 | SELL | BAC | 3 | $46.03 | $-0.64 | 65 |
| 2025-07-16 22:26:12 | SELL | INTC | 7 | $22.69 | $2.23 | 60 |
| 2025-07-16 22:26:12 | BUY | NKE | 1 | $72.10 | N/A | 70 |
| 2025-07-16 22:26:12 | BUY | UNP | 1 | $231.18 | N/A | 75 |
| 2025-07-16 22:08:20 | SELL | XOM | 1 | $112.23 | $2.25 | 70 |
| 2025-07-16 22:08:20 | SELL | NKE | 3 | $72.10 | $0.34 | 65 |
| 2025-07-16 22:08:20 | BUY | BAC | 3 | $46.03 | N/A | 70 |
| 2025-07-16 22:08:20 | BUY | INTC | 7 | $22.69 | N/A | 65 |
| 2025-07-16 21:51:17 | SELL | CSCO | 2 | $67.37 | $-2.04 | 65 |
| 2025-07-16 21:51:17 | BUY | NKE | 3 | $72.10 | N/A | 75 |
| 2025-07-16 21:51:17 | BUY | WFC | 1 | $79.91 | N/A | 75 |
| 2025-07-16 21:38:15 | SELL | NKE | 3 | $72.10 | $0.34 | 65 |
| 2025-07-16 21:38:15 | SELL | WFC | 1 | $79.91 | $1.05 | 70 |
| 2025-07-16 21:38:15 | SELL | UNP | 1 | $231.18 | $-5.04 | 65 |
| 2025-07-16 21:38:15 | BUY | XOM | 1 | $112.23 | N/A | 75 |
| 2025-07-16 21:38:15 | BUY | CSCO | 2 | $67.37 | N/A | 70 |
| 2025-07-16 21:26:03 | SELL | XOM | 1 | $112.23 | $2.25 | 70 |
| 2025-07-16 21:26:03 | BUY | NKE | 1 | $72.10 | N/A | 75 |
| 2025-07-16 21:26:03 | BUY | WFC | 1 | $79.91 | N/A | 75 |
| 2025-07-16 21:08:30 | SELL | NKE | 2 | $72.10 | $0.22 | 70 |
| 2025-07-16 21:08:30 | SELL | WFC | 1 | $79.91 | $1.05 | 70 |
| 2025-07-16 21:08:30 | SELL | CVX | 2 | $149.92 | $5.50 | 75 |
| 2025-07-16 21:08:30 | SELL | INTC | 7 | $22.69 | $2.23 | 60 |
| 2025-07-16 21:08:30 | BUY | XOM | 1 | $112.23 | N/A | 75 |
| 2025-07-16 21:08:30 | BUY | UNP | 1 | $231.18 | N/A | 75 |

<!--TRADE_LOG_END--> 
