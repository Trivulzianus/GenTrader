# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 14:41:04**

| Metric | Value |
|---|---|
| **Total Value** | **$100,423.67** |
| Cash | $1,146.93 |
| Holdings Value | $99,276.74 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.33 | $2,113.30 | 65 |
| ADBE | 6 | $375.23 | $361.15 | $2,166.93 | 65 |
| AMD | 14 | $144.36 | $154.88 | $2,168.32 | 70 |
| AMZN | 10 | $221.65 | $225.43 | $2,254.30 | 75 |
| AVGO | 8 | $275.34 | $278.88 | $2,231.08 | 70 |
| AXP | 7 | $325.34 | $310.09 | $2,170.63 | 65 |
| BA | 9 | $210.81 | $228.95 | $2,060.55 | 65 |
| BAC | 45 | $46.28 | $45.49 | $2,047.27 | 65 |
| C | 30 | $86.78 | $89.59 | $2,687.70 | 85 |
| CAT | 6 | $397.74 | $406.88 | $2,441.31 | 70 |
| COST | 2 | $979.83 | $958.65 | $1,917.30 | 65 |
| CRM | 8 | $267.44 | $256.46 | $2,051.68 | 65 |
| CSCO | 31 | $68.46 | $67.47 | $2,091.72 | 65 |
| CVX | 16 | $146.76 | $149.61 | $2,393.76 | 75 |
| DIS | 18 | $122.77 | $119.92 | $2,158.65 | 65 |
| GOOGL | 14 | $179.71 | $183.70 | $2,571.80 | 75 |
| GS | 3 | $717.52 | $696.59 | $2,089.77 | 85 |
| HD | 6 | $372.64 | $357.38 | $2,144.28 | 65 |
| INTC | 84 | $22.36 | $22.73 | $1,908.90 | 60 |
| JNJ | 13 | $155.43 | $163.87 | $2,130.24 | 65 |
| JPM | 9 | $291.63 | $286.05 | $2,574.45 | 80 |
| KO | 30 | $70.97 | $69.11 | $2,073.30 | 65 |
| LLY | 3 | $781.32 | $788.21 | $2,364.63 | 70 |
| MA | 4 | $563.08 | $553.38 | $2,213.52 | 65 |
| META | 3 | $717.12 | $707.84 | $2,123.52 | 75 |
| MRK | 29 | $82.47 | $82.35 | $2,388.15 | 75 |
| MSFT | 5 | $498.84 | $503.91 | $2,519.55 | 75 |
| NFLX | 1 | $1,279.00 | $1,260.89 | $1,260.89 | 65 |
| NKE | 29 | $72.03 | $71.82 | $2,082.78 | 65 |
| NVDA | 14 | $171.58 | $170.09 | $2,381.19 | 70 |
| ORCL | 10 | $233.28 | $234.44 | $2,344.38 | 75 |
| PEP | 15 | $136.57 | $134.09 | $2,011.35 | 65 |
| PFE | 83 | $25.29 | $24.82 | $2,060.45 | 65 |
| PG | 14 | $152.15 | $152.99 | $2,141.86 | 65 |
| PYPL | 29 | $72.15 | $71.99 | $2,087.71 | 65 |
| QCOM | 14 | $153.83 | $153.54 | $2,149.56 | 65 |
| T | 77 | $27.09 | $26.98 | $2,077.84 | 65 |
| TGT | 20 | $104.94 | $101.48 | $2,029.66 | 65 |
| TSLA | 6 | $318.51 | $319.29 | $1,915.71 | 65 |
| UNH | 7 | $298.51 | $292.84 | $2,049.88 | 65 |
| UNP | 9 | $236.78 | $230.73 | $2,076.57 | 65 |
| V | 6 | $355.85 | $348.24 | $2,089.44 | 65 |
| VZ | 50 | $43.08 | $41.28 | $2,064.00 | 65 |
| WFC | 26 | $78.81 | $79.13 | $2,057.32 | 65 |
| WMT | 22 | $97.29 | $95.16 | $2,093.52 | 65 |
| XOM | 20 | $109.86 | $112.30 | $2,246.00 | 70 |

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
| 2025-07-16 14:40:59 | SELL | NVDA | 1 | $170.23 | $-1.26 | 70 |
| 2025-07-16 14:40:59 | BUY | ORCL | 1 | $234.45 | N/A | 75 |
| 2025-07-16 14:26:09 | SELL | XOM | 1 | $112.84 | $2.84 | 70 |
| 2025-07-16 14:26:09 | SELL | NKE | 1 | $72.13 | $0.10 | 65 |
| 2025-07-16 14:26:09 | BUY | NVDA | 1 | $169.74 | N/A | 85 |
| 2025-07-16 14:08:31 | SELL | INTC | 7 | $22.69 | $2.16 | 60 |
| 2025-07-16 14:08:31 | SELL | AMD | 1 | $154.68 | $9.64 | 65 |
| 2025-07-16 14:08:31 | SELL | PFE | 1 | $24.86 | $-0.42 | 65 |
| 2025-07-16 14:08:31 | SELL | WFC | 1 | $79.43 | $0.60 | 65 |
| 2025-07-16 14:08:31 | SELL | UNP | 1 | $230.54 | $-5.61 | 65 |
| 2025-07-16 14:08:31 | BUY | XOM | 1 | $112.48 | N/A | 75 |
| 2025-07-16 14:08:31 | BUY | NKE | 1 | $72.00 | N/A | 70 |
| 2025-07-16 13:50:09 | SELL | NVDA | 1 | $170.74 | $-0.81 | 70 |
| 2025-07-16 13:50:09 | SELL | JNJ | 1 | $161.91 | $6.02 | 65 |
| 2025-07-16 13:50:09 | SELL | XOM | 1 | $112.87 | $2.85 | 70 |
| 2025-07-16 13:50:09 | SELL | PFE | 1 | $24.92 | $-0.36 | 65 |
| 2025-07-16 13:50:09 | SELL | BA | 1 | $230.91 | $18.09 | 65 |
| 2025-07-16 13:50:09 | SELL | WFC | 3 | $79.46 | $1.71 | 65 |
| 2025-07-16 13:50:09 | SELL | CVX | 1 | $150.89 | $3.88 | 75 |
| 2025-07-16 13:50:09 | BUY | INTC | 7 | $22.65 | N/A | 65 |
| 2025-07-16 13:50:09 | BUY | MRK | 3 | $82.21 | N/A | 75 |
| 2025-07-16 13:50:09 | BUY | UNP | 1 | $231.38 | N/A | 75 |
| 2025-07-16 13:30:02 | SELL | BAC | 3 | $46.15 | $-0.37 | 65 |
| 2025-07-16 13:30:02 | BUY | NVDA | 1 | $170.70 | N/A | 85 |
| 2025-07-16 13:30:02 | BUY | WFC | 2 | $78.86 | N/A | 75 |

<!--TRADE_LOG_END--> 
