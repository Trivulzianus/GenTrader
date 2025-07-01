# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 14:48:51**

| Metric | Value |
|---|---|
| **Total Value** | **$100,628.18** |
| Cash | $26.11 |
| Holdings Value | $100,602.07 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.64 | $2,491.68 | 85 |
| ADBE | 5 | $385.76 | $388.56 | $1,942.80 | 75 |
| AMD | 16 | $141.95 | $136.76 | $2,188.23 | 75 |
| AMZN | 11 | $226.80 | $219.29 | $2,412.19 | 85 |
| AVGO | 9 | $275.08 | $266.79 | $2,401.11 | 85 |
| AXP | 6 | $315.94 | $318.03 | $1,908.18 | 65 |
| BA | 10 | $214.55 | $207.97 | $2,079.70 | 65 |
| BAC | 40 | $47.18 | $47.48 | $1,899.40 | 65 |
| C | 23 | $84.14 | $84.86 | $1,951.73 | 65 |
| CAT | 5 | $381.20 | $386.76 | $1,933.80 | 65 |
| COST | 2 | $991.47 | $992.39 | $1,984.79 | 65 |
| CRM | 9 | $274.67 | $272.35 | $2,451.15 | 85 |
| CSCO | 36 | $68.92 | $68.93 | $2,481.48 | 85 |
| CVX | 13 | $143.34 | $144.43 | $1,877.55 | 85 |
| DIS | 16 | $122.90 | $122.81 | $1,965.04 | 65 |
| GOOGL | 14 | $175.62 | $175.19 | $2,452.66 | 85 |
| GS | 3 | $706.65 | $703.36 | $2,110.07 | 65 |
| HD | 7 | $369.90 | $373.38 | $2,613.64 | 85 |
| INTC | 83 | $22.33 | $22.66 | $1,880.78 | 65 |
| JNJ | 12 | $151.53 | $156.48 | $1,877.76 | 65 |
| JPM | 7 | $285.02 | $287.86 | $2,015.02 | 65 |
| KO | 27 | $70.44 | $72.02 | $1,944.54 | 65 |
| LLY | 3 | $767.33 | $789.40 | $2,368.20 | 65 |
| MA | 4 | $537.87 | $562.75 | $2,251.00 | 65 |
| META | 3 | $712.71 | $727.23 | $2,181.68 | 90 |
| MRK | 30 | $79.35 | $81.03 | $2,430.90 | 85 |
| MSFT | 4 | $492.89 | $496.52 | $1,986.10 | 65 |
| NFLX | 1 | $1,334.07 | $1,314.08 | $1,314.08 | 85 |
| NKE | 33 | $71.01 | $73.62 | $2,429.46 | 85 |
| NVDA | 15 | $156.23 | $153.28 | $2,299.20 | 85 |
| ORCL | 9 | $219.56 | $217.71 | $1,959.39 | 65 |
| PEP | 17 | $131.85 | $135.16 | $2,297.72 | 75 |
| PFE | 99 | $24.30 | $24.87 | $2,462.01 | 85 |
| PG | 12 | $159.73 | $160.81 | $1,929.78 | 65 |
| PYPL | 33 | $73.91 | $74.46 | $2,457.18 | 85 |
| QCOM | 16 | $159.24 | $158.85 | $2,541.60 | 85 |
| T | 76 | $28.47 | $28.99 | $2,203.11 | 85 |
| TGT | 21 | $98.42 | $103.21 | $2,167.41 | 75 |
| TSLA | 7 | $294.26 | $299.18 | $2,094.26 | 65 |
| UNH | 8 | $306.63 | $323.26 | $2,586.08 | 85 |
| UNP | 11 | $232.22 | $233.55 | $2,569.05 | 85 |
| V | 6 | $344.95 | $353.56 | $2,121.39 | 85 |
| VZ | 50 | $42.73 | $43.56 | $2,178.00 | 75 |
| WFC | 31 | $79.89 | $80.30 | $2,489.14 | 85 |
| WMT | 25 | $97.07 | $99.10 | $2,477.50 | 85 |
| XOM | 18 | $109.40 | $108.03 | $1,944.54 | 65 |

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
| 2025-07-01 14:48:45 | SELL | JNJ | 1 | $156.44 | $4.53 | 65 |
| 2025-07-01 14:48:45 | SELL | INTC | 2 | $22.64 | $0.60 | 65 |
| 2025-07-01 14:48:45 | SELL | PYPL | 1 | $74.48 | $0.56 | 85 |
| 2025-07-01 14:48:45 | SELL | WMT | 1 | $99.08 | $1.93 | 85 |
| 2025-07-01 14:48:45 | SELL | PFE | 1 | $24.85 | $0.55 | 85 |
| 2025-07-01 14:48:45 | SELL | CSCO | 1 | $68.95 | $0.03 | 85 |
| 2025-07-01 14:48:45 | SELL | TGT | 1 | $103.21 | $4.57 | 75 |
| 2025-07-01 14:48:45 | BUY | NVDA | 2 | $153.41 | N/A | 85 |
| 2025-07-01 14:48:45 | BUY | MRK | 5 | $81.01 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
