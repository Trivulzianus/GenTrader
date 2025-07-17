# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 15:41:18**

| Metric | Value |
|---|---|
| **Total Value** | **$101,382.14** |
| Cash | $332.14 |
| Holdings Value | $101,050.00 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.19 | $2,101.95 | 65 |
| ADBE | 6 | $375.23 | $365.02 | $2,190.15 | 65 |
| AMD | 14 | $160.03 | $159.87 | $2,238.12 | 70 |
| AMZN | 10 | $221.65 | $223.62 | $2,236.20 | 75 |
| AVGO | 8 | $275.34 | $287.20 | $2,297.60 | 65 |
| AXP | 7 | $309.18 | $314.37 | $2,200.59 | 75 |
| BA | 9 | $210.81 | $229.88 | $2,068.88 | 65 |
| BAC | 45 | $46.26 | $46.53 | $2,093.85 | 65 |
| C | 30 | $86.85 | $92.48 | $2,774.40 | 85 |
| CAT | 6 | $397.74 | $416.64 | $2,499.84 | 70 |
| COST | 2 | $979.83 | $951.79 | $1,903.58 | 65 |
| CRM | 8 | $267.44 | $259.42 | $2,075.32 | 60 |
| CSCO | 31 | $68.58 | $68.22 | $2,114.66 | 65 |
| CVX | 16 | $146.82 | $150.23 | $2,403.68 | 75 |
| DIS | 19 | $122.69 | $121.60 | $2,310.40 | 75 |
| GOOGL | 13 | $179.34 | $182.32 | $2,370.16 | 70 |
| GS | 3 | $717.52 | $712.47 | $2,137.41 | 85 |
| HD | 6 | $354.18 | $356.71 | $2,140.29 | 65 |
| INTC | 84 | $22.34 | $22.91 | $1,924.45 | 60 |
| JNJ | 13 | $155.43 | $162.85 | $2,117.05 | 65 |
| JPM | 9 | $291.90 | $288.20 | $2,593.80 | 80 |
| KO | 30 | $70.97 | $69.84 | $2,095.35 | 65 |
| LLY | 3 | $781.32 | $785.43 | $2,356.29 | 65 |
| MA | 4 | $563.08 | $554.32 | $2,217.28 | 65 |
| META | 3 | $717.12 | $701.75 | $2,105.25 | 70 |
| MRK | 29 | $82.56 | $82.11 | $2,381.19 | 75 |
| MSFT | 5 | $498.84 | $512.38 | $2,561.92 | 85 |
| NFLX | 1 | $1,279.00 | $1,259.81 | $1,259.81 | 65 |
| NKE | 32 | $71.98 | $73.01 | $2,336.32 | 75 |
| NVDA | 15 | $171.87 | $173.35 | $2,600.32 | 85 |
| ORCL | 9 | $232.91 | $249.44 | $2,245.01 | 70 |
| PEP | 16 | $136.49 | $144.85 | $2,317.60 | 75 |
| PFE | 84 | $25.28 | $24.68 | $2,073.54 | 65 |
| PG | 14 | $152.18 | $154.62 | $2,164.75 | 65 |
| PYPL | 28 | $72.12 | $73.34 | $2,053.52 | 65 |
| QCOM | 14 | $153.83 | $153.36 | $2,147.04 | 65 |
| T | 77 | $27.10 | $26.88 | $2,069.38 | 65 |
| TGT | 20 | $104.83 | $103.42 | $2,068.30 | 65 |
| TSLA | 6 | $318.51 | $322.18 | $1,933.10 | 65 |
| UNH | 7 | $298.51 | $289.35 | $2,025.45 | 65 |
| UNP | 10 | $236.33 | $228.41 | $2,284.10 | 65 |
| V | 6 | $355.85 | $349.63 | $2,097.78 | 65 |
| VZ | 51 | $43.04 | $40.98 | $2,089.72 | 65 |
| WFC | 29 | $78.84 | $80.30 | $2,328.70 | 75 |
| WMT | 22 | $97.29 | $95.23 | $2,095.06 | 65 |
| XOM | 21 | $109.98 | $111.94 | $2,350.84 | 75 |

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
| 2025-07-17 15:41:13 | SELL | AMD | 1 | $159.85 | $-0.16 | 70 |
| 2025-07-17 15:41:13 | SELL | PFE | 1 | $24.69 | $-0.58 | 65 |
| 2025-07-17 15:41:13 | SELL | CSCO | 4 | $67.37 | $-4.30 | 65 |
| 2025-07-17 15:41:13 | SELL | T | 1 | $26.88 | $-0.22 | 65 |
| 2025-07-17 15:41:13 | SELL | TGT | 1 | $103.42 | $-1.35 | 65 |
| 2025-07-17 15:41:13 | BUY | NVDA | 2 | $173.33 | N/A | 85 |
| 2025-07-17 15:41:13 | BUY | XOM | 2 | $111.93 | N/A | 75 |
| 2025-07-17 15:41:13 | BUY | NKE | 3 | $73.00 | N/A | 75 |
| 2025-07-17 15:41:13 | BUY | WFC | 3 | $80.32 | N/A | 75 |
| 2025-07-17 15:26:56 | SELL | NVDA | 2 | $173.08 | $2.49 | 70 |
| 2025-07-17 15:26:56 | SELL | XOM | 2 | $111.78 | $3.63 | 65 |
| 2025-07-17 15:26:56 | SELL | NKE | 1 | $72.99 | $1.08 | 65 |
| 2025-07-17 15:26:56 | SELL | WFC | 2 | $80.14 | $2.73 | 65 |
| 2025-07-17 15:26:56 | BUY | AMD | 1 | $159.26 | N/A | 75 |
| 2025-07-17 15:26:56 | BUY | CSCO | 3 | $68.11 | N/A | 75 |
| 2025-07-17 15:09:30 | SELL | DIS | 1 | $121.64 | $-1.00 | 70 |
| 2025-07-17 15:09:30 | BUY | NVDA | 2 | $173.26 | N/A | 85 |
| 2025-07-17 15:09:30 | BUY | MRK | 1 | $82.01 | N/A | 75 |
| 2025-07-17 15:09:30 | BUY | CSCO | 1 | $68.25 | N/A | 70 |
| 2025-07-17 14:53:19 | SELL | NVDA | 1 | $172.82 | $1.11 | 70 |
| 2025-07-17 14:53:19 | SELL | AMD | 1 | $160.08 | $0.01 | 70 |
| 2025-07-17 14:53:19 | SELL | INTC | 2 | $22.80 | $0.89 | 60 |
| 2025-07-17 14:53:19 | SELL | DIS | 1 | $121.26 | $-1.31 | 75 |
| 2025-07-17 14:53:19 | SELL | MRK | 1 | $81.96 | $-0.60 | 70 |
| 2025-07-17 14:53:19 | SELL | ORCL | 1 | $249.93 | $15.33 | 65 |

<!--TRADE_LOG_END--> 
