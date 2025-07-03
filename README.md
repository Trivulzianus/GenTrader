# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 15:08:57**

| Metric | Value |
|---|---|
| **Total Value** | **$101,924.90** |
| Cash | $2,508.81 |
| Holdings Value | $99,416.09 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $214.11 | $2,141.10 | 75 |
| ADBE | 5 | $377.60 | $381.17 | $1,905.85 | 65 |
| AMD | 15 | $135.93 | $138.12 | $2,071.80 | 70 |
| AMZN | 10 | $221.48 | $222.23 | $2,222.32 | 75 |
| AVGO | 8 | $269.90 | $274.42 | $2,195.36 | 70 |
| AXP | 8 | $324.40 | $328.98 | $2,631.84 | 85 |
| BA | 10 | $212.15 | $216.12 | $2,161.20 | 70 |
| BAC | 53 | $48.69 | $49.03 | $2,598.66 | 85 |
| C | 30 | $86.80 | $88.51 | $2,655.30 | 85 |
| CAT | 6 | $396.45 | $400.49 | $2,402.97 | 70 |
| COST | 2 | $979.83 | $985.09 | $1,970.17 | 65 |
| CRM | 7 | $267.51 | $273.80 | $1,916.57 | 65 |
| CSCO | 33 | $68.37 | $69.30 | $2,286.74 | 75 |
| CVX | 16 | $146.55 | $148.69 | $2,379.04 | 80 |
| DIS | 18 | $122.90 | $123.42 | $2,221.48 | 70 |
| GOOGL | 13 | $177.82 | $178.60 | $2,321.80 | 70 |
| GS | 3 | $717.52 | $723.68 | $2,171.04 | 85 |
| HD | 6 | $372.64 | $372.36 | $2,234.16 | 65 |
| INTC | 83 | $22.33 | $22.43 | $1,861.28 | 60 |
| JNJ | 13 | $155.80 | $155.96 | $2,027.42 | 65 |
| JPM | 9 | $292.50 | $295.87 | $2,662.83 | 85 |
| KO | 28 | $71.03 | $71.07 | $1,989.96 | 65 |
| LLY | 2 | $776.66 | $779.46 | $1,558.92 | 70 |
| MA | 3 | $561.03 | $567.91 | $1,703.73 | 65 |
| META | 3 | $717.12 | $717.54 | $2,152.62 | 85 |
| MRK | 25 | $82.46 | $81.34 | $2,033.41 | 65 |
| MSFT | 5 | $491.36 | $499.51 | $2,497.55 | 85 |
| NFLX | 1 | $1,279.00 | $1,295.28 | $1,295.28 | 65 |
| NKE | 29 | $75.74 | $76.23 | $2,210.69 | 70 |
| NVDA | 16 | $156.46 | $159.62 | $2,553.92 | 85 |
| ORCL | 9 | $224.73 | $234.33 | $2,108.97 | 70 |
| PEP | 15 | $136.59 | $135.30 | $2,029.50 | 65 |
| PFE | 80 | $25.32 | $25.45 | $2,036.00 | 65 |
| PG | 12 | $160.76 | $160.83 | $1,929.96 | 65 |
| PYPL | 29 | $76.80 | $77.24 | $2,239.96 | 70 |
| QCOM | 15 | $161.56 | $163.60 | $2,454.00 | 80 |
| T | 77 | $28.52 | $28.32 | $2,180.64 | 70 |
| TGT | 20 | $105.04 | $104.39 | $2,087.80 | 65 |
| TSLA | 6 | $313.02 | $316.31 | $1,897.86 | 55 |
| UNH | 7 | $314.75 | $311.99 | $2,183.90 | 65 |
| UNP | 9 | $236.50 | $237.73 | $2,139.57 | 70 |
| V | 6 | $352.90 | $358.46 | $2,150.76 | 70 |
| VZ | 47 | $43.73 | $43.45 | $2,042.32 | 65 |
| WFC | 31 | $82.32 | $83.86 | $2,599.51 | 85 |
| WMT | 21 | $97.31 | $97.93 | $2,056.56 | 65 |
| XOM | 20 | $109.86 | $112.19 | $2,243.80 | 75 |

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
| 2025-07-03 14:26:03 | BUY | NVDA | 2 | $160.84 | N/A | 85 |
| 2025-07-03 14:26:03 | BUY | PFE | 6 | $25.25 | N/A | 70 |
| 2025-07-03 14:08:35 | SELL | NKE | 5 | $76.23 | $1.92 | 70 |
| 2025-07-03 14:08:35 | SELL | MRK | 2 | $81.92 | $-0.99 | 65 |
| 2025-07-03 14:08:35 | SELL | PFE | 4 | $25.33 | $0.02 | 65 |
| 2025-07-03 14:08:35 | SELL | VZ | 2 | $43.67 | $-0.12 | 65 |
| 2025-07-03 14:08:35 | SELL | T | 5 | $28.35 | $-0.83 | 65 |

<!--TRADE_LOG_END--> 
