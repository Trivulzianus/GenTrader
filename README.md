# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 18:17:55**

| Metric | Value |
|---|---|
| **Total Value** | **$101,098.48** |
| Cash | $103.40 |
| Holdings Value | $100,995.08 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.09 | $2,497.08 | 85 |
| ADBE | 5 | $385.76 | $390.68 | $1,953.38 | 75 |
| AMD | 18 | $139.86 | $137.34 | $2,472.12 | 85 |
| AMZN | 10 | $227.67 | $220.90 | $2,209.00 | 85 |
| AVGO | 9 | $272.95 | $265.25 | $2,387.20 | 85 |
| AXP | 6 | $315.94 | $323.04 | $1,938.24 | 65 |
| BA | 9 | $215.30 | $210.36 | $1,893.24 | 65 |
| BAC | 51 | $47.30 | $48.20 | $2,457.95 | 85 |
| C | 22 | $84.06 | $86.21 | $1,896.62 | 65 |
| CAT | 5 | $381.20 | $392.05 | $1,960.24 | 65 |
| COST | 2 | $991.47 | $984.42 | $1,968.85 | 65 |
| CRM | 8 | $274.93 | $273.28 | $2,186.24 | 85 |
| CSCO | 27 | $68.84 | $69.09 | $1,865.43 | 65 |
| CVX | 17 | $143.81 | $145.51 | $2,473.75 | 85 |
| DIS | 16 | $122.87 | $123.30 | $1,972.80 | 65 |
| GOOGL | 14 | $175.62 | $175.72 | $2,460.14 | 85 |
| GS | 3 | $706.65 | $705.72 | $2,117.16 | 65 |
| HD | 7 | $369.90 | $374.68 | $2,622.77 | 85 |
| INTC | 81 | $22.22 | $22.98 | $1,861.78 | 65 |
| JNJ | 12 | $151.63 | $155.58 | $1,866.96 | 65 |
| JPM | 7 | $285.02 | $289.15 | $2,024.05 | 65 |
| KO | 26 | $70.42 | $71.71 | $1,864.46 | 65 |
| LLY | 3 | $767.33 | $773.53 | $2,320.59 | 65 |
| MA | 4 | $537.87 | $564.93 | $2,259.74 | 75 |
| META | 3 | $712.71 | $720.55 | $2,161.65 | 85 |
| MRK | 30 | $79.35 | $81.92 | $2,457.45 | 85 |
| MSFT | 4 | $492.89 | $492.50 | $1,970.00 | 85 |
| NFLX | 1 | $1,334.07 | $1,298.31 | $1,298.31 | 85 |
| NKE | 33 | $70.94 | $72.89 | $2,405.53 | 85 |
| NVDA | 16 | $153.32 | $154.70 | $2,475.20 | 85 |
| ORCL | 9 | $219.56 | $218.43 | $1,965.87 | 65 |
| PEP | 16 | $131.60 | $135.09 | $2,161.44 | 75 |
| PFE | 96 | $24.28 | $25.05 | $2,405.28 | 85 |
| PG | 12 | $159.73 | $161.16 | $1,933.92 | 65 |
| PYPL | 32 | $73.86 | $75.50 | $2,415.84 | 85 |
| QCOM | 15 | $159.12 | $160.54 | $2,408.10 | 85 |
| T | 85 | $28.52 | $28.81 | $2,448.65 | 85 |
| TGT | 21 | $98.42 | $103.88 | $2,181.48 | 85 |
| TSLA | 7 | $287.46 | $300.62 | $2,104.34 | 75 |
| UNH | 8 | $306.63 | $323.07 | $2,584.56 | 85 |
| UNP | 11 | $232.22 | $234.96 | $2,584.56 | 85 |
| V | 6 | $344.95 | $356.27 | $2,137.64 | 65 |
| VZ | 50 | $42.73 | $43.67 | $2,183.50 | 75 |
| WFC | 30 | $79.85 | $81.09 | $2,432.85 | 85 |
| WMT | 25 | $97.07 | $98.25 | $2,456.12 | 85 |
| XOM | 21 | $109.38 | $109.19 | $2,292.99 | 85 |

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
| 2025-07-01 18:17:48 | SELL | INTC | 1 | $22.99 | $0.76 | 65 |
| 2025-07-01 18:17:48 | SELL | C | 3 | $86.22 | $5.70 | 65 |
| 2025-07-01 18:17:48 | SELL | T | 1 | $28.81 | $0.28 | 85 |
| 2025-07-01 18:17:48 | BUY | AMZN | 1 | $220.89 | N/A | 85 |
| 2025-07-01 18:17:48 | BUY | NKE | 6 | $72.90 | N/A | 85 |
| 2025-07-01 18:17:48 | BUY | PFE | 8 | $25.05 | N/A | 85 |
| 2025-07-01 18:04:57 | SELL | AMZN | 2 | $219.39 | $-14.77 | 65 |
| 2025-07-01 18:04:57 | SELL | CRM | 1 | $273.68 | $-1.11 | 75 |
| 2025-07-01 18:04:57 | SELL | XOM | 1 | $109.05 | $-0.31 | 75 |
| 2025-07-01 18:04:57 | SELL | PFE | 10 | $25.00 | $7.12 | 75 |
| 2025-07-01 18:04:57 | SELL | NKE | 6 | $72.87 | $11.63 | 65 |
| 2025-07-01 18:04:57 | BUY | NVDA | 4 | $154.66 | N/A | 85 |
| 2025-07-01 18:04:57 | BUY | TSLA | 1 | $299.66 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | AMD | 1 | $137.18 | N/A | 85 |
| 2025-07-01 18:04:57 | BUY | C | 3 | $86.44 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | VZ | 1 | $43.69 | N/A | 75 |
| 2025-07-01 18:04:57 | BUY | T | 1 | $28.82 | N/A | 85 |
| 2025-07-01 17:56:28 | SELL | NVDA | 3 | $157.99 | $12.29 | 65 |
| 2025-07-01 17:56:28 | SELL | TSLA | 1 | $317.66 | $27.63 | 65 |
| 2025-07-01 17:56:28 | SELL | C | 2 | $86.39 | $4.32 | 65 |
| 2025-07-01 17:56:28 | BUY | CRM | 1 | $273.90 | N/A | 85 |
| 2025-07-01 17:56:28 | BUY | INTC | 1 | $22.98 | N/A | 65 |
| 2025-07-01 17:56:28 | BUY | XOM | 2 | $109.14 | N/A | 85 |
| 2025-07-01 17:49:44 | SELL | TGT | 2 | $104.10 | $10.37 | 75 |
| 2025-07-01 17:49:44 | BUY | C | 2 | $86.38 | N/A | 75 |

<!--TRADE_LOG_END--> 
