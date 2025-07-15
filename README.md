# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 16:10:13**

| Metric | Value |
|---|---|
| **Total Value** | **$100,640.28** |
| Cash | $1,032.06 |
| Holdings Value | $99,608.22 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.57 | $2,105.75 | 65 |
| ADBE | 6 | $375.23 | $364.62 | $2,187.72 | 65 |
| AMD | 17 | $146.29 | $156.25 | $2,656.19 | 85 |
| AMZN | 10 | $221.60 | $226.63 | $2,266.30 | 75 |
| AVGO | 8 | $275.34 | $281.10 | $2,248.80 | 70 |
| AXP | 7 | $325.34 | $312.55 | $2,187.85 | 65 |
| BA | 11 | $214.40 | $231.42 | $2,545.62 | 85 |
| BAC | 44 | $48.83 | $46.47 | $2,044.68 | 65 |
| C | 30 | $86.78 | $89.59 | $2,687.70 | 85 |
| CAT | 6 | $397.74 | $405.49 | $2,432.91 | 85 |
| COST | 2 | $979.83 | $968.09 | $1,936.18 | 65 |
| CRM | 8 | $267.44 | $258.19 | $2,065.52 | 65 |
| CSCO | 31 | $68.46 | $67.34 | $2,087.54 | 65 |
| CVX | 16 | $146.80 | $150.93 | $2,414.89 | 75 |
| DIS | 17 | $122.96 | $119.32 | $2,028.44 | 65 |
| GOOGL | 14 | $179.71 | $183.12 | $2,563.68 | 85 |
| GS | 3 | $717.52 | $705.28 | $2,115.84 | 75 |
| HD | 6 | $372.64 | $363.31 | $2,179.86 | 65 |
| INTC | 87 | $22.37 | $23.36 | $2,031.88 | 65 |
| JNJ | 13 | $155.95 | $155.18 | $2,017.34 | 65 |
| JPM | 9 | $291.63 | $286.68 | $2,580.12 | 85 |
| KO | 30 | $70.97 | $69.22 | $2,076.45 | 65 |
| LLY | 3 | $781.32 | $773.84 | $2,321.52 | 70 |
| MA | 4 | $563.08 | $549.08 | $2,196.30 | 65 |
| META | 3 | $717.12 | $718.09 | $2,154.27 | 70 |
| MRK | 25 | $82.54 | $81.64 | $2,041.00 | 65 |
| MSFT | 5 | $498.84 | $506.37 | $2,531.85 | 75 |
| NFLX | 1 | $1,279.00 | $1,260.00 | $1,260.00 | 65 |
| NKE | 30 | $72.04 | $72.03 | $2,160.90 | 70 |
| NVDA | 13 | $171.78 | $171.29 | $2,226.77 | 70 |
| ORCL | 9 | $233.27 | $232.21 | $2,089.85 | 65 |
| PEP | 15 | $136.57 | $134.04 | $2,010.60 | 65 |
| PFE | 83 | $25.22 | $24.76 | $2,055.07 | 65 |
| PG | 13 | $152.12 | $152.50 | $1,982.50 | 65 |
| PYPL | 28 | $72.13 | $73.51 | $2,058.28 | 65 |
| QCOM | 14 | $153.83 | $154.63 | $2,164.82 | 70 |
| T | 77 | $27.09 | $26.89 | $2,070.53 | 65 |
| TGT | 20 | $104.94 | $103.20 | $2,064.00 | 65 |
| TSLA | 6 | $318.51 | $314.41 | $1,886.48 | 65 |
| UNH | 7 | $298.51 | $294.81 | $2,063.67 | 65 |
| UNP | 9 | $236.54 | $232.49 | $2,092.41 | 65 |
| V | 6 | $355.85 | $347.07 | $2,082.42 | 65 |
| VZ | 50 | $43.08 | $41.20 | $2,060.25 | 65 |
| WFC | 28 | $78.71 | $78.65 | $2,202.20 | 70 |
| WMT | 21 | $97.38 | $95.23 | $1,999.83 | 65 |
| XOM | 21 | $109.99 | $112.92 | $2,371.42 | 75 |

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
| 2025-07-15 16:10:04 | SELL | BAC | 1 | $46.51 | $-2.28 | 65 |
| 2025-07-15 16:10:04 | SELL | T | 5 | $26.89 | $-0.98 | 65 |
| 2025-07-15 16:10:04 | BUY | INTC | 5 | $23.37 | N/A | 65 |
| 2025-07-15 16:10:04 | BUY | WFC | 1 | $78.69 | N/A | 70 |
| 2025-07-15 15:51:49 | SELL | BAC | 2 | $46.65 | $-4.09 | 65 |
| 2025-07-15 15:51:49 | SELL | PYPL | 1 | $73.72 | $1.53 | 65 |
| 2025-07-15 15:51:49 | BUY | NKE | 1 | $72.13 | N/A | 70 |
| 2025-07-15 15:51:49 | BUY | BA | 2 | $230.76 | N/A | 80 |
| 2025-07-15 15:51:49 | BUY | T | 5 | $26.86 | N/A | 70 |
| 2025-07-15 15:40:17 | SELL | NVDA | 1 | $171.33 | $-0.42 | 70 |
| 2025-07-15 15:40:17 | SELL | INTC | 6 | $23.37 | $5.90 | 60 |
| 2025-07-15 15:40:17 | SELL | PYPL | 1 | $73.64 | $1.41 | 65 |
| 2025-07-15 15:40:17 | SELL | WFC | 1 | $78.91 | $0.19 | 65 |
| 2025-07-15 15:40:17 | BUY | GOOGL | 1 | $183.45 | N/A | 85 |
| 2025-07-15 15:40:17 | BUY | BAC | 3 | $46.65 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
