# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 13:55:05**

| Metric | Value |
|---|---|
| **Total Value** | **$101,730.38** |
| Cash | $2,832.14 |
| Holdings Value | $98,898.24 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $213.18 | $2,131.80 | 70 |
| ADBE | 5 | $377.60 | $380.93 | $1,904.62 | 65 |
| AMD | 15 | $135.93 | $137.72 | $2,065.80 | 65 |
| AMZN | 10 | $221.48 | $222.41 | $2,224.10 | 75 |
| AVGO | 8 | $269.90 | $272.57 | $2,180.56 | 70 |
| AXP | 8 | $324.40 | $327.67 | $2,621.36 | 85 |
| BA | 10 | $212.15 | $215.45 | $2,154.50 | 65 |
| BAC | 47 | $48.61 | $49.27 | $2,315.92 | 75 |
| C | 30 | $86.80 | $88.09 | $2,642.85 | 85 |
| CAT | 6 | $396.45 | $402.21 | $2,413.26 | 70 |
| COST | 2 | $979.83 | $982.78 | $1,965.57 | 65 |
| CRM | 7 | $267.51 | $272.89 | $1,910.23 | 70 |
| CSCO | 33 | $68.37 | $68.69 | $2,266.77 | 75 |
| CVX | 16 | $146.55 | $147.98 | $2,367.68 | 75 |
| DIS | 18 | $122.90 | $123.69 | $2,226.33 | 75 |
| GOOGL | 13 | $177.82 | $178.07 | $2,314.90 | 70 |
| GS | 3 | $717.52 | $721.33 | $2,163.99 | 85 |
| HD | 6 | $372.64 | $369.95 | $2,219.70 | 70 |
| INTC | 83 | $22.33 | $22.28 | $1,849.25 | 60 |
| JNJ | 13 | $155.80 | $155.80 | $2,025.41 | 65 |
| JPM | 9 | $292.50 | $294.29 | $2,648.62 | 85 |
| KO | 28 | $71.03 | $70.77 | $1,981.56 | 65 |
| LLY | 2 | $776.66 | $779.85 | $1,559.70 | 70 |
| MA | 3 | $561.03 | $564.86 | $1,694.57 | 65 |
| META | 3 | $717.12 | $721.71 | $2,165.12 | 85 |
| MRK | 27 | $82.42 | $81.87 | $2,210.61 | 70 |
| MSFT | 5 | $491.36 | $495.13 | $2,475.65 | 85 |
| NFLX | 1 | $1,279.00 | $1,287.45 | $1,287.45 | 65 |
| NKE | 34 | $75.85 | $76.45 | $2,599.47 | 85 |
| NVDA | 14 | $155.93 | $158.34 | $2,216.76 | 70 |
| ORCL | 9 | $224.73 | $232.19 | $2,089.71 | 70 |
| PEP | 15 | $136.59 | $135.91 | $2,038.65 | 65 |
| PFE | 84 | $25.33 | $25.39 | $2,133.18 | 70 |
| PG | 12 | $160.76 | $161.26 | $1,935.18 | 65 |
| PYPL | 30 | $76.82 | $77.19 | $2,315.70 | 75 |
| QCOM | 14 | $161.41 | $163.03 | $2,282.42 | 70 |
| T | 77 | $28.52 | $28.36 | $2,183.34 | 70 |
| TGT | 20 | $105.04 | $105.29 | $2,105.80 | 70 |
| TSLA | 6 | $313.02 | $315.57 | $1,893.42 | 65 |
| UNH | 7 | $314.75 | $310.00 | $2,170.00 | 65 |
| UNP | 9 | $236.50 | $238.46 | $2,146.13 | 75 |
| V | 5 | $352.10 | $356.13 | $1,780.65 | 65 |
| VZ | 49 | $43.73 | $43.63 | $2,137.87 | 70 |
| WFC | 31 | $82.32 | $83.72 | $2,595.47 | 85 |
| WMT | 21 | $97.32 | $97.81 | $2,054.01 | 65 |
| XOM | 20 | $109.86 | $111.63 | $2,232.60 | 75 |

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
| 2025-07-03 13:44:30 | SELL | T | 3 | $28.29 | $-0.65 | 70 |
| 2025-07-03 13:44:30 | SELL | CVX | 1 | $147.80 | $1.18 | 75 |
| 2025-07-03 13:44:30 | BUY | DIS | 1 | $123.52 | N/A | 70 |
| 2025-07-03 13:44:30 | BUY | WMT | 1 | $97.80 | N/A | 70 |
| 2025-07-03 13:44:30 | BUY | TGT | 1 | $105.13 | N/A | 70 |
| 2025-07-03 13:28:20 | SELL | DIS | 1 | $122.98 | $0.15 | 65 |
| 2025-07-03 13:28:20 | SELL | PFE | 1 | $25.32 | $-0.01 | 70 |

<!--TRADE_LOG_END--> 
