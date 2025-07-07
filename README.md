# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 14:40:36**

| Metric | Value |
|---|---|
| **Total Value** | **$101,014.92** |
| Cash | $854.48 |
| Holdings Value | $100,160.43 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $212.06 | $2,120.65 | 70 |
| ADBE | 5 | $377.60 | $378.00 | $1,890.00 | 65 |
| AMD | 15 | $135.79 | $134.66 | $2,019.83 | 65 |
| AMZN | 11 | $221.66 | $223.66 | $2,460.26 | 75 |
| AVGO | 8 | $269.90 | $275.95 | $2,207.60 | 70 |
| AXP | 8 | $324.34 | $326.23 | $2,609.84 | 75 |
| BA | 10 | $212.15 | $215.87 | $2,158.65 | 65 |
| BAC | 53 | $48.70 | $49.05 | $2,599.55 | 85 |
| C | 29 | $86.69 | $88.23 | $2,558.67 | 85 |
| CAT | 6 | $397.86 | $394.16 | $2,364.96 | 85 |
| COST | 2 | $979.83 | $981.63 | $1,963.27 | 65 |
| CRM | 8 | $268.33 | $272.82 | $2,182.56 | 65 |
| CSCO | 33 | $68.36 | $69.23 | $2,284.59 | 75 |
| CVX | 16 | $146.63 | $147.46 | $2,359.28 | 75 |
| DIS | 18 | $122.89 | $123.75 | $2,227.41 | 70 |
| GOOGL | 13 | $179.40 | $177.44 | $2,306.72 | 70 |
| GS | 3 | $717.52 | $720.60 | $2,161.80 | 70 |
| HD | 6 | $372.64 | $370.10 | $2,220.60 | 70 |
| INTC | 91 | $22.26 | $22.10 | $2,011.10 | 65 |
| JNJ | 13 | $155.80 | $155.91 | $2,026.83 | 65 |
| JPM | 9 | $292.50 | $293.91 | $2,645.19 | 85 |
| KO | 28 | $71.03 | $71.02 | $1,988.56 | 65 |
| LLY | 2 | $776.66 | $765.12 | $1,530.24 | 60 |
| MA | 4 | $563.08 | $565.11 | $2,260.44 | 65 |
| META | 3 | $717.12 | $724.34 | $2,173.01 | 75 |
| MRK | 28 | $82.37 | $80.82 | $2,262.99 | 75 |
| MSFT | 5 | $498.84 | $497.82 | $2,489.12 | 85 |
| NFLX | 1 | $1,279.00 | $1,282.36 | $1,282.36 | 65 |
| NKE | 29 | $75.88 | $76.17 | $2,208.93 | 70 |
| NVDA | 14 | $156.12 | $158.33 | $2,216.62 | 70 |
| ORCL | 10 | $226.66 | $232.97 | $2,329.70 | 75 |
| PEP | 15 | $136.59 | $134.36 | $2,015.40 | 65 |
| PFE | 85 | $25.30 | $25.30 | $2,150.08 | 70 |
| PG | 13 | $160.77 | $160.06 | $2,080.78 | 65 |
| PYPL | 30 | $76.81 | $76.59 | $2,297.70 | 75 |
| QCOM | 14 | $161.69 | $158.50 | $2,218.93 | 75 |
| T | 76 | $28.53 | $28.38 | $2,156.50 | 70 |
| TGT | 19 | $105.09 | $101.95 | $1,937.05 | 65 |
| TSLA | 6 | $288.90 | $293.65 | $1,761.90 | 65 |
| UNH | 7 | $314.75 | $303.50 | $2,124.50 | 65 |
| UNP | 10 | $236.48 | $236.72 | $2,367.20 | 75 |
| V | 6 | $352.90 | $355.57 | $2,133.45 | 65 |
| VZ | 46 | $43.73 | $43.12 | $1,983.52 | 65 |
| WFC | 28 | $82.26 | $82.95 | $2,322.74 | 75 |
| WMT | 23 | $97.34 | $98.08 | $2,255.95 | 75 |
| XOM | 20 | $109.90 | $111.67 | $2,233.40 | 70 |

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
| 2025-07-07 14:40:29 | SELL | NVDA | 2 | $158.33 | $3.87 | 70 |
| 2025-07-07 14:40:29 | SELL | DIS | 2 | $123.74 | $1.53 | 70 |
| 2025-07-07 14:40:29 | SELL | NKE | 1 | $76.17 | $0.28 | 70 |
| 2025-07-07 14:40:29 | SELL | UNP | 1 | $236.72 | $0.22 | 75 |
| 2025-07-07 14:40:29 | SELL | CVX | 1 | $147.39 | $0.72 | 75 |
| 2025-07-07 14:40:29 | BUY | INTC | 9 | $22.09 | N/A | 65 |
| 2025-07-07 14:40:29 | BUY | MRK | 1 | $80.83 | N/A | 75 |
| 2025-07-07 14:40:29 | BUY | PFE | 2 | $25.30 | N/A | 70 |
| 2025-07-07 14:40:29 | BUY | C | 5 | $88.32 | N/A | 85 |
| 2025-07-07 14:40:29 | BUY | T | 2 | $28.38 | N/A | 70 |
| 2025-07-07 14:25:56 | SELL | INTC | 8 | $22.19 | $-0.68 | 60 |
| 2025-07-07 14:25:56 | SELL | NKE | 2 | $76.39 | $0.95 | 75 |
| 2025-07-07 14:25:56 | SELL | MRK | 2 | $81.06 | $-2.56 | 70 |
| 2025-07-07 14:25:56 | SELL | C | 1 | $88.24 | $1.80 | 70 |
| 2025-07-07 14:25:56 | SELL | WFC | 2 | $82.93 | $1.26 | 75 |
| 2025-07-07 14:25:56 | BUY | WMT | 1 | $98.04 | N/A | 75 |
| 2025-07-07 14:25:56 | BUY | PFE | 4 | $25.41 | N/A | 70 |
| 2025-07-07 14:25:56 | BUY | DIS | 3 | $123.82 | N/A | 85 |
| 2025-07-07 14:25:56 | BUY | T | 3 | $28.31 | N/A | 70 |
| 2025-07-07 14:25:56 | BUY | CVX | 2 | $147.64 | N/A | 85 |
| 2025-07-07 14:09:13 | SELL | MRK | 3 | $81.42 | $-2.49 | 75 |
| 2025-07-07 14:09:13 | SELL | PFE | 11 | $25.48 | $1.80 | 65 |
| 2025-07-07 14:09:13 | SELL | WFC | 1 | $83.07 | $0.74 | 80 |
| 2025-07-07 14:09:13 | SELL | T | 4 | $28.36 | $-0.68 | 65 |
| 2025-07-07 14:09:13 | BUY | WMT | 1 | $97.79 | N/A | 70 |

<!--TRADE_LOG_END--> 
