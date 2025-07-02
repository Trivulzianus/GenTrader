# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 17:08:24**

| Metric | Value |
|---|---|
| **Total Value** | **$100,993.77** |
| Cash | $3,707.85 |
| Holdings Value | $97,285.91 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $210.99 | $2,109.85 | 70 |
| ADBE | 5 | $377.60 | $373.74 | $1,868.69 | 70 |
| AMD | 16 | $136.11 | $139.28 | $2,228.56 | 70 |
| AMZN | 10 | $221.48 | $220.79 | $2,207.95 | 75 |
| AVGO | 8 | $269.38 | $271.00 | $2,168.04 | 70 |
| AXP | 8 | $324.40 | $324.87 | $2,598.96 | 85 |
| BA | 10 | $212.15 | $212.40 | $2,123.99 | 65 |
| BAC | 54 | $48.67 | $48.49 | $2,618.46 | 85 |
| C | 24 | $86.82 | $86.64 | $2,079.24 | 65 |
| CAT | 6 | $396.45 | $395.52 | $2,373.12 | 65 |
| COST | 2 | $979.83 | $981.52 | $1,963.04 | 65 |
| CRM | 7 | $267.51 | $267.39 | $1,871.76 | 65 |
| CSCO | 34 | $68.37 | $68.53 | $2,330.02 | 75 |
| CVX | 16 | $146.51 | $146.46 | $2,343.36 | 75 |
| DIS | 17 | $122.83 | $122.79 | $2,087.45 | 65 |
| GOOGL | 13 | $177.82 | $178.24 | $2,317.12 | 75 |
| GS | 3 | $717.52 | $715.41 | $2,146.22 | 70 |
| HD | 5 | $372.57 | $371.40 | $1,857.02 | 65 |
| INTC | 85 | $22.36 | $22.09 | $1,877.23 | 60 |
| JNJ | 13 | $155.80 | $155.49 | $2,021.37 | 65 |
| JPM | 9 | $292.49 | $291.85 | $2,626.61 | 85 |
| KO | 28 | $71.03 | $70.94 | $1,986.18 | 65 |
| LLY | 2 | $776.66 | $776.90 | $1,553.81 | 65 |
| MA | 3 | $561.03 | $559.55 | $1,678.65 | 70 |
| META | 3 | $717.12 | $717.37 | $2,152.11 | 75 |
| MRK | 28 | $82.40 | $82.00 | $2,296.00 | 75 |
| MSFT | 4 | $491.43 | $490.98 | $1,963.92 | 70 |
| NFLX | 1 | $1,279.00 | $1,277.33 | $1,277.33 | 65 |
| NKE | 34 | $75.85 | $76.03 | $2,585.19 | 85 |
| NVDA | 15 | $156.27 | $157.41 | $2,361.20 | 75 |
| ORCL | 10 | $224.98 | $225.35 | $2,253.55 | 65 |
| PEP | 15 | $136.59 | $136.39 | $2,045.85 | 65 |
| PFE | 86 | $25.33 | $25.21 | $2,168.09 | 70 |
| PG | 12 | $160.76 | $160.67 | $1,928.04 | 65 |
| PYPL | 30 | $76.82 | $76.05 | $2,281.50 | 75 |
| QCOM | 14 | $161.49 | $161.55 | $2,261.70 | 75 |
| T | 71 | $28.50 | $28.46 | $2,020.66 | 65 |
| TGT | 20 | $105.06 | $104.42 | $2,088.40 | 65 |
| TSLA | 6 | $313.02 | $314.35 | $1,886.11 | 65 |
| UNH | 6 | $315.70 | $312.67 | $1,875.99 | 65 |
| UNP | 9 | $236.50 | $235.58 | $2,120.22 | 75 |
| V | 5 | $352.10 | $351.88 | $1,759.42 | 65 |
| VZ | 47 | $43.75 | $43.59 | $2,048.97 | 65 |
| WFC | 32 | $82.28 | $82.03 | $2,624.80 | 85 |
| WMT | 21 | $97.30 | $97.50 | $2,047.39 | 65 |
| XOM | 20 | $109.91 | $110.14 | $2,202.80 | 70 |

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
| 2025-07-02 17:08:18 | SELL | INTC | 7 | $22.10 | $-1.65 | 60 |
| 2025-07-02 17:08:18 | SELL | WMT | 2 | $97.50 | $0.36 | 65 |
| 2025-07-02 17:08:18 | SELL | C | 6 | $86.64 | $-0.86 | 65 |
| 2025-07-02 17:08:18 | SELL | VZ | 2 | $43.60 | $-0.29 | 65 |
| 2025-07-02 17:08:18 | BUY | NVDA | 1 | $153.30 | N/A | 75 |
| 2025-07-02 17:08:18 | BUY | NKE | 2 | $76.04 | N/A | 85 |
| 2025-07-02 17:08:18 | BUY | PFE | 5 | $25.22 | N/A | 70 |
| 2025-07-02 17:08:18 | BUY | MRK | 3 | $81.81 | N/A | 75 |
| 2025-07-02 16:55:51 | SELL | NVDA | 2 | $157.33 | $1.47 | 70 |
| 2025-07-02 16:55:51 | SELL | MRK | 3 | $82.13 | $-0.91 | 65 |
| 2025-07-02 16:55:51 | SELL | T | 1 | $28.52 | $0.02 | 65 |
| 2025-07-02 16:55:51 | SELL | CVX | 1 | $146.48 | $-0.03 | 75 |
| 2025-07-02 16:55:51 | BUY | WMT | 2 | $97.59 | N/A | 75 |
| 2025-07-02 16:55:51 | BUY | NKE | 1 | $76.05 | N/A | 80 |
| 2025-07-02 16:55:51 | BUY | C | 4 | $86.75 | N/A | 85 |
| 2025-07-02 16:55:51 | BUY | BA | 1 | $212.72 | N/A | 70 |
| 2025-07-02 16:55:51 | BUY | CAT | 1 | $395.95 | N/A | 85 |
| 2025-07-02 16:55:51 | BUY | CSCO | 2 | $68.61 | N/A | 75 |
| 2025-07-02 16:55:51 | BUY | VZ | 3 | $43.69 | N/A | 70 |
| 2025-07-02 16:43:41 | SELL | AAPL | 1 | $210.38 | $-0.98 | 65 |
| 2025-07-02 16:43:41 | SELL | NKE | 3 | $76.15 | $0.86 | 75 |
| 2025-07-02 16:43:41 | SELL | PFE | 5 | $25.24 | $-0.47 | 65 |
| 2025-07-02 16:43:41 | SELL | CSCO | 2 | $68.62 | $0.50 | 70 |
| 2025-07-02 16:43:41 | BUY | INTC | 7 | $22.10 | N/A | 65 |
| 2025-07-02 16:43:41 | BUY | AXP | 1 | $324.77 | N/A | 85 |

<!--TRADE_LOG_END--> 
