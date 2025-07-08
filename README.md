# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 17:08:43**

| Metric | Value |
|---|---|
| **Total Value** | **$100,716.49** |
| Cash | $925.65 |
| Holdings Value | $99,790.85 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.21 | $2,102.10 | 65 |
| ADBE | 5 | $377.60 | $381.10 | $1,905.48 | 65 |
| AMD | 16 | $135.69 | $137.96 | $2,207.36 | 70 |
| AMZN | 10 | $221.61 | $220.64 | $2,206.40 | 70 |
| AVGO | 8 | $275.34 | $275.49 | $2,203.88 | 70 |
| AXP | 8 | $324.24 | $320.04 | $2,560.32 | 85 |
| BA | 10 | $212.43 | $217.76 | $2,177.61 | 70 |
| BAC | 49 | $48.66 | $47.29 | $2,317.21 | 75 |
| C | 26 | $86.64 | $86.33 | $2,244.71 | 70 |
| CAT | 6 | $397.86 | $395.27 | $2,371.62 | 75 |
| COST | 2 | $979.83 | $989.35 | $1,978.70 | 65 |
| CRM | 8 | $268.33 | $273.24 | $2,185.92 | 65 |
| CSCO | 34 | $68.36 | $68.58 | $2,331.72 | 75 |
| CVX | 16 | $146.69 | $152.53 | $2,440.48 | 75 |
| DIS | 17 | $122.85 | $122.09 | $2,075.61 | 65 |
| GOOGL | 12 | $179.60 | $174.08 | $2,088.96 | 65 |
| GS | 3 | $717.52 | $699.23 | $2,097.69 | 70 |
| HD | 6 | $372.64 | $367.52 | $2,205.15 | 65 |
| INTC | 81 | $22.25 | $23.48 | $1,901.94 | 60 |
| JNJ | 14 | $155.85 | $154.95 | $2,169.27 | 65 |
| JPM | 9 | $291.61 | $282.03 | $2,538.27 | 75 |
| KO | 29 | $71.03 | $70.14 | $2,034.06 | 65 |
| LLY | 2 | $776.66 | $776.98 | $1,553.95 | 65 |
| MA | 4 | $563.08 | $562.54 | $2,250.15 | 65 |
| META | 3 | $717.12 | $720.62 | $2,161.88 | 75 |
| MRK | 29 | $82.49 | $80.67 | $2,339.43 | 75 |
| MSFT | 5 | $498.84 | $495.61 | $2,478.05 | 75 |
| NFLX | 1 | $1,279.00 | $1,275.98 | $1,275.98 | 65 |
| NKE | 30 | $75.91 | $73.95 | $2,218.49 | 70 |
| NVDA | 16 | $156.90 | $159.49 | $2,551.92 | 85 |
| ORCL | 9 | $233.41 | $236.56 | $2,129.04 | 75 |
| PEP | 15 | $136.57 | $134.61 | $2,019.15 | 65 |
| PFE | 87 | $25.25 | $25.34 | $2,204.58 | 70 |
| PG | 13 | $160.77 | $158.15 | $2,055.95 | 65 |
| PYPL | 31 | $76.64 | $74.61 | $2,312.91 | 75 |
| QCOM | 14 | $161.75 | $160.49 | $2,246.86 | 75 |
| T | 72 | $28.54 | $28.32 | $2,039.05 | 65 |
| TGT | 20 | $104.90 | $101.41 | $2,028.20 | 65 |
| TSLA | 6 | $288.62 | $301.37 | $1,808.22 | 65 |
| UNH | 7 | $314.75 | $305.26 | $2,136.79 | 65 |
| UNP | 10 | $236.66 | $236.63 | $2,366.30 | 75 |
| V | 6 | $355.95 | $355.04 | $2,130.24 | 65 |
| VZ | 47 | $43.72 | $43.02 | $2,022.17 | 65 |
| WFC | 29 | $82.34 | $81.89 | $2,374.81 | 75 |
| WMT | 24 | $97.42 | $97.67 | $2,344.08 | 75 |
| XOM | 21 | $110.00 | $114.20 | $2,398.20 | 75 |

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
| 2025-07-08 17:08:36 | SELL | INTC | 5 | $23.49 | $5.84 | 60 |
| 2025-07-08 17:08:36 | SELL | C | 5 | $86.33 | $-1.28 | 70 |
| 2025-07-08 17:08:36 | SELL | T | 1 | $28.33 | $-0.22 | 65 |
| 2025-07-08 17:08:36 | BUY | WMT | 3 | $97.67 | N/A | 75 |
| 2025-07-08 17:08:36 | BUY | BA | 1 | $217.69 | N/A | 70 |
| 2025-07-08 17:08:36 | BUY | CSCO | 2 | $68.58 | N/A | 75 |
| 2025-07-08 16:55:22 | SELL | INTC | 1 | $22.00 | $-0.32 | 60 |
| 2025-07-08 16:55:22 | SELL | WMT | 1 | $97.77 | $0.37 | 65 |
| 2025-07-08 16:55:22 | SELL | MRK | 3 | $81.90 | $-1.60 | 75 |
| 2025-07-08 16:55:22 | SELL | T | 5 | $28.30 | $-1.15 | 65 |
| 2025-07-08 16:55:22 | BUY | NVDA | 2 | $159.71 | N/A | 85 |
| 2025-07-08 16:55:22 | BUY | PFE | 7 | $25.24 | N/A | 70 |
| 2025-07-08 16:55:22 | BUY | C | 1 | $86.14 | N/A | 85 |
| 2025-07-08 16:43:31 | SELL | NVDA | 2 | $158.24 | $3.04 | 70 |
| 2025-07-08 16:43:31 | SELL | T | 4 | $28.33 | $-0.74 | 70 |
| 2025-07-08 16:43:31 | SELL | WFC | 1 | $81.65 | $-0.66 | 75 |
| 2025-07-08 16:43:31 | BUY | INTC | 1 | $23.38 | N/A | 65 |
| 2025-07-08 16:43:31 | BUY | BAC | 3 | $47.17 | N/A | 75 |
| 2025-07-08 16:28:46 | SELL | PFE | 12 | $25.68 | $4.43 | 65 |
| 2025-07-08 16:28:46 | SELL | CSCO | 2 | $68.78 | $0.81 | 70 |
| 2025-07-08 16:28:46 | BUY | NVDA | 2 | $159.84 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | INTC | 4 | $23.38 | N/A | 65 |
| 2025-07-08 16:28:46 | BUY | WMT | 1 | $97.81 | N/A | 70 |
| 2025-07-08 16:28:46 | BUY | MRK | 5 | $82.31 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | WFC | 1 | $81.61 | N/A | 80 |

<!--TRADE_LOG_END--> 
