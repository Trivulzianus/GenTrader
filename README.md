# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 16:09:59**

| Metric | Value |
|---|---|
| **Total Value** | **$100,749.11** |
| Cash | $1,597.49 |
| Holdings Value | $99,151.62 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.83 | $2,108.30 | 65 |
| ADBE | 5 | $377.60 | $383.75 | $1,918.77 | 65 |
| AMD | 16 | $135.69 | $137.50 | $2,200.00 | 70 |
| AMZN | 10 | $221.61 | $220.74 | $2,207.40 | 65 |
| AVGO | 8 | $275.34 | $274.70 | $2,197.60 | 70 |
| AXP | 8 | $324.24 | $319.62 | $2,556.96 | 85 |
| BA | 9 | $211.84 | $217.22 | $1,954.98 | 65 |
| BAC | 46 | $48.76 | $47.02 | $2,163.15 | 70 |
| C | 28 | $86.63 | $85.92 | $2,405.76 | 75 |
| CAT | 6 | $397.86 | $392.96 | $2,357.76 | 70 |
| COST | 2 | $979.83 | $990.66 | $1,981.32 | 70 |
| CRM | 8 | $268.33 | $274.47 | $2,195.76 | 65 |
| CSCO | 34 | $68.37 | $68.56 | $2,330.87 | 75 |
| CVX | 16 | $146.69 | $151.25 | $2,420.00 | 75 |
| DIS | 17 | $122.85 | $122.43 | $2,081.31 | 65 |
| GOOGL | 12 | $179.60 | $174.31 | $2,091.68 | 65 |
| GS | 3 | $717.52 | $699.08 | $2,097.24 | 70 |
| HD | 6 | $372.64 | $368.74 | $2,212.41 | 70 |
| INTC | 82 | $22.25 | $23.23 | $1,904.86 | 60 |
| JNJ | 14 | $155.85 | $156.00 | $2,183.93 | 65 |
| JPM | 9 | $291.61 | $281.16 | $2,530.44 | 85 |
| KO | 29 | $71.03 | $70.08 | $2,032.32 | 65 |
| LLY | 2 | $776.66 | $788.50 | $1,577.00 | 65 |
| MA | 4 | $563.08 | $563.24 | $2,252.96 | 65 |
| META | 3 | $717.12 | $720.69 | $2,162.07 | 70 |
| MRK | 27 | $82.46 | $81.94 | $2,212.38 | 70 |
| MSFT | 5 | $498.84 | $495.50 | $2,477.50 | 85 |
| NFLX | 1 | $1,279.00 | $1,275.62 | $1,275.62 | 65 |
| NKE | 30 | $75.91 | $73.99 | $2,219.70 | 70 |
| NVDA | 14 | $156.27 | $159.35 | $2,230.97 | 70 |
| ORCL | 9 | $233.41 | $235.76 | $2,121.88 | 70 |
| PEP | 15 | $136.57 | $134.71 | $2,020.65 | 65 |
| PFE | 92 | $25.31 | $25.64 | $2,358.42 | 75 |
| PG | 13 | $160.77 | $158.43 | $2,059.59 | 65 |
| PYPL | 31 | $76.64 | $74.88 | $2,321.17 | 75 |
| QCOM | 14 | $161.75 | $160.17 | $2,242.38 | 75 |
| T | 77 | $28.53 | $28.34 | $2,182.18 | 70 |
| TGT | 20 | $104.90 | $101.81 | $2,036.20 | 65 |
| TSLA | 6 | $288.62 | $302.20 | $1,813.20 | 65 |
| UNH | 7 | $314.75 | $305.99 | $2,141.93 | 65 |
| UNP | 10 | $236.66 | $236.88 | $2,368.80 | 75 |
| V | 6 | $355.95 | $354.88 | $2,129.28 | 65 |
| VZ | 47 | $43.72 | $43.10 | $2,025.70 | 65 |
| WFC | 29 | $82.34 | $81.34 | $2,358.86 | 75 |
| WMT | 21 | $97.39 | $97.67 | $2,051.07 | 65 |
| XOM | 21 | $110.00 | $113.30 | $2,379.30 | 75 |

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
| 2025-07-08 16:09:53 | SELL | XOM | 2 | $113.31 | $6.04 | 75 |
| 2025-07-08 16:09:53 | SELL | WMT | 3 | $97.66 | $0.72 | 65 |
| 2025-07-08 16:09:53 | SELL | MRK | 2 | $81.93 | $-0.99 | 70 |
| 2025-07-08 16:09:53 | SELL | C | 3 | $85.91 | $-1.96 | 75 |
| 2025-07-08 16:09:53 | BUY | PFE | 6 | $25.62 | N/A | 75 |
| 2025-07-08 16:09:53 | BUY | CSCO | 2 | $68.56 | N/A | 75 |
| 2025-07-08 16:09:53 | BUY | T | 5 | $28.33 | N/A | 70 |
| 2025-07-08 15:51:38 | SELL | NVDA | 2 | $159.14 | $5.01 | 70 |
| 2025-07-08 15:51:38 | SELL | INTC | 3 | $23.18 | $2.68 | 60 |
| 2025-07-08 15:51:38 | SELL | PFE | 4 | $25.78 | $1.92 | 70 |
| 2025-07-08 15:51:38 | SELL | T | 4 | $28.36 | $-0.66 | 65 |
| 2025-07-08 15:51:38 | BUY | JNJ | 1 | $156.38 | N/A | 70 |
| 2025-07-08 15:51:38 | BUY | WMT | 1 | $97.38 | N/A | 75 |
| 2025-07-08 15:51:38 | BUY | C | 1 | $86.11 | N/A | 85 |
| 2025-07-08 15:39:25 | SELL | BAC | 1 | $47.29 | $-1.43 | 70 |
| 2025-07-08 15:39:25 | SELL | INTC | 3 | $22.00 | $-0.83 | 60 |
| 2025-07-08 15:39:25 | SELL | UNP | 1 | $237.31 | $0.59 | 75 |
| 2025-07-08 15:39:25 | SELL | CSCO | 1 | $68.58 | $0.22 | 70 |
| 2025-07-08 15:39:25 | BUY | XOM | 1 | $113.43 | N/A | 85 |
| 2025-07-08 15:39:25 | BUY | WMT | 2 | $97.29 | N/A | 75 |
| 2025-07-08 15:39:25 | BUY | PFE | 9 | $25.76 | N/A | 75 |
| 2025-07-08 15:39:25 | BUY | C | 2 | $86.16 | N/A | 85 |
| 2025-07-08 15:39:25 | BUY | T | 3 | $28.25 | N/A | 70 |
| 2025-07-08 15:26:24 | SELL | XOM | 1 | $113.18 | $2.90 | 75 |
| 2025-07-08 15:26:24 | SELL | DIS | 1 | $122.26 | $-0.55 | 65 |

<!--TRADE_LOG_END--> 
