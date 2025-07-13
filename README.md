# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-13 19:50:19**

| Metric | Value |
|---|---|
| **Total Value** | **$100,744.85** |
| Cash | $1,427.26 |
| Holdings Value | $99,317.59 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.27 | $211.16 | $2,322.76 | 70 |
| ADBE | 5 | $377.60 | $363.35 | $1,816.75 | 65 |
| AMD | 14 | $133.79 | $146.42 | $2,049.88 | 70 |
| AMZN | 11 | $221.97 | $225.02 | $2,475.22 | 75 |
| AVGO | 8 | $275.34 | $274.38 | $2,195.04 | 65 |
| AXP | 7 | $325.34 | $319.47 | $2,236.29 | 75 |
| BA | 10 | $212.59 | $226.84 | $2,268.40 | 75 |
| BAC | 49 | $48.62 | $46.73 | $2,289.77 | 75 |
| C | 27 | $86.65 | $86.73 | $2,341.71 | 75 |
| CAT | 5 | $396.39 | $405.92 | $2,029.60 | 70 |
| COST | 2 | $979.83 | $970.33 | $1,940.66 | 65 |
| CRM | 7 | $268.68 | $258.07 | $1,806.49 | 65 |
| CSCO | 32 | $68.41 | $67.95 | $2,174.40 | 70 |
| CVX | 17 | $147.16 | $155.31 | $2,640.27 | 85 |
| DIS | 17 | $122.98 | $119.87 | $2,037.79 | 65 |
| GOOGL | 13 | $179.61 | $180.19 | $2,342.47 | 75 |
| GS | 3 | $717.52 | $704.95 | $2,114.85 | 85 |
| HD | 6 | $372.64 | $370.07 | $2,220.42 | 65 |
| INTC | 86 | $22.35 | $23.43 | $2,014.98 | 65 |
| JNJ | 13 | $155.89 | $156.90 | $2,039.70 | 65 |
| JPM | 8 | $292.23 | $286.86 | $2,294.88 | 70 |
| KO | 29 | $71.03 | $69.87 | $2,026.23 | 65 |
| LLY | 3 | $781.32 | $793.01 | $2,379.03 | 75 |
| MA | 4 | $563.08 | $550.18 | $2,200.72 | 65 |
| META | 3 | $717.12 | $717.51 | $2,152.53 | 85 |
| MRK | 26 | $82.34 | $83.36 | $2,167.36 | 70 |
| MSFT | 5 | $498.84 | $503.32 | $2,516.60 | 85 |
| NFLX | 1 | $1,279.00 | $1,245.11 | $1,245.11 | 65 |
| NKE | 30 | $75.87 | $72.63 | $2,178.90 | 70 |
| NVDA | 16 | $157.38 | $164.92 | $2,638.72 | 85 |
| ORCL | 9 | $233.26 | $230.56 | $2,075.04 | 70 |
| PEP | 15 | $136.57 | $135.26 | $2,028.90 | 65 |
| PFE | 84 | $25.20 | $25.65 | $2,154.60 | 70 |
| PG | 13 | $160.78 | $157.05 | $2,041.65 | 65 |
| PYPL | 29 | $72.10 | $71.36 | $2,069.44 | 65 |
| QCOM | 15 | $161.55 | $157.46 | $2,361.90 | 75 |
| T | 75 | $27.11 | $26.97 | $2,022.75 | 65 |
| TGT | 20 | $104.91 | $104.24 | $2,084.80 | 65 |
| TSLA | 6 | $288.62 | $313.51 | $1,881.06 | 65 |
| UNH | 7 | $298.51 | $304.10 | $2,128.70 | 65 |
| UNP | 10 | $236.18 | $235.10 | $2,351.00 | 75 |
| V | 6 | $355.85 | $347.93 | $2,087.58 | 65 |
| VZ | 49 | $43.12 | $41.62 | $2,039.38 | 65 |
| WFC | 28 | $82.27 | $82.55 | $2,311.40 | 75 |
| WMT | 21 | $97.38 | $94.40 | $1,982.40 | 65 |
| XOM | 22 | $110.24 | $115.43 | $2,539.46 | 85 |

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
| 2025-07-13 19:50:13 | SELL | C | 3 | $86.73 | $0.21 | 75 |
| 2025-07-13 19:50:13 | BUY | XOM | 1 | $115.43 | N/A | 85 |
| 2025-07-13 19:50:13 | BUY | PFE | 5 | $25.65 | N/A | 70 |
| 2025-07-13 19:36:43 | BUY | MRK | 1 | $83.36 | N/A | 70 |
| 2025-07-13 19:36:43 | BUY | C | 1 | $86.73 | N/A | 85 |
| 2025-07-13 19:23:58 | SELL | JPM | 1 | $286.86 | $-4.77 | 70 |
| 2025-07-13 19:23:58 | SELL | C | 1 | $86.73 | $0.07 | 80 |
| 2025-07-13 19:23:58 | SELL | VZ | 2 | $41.62 | $-2.88 | 65 |
| 2025-07-13 19:23:58 | BUY | BAC | 2 | $46.73 | N/A | 75 |
| 2025-07-13 19:23:58 | BUY | INTC | 1 | $23.43 | N/A | 65 |
| 2025-07-13 19:06:57 | SELL | BAC | 3 | $46.73 | $-5.56 | 70 |
| 2025-07-13 19:06:57 | SELL | PFE | 6 | $25.65 | $2.67 | 65 |
| 2025-07-13 19:06:57 | SELL | WFC | 1 | $82.55 | $0.27 | 75 |
| 2025-07-13 19:06:57 | BUY | JPM | 1 | $286.86 | N/A | 85 |
| 2025-07-13 19:06:57 | BUY | INTC | 5 | $23.43 | N/A | 65 |
| 2025-07-13 19:06:57 | BUY | C | 5 | $86.73 | N/A | 85 |
| 2025-07-13 19:06:57 | BUY | VZ | 3 | $41.62 | N/A | 70 |
| 2025-07-13 18:54:15 | SELL | MRK | 1 | $83.36 | $1.02 | 65 |
| 2025-07-13 18:54:15 | BUY | PFE | 1 | $25.65 | N/A | 70 |
| 2025-07-13 18:54:15 | BUY | PEP | 1 | $135.26 | N/A | 65 |
| 2025-07-13 18:43:14 | SELL | PEP | 1 | $135.26 | $-1.31 | 60 |
| 2025-07-13 18:43:14 | BUY | MRK | 1 | $83.36 | N/A | 70 |
| 2025-07-13 18:43:14 | BUY | PFE | 5 | $25.65 | N/A | 70 |
| 2025-07-13 18:26:59 | SELL | INTC | 6 | $23.43 | $6.47 | 60 |
| 2025-07-13 18:26:59 | SELL | MRK | 1 | $83.36 | $1.02 | 65 |

<!--TRADE_LOG_END--> 
