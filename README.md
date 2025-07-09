# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 17:25:48**

| Metric | Value |
|---|---|
| **Total Value** | **$100,893.58** |
| Cash | $1,629.48 |
| Holdings Value | $99,264.10 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $208.93 | $2,089.30 | 65 |
| ADBE | 5 | $377.60 | $371.78 | $1,858.90 | 65 |
| AMD | 15 | $135.39 | $138.53 | $2,077.95 | 70 |
| AMZN | 10 | $221.83 | $222.64 | $2,226.40 | 75 |
| AVGO | 8 | $275.34 | $277.86 | $2,222.90 | 70 |
| AXP | 7 | $325.28 | $318.90 | $2,232.30 | 70 |
| BA | 10 | $212.53 | $229.94 | $2,299.35 | 70 |
| BAC | 47 | $48.69 | $47.02 | $2,210.17 | 70 |
| C | 31 | $86.66 | $86.03 | $2,666.78 | 85 |
| CAT | 6 | $397.86 | $402.27 | $2,413.65 | 85 |
| COST | 2 | $979.83 | $975.61 | $1,951.22 | 65 |
| CRM | 8 | $268.33 | $270.34 | $2,162.72 | 65 |
| CSCO | 33 | $68.35 | $68.90 | $2,273.70 | 75 |
| CVX | 17 | $147.03 | $153.20 | $2,604.40 | 85 |
| DIS | 18 | $122.81 | $120.82 | $2,174.76 | 70 |
| GOOGL | 13 | $179.50 | $177.35 | $2,305.55 | 70 |
| GS | 3 | $717.52 | $698.37 | $2,095.12 | 70 |
| HD | 6 | $372.64 | $366.07 | $2,196.45 | 70 |
| INTC | 80 | $22.23 | $23.34 | $1,866.80 | 60 |
| JNJ | 13 | $155.89 | $155.59 | $2,022.61 | 65 |
| JPM | 9 | $291.61 | $283.71 | $2,553.43 | 75 |
| KO | 29 | $71.03 | $69.28 | $2,008.98 | 65 |
| LLY | 2 | $776.66 | $786.54 | $1,573.08 | 65 |
| MA | 4 | $563.08 | $561.00 | $2,244.00 | 65 |
| META | 3 | $717.12 | $733.98 | $2,201.94 | 85 |
| MRK | 29 | $82.50 | $83.94 | $2,434.26 | 75 |
| MSFT | 5 | $498.84 | $501.61 | $2,508.03 | 85 |
| NFLX | 1 | $1,279.00 | $1,277.13 | $1,277.13 | 65 |
| NKE | 28 | $76.06 | $73.89 | $2,069.06 | 65 |
| NVDA | 16 | $157.22 | $162.74 | $2,603.84 | 85 |
| ORCL | 9 | $233.31 | $235.61 | $2,120.49 | 70 |
| PEP | 15 | $136.57 | $133.73 | $2,005.95 | 65 |
| PFE | 85 | $25.22 | $25.48 | $2,165.38 | 70 |
| PG | 13 | $160.75 | $156.52 | $2,034.76 | 65 |
| PYPL | 31 | $76.63 | $75.02 | $2,325.62 | 75 |
| QCOM | 14 | $161.87 | $159.47 | $2,232.51 | 70 |
| T | 72 | $28.56 | $28.10 | $2,023.20 | 65 |
| TGT | 20 | $104.89 | $102.47 | $2,049.40 | 65 |
| TSLA | 6 | $288.62 | $294.65 | $1,767.90 | 65 |
| UNH | 7 | $314.75 | $302.26 | $2,115.82 | 65 |
| UNP | 9 | $236.60 | $237.49 | $2,137.41 | 65 |
| V | 6 | $355.95 | $354.99 | $2,129.91 | 70 |
| VZ | 48 | $43.15 | $42.71 | $2,050.08 | 65 |
| WFC | 29 | $82.28 | $81.95 | $2,376.55 | 75 |
| WMT | 21 | $97.35 | $96.86 | $2,034.06 | 65 |
| XOM | 20 | $109.83 | $113.52 | $2,270.30 | 75 |

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
| 2025-07-09 17:25:41 | SELL | BAC | 3 | $47.03 | $-4.69 | 70 |
| 2025-07-09 17:25:41 | SELL | NKE | 1 | $73.92 | $-2.06 | 65 |
| 2025-07-09 17:25:41 | BUY | PFE | 4 | $25.48 | N/A | 70 |
| 2025-07-09 17:25:41 | BUY | CSCO | 1 | $68.89 | N/A | 75 |
| 2025-07-09 17:25:41 | BUY | CVX | 1 | $153.27 | N/A | 85 |
| 2025-07-09 17:10:02 | SELL | INTC | 7 | $23.59 | $8.73 | 60 |
| 2025-07-09 17:10:02 | SELL | PFE | 6 | $25.44 | $1.30 | 65 |
| 2025-07-09 17:10:02 | SELL | CVX | 1 | $153.25 | $6.22 | 75 |
| 2025-07-09 17:10:02 | BUY | BAC | 4 | $46.78 | N/A | 75 |
| 2025-07-09 17:10:02 | BUY | NKE | 1 | $73.95 | N/A | 70 |
| 2025-07-09 17:10:02 | BUY | PYPL | 1 | $74.82 | N/A | 75 |
| 2025-07-09 17:10:02 | BUY | MRK | 1 | $83.86 | N/A | 80 |
| 2025-07-09 16:56:47 | SELL | PYPL | 1 | $74.84 | $-1.79 | 70 |
| 2025-07-09 16:56:47 | SELL | PFE | 5 | $25.44 | $1.02 | 70 |
| 2025-07-09 16:56:47 | SELL | ORCL | 1 | $234.93 | $1.46 | 65 |
| 2025-07-09 16:56:47 | BUY | BAC | 2 | $46.74 | N/A | 70 |
| 2025-07-09 16:56:47 | BUY | C | 3 | $85.75 | N/A | 85 |
| 2025-07-09 16:43:39 | SELL | NKE | 1 | $73.73 | $-2.24 | 65 |
| 2025-07-09 16:43:39 | SELL | MRK | 1 | $83.84 | $1.35 | 75 |
| 2025-07-09 16:43:39 | SELL | C | 3 | $85.68 | $-2.94 | 75 |
| 2025-07-09 16:43:39 | SELL | WFC | 1 | $81.47 | $-0.78 | 75 |
| 2025-07-09 16:43:39 | BUY | NVDA | 2 | $163.10 | N/A | 85 |
| 2025-07-09 16:43:39 | BUY | DIS | 1 | $121.03 | N/A | 70 |
| 2025-07-09 16:43:39 | BUY | PFE | 6 | $25.42 | N/A | 75 |
| 2025-07-09 16:43:39 | BUY | CVX | 1 | $152.71 | N/A | 85 |

<!--TRADE_LOG_END--> 
