# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 13:46:12**

| Metric | Value |
|---|---|
| **Total Value** | **$101,241.31** |
| Cash | $1,805.86 |
| Holdings Value | $99,435.45 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $213.12 | $2,131.15 | 75 |
| ADBE | 5 | $377.60 | $378.66 | $1,893.30 | 65 |
| AMD | 16 | $135.92 | $136.23 | $2,179.68 | 70 |
| AMZN | 11 | $221.66 | $223.50 | $2,458.45 | 85 |
| AVGO | 8 | $269.90 | $275.95 | $2,207.64 | 70 |
| AXP | 8 | $324.34 | $327.61 | $2,620.88 | 85 |
| BA | 10 | $212.15 | $215.60 | $2,156.00 | 70 |
| BAC | 53 | $48.70 | $49.13 | $2,604.15 | 85 |
| C | 25 | $86.43 | $88.67 | $2,216.67 | 70 |
| CAT | 6 | $397.86 | $396.99 | $2,381.91 | 75 |
| COST | 2 | $979.83 | $982.26 | $1,964.52 | 65 |
| CRM | 8 | $268.33 | $273.00 | $2,184.00 | 65 |
| CSCO | 33 | $68.36 | $69.09 | $2,280.13 | 75 |
| CVX | 15 | $146.54 | $147.21 | $2,208.15 | 70 |
| DIS | 17 | $122.82 | $123.84 | $2,105.28 | 70 |
| GOOGL | 13 | $179.40 | $178.12 | $2,315.56 | 75 |
| GS | 3 | $717.52 | $721.92 | $2,165.76 | 75 |
| HD | 6 | $372.64 | $371.04 | $2,226.25 | 65 |
| INTC | 90 | $22.27 | $22.27 | $2,004.29 | 65 |
| JNJ | 13 | $155.80 | $155.88 | $2,026.44 | 65 |
| JPM | 9 | $292.50 | $295.16 | $2,656.44 | 85 |
| KO | 28 | $71.03 | $71.01 | $1,988.28 | 65 |
| LLY | 2 | $776.66 | $766.28 | $1,532.56 | 65 |
| MA | 4 | $563.08 | $568.47 | $2,273.86 | 65 |
| META | 3 | $717.12 | $718.80 | $2,156.40 | 85 |
| MRK | 24 | $82.64 | $80.99 | $1,943.76 | 65 |
| MSFT | 5 | $498.84 | $497.74 | $2,488.68 | 70 |
| NFLX | 1 | $1,279.00 | $1,286.78 | $1,286.78 | 65 |
| NKE | 28 | $75.80 | $76.75 | $2,149.03 | 70 |
| NVDA | 16 | $156.39 | $158.99 | $2,543.81 | 85 |
| ORCL | 10 | $226.66 | $231.52 | $2,315.20 | 70 |
| PEP | 15 | $136.59 | $133.91 | $2,008.65 | 65 |
| PFE | 80 | $25.31 | $25.45 | $2,035.60 | 65 |
| PG | 13 | $160.77 | $160.67 | $2,088.75 | 70 |
| PYPL | 29 | $76.82 | $76.48 | $2,217.92 | 70 |
| QCOM | 14 | $161.69 | $160.22 | $2,243.08 | 70 |
| T | 70 | $28.54 | $28.39 | $1,986.95 | 65 |
| TGT | 19 | $105.09 | $102.82 | $1,953.60 | 65 |
| TSLA | 5 | $315.35 | $291.71 | $1,458.57 | 60 |
| UNH | 7 | $314.75 | $307.64 | $2,153.51 | 65 |
| UNP | 11 | $236.50 | $236.64 | $2,603.01 | 85 |
| V | 6 | $352.90 | $358.04 | $2,148.24 | 70 |
| VZ | 46 | $43.73 | $43.22 | $1,987.89 | 65 |
| WFC | 30 | $82.28 | $83.47 | $2,503.95 | 80 |
| WMT | 22 | $97.32 | $97.86 | $2,152.92 | 70 |
| XOM | 20 | $109.90 | $111.39 | $2,227.80 | 70 |

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
| 2025-07-07 13:46:03 | SELL | XOM | 1 | $111.39 | $1.42 | 70 |
| 2025-07-07 13:46:03 | SELL | PYPL | 1 | $76.46 | $-0.34 | 70 |
| 2025-07-07 13:46:03 | SELL | PFE | 4 | $25.45 | $0.55 | 65 |
| 2025-07-07 13:46:03 | SELL | C | 4 | $88.65 | $7.67 | 70 |
| 2025-07-07 13:46:03 | SELL | WFC | 1 | $83.47 | $1.15 | 80 |
| 2025-07-07 13:46:03 | SELL | ORCL | 1 | $231.60 | $4.49 | 70 |
| 2025-07-07 13:46:03 | SELL | QCOM | 1 | $159.20 | $-2.32 | 70 |
| 2025-07-07 13:46:03 | SELL | CVX | 2 | $147.30 | $1.34 | 70 |
| 2025-07-07 13:46:03 | BUY | TSLA | 5 | $315.35 | N/A | 60 |
| 2025-07-07 13:46:03 | BUY | GOOGL | 1 | $177.86 | N/A | 75 |
| 2025-07-07 13:46:03 | BUY | AMD | 1 | $135.72 | N/A | 70 |
| 2025-07-07 13:46:03 | BUY | INTC | 8 | $22.21 | N/A | 65 |
| 2025-07-07 13:46:03 | BUY | NKE | 2 | $76.80 | N/A | 70 |
| 2025-07-07 13:46:03 | BUY | WMT | 1 | $98.00 | N/A | 70 |
| 2025-07-07 13:46:03 | BUY | AXP | 1 | $327.69 | N/A | 85 |
| 2025-07-07 13:46:03 | BUY | UNP | 1 | $236.73 | N/A | 85 |
| 2025-07-07 13:46:03 | BUY | CSCO | 2 | $69.37 | N/A | 75 |
| 2025-07-07 13:45:37 | SELL | TSLA | 6 | $290.44 | $-135.48 | 65 |
| 2025-07-07 13:28:48 | SELL | INTC | 6 | $22.49 | $1.17 | 60 |
| 2025-07-07 13:28:48 | SELL | XOM | 2 | $112.20 | $4.08 | 75 |
| 2025-07-07 13:28:48 | SELL | NKE | 1 | $76.39 | $0.64 | 65 |
| 2025-07-07 13:28:48 | SELL | T | 5 | $28.36 | $-0.82 | 65 |
| 2025-07-07 13:28:48 | BUY | PFE | 6 | $25.38 | N/A | 70 |
| 2025-07-07 13:28:48 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-07 13:03:15 | SELL | PFE | 6 | $25.38 | $0.41 | 65 |

<!--TRADE_LOG_END--> 
