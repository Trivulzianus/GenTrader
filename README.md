# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 15:27:00**

| Metric | Value |
|---|---|
| **Total Value** | **$100,674.42** |
| Cash | $1,406.91 |
| Holdings Value | $99,267.51 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.83 | $2,108.30 | 65 |
| ADBE | 6 | $375.23 | $365.77 | $2,194.62 | 65 |
| AMD | 17 | $146.29 | $155.28 | $2,639.76 | 85 |
| AMZN | 10 | $221.60 | $226.50 | $2,264.95 | 75 |
| AVGO | 8 | $275.34 | $281.11 | $2,248.88 | 70 |
| AXP | 7 | $325.34 | $313.44 | $2,194.05 | 70 |
| BA | 9 | $210.77 | $230.99 | $2,078.92 | 65 |
| BAC | 44 | $48.83 | $46.50 | $2,046.00 | 65 |
| C | 30 | $86.78 | $88.42 | $2,652.60 | 85 |
| CAT | 6 | $397.74 | $407.06 | $2,442.36 | 85 |
| COST | 2 | $979.83 | $968.38 | $1,936.76 | 65 |
| CRM | 8 | $267.44 | $259.06 | $2,072.49 | 65 |
| CSCO | 31 | $68.46 | $67.61 | $2,095.76 | 65 |
| CVX | 16 | $146.80 | $151.18 | $2,418.94 | 75 |
| DIS | 17 | $122.96 | $118.98 | $2,022.66 | 65 |
| GOOGL | 13 | $179.43 | $183.96 | $2,391.48 | 75 |
| GS | 3 | $717.52 | $705.57 | $2,116.70 | 75 |
| HD | 6 | $372.64 | $364.64 | $2,187.84 | 65 |
| INTC | 88 | $22.39 | $23.39 | $2,058.24 | 65 |
| JNJ | 13 | $155.95 | $155.28 | $2,018.64 | 65 |
| JPM | 9 | $291.63 | $286.58 | $2,579.22 | 85 |
| KO | 30 | $70.97 | $69.36 | $2,080.88 | 65 |
| LLY | 3 | $781.32 | $772.06 | $2,316.19 | 65 |
| MA | 4 | $563.08 | $549.52 | $2,198.09 | 65 |
| META | 3 | $717.12 | $717.21 | $2,151.62 | 65 |
| MRK | 25 | $82.54 | $81.73 | $2,043.25 | 65 |
| MSFT | 5 | $498.84 | $506.56 | $2,532.78 | 85 |
| NFLX | 1 | $1,279.00 | $1,258.11 | $1,258.11 | 65 |
| NKE | 29 | $72.03 | $72.36 | $2,098.44 | 65 |
| NVDA | 14 | $171.75 | $171.25 | $2,397.43 | 70 |
| ORCL | 9 | $233.27 | $231.40 | $2,082.60 | 70 |
| PEP | 15 | $136.57 | $134.28 | $2,014.12 | 65 |
| PFE | 83 | $25.22 | $24.80 | $2,057.99 | 65 |
| PG | 13 | $152.12 | $152.49 | $1,982.37 | 65 |
| PYPL | 30 | $72.23 | $73.52 | $2,205.60 | 70 |
| QCOM | 14 | $153.83 | $155.07 | $2,171.05 | 65 |
| T | 77 | $27.10 | $26.91 | $2,071.68 | 65 |
| TGT | 20 | $104.94 | $103.79 | $2,075.90 | 65 |
| TSLA | 6 | $318.51 | $314.03 | $1,884.18 | 65 |
| UNH | 7 | $298.51 | $293.87 | $2,057.06 | 65 |
| UNP | 9 | $236.54 | $232.70 | $2,094.27 | 65 |
| V | 6 | $355.85 | $347.61 | $2,085.66 | 65 |
| VZ | 50 | $43.08 | $41.24 | $2,062.25 | 65 |
| WFC | 28 | $78.72 | $78.72 | $2,204.02 | 70 |
| WMT | 21 | $97.38 | $95.15 | $1,998.15 | 65 |
| XOM | 21 | $109.99 | $113.08 | $2,374.67 | 75 |

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
| 2025-07-15 14:52:34 | BUY | CVX | 2 | $151.16 | N/A | 85 |
| 2025-07-15 14:52:34 | BUY | T | 1 | $26.91 | N/A | 65 |
| 2025-07-15 14:41:32 | SELL | AMZN | 1 | $226.26 | $4.24 | 70 |
| 2025-07-15 14:41:32 | SELL | PYPL | 3 | $73.44 | $3.40 | 65 |
| 2025-07-15 14:41:32 | SELL | BA | 2 | $230.57 | $32.40 | 65 |
| 2025-07-15 14:41:32 | SELL | CVX | 1 | $151.29 | $4.23 | 75 |

<!--TRADE_LOG_END--> 
