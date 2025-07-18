# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 18:45:31**

| Metric | Value |
|---|---|
| **Total Value** | **$101,017.84** |
| Cash | $1,443.59 |
| Holdings Value | $99,574.25 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.01 | $2,110.15 | 70 |
| ADBE | 6 | $375.23 | $365.93 | $2,195.58 | 65 |
| AMD | 14 | $159.84 | $157.54 | $2,205.56 | 70 |
| AMZN | 10 | $221.57 | $226.00 | $2,260.00 | 75 |
| AVGO | 8 | $275.34 | $283.74 | $2,269.92 | 70 |
| AXP | 7 | $309.18 | $307.38 | $2,151.62 | 65 |
| BA | 10 | $232.01 | $229.43 | $2,294.25 | 65 |
| BAC | 49 | $46.31 | $47.34 | $2,319.90 | 70 |
| C | 29 | $86.64 | $93.08 | $2,699.46 | 85 |
| CAT | 6 | $397.74 | $412.53 | $2,475.18 | 70 |
| COST | 2 | $979.83 | $951.91 | $1,903.82 | 65 |
| CRM | 8 | $267.44 | $261.15 | $2,089.20 | 65 |
| CSCO | 31 | $68.61 | $68.03 | $2,109.09 | 65 |
| CVX | 15 | $147.07 | $146.84 | $2,202.60 | 65 |
| DIS | 18 | $122.74 | $121.23 | $2,182.14 | 70 |
| GOOGL | 12 | $178.88 | $184.97 | $2,219.62 | 70 |
| GS | 3 | $717.52 | $708.16 | $2,124.48 | 70 |
| HD | 6 | $354.18 | $357.70 | $2,146.20 | 65 |
| INTC | 90 | $22.38 | $23.20 | $2,088.21 | 65 |
| JNJ | 14 | $155.98 | $163.48 | $2,288.72 | 70 |
| JPM | 8 | $292.14 | $291.53 | $2,332.24 | 75 |
| KO | 30 | $70.96 | $70.09 | $2,102.70 | 65 |
| LLY | 3 | $781.32 | $774.20 | $2,322.60 | 65 |
| MA | 4 | $563.08 | $551.99 | $2,207.96 | 65 |
| META | 3 | $717.12 | $701.64 | $2,104.92 | 65 |
| MRK | 26 | $82.73 | $80.08 | $2,082.08 | 65 |
| MSFT | 5 | $498.84 | $511.69 | $2,558.43 | 85 |
| NFLX | 1 | $1,208.39 | $1,210.35 | $1,210.35 | 65 |
| NKE | 29 | $71.98 | $72.61 | $2,105.57 | 65 |
| NVDA | 14 | $171.90 | $172.30 | $2,412.20 | 70 |
| ORCL | 9 | $232.91 | $246.54 | $2,218.87 | 70 |
| PEP | 15 | $135.89 | $143.55 | $2,153.25 | 70 |
| PFE | 86 | $25.26 | $24.42 | $2,100.49 | 65 |
| PG | 14 | $152.14 | $154.95 | $2,169.30 | 65 |
| PYPL | 29 | $72.21 | $73.98 | $2,145.57 | 65 |
| QCOM | 13 | $153.79 | $154.11 | $2,003.43 | 65 |
| T | 78 | $27.11 | $26.89 | $2,097.81 | 65 |
| TGT | 20 | $104.82 | $102.69 | $2,053.80 | 65 |
| TSLA | 6 | $318.51 | $330.05 | $1,980.30 | 65 |
| UNH | 8 | $283.36 | $283.28 | $2,266.21 | 65 |
| UNP | 9 | $225.02 | $223.83 | $2,014.49 | 65 |
| V | 6 | $355.85 | $349.20 | $2,095.20 | 65 |
| VZ | 51 | $40.87 | $40.76 | $2,078.61 | 65 |
| WFC | 27 | $78.72 | $80.41 | $2,170.93 | 65 |
| WMT | 22 | $97.29 | $95.22 | $2,094.84 | 65 |
| XOM | 20 | $109.90 | $107.82 | $2,156.40 | 65 |

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
| 2025-07-18 18:45:25 | SELL | BAC | 2 | $47.34 | $1.98 | 70 |
| 2025-07-18 18:45:25 | SELL | WFC | 1 | $80.39 | $1.62 | 65 |
| 2025-07-18 18:45:25 | SELL | CVX | 1 | $146.93 | $-0.13 | 65 |
| 2025-07-18 18:27:27 | BUY | BAC | 3 | $47.28 | N/A | 75 |
| 2025-07-18 18:27:27 | BUY | C | 2 | $93.11 | N/A | 85 |
| 2025-07-18 18:27:27 | BUY | WFC | 1 | $80.35 | N/A | 70 |
| 2025-07-18 18:10:57 | SELL | C | 2 | $93.21 | $13.13 | 75 |
| 2025-07-18 18:10:57 | SELL | CSCO | 4 | $68.07 | $-1.94 | 65 |
| 2025-07-18 18:10:57 | BUY | INTC | 5 | $23.18 | N/A | 65 |
| 2025-07-18 17:53:12 | SELL | NVDA | 1 | $172.46 | $0.53 | 70 |
| 2025-07-18 17:53:12 | SELL | INTC | 5 | $23.22 | $4.15 | 60 |
| 2025-07-18 17:53:12 | SELL | PYPL | 3 | $73.82 | $4.38 | 65 |
| 2025-07-18 17:53:12 | SELL | WFC | 2 | $80.47 | $3.26 | 65 |
| 2025-07-18 17:53:12 | BUY | PFE | 1 | $24.44 | N/A | 65 |
| 2025-07-18 17:53:12 | BUY | CSCO | 3 | $68.14 | N/A | 75 |
| 2025-07-18 17:40:48 | SELL | KO | 2 | $70.23 | $-1.37 | 65 |
| 2025-07-18 17:40:48 | SELL | PFE | 1 | $24.44 | $-0.82 | 65 |
| 2025-07-18 17:40:48 | SELL | CVX | 1 | $149.87 | $2.64 | 75 |
| 2025-07-18 17:40:48 | SELL | INTC | 1 | $23.29 | $0.90 | 65 |
| 2025-07-18 17:40:48 | SELL | T | 1 | $26.93 | $-0.17 | 65 |
| 2025-07-18 17:40:48 | SELL | VZ | 1 | $40.81 | $-0.05 | 65 |
| 2025-07-18 17:40:48 | BUY | UNH | 1 | $281.89 | N/A | 75 |
| 2025-07-18 17:40:48 | BUY | PYPL | 3 | $74.08 | N/A | 75 |
| 2025-07-18 17:40:48 | BUY | WFC | 1 | $80.50 | N/A | 75 |
| 2025-07-18 17:40:48 | BUY | PG | 1 | $155.14 | N/A | 70 |

<!--TRADE_LOG_END--> 
