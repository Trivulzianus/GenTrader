# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 16:11:04**

| Metric | Value |
|---|---|
| **Total Value** | **$101,132.38** |
| Cash | $1,233.13 |
| Holdings Value | $99,899.25 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.98 | $2,109.80 | 65 |
| ADBE | 6 | $375.23 | $365.27 | $2,191.62 | 65 |
| AMD | 14 | $159.84 | $158.96 | $2,225.44 | 70 |
| AMZN | 10 | $221.57 | $225.04 | $2,250.40 | 70 |
| AVGO | 8 | $275.34 | $283.75 | $2,270.00 | 70 |
| AXP | 7 | $309.18 | $307.27 | $2,150.89 | 65 |
| BA | 10 | $232.01 | $229.02 | $2,290.20 | 65 |
| BAC | 51 | $46.35 | $47.21 | $2,407.71 | 75 |
| C | 29 | $86.64 | $93.53 | $2,712.37 | 85 |
| CAT | 6 | $397.74 | $415.23 | $2,491.35 | 85 |
| COST | 2 | $979.83 | $954.30 | $1,908.60 | 65 |
| CRM | 8 | $267.44 | $260.29 | $2,082.34 | 65 |
| CSCO | 33 | $68.56 | $68.26 | $2,252.58 | 70 |
| CVX | 17 | $147.15 | $149.98 | $2,549.66 | 80 |
| DIS | 18 | $122.74 | $121.25 | $2,182.59 | 70 |
| GOOGL | 13 | $179.34 | $185.17 | $2,407.21 | 70 |
| GS | 3 | $717.52 | $709.84 | $2,129.52 | 85 |
| HD | 6 | $354.18 | $357.97 | $2,147.82 | 65 |
| INTC | 83 | $22.32 | $23.32 | $1,935.97 | 60 |
| JNJ | 14 | $155.97 | $164.18 | $2,298.45 | 70 |
| JPM | 8 | $292.14 | $291.86 | $2,334.84 | 70 |
| KO | 30 | $70.97 | $70.27 | $2,107.95 | 65 |
| LLY | 3 | $781.32 | $771.23 | $2,313.68 | 65 |
| MA | 4 | $563.08 | $552.57 | $2,210.28 | 65 |
| META | 3 | $717.12 | $699.85 | $2,099.55 | 70 |
| MRK | 26 | $82.73 | $80.56 | $2,094.56 | 65 |
| MSFT | 5 | $498.84 | $508.97 | $2,544.85 | 85 |
| NFLX | 1 | $1,208.39 | $1,214.49 | $1,214.49 | 65 |
| NKE | 29 | $71.98 | $72.50 | $2,102.64 | 65 |
| NVDA | 15 | $171.93 | $172.46 | $2,586.83 | 85 |
| ORCL | 9 | $232.91 | $246.83 | $2,221.48 | 70 |
| PEP | 15 | $135.89 | $143.96 | $2,159.41 | 65 |
| PFE | 85 | $25.27 | $24.46 | $2,079.53 | 65 |
| PG | 13 | $151.91 | $154.94 | $2,014.25 | 65 |
| PYPL | 29 | $72.18 | $73.91 | $2,143.24 | 65 |
| QCOM | 14 | $153.83 | $154.51 | $2,163.14 | 65 |
| T | 78 | $27.10 | $26.97 | $2,103.64 | 65 |
| TGT | 20 | $104.82 | $102.48 | $2,049.60 | 65 |
| TSLA | 6 | $318.51 | $327.67 | $1,966.02 | 65 |
| UNH | 7 | $283.57 | $283.00 | $1,981.01 | 65 |
| UNP | 9 | $225.02 | $223.83 | $2,014.47 | 65 |
| V | 6 | $355.85 | $348.20 | $2,089.20 | 65 |
| VZ | 48 | $40.87 | $40.84 | $1,960.56 | 60 |
| WFC | 26 | $78.66 | $80.27 | $2,086.89 | 65 |
| WMT | 22 | $97.29 | $95.06 | $2,091.32 | 65 |
| XOM | 20 | $109.90 | $108.56 | $2,171.30 | 65 |

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
| 2025-07-18 16:10:58 | SELL | AMZN | 1 | $225.05 | $3.16 | 70 |
| 2025-07-18 16:10:58 | SELL | NKE | 2 | $72.50 | $0.98 | 65 |
| 2025-07-18 16:10:58 | SELL | WFC | 1 | $80.27 | $1.55 | 65 |
| 2025-07-18 16:10:58 | SELL | VZ | 3 | $40.84 | $-0.08 | 60 |
| 2025-07-18 15:53:05 | SELL | INTC | 7 | $23.44 | $7.19 | 60 |
| 2025-07-18 15:53:05 | SELL | CVX | 1 | $150.71 | $3.36 | 75 |
| 2025-07-18 15:53:05 | BUY | NVDA | 2 | $172.51 | N/A | 85 |
| 2025-07-18 15:53:05 | BUY | UNH | 7 | $283.57 | N/A | 65 |
| 2025-07-18 15:53:05 | BUY | NKE | 2 | $72.36 | N/A | 70 |
| 2025-07-18 15:53:05 | BUY | CSCO | 2 | $68.33 | N/A | 70 |
| 2025-07-18 15:52:44 | SELL | UNH | 7 | $283.57 | $-104.53 | 65 |
| 2025-07-18 15:39:48 | SELL | NKE | 1 | $72.44 | $0.43 | 65 |
| 2025-07-18 15:39:48 | SELL | T | 5 | $26.97 | $-0.65 | 65 |
| 2025-07-18 15:39:48 | SELL | CSCO | 2 | $68.29 | $-0.55 | 65 |
| 2025-07-18 15:39:48 | BUY | BAC | 6 | $47.12 | N/A | 75 |
| 2025-07-18 15:39:48 | BUY | CVX | 1 | $150.86 | N/A | 85 |
| 2025-07-18 15:26:20 | SELL | BAC | 3 | $47.08 | $2.33 | 65 |
| 2025-07-18 15:26:20 | SELL | NKE | 3 | $72.32 | $0.86 | 65 |
| 2025-07-18 15:26:20 | SELL | KO | 4 | $70.38 | $-2.08 | 65 |
| 2025-07-18 15:26:20 | BUY | T | 5 | $26.98 | N/A | 70 |
| 2025-07-18 15:08:54 | SELL | WFC | 1 | $80.03 | $1.26 | 65 |
| 2025-07-18 15:08:54 | SELL | CVX | 1 | $150.64 | $3.31 | 75 |
| 2025-07-18 15:08:54 | BUY | BAC | 1 | $47.13 | N/A | 70 |
| 2025-07-18 15:08:54 | BUY | INTC | 1 | $23.39 | N/A | 65 |
| 2025-07-18 15:08:54 | BUY | KO | 4 | $70.37 | N/A | 75 |

<!--TRADE_LOG_END--> 
