# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 16:09:47**

| Metric | Value |
|---|---|
| **Total Value** | **$101,961.10** |
| Cash | $2,857.25 |
| Holdings Value | $99,103.85 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $214.30 | $2,143.00 | 70 |
| ADBE | 5 | $377.60 | $382.13 | $1,910.65 | 65 |
| AMD | 15 | $135.93 | $138.19 | $2,072.85 | 70 |
| AMZN | 10 | $221.48 | $223.38 | $2,233.80 | 75 |
| AVGO | 8 | $269.90 | $274.92 | $2,199.36 | 70 |
| AXP | 8 | $324.40 | $328.29 | $2,626.32 | 85 |
| BA | 10 | $212.15 | $216.09 | $2,160.90 | 70 |
| BAC | 45 | $48.64 | $48.98 | $2,204.32 | 70 |
| C | 30 | $86.80 | $88.58 | $2,657.25 | 85 |
| CAT | 6 | $396.45 | $399.47 | $2,396.82 | 75 |
| COST | 2 | $979.83 | $985.41 | $1,970.83 | 65 |
| CRM | 8 | $268.33 | $273.56 | $2,188.52 | 65 |
| CSCO | 32 | $68.33 | $69.42 | $2,221.44 | 70 |
| CVX | 16 | $146.55 | $148.59 | $2,377.44 | 75 |
| DIS | 17 | $122.84 | $123.94 | $2,107.07 | 65 |
| GOOGL | 12 | $177.75 | $178.76 | $2,145.12 | 70 |
| GS | 3 | $717.52 | $721.79 | $2,165.37 | 85 |
| HD | 6 | $372.64 | $371.88 | $2,231.26 | 65 |
| INTC | 89 | $22.34 | $22.55 | $2,006.51 | 65 |
| JNJ | 13 | $155.80 | $156.09 | $2,029.17 | 65 |
| JPM | 9 | $292.50 | $295.55 | $2,659.93 | 85 |
| KO | 30 | $71.05 | $71.21 | $2,136.22 | 70 |
| LLY | 2 | $776.66 | $776.74 | $1,553.48 | 65 |
| MA | 3 | $561.03 | $567.41 | $1,702.24 | 65 |
| META | 3 | $717.12 | $718.84 | $2,156.51 | 85 |
| MRK | 25 | $82.46 | $81.33 | $2,033.25 | 65 |
| MSFT | 5 | $491.36 | $499.64 | $2,498.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,300.50 | $1,300.50 | 65 |
| NKE | 33 | $75.82 | $76.52 | $2,524.99 | 80 |
| NVDA | 14 | $155.97 | $159.53 | $2,233.44 | 70 |
| ORCL | 9 | $224.73 | $236.54 | $2,128.90 | 75 |
| PEP | 15 | $136.59 | $135.40 | $2,031.00 | 65 |
| PFE | 91 | $25.33 | $25.48 | $2,318.68 | 75 |
| PG | 12 | $160.76 | $160.49 | $1,925.88 | 65 |
| PYPL | 30 | $76.80 | $76.81 | $2,304.45 | 75 |
| QCOM | 14 | $161.41 | $163.23 | $2,285.17 | 75 |
| T | 76 | $28.52 | $28.35 | $2,154.60 | 70 |
| TGT | 19 | $105.07 | $104.64 | $1,988.07 | 65 |
| TSLA | 6 | $313.02 | $317.63 | $1,905.76 | 60 |
| UNH | 7 | $314.75 | $309.69 | $2,167.83 | 65 |
| UNP | 9 | $236.50 | $237.84 | $2,140.56 | 70 |
| V | 6 | $352.90 | $358.36 | $2,150.16 | 70 |
| VZ | 46 | $43.73 | $43.52 | $2,002.15 | 65 |
| WFC | 28 | $82.19 | $83.55 | $2,339.26 | 75 |
| WMT | 21 | $97.30 | $97.99 | $2,057.79 | 65 |
| XOM | 21 | $109.97 | $112.23 | $2,356.83 | 75 |

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
| 2025-07-03 16:09:40 | SELL | NVDA | 2 | $159.57 | $6.29 | 70 |
| 2025-07-03 16:09:40 | SELL | BAC | 2 | $48.99 | $0.65 | 70 |
| 2025-07-03 16:09:40 | SELL | XOM | 2 | $112.21 | $4.10 | 75 |
| 2025-07-03 16:09:40 | SELL | NKE | 1 | $76.53 | $0.68 | 80 |
| 2025-07-03 16:09:40 | SELL | WMT | 2 | $98.00 | $1.27 | 65 |
| 2025-07-03 16:09:40 | SELL | DIS | 1 | $123.95 | $1.05 | 65 |
| 2025-07-03 16:09:40 | SELL | WFC | 3 | $83.54 | $3.67 | 75 |
| 2025-07-03 16:09:40 | SELL | CSCO | 1 | $69.42 | $1.05 | 70 |
| 2025-07-03 16:09:40 | BUY | INTC | 1 | $22.54 | N/A | 65 |
| 2025-07-03 16:09:40 | BUY | KO | 1 | $71.22 | N/A | 70 |
| 2025-07-03 16:09:40 | BUY | PFE | 13 | $25.48 | N/A | 75 |
| 2025-07-03 16:09:40 | BUY | T | 1 | $28.35 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
