# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 15:39:10**

| Metric | Value |
|---|---|
| **Total Value** | **$101,922.05** |
| Cash | $2,418.49 |
| Holdings Value | $99,503.55 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $214.03 | $2,140.25 | 70 |
| ADBE | 5 | $377.60 | $382.11 | $1,910.55 | 65 |
| AMD | 15 | $135.93 | $138.42 | $2,076.30 | 70 |
| AMZN | 10 | $221.48 | $223.09 | $2,230.85 | 75 |
| AVGO | 8 | $269.90 | $274.94 | $2,199.52 | 70 |
| AXP | 8 | $324.40 | $327.86 | $2,622.88 | 85 |
| BA | 10 | $212.15 | $215.80 | $2,158.01 | 65 |
| BAC | 48 | $48.66 | $48.93 | $2,348.75 | 75 |
| C | 30 | $86.80 | $88.49 | $2,654.70 | 85 |
| CAT | 6 | $396.45 | $399.95 | $2,399.72 | 70 |
| COST | 2 | $979.83 | $983.06 | $1,966.12 | 65 |
| CRM | 7 | $267.51 | $274.49 | $1,921.44 | 65 |
| CSCO | 33 | $68.37 | $69.19 | $2,283.11 | 75 |
| CVX | 17 | $146.67 | $148.53 | $2,525.01 | 85 |
| DIS | 18 | $122.90 | $123.56 | $2,224.10 | 75 |
| GOOGL | 13 | $177.82 | $178.95 | $2,326.35 | 70 |
| GS | 3 | $717.52 | $721.52 | $2,164.57 | 85 |
| HD | 6 | $372.64 | $371.20 | $2,227.20 | 70 |
| INTC | 90 | $22.34 | $22.61 | $2,034.91 | 65 |
| JNJ | 13 | $155.80 | $155.94 | $2,027.22 | 65 |
| JPM | 9 | $292.50 | $295.10 | $2,655.86 | 85 |
| KO | 28 | $71.03 | $71.19 | $1,993.46 | 65 |
| LLY | 2 | $776.66 | $773.78 | $1,547.56 | 65 |
| MA | 3 | $561.03 | $568.39 | $1,705.18 | 65 |
| META | 3 | $717.12 | $719.03 | $2,157.11 | 85 |
| MRK | 25 | $82.46 | $81.31 | $2,032.63 | 65 |
| MSFT | 5 | $491.36 | $499.06 | $2,495.30 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.51 | $1,297.51 | 65 |
| NKE | 34 | $75.84 | $76.43 | $2,598.62 | 85 |
| NVDA | 14 | $155.97 | $159.96 | $2,239.44 | 70 |
| ORCL | 9 | $224.73 | $236.20 | $2,125.78 | 75 |
| PEP | 15 | $136.59 | $135.42 | $2,031.30 | 65 |
| PFE | 80 | $25.31 | $25.45 | $2,035.60 | 65 |
| PG | 12 | $160.76 | $160.86 | $1,930.32 | 65 |
| PYPL | 30 | $76.80 | $76.82 | $2,304.60 | 75 |
| QCOM | 14 | $161.41 | $163.60 | $2,290.40 | 70 |
| T | 72 | $28.54 | $28.29 | $2,036.52 | 65 |
| TGT | 20 | $105.04 | $104.69 | $2,093.70 | 65 |
| TSLA | 6 | $313.02 | $316.36 | $1,898.17 | 65 |
| UNH | 7 | $314.75 | $310.12 | $2,170.84 | 65 |
| UNP | 9 | $236.50 | $237.73 | $2,139.57 | 65 |
| V | 6 | $352.90 | $357.95 | $2,147.73 | 65 |
| VZ | 47 | $43.73 | $43.49 | $2,044.26 | 65 |
| WFC | 31 | $82.32 | $83.64 | $2,592.84 | 85 |
| WMT | 23 | $97.36 | $97.86 | $2,250.89 | 75 |
| XOM | 20 | $109.86 | $112.34 | $2,246.80 | 75 |

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
| 2025-07-03 15:26:19 | BUY | PFE | 6 | $25.32 | N/A | 70 |
| 2025-07-03 15:08:50 | SELL | INTC | 1 | $22.42 | $0.09 | 60 |
| 2025-07-03 15:08:50 | SELL | WMT | 1 | $97.94 | $0.60 | 65 |
| 2025-07-03 15:08:50 | SELL | NKE | 5 | $76.24 | $2.12 | 70 |
| 2025-07-03 15:08:50 | SELL | PYPL | 1 | $77.21 | $0.39 | 70 |
| 2025-07-03 15:08:50 | BUY | NVDA | 2 | $159.63 | N/A | 85 |
| 2025-07-03 15:08:50 | BUY | BAC | 6 | $49.03 | N/A | 85 |
| 2025-07-03 15:08:50 | BUY | QCOM | 1 | $163.60 | N/A | 80 |
| 2025-07-03 14:52:10 | SELL | INTC | 6 | $22.36 | $0.16 | 60 |
| 2025-07-03 14:52:10 | SELL | PFE | 6 | $25.45 | $0.77 | 65 |
| 2025-07-03 14:52:10 | BUY | NKE | 5 | $76.02 | N/A | 85 |
| 2025-07-03 14:52:10 | BUY | WFC | 1 | $83.65 | N/A | 85 |

<!--TRADE_LOG_END--> 
