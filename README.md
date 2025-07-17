# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 17:40:36**

| Metric | Value |
|---|---|
| **Total Value** | **$101,291.30** |
| Cash | $601.53 |
| Holdings Value | $100,689.77 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.28 | $2,112.80 | 65 |
| ADBE | 6 | $375.23 | $365.85 | $2,195.08 | 65 |
| AMD | 14 | $160.03 | $159.31 | $2,230.27 | 70 |
| AMZN | 10 | $221.65 | $223.78 | $2,237.80 | 75 |
| AVGO | 8 | $275.34 | $286.97 | $2,295.76 | 70 |
| AXP | 7 | $309.18 | $314.69 | $2,202.83 | 75 |
| BA | 9 | $210.81 | $229.65 | $2,066.85 | 65 |
| BAC | 45 | $46.25 | $46.90 | $2,110.50 | 65 |
| C | 30 | $86.85 | $92.55 | $2,776.50 | 85 |
| CAT | 6 | $397.74 | $417.41 | $2,504.46 | 70 |
| COST | 2 | $979.83 | $952.73 | $1,905.46 | 65 |
| CRM | 8 | $267.44 | $259.24 | $2,073.92 | 65 |
| CSCO | 33 | $68.56 | $68.28 | $2,253.24 | 70 |
| CVX | 16 | $146.82 | $150.37 | $2,405.92 | 75 |
| DIS | 22 | $122.51 | $121.52 | $2,673.44 | 85 |
| GOOGL | 13 | $179.34 | $183.14 | $2,380.82 | 75 |
| GS | 3 | $717.52 | $709.27 | $2,127.81 | 75 |
| HD | 6 | $354.18 | $358.51 | $2,151.08 | 65 |
| INTC | 84 | $22.34 | $22.94 | $1,926.96 | 60 |
| JNJ | 13 | $155.43 | $163.56 | $2,126.28 | 65 |
| JPM | 9 | $291.90 | $287.55 | $2,587.95 | 75 |
| KO | 30 | $70.97 | $69.78 | $2,093.55 | 65 |
| LLY | 3 | $781.32 | $761.53 | $2,284.59 | 65 |
| MA | 4 | $563.08 | $554.11 | $2,216.44 | 65 |
| META | 3 | $717.12 | $700.88 | $2,102.65 | 70 |
| MRK | 28 | $82.59 | $81.55 | $2,283.41 | 70 |
| MSFT | 5 | $498.84 | $512.55 | $2,562.75 | 85 |
| NFLX | 1 | $1,279.00 | $1,265.09 | $1,265.09 | 65 |
| NKE | 29 | $71.88 | $73.02 | $2,117.43 | 65 |
| NVDA | 13 | $171.56 | $173.66 | $2,257.64 | 70 |
| ORCL | 9 | $232.91 | $247.00 | $2,223.00 | 75 |
| PEP | 16 | $136.49 | $144.94 | $2,319.11 | 70 |
| PFE | 84 | $25.28 | $24.59 | $2,065.14 | 65 |
| PG | 14 | $152.18 | $154.76 | $2,166.64 | 65 |
| PYPL | 28 | $72.12 | $73.56 | $2,059.68 | 65 |
| QCOM | 14 | $153.83 | $153.16 | $2,144.24 | 65 |
| T | 77 | $27.09 | $26.96 | $2,075.92 | 65 |
| TGT | 20 | $104.83 | $103.68 | $2,073.60 | 65 |
| TSLA | 6 | $318.51 | $318.65 | $1,911.90 | 65 |
| UNH | 7 | $298.51 | $288.59 | $2,020.14 | 65 |
| UNP | 10 | $236.33 | $227.95 | $2,279.47 | 65 |
| V | 6 | $355.85 | $349.69 | $2,098.14 | 65 |
| VZ | 50 | $40.87 | $40.95 | $2,047.50 | 65 |
| WFC | 28 | $78.78 | $79.81 | $2,234.82 | 70 |
| WMT | 22 | $97.29 | $95.22 | $2,094.95 | 65 |
| XOM | 21 | $109.97 | $111.72 | $2,346.22 | 70 |

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
| 2025-07-17 16:44:33 | BUY | XOM | 2 | $111.66 | N/A | 75 |
| 2025-07-17 16:44:33 | BUY | INTC | 6 | $22.92 | N/A | 65 |
| 2025-07-17 16:27:10 | SELL | NVDA | 2 | $174.01 | $4.26 | 70 |
| 2025-07-17 16:27:10 | SELL | BAC | 3 | $46.61 | $1.01 | 65 |
| 2025-07-17 16:27:10 | SELL | INTC | 6 | $22.94 | $3.32 | 60 |

<!--TRADE_LOG_END--> 
