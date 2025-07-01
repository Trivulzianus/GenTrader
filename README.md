# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 15:17:07**

| Metric | Value |
|---|---|
| **Total Value** | **$100,623.05** |
| Cash | $22.87 |
| Holdings Value | $100,600.19 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.58 | $2,502.96 | 85 |
| ADBE | 5 | $385.76 | $388.11 | $1,940.56 | 75 |
| AMD | 18 | $141.22 | $135.46 | $2,438.24 | 85 |
| AMZN | 11 | $226.80 | $218.13 | $2,399.43 | 85 |
| AVGO | 9 | $275.08 | $264.62 | $2,381.58 | 85 |
| AXP | 6 | $315.94 | $318.64 | $1,911.87 | 75 |
| BA | 10 | $214.55 | $207.41 | $2,074.12 | 65 |
| BAC | 40 | $47.18 | $47.59 | $1,903.80 | 65 |
| C | 23 | $84.14 | $84.89 | $1,952.47 | 65 |
| CAT | 5 | $381.20 | $389.78 | $1,948.90 | 65 |
| COST | 2 | $991.47 | $990.30 | $1,980.60 | 65 |
| CRM | 9 | $274.67 | $271.22 | $2,440.98 | 75 |
| CSCO | 28 | $68.90 | $68.83 | $1,927.38 | 65 |
| CVX | 14 | $143.46 | $145.09 | $2,031.26 | 75 |
| DIS | 16 | $122.90 | $122.58 | $1,961.28 | 65 |
| GOOGL | 14 | $175.62 | $173.72 | $2,432.02 | 85 |
| GS | 3 | $706.65 | $700.83 | $2,102.48 | 65 |
| HD | 7 | $369.90 | $377.06 | $2,639.42 | 85 |
| INTC | 84 | $22.33 | $22.66 | $1,903.86 | 65 |
| JNJ | 13 | $151.98 | $157.30 | $2,044.90 | 75 |
| JPM | 7 | $285.02 | $287.54 | $2,012.78 | 65 |
| KO | 26 | $70.37 | $72.38 | $1,882.00 | 65 |
| LLY | 3 | $767.33 | $784.45 | $2,353.35 | 65 |
| MA | 4 | $537.87 | $561.86 | $2,247.44 | 65 |
| META | 3 | $712.71 | $719.09 | $2,157.27 | 90 |
| MRK | 30 | $79.35 | $82.05 | $2,461.50 | 85 |
| MSFT | 4 | $492.89 | $492.01 | $1,968.04 | 65 |
| NFLX | 1 | $1,334.07 | $1,293.56 | $1,293.56 | 85 |
| NKE | 34 | $71.01 | $73.00 | $2,482.17 | 85 |
| NVDA | 16 | $156.03 | $151.74 | $2,427.76 | 85 |
| ORCL | 9 | $219.56 | $217.05 | $1,953.45 | 65 |
| PEP | 16 | $131.60 | $135.70 | $2,171.16 | 75 |
| PFE | 99 | $24.31 | $25.03 | $2,477.98 | 85 |
| PG | 12 | $159.73 | $162.27 | $1,947.24 | 65 |
| PYPL | 33 | $73.91 | $74.53 | $2,459.49 | 85 |
| QCOM | 16 | $159.24 | $158.34 | $2,533.44 | 85 |
| T | 85 | $28.52 | $29.02 | $2,466.28 | 85 |
| TGT | 21 | $98.42 | $103.92 | $2,182.31 | 75 |
| TSLA | 6 | $290.36 | $300.37 | $1,802.22 | 65 |
| UNH | 8 | $306.63 | $322.85 | $2,582.80 | 85 |
| UNP | 11 | $232.22 | $234.79 | $2,582.69 | 85 |
| V | 6 | $344.95 | $354.49 | $2,126.91 | 85 |
| VZ | 50 | $42.73 | $43.83 | $2,191.50 | 75 |
| WFC | 31 | $79.89 | $80.37 | $2,491.47 | 85 |
| WMT | 25 | $97.07 | $98.82 | $2,470.59 | 85 |
| XOM | 18 | $109.40 | $108.70 | $1,956.69 | 65 |

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
| 2025-07-01 15:16:59 | SELL | KO | 1 | $72.42 | $1.98 | 65 |
| 2025-07-01 15:16:59 | SELL | PEP | 1 | $135.79 | $3.93 | 75 |
| 2025-07-01 15:16:59 | BUY | JNJ | 1 | $157.42 | N/A | 75 |
| 2025-07-01 15:16:59 | BUY | AMD | 2 | $135.28 | N/A | 85 |
| 2025-07-01 15:16:59 | BUY | CVX | 1 | $145.10 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
