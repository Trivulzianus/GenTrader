# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 09:51:52**

| Metric | Value |
|---|---|
| **Total Value** | **$101,223.79** |
| Cash | $2,569.72 |
| Holdings Value | $98,654.07 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.44 | $2,124.40 | 70 |
| ADBE | 5 | $377.60 | $378.47 | $1,892.35 | 65 |
| AMD | 15 | $135.93 | $138.52 | $2,077.80 | 70 |
| AMZN | 10 | $221.48 | $219.92 | $2,199.20 | 70 |
| AVGO | 8 | $269.90 | $269.90 | $2,159.20 | 70 |
| AXP | 8 | $324.40 | $325.61 | $2,604.88 | 85 |
| BA | 10 | $212.15 | $212.03 | $2,120.30 | 70 |
| BAC | 54 | $48.69 | $48.71 | $2,630.34 | 85 |
| C | 26 | $86.81 | $86.76 | $2,255.76 | 75 |
| CAT | 6 | $396.45 | $398.43 | $2,390.58 | 85 |
| COST | 2 | $979.83 | $982.36 | $1,964.72 | 65 |
| CRM | 7 | $267.51 | $269.21 | $1,884.47 | 65 |
| CSCO | 34 | $68.37 | $68.59 | $2,332.06 | 75 |
| CVX | 16 | $146.54 | $147.98 | $2,367.68 | 75 |
| DIS | 17 | $122.83 | $122.98 | $2,090.66 | 70 |
| GOOGL | 13 | $177.82 | $178.64 | $2,322.32 | 75 |
| GS | 3 | $717.52 | $715.89 | $2,147.67 | 85 |
| HD | 6 | $372.64 | $371.85 | $2,231.10 | 70 |
| INTC | 90 | $22.33 | $21.88 | $1,969.20 | 65 |
| JNJ | 13 | $155.80 | $155.56 | $2,022.28 | 65 |
| JPM | 9 | $292.50 | $292.00 | $2,628.00 | 85 |
| KO | 28 | $71.03 | $70.91 | $1,985.48 | 65 |
| LLY | 2 | $776.66 | $779.28 | $1,558.56 | 70 |
| MA | 3 | $561.03 | $561.52 | $1,684.56 | 65 |
| META | 3 | $717.12 | $713.57 | $2,140.71 | 75 |
| MRK | 28 | $82.40 | $82.39 | $2,306.92 | 75 |
| MSFT | 5 | $491.36 | $491.09 | $2,455.45 | 85 |
| NFLX | 1 | $1,279.00 | $1,284.86 | $1,284.86 | 65 |
| NKE | 34 | $75.86 | $76.39 | $2,597.26 | 85 |
| NVDA | 14 | $155.93 | $157.25 | $2,201.50 | 75 |
| ORCL | 9 | $224.73 | $229.98 | $2,069.82 | 70 |
| PEP | 15 | $136.59 | $136.48 | $2,047.20 | 65 |
| PFE | 85 | $25.33 | $25.32 | $2,152.20 | 70 |
| PG | 12 | $160.76 | $161.20 | $1,934.40 | 65 |
| PYPL | 30 | $76.82 | $76.31 | $2,289.30 | 75 |
| QCOM | 15 | $161.52 | $162.32 | $2,434.80 | 85 |
| T | 70 | $28.54 | $28.31 | $1,981.70 | 65 |
| TGT | 20 | $105.06 | $105.45 | $2,109.00 | 70 |
| TSLA | 6 | $313.02 | $315.65 | $1,893.90 | 60 |
| UNH | 7 | $314.75 | $307.56 | $2,152.92 | 65 |
| UNP | 9 | $236.50 | $237.16 | $2,134.44 | 75 |
| V | 5 | $352.10 | $354.22 | $1,771.10 | 65 |
| VZ | 46 | $43.75 | $43.59 | $2,005.14 | 65 |
| WFC | 30 | $82.28 | $82.36 | $2,470.80 | 80 |
| WMT | 23 | $97.34 | $97.61 | $2,245.03 | 75 |
| XOM | 21 | $109.93 | $111.05 | $2,332.05 | 75 |

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
| 2025-07-03 09:51:48 | SELL | T | 1 | $28.31 | $-0.22 | 65 |
| 2025-07-03 09:51:48 | SELL | CVX | 1 | $147.98 | $1.36 | 75 |
| 2025-07-03 09:51:48 | BUY | INTC | 6 | $21.88 | N/A | 65 |
| 2025-07-03 09:51:48 | BUY | WMT | 2 | $97.61 | N/A | 75 |
| 2025-07-03 09:51:48 | BUY | TGT | 1 | $105.45 | N/A | 70 |
| 2025-07-03 09:40:18 | SELL | INTC | 1 | $21.88 | $-0.48 | 60 |
| 2025-07-03 09:40:18 | SELL | WMT | 1 | $97.61 | $0.28 | 65 |
| 2025-07-03 09:40:18 | SELL | WFC | 1 | $82.36 | $0.08 | 80 |
| 2025-07-03 09:40:18 | SELL | QCOM | 1 | $162.32 | $0.75 | 75 |
| 2025-07-03 09:40:18 | SELL | TGT | 1 | $105.45 | $0.39 | 65 |
| 2025-07-03 09:40:18 | BUY | C | 1 | $86.76 | N/A | 75 |
| 2025-07-03 09:26:32 | SELL | C | 1 | $86.76 | $-0.05 | 70 |
| 2025-07-03 09:26:32 | SELL | VZ | 1 | $43.59 | $-0.15 | 65 |
| 2025-07-03 09:26:32 | BUY | NKE | 1 | $76.39 | N/A | 85 |
| 2025-07-03 09:26:32 | BUY | QCOM | 1 | $162.32 | N/A | 85 |
| 2025-07-03 09:26:32 | BUY | CVX | 1 | $147.98 | N/A | 85 |
| 2025-07-03 09:09:35 | SELL | NKE | 1 | $76.39 | $0.53 | 80 |
| 2025-07-03 09:09:35 | SELL | QCOM | 1 | $162.32 | $0.75 | 75 |
| 2025-07-03 09:09:35 | SELL | VZ | 3 | $43.59 | $-0.43 | 65 |
| 2025-07-03 09:09:35 | SELL | CVX | 1 | $147.98 | $1.36 | 75 |
| 2025-07-03 09:09:35 | BUY | JPM | 1 | $292.00 | N/A | 85 |
| 2025-07-03 08:55:20 | SELL | INTC | 6 | $21.88 | $-2.68 | 60 |
| 2025-07-03 08:55:20 | SELL | VZ | 3 | $43.59 | $-0.41 | 70 |
| 2025-07-03 08:55:20 | SELL | T | 4 | $28.31 | $-0.84 | 65 |
| 2025-07-03 08:55:20 | BUY | WMT | 1 | $97.61 | N/A | 70 |

<!--TRADE_LOG_END--> 
