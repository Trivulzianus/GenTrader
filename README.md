# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 17:51:46**

| Metric | Value |
|---|---|
| **Total Value** | **$100,622.10** |
| Cash | $485.21 |
| Holdings Value | $100,136.89 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.03 | $2,110.32 | 70 |
| ADBE | 6 | $375.23 | $365.24 | $2,191.44 | 65 |
| AMD | 17 | $146.29 | $155.90 | $2,650.30 | 85 |
| AMZN | 11 | $222.06 | $226.47 | $2,491.17 | 75 |
| AVGO | 8 | $275.34 | $280.86 | $2,246.88 | 65 |
| AXP | 7 | $325.34 | $311.88 | $2,183.12 | 65 |
| BA | 10 | $212.82 | $230.26 | $2,302.60 | 70 |
| BAC | 44 | $46.24 | $46.23 | $2,033.90 | 65 |
| C | 30 | $86.78 | $90.39 | $2,711.70 | 85 |
| CAT | 6 | $397.74 | $403.45 | $2,420.70 | 65 |
| COST | 2 | $979.83 | $971.29 | $1,942.59 | 65 |
| CRM | 8 | $267.44 | $258.84 | $2,070.72 | 65 |
| CSCO | 31 | $68.46 | $67.37 | $2,088.47 | 65 |
| CVX | 16 | $146.80 | $150.50 | $2,408.08 | 75 |
| DIS | 18 | $122.77 | $119.12 | $2,144.25 | 70 |
| GOOGL | 14 | $179.71 | $183.80 | $2,573.20 | 85 |
| GS | 3 | $717.52 | $702.01 | $2,106.03 | 65 |
| HD | 6 | $372.64 | $361.71 | $2,170.26 | 65 |
| INTC | 89 | $22.39 | $23.24 | $2,068.27 | 65 |
| JNJ | 13 | $155.95 | $155.53 | $2,021.83 | 65 |
| JPM | 9 | $291.63 | $286.64 | $2,579.80 | 85 |
| KO | 30 | $70.97 | $69.41 | $2,082.15 | 65 |
| LLY | 3 | $781.32 | $778.00 | $2,334.00 | 65 |
| MA | 4 | $563.08 | $553.04 | $2,212.16 | 65 |
| META | 3 | $717.12 | $716.42 | $2,149.27 | 65 |
| MRK | 25 | $82.54 | $81.62 | $2,040.50 | 65 |
| MSFT | 5 | $498.84 | $507.52 | $2,537.60 | 75 |
| NFLX | 1 | $1,279.00 | $1,258.41 | $1,258.41 | 65 |
| NKE | 31 | $72.02 | $71.67 | $2,221.77 | 70 |
| NVDA | 13 | $171.77 | $170.58 | $2,217.54 | 70 |
| ORCL | 10 | $233.25 | $233.38 | $2,333.80 | 75 |
| PEP | 15 | $136.57 | $134.13 | $2,011.95 | 65 |
| PFE | 83 | $25.22 | $24.72 | $2,051.75 | 65 |
| PG | 14 | $152.15 | $152.75 | $2,138.50 | 65 |
| PYPL | 28 | $72.12 | $73.79 | $2,066.12 | 65 |
| QCOM | 14 | $153.83 | $154.78 | $2,166.92 | 70 |
| T | 77 | $27.09 | $26.97 | $2,076.69 | 65 |
| TGT | 20 | $104.94 | $102.59 | $2,051.80 | 65 |
| TSLA | 6 | $318.51 | $313.88 | $1,883.25 | 65 |
| UNH | 7 | $298.51 | $293.81 | $2,056.67 | 65 |
| UNP | 9 | $236.60 | $231.92 | $2,087.28 | 65 |
| V | 6 | $355.85 | $348.06 | $2,088.39 | 65 |
| VZ | 50 | $43.08 | $41.28 | $2,063.84 | 65 |
| WFC | 27 | $78.89 | $78.11 | $2,108.84 | 65 |
| WMT | 21 | $97.38 | $95.76 | $2,010.93 | 65 |
| XOM | 21 | $109.99 | $112.91 | $2,371.11 | 75 |

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
| 2025-07-15 17:09:19 | SELL | INTC | 6 | $23.23 | $4.98 | 60 |
| 2025-07-15 17:09:19 | BUY | PG | 1 | $152.54 | N/A | 70 |
| 2025-07-15 17:09:19 | BUY | UNP | 1 | $232.19 | N/A | 75 |
| 2025-07-15 17:09:19 | BUY | CVX | 2 | $150.43 | N/A | 85 |
| 2025-07-15 16:57:02 | SELL | NKE | 1 | $71.99 | $-0.05 | 65 |
| 2025-07-15 16:57:02 | SELL | WFC | 1 | $78.58 | $-0.28 | 65 |

<!--TRADE_LOG_END--> 
