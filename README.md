# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-12 06:10:38**

| Metric | Value |
|---|---|
| **Total Value** | **$100,744.85** |
| Cash | $533.25 |
| Holdings Value | $100,211.60 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.16 | $2,111.60 | 65 |
| ADBE | 5 | $377.60 | $363.35 | $1,816.75 | 65 |
| AMD | 14 | $133.79 | $146.42 | $2,049.88 | 65 |
| AMZN | 11 | $221.97 | $225.02 | $2,475.22 | 85 |
| AVGO | 8 | $275.34 | $274.38 | $2,195.04 | 65 |
| AXP | 7 | $325.34 | $319.47 | $2,236.29 | 75 |
| BA | 10 | $212.59 | $226.84 | $2,268.40 | 75 |
| BAC | 50 | $48.58 | $46.73 | $2,336.50 | 75 |
| C | 30 | $86.66 | $86.73 | $2,601.90 | 85 |
| CAT | 6 | $397.98 | $405.92 | $2,435.52 | 70 |
| COST | 2 | $979.83 | $970.33 | $1,940.66 | 65 |
| CRM | 7 | $268.68 | $258.07 | $1,806.49 | 65 |
| CSCO | 34 | $68.38 | $67.95 | $2,310.30 | 75 |
| CVX | 17 | $147.16 | $155.31 | $2,640.27 | 85 |
| DIS | 17 | $122.98 | $119.87 | $2,037.79 | 65 |
| GOOGL | 14 | $179.65 | $180.19 | $2,522.66 | 80 |
| GS | 3 | $717.52 | $704.95 | $2,114.85 | 70 |
| HD | 6 | $372.64 | $370.07 | $2,220.42 | 65 |
| INTC | 86 | $22.35 | $23.43 | $2,014.98 | 65 |
| JNJ | 13 | $155.89 | $156.90 | $2,039.70 | 65 |
| JPM | 9 | $291.63 | $286.86 | $2,581.74 | 85 |
| KO | 29 | $71.03 | $69.87 | $2,026.23 | 65 |
| LLY | 3 | $781.32 | $793.01 | $2,379.03 | 70 |
| MA | 4 | $563.08 | $550.18 | $2,200.72 | 65 |
| META | 3 | $717.12 | $717.51 | $2,152.53 | 70 |
| MRK | 26 | $82.34 | $83.36 | $2,167.36 | 70 |
| MSFT | 5 | $498.84 | $503.32 | $2,516.60 | 70 |
| NFLX | 1 | $1,279.00 | $1,245.11 | $1,245.11 | 65 |
| NKE | 28 | $76.10 | $72.63 | $2,033.64 | 65 |
| NVDA | 16 | $157.38 | $164.92 | $2,638.72 | 85 |
| ORCL | 9 | $233.26 | $230.56 | $2,075.04 | 65 |
| PEP | 15 | $136.57 | $135.26 | $2,028.90 | 65 |
| PFE | 80 | $25.18 | $25.65 | $2,052.00 | 65 |
| PG | 13 | $160.78 | $157.05 | $2,041.65 | 65 |
| PYPL | 29 | $72.10 | $71.36 | $2,069.44 | 65 |
| QCOM | 14 | $161.84 | $157.46 | $2,204.44 | 75 |
| T | 81 | $27.10 | $26.97 | $2,184.57 | 70 |
| TGT | 20 | $104.91 | $104.24 | $2,084.80 | 65 |
| TSLA | 6 | $288.62 | $313.51 | $1,881.06 | 65 |
| UNH | 7 | $298.51 | $304.10 | $2,128.70 | 65 |
| UNP | 10 | $236.18 | $235.10 | $2,351.00 | 75 |
| V | 6 | $355.85 | $347.93 | $2,087.58 | 65 |
| VZ | 49 | $43.12 | $41.62 | $2,039.38 | 65 |
| WFC | 27 | $82.26 | $82.55 | $2,228.85 | 70 |
| WMT | 21 | $97.38 | $94.40 | $1,982.40 | 65 |
| XOM | 23 | $110.46 | $115.43 | $2,654.89 | 85 |

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
| 2025-07-12 06:10:32 | SELL | AMD | 1 | $146.42 | $11.79 | 65 |
| 2025-07-12 06:10:32 | SELL | NKE | 1 | $72.63 | $-3.35 | 65 |
| 2025-07-12 06:10:32 | SELL | PFE | 4 | $25.65 | $1.80 | 65 |
| 2025-07-12 06:10:32 | SELL | WFC | 1 | $82.55 | $0.28 | 70 |
| 2025-07-12 06:10:32 | BUY | INTC | 6 | $23.43 | N/A | 65 |
| 2025-07-12 06:10:32 | BUY | XOM | 2 | $115.43 | N/A | 85 |
| 2025-07-12 06:10:32 | BUY | CSCO | 2 | $67.95 | N/A | 75 |
| 2025-07-12 05:51:13 | SELL | INTC | 6 | $23.43 | $6.47 | 60 |
| 2025-07-12 05:40:02 | SELL | XOM | 1 | $115.43 | $5.19 | 75 |
| 2025-07-12 05:40:02 | BUY | NKE | 1 | $72.63 | N/A | 70 |
| 2025-07-12 05:40:02 | BUY | MRK | 1 | $83.36 | N/A | 70 |
| 2025-07-12 05:40:02 | BUY | PFE | 5 | $25.65 | N/A | 70 |
| 2025-07-12 05:25:50 | SELL | PFE | 6 | $25.65 | $2.67 | 65 |
| 2025-07-12 05:25:50 | SELL | MRK | 1 | $83.36 | $1.02 | 65 |
| 2025-07-12 05:25:50 | BUY | JPM | 1 | $286.86 | N/A | 85 |
| 2025-07-12 05:25:50 | BUY | XOM | 1 | $115.43 | N/A | 85 |
| 2025-07-12 05:09:02 | SELL | DIS | 1 | $119.87 | $-2.93 | 65 |
| 2025-07-12 05:09:02 | BUY | BAC | 3 | $46.73 | N/A | 75 |
| 2025-07-12 05:09:02 | BUY | MRK | 1 | $83.36 | N/A | 70 |
| 2025-07-12 05:09:02 | BUY | PFE | 1 | $25.65 | N/A | 70 |
| 2025-07-12 05:09:02 | BUY | WFC | 1 | $82.55 | N/A | 75 |
| 2025-07-12 04:54:47 | SELL | NKE | 1 | $72.63 | $-3.35 | 65 |
| 2025-07-12 04:54:47 | SELL | WFC | 2 | $82.55 | $0.54 | 70 |
| 2025-07-12 04:54:47 | BUY | INTC | 5 | $23.43 | N/A | 65 |
| 2025-07-12 04:54:47 | BUY | PFE | 4 | $25.65 | N/A | 70 |

<!--TRADE_LOG_END--> 
