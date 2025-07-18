# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 17:26:35**

| Metric | Value |
|---|---|
| **Total Value** | **$100,996.75** |
| Cash | $1,333.66 |
| Holdings Value | $99,663.10 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.21 | $2,112.10 | 65 |
| ADBE | 6 | $375.23 | $365.54 | $2,193.24 | 65 |
| AMD | 14 | $159.84 | $157.62 | $2,206.68 | 70 |
| AMZN | 10 | $221.57 | $225.97 | $2,259.70 | 75 |
| AVGO | 8 | $275.34 | $283.31 | $2,266.48 | 70 |
| AXP | 7 | $309.18 | $307.08 | $2,149.56 | 65 |
| BA | 10 | $232.01 | $228.21 | $2,282.10 | 65 |
| BAC | 48 | $46.29 | $47.17 | $2,264.16 | 70 |
| C | 27 | $86.16 | $93.22 | $2,516.94 | 75 |
| CAT | 6 | $397.74 | $413.32 | $2,479.92 | 65 |
| COST | 2 | $979.83 | $951.31 | $1,902.62 | 65 |
| CRM | 8 | $267.44 | $260.40 | $2,083.20 | 65 |
| CSCO | 31 | $68.60 | $68.11 | $2,111.57 | 65 |
| CVX | 17 | $147.23 | $149.62 | $2,543.50 | 80 |
| DIS | 18 | $122.74 | $121.50 | $2,187.00 | 70 |
| GOOGL | 12 | $178.88 | $185.16 | $2,221.98 | 65 |
| GS | 3 | $717.52 | $707.90 | $2,123.70 | 75 |
| HD | 6 | $354.18 | $357.27 | $2,143.62 | 65 |
| INTC | 91 | $22.40 | $23.20 | $2,111.65 | 65 |
| JNJ | 14 | $155.98 | $164.09 | $2,297.26 | 70 |
| JPM | 8 | $292.14 | $291.35 | $2,330.80 | 70 |
| KO | 32 | $70.91 | $70.09 | $2,243.04 | 70 |
| LLY | 3 | $781.32 | $772.59 | $2,317.76 | 65 |
| MA | 4 | $563.08 | $552.69 | $2,210.76 | 65 |
| META | 3 | $717.12 | $700.38 | $2,101.14 | 70 |
| MRK | 26 | $82.73 | $80.18 | $2,084.68 | 65 |
| MSFT | 5 | $498.84 | $510.84 | $2,554.20 | 75 |
| NFLX | 1 | $1,208.39 | $1,212.12 | $1,212.12 | 65 |
| NKE | 29 | $71.98 | $72.64 | $2,106.56 | 65 |
| NVDA | 15 | $171.94 | $172.50 | $2,587.50 | 75 |
| ORCL | 9 | $232.91 | $246.50 | $2,218.50 | 65 |
| PEP | 15 | $135.89 | $143.14 | $2,147.12 | 65 |
| PFE | 86 | $25.26 | $24.43 | $2,101.40 | 65 |
| PG | 13 | $151.91 | $154.78 | $2,012.11 | 65 |
| PYPL | 29 | $72.18 | $74.02 | $2,146.58 | 65 |
| QCOM | 13 | $153.79 | $154.30 | $2,005.90 | 65 |
| T | 79 | $27.10 | $26.88 | $2,123.12 | 65 |
| TGT | 20 | $104.82 | $102.41 | $2,048.19 | 65 |
| TSLA | 6 | $318.51 | $326.91 | $1,961.46 | 65 |
| UNH | 7 | $283.57 | $281.53 | $1,970.71 | 65 |
| UNP | 9 | $225.02 | $223.66 | $2,012.94 | 65 |
| V | 6 | $355.85 | $348.47 | $2,090.82 | 65 |
| VZ | 52 | $40.87 | $40.72 | $2,117.18 | 65 |
| WFC | 28 | $78.78 | $80.39 | $2,250.78 | 70 |
| WMT | 22 | $97.29 | $94.92 | $2,088.35 | 65 |
| XOM | 20 | $109.90 | $108.12 | $2,162.40 | 65 |

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
| 2025-07-18 17:26:26 | SELL | JNJ | 1 | $164.11 | $7.59 | 70 |
| 2025-07-18 17:26:26 | SELL | C | 2 | $93.24 | $13.19 | 75 |
| 2025-07-18 17:26:26 | SELL | T | 4 | $26.88 | $-0.88 | 65 |
| 2025-07-18 17:26:26 | BUY | INTC | 8 | $23.20 | N/A | 65 |
| 2025-07-18 17:26:26 | BUY | PFE | 1 | $24.58 | N/A | 65 |
| 2025-07-18 17:26:26 | BUY | KO | 1 | $70.11 | N/A | 70 |
| 2025-07-18 17:26:26 | BUY | CVX | 1 | $149.60 | N/A | 80 |
| 2025-07-18 17:26:26 | BUY | VZ | 1 | $40.72 | N/A | 65 |
| 2025-07-18 17:11:45 | SELL | BAC | 3 | $47.31 | $2.89 | 70 |
| 2025-07-18 17:11:45 | SELL | INTC | 7 | $23.18 | $5.56 | 60 |
| 2025-07-18 17:11:45 | SELL | NKE | 2 | $72.63 | $1.22 | 65 |
| 2025-07-18 17:11:45 | SELL | WFC | 1 | $80.51 | $1.66 | 70 |
| 2025-07-18 17:11:45 | SELL | CSCO | 4 | $68.08 | $-1.86 | 65 |
| 2025-07-18 17:11:45 | SELL | QCOM | 1 | $154.28 | $0.45 | 60 |
| 2025-07-18 17:11:45 | BUY | JNJ | 1 | $164.32 | N/A | 80 |
| 2025-07-18 17:11:45 | BUY | KO | 1 | $70.18 | N/A | 70 |
| 2025-07-18 17:11:45 | BUY | T | 5 | $26.94 | N/A | 70 |
| 2025-07-18 16:58:19 | SELL | GOOGL | 1 | $184.97 | $5.63 | 65 |
| 2025-07-18 16:58:19 | SELL | WFC | 1 | $80.44 | $1.54 | 70 |
| 2025-07-18 16:58:19 | BUY | NVDA | 1 | $172.14 | N/A | 85 |
| 2025-07-18 16:58:19 | BUY | INTC | 6 | $23.21 | N/A | 65 |
| 2025-07-18 16:58:19 | BUY | CSCO | 2 | $68.24 | N/A | 75 |
| 2025-07-18 16:58:19 | BUY | CVX | 1 | $149.43 | N/A | 75 |
| 2025-07-18 16:44:31 | SELL | INTC | 6 | $23.25 | $5.17 | 60 |
| 2025-07-18 16:44:31 | SELL | KO | 2 | $70.26 | $-1.31 | 65 |

<!--TRADE_LOG_END--> 
