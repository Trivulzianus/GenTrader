# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 20:09:20**

| Metric | Value |
|---|---|
| **Total Value** | **$100,729.63** |
| Cash | $2,047.93 |
| Holdings Value | $98,681.70 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.27 | $211.16 | $2,322.76 | 70 |
| ADBE | 5 | $377.60 | $363.35 | $1,816.75 | 65 |
| AMD | 15 | $134.63 | $146.42 | $2,196.30 | 70 |
| AMZN | 11 | $221.97 | $225.02 | $2,475.22 | 85 |
| AVGO | 8 | $275.34 | $274.38 | $2,195.04 | 70 |
| AXP | 7 | $325.34 | $319.51 | $2,236.55 | 75 |
| BA | 10 | $212.59 | $226.81 | $2,268.15 | 70 |
| BAC | 47 | $48.70 | $46.71 | $2,195.37 | 70 |
| C | 25 | $86.65 | $86.69 | $2,167.25 | 70 |
| CAT | 5 | $396.39 | $405.77 | $2,028.85 | 75 |
| COST | 2 | $979.83 | $970.33 | $1,940.66 | 65 |
| CRM | 7 | $268.68 | $258.07 | $1,806.49 | 65 |
| CSCO | 33 | $68.40 | $67.95 | $2,242.35 | 70 |
| CVX | 17 | $147.16 | $155.30 | $2,640.10 | 85 |
| DIS | 18 | $122.80 | $119.85 | $2,157.30 | 70 |
| GOOGL | 13 | $179.61 | $180.19 | $2,342.47 | 75 |
| GS | 3 | $717.52 | $704.45 | $2,113.35 | 70 |
| HD | 6 | $372.64 | $370.14 | $2,220.84 | 65 |
| INTC | 80 | $22.27 | $23.43 | $1,874.40 | 60 |
| JNJ | 13 | $155.89 | $156.86 | $2,039.18 | 65 |
| JPM | 8 | $292.23 | $286.68 | $2,293.44 | 70 |
| KO | 29 | $71.03 | $69.87 | $2,026.23 | 65 |
| LLY | 3 | $781.32 | $792.89 | $2,378.67 | 85 |
| MA | 4 | $563.08 | $550.11 | $2,200.44 | 70 |
| META | 3 | $717.12 | $717.51 | $2,152.53 | 75 |
| MRK | 26 | $82.34 | $83.30 | $2,165.80 | 70 |
| MSFT | 5 | $498.84 | $503.32 | $2,516.60 | 85 |
| NFLX | 1 | $1,279.00 | $1,245.11 | $1,245.11 | 65 |
| NKE | 30 | $75.87 | $72.67 | $2,180.10 | 70 |
| NVDA | 16 | $157.38 | $164.92 | $2,638.72 | 85 |
| ORCL | 9 | $233.26 | $230.41 | $2,073.69 | 70 |
| PEP | 15 | $136.57 | $135.26 | $2,028.90 | 65 |
| PFE | 79 | $25.17 | $25.64 | $2,025.95 | 65 |
| PG | 13 | $160.78 | $156.94 | $2,040.22 | 65 |
| PYPL | 28 | $72.13 | $71.36 | $1,998.08 | 65 |
| QCOM | 13 | $162.18 | $157.46 | $2,046.98 | 70 |
| T | 75 | $27.11 | $26.96 | $2,022.38 | 65 |
| TGT | 20 | $104.91 | $104.25 | $2,085.00 | 65 |
| TSLA | 6 | $288.62 | $313.51 | $1,881.06 | 65 |
| UNH | 7 | $298.51 | $303.85 | $2,126.91 | 70 |
| UNP | 10 | $236.18 | $235.11 | $2,351.10 | 75 |
| V | 6 | $355.85 | $347.82 | $2,086.92 | 65 |
| VZ | 49 | $43.12 | $41.62 | $2,039.37 | 65 |
| WFC | 29 | $82.28 | $82.53 | $2,393.37 | 75 |
| WMT | 21 | $97.38 | $94.36 | $1,981.56 | 65 |
| XOM | 21 | $109.99 | $115.39 | $2,423.19 | 75 |

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
| 2025-07-11 20:09:14 | SELL | INTC | 7 | $23.43 | $7.46 | 60 |
| 2025-07-11 20:09:14 | SELL | NKE | 1 | $72.67 | $-3.10 | 70 |
| 2025-07-11 20:09:14 | SELL | PFE | 12 | $25.65 | $4.93 | 65 |
| 2025-07-11 20:09:14 | BUY | WMT | 1 | $94.36 | N/A | 65 |
| 2025-07-11 19:50:20 | SELL | WMT | 2 | $94.42 | $-5.66 | 60 |
| 2025-07-11 19:50:20 | SELL | BA | 1 | $226.44 | $12.59 | 70 |
| 2025-07-11 19:50:20 | SELL | CSCO | 1 | $68.00 | $-0.38 | 70 |
| 2025-07-11 19:50:20 | BUY | MRK | 1 | $83.46 | N/A | 70 |
| 2025-07-11 19:50:20 | BUY | PFE | 11 | $25.69 | N/A | 75 |
| 2025-07-11 19:50:20 | BUY | C | 1 | $86.91 | N/A | 70 |
| 2025-07-11 19:50:20 | BUY | T | 5 | $27.00 | N/A | 65 |
| 2025-07-11 19:36:57 | SELL | AMD | 1 | $146.60 | $11.22 | 70 |
| 2025-07-11 19:36:57 | SELL | C | 2 | $86.85 | $0.40 | 65 |
| 2025-07-11 19:36:57 | SELL | T | 6 | $27.09 | $-0.17 | 60 |
| 2025-07-11 19:36:57 | BUY | AAPL | 1 | $211.14 | N/A | 75 |
| 2025-07-11 19:36:57 | BUY | BA | 1 | $226.66 | N/A | 85 |
| 2025-07-11 19:24:57 | SELL | XOM | 2 | $115.43 | $9.94 | 75 |
| 2025-07-11 19:24:57 | SELL | C | 1 | $86.78 | $0.12 | 70 |
| 2025-07-11 19:24:57 | BUY | DIS | 1 | $120.19 | N/A | 70 |
| 2025-07-11 19:24:57 | BUY | CSCO | 1 | $68.08 | N/A | 75 |
| 2025-07-11 19:07:37 | SELL | PFE | 5 | $25.62 | $2.14 | 65 |
| 2025-07-11 19:07:37 | SELL | BA | 1 | $226.55 | $12.71 | 70 |
| 2025-07-11 19:07:37 | BUY | AMD | 1 | $146.18 | N/A | 75 |
| 2025-07-11 19:07:37 | BUY | C | 1 | $86.73 | N/A | 75 |
| 2025-07-11 18:56:16 | SELL | AMD | 2 | $146.87 | $21.55 | 70 |

<!--TRADE_LOG_END--> 
