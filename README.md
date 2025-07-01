# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 15:04:13**

| Metric | Value |
|---|---|
| **Total Value** | **$100,706.81** |
| Cash | $387.74 |
| Holdings Value | $100,319.07 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $209.98 | $2,519.76 | 85 |
| ADBE | 5 | $385.76 | $387.81 | $1,939.03 | 75 |
| AMD | 16 | $141.96 | $136.53 | $2,184.56 | 75 |
| AMZN | 11 | $226.80 | $218.99 | $2,408.89 | 85 |
| AVGO | 9 | $275.08 | $266.40 | $2,397.64 | 85 |
| AXP | 6 | $315.94 | $319.35 | $1,916.10 | 65 |
| BA | 10 | $214.55 | $208.39 | $2,083.90 | 65 |
| BAC | 40 | $47.18 | $47.59 | $1,903.40 | 65 |
| C | 23 | $84.14 | $85.08 | $1,956.95 | 65 |
| CAT | 5 | $381.20 | $389.10 | $1,945.50 | 65 |
| COST | 2 | $991.47 | $990.45 | $1,980.89 | 65 |
| CRM | 9 | $274.67 | $271.90 | $2,447.14 | 75 |
| CSCO | 28 | $68.90 | $69.04 | $1,933.12 | 65 |
| CVX | 13 | $143.34 | $144.69 | $1,880.97 | 85 |
| DIS | 16 | $122.90 | $122.88 | $1,966.08 | 65 |
| GOOGL | 14 | $175.62 | $174.35 | $2,440.90 | 85 |
| GS | 3 | $706.65 | $705.52 | $2,116.56 | 75 |
| HD | 7 | $369.90 | $374.30 | $2,620.07 | 85 |
| INTC | 84 | $22.33 | $22.73 | $1,909.32 | 65 |
| JNJ | 12 | $151.53 | $156.56 | $1,878.72 | 65 |
| JPM | 7 | $285.02 | $288.63 | $2,020.44 | 65 |
| KO | 27 | $70.44 | $72.06 | $1,945.49 | 65 |
| LLY | 3 | $767.33 | $784.48 | $2,353.44 | 65 |
| MA | 4 | $537.87 | $563.24 | $2,252.96 | 65 |
| META | 3 | $712.71 | $724.57 | $2,173.71 | 90 |
| MRK | 30 | $79.35 | $81.25 | $2,437.50 | 85 |
| MSFT | 4 | $492.89 | $494.21 | $1,976.84 | 65 |
| NFLX | 1 | $1,334.07 | $1,305.36 | $1,305.36 | 85 |
| NKE | 34 | $71.01 | $73.28 | $2,491.52 | 85 |
| NVDA | 16 | $156.03 | $153.39 | $2,454.24 | 85 |
| ORCL | 9 | $219.56 | $218.66 | $1,967.94 | 65 |
| PEP | 17 | $131.85 | $135.16 | $2,297.76 | 75 |
| PFE | 99 | $24.31 | $24.86 | $2,461.63 | 85 |
| PG | 12 | $159.73 | $161.35 | $1,936.20 | 65 |
| PYPL | 33 | $73.91 | $74.73 | $2,466.09 | 85 |
| QCOM | 16 | $159.24 | $158.94 | $2,543.04 | 85 |
| T | 85 | $28.52 | $28.96 | $2,462.03 | 85 |
| TGT | 21 | $98.42 | $103.62 | $2,176.02 | 75 |
| TSLA | 6 | $290.36 | $300.86 | $1,805.17 | 65 |
| UNH | 8 | $306.63 | $320.76 | $2,566.12 | 85 |
| UNP | 11 | $232.22 | $233.89 | $2,572.79 | 85 |
| V | 6 | $344.95 | $354.35 | $2,126.07 | 85 |
| VZ | 50 | $42.73 | $43.55 | $2,177.75 | 75 |
| WFC | 31 | $79.89 | $80.55 | $2,496.89 | 85 |
| WMT | 25 | $97.07 | $98.93 | $2,473.25 | 85 |
| XOM | 18 | $109.40 | $108.30 | $1,949.31 | 65 |

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
| 2025-07-01 15:04:07 | SELL | AMD | 2 | $136.43 | $-9.83 | 75 |
| 2025-07-01 15:04:07 | SELL | CSCO | 4 | $69.05 | $0.54 | 65 |
| 2025-07-01 15:04:07 | BUY | NKE | 1 | $71.04 | N/A | 85 |
| 2025-07-01 15:04:07 | BUY | PFE | 10 | $24.85 | N/A | 85 |
| 2025-07-01 14:55:20 | SELL | TSLA | 1 | $317.66 | $23.40 | 65 |
| 2025-07-01 14:55:20 | SELL | PFE | 10 | $24.80 | $4.99 | 75 |
| 2025-07-01 14:55:20 | SELL | CSCO | 4 | $68.99 | $0.27 | 75 |
| 2025-07-01 14:55:20 | BUY | NVDA | 1 | $152.99 | N/A | 85 |
| 2025-07-01 14:55:20 | BUY | INTC | 1 | $22.64 | N/A | 65 |
| 2025-07-01 14:55:20 | BUY | AMD | 2 | $136.55 | N/A | 85 |
| 2025-07-01 14:55:20 | BUY | T | 9 | $28.98 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
