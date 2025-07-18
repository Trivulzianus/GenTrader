# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 17:40:56**

| Metric | Value |
|---|---|
| **Total Value** | **$101,101.78** |
| Cash | $745.14 |
| Holdings Value | $100,356.64 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.42 | $2,114.20 | 65 |
| ADBE | 6 | $375.23 | $366.33 | $2,197.98 | 65 |
| AMD | 14 | $159.84 | $157.81 | $2,209.34 | 70 |
| AMZN | 10 | $221.57 | $225.73 | $2,257.30 | 75 |
| AVGO | 8 | $275.34 | $283.40 | $2,267.20 | 70 |
| AXP | 7 | $309.18 | $306.93 | $2,148.47 | 65 |
| BA | 10 | $232.01 | $228.25 | $2,282.45 | 65 |
| BAC | 48 | $46.29 | $47.29 | $2,270.01 | 70 |
| C | 29 | $86.64 | $93.20 | $2,702.95 | 85 |
| CAT | 6 | $397.74 | $413.97 | $2,483.82 | 70 |
| COST | 2 | $979.83 | $952.14 | $1,904.28 | 65 |
| CRM | 8 | $267.44 | $260.57 | $2,084.56 | 65 |
| CSCO | 32 | $68.59 | $68.12 | $2,180.00 | 70 |
| CVX | 16 | $147.06 | $149.88 | $2,398.16 | 75 |
| DIS | 18 | $122.74 | $121.57 | $2,188.26 | 70 |
| GOOGL | 12 | $178.88 | $185.21 | $2,222.52 | 65 |
| GS | 3 | $717.52 | $708.10 | $2,124.28 | 75 |
| HD | 6 | $354.18 | $357.77 | $2,146.65 | 65 |
| INTC | 90 | $22.39 | $23.30 | $2,096.55 | 65 |
| JNJ | 14 | $155.98 | $164.38 | $2,301.28 | 70 |
| JPM | 8 | $292.14 | $291.35 | $2,330.76 | 70 |
| KO | 30 | $70.96 | $70.23 | $2,106.90 | 65 |
| LLY | 3 | $781.32 | $772.07 | $2,316.20 | 65 |
| MA | 4 | $563.08 | $552.88 | $2,211.52 | 65 |
| META | 3 | $717.12 | $699.81 | $2,099.43 | 70 |
| MRK | 26 | $82.73 | $80.23 | $2,085.98 | 65 |
| MSFT | 5 | $498.84 | $510.98 | $2,554.90 | 85 |
| NFLX | 1 | $1,208.39 | $1,213.41 | $1,213.41 | 65 |
| NKE | 29 | $71.98 | $72.65 | $2,106.85 | 65 |
| NVDA | 15 | $171.94 | $172.42 | $2,586.30 | 85 |
| ORCL | 9 | $232.91 | $247.22 | $2,224.98 | 70 |
| PEP | 15 | $135.89 | $143.63 | $2,154.45 | 65 |
| PFE | 85 | $25.27 | $24.45 | $2,078.25 | 65 |
| PG | 14 | $152.14 | $155.15 | $2,172.10 | 70 |
| PYPL | 32 | $72.36 | $74.05 | $2,369.60 | 75 |
| QCOM | 13 | $153.79 | $154.43 | $2,007.59 | 65 |
| T | 78 | $27.11 | $26.94 | $2,101.32 | 65 |
| TGT | 20 | $104.82 | $102.56 | $2,051.10 | 65 |
| TSLA | 6 | $318.51 | $327.57 | $1,965.44 | 65 |
| UNH | 8 | $283.36 | $281.88 | $2,255.00 | 75 |
| UNP | 9 | $225.02 | $224.00 | $2,015.95 | 65 |
| V | 6 | $355.85 | $348.91 | $2,093.46 | 65 |
| VZ | 51 | $40.87 | $40.81 | $2,081.57 | 65 |
| WFC | 29 | $78.84 | $80.51 | $2,334.79 | 75 |
| WMT | 22 | $97.29 | $95.01 | $2,090.22 | 65 |
| XOM | 20 | $109.90 | $108.41 | $2,168.29 | 65 |

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
| 2025-07-18 17:26:26 | BUY | PFE | 1 | $24.58 | N/A | 65 |
| 2025-07-18 17:26:26 | BUY | KO | 1 | $70.11 | N/A | 70 |
| 2025-07-18 17:26:26 | BUY | CVX | 1 | $149.60 | N/A | 80 |
| 2025-07-18 17:26:26 | BUY | VZ | 1 | $40.72 | N/A | 65 |
| 2025-07-18 17:11:45 | SELL | BAC | 3 | $47.31 | $2.89 | 70 |
| 2025-07-18 17:11:45 | SELL | INTC | 7 | $23.18 | $5.56 | 60 |
| 2025-07-18 17:11:45 | SELL | NKE | 2 | $72.63 | $1.22 | 65 |
| 2025-07-18 17:11:45 | SELL | WFC | 1 | $80.51 | $1.66 | 70 |
| 2025-07-18 17:11:45 | SELL | CSCO | 4 | $68.08 | $-1.86 | 65 |

<!--TRADE_LOG_END--> 
