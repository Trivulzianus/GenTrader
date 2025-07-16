# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 14:08:38**

| Metric | Value |
|---|---|
| **Total Value** | **$100,429.81** |
| Cash | $1,195.93 |
| Holdings Value | $99,233.88 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.83 | $2,108.30 | 70 |
| ADBE | 6 | $375.23 | $360.11 | $2,160.63 | 65 |
| AMD | 14 | $144.36 | $154.62 | $2,164.75 | 65 |
| AMZN | 10 | $221.65 | $224.66 | $2,246.56 | 75 |
| AVGO | 8 | $275.34 | $278.43 | $2,227.44 | 70 |
| AXP | 7 | $325.34 | $310.70 | $2,174.90 | 65 |
| BA | 9 | $210.81 | $230.69 | $2,076.26 | 65 |
| BAC | 45 | $46.28 | $46.02 | $2,070.90 | 65 |
| C | 30 | $86.78 | $90.32 | $2,709.60 | 85 |
| CAT | 6 | $397.74 | $406.66 | $2,439.96 | 85 |
| COST | 2 | $979.83 | $955.54 | $1,911.08 | 65 |
| CRM | 8 | $267.44 | $256.48 | $2,051.80 | 65 |
| CSCO | 31 | $68.46 | $67.42 | $2,090.02 | 65 |
| CVX | 16 | $146.76 | $150.37 | $2,405.92 | 75 |
| DIS | 18 | $122.77 | $119.85 | $2,157.30 | 70 |
| GOOGL | 14 | $179.71 | $182.77 | $2,558.78 | 75 |
| GS | 3 | $717.52 | $701.89 | $2,105.67 | 85 |
| HD | 6 | $372.64 | $357.70 | $2,146.20 | 65 |
| INTC | 84 | $22.36 | $22.70 | $1,906.38 | 60 |
| JNJ | 13 | $155.43 | $162.15 | $2,107.95 | 65 |
| JPM | 9 | $291.63 | $287.08 | $2,583.69 | 85 |
| KO | 30 | $70.97 | $69.17 | $2,075.25 | 65 |
| LLY | 3 | $781.32 | $783.18 | $2,349.54 | 65 |
| MA | 4 | $563.08 | $551.34 | $2,205.36 | 65 |
| META | 3 | $717.12 | $705.91 | $2,117.73 | 70 |
| MRK | 29 | $82.47 | $82.15 | $2,382.35 | 75 |
| MSFT | 5 | $498.84 | $503.02 | $2,515.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,256.49 | $1,256.49 | 65 |
| NKE | 30 | $72.03 | $71.99 | $2,159.70 | 70 |
| NVDA | 14 | $171.61 | $170.24 | $2,383.38 | 70 |
| ORCL | 9 | $233.15 | $235.23 | $2,117.07 | 65 |
| PEP | 15 | $136.57 | $134.63 | $2,019.45 | 65 |
| PFE | 83 | $25.29 | $24.86 | $2,063.80 | 65 |
| PG | 14 | $152.15 | $153.10 | $2,143.47 | 65 |
| PYPL | 29 | $72.15 | $72.47 | $2,101.63 | 65 |
| QCOM | 14 | $153.83 | $153.03 | $2,142.42 | 70 |
| T | 77 | $27.09 | $26.93 | $2,073.22 | 65 |
| TGT | 20 | $104.94 | $101.92 | $2,038.30 | 65 |
| TSLA | 6 | $318.51 | $315.85 | $1,895.10 | 65 |
| UNH | 7 | $298.51 | $293.58 | $2,055.06 | 65 |
| UNP | 9 | $236.78 | $230.54 | $2,074.90 | 65 |
| V | 6 | $355.85 | $346.57 | $2,079.43 | 65 |
| VZ | 50 | $43.08 | $41.26 | $2,062.75 | 65 |
| WFC | 26 | $78.81 | $79.41 | $2,064.53 | 65 |
| WMT | 22 | $97.29 | $95.06 | $2,091.36 | 65 |
| XOM | 21 | $110.00 | $112.50 | $2,362.39 | 75 |

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
| 2025-07-16 13:04:56 | SELL | UNP | 1 | $231.14 | $-4.99 | 65 |
| 2025-07-16 13:04:56 | SELL | T | 1 | $27.02 | $-0.07 | 65 |
| 2025-07-16 13:04:56 | BUY | WFC | 1 | $78.86 | N/A | 70 |
| 2025-07-16 13:04:56 | BUY | BA | 1 | $230.00 | N/A | 75 |
| 2025-07-16 12:32:59 | SELL | CVX | 1 | $150.69 | $3.48 | 75 |

<!--TRADE_LOG_END--> 
