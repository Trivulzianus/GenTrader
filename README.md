# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 17:40:04**

| Metric | Value |
|---|---|
| **Total Value** | **$101,518.11** |
| Cash | $2,207.55 |
| Holdings Value | $99,310.56 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.81 | $2,128.10 | 75 |
| ADBE | 5 | $377.60 | $372.50 | $1,862.47 | 65 |
| AMD | 16 | $135.49 | $144.40 | $2,310.40 | 75 |
| AMZN | 11 | $221.97 | $222.65 | $2,449.10 | 85 |
| AVGO | 8 | $275.34 | $274.61 | $2,196.88 | 70 |
| AXP | 7 | $325.28 | $324.21 | $2,269.47 | 70 |
| BA | 9 | $210.97 | $224.93 | $2,024.37 | 70 |
| BAC | 49 | $48.60 | $46.97 | $2,301.29 | 75 |
| C | 30 | $86.81 | $86.80 | $2,603.85 | 85 |
| CAT | 6 | $397.86 | $409.71 | $2,458.26 | 75 |
| COST | 2 | $979.83 | $972.25 | $1,944.50 | 65 |
| CRM | 8 | $268.33 | $266.70 | $2,133.60 | 65 |
| CSCO | 32 | $68.36 | $68.84 | $2,202.88 | 70 |
| CVX | 16 | $146.74 | $153.89 | $2,462.24 | 85 |
| DIS | 18 | $122.80 | $121.32 | $2,183.76 | 70 |
| GOOGL | 13 | $179.61 | $178.00 | $2,314.00 | 75 |
| GS | 3 | $717.52 | $707.73 | $2,123.18 | 85 |
| HD | 6 | $372.64 | $377.12 | $2,262.75 | 70 |
| INTC | 84 | $22.27 | $23.79 | $1,998.36 | 65 |
| JNJ | 13 | $155.89 | $157.38 | $2,045.94 | 65 |
| JPM | 9 | $291.61 | $287.33 | $2,585.97 | 85 |
| KO | 29 | $71.03 | $69.52 | $2,015.93 | 65 |
| LLY | 2 | $776.66 | $794.41 | $1,588.82 | 70 |
| MA | 4 | $563.08 | $564.57 | $2,258.28 | 70 |
| META | 3 | $717.12 | $725.10 | $2,175.30 | 85 |
| MRK | 28 | $82.46 | $84.64 | $2,369.92 | 75 |
| MSFT | 5 | $498.84 | $501.01 | $2,505.05 | 85 |
| NFLX | 1 | $1,279.00 | $1,250.28 | $1,250.28 | 65 |
| NKE | 30 | $75.81 | $75.35 | $2,260.50 | 75 |
| NVDA | 14 | $156.61 | $163.85 | $2,293.97 | 70 |
| ORCL | 9 | $233.31 | $236.40 | $2,127.56 | 70 |
| PEP | 15 | $136.57 | $136.25 | $2,043.75 | 65 |
| PFE | 78 | $25.15 | $25.83 | $2,014.73 | 65 |
| PG | 12 | $160.91 | $159.03 | $1,908.42 | 60 |
| PYPL | 30 | $76.66 | $76.16 | $2,284.80 | 75 |
| QCOM | 16 | $161.59 | $159.79 | $2,556.72 | 85 |
| T | 73 | $28.55 | $27.64 | $2,017.36 | 65 |
| TGT | 19 | $104.85 | $106.14 | $2,016.66 | 65 |
| TSLA | 6 | $288.62 | $303.50 | $1,821.00 | 60 |
| UNH | 6 | $298.34 | $302.69 | $1,816.14 | 65 |
| UNP | 9 | $236.20 | $238.16 | $2,143.49 | 75 |
| V | 6 | $355.85 | $357.00 | $2,141.97 | 65 |
| VZ | 48 | $43.15 | $41.98 | $2,015.28 | 65 |
| WFC | 28 | $82.32 | $82.41 | $2,307.48 | 75 |
| WMT | 21 | $97.36 | $94.97 | $1,994.37 | 65 |
| XOM | 22 | $110.12 | $114.61 | $2,521.42 | 85 |

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
| 2025-07-10 17:39:54 | SELL | PFE | 5 | $25.83 | $3.20 | 65 |
| 2025-07-10 17:39:54 | SELL | WFC | 4 | $82.40 | $0.31 | 75 |
| 2025-07-10 17:39:54 | SELL | AMD | 2 | $144.39 | $15.83 | 75 |
| 2025-07-10 17:39:54 | SELL | PG | 1 | $159.08 | $-1.69 | 60 |
| 2025-07-10 17:39:54 | SELL | CSCO | 2 | $68.84 | $0.91 | 70 |
| 2025-07-10 17:39:54 | SELL | TGT | 1 | $106.18 | $1.27 | 65 |
| 2025-07-10 17:39:54 | BUY | AMZN | 1 | $222.60 | N/A | 85 |
| 2025-07-10 17:39:54 | BUY | BAC | 1 | $46.84 | N/A | 75 |
| 2025-07-10 17:39:54 | BUY | XOM | 1 | $114.62 | N/A | 85 |
| 2025-07-10 17:39:54 | BUY | NKE | 1 | $75.40 | N/A | 75 |
| 2025-07-10 17:39:54 | BUY | PYPL | 1 | $76.17 | N/A | 75 |
| 2025-07-10 17:39:54 | BUY | QCOM | 1 | $159.84 | N/A | 85 |
| 2025-07-10 17:39:54 | BUY | CVX | 1 | $153.91 | N/A | 85 |
| 2025-07-10 17:25:53 | SELL | NVDA | 2 | $163.37 | $11.84 | 70 |
| 2025-07-10 17:25:53 | SELL | XOM | 1 | $114.53 | $4.41 | 75 |
| 2025-07-10 17:25:53 | SELL | PYPL | 2 | $76.08 | $-1.11 | 70 |
| 2025-07-10 17:25:53 | SELL | CVX | 2 | $153.84 | $13.36 | 75 |
| 2025-07-10 17:25:53 | BUY | INTC | 5 | $23.72 | N/A | 65 |
| 2025-07-10 17:25:53 | BUY | BAC | 2 | $47.10 | N/A | 75 |
| 2025-07-10 17:25:53 | BUY | AMD | 2 | $144.12 | N/A | 85 |
| 2025-07-10 17:25:53 | BUY | PFE | 5 | $25.88 | N/A | 70 |
| 2025-07-10 17:25:53 | BUY | C | 3 | $86.80 | N/A | 85 |
| 2025-07-10 17:25:53 | BUY | TGT | 1 | $106.11 | N/A | 70 |
| 2025-07-10 17:10:42 | SELL | INTC | 5 | $23.69 | $7.15 | 60 |
| 2025-07-10 17:10:42 | SELL | PFE | 5 | $25.88 | $3.42 | 65 |

<!--TRADE_LOG_END--> 
