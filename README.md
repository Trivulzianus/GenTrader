# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 17:11:54**

| Metric | Value |
|---|---|
| **Total Value** | **$101,004.81** |
| Cash | $1,346.17 |
| Holdings Value | $99,658.64 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.18 | $2,111.80 | 70 |
| ADBE | 6 | $375.23 | $365.67 | $2,194.02 | 70 |
| AMD | 14 | $159.84 | $157.27 | $2,201.78 | 65 |
| AMZN | 10 | $221.57 | $225.68 | $2,256.80 | 75 |
| AVGO | 8 | $275.34 | $282.82 | $2,262.56 | 70 |
| AXP | 7 | $309.18 | $306.72 | $2,147.06 | 65 |
| BA | 10 | $232.01 | $228.09 | $2,280.90 | 65 |
| BAC | 48 | $46.29 | $47.31 | $2,270.88 | 70 |
| C | 29 | $86.64 | $93.48 | $2,711.07 | 85 |
| CAT | 6 | $397.74 | $414.15 | $2,484.90 | 70 |
| COST | 2 | $979.83 | $952.42 | $1,904.85 | 65 |
| CRM | 8 | $267.44 | $259.85 | $2,078.80 | 65 |
| CSCO | 31 | $68.60 | $68.10 | $2,111.02 | 65 |
| CVX | 16 | $147.08 | $149.78 | $2,396.48 | 75 |
| DIS | 18 | $122.74 | $121.39 | $2,185.02 | 70 |
| GOOGL | 12 | $178.88 | $184.98 | $2,219.76 | 70 |
| GS | 3 | $717.52 | $707.62 | $2,122.86 | 70 |
| HD | 6 | $354.18 | $357.61 | $2,145.64 | 65 |
| INTC | 83 | $22.32 | $23.18 | $1,924.35 | 60 |
| JNJ | 15 | $156.52 | $164.33 | $2,464.95 | 80 |
| JPM | 8 | $292.14 | $291.62 | $2,332.92 | 70 |
| KO | 31 | $70.94 | $70.18 | $2,175.58 | 70 |
| LLY | 3 | $781.32 | $771.00 | $2,313.00 | 65 |
| MA | 4 | $563.08 | $552.34 | $2,209.37 | 65 |
| META | 3 | $717.12 | $698.43 | $2,095.29 | 70 |
| MRK | 26 | $82.73 | $80.35 | $2,089.10 | 65 |
| MSFT | 5 | $498.84 | $510.23 | $2,551.14 | 85 |
| NFLX | 1 | $1,208.39 | $1,207.34 | $1,207.34 | 65 |
| NKE | 29 | $71.98 | $72.67 | $2,107.43 | 65 |
| NVDA | 15 | $171.94 | $172.08 | $2,581.22 | 85 |
| ORCL | 9 | $232.91 | $245.85 | $2,212.63 | 65 |
| PEP | 15 | $135.89 | $143.59 | $2,153.78 | 70 |
| PFE | 85 | $25.27 | $24.50 | $2,082.50 | 65 |
| PG | 13 | $151.91 | $155.09 | $2,016.23 | 65 |
| PYPL | 29 | $72.18 | $74.03 | $2,147.01 | 65 |
| QCOM | 13 | $153.79 | $154.29 | $2,005.77 | 60 |
| T | 83 | $27.09 | $26.94 | $2,236.02 | 70 |
| TGT | 20 | $104.82 | $102.57 | $2,051.35 | 65 |
| TSLA | 6 | $318.51 | $325.12 | $1,950.75 | 65 |
| UNH | 7 | $283.57 | $281.40 | $1,969.80 | 70 |
| UNP | 9 | $225.02 | $223.88 | $2,014.92 | 65 |
| V | 6 | $355.85 | $348.25 | $2,089.47 | 65 |
| VZ | 51 | $40.87 | $40.82 | $2,081.65 | 65 |
| WFC | 28 | $78.78 | $80.49 | $2,253.72 | 70 |
| WMT | 22 | $97.29 | $95.02 | $2,090.33 | 65 |
| XOM | 20 | $109.90 | $108.24 | $2,164.80 | 70 |

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
| 2025-07-18 16:44:31 | SELL | CVX | 2 | $148.85 | $3.40 | 65 |
| 2025-07-18 16:44:31 | BUY | PFE | 5 | $24.48 | N/A | 65 |
| 2025-07-18 16:44:31 | BUY | WFC | 2 | $80.48 | N/A | 75 |
| 2025-07-18 16:44:31 | BUY | NKE | 2 | $72.54 | N/A | 70 |
| 2025-07-18 16:27:10 | SELL | NVDA | 1 | $172.01 | $0.08 | 70 |
| 2025-07-18 16:27:10 | SELL | PFE | 5 | $24.42 | $-4.21 | 60 |
| 2025-07-18 16:27:10 | BUY | KO | 2 | $70.18 | N/A | 70 |
| 2025-07-18 16:27:10 | BUY | INTC | 7 | $23.18 | N/A | 65 |

<!--TRADE_LOG_END--> 
