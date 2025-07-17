# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 16:27:17**

| Metric | Value |
|---|---|
| **Total Value** | **$101,295.67** |
| Cash | $623.64 |
| Holdings Value | $100,672.02 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.30 | $2,113.00 | 65 |
| ADBE | 6 | $375.23 | $365.99 | $2,195.94 | 65 |
| AMD | 14 | $160.03 | $159.81 | $2,237.27 | 75 |
| AMZN | 10 | $221.65 | $223.75 | $2,237.50 | 65 |
| AVGO | 8 | $275.34 | $287.90 | $2,303.24 | 70 |
| AXP | 7 | $309.18 | $313.69 | $2,195.83 | 65 |
| BA | 9 | $210.81 | $228.45 | $2,056.05 | 70 |
| BAC | 45 | $46.25 | $46.61 | $2,097.45 | 65 |
| C | 30 | $86.85 | $92.42 | $2,772.45 | 85 |
| CAT | 6 | $397.74 | $416.56 | $2,499.36 | 70 |
| COST | 2 | $979.83 | $953.72 | $1,907.44 | 65 |
| CRM | 8 | $267.44 | $259.79 | $2,078.32 | 65 |
| CSCO | 32 | $68.57 | $68.28 | $2,185.12 | 70 |
| CVX | 16 | $146.82 | $150.07 | $2,401.12 | 75 |
| DIS | 22 | $122.51 | $121.42 | $2,671.26 | 85 |
| GOOGL | 13 | $179.34 | $182.78 | $2,376.20 | 75 |
| GS | 3 | $717.52 | $710.70 | $2,132.10 | 75 |
| HD | 6 | $354.18 | $356.25 | $2,137.50 | 65 |
| INTC | 84 | $22.35 | $22.92 | $1,925.44 | 60 |
| JNJ | 13 | $155.43 | $163.12 | $2,120.56 | 65 |
| JPM | 9 | $291.90 | $287.53 | $2,587.77 | 85 |
| KO | 30 | $70.97 | $69.72 | $2,091.75 | 65 |
| LLY | 3 | $781.32 | $773.38 | $2,320.12 | 65 |
| MA | 4 | $563.08 | $553.44 | $2,213.78 | 65 |
| META | 3 | $717.12 | $703.58 | $2,110.74 | 65 |
| MRK | 29 | $82.56 | $81.75 | $2,370.75 | 75 |
| MSFT | 5 | $498.84 | $512.92 | $2,564.60 | 85 |
| NFLX | 1 | $1,279.00 | $1,262.30 | $1,262.30 | 65 |
| NKE | 31 | $71.96 | $72.95 | $2,261.61 | 70 |
| NVDA | 13 | $171.55 | $174.10 | $2,263.30 | 70 |
| ORCL | 9 | $232.91 | $248.37 | $2,235.28 | 70 |
| PEP | 16 | $136.49 | $144.74 | $2,315.82 | 75 |
| PFE | 84 | $25.28 | $24.59 | $2,065.18 | 65 |
| PG | 14 | $152.18 | $154.59 | $2,164.26 | 65 |
| PYPL | 28 | $72.12 | $73.28 | $2,051.84 | 65 |
| QCOM | 14 | $153.83 | $153.01 | $2,142.14 | 65 |
| T | 77 | $27.10 | $26.89 | $2,070.54 | 65 |
| TGT | 20 | $104.83 | $103.37 | $2,067.39 | 65 |
| TSLA | 6 | $318.51 | $320.73 | $1,924.38 | 65 |
| UNH | 7 | $298.51 | $289.35 | $2,025.45 | 65 |
| UNP | 10 | $236.33 | $227.34 | $2,273.40 | 65 |
| V | 6 | $355.85 | $349.47 | $2,096.82 | 65 |
| VZ | 51 | $43.04 | $40.91 | $2,086.66 | 65 |
| WFC | 28 | $78.79 | $80.17 | $2,244.90 | 70 |
| WMT | 22 | $97.29 | $95.28 | $2,096.16 | 65 |
| XOM | 19 | $109.80 | $111.68 | $2,121.92 | 65 |

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
| 2025-07-17 16:27:10 | SELL | NVDA | 2 | $174.01 | $4.26 | 70 |
| 2025-07-17 16:27:10 | SELL | BAC | 3 | $46.61 | $1.01 | 65 |
| 2025-07-17 16:27:10 | SELL | INTC | 6 | $22.94 | $3.32 | 60 |
| 2025-07-17 16:27:10 | SELL | XOM | 2 | $111.70 | $3.44 | 65 |
| 2025-07-17 16:27:10 | SELL | NKE | 1 | $72.97 | $0.98 | 70 |
| 2025-07-17 16:27:10 | SELL | WFC | 1 | $80.18 | $1.33 | 70 |
| 2025-07-17 16:27:10 | BUY | DIS | 3 | $121.40 | N/A | 85 |
| 2025-07-17 16:27:10 | BUY | CSCO | 1 | $68.29 | N/A | 70 |
| 2025-07-17 16:10:07 | SELL | CSCO | 1 | $68.43 | $-0.15 | 65 |
| 2025-07-17 16:10:07 | BUY | NVDA | 2 | $173.51 | N/A | 85 |
| 2025-07-17 16:10:07 | BUY | NKE | 3 | $72.90 | N/A | 75 |
| 2025-07-17 16:10:07 | BUY | WFC | 1 | $80.31 | N/A | 75 |
| 2025-07-17 15:52:40 | SELL | NVDA | 2 | $173.43 | $3.11 | 70 |
| 2025-07-17 15:52:40 | SELL | NKE | 3 | $72.80 | $2.46 | 65 |
| 2025-07-17 15:52:40 | SELL | WFC | 1 | $80.25 | $1.41 | 70 |
| 2025-07-17 15:52:40 | BUY | BAC | 3 | $46.51 | N/A | 70 |
| 2025-07-17 15:52:40 | BUY | INTC | 6 | $23.01 | N/A | 65 |
| 2025-07-17 15:52:40 | BUY | CSCO | 1 | $68.32 | N/A | 70 |
| 2025-07-17 15:41:13 | SELL | AMD | 1 | $159.85 | $-0.16 | 70 |
| 2025-07-17 15:41:13 | SELL | PFE | 1 | $24.69 | $-0.58 | 65 |
| 2025-07-17 15:41:13 | SELL | CSCO | 4 | $67.37 | $-4.30 | 65 |
| 2025-07-17 15:41:13 | SELL | T | 1 | $26.88 | $-0.22 | 65 |
| 2025-07-17 15:41:13 | SELL | TGT | 1 | $103.42 | $-1.35 | 65 |
| 2025-07-17 15:41:13 | BUY | NVDA | 2 | $173.33 | N/A | 85 |
| 2025-07-17 15:41:13 | BUY | XOM | 2 | $111.93 | N/A | 75 |

<!--TRADE_LOG_END--> 
