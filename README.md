# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 15:40:25**

| Metric | Value |
|---|---|
| **Total Value** | **$100,698.54** |
| Cash | $1,547.61 |
| Holdings Value | $99,150.93 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.60 | $2,116.05 | 65 |
| ADBE | 6 | $375.23 | $365.53 | $2,193.18 | 65 |
| AMD | 17 | $146.29 | $155.41 | $2,641.98 | 85 |
| AMZN | 10 | $221.60 | $226.63 | $2,266.30 | 75 |
| AVGO | 8 | $275.34 | $281.50 | $2,252.00 | 65 |
| AXP | 7 | $325.34 | $314.04 | $2,198.28 | 70 |
| BA | 9 | $210.77 | $230.41 | $2,073.69 | 65 |
| BAC | 47 | $48.69 | $46.65 | $2,192.46 | 70 |
| C | 30 | $86.78 | $90.22 | $2,706.60 | 85 |
| CAT | 6 | $397.74 | $406.96 | $2,441.76 | 85 |
| COST | 2 | $979.83 | $967.16 | $1,934.33 | 65 |
| CRM | 8 | $267.44 | $259.21 | $2,073.72 | 65 |
| CSCO | 31 | $68.46 | $67.50 | $2,092.35 | 65 |
| CVX | 16 | $146.80 | $151.13 | $2,418.08 | 75 |
| DIS | 17 | $122.96 | $119.01 | $2,023.17 | 65 |
| GOOGL | 14 | $179.71 | $183.49 | $2,568.86 | 85 |
| GS | 3 | $717.52 | $706.18 | $2,118.55 | 75 |
| HD | 6 | $372.64 | $364.19 | $2,185.17 | 65 |
| INTC | 82 | $22.31 | $23.36 | $1,915.93 | 60 |
| JNJ | 13 | $155.95 | $154.90 | $2,013.64 | 65 |
| JPM | 9 | $291.63 | $287.76 | $2,589.84 | 85 |
| KO | 30 | $70.97 | $69.15 | $2,074.50 | 65 |
| LLY | 3 | $781.32 | $771.84 | $2,315.52 | 65 |
| MA | 4 | $563.08 | $549.95 | $2,199.80 | 65 |
| META | 3 | $717.12 | $717.73 | $2,153.19 | 70 |
| MRK | 25 | $82.54 | $81.47 | $2,036.62 | 65 |
| MSFT | 5 | $498.84 | $506.64 | $2,533.22 | 85 |
| NFLX | 1 | $1,279.00 | $1,259.63 | $1,259.63 | 65 |
| NKE | 29 | $72.03 | $72.13 | $2,091.77 | 65 |
| NVDA | 13 | $171.78 | $171.29 | $2,226.84 | 70 |
| ORCL | 9 | $233.27 | $231.56 | $2,084.09 | 65 |
| PEP | 15 | $136.57 | $133.89 | $2,008.35 | 65 |
| PFE | 83 | $25.22 | $24.71 | $2,051.09 | 65 |
| PG | 13 | $152.12 | $152.44 | $1,981.72 | 65 |
| PYPL | 29 | $72.19 | $73.65 | $2,135.85 | 65 |
| QCOM | 14 | $153.83 | $154.88 | $2,168.25 | 70 |
| T | 77 | $27.10 | $26.82 | $2,064.97 | 65 |
| TGT | 20 | $104.94 | $103.41 | $2,068.26 | 65 |
| TSLA | 6 | $318.51 | $314.22 | $1,885.35 | 65 |
| UNH | 7 | $298.51 | $293.94 | $2,057.56 | 65 |
| UNP | 9 | $236.54 | $232.81 | $2,095.31 | 65 |
| V | 6 | $355.85 | $347.51 | $2,085.04 | 70 |
| VZ | 50 | $43.08 | $41.11 | $2,055.50 | 65 |
| WFC | 27 | $78.71 | $78.89 | $2,130.16 | 65 |
| WMT | 21 | $97.38 | $95.10 | $1,997.10 | 65 |
| XOM | 21 | $109.99 | $113.11 | $2,375.31 | 75 |

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
| 2025-07-15 15:40:17 | SELL | NVDA | 1 | $171.33 | $-0.42 | 70 |
| 2025-07-15 15:40:17 | SELL | INTC | 6 | $23.37 | $5.90 | 60 |
| 2025-07-15 15:40:17 | SELL | PYPL | 1 | $73.64 | $1.41 | 65 |
| 2025-07-15 15:40:17 | SELL | WFC | 1 | $78.91 | $0.19 | 65 |
| 2025-07-15 15:40:17 | BUY | GOOGL | 1 | $183.45 | N/A | 85 |
| 2025-07-15 15:40:17 | BUY | BAC | 3 | $46.65 | N/A | 70 |
| 2025-07-15 15:26:50 | SELL | GOOGL | 1 | $183.84 | $4.10 | 75 |
| 2025-07-15 15:26:50 | SELL | NKE | 2 | $72.35 | $0.59 | 65 |
| 2025-07-15 15:26:50 | SELL | UNP | 1 | $232.75 | $-3.41 | 65 |
| 2025-07-15 15:26:50 | BUY | INTC | 5 | $23.38 | N/A | 65 |
| 2025-07-15 15:26:50 | BUY | PYPL | 1 | $73.56 | N/A | 70 |
| 2025-07-15 15:26:50 | BUY | WFC | 28 | $78.72 | N/A | 70 |
| 2025-07-15 15:26:26 | SELL | WFC | 27 | $78.75 | $-112.80 | 65 |
| 2025-07-15 15:08:18 | SELL | CVX | 2 | $151.18 | $7.79 | 75 |
| 2025-07-15 15:08:18 | BUY | AMD | 1 | $155.67 | N/A | 85 |
| 2025-07-15 15:08:18 | BUY | C | 3 | $89.11 | N/A | 85 |
| 2025-07-15 15:08:18 | BUY | UNP | 1 | $232.60 | N/A | 75 |
| 2025-07-15 14:52:34 | SELL | NVDA | 1 | $171.28 | $-0.44 | 70 |
| 2025-07-15 14:52:34 | SELL | INTC | 5 | $23.39 | $5.02 | 60 |
| 2025-07-15 14:52:34 | SELL | WFC | 1 | $78.90 | $-3.87 | 65 |
| 2025-07-15 14:52:34 | SELL | C | 3 | $89.18 | $7.17 | 75 |
| 2025-07-15 14:52:34 | BUY | AMD | 1 | $146.24 | N/A | 75 |
| 2025-07-15 14:52:34 | BUY | CRM | 1 | $258.71 | N/A | 65 |
| 2025-07-15 14:52:34 | BUY | KO | 1 | $69.33 | N/A | 65 |
| 2025-07-15 14:52:34 | BUY | NKE | 1 | $72.17 | N/A | 70 |

<!--TRADE_LOG_END--> 
