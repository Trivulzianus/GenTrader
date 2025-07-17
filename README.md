# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 17:51:47**

| Metric | Value |
|---|---|
| **Total Value** | **$101,313.13** |
| Cash | $337.32 |
| Holdings Value | $100,975.82 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.21 | $2,112.05 | 70 |
| ADBE | 6 | $375.23 | $366.47 | $2,198.79 | 65 |
| AMD | 14 | $160.03 | $159.32 | $2,230.47 | 70 |
| AMZN | 10 | $221.65 | $223.84 | $2,238.40 | 70 |
| AVGO | 8 | $275.34 | $287.06 | $2,296.48 | 65 |
| AXP | 7 | $309.18 | $314.79 | $2,203.53 | 75 |
| BA | 9 | $210.81 | $229.98 | $2,069.82 | 65 |
| BAC | 45 | $46.25 | $46.87 | $2,108.93 | 65 |
| C | 30 | $86.85 | $92.58 | $2,777.40 | 85 |
| CAT | 6 | $397.74 | $418.00 | $2,508.00 | 75 |
| COST | 2 | $979.83 | $952.96 | $1,905.92 | 65 |
| CRM | 8 | $267.44 | $259.40 | $2,075.20 | 65 |
| CSCO | 33 | $68.56 | $68.38 | $2,256.38 | 70 |
| CVX | 16 | $146.82 | $150.51 | $2,408.24 | 75 |
| DIS | 22 | $122.51 | $121.33 | $2,669.37 | 85 |
| GOOGL | 13 | $179.34 | $183.24 | $2,382.12 | 75 |
| GS | 3 | $717.52 | $710.39 | $2,131.17 | 75 |
| HD | 6 | $354.18 | $358.40 | $2,150.40 | 65 |
| INTC | 84 | $22.34 | $22.91 | $1,924.86 | 60 |
| JNJ | 13 | $155.43 | $163.51 | $2,125.69 | 70 |
| JPM | 9 | $291.90 | $287.75 | $2,589.75 | 75 |
| KO | 30 | $70.97 | $69.78 | $2,093.55 | 65 |
| LLY | 3 | $781.32 | $763.85 | $2,291.55 | 65 |
| MA | 4 | $563.08 | $554.38 | $2,217.52 | 65 |
| META | 3 | $717.12 | $701.34 | $2,104.02 | 65 |
| MRK | 29 | $82.56 | $81.59 | $2,366.11 | 75 |
| MSFT | 5 | $498.84 | $512.77 | $2,563.85 | 85 |
| NFLX | 1 | $1,279.00 | $1,265.79 | $1,265.79 | 65 |
| NKE | 32 | $71.99 | $73.08 | $2,338.40 | 75 |
| NVDA | 15 | $171.77 | $173.14 | $2,597.07 | 85 |
| ORCL | 9 | $232.91 | $247.39 | $2,226.47 | 70 |
| PEP | 16 | $136.49 | $144.93 | $2,318.88 | 70 |
| PFE | 84 | $25.28 | $24.57 | $2,064.30 | 65 |
| PG | 14 | $152.18 | $154.71 | $2,165.94 | 65 |
| PYPL | 28 | $72.12 | $73.72 | $2,064.16 | 65 |
| QCOM | 14 | $153.83 | $153.20 | $2,144.80 | 65 |
| T | 77 | $27.09 | $26.93 | $2,073.60 | 65 |
| TGT | 20 | $104.83 | $103.65 | $2,073.00 | 65 |
| TSLA | 6 | $318.51 | $317.82 | $1,906.95 | 65 |
| UNH | 7 | $298.51 | $288.69 | $2,020.83 | 65 |
| UNP | 10 | $236.33 | $227.90 | $2,279.00 | 65 |
| V | 6 | $355.85 | $349.81 | $2,098.89 | 65 |
| VZ | 50 | $40.87 | $40.93 | $2,046.50 | 65 |
| WFC | 26 | $78.70 | $79.84 | $2,075.84 | 65 |
| WMT | 22 | $97.29 | $95.22 | $2,094.95 | 65 |
| XOM | 19 | $109.80 | $111.62 | $2,120.88 | 65 |

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
| 2025-07-17 17:51:42 | SELL | XOM | 2 | $111.62 | $3.31 | 65 |
| 2025-07-17 17:51:42 | SELL | WFC | 2 | $79.84 | $2.13 | 65 |
| 2025-07-17 17:51:42 | BUY | NVDA | 2 | $173.15 | N/A | 85 |
| 2025-07-17 17:51:42 | BUY | NKE | 3 | $73.08 | N/A | 75 |
| 2025-07-17 17:51:42 | BUY | MRK | 1 | $81.60 | N/A | 75 |
| 2025-07-17 17:40:27 | SELL | MRK | 1 | $81.55 | $-1.01 | 70 |
| 2025-07-17 17:40:27 | BUY | WFC | 1 | $79.77 | N/A | 70 |
| 2025-07-17 17:26:16 | SELL | NKE | 1 | $72.96 | $1.05 | 65 |
| 2025-07-17 17:26:16 | SELL | CSCO | 2 | $68.18 | $-0.70 | 70 |
| 2025-07-17 17:26:16 | SELL | T | 1 | $26.90 | $-0.20 | 65 |
| 2025-07-17 17:26:16 | BUY | XOM | 2 | $111.64 | N/A | 75 |
| 2025-07-17 17:09:24 | SELL | NVDA | 2 | $173.65 | $3.62 | 70 |
| 2025-07-17 17:09:24 | SELL | XOM | 2 | $111.69 | $3.43 | 65 |
| 2025-07-17 17:09:24 | SELL | T | 5 | $26.86 | $-1.09 | 65 |
| 2025-07-17 17:09:24 | BUY | WFC | 1 | $80.10 | N/A | 70 |
| 2025-07-17 17:09:24 | BUY | CSCO | 4 | $68.19 | N/A | 75 |
| 2025-07-17 16:56:39 | SELL | INTC | 6 | $22.99 | $3.60 | 60 |
| 2025-07-17 16:56:39 | SELL | CSCO | 1 | $68.29 | $-0.29 | 65 |
| 2025-07-17 16:56:39 | BUY | NVDA | 2 | $173.66 | N/A | 85 |
| 2025-07-17 16:56:39 | BUY | NKE | 1 | $73.01 | N/A | 70 |
| 2025-07-17 16:56:39 | BUY | VZ | 50 | $40.87 | N/A | 65 |
| 2025-07-17 16:56:39 | BUY | T | 6 | $26.84 | N/A | 70 |
| 2025-07-17 16:56:16 | SELL | VZ | 51 | $40.86 | $-111.01 | 65 |
| 2025-07-17 16:44:33 | SELL | NKE | 2 | $73.14 | $2.38 | 65 |
| 2025-07-17 16:44:33 | SELL | WFC | 2 | $80.17 | $2.74 | 65 |

<!--TRADE_LOG_END--> 
