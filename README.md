# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 16:44:43**

| Metric | Value |
|---|---|
| **Total Value** | **$101,255.45** |
| Cash | $569.39 |
| Holdings Value | $100,686.06 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.23 | $2,112.30 | 65 |
| ADBE | 6 | $375.23 | $365.51 | $2,193.06 | 65 |
| AMD | 14 | $160.03 | $159.75 | $2,236.43 | 70 |
| AMZN | 10 | $221.65 | $223.61 | $2,236.10 | 75 |
| AVGO | 8 | $275.34 | $287.79 | $2,302.28 | 70 |
| AXP | 7 | $309.18 | $313.73 | $2,196.11 | 70 |
| BA | 9 | $210.81 | $228.05 | $2,052.45 | 65 |
| BAC | 45 | $46.25 | $46.65 | $2,099.25 | 65 |
| C | 30 | $86.85 | $92.53 | $2,775.75 | 85 |
| CAT | 6 | $397.74 | $416.47 | $2,498.82 | 75 |
| COST | 2 | $979.83 | $953.03 | $1,906.06 | 65 |
| CRM | 8 | $267.44 | $259.42 | $2,075.36 | 65 |
| CSCO | 32 | $68.57 | $68.35 | $2,187.20 | 70 |
| CVX | 16 | $146.82 | $149.98 | $2,399.68 | 75 |
| DIS | 22 | $122.51 | $121.58 | $2,674.87 | 85 |
| GOOGL | 13 | $179.34 | $183.03 | $2,379.33 | 75 |
| GS | 3 | $717.52 | $709.67 | $2,129.02 | 85 |
| HD | 6 | $354.18 | $356.82 | $2,140.95 | 65 |
| INTC | 90 | $22.38 | $22.93 | $2,063.25 | 65 |
| JNJ | 13 | $155.43 | $163.12 | $2,120.49 | 65 |
| JPM | 9 | $291.90 | $287.55 | $2,587.95 | 75 |
| KO | 30 | $70.97 | $69.72 | $2,091.75 | 65 |
| LLY | 3 | $781.32 | $766.64 | $2,299.92 | 65 |
| MA | 4 | $563.08 | $553.16 | $2,212.64 | 65 |
| META | 3 | $717.12 | $701.90 | $2,105.70 | 75 |
| MRK | 29 | $82.56 | $81.65 | $2,367.74 | 75 |
| MSFT | 5 | $498.84 | $512.91 | $2,564.55 | 85 |
| NFLX | 1 | $1,279.00 | $1,260.09 | $1,260.09 | 65 |
| NKE | 29 | $71.88 | $73.16 | $2,121.49 | 65 |
| NVDA | 13 | $171.55 | $173.49 | $2,255.31 | 70 |
| ORCL | 9 | $232.91 | $247.44 | $2,226.91 | 70 |
| PEP | 16 | $136.49 | $144.42 | $2,310.72 | 75 |
| PFE | 84 | $25.28 | $24.61 | $2,067.24 | 65 |
| PG | 14 | $152.18 | $154.74 | $2,166.36 | 65 |
| PYPL | 28 | $72.12 | $73.46 | $2,056.88 | 65 |
| QCOM | 14 | $153.83 | $152.98 | $2,141.72 | 65 |
| T | 77 | $27.10 | $26.86 | $2,067.84 | 65 |
| TGT | 20 | $104.83 | $103.25 | $2,065.10 | 65 |
| TSLA | 6 | $318.51 | $320.72 | $1,924.32 | 65 |
| UNH | 7 | $298.51 | $288.87 | $2,022.09 | 65 |
| UNP | 10 | $236.33 | $228.24 | $2,282.35 | 65 |
| V | 6 | $355.85 | $349.61 | $2,097.66 | 65 |
| VZ | 51 | $43.04 | $40.92 | $2,086.92 | 65 |
| WFC | 26 | $78.69 | $80.20 | $2,085.20 | 65 |
| WMT | 22 | $97.29 | $95.19 | $2,094.08 | 65 |
| XOM | 21 | $109.97 | $111.66 | $2,344.76 | 75 |

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
| 2025-07-17 16:44:33 | SELL | NKE | 2 | $73.14 | $2.38 | 65 |
| 2025-07-17 16:44:33 | SELL | WFC | 2 | $80.17 | $2.74 | 65 |
| 2025-07-17 16:44:33 | BUY | XOM | 2 | $111.66 | N/A | 75 |
| 2025-07-17 16:44:33 | BUY | INTC | 6 | $22.92 | N/A | 65 |
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

<!--TRADE_LOG_END--> 
