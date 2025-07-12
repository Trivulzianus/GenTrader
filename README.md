# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-12 20:08:25**

| Metric | Value |
|---|---|
| **Total Value** | **$100,744.85** |
| Cash | $754.31 |
| Holdings Value | $99,990.54 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.16 | $2,111.60 | 65 |
| ADBE | 5 | $377.60 | $363.35 | $1,816.75 | 65 |
| AMD | 16 | $135.37 | $146.42 | $2,342.72 | 75 |
| AMZN | 11 | $221.97 | $225.02 | $2,475.22 | 85 |
| AVGO | 8 | $275.34 | $274.38 | $2,195.04 | 70 |
| AXP | 7 | $325.34 | $319.47 | $2,236.29 | 75 |
| BA | 9 | $211.01 | $226.84 | $2,041.56 | 65 |
| BAC | 50 | $48.58 | $46.73 | $2,336.50 | 75 |
| C | 26 | $86.65 | $86.73 | $2,254.98 | 75 |
| CAT | 6 | $397.98 | $405.92 | $2,435.52 | 70 |
| COST | 2 | $979.83 | $970.33 | $1,940.66 | 65 |
| CRM | 7 | $268.68 | $258.07 | $1,806.49 | 65 |
| CSCO | 32 | $68.41 | $67.95 | $2,174.40 | 70 |
| CVX | 17 | $147.16 | $155.31 | $2,640.27 | 85 |
| DIS | 17 | $122.98 | $119.87 | $2,037.79 | 65 |
| GOOGL | 14 | $179.65 | $180.19 | $2,522.66 | 85 |
| GS | 3 | $717.52 | $704.95 | $2,114.85 | 70 |
| HD | 6 | $372.64 | $370.07 | $2,220.42 | 65 |
| INTC | 87 | $22.36 | $23.43 | $2,038.41 | 65 |
| JNJ | 13 | $155.89 | $156.90 | $2,039.70 | 65 |
| JPM | 9 | $291.63 | $286.86 | $2,581.74 | 85 |
| KO | 29 | $71.03 | $69.87 | $2,026.23 | 65 |
| LLY | 3 | $781.32 | $793.01 | $2,379.03 | 70 |
| MA | 4 | $563.08 | $550.18 | $2,200.72 | 65 |
| META | 3 | $717.12 | $717.51 | $2,152.53 | 70 |
| MRK | 25 | $82.30 | $83.36 | $2,084.00 | 65 |
| MSFT | 5 | $498.84 | $503.32 | $2,516.60 | 75 |
| NFLX | 1 | $1,279.00 | $1,245.11 | $1,245.11 | 65 |
| NKE | 30 | $75.87 | $72.63 | $2,178.90 | 70 |
| NVDA | 16 | $157.38 | $164.92 | $2,638.72 | 85 |
| ORCL | 9 | $233.26 | $230.56 | $2,075.04 | 65 |
| PEP | 15 | $136.57 | $135.26 | $2,028.90 | 65 |
| PFE | 85 | $25.21 | $25.65 | $2,180.25 | 70 |
| PG | 13 | $160.78 | $157.05 | $2,041.65 | 65 |
| PYPL | 29 | $72.10 | $71.36 | $2,069.44 | 65 |
| QCOM | 15 | $161.55 | $157.46 | $2,361.90 | 75 |
| T | 80 | $27.10 | $26.97 | $2,157.60 | 70 |
| TGT | 20 | $104.91 | $104.24 | $2,084.80 | 65 |
| TSLA | 6 | $288.62 | $313.51 | $1,881.06 | 65 |
| UNH | 7 | $298.51 | $304.10 | $2,128.70 | 65 |
| UNP | 10 | $236.18 | $235.10 | $2,351.00 | 75 |
| V | 6 | $355.85 | $347.93 | $2,087.58 | 70 |
| VZ | 49 | $43.12 | $41.62 | $2,039.38 | 65 |
| WFC | 28 | $82.27 | $82.55 | $2,311.40 | 75 |
| WMT | 21 | $97.38 | $94.40 | $1,982.40 | 65 |
| XOM | 21 | $109.99 | $115.43 | $2,424.03 | 75 |

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
| 2025-07-12 20:08:19 | SELL | MRK | 1 | $83.36 | $1.02 | 65 |
| 2025-07-12 20:08:19 | SELL | PEP | 1 | $135.26 | $-1.23 | 65 |
| 2025-07-12 20:08:19 | BUY | NKE | 1 | $72.63 | N/A | 70 |
| 2025-07-12 20:08:19 | BUY | T | 4 | $26.97 | N/A | 70 |
| 2025-07-12 19:50:09 | SELL | DIS | 1 | $119.87 | $-2.93 | 65 |
| 2025-07-12 19:50:09 | BUY | PFE | 5 | $25.65 | N/A | 70 |
| 2025-07-12 19:35:45 | SELL | NKE | 1 | $72.63 | $-3.24 | 65 |
| 2025-07-12 19:35:45 | BUY | MRK | 1 | $83.36 | N/A | 70 |
| 2025-07-12 19:23:19 | SELL | PFE | 5 | $25.65 | $2.22 | 65 |
| 2025-07-12 19:23:19 | SELL | C | 4 | $86.73 | $0.27 | 70 |
| 2025-07-12 19:23:19 | SELL | T | 5 | $26.97 | $-0.64 | 65 |
| 2025-07-12 19:23:19 | BUY | NKE | 4 | $72.63 | N/A | 70 |
| 2025-07-12 19:23:19 | BUY | WMT | 1 | $94.40 | N/A | 65 |
| 2025-07-12 19:07:01 | SELL | XOM | 2 | $115.43 | $9.93 | 75 |
| 2025-07-12 19:07:01 | SELL | NKE | 3 | $72.63 | $-10.06 | 60 |
| 2025-07-12 19:07:01 | SELL | MRK | 1 | $83.36 | $1.02 | 65 |
| 2025-07-12 19:07:01 | SELL | WMT | 1 | $94.40 | $-2.98 | 60 |
| 2025-07-12 19:07:01 | BUY | NVDA | 1 | $164.92 | N/A | 85 |
| 2025-07-12 19:07:01 | BUY | PFE | 5 | $25.65 | N/A | 70 |
| 2025-07-12 19:07:01 | BUY | C | 6 | $86.73 | N/A | 85 |
| 2025-07-12 19:07:01 | BUY | T | 5 | $26.97 | N/A | 70 |
| 2025-07-12 18:54:27 | SELL | NVDA | 1 | $164.92 | $7.54 | 75 |
| 2025-07-12 18:54:27 | BUY | INTC | 6 | $23.43 | N/A | 65 |
| 2025-07-12 18:54:27 | BUY | DIS | 1 | $119.87 | N/A | 70 |
| 2025-07-12 18:54:27 | BUY | XOM | 2 | $115.43 | N/A | 85 |

<!--TRADE_LOG_END--> 
