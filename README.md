# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 18:27:32**

| Metric | Value |
|---|---|
| **Total Value** | **$101,039.77** |
| Cash | $1,121.59 |
| Holdings Value | $99,918.18 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.91 | $2,109.05 | 65 |
| ADBE | 6 | $375.23 | $366.15 | $2,196.93 | 65 |
| AMD | 14 | $159.84 | $157.73 | $2,208.27 | 65 |
| AMZN | 10 | $221.57 | $225.85 | $2,258.50 | 75 |
| AVGO | 8 | $275.34 | $283.55 | $2,268.36 | 70 |
| AXP | 7 | $309.18 | $307.32 | $2,151.24 | 65 |
| BA | 10 | $232.01 | $229.03 | $2,290.32 | 65 |
| BAC | 51 | $46.35 | $47.29 | $2,411.79 | 75 |
| C | 29 | $86.64 | $93.11 | $2,700.34 | 85 |
| CAT | 6 | $397.74 | $412.57 | $2,475.42 | 70 |
| COST | 2 | $979.83 | $951.57 | $1,903.14 | 65 |
| CRM | 8 | $267.44 | $261.38 | $2,091.05 | 65 |
| CSCO | 31 | $68.61 | $67.98 | $2,107.38 | 65 |
| CVX | 16 | $147.06 | $148.53 | $2,376.48 | 75 |
| DIS | 18 | $122.74 | $121.43 | $2,185.74 | 70 |
| GOOGL | 12 | $178.88 | $184.97 | $2,219.64 | 70 |
| GS | 3 | $717.52 | $707.44 | $2,122.32 | 70 |
| HD | 6 | $354.18 | $357.68 | $2,146.08 | 65 |
| INTC | 90 | $22.38 | $23.25 | $2,092.05 | 65 |
| JNJ | 14 | $155.98 | $163.79 | $2,293.06 | 70 |
| JPM | 8 | $292.14 | $291.50 | $2,332.04 | 75 |
| KO | 30 | $70.96 | $70.17 | $2,104.95 | 65 |
| LLY | 3 | $781.32 | $773.76 | $2,321.29 | 65 |
| MA | 4 | $563.08 | $552.03 | $2,208.14 | 65 |
| META | 3 | $717.12 | $700.56 | $2,101.68 | 70 |
| MRK | 26 | $82.73 | $80.16 | $2,084.03 | 65 |
| MSFT | 5 | $498.84 | $511.44 | $2,557.18 | 85 |
| NFLX | 1 | $1,208.39 | $1,215.00 | $1,215.00 | 65 |
| NKE | 29 | $71.98 | $72.59 | $2,105.26 | 65 |
| NVDA | 14 | $171.90 | $172.34 | $2,412.69 | 70 |
| ORCL | 9 | $232.91 | $246.66 | $2,219.94 | 70 |
| PEP | 15 | $135.89 | $143.48 | $2,152.16 | 65 |
| PFE | 86 | $25.26 | $24.43 | $2,101.41 | 65 |
| PG | 14 | $152.14 | $155.02 | $2,170.28 | 65 |
| PYPL | 29 | $72.21 | $73.95 | $2,144.55 | 65 |
| QCOM | 13 | $153.79 | $154.21 | $2,004.67 | 65 |
| T | 78 | $27.11 | $26.91 | $2,098.59 | 65 |
| TGT | 20 | $104.82 | $102.73 | $2,054.70 | 65 |
| TSLA | 6 | $318.51 | $329.50 | $1,977.00 | 65 |
| UNH | 8 | $283.36 | $283.12 | $2,264.96 | 65 |
| UNP | 9 | $225.02 | $223.69 | $2,013.21 | 65 |
| V | 6 | $355.85 | $348.87 | $2,093.22 | 70 |
| VZ | 51 | $40.87 | $40.77 | $2,079.53 | 65 |
| WFC | 28 | $78.78 | $80.35 | $2,249.80 | 70 |
| WMT | 22 | $97.29 | $95.13 | $2,092.86 | 65 |
| XOM | 20 | $109.90 | $107.59 | $2,151.90 | 65 |

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
| 2025-07-18 17:40:48 | BUY | C | 2 | $93.21 | N/A | 85 |
| 2025-07-18 17:40:48 | BUY | CSCO | 1 | $68.12 | N/A | 70 |
| 2025-07-18 17:26:26 | SELL | JNJ | 1 | $164.11 | $7.59 | 70 |

<!--TRADE_LOG_END--> 
