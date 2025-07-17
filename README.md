# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 13:30:07**

| Metric | Value |
|---|---|
| **Total Value** | **$100,863.95** |
| Cash | $903.33 |
| Holdings Value | $99,960.62 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.16 | $2,101.60 | 65 |
| ADBE | 6 | $375.23 | $361.77 | $2,170.62 | 65 |
| AMD | 14 | $160.08 | $161.81 | $2,265.34 | 70 |
| AMZN | 10 | $221.65 | $223.32 | $2,233.20 | 75 |
| AVGO | 8 | $275.34 | $281.13 | $2,249.04 | 70 |
| AXP | 6 | $308.37 | $311.90 | $1,871.40 | 65 |
| BA | 9 | $210.81 | $229.90 | $2,069.10 | 65 |
| BAC | 45 | $46.26 | $45.87 | $2,064.15 | 65 |
| C | 30 | $86.85 | $90.02 | $2,700.60 | 85 |
| CAT | 6 | $397.74 | $413.31 | $2,479.83 | 85 |
| COST | 2 | $979.83 | $951.28 | $1,902.57 | 65 |
| CRM | 8 | $267.44 | $257.95 | $2,063.60 | 65 |
| CSCO | 31 | $68.46 | $67.57 | $2,094.67 | 65 |
| CVX | 16 | $146.83 | $149.92 | $2,398.72 | 75 |
| DIS | 18 | $122.77 | $119.75 | $2,155.50 | 70 |
| GOOGL | 13 | $179.34 | $182.37 | $2,370.81 | 75 |
| GS | 3 | $717.52 | $708.82 | $2,126.46 | 85 |
| HD | 6 | $354.18 | $357.40 | $2,144.40 | 65 |
| INTC | 84 | $22.35 | $22.69 | $1,905.96 | 60 |
| JNJ | 13 | $155.43 | $164.78 | $2,142.14 | 70 |
| JPM | 9 | $291.90 | $285.82 | $2,572.38 | 85 |
| KO | 30 | $70.97 | $69.27 | $2,078.10 | 65 |
| LLY | 3 | $781.32 | $786.79 | $2,360.37 | 70 |
| MA | 4 | $563.08 | $555.52 | $2,222.08 | 65 |
| META | 3 | $717.12 | $702.91 | $2,108.73 | 75 |
| MRK | 29 | $82.56 | $82.43 | $2,390.47 | 75 |
| MSFT | 5 | $498.84 | $506.13 | $2,530.65 | 65 |
| NFLX | 1 | $1,279.00 | $1,250.31 | $1,250.31 | 65 |
| NKE | 33 | $71.99 | $72.10 | $2,379.30 | 75 |
| NVDA | 13 | $171.54 | $172.09 | $2,237.17 | 70 |
| ORCL | 9 | $232.99 | $242.45 | $2,182.05 | 65 |
| PEP | 16 | $136.49 | $141.96 | $2,271.36 | 65 |
| PFE | 84 | $25.28 | $24.61 | $2,067.24 | 65 |
| PG | 14 | $152.18 | $154.04 | $2,156.56 | 65 |
| PYPL | 28 | $72.12 | $72.64 | $2,034.06 | 65 |
| QCOM | 14 | $153.83 | $153.00 | $2,142.00 | 65 |
| T | 77 | $27.10 | $26.82 | $2,065.53 | 65 |
| TGT | 21 | $104.77 | $101.34 | $2,128.14 | 65 |
| TSLA | 6 | $318.51 | $323.11 | $1,938.66 | 65 |
| UNH | 7 | $298.51 | $291.23 | $2,038.61 | 65 |
| UNP | 10 | $236.22 | $231.18 | $2,311.80 | 75 |
| V | 6 | $355.85 | $349.90 | $2,099.40 | 65 |
| VZ | 50 | $43.08 | $41.12 | $2,055.75 | 65 |
| WFC | 30 | $78.89 | $79.91 | $2,397.30 | 75 |
| WMT | 22 | $97.29 | $95.03 | $2,090.77 | 65 |
| XOM | 21 | $109.98 | $111.53 | $2,342.13 | 75 |

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
| 2025-07-17 13:30:02 | SELL | INTC | 6 | $22.69 | $1.93 | 60 |
| 2025-07-17 13:30:02 | BUY | UNP | 1 | $231.18 | N/A | 75 |
| 2025-07-17 13:04:44 | SELL | BAC | 3 | $46.03 | $-0.64 | 65 |
| 2025-07-17 13:04:44 | SELL | UNP | 1 | $231.18 | $-5.04 | 65 |
| 2025-07-17 13:04:44 | BUY | INTC | 5 | $22.69 | N/A | 65 |
| 2025-07-17 13:04:44 | BUY | NKE | 4 | $72.10 | N/A | 75 |
| 2025-07-17 13:04:44 | BUY | VZ | 3 | $41.25 | N/A | 65 |
| 2025-07-17 13:04:44 | BUY | TGT | 1 | $101.34 | N/A | 70 |
| 2025-07-17 12:32:27 | SELL | VZ | 3 | $41.25 | $-5.49 | 60 |
| 2025-07-17 12:14:03 | SELL | T | 5 | $26.95 | $-0.69 | 65 |
| 2025-07-17 12:14:03 | BUY | BAC | 3 | $46.03 | N/A | 70 |
| 2025-07-17 11:50:40 | SELL | INTC | 1 | $22.69 | $0.34 | 60 |
| 2025-07-17 11:50:40 | SELL | BAC | 1 | $46.03 | $-0.22 | 65 |
| 2025-07-17 11:50:40 | BUY | VZ | 3 | $41.25 | N/A | 65 |
| 2025-07-17 11:50:40 | BUY | T | 5 | $26.95 | N/A | 70 |
| 2025-07-17 11:37:41 | SELL | BAC | 5 | $46.03 | $-1.00 | 65 |
| 2025-07-17 11:37:41 | SELL | INTC | 5 | $22.69 | $1.59 | 60 |
| 2025-07-17 11:37:41 | SELL | VZ | 3 | $41.25 | $-5.49 | 60 |
| 2025-07-17 11:37:41 | BUY | AMD | 1 | $160.08 | N/A | 70 |
| 2025-07-17 11:37:41 | BUY | KO | 1 | $69.27 | N/A | 65 |
| 2025-07-17 11:37:41 | BUY | AVGO | 1 | $280.81 | N/A | 70 |
| 2025-07-17 11:25:43 | SELL | T | 5 | $26.95 | $-0.69 | 65 |
| 2025-07-17 11:25:43 | BUY | INTC | 1 | $22.69 | N/A | 65 |
| 2025-07-17 11:25:43 | BUY | BAC | 6 | $46.03 | N/A | 75 |
| 2025-07-17 11:25:43 | BUY | XOM | 2 | $112.23 | N/A | 75 |

<!--TRADE_LOG_END--> 
