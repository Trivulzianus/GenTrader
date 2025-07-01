# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 16:57:58**

| Metric | Value |
|---|---|
| **Total Value** | **$100,894.36** |
| Cash | $306.41 |
| Holdings Value | $100,587.95 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.21 | $2,486.52 | 85 |
| ADBE | 5 | $385.76 | $389.31 | $1,946.55 | 65 |
| AMD | 17 | $140.05 | $136.95 | $2,328.15 | 85 |
| AMZN | 11 | $226.78 | $219.78 | $2,417.58 | 85 |
| AVGO | 7 | $274.91 | $266.77 | $1,867.39 | 85 |
| AXP | 6 | $315.94 | $322.01 | $1,932.09 | 65 |
| BA | 9 | $215.30 | $209.30 | $1,883.72 | 65 |
| BAC | 51 | $47.30 | $47.95 | $2,445.70 | 85 |
| C | 22 | $84.08 | $85.58 | $1,882.65 | 65 |
| CAT | 5 | $381.20 | $390.62 | $1,953.12 | 65 |
| COST | 2 | $991.47 | $985.56 | $1,971.12 | 65 |
| CRM | 8 | $274.90 | $272.52 | $2,180.16 | 75 |
| CSCO | 35 | $68.88 | $68.92 | $2,412.03 | 85 |
| CVX | 17 | $143.81 | $144.76 | $2,460.92 | 85 |
| DIS | 20 | $122.93 | $123.03 | $2,460.60 | 85 |
| GOOGL | 14 | $175.62 | $174.94 | $2,449.09 | 85 |
| GS | 3 | $706.65 | $706.97 | $2,120.91 | 65 |
| HD | 7 | $369.90 | $375.12 | $2,625.81 | 85 |
| INTC | 83 | $22.23 | $22.82 | $1,894.47 | 65 |
| JNJ | 12 | $151.63 | $155.40 | $1,864.80 | 65 |
| JPM | 7 | $285.02 | $288.89 | $2,022.23 | 65 |
| KO | 26 | $70.42 | $71.61 | $1,861.86 | 65 |
| LLY | 3 | $767.33 | $778.71 | $2,336.13 | 65 |
| MA | 4 | $537.87 | $563.53 | $2,254.14 | 65 |
| META | 3 | $712.71 | $720.67 | $2,162.01 | 85 |
| MRK | 30 | $79.35 | $81.42 | $2,442.60 | 85 |
| MSFT | 4 | $492.89 | $493.51 | $1,974.04 | 65 |
| NFLX | 1 | $1,334.07 | $1,297.75 | $1,297.75 | 85 |
| NKE | 33 | $70.93 | $72.98 | $2,408.34 | 85 |
| NVDA | 12 | $153.68 | $154.56 | $1,854.74 | 65 |
| ORCL | 9 | $219.56 | $219.82 | $1,978.42 | 65 |
| PEP | 16 | $131.60 | $134.87 | $2,157.92 | 75 |
| PFE | 99 | $24.30 | $24.89 | $2,464.11 | 85 |
| PG | 12 | $159.73 | $160.81 | $1,929.78 | 65 |
| PYPL | 32 | $73.86 | $75.21 | $2,406.72 | 85 |
| QCOM | 15 | $159.12 | $159.72 | $2,395.80 | 85 |
| T | 85 | $28.52 | $28.82 | $2,450.12 | 85 |
| TGT | 21 | $98.42 | $103.77 | $2,179.17 | 75 |
| TSLA | 7 | $290.03 | $303.28 | $2,122.96 | 75 |
| UNH | 8 | $306.63 | $321.07 | $2,568.56 | 85 |
| UNP | 11 | $232.22 | $234.80 | $2,582.76 | 85 |
| V | 6 | $344.95 | $355.26 | $2,131.56 | 65 |
| VZ | 50 | $42.73 | $43.65 | $2,182.25 | 75 |
| WFC | 30 | $79.85 | $80.87 | $2,426.10 | 85 |
| WMT | 25 | $97.07 | $98.39 | $2,459.87 | 85 |
| XOM | 18 | $109.48 | $108.59 | $1,954.62 | 65 |

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
| 2025-07-01 16:57:52 | SELL | NVDA | 4 | $157.99 | $12.93 | 65 |
| 2025-07-01 16:57:52 | SELL | CRM | 1 | $272.54 | $-2.10 | 75 |
| 2025-07-01 16:57:52 | BUY | AMD | 3 | $137.14 | N/A | 85 |
| 2025-07-01 16:57:52 | BUY | DIS | 4 | $123.06 | N/A | 85 |
| 2025-07-01 16:48:11 | SELL | AMD | 3 | $141.90 | $3.02 | 65 |
| 2025-07-01 16:48:11 | SELL | XOM | 4 | $108.77 | $-2.32 | 65 |
| 2025-07-01 16:48:11 | SELL | INTC | 12 | $22.94 | $7.39 | 65 |
| 2025-07-01 16:48:11 | BUY | CRM | 1 | $273.07 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | PFE | 3 | $25.00 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | CSCO | 8 | $68.88 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | CVX | 1 | $145.12 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | VZ | 1 | $43.67 | N/A | 75 |
| 2025-07-01 16:48:11 | BUY | T | 1 | $28.78 | N/A | 85 |
| 2025-07-01 16:32:02 | SELL | JNJ | 1 | $156.45 | $4.44 | 65 |
| 2025-07-01 16:32:02 | SELL | PYPL | 1 | $75.43 | $1.52 | 85 |
| 2025-07-01 16:32:02 | SELL | NKE | 1 | $73.48 | $2.47 | 85 |
| 2025-07-01 16:32:02 | SELL | PFE | 1 | $25.17 | $0.89 | 85 |
| 2025-07-01 16:32:02 | SELL | KO | 3 | $71.72 | $3.51 | 65 |
| 2025-07-01 16:32:02 | SELL | WFC | 1 | $81.15 | $1.26 | 85 |
| 2025-07-01 16:32:02 | SELL | QCOM | 1 | $161.04 | $1.79 | 85 |
| 2025-07-01 16:32:02 | SELL | VZ | 1 | $43.66 | $0.93 | 75 |
| 2025-07-01 16:32:02 | SELL | T | 1 | $28.73 | $0.21 | 85 |
| 2025-07-01 16:32:02 | BUY | TSLA | 1 | $303.60 | N/A | 75 |
| 2025-07-01 16:32:02 | BUY | INTC | 14 | $22.40 | N/A | 75 |
| 2025-07-01 16:17:47 | SELL | AVGO | 2 | $275.65 | $1.15 | 65 |

<!--TRADE_LOG_END--> 
