# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 14:41:36**

| Metric | Value |
|---|---|
| **Total Value** | **$100,994.03** |
| Cash | $179.28 |
| Holdings Value | $100,814.75 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.02 | $2,100.20 | 65 |
| ADBE | 6 | $375.23 | $362.20 | $2,173.20 | 65 |
| AMD | 15 | $160.07 | $160.30 | $2,404.50 | 70 |
| AMZN | 10 | $221.65 | $222.84 | $2,228.40 | 75 |
| AVGO | 8 | $275.34 | $285.19 | $2,281.52 | 70 |
| AXP | 7 | $309.18 | $311.61 | $2,181.25 | 65 |
| BA | 9 | $210.81 | $229.48 | $2,065.32 | 65 |
| BAC | 45 | $46.26 | $46.11 | $2,074.95 | 65 |
| C | 30 | $86.85 | $90.55 | $2,716.50 | 85 |
| CAT | 6 | $397.74 | $415.28 | $2,491.68 | 70 |
| COST | 2 | $979.83 | $948.14 | $1,896.29 | 65 |
| CRM | 8 | $267.44 | $257.25 | $2,058.04 | 65 |
| CSCO | 31 | $68.48 | $68.16 | $2,112.96 | 65 |
| CVX | 16 | $146.82 | $149.45 | $2,391.20 | 75 |
| DIS | 21 | $122.57 | $120.85 | $2,537.94 | 75 |
| GOOGL | 13 | $179.34 | $182.34 | $2,370.36 | 75 |
| GS | 3 | $717.52 | $707.06 | $2,121.18 | 70 |
| HD | 6 | $354.18 | $355.27 | $2,131.62 | 65 |
| INTC | 86 | $22.35 | $22.79 | $1,959.78 | 60 |
| JNJ | 13 | $155.43 | $162.81 | $2,116.53 | 65 |
| JPM | 9 | $291.90 | $287.22 | $2,584.98 | 75 |
| KO | 30 | $70.97 | $69.72 | $2,091.60 | 65 |
| LLY | 3 | $781.32 | $785.44 | $2,356.32 | 65 |
| MA | 4 | $563.08 | $551.37 | $2,205.46 | 65 |
| META | 3 | $717.12 | $699.35 | $2,098.03 | 65 |
| MRK | 29 | $82.56 | $81.92 | $2,375.68 | 75 |
| MSFT | 5 | $498.84 | $510.90 | $2,554.52 | 70 |
| NFLX | 1 | $1,279.00 | $1,258.28 | $1,258.28 | 65 |
| NKE | 29 | $71.87 | $72.86 | $2,112.94 | 65 |
| NVDA | 14 | $171.70 | $172.89 | $2,420.41 | 70 |
| ORCL | 10 | $234.61 | $249.19 | $2,491.90 | 80 |
| PEP | 16 | $136.49 | $144.24 | $2,307.84 | 70 |
| PFE | 85 | $25.27 | $24.62 | $2,093.12 | 65 |
| PG | 14 | $152.18 | $154.43 | $2,162.01 | 65 |
| PYPL | 28 | $72.12 | $72.76 | $2,037.28 | 65 |
| QCOM | 14 | $153.83 | $152.67 | $2,137.38 | 65 |
| T | 78 | $27.09 | $26.90 | $2,098.21 | 65 |
| TGT | 21 | $104.77 | $102.40 | $2,150.40 | 65 |
| TSLA | 6 | $318.51 | $321.45 | $1,928.73 | 65 |
| UNH | 7 | $298.51 | $288.51 | $2,019.57 | 65 |
| UNP | 10 | $236.33 | $227.50 | $2,275.00 | 65 |
| V | 6 | $355.85 | $348.91 | $2,093.46 | 65 |
| VZ | 51 | $43.04 | $40.97 | $2,089.22 | 65 |
| WFC | 28 | $78.77 | $79.97 | $2,239.30 | 70 |
| WMT | 22 | $97.29 | $95.24 | $2,095.28 | 65 |
| XOM | 19 | $109.76 | $111.81 | $2,124.39 | 65 |

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
| 2025-07-17 14:41:28 | SELL | NVDA | 1 | $171.37 | $-0.31 | 70 |
| 2025-07-17 14:41:28 | SELL | AMD | 1 | $160.24 | $0.16 | 70 |
| 2025-07-17 14:41:28 | SELL | INTC | 5 | $22.69 | $1.60 | 60 |
| 2025-07-17 14:41:28 | SELL | NKE | 3 | $72.86 | $2.69 | 65 |
| 2025-07-17 14:41:28 | SELL | DIS | 1 | $120.84 | $-1.65 | 75 |
| 2025-07-17 14:41:28 | BUY | PFE | 1 | $24.62 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | WFC | 2 | $79.96 | N/A | 70 |
| 2025-07-17 14:41:28 | BUY | VZ | 1 | $40.96 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | ORCL | 1 | $249.18 | N/A | 80 |
| 2025-07-17 14:41:28 | BUY | T | 1 | $26.91 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | CVX | 1 | $149.46 | N/A | 75 |
| 2025-07-17 14:26:31 | SELL | XOM | 1 | $112.23 | $2.35 | 65 |
| 2025-07-17 14:26:31 | BUY | NVDA | 2 | $172.63 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | AMD | 2 | $160.08 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | DIS | 3 | $121.17 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | NKE | 3 | $72.73 | N/A | 75 |
| 2025-07-17 14:26:31 | BUY | UNP | 1 | $231.18 | N/A | 75 |
| 2025-07-17 14:08:25 | SELL | XOM | 1 | $112.00 | $2.02 | 70 |
| 2025-07-17 14:08:25 | SELL | WFC | 4 | $80.25 | $5.45 | 65 |
| 2025-07-17 14:08:25 | SELL | CSCO | 1 | $67.37 | $-1.08 | 65 |
| 2025-07-17 14:08:25 | SELL | CVX | 1 | $149.52 | $2.69 | 70 |
| 2025-07-17 14:08:25 | BUY | DIS | 1 | $121.55 | N/A | 75 |
| 2025-07-17 13:49:19 | SELL | NKE | 4 | $72.76 | $3.08 | 65 |
| 2025-07-17 13:49:19 | SELL | UNP | 1 | $230.08 | $-6.14 | 65 |
| 2025-07-17 13:49:19 | BUY | INTC | 7 | $22.67 | N/A | 65 |

<!--TRADE_LOG_END--> 
