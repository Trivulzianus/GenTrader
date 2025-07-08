# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 14:40:51**

| Metric | Value |
|---|---|
| **Total Value** | **$100,991.95** |
| Cash | $1,032.20 |
| Holdings Value | $99,959.76 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.18 | $2,101.78 | 65 |
| ADBE | 5 | $377.60 | $384.20 | $1,921.02 | 65 |
| AMD | 16 | $135.69 | $138.58 | $2,217.28 | 70 |
| AMZN | 10 | $221.61 | $222.06 | $2,220.65 | 65 |
| AVGO | 8 | $275.34 | $273.29 | $2,186.32 | 70 |
| AXP | 8 | $324.24 | $321.61 | $2,572.88 | 85 |
| BA | 10 | $212.15 | $215.65 | $2,156.50 | 65 |
| BAC | 47 | $48.73 | $47.30 | $2,222.87 | 70 |
| C | 27 | $86.65 | $86.14 | $2,325.78 | 75 |
| CAT | 6 | $397.86 | $393.65 | $2,361.90 | 70 |
| COST | 2 | $979.83 | $990.65 | $1,981.30 | 65 |
| CRM | 8 | $268.33 | $276.56 | $2,212.48 | 75 |
| CSCO | 32 | $68.37 | $68.69 | $2,198.15 | 70 |
| CVX | 16 | $146.65 | $150.68 | $2,410.88 | 75 |
| DIS | 18 | $122.81 | $122.28 | $2,201.04 | 70 |
| GOOGL | 12 | $179.60 | $175.66 | $2,107.86 | 70 |
| GS | 3 | $717.52 | $701.45 | $2,104.35 | 70 |
| HD | 6 | $372.64 | $368.59 | $2,211.54 | 70 |
| INTC | 87 | $22.27 | $23.32 | $2,028.41 | 65 |
| JNJ | 13 | $155.81 | $156.47 | $2,034.11 | 65 |
| JPM | 9 | $291.61 | $284.36 | $2,559.20 | 85 |
| KO | 29 | $71.03 | $70.12 | $2,033.48 | 65 |
| LLY | 2 | $776.66 | $789.12 | $1,578.24 | 70 |
| MA | 4 | $563.08 | $565.52 | $2,262.08 | 65 |
| META | 3 | $717.12 | $720.14 | $2,160.42 | 75 |
| MRK | 29 | $82.43 | $81.97 | $2,377.09 | 75 |
| MSFT | 5 | $498.84 | $497.05 | $2,485.25 | 75 |
| NFLX | 1 | $1,279.00 | $1,273.91 | $1,273.91 | 75 |
| NKE | 28 | $76.04 | $74.51 | $2,086.25 | 70 |
| NVDA | 16 | $156.62 | $159.12 | $2,545.92 | 85 |
| ORCL | 9 | $233.41 | $238.59 | $2,147.31 | 65 |
| PEP | 15 | $136.57 | $135.13 | $2,026.96 | 65 |
| PFE | 90 | $25.31 | $25.77 | $2,318.85 | 75 |
| PG | 13 | $160.77 | $158.31 | $2,058.03 | 65 |
| PYPL | 31 | $76.64 | $75.51 | $2,340.81 | 75 |
| QCOM | 14 | $161.75 | $160.34 | $2,244.69 | 75 |
| T | 72 | $28.55 | $28.20 | $2,030.76 | 65 |
| TGT | 20 | $104.90 | $101.75 | $2,035.10 | 65 |
| TSLA | 6 | $288.62 | $303.40 | $1,820.40 | 60 |
| UNH | 7 | $314.75 | $307.12 | $2,149.84 | 65 |
| UNP | 10 | $236.53 | $237.45 | $2,374.50 | 75 |
| V | 6 | $355.95 | $357.43 | $2,144.55 | 65 |
| VZ | 47 | $43.72 | $43.03 | $2,022.41 | 65 |
| WFC | 29 | $82.34 | $81.72 | $2,369.74 | 75 |
| WMT | 23 | $97.38 | $97.74 | $2,248.02 | 75 |
| XOM | 22 | $110.11 | $113.13 | $2,488.86 | 75 |

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
| 2025-07-08 14:40:40 | SELL | JNJ | 1 | $156.44 | $0.58 | 65 |
| 2025-07-08 14:40:40 | SELL | INTC | 2 | $23.32 | $2.06 | 65 |
| 2025-07-08 14:40:40 | SELL | WFC | 3 | $81.74 | $-1.65 | 75 |
| 2025-07-08 14:40:40 | SELL | T | 1 | $28.41 | $-0.13 | 65 |
| 2025-07-08 14:40:40 | SELL | CSCO | 1 | $68.69 | $0.31 | 70 |
| 2025-07-08 14:40:40 | BUY | NVDA | 1 | $159.12 | N/A | 85 |
| 2025-07-08 14:40:40 | BUY | PFE | 4 | $25.77 | N/A | 75 |
| 2025-07-08 14:40:40 | BUY | C | 1 | $86.14 | N/A | 75 |
| 2025-07-08 14:26:03 | SELL | BAC | 2 | $47.44 | $-2.47 | 70 |
| 2025-07-08 14:26:03 | SELL | NVDA | 1 | $158.69 | $2.10 | 75 |
| 2025-07-08 14:26:03 | SELL | PFE | 1 | $25.74 | $0.44 | 70 |
| 2025-07-08 14:26:03 | SELL | C | 4 | $86.01 | $-2.27 | 70 |
| 2025-07-08 14:26:03 | SELL | CVX | 1 | $150.30 | $3.44 | 75 |
| 2025-07-08 14:26:03 | BUY | JNJ | 1 | $156.58 | N/A | 70 |
| 2025-07-08 14:26:03 | BUY | JPM | 1 | $284.00 | N/A | 85 |
| 2025-07-08 14:26:03 | BUY | AMD | 1 | $136.73 | N/A | 70 |
| 2025-07-08 14:26:03 | BUY | XOM | 1 | $113.11 | N/A | 80 |
| 2025-07-08 14:26:03 | BUY | DIS | 1 | $122.42 | N/A | 70 |
| 2025-07-08 14:26:03 | BUY | WFC | 3 | $81.67 | N/A | 85 |
| 2025-07-08 14:08:44 | SELL | AMD | 1 | $136.47 | $0.79 | 65 |
| 2025-07-08 14:08:44 | SELL | NKE | 3 | $73.92 | $-5.75 | 65 |
| 2025-07-08 14:08:44 | SELL | T | 4 | $28.22 | $-1.23 | 65 |
| 2025-07-08 14:08:44 | BUY | BAC | 2 | $47.51 | N/A | 75 |
| 2025-07-08 14:08:44 | BUY | PYPL | 4 | $75.20 | N/A | 75 |
| 2025-07-08 14:08:44 | BUY | MRK | 1 | $81.14 | N/A | 75 |

<!--TRADE_LOG_END--> 
