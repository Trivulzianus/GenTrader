# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 20:09:23**

| Metric | Value |
|---|---|
| **Total Value** | **$100,770.94** |
| Cash | $616.93 |
| Holdings Value | $100,154.01 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $210.97 | $209.95 | $2,309.45 | 75 |
| ADBE | 5 | $377.60 | $376.93 | $1,884.65 | 65 |
| AMD | 15 | $135.73 | $134.80 | $2,022.00 | 65 |
| AMZN | 11 | $221.72 | $223.47 | $2,458.17 | 75 |
| AVGO | 8 | $275.34 | $274.18 | $2,193.44 | 70 |
| AXP | 7 | $324.46 | $322.77 | $2,259.39 | 70 |
| BA | 10 | $212.15 | $218.52 | $2,185.20 | 65 |
| BAC | 54 | $48.70 | $48.65 | $2,626.83 | 85 |
| C | 30 | $86.58 | $87.61 | $2,628.45 | 85 |
| CAT | 6 | $397.86 | $391.62 | $2,349.72 | 85 |
| COST | 2 | $979.83 | $992.18 | $1,984.36 | 65 |
| CRM | 8 | $268.33 | $269.71 | $2,157.68 | 65 |
| CSCO | 32 | $68.36 | $68.93 | $2,205.76 | 70 |
| CVX | 16 | $146.70 | $147.39 | $2,358.24 | 75 |
| DIS | 17 | $122.84 | $123.18 | $2,094.06 | 65 |
| GOOGL | 13 | $179.38 | $176.79 | $2,298.27 | 75 |
| GS | 3 | $717.52 | $710.27 | $2,130.81 | 70 |
| HD | 6 | $372.64 | $367.71 | $2,206.26 | 65 |
| INTC | 85 | $22.27 | $22.00 | $1,870.00 | 60 |
| JNJ | 13 | $155.80 | $155.28 | $2,018.64 | 65 |
| JPM | 9 | $292.50 | $291.89 | $2,627.01 | 85 |
| KO | 29 | $71.03 | $71.03 | $2,059.87 | 65 |
| LLY | 2 | $776.66 | $772.84 | $1,545.68 | 65 |
| MA | 4 | $563.08 | $565.12 | $2,260.48 | 70 |
| META | 3 | $717.12 | $718.35 | $2,155.05 | 70 |
| MRK | 28 | $82.42 | $80.89 | $2,265.06 | 75 |
| MSFT | 5 | $498.84 | $497.72 | $2,488.60 | 85 |
| NFLX | 1 | $1,279.00 | $1,289.62 | $1,289.62 | 70 |
| NKE | 29 | $75.84 | $76.56 | $2,220.10 | 70 |
| NVDA | 14 | $156.23 | $158.24 | $2,215.36 | 70 |
| ORCL | 10 | $233.29 | $232.34 | $2,323.45 | 75 |
| PEP | 15 | $136.57 | $134.45 | $2,016.75 | 65 |
| PFE | 85 | $25.29 | $25.24 | $2,145.40 | 70 |
| PG | 13 | $160.77 | $160.49 | $2,086.37 | 65 |
| PYPL | 29 | $76.81 | $76.18 | $2,209.22 | 70 |
| QCOM | 15 | $161.50 | $158.09 | $2,371.35 | 75 |
| T | 71 | $28.54 | $28.41 | $2,016.76 | 65 |
| TGT | 20 | $104.90 | $101.61 | $2,032.20 | 65 |
| TSLA | 7 | $289.38 | $293.94 | $2,057.58 | 65 |
| UNH | 7 | $314.75 | $303.73 | $2,126.11 | 65 |
| UNP | 10 | $236.53 | $235.34 | $2,353.45 | 75 |
| V | 6 | $355.95 | $356.64 | $2,139.84 | 70 |
| VZ | 47 | $43.72 | $42.82 | $2,012.54 | 65 |
| WFC | 29 | $82.35 | $82.33 | $2,387.57 | 75 |
| WMT | 23 | $97.38 | $99.34 | $2,284.82 | 75 |
| XOM | 20 | $109.91 | $111.12 | $2,222.40 | 75 |

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
| 2025-07-07 20:09:18 | SELL | DIS | 1 | $123.18 | $0.32 | 65 |
| 2025-07-07 20:09:18 | SELL | NKE | 5 | $76.56 | $3.04 | 70 |
| 2025-07-07 20:09:18 | SELL | PYPL | 2 | $76.18 | $-1.17 | 70 |
| 2025-07-07 20:09:18 | SELL | WFC | 2 | $82.33 | $-0.04 | 75 |
| 2025-07-07 20:09:18 | SELL | UNP | 1 | $235.35 | $-1.08 | 75 |
| 2025-07-07 20:09:18 | BUY | AAPL | 1 | $209.95 | N/A | 75 |
| 2025-07-07 20:09:18 | BUY | C | 5 | $87.61 | N/A | 85 |
| 2025-07-07 19:50:12 | SELL | NVDA | 2 | $158.18 | $3.42 | 70 |
| 2025-07-07 19:50:12 | SELL | CVX | 1 | $146.84 | $0.13 | 75 |
| 2025-07-07 19:50:12 | SELL | T | 1 | $28.36 | $-0.18 | 65 |
| 2025-07-07 19:50:12 | BUY | WMT | 2 | $99.08 | N/A | 75 |
| 2025-07-07 19:50:12 | BUY | NKE | 4 | $76.60 | N/A | 85 |
| 2025-07-07 19:50:12 | BUY | PFE | 4 | $25.22 | N/A | 70 |
| 2025-07-07 19:50:12 | BUY | WFC | 2 | $83.60 | N/A | 85 |
| 2025-07-07 19:50:12 | BUY | UNP | 1 | $235.25 | N/A | 85 |
| 2025-07-07 19:36:19 | SELL | PFE | 5 | $25.21 | $-0.42 | 65 |
| 2025-07-07 19:36:19 | SELL | T | 4 | $28.39 | $-0.59 | 65 |
| 2025-07-07 19:36:19 | BUY | NVDA | 2 | $158.40 | N/A | 85 |
| 2025-07-07 19:36:19 | BUY | NKE | 1 | $76.54 | N/A | 75 |
| 2025-07-07 19:36:19 | BUY | CVX | 1 | $146.75 | N/A | 85 |
| 2025-07-07 19:25:04 | SELL | AAPL | 1 | $209.43 | $-1.49 | 65 |
| 2025-07-07 19:25:04 | SELL | NKE | 1 | $76.50 | $0.64 | 70 |
| 2025-07-07 19:25:04 | SELL | C | 5 | $87.36 | $4.12 | 70 |
| 2025-07-07 19:25:04 | SELL | UNP | 1 | $234.88 | $-1.52 | 75 |
| 2025-07-07 19:25:04 | SELL | CSCO | 1 | $68.71 | $0.34 | 70 |

<!--TRADE_LOG_END--> 
