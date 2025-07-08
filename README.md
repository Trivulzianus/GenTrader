# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 18:57:20**

| Metric | Value |
|---|---|
| **Total Value** | **$100,753.66** |
| Cash | $465.44 |
| Holdings Value | $100,288.22 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.78 | $2,097.80 | 70 |
| ADBE | 5 | $377.60 | $381.87 | $1,909.36 | 65 |
| AMD | 16 | $135.69 | $138.07 | $2,209.13 | 70 |
| AMZN | 10 | $221.61 | $219.85 | $2,198.49 | 65 |
| AVGO | 8 | $275.34 | $273.05 | $2,184.36 | 70 |
| AXP | 8 | $324.24 | $318.98 | $2,551.84 | 80 |
| BA | 10 | $212.43 | $218.87 | $2,188.65 | 70 |
| BAC | 50 | $48.63 | $47.33 | $2,366.25 | 75 |
| C | 26 | $86.68 | $85.91 | $2,233.53 | 70 |
| CAT | 6 | $397.86 | $395.38 | $2,372.25 | 70 |
| COST | 2 | $979.83 | $985.25 | $1,970.50 | 65 |
| CRM | 8 | $268.33 | $273.74 | $2,189.92 | 65 |
| CSCO | 34 | $68.36 | $68.67 | $2,334.61 | 75 |
| CVX | 16 | $146.71 | $152.49 | $2,439.84 | 75 |
| DIS | 17 | $122.85 | $122.12 | $2,076.04 | 65 |
| GOOGL | 12 | $179.60 | $173.63 | $2,083.56 | 65 |
| GS | 3 | $717.52 | $697.78 | $2,093.34 | 70 |
| HD | 6 | $372.64 | $367.82 | $2,206.92 | 65 |
| INTC | 86 | $22.32 | $23.64 | $2,033.47 | 65 |
| JNJ | 13 | $155.89 | $155.40 | $2,020.22 | 65 |
| JPM | 9 | $291.61 | $282.55 | $2,542.95 | 85 |
| KO | 29 | $71.03 | $70.34 | $2,040.00 | 65 |
| LLY | 2 | $776.66 | $782.63 | $1,565.26 | 65 |
| MA | 4 | $563.08 | $561.81 | $2,247.24 | 65 |
| META | 3 | $717.12 | $718.69 | $2,156.07 | 75 |
| MRK | 29 | $82.50 | $81.47 | $2,362.63 | 75 |
| MSFT | 5 | $498.84 | $496.15 | $2,480.75 | 75 |
| NFLX | 1 | $1,279.00 | $1,272.44 | $1,272.44 | 65 |
| NKE | 29 | $75.97 | $73.89 | $2,142.81 | 70 |
| NVDA | 17 | $157.07 | $159.72 | $2,715.24 | 85 |
| ORCL | 9 | $233.41 | $234.38 | $2,109.38 | 70 |
| PEP | 15 | $136.57 | $135.05 | $2,025.75 | 65 |
| PFE | 91 | $25.26 | $25.62 | $2,331.88 | 75 |
| PG | 13 | $160.77 | $158.09 | $2,055.19 | 70 |
| PYPL | 31 | $76.65 | $74.74 | $2,316.94 | 75 |
| QCOM | 15 | $161.62 | $160.07 | $2,401.05 | 75 |
| T | 76 | $28.54 | $28.41 | $2,159.16 | 70 |
| TGT | 20 | $104.90 | $102.07 | $2,041.45 | 65 |
| TSLA | 6 | $288.62 | $302.13 | $1,812.81 | 65 |
| UNH | 7 | $314.75 | $306.61 | $2,146.27 | 65 |
| UNP | 10 | $236.66 | $237.10 | $2,371.00 | 75 |
| V | 6 | $355.95 | $353.98 | $2,123.88 | 65 |
| VZ | 47 | $43.16 | $43.06 | $2,024.05 | 65 |
| WFC | 30 | $82.31 | $81.65 | $2,449.50 | 80 |
| WMT | 23 | $97.35 | $97.41 | $2,240.43 | 70 |
| XOM | 21 | $110.02 | $114.00 | $2,394.00 | 75 |

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
| 2025-07-08 18:57:14 | SELL | XOM | 1 | $114.01 | $3.81 | 75 |
| 2025-07-08 18:57:14 | SELL | C | 2 | $85.92 | $-1.43 | 70 |
| 2025-07-08 18:57:14 | SELL | CVX | 1 | $152.49 | $5.44 | 75 |
| 2025-07-08 18:57:14 | BUY | WFC | 1 | $81.60 | N/A | 80 |
| 2025-07-08 18:57:14 | BUY | CSCO | 2 | $68.67 | N/A | 75 |
| 2025-07-08 18:57:14 | BUY | PFE | 6 | $25.62 | N/A | 75 |
| 2025-07-08 18:57:14 | BUY | T | 4 | $28.41 | N/A | 70 |
| 2025-07-08 18:45:11 | SELL | C | 2 | $85.97 | $-1.22 | 75 |
| 2025-07-08 18:45:11 | BUY | WMT | 2 | $97.38 | N/A | 75 |
| 2025-07-08 18:45:11 | BUY | CVX | 1 | $152.41 | N/A | 85 |
| 2025-07-08 18:27:39 | SELL | WMT | 2 | $97.54 | $0.37 | 65 |
| 2025-07-08 18:27:39 | SELL | XOM | 1 | $114.14 | $3.77 | 80 |
| 2025-07-08 18:27:39 | SELL | MRK | 1 | $81.34 | $-1.12 | 75 |
| 2025-07-08 18:27:39 | SELL | CSCO | 1 | $68.71 | $0.35 | 70 |
| 2025-07-08 18:27:39 | SELL | T | 9 | $28.40 | $-1.18 | 65 |
| 2025-07-08 18:27:39 | BUY | NKE | 1 | $74.00 | N/A | 70 |
| 2025-07-08 18:27:39 | BUY | VZ | 1 | $43.12 | N/A | 65 |
| 2025-07-08 18:10:59 | SELL | JNJ | 1 | $155.35 | $-0.50 | 65 |
| 2025-07-08 18:10:59 | SELL | INTC | 2 | $23.68 | $2.67 | 65 |
| 2025-07-08 18:10:59 | SELL | BAC | 1 | $47.35 | $-1.26 | 75 |
| 2025-07-08 18:10:59 | SELL | NKE | 2 | $74.03 | $-3.76 | 65 |
| 2025-07-08 18:10:59 | SELL | PFE | 9 | $25.57 | $2.72 | 70 |
| 2025-07-08 18:10:59 | SELL | WFC | 2 | $81.79 | $-1.03 | 75 |
| 2025-07-08 18:10:59 | SELL | CVX | 1 | $152.79 | $5.72 | 75 |
| 2025-07-08 18:10:59 | BUY | WMT | 2 | $97.56 | N/A | 75 |

<!--TRADE_LOG_END--> 
