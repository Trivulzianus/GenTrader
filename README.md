# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 16:28:56**

| Metric | Value |
|---|---|
| **Total Value** | **$101,002.95** |
| Cash | $724.82 |
| Holdings Value | $100,278.13 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.92 | $2,109.20 | 65 |
| ADBE | 5 | $377.60 | $384.32 | $1,921.60 | 65 |
| AMD | 16 | $135.69 | $138.22 | $2,211.52 | 70 |
| AMZN | 10 | $221.61 | $220.94 | $2,209.35 | 70 |
| AVGO | 8 | $275.34 | $275.06 | $2,200.48 | 70 |
| AXP | 8 | $324.24 | $320.73 | $2,565.84 | 85 |
| BA | 9 | $211.84 | $217.93 | $1,961.37 | 65 |
| BAC | 46 | $48.76 | $47.18 | $2,170.28 | 70 |
| C | 30 | $86.60 | $86.24 | $2,587.20 | 85 |
| CAT | 6 | $397.86 | $394.03 | $2,364.18 | 70 |
| COST | 2 | $979.83 | $989.79 | $1,979.58 | 65 |
| CRM | 8 | $268.33 | $275.40 | $2,203.20 | 70 |
| CSCO | 32 | $68.35 | $68.80 | $2,201.44 | 70 |
| CVX | 16 | $146.69 | $152.30 | $2,436.80 | 75 |
| DIS | 17 | $122.85 | $122.66 | $2,085.22 | 70 |
| GOOGL | 12 | $179.60 | $174.59 | $2,095.08 | 65 |
| GS | 3 | $717.52 | $700.66 | $2,101.98 | 70 |
| HD | 6 | $372.64 | $369.75 | $2,218.50 | 65 |
| INTC | 86 | $22.31 | $23.38 | $2,010.25 | 65 |
| JNJ | 14 | $155.85 | $156.32 | $2,188.48 | 65 |
| JPM | 9 | $291.61 | $281.38 | $2,532.42 | 75 |
| KO | 29 | $71.03 | $70.22 | $2,036.24 | 65 |
| LLY | 2 | $776.66 | $790.04 | $1,580.08 | 65 |
| MA | 4 | $563.08 | $563.12 | $2,252.48 | 65 |
| META | 3 | $717.12 | $720.44 | $2,161.32 | 75 |
| MRK | 32 | $82.44 | $82.31 | $2,634.08 | 85 |
| MSFT | 5 | $498.84 | $496.04 | $2,480.22 | 75 |
| NFLX | 1 | $1,279.00 | $1,275.23 | $1,275.23 | 65 |
| NKE | 30 | $75.91 | $74.47 | $2,234.10 | 70 |
| NVDA | 16 | $156.72 | $159.72 | $2,555.60 | 85 |
| ORCL | 9 | $233.41 | $236.59 | $2,129.36 | 65 |
| PEP | 15 | $136.57 | $135.10 | $2,026.50 | 65 |
| PFE | 80 | $25.25 | $25.68 | $2,054.80 | 65 |
| PG | 13 | $160.77 | $158.74 | $2,063.62 | 65 |
| PYPL | 31 | $76.64 | $75.04 | $2,326.24 | 75 |
| QCOM | 14 | $161.75 | $160.67 | $2,249.38 | 75 |
| T | 82 | $28.52 | $28.39 | $2,327.57 | 75 |
| TGT | 20 | $104.90 | $102.14 | $2,042.90 | 65 |
| TSLA | 6 | $288.62 | $302.19 | $1,813.17 | 65 |
| UNH | 7 | $314.75 | $307.20 | $2,150.39 | 65 |
| UNP | 10 | $236.66 | $237.72 | $2,377.15 | 75 |
| V | 6 | $355.95 | $355.33 | $2,132.01 | 65 |
| VZ | 47 | $43.72 | $43.14 | $2,027.58 | 65 |
| WFC | 30 | $82.32 | $81.64 | $2,449.35 | 80 |
| WMT | 22 | $97.40 | $97.78 | $2,151.16 | 70 |
| XOM | 21 | $110.00 | $113.98 | $2,393.65 | 75 |

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
| 2025-07-08 16:28:46 | SELL | PFE | 12 | $25.68 | $4.43 | 65 |
| 2025-07-08 16:28:46 | SELL | CSCO | 2 | $68.78 | $0.81 | 70 |
| 2025-07-08 16:28:46 | BUY | NVDA | 2 | $159.84 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | INTC | 4 | $23.38 | N/A | 65 |
| 2025-07-08 16:28:46 | BUY | WMT | 1 | $97.81 | N/A | 70 |
| 2025-07-08 16:28:46 | BUY | MRK | 5 | $82.31 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | WFC | 1 | $81.61 | N/A | 80 |
| 2025-07-08 16:28:46 | BUY | C | 2 | $86.18 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | T | 5 | $28.36 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
