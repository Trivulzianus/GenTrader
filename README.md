# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 06:11:54**

| Metric | Value |
|---|---|
| **Total Value** | **$100,778.09** |
| Cash | $2,210.68 |
| Holdings Value | $98,567.41 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.16 | $2,101.60 | 65 |
| ADBE | 6 | $375.23 | $361.77 | $2,170.62 | 65 |
| AMD | 13 | $160.08 | $160.08 | $2,081.04 | 70 |
| AMZN | 10 | $221.65 | $223.19 | $2,231.90 | 75 |
| AVGO | 7 | $274.56 | $280.81 | $1,965.67 | 70 |
| AXP | 6 | $308.37 | $311.90 | $1,871.40 | 65 |
| BA | 10 | $212.72 | $229.90 | $2,299.00 | 70 |
| BAC | 45 | $46.26 | $46.03 | $2,071.35 | 65 |
| C | 30 | $86.85 | $90.02 | $2,700.60 | 85 |
| CAT | 6 | $397.74 | $412.88 | $2,477.28 | 85 |
| COST | 2 | $979.83 | $951.37 | $1,902.74 | 65 |
| CRM | 8 | $267.44 | $257.95 | $2,063.60 | 65 |
| CSCO | 31 | $68.46 | $67.37 | $2,088.47 | 65 |
| CVX | 16 | $146.83 | $149.92 | $2,398.72 | 75 |
| DIS | 18 | $122.77 | $119.82 | $2,156.76 | 70 |
| GOOGL | 13 | $179.34 | $182.97 | $2,378.61 | 75 |
| GS | 3 | $717.52 | $708.82 | $2,126.46 | 75 |
| HD | 5 | $353.54 | $357.40 | $1,787.00 | 65 |
| INTC | 84 | $22.35 | $22.69 | $1,905.96 | 60 |
| JNJ | 13 | $155.43 | $164.78 | $2,142.14 | 70 |
| JPM | 9 | $291.90 | $285.82 | $2,572.38 | 75 |
| KO | 30 | $70.97 | $69.27 | $2,078.10 | 65 |
| LLY | 3 | $781.32 | $789.80 | $2,369.40 | 85 |
| MA | 4 | $563.08 | $555.52 | $2,222.08 | 65 |
| META | 3 | $717.12 | $702.91 | $2,108.73 | 70 |
| MRK | 29 | $82.56 | $82.43 | $2,390.47 | 75 |
| MSFT | 5 | $498.84 | $505.62 | $2,528.10 | 70 |
| NFLX | 1 | $1,279.00 | $1,250.31 | $1,250.31 | 65 |
| NKE | 29 | $71.97 | $72.10 | $2,090.90 | 65 |
| NVDA | 13 | $171.54 | $171.37 | $2,227.81 | 70 |
| ORCL | 9 | $232.99 | $241.30 | $2,171.70 | 65 |
| PEP | 15 | $136.57 | $135.35 | $2,030.25 | 65 |
| PFE | 78 | $25.33 | $24.61 | $1,919.58 | 60 |
| PG | 14 | $152.18 | $153.73 | $2,152.22 | 65 |
| PYPL | 29 | $72.15 | $72.97 | $2,116.13 | 65 |
| QCOM | 14 | $153.83 | $154.07 | $2,156.98 | 70 |
| T | 76 | $27.10 | $26.95 | $2,048.20 | 65 |
| TGT | 20 | $104.94 | $101.34 | $2,026.80 | 65 |
| TSLA | 6 | $318.51 | $321.67 | $1,930.02 | 65 |
| UNH | 7 | $298.51 | $292.49 | $2,047.43 | 65 |
| UNP | 10 | $236.22 | $231.18 | $2,311.80 | 75 |
| V | 6 | $355.85 | $349.90 | $2,099.40 | 70 |
| VZ | 50 | $43.08 | $41.25 | $2,062.50 | 65 |
| WFC | 30 | $78.89 | $79.91 | $2,397.30 | 75 |
| WMT | 22 | $97.29 | $95.15 | $2,093.30 | 65 |
| XOM | 20 | $109.87 | $112.23 | $2,244.60 | 70 |

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
| 2025-07-17 06:11:50 | SELL | NVDA | 2 | $171.37 | $-0.29 | 70 |
| 2025-07-17 06:11:50 | SELL | PFE | 6 | $24.61 | $-4.02 | 60 |
| 2025-07-17 05:54:34 | SELL | XOM | 1 | $112.23 | $2.25 | 70 |
| 2025-07-17 05:54:34 | SELL | WMT | 1 | $95.15 | $-2.05 | 65 |
| 2025-07-17 05:54:34 | BUY | NVDA | 2 | $171.37 | N/A | 85 |
| 2025-07-17 05:43:42 | SELL | NVDA | 1 | $171.37 | $-0.15 | 70 |
| 2025-07-17 05:43:42 | SELL | BAC | 3 | $46.03 | $-0.64 | 65 |
| 2025-07-17 05:43:42 | SELL | INTC | 1 | $22.69 | $0.34 | 60 |
| 2025-07-17 05:43:42 | SELL | T | 1 | $26.95 | $-0.15 | 65 |
| 2025-07-17 05:43:42 | BUY | JPM | 1 | $285.82 | N/A | 85 |
| 2025-07-17 05:43:42 | BUY | XOM | 1 | $112.23 | N/A | 75 |
| 2025-07-17 05:43:42 | BUY | WMT | 1 | $95.15 | N/A | 70 |
| 2025-07-17 05:43:42 | BUY | PG | 1 | $153.73 | N/A | 70 |
| 2025-07-17 05:27:53 | SELL | NVDA | 1 | $171.37 | $-0.14 | 70 |
| 2025-07-17 05:27:53 | SELL | INTC | 5 | $22.69 | $1.61 | 60 |
| 2025-07-17 05:27:53 | SELL | XOM | 1 | $112.23 | $2.25 | 70 |
| 2025-07-17 05:27:53 | BUY | BA | 1 | $229.90 | N/A | 75 |
| 2025-07-17 05:27:53 | BUY | BAC | 3 | $46.03 | N/A | 70 |
| 2025-07-17 05:12:02 | SELL | AVGO | 1 | $280.81 | $5.47 | 60 |
| 2025-07-17 05:12:02 | BUY | INTC | 6 | $22.69 | N/A | 65 |
| 2025-07-17 05:12:02 | BUY | XOM | 2 | $112.23 | N/A | 75 |
| 2025-07-17 04:49:31 | SELL | XOM | 2 | $112.23 | $4.49 | 65 |
| 2025-07-17 04:49:31 | BUY | NVDA | 2 | $171.37 | N/A | 85 |
| 2025-07-17 04:29:16 | SELL | NVDA | 2 | $171.37 | $-0.29 | 70 |
| 2025-07-17 04:29:16 | SELL | WMT | 1 | $95.15 | $-2.05 | 65 |

<!--TRADE_LOG_END--> 
