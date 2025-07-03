# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 15:26:26**

| Metric | Value |
|---|---|
| **Total Value** | **$101,874.17** |
| Cash | $2,277.14 |
| Holdings Value | $99,597.03 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $214.06 | $2,140.55 | 75 |
| ADBE | 5 | $377.60 | $381.45 | $1,907.27 | 65 |
| AMD | 15 | $135.93 | $138.20 | $2,073.00 | 65 |
| AMZN | 10 | $221.48 | $222.79 | $2,227.94 | 75 |
| AVGO | 8 | $269.90 | $275.00 | $2,200.00 | 70 |
| AXP | 8 | $324.40 | $327.23 | $2,617.84 | 85 |
| BA | 10 | $212.15 | $215.85 | $2,158.50 | 70 |
| BAC | 54 | $48.70 | $48.91 | $2,641.14 | 85 |
| C | 30 | $86.80 | $88.31 | $2,649.30 | 85 |
| CAT | 6 | $396.45 | $399.58 | $2,397.51 | 70 |
| COST | 2 | $979.83 | $984.69 | $1,969.38 | 60 |
| CRM | 7 | $267.51 | $274.25 | $1,919.75 | 65 |
| CSCO | 33 | $68.37 | $69.05 | $2,278.70 | 75 |
| CVX | 16 | $146.55 | $148.82 | $2,381.12 | 75 |
| DIS | 18 | $122.90 | $123.41 | $2,221.38 | 70 |
| GOOGL | 13 | $177.82 | $178.88 | $2,325.44 | 70 |
| GS | 3 | $717.52 | $721.65 | $2,164.95 | 85 |
| HD | 6 | $372.64 | $370.90 | $2,225.43 | 65 |
| INTC | 90 | $22.34 | $22.48 | $2,022.98 | 65 |
| JNJ | 13 | $155.80 | $155.93 | $2,027.09 | 65 |
| JPM | 9 | $292.50 | $295.24 | $2,657.16 | 85 |
| KO | 28 | $71.03 | $71.12 | $1,991.31 | 65 |
| LLY | 2 | $776.66 | $778.45 | $1,556.89 | 65 |
| MA | 3 | $561.03 | $567.82 | $1,703.46 | 65 |
| META | 3 | $717.12 | $718.08 | $2,154.23 | 75 |
| MRK | 25 | $82.46 | $81.31 | $2,032.63 | 65 |
| MSFT | 5 | $491.36 | $498.55 | $2,492.72 | 85 |
| NFLX | 1 | $1,279.00 | $1,297.20 | $1,297.20 | 70 |
| NKE | 29 | $75.74 | $76.31 | $2,212.85 | 70 |
| NVDA | 15 | $156.23 | $159.90 | $2,398.50 | 75 |
| ORCL | 9 | $224.73 | $235.19 | $2,116.71 | 65 |
| PEP | 15 | $136.59 | $135.40 | $2,031.00 | 65 |
| PFE | 86 | $25.32 | $25.45 | $2,189.13 | 70 |
| PG | 12 | $160.76 | $160.66 | $1,927.92 | 65 |
| PYPL | 30 | $76.80 | $76.89 | $2,306.85 | 75 |
| QCOM | 15 | $161.56 | $163.88 | $2,458.12 | 75 |
| T | 72 | $28.54 | $28.28 | $2,036.16 | 65 |
| TGT | 20 | $105.04 | $104.36 | $2,087.28 | 65 |
| TSLA | 6 | $313.02 | $317.70 | $1,906.19 | 65 |
| UNH | 7 | $314.75 | $310.40 | $2,172.80 | 65 |
| UNP | 9 | $236.50 | $237.55 | $2,137.95 | 70 |
| V | 6 | $352.90 | $358.00 | $2,148.03 | 70 |
| VZ | 47 | $43.73 | $43.46 | $2,042.62 | 65 |
| WFC | 31 | $82.32 | $83.52 | $2,588.97 | 85 |
| WMT | 22 | $97.34 | $97.89 | $2,153.47 | 70 |
| XOM | 20 | $109.86 | $112.38 | $2,247.60 | 75 |

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
| 2025-07-03 14:52:10 | BUY | T | 5 | $28.39 | N/A | 70 |
| 2025-07-03 14:40:23 | SELL | NVDA | 2 | $160.31 | $7.52 | 70 |
| 2025-07-03 14:40:23 | SELL | WFC | 1 | $83.73 | $1.41 | 80 |
| 2025-07-03 14:40:23 | BUY | BAC | 2 | $49.05 | N/A | 75 |
| 2025-07-03 14:40:23 | BUY | INTC | 7 | $22.34 | N/A | 65 |
| 2025-07-03 14:40:23 | BUY | WMT | 1 | $97.88 | N/A | 70 |
| 2025-07-03 14:26:03 | SELL | BAC | 8 | $48.94 | $2.14 | 70 |

<!--TRADE_LOG_END--> 
