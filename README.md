# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 20:26:11**

| Metric | Value |
|---|---|
| **Total Value** | **$101,223.79** |
| Cash | $2,456.63 |
| Holdings Value | $98,767.16 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.44 | $2,124.40 | 70 |
| ADBE | 5 | $377.60 | $378.47 | $1,892.35 | 65 |
| AMD | 15 | $135.93 | $138.52 | $2,077.80 | 70 |
| AMZN | 10 | $221.48 | $219.92 | $2,199.20 | 70 |
| AVGO | 8 | $269.38 | $269.90 | $2,159.20 | 70 |
| AXP | 8 | $324.40 | $325.61 | $2,604.88 | 80 |
| BA | 10 | $212.15 | $212.03 | $2,120.30 | 70 |
| BAC | 54 | $48.69 | $48.71 | $2,630.34 | 85 |
| C | 30 | $86.80 | $86.76 | $2,602.80 | 85 |
| CAT | 6 | $396.45 | $398.43 | $2,390.58 | 85 |
| COST | 2 | $979.83 | $982.36 | $1,964.72 | 65 |
| CRM | 7 | $267.51 | $269.21 | $1,884.47 | 65 |
| CSCO | 34 | $68.37 | $68.59 | $2,332.06 | 75 |
| CVX | 16 | $146.54 | $147.98 | $2,367.68 | 75 |
| DIS | 17 | $122.83 | $122.98 | $2,090.66 | 70 |
| GOOGL | 13 | $177.82 | $178.64 | $2,322.32 | 75 |
| GS | 3 | $717.52 | $715.89 | $2,147.67 | 70 |
| HD | 6 | $372.64 | $371.85 | $2,231.10 | 65 |
| INTC | 85 | $22.36 | $21.88 | $1,859.80 | 60 |
| JNJ | 13 | $155.80 | $155.56 | $2,022.28 | 65 |
| JPM | 8 | $292.56 | $292.00 | $2,336.00 | 85 |
| KO | 29 | $71.03 | $70.91 | $2,056.39 | 65 |
| LLY | 2 | $776.66 | $779.28 | $1,558.56 | 65 |
| MA | 3 | $561.03 | $561.52 | $1,684.56 | 65 |
| META | 3 | $717.12 | $713.57 | $2,140.71 | 75 |
| MRK | 28 | $82.40 | $82.39 | $2,306.92 | 75 |
| MSFT | 4 | $491.43 | $491.09 | $1,964.36 | 75 |
| NFLX | 1 | $1,279.00 | $1,284.86 | $1,284.86 | 70 |
| NKE | 34 | $75.86 | $76.39 | $2,597.26 | 85 |
| NVDA | 16 | $156.10 | $157.25 | $2,516.00 | 85 |
| ORCL | 10 | $225.25 | $229.98 | $2,299.80 | 70 |
| PEP | 15 | $136.59 | $136.48 | $2,047.20 | 65 |
| PFE | 85 | $25.33 | $25.32 | $2,152.20 | 70 |
| PG | 12 | $160.76 | $161.20 | $1,934.40 | 65 |
| PYPL | 30 | $76.82 | $76.31 | $2,289.30 | 75 |
| QCOM | 15 | $161.52 | $162.32 | $2,434.80 | 75 |
| T | 75 | $28.52 | $28.31 | $2,123.25 | 70 |
| TGT | 20 | $105.06 | $105.45 | $2,109.00 | 70 |
| TSLA | 6 | $313.02 | $315.65 | $1,893.90 | 65 |
| UNH | 7 | $314.75 | $307.56 | $2,152.92 | 65 |
| UNP | 9 | $236.50 | $237.16 | $2,134.44 | 70 |
| V | 5 | $352.10 | $354.22 | $1,771.10 | 65 |
| VZ | 52 | $43.73 | $43.59 | $2,266.68 | 75 |
| WFC | 28 | $82.27 | $82.36 | $2,306.08 | 75 |
| WMT | 21 | $97.32 | $97.61 | $2,049.81 | 70 |
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
| 2025-07-02 20:26:04 | SELL | GOOGL | 1 | $178.64 | $0.76 | 75 |
| 2025-07-02 20:26:04 | SELL | INTC | 7 | $21.88 | $-3.10 | 60 |
| 2025-07-02 20:26:04 | SELL | PFE | 1 | $25.32 | $-0.01 | 70 |
| 2025-07-02 20:26:04 | SELL | WFC | 4 | $82.36 | $0.31 | 75 |
| 2025-07-02 20:26:04 | SELL | ORCL | 1 | $229.98 | $4.30 | 70 |
| 2025-07-02 20:26:04 | BUY | NVDA | 2 | $157.25 | N/A | 85 |
| 2025-07-02 20:26:04 | BUY | C | 4 | $86.76 | N/A | 85 |
| 2025-07-02 20:26:04 | BUY | T | 4 | $28.31 | N/A | 70 |
| 2025-07-02 20:26:04 | BUY | VZ | 5 | $43.59 | N/A | 75 |
| 2025-07-02 20:09:02 | SELL | JPM | 1 | $291.94 | $-0.55 | 75 |
| 2025-07-02 20:09:02 | SELL | NVDA | 1 | $157.25 | $1.23 | 70 |
| 2025-07-02 20:09:02 | SELL | WMT | 1 | $97.60 | $0.27 | 65 |
| 2025-07-02 20:09:02 | SELL | C | 4 | $86.74 | $-0.24 | 70 |
| 2025-07-02 20:09:02 | BUY | INTC | 7 | $21.88 | N/A | 65 |
| 2025-07-02 20:09:02 | BUY | WFC | 1 | $82.35 | N/A | 85 |
| 2025-07-02 20:09:02 | BUY | CSCO | 1 | $68.59 | N/A | 75 |
| 2025-07-02 20:09:02 | BUY | ORCL | 2 | $229.98 | N/A | 85 |
| 2025-07-02 19:50:11 | SELL | NVDA | 1 | $157.05 | $0.96 | 75 |
| 2025-07-02 19:50:11 | SELL | INTC | 7 | $21.85 | $-3.29 | 60 |
| 2025-07-02 19:50:11 | SELL | BAC | 1 | $48.69 | $-0.00 | 85 |
| 2025-07-02 19:50:11 | SELL | PFE | 1 | $25.28 | $-0.04 | 70 |
| 2025-07-02 19:50:11 | SELL | ORCL | 1 | $227.85 | $2.81 | 65 |
| 2025-07-02 19:50:11 | SELL | T | 5 | $28.38 | $-0.74 | 65 |
| 2025-07-02 19:50:11 | BUY | GOOGL | 1 | $178.27 | N/A | 85 |
| 2025-07-02 19:50:11 | BUY | WMT | 1 | $97.63 | N/A | 70 |

<!--TRADE_LOG_END--> 
