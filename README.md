# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 14:40:20**

| Metric | Value |
|---|---|
| **Total Value** | **$100,605.94** |
| Cash | $165.70 |
| Holdings Value | $100,440.23 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.48 | $2,501.76 | 85 |
| ADBE | 5 | $385.76 | $388.15 | $1,940.75 | 75 |
| AMD | 16 | $141.95 | $136.26 | $2,180.16 | 75 |
| AMZN | 11 | $226.80 | $219.49 | $2,414.39 | 85 |
| AVGO | 9 | $275.08 | $266.19 | $2,395.66 | 85 |
| AXP | 6 | $315.94 | $318.74 | $1,912.44 | 65 |
| BA | 10 | $214.55 | $208.50 | $2,085.00 | 65 |
| BAC | 40 | $47.18 | $47.57 | $1,902.80 | 65 |
| C | 23 | $84.14 | $84.95 | $1,953.96 | 65 |
| CAT | 5 | $381.20 | $387.08 | $1,935.40 | 65 |
| COST | 2 | $991.47 | $989.61 | $1,979.21 | 65 |
| CRM | 9 | $274.67 | $272.47 | $2,452.23 | 75 |
| CSCO | 37 | $68.92 | $68.88 | $2,548.56 | 85 |
| CVX | 13 | $143.34 | $143.97 | $1,871.67 | 85 |
| DIS | 16 | $122.90 | $123.24 | $1,971.84 | 65 |
| GOOGL | 14 | $175.62 | $174.76 | $2,446.64 | 85 |
| GS | 3 | $706.65 | $706.34 | $2,119.01 | 65 |
| HD | 7 | $369.90 | $372.51 | $2,607.56 | 85 |
| INTC | 85 | $22.34 | $22.54 | $1,915.47 | 65 |
| JNJ | 13 | $151.91 | $156.28 | $2,031.64 | 65 |
| JPM | 7 | $285.02 | $289.05 | $2,023.35 | 65 |
| KO | 27 | $70.44 | $71.92 | $1,941.84 | 65 |
| LLY | 3 | $767.33 | $788.99 | $2,366.97 | 65 |
| MA | 4 | $537.87 | $561.74 | $2,246.94 | 65 |
| META | 3 | $712.71 | $727.49 | $2,182.47 | 85 |
| MRK | 25 | $79.01 | $80.76 | $2,019.00 | 85 |
| MSFT | 4 | $492.89 | $496.34 | $1,985.36 | 65 |
| NFLX | 1 | $1,334.07 | $1,315.70 | $1,315.70 | 85 |
| NKE | 33 | $71.01 | $73.61 | $2,428.97 | 85 |
| NVDA | 13 | $156.66 | $153.78 | $1,999.14 | 65 |
| ORCL | 9 | $219.56 | $217.21 | $1,954.89 | 65 |
| PEP | 17 | $131.85 | $134.91 | $2,293.47 | 75 |
| PFE | 100 | $24.31 | $24.81 | $2,480.64 | 85 |
| PG | 12 | $159.73 | $161.00 | $1,932.00 | 65 |
| PYPL | 34 | $73.92 | $74.64 | $2,537.76 | 85 |
| QCOM | 16 | $159.24 | $158.40 | $2,534.32 | 85 |
| T | 76 | $28.47 | $28.98 | $2,202.86 | 75 |
| TGT | 22 | $98.63 | $102.91 | $2,264.10 | 75 |
| TSLA | 7 | $294.26 | $301.37 | $2,109.58 | 75 |
| UNH | 8 | $306.63 | $322.58 | $2,580.64 | 85 |
| UNP | 11 | $232.22 | $233.14 | $2,564.54 | 85 |
| V | 6 | $344.95 | $353.47 | $2,120.82 | 75 |
| VZ | 50 | $42.73 | $43.53 | $2,176.50 | 75 |
| WFC | 31 | $79.89 | $80.58 | $2,497.98 | 85 |
| WMT | 26 | $97.15 | $98.99 | $2,573.74 | 85 |
| XOM | 18 | $109.40 | $107.81 | $1,940.49 | 65 |

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
| 2025-07-01 14:40:14 | SELL | NVDA | 3 | $157.99 | $3.24 | 65 |
| 2025-07-01 14:40:14 | SELL | JNJ | 1 | $156.26 | $4.04 | 65 |
| 2025-07-01 14:40:14 | SELL | BAC | 1 | $47.57 | $0.37 | 65 |
| 2025-07-01 14:40:14 | SELL | INTC | 3 | $22.52 | $0.55 | 65 |
| 2025-07-01 14:40:14 | SELL | AXP | 1 | $318.68 | $2.35 | 65 |
| 2025-07-01 14:40:14 | SELL | WFC | 1 | $80.59 | $0.68 | 85 |
| 2025-07-01 14:40:14 | SELL | TGT | 1 | $102.93 | $4.11 | 75 |
| 2025-07-01 14:40:14 | SELL | T | 12 | $28.99 | $5.35 | 75 |
| 2025-07-01 14:40:14 | BUY | AMZN | 2 | $219.61 | N/A | 85 |
| 2025-07-01 14:40:14 | BUY | AMD | 2 | $136.27 | N/A | 75 |
| 2025-07-01 14:40:14 | BUY | NKE | 6 | $73.67 | N/A | 85 |
| 2025-07-01 14:40:14 | BUY | PFE | 7 | $24.82 | N/A | 85 |
| 2025-07-01 14:40:14 | BUY | VZ | 5 | $43.54 | N/A | 75 |
| 2025-07-01 14:29:22 | SELL | AMD | 1 | $141.90 | $-0.80 | 65 |
| 2025-07-01 14:29:22 | SELL | NKE | 8 | $73.59 | $19.60 | 65 |
| 2025-07-01 14:29:22 | SELL | MRK | 7 | $79.16 | $0.81 | 65 |
| 2025-07-01 14:29:22 | BUY | NVDA | 3 | $154.47 | N/A | 85 |
| 2025-07-01 14:29:22 | BUY | JNJ | 1 | $155.55 | N/A | 75 |
| 2025-07-01 14:29:22 | BUY | PFE | 1 | $24.24 | N/A | 75 |
| 2025-07-01 14:29:22 | BUY | CSCO | 8 | $68.89 | N/A | 85 |
| 2025-07-01 14:16:46 | SELL | AMZN | 2 | $219.39 | $-14.74 | 65 |
| 2025-07-01 14:16:46 | SELL | AMD | 2 | $138.58 | $-7.27 | 65 |
| 2025-07-01 14:16:46 | SELL | CSCO | 3 | $69.19 | $0.71 | 65 |
| 2025-07-01 14:16:46 | SELL | T | 1 | $28.94 | $0.40 | 85 |
| 2025-07-01 14:16:46 | BUY | GOOGL | 14 | $175.62 | N/A | 85 |

<!--TRADE_LOG_END--> 
