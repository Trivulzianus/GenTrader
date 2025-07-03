# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 14:08:41**

| Metric | Value |
|---|---|
| **Total Value** | **$101,810.79** |
| Cash | $3,055.54 |
| Holdings Value | $98,755.25 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $213.38 | $2,133.80 | 70 |
| ADBE | 5 | $377.60 | $381.10 | $1,905.48 | 60 |
| AMD | 15 | $135.93 | $138.28 | $2,074.13 | 70 |
| AMZN | 10 | $221.48 | $223.01 | $2,230.10 | 75 |
| AVGO | 8 | $269.90 | $273.90 | $2,191.23 | 70 |
| AXP | 8 | $324.40 | $327.87 | $2,622.94 | 85 |
| BA | 10 | $212.15 | $215.92 | $2,159.20 | 70 |
| BAC | 53 | $48.68 | $49.16 | $2,605.48 | 85 |
| C | 30 | $86.80 | $88.06 | $2,641.85 | 85 |
| CAT | 6 | $396.45 | $401.53 | $2,409.18 | 70 |
| COST | 2 | $979.83 | $985.66 | $1,971.32 | 65 |
| CRM | 7 | $267.51 | $272.57 | $1,907.99 | 65 |
| CSCO | 33 | $68.37 | $68.86 | $2,272.22 | 75 |
| CVX | 16 | $146.55 | $147.83 | $2,365.28 | 75 |
| DIS | 18 | $122.90 | $123.75 | $2,227.59 | 70 |
| GOOGL | 13 | $177.82 | $178.12 | $2,315.56 | 75 |
| GS | 3 | $717.52 | $721.74 | $2,165.22 | 75 |
| HD | 6 | $372.64 | $369.95 | $2,219.69 | 65 |
| INTC | 83 | $22.33 | $22.48 | $1,866.25 | 60 |
| JNJ | 13 | $155.80 | $155.43 | $2,020.64 | 65 |
| JPM | 9 | $292.50 | $294.39 | $2,649.51 | 85 |
| KO | 28 | $71.03 | $70.66 | $1,978.34 | 65 |
| LLY | 2 | $776.66 | $779.76 | $1,559.51 | 70 |
| MA | 3 | $561.03 | $566.35 | $1,699.05 | 65 |
| META | 3 | $717.12 | $719.71 | $2,159.14 | 85 |
| MRK | 25 | $82.46 | $81.91 | $2,047.75 | 65 |
| MSFT | 5 | $491.36 | $497.92 | $2,489.58 | 85 |
| NFLX | 1 | $1,279.00 | $1,293.50 | $1,293.50 | 65 |
| NKE | 29 | $75.78 | $76.13 | $2,207.77 | 70 |
| NVDA | 14 | $155.93 | $159.36 | $2,230.97 | 75 |
| ORCL | 9 | $224.73 | $233.16 | $2,098.44 | 70 |
| PEP | 15 | $136.59 | $136.23 | $2,043.45 | 65 |
| PFE | 80 | $25.33 | $25.34 | $2,027.14 | 65 |
| PG | 12 | $160.76 | $160.55 | $1,926.60 | 65 |
| PYPL | 30 | $76.82 | $77.24 | $2,317.20 | 75 |
| QCOM | 14 | $161.41 | $163.47 | $2,288.58 | 75 |
| T | 72 | $28.53 | $28.35 | $2,041.54 | 65 |
| TGT | 20 | $105.04 | $105.22 | $2,104.40 | 65 |
| TSLA | 6 | $313.02 | $315.79 | $1,894.74 | 65 |
| UNH | 7 | $314.75 | $310.66 | $2,174.63 | 65 |
| UNP | 9 | $236.50 | $238.17 | $2,143.53 | 75 |
| V | 6 | $352.90 | $356.90 | $2,141.38 | 70 |
| VZ | 47 | $43.73 | $43.66 | $2,052.26 | 65 |
| WFC | 31 | $82.32 | $83.84 | $2,599.17 | 85 |
| WMT | 21 | $97.32 | $97.63 | $2,050.13 | 65 |
| XOM | 20 | $109.86 | $111.59 | $2,231.80 | 75 |

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
| 2025-07-03 14:08:35 | SELL | NKE | 5 | $76.23 | $1.92 | 70 |
| 2025-07-03 14:08:35 | SELL | MRK | 2 | $81.92 | $-0.99 | 65 |
| 2025-07-03 14:08:35 | SELL | PFE | 4 | $25.33 | $0.02 | 65 |
| 2025-07-03 14:08:35 | SELL | VZ | 2 | $43.67 | $-0.12 | 65 |
| 2025-07-03 14:08:35 | SELL | T | 5 | $28.35 | $-0.83 | 65 |
| 2025-07-03 14:08:35 | BUY | V | 1 | $356.90 | N/A | 70 |
| 2025-07-03 14:08:35 | BUY | BAC | 6 | $49.19 | N/A | 85 |
| 2025-07-03 13:54:59 | SELL | BAC | 6 | $49.28 | $3.57 | 75 |
| 2025-07-03 13:54:59 | SELL | INTC | 1 | $22.33 | $-0.01 | 60 |
| 2025-07-03 13:54:59 | SELL | WMT | 1 | $97.82 | $0.47 | 65 |
| 2025-07-03 13:54:59 | SELL | MRK | 1 | $81.90 | $-0.50 | 70 |
| 2025-07-03 13:54:59 | SELL | QCOM | 1 | $163.02 | $1.50 | 70 |
| 2025-07-03 13:54:59 | BUY | NKE | 3 | $76.49 | N/A | 85 |
| 2025-07-03 13:54:59 | BUY | DIS | 1 | $123.64 | N/A | 75 |
| 2025-07-03 13:54:59 | BUY | PFE | 4 | $25.41 | N/A | 70 |
| 2025-07-03 13:54:59 | BUY | WFC | 3 | $83.72 | N/A | 85 |
| 2025-07-03 13:54:59 | BUY | CSCO | 1 | $68.79 | N/A | 75 |
| 2025-07-03 13:54:59 | BUY | VZ | 3 | $43.63 | N/A | 70 |
| 2025-07-03 13:44:30 | SELL | XOM | 1 | $111.39 | $1.46 | 70 |
| 2025-07-03 13:44:30 | SELL | INTC | 6 | $22.29 | $-0.22 | 60 |
| 2025-07-03 13:44:30 | SELL | PFE | 3 | $25.31 | $-0.06 | 65 |
| 2025-07-03 13:44:30 | SELL | NKE | 2 | $76.68 | $1.68 | 75 |
| 2025-07-03 13:44:30 | SELL | WFC | 3 | $83.26 | $2.94 | 75 |
| 2025-07-03 13:44:30 | SELL | CSCO | 1 | $68.65 | $0.29 | 70 |
| 2025-07-03 13:44:30 | SELL | VZ | 5 | $43.72 | $-0.05 | 65 |

<!--TRADE_LOG_END--> 
