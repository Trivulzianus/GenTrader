# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 15:51:40**

| Metric | Value |
|---|---|
| **Total Value** | **$101,954.38** |
| Cash | $1,952.53 |
| Holdings Value | $100,001.85 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $214.47 | $2,144.65 | 70 |
| ADBE | 5 | $377.60 | $382.42 | $1,912.10 | 65 |
| AMD | 15 | $135.93 | $137.90 | $2,068.50 | 70 |
| AMZN | 10 | $221.48 | $223.46 | $2,234.55 | 75 |
| AVGO | 8 | $269.90 | $274.94 | $2,199.48 | 70 |
| AXP | 8 | $324.40 | $328.02 | $2,624.20 | 85 |
| BA | 10 | $212.15 | $216.03 | $2,160.25 | 70 |
| BAC | 47 | $48.66 | $48.98 | $2,302.30 | 75 |
| C | 30 | $86.80 | $88.51 | $2,655.22 | 85 |
| CAT | 6 | $396.45 | $399.11 | $2,394.66 | 70 |
| COST | 2 | $979.83 | $984.76 | $1,969.52 | 65 |
| CRM | 8 | $268.33 | $274.12 | $2,192.96 | 75 |
| CSCO | 33 | $68.37 | $69.33 | $2,287.72 | 75 |
| CVX | 16 | $146.55 | $148.48 | $2,375.68 | 75 |
| DIS | 18 | $122.90 | $123.74 | $2,227.25 | 75 |
| GOOGL | 12 | $177.75 | $178.69 | $2,144.22 | 70 |
| GS | 3 | $717.52 | $721.75 | $2,165.24 | 85 |
| HD | 6 | $372.64 | $371.85 | $2,231.10 | 65 |
| INTC | 88 | $22.34 | $22.48 | $1,978.68 | 65 |
| JNJ | 13 | $155.80 | $156.17 | $2,030.21 | 65 |
| JPM | 9 | $292.50 | $295.44 | $2,658.96 | 85 |
| KO | 29 | $71.04 | $71.25 | $2,066.39 | 70 |
| LLY | 2 | $776.66 | $776.60 | $1,553.20 | 65 |
| MA | 3 | $561.03 | $569.16 | $1,707.49 | 65 |
| META | 3 | $717.12 | $719.05 | $2,157.15 | 85 |
| MRK | 25 | $82.46 | $81.40 | $2,035.00 | 65 |
| MSFT | 5 | $491.36 | $499.44 | $2,497.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,300.05 | $1,300.05 | 75 |
| NKE | 34 | $75.84 | $76.48 | $2,600.20 | 85 |
| NVDA | 16 | $156.42 | $159.55 | $2,552.76 | 85 |
| ORCL | 9 | $224.73 | $236.75 | $2,130.76 | 70 |
| PEP | 15 | $136.59 | $135.55 | $2,033.25 | 65 |
| PFE | 78 | $25.30 | $25.48 | $1,987.05 | 65 |
| PG | 12 | $160.76 | $160.91 | $1,930.92 | 65 |
| PYPL | 30 | $76.80 | $76.83 | $2,304.90 | 75 |
| QCOM | 14 | $161.41 | $163.42 | $2,287.88 | 75 |
| T | 75 | $28.53 | $28.30 | $2,122.72 | 70 |
| TGT | 19 | $105.07 | $104.48 | $1,985.12 | 65 |
| TSLA | 6 | $313.02 | $317.52 | $1,905.12 | 65 |
| UNH | 7 | $314.75 | $310.00 | $2,170.00 | 70 |
| UNP | 9 | $236.50 | $237.88 | $2,140.92 | 70 |
| V | 6 | $352.90 | $358.38 | $2,150.28 | 70 |
| VZ | 46 | $43.73 | $43.53 | $2,002.61 | 65 |
| WFC | 31 | $82.32 | $83.53 | $2,589.28 | 85 |
| WMT | 23 | $97.36 | $97.96 | $2,253.08 | 75 |
| XOM | 23 | $110.16 | $112.22 | $2,581.06 | 85 |

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
| 2025-07-03 15:51:34 | SELL | GOOGL | 1 | $178.71 | $0.89 | 70 |
| 2025-07-03 15:51:34 | SELL | BAC | 1 | $48.99 | $0.32 | 75 |
| 2025-07-03 15:51:34 | SELL | INTC | 2 | $22.49 | $0.28 | 65 |
| 2025-07-03 15:51:34 | SELL | PFE | 2 | $25.48 | $0.34 | 65 |
| 2025-07-03 15:51:34 | SELL | CVX | 1 | $148.44 | $1.77 | 75 |
| 2025-07-03 15:51:34 | SELL | TGT | 1 | $104.50 | $-0.54 | 65 |
| 2025-07-03 15:51:34 | SELL | VZ | 1 | $43.53 | $-0.19 | 65 |
| 2025-07-03 15:51:34 | BUY | NVDA | 2 | $159.59 | N/A | 85 |
| 2025-07-03 15:51:34 | BUY | CRM | 1 | $274.11 | N/A | 75 |
| 2025-07-03 15:51:34 | BUY | XOM | 3 | $112.21 | N/A | 85 |
| 2025-07-03 15:51:34 | BUY | KO | 1 | $71.25 | N/A | 70 |
| 2025-07-03 15:51:34 | BUY | T | 3 | $28.30 | N/A | 70 |
| 2025-07-03 15:39:04 | SELL | NVDA | 1 | $159.87 | $3.64 | 70 |
| 2025-07-03 15:39:04 | SELL | BAC | 6 | $48.94 | $1.49 | 75 |
| 2025-07-03 15:39:04 | SELL | PFE | 6 | $25.45 | $0.81 | 65 |
| 2025-07-03 15:39:04 | SELL | QCOM | 1 | $163.60 | $2.04 | 70 |
| 2025-07-03 15:39:04 | BUY | WMT | 1 | $97.87 | N/A | 75 |
| 2025-07-03 15:39:04 | BUY | NKE | 5 | $76.42 | N/A | 85 |
| 2025-07-03 15:39:04 | BUY | CVX | 1 | $148.52 | N/A | 85 |
| 2025-07-03 15:26:19 | SELL | NVDA | 1 | $159.95 | $3.49 | 75 |
| 2025-07-03 15:26:19 | SELL | T | 5 | $28.27 | $-1.24 | 65 |
| 2025-07-03 15:26:19 | BUY | INTC | 7 | $22.48 | N/A | 65 |
| 2025-07-03 15:26:19 | BUY | BAC | 1 | $48.91 | N/A | 85 |
| 2025-07-03 15:26:19 | BUY | PYPL | 1 | $76.90 | N/A | 75 |
| 2025-07-03 15:26:19 | BUY | WMT | 1 | $97.87 | N/A | 70 |

<!--TRADE_LOG_END--> 
