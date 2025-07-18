# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 18:11:03**

| Metric | Value |
|---|---|
| **Total Value** | **$101,041.68** |
| Cash | $1,530.02 |
| Holdings Value | $99,511.66 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.91 | $2,109.05 | 65 |
| ADBE | 6 | $375.23 | $365.92 | $2,195.52 | 65 |
| AMD | 14 | $159.84 | $157.34 | $2,202.69 | 70 |
| AMZN | 10 | $221.57 | $225.81 | $2,258.10 | 75 |
| AVGO | 8 | $275.34 | $283.50 | $2,268.00 | 70 |
| AXP | 7 | $309.18 | $307.99 | $2,155.93 | 65 |
| BA | 10 | $232.01 | $229.02 | $2,290.20 | 65 |
| BAC | 48 | $46.29 | $47.33 | $2,271.98 | 70 |
| C | 27 | $86.16 | $93.20 | $2,516.40 | 75 |
| CAT | 6 | $397.74 | $412.93 | $2,477.58 | 70 |
| COST | 2 | $979.83 | $951.76 | $1,903.53 | 65 |
| CRM | 8 | $267.44 | $261.04 | $2,088.32 | 65 |
| CSCO | 31 | $68.61 | $68.06 | $2,110.01 | 65 |
| CVX | 16 | $147.06 | $149.43 | $2,390.88 | 75 |
| DIS | 18 | $122.74 | $121.48 | $2,186.64 | 70 |
| GOOGL | 12 | $178.88 | $184.84 | $2,218.08 | 70 |
| GS | 3 | $717.52 | $708.24 | $2,124.72 | 85 |
| HD | 6 | $354.18 | $357.72 | $2,146.32 | 65 |
| INTC | 90 | $22.38 | $23.17 | $2,085.30 | 65 |
| JNJ | 14 | $155.98 | $163.95 | $2,295.30 | 70 |
| JPM | 8 | $292.14 | $291.61 | $2,332.84 | 70 |
| KO | 30 | $70.96 | $70.17 | $2,105.25 | 65 |
| LLY | 3 | $781.32 | $773.29 | $2,319.87 | 65 |
| MA | 4 | $563.08 | $551.93 | $2,207.72 | 65 |
| META | 3 | $717.12 | $699.53 | $2,098.59 | 70 |
| MRK | 26 | $82.73 | $80.11 | $2,082.86 | 65 |
| MSFT | 5 | $498.84 | $510.86 | $2,554.28 | 85 |
| NFLX | 1 | $1,208.39 | $1,214.50 | $1,214.50 | 65 |
| NKE | 29 | $71.98 | $72.54 | $2,103.66 | 65 |
| NVDA | 14 | $171.90 | $172.19 | $2,410.73 | 70 |
| ORCL | 9 | $232.91 | $246.96 | $2,222.64 | 70 |
| PEP | 15 | $135.89 | $143.08 | $2,146.20 | 65 |
| PFE | 86 | $25.26 | $24.43 | $2,101.41 | 65 |
| PG | 14 | $152.14 | $154.92 | $2,168.88 | 65 |
| PYPL | 29 | $72.21 | $73.84 | $2,141.51 | 65 |
| QCOM | 13 | $153.79 | $154.14 | $2,003.82 | 65 |
| T | 78 | $27.11 | $26.93 | $2,100.17 | 65 |
| TGT | 20 | $104.82 | $102.70 | $2,054.00 | 65 |
| TSLA | 6 | $318.51 | $330.61 | $1,983.66 | 65 |
| UNH | 8 | $283.36 | $282.08 | $2,256.64 | 65 |
| UNP | 9 | $225.02 | $222.98 | $2,006.82 | 65 |
| V | 6 | $355.85 | $348.61 | $2,091.66 | 65 |
| VZ | 51 | $40.87 | $40.77 | $2,079.27 | 65 |
| WFC | 27 | $78.72 | $80.47 | $2,172.82 | 65 |
| WMT | 22 | $97.29 | $95.13 | $2,092.81 | 65 |
| XOM | 20 | $109.90 | $108.22 | $2,164.50 | 70 |

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
| 2025-07-18 17:40:48 | BUY | C | 2 | $93.21 | N/A | 85 |
| 2025-07-18 17:40:48 | BUY | CSCO | 1 | $68.12 | N/A | 70 |
| 2025-07-18 17:26:26 | SELL | JNJ | 1 | $164.11 | $7.59 | 70 |
| 2025-07-18 17:26:26 | SELL | C | 2 | $93.24 | $13.19 | 75 |
| 2025-07-18 17:26:26 | SELL | T | 4 | $26.88 | $-0.88 | 65 |
| 2025-07-18 17:26:26 | BUY | INTC | 8 | $23.20 | N/A | 65 |

<!--TRADE_LOG_END--> 
