# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 13:46:39**

| Metric | Value |
|---|---|
| **Total Value** | **$100,978.82** |
| Cash | $1,671.06 |
| Holdings Value | $99,307.76 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.08 | $2,100.80 | 65 |
| ADBE | 5 | $377.60 | $383.54 | $1,917.69 | 65 |
| AMD | 15 | $135.55 | $139.62 | $2,094.30 | 65 |
| AMZN | 10 | $221.61 | $222.90 | $2,229.00 | 75 |
| AVGO | 8 | $275.34 | $278.77 | $2,230.16 | 70 |
| AXP | 7 | $325.28 | $316.98 | $2,218.86 | 75 |
| BA | 10 | $212.43 | $218.52 | $2,185.20 | 65 |
| BAC | 44 | $48.82 | $47.15 | $2,074.60 | 65 |
| C | 27 | $86.71 | $85.57 | $2,310.39 | 75 |
| CAT | 6 | $397.86 | $394.29 | $2,365.74 | 70 |
| COST | 2 | $979.83 | $983.29 | $1,966.58 | 65 |
| CRM | 8 | $268.33 | $273.65 | $2,189.20 | 65 |
| CSCO | 33 | $68.34 | $68.82 | $2,271.06 | 70 |
| CVX | 17 | $147.04 | $153.24 | $2,605.08 | 85 |
| DIS | 19 | $122.74 | $121.82 | $2,314.58 | 75 |
| GOOGL | 12 | $179.60 | $176.04 | $2,112.48 | 65 |
| GS | 3 | $717.52 | $697.28 | $2,091.84 | 70 |
| HD | 6 | $372.64 | $367.50 | $2,205.00 | 65 |
| INTC | 81 | $22.25 | $23.46 | $1,900.25 | 60 |
| JNJ | 13 | $155.89 | $155.79 | $2,025.27 | 65 |
| JPM | 9 | $291.61 | $282.78 | $2,545.02 | 75 |
| KO | 29 | $71.03 | $70.24 | $2,036.96 | 65 |
| LLY | 2 | $776.66 | $777.66 | $1,555.32 | 65 |
| MA | 4 | $563.08 | $562.44 | $2,249.76 | 65 |
| META | 3 | $717.12 | $728.97 | $2,186.91 | 85 |
| MRK | 29 | $82.50 | $81.37 | $2,359.73 | 75 |
| MSFT | 5 | $498.84 | $504.13 | $2,520.64 | 85 |
| NFLX | 1 | $1,279.00 | $1,269.09 | $1,269.09 | 65 |
| NKE | 29 | $75.97 | $73.92 | $2,143.68 | 70 |
| NVDA | 16 | $157.22 | $164.18 | $2,626.88 | 85 |
| ORCL | 9 | $233.41 | $234.50 | $2,110.50 | 65 |
| PEP | 15 | $136.57 | $135.36 | $2,030.40 | 65 |
| PFE | 81 | $25.20 | $25.62 | $2,075.22 | 65 |
| PG | 13 | $160.77 | $157.89 | $2,052.57 | 65 |
| PYPL | 28 | $76.76 | $75.59 | $2,116.52 | 65 |
| QCOM | 16 | $161.57 | $161.07 | $2,577.12 | 85 |
| T | 73 | $28.55 | $28.29 | $2,065.17 | 65 |
| TGT | 21 | $104.81 | $102.01 | $2,142.21 | 70 |
| TSLA | 6 | $288.62 | $297.97 | $1,787.82 | 65 |
| UNH | 7 | $314.75 | $307.70 | $2,153.90 | 65 |
| UNP | 9 | $236.60 | $236.54 | $2,128.86 | 65 |
| V | 6 | $355.95 | $354.55 | $2,127.30 | 65 |
| VZ | 47 | $43.16 | $43.06 | $2,023.82 | 65 |
| WFC | 29 | $82.27 | $81.59 | $2,366.11 | 75 |
| WMT | 22 | $97.35 | $97.09 | $2,135.98 | 65 |
| XOM | 22 | $110.20 | $114.19 | $2,512.18 | 80 |

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
| 2025-07-09 13:46:32 | SELL | BAC | 6 | $47.26 | $-8.24 | 65 |
| 2025-07-09 13:46:32 | SELL | INTC | 5 | $23.45 | $5.64 | 60 |
| 2025-07-09 13:46:32 | SELL | PYPL | 3 | $75.58 | $-3.20 | 65 |
| 2025-07-09 13:46:32 | SELL | WMT | 2 | $96.98 | $-0.67 | 65 |
| 2025-07-09 13:46:32 | SELL | PFE | 22 | $25.68 | $8.25 | 65 |
| 2025-07-09 13:46:32 | SELL | WFC | 3 | $82.17 | $-0.28 | 75 |
| 2025-07-09 13:46:32 | SELL | UNP | 1 | $237.24 | $0.58 | 65 |
| 2025-07-09 13:46:32 | SELL | CSCO | 1 | $68.85 | $0.49 | 70 |
| 2025-07-09 13:46:32 | BUY | NVDA | 1 | $160.00 | N/A | 85 |
| 2025-07-09 13:46:32 | BUY | XOM | 1 | $113.72 | N/A | 80 |
| 2025-07-09 13:46:32 | BUY | QCOM | 1 | $160.97 | N/A | 85 |
| 2025-07-09 13:46:32 | BUY | T | 1 | $28.16 | N/A | 65 |
| 2025-07-09 13:46:32 | BUY | TGT | 1 | $102.87 | N/A | 70 |
| 2025-07-09 13:28:47 | SELL | XOM | 2 | $114.19 | $7.60 | 75 |
| 2025-07-09 13:28:47 | SELL | MRK | 3 | $81.37 | $-3.06 | 75 |
| 2025-07-09 13:28:47 | SELL | T | 5 | $28.29 | $-1.25 | 65 |
| 2025-07-09 13:28:47 | BUY | DIS | 2 | $121.82 | N/A | 75 |
| 2025-07-09 13:28:47 | BUY | PFE | 11 | $25.62 | N/A | 85 |
| 2025-07-09 13:28:47 | BUY | WFC | 3 | $81.59 | N/A | 85 |
| 2025-07-09 13:28:47 | BUY | CVX | 1 | $153.24 | N/A | 85 |
| 2025-07-09 13:03:44 | SELL | GOOGL | 1 | $174.36 | $-4.83 | 65 |
| 2025-07-09 13:03:44 | SELL | NVDA | 1 | $160.00 | $2.78 | 75 |
| 2025-07-09 13:03:44 | SELL | WFC | 1 | $81.59 | $-0.72 | 75 |
| 2025-07-09 13:03:44 | BUY | XOM | 2 | $114.19 | N/A | 85 |
| 2025-07-09 13:03:44 | BUY | WMT | 3 | $97.09 | N/A | 75 |

<!--TRADE_LOG_END--> 
