# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 21:45:39**

| Metric | Value |
|---|---|
| **Total Value** | **$101,079.66** |
| Cash | $686.82 |
| Holdings Value | $100,392.84 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $207.82 | $2,493.84 | 85 |
| ADBE | 5 | $385.76 | $392.10 | $1,960.50 | 75 |
| AMD | 16 | $138.96 | $136.11 | $2,177.76 | 75 |
| AMZN | 11 | $227.14 | $220.46 | $2,425.06 | 85 |
| AVGO | 9 | $272.95 | $264.74 | $2,382.66 | 85 |
| AXP | 6 | $315.94 | $322.53 | $1,935.18 | 65 |
| BA | 9 | $215.30 | $209.79 | $1,888.11 | 65 |
| BAC | 50 | $47.28 | $48.15 | $2,407.50 | 85 |
| C | 24 | $84.24 | $86.27 | $2,070.48 | 75 |
| CAT | 5 | $381.20 | $390.92 | $1,954.60 | 65 |
| COST | 2 | $991.47 | $985.96 | $1,971.92 | 65 |
| CRM | 7 | $275.36 | $271.91 | $1,903.37 | 75 |
| CSCO | 27 | $68.84 | $69.10 | $1,865.70 | 65 |
| CVX | 16 | $143.71 | $145.57 | $2,329.12 | 85 |
| DIS | 16 | $122.87 | $123.49 | $1,975.84 | 65 |
| GOOGL | 14 | $175.62 | $175.84 | $2,461.76 | 85 |
| GS | 3 | $706.65 | $706.46 | $2,119.38 | 75 |
| HD | 7 | $369.90 | $373.16 | $2,612.12 | 85 |
| INTC | 82 | $22.23 | $22.85 | $1,873.70 | 65 |
| JNJ | 12 | $151.64 | $155.92 | $1,871.04 | 65 |
| JPM | 7 | $285.02 | $290.41 | $2,032.87 | 65 |
| KO | 26 | $70.43 | $71.67 | $1,863.42 | 65 |
| LLY | 3 | $767.33 | $775.90 | $2,327.70 | 75 |
| MA | 4 | $537.87 | $564.61 | $2,258.44 | 65 |
| META | 3 | $712.71 | $719.22 | $2,157.66 | 90 |
| MRK | 30 | $79.35 | $81.81 | $2,454.30 | 85 |
| MSFT | 4 | $492.89 | $492.05 | $1,968.20 | 85 |
| NFLX | 1 | $1,334.07 | $1,293.60 | $1,293.60 | 85 |
| NKE | 26 | $70.33 | $73.41 | $1,908.66 | 65 |
| NVDA | 16 | $153.32 | $153.30 | $2,452.80 | 85 |
| ORCL | 9 | $219.56 | $218.96 | $1,970.64 | 65 |
| PEP | 16 | $131.60 | $135.26 | $2,164.16 | 75 |
| PFE | 97 | $24.29 | $25.04 | $2,428.88 | 85 |
| PG | 12 | $159.73 | $161.22 | $1,934.64 | 65 |
| PYPL | 32 | $73.86 | $75.29 | $2,409.28 | 85 |
| QCOM | 15 | $159.12 | $159.40 | $2,391.00 | 85 |
| T | 84 | $28.52 | $28.88 | $2,425.92 | 85 |
| TGT | 23 | $98.93 | $103.85 | $2,388.55 | 85 |
| TSLA | 7 | $287.46 | $300.71 | $2,104.97 | 75 |
| UNH | 8 | $306.63 | $326.14 | $2,609.12 | 85 |
| UNP | 11 | $232.22 | $235.57 | $2,591.27 | 85 |
| V | 6 | $344.95 | $355.47 | $2,132.82 | 65 |
| VZ | 49 | $42.72 | $43.68 | $2,140.32 | 75 |
| WFC | 30 | $79.85 | $81.49 | $2,444.70 | 85 |
| WMT | 25 | $97.07 | $98.24 | $2,456.00 | 85 |
| XOM | 22 | $109.37 | $109.24 | $2,403.28 | 85 |

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
| 2025-07-01 21:45:33 | SELL | AMD | 1 | $136.11 | $-2.68 | 75 |
| 2025-07-01 21:45:33 | SELL | NKE | 7 | $73.41 | $16.97 | 65 |
| 2025-07-01 21:37:12 | BUY | AMD | 1 | $136.11 | N/A | 85 |
| 2025-07-01 21:37:12 | BUY | XOM | 2 | $109.24 | N/A | 85 |
| 2025-07-01 21:28:26 | SELL | AMD | 1 | $136.11 | $-2.68 | 75 |
| 2025-07-01 21:28:26 | SELL | INTC | 5 | $22.85 | $2.93 | 65 |
| 2025-07-01 21:28:26 | BUY | NKE | 3 | $73.41 | N/A | 85 |
| 2025-07-01 21:16:50 | SELL | XOM | 2 | $109.24 | $-0.26 | 75 |
| 2025-07-01 21:16:50 | BUY | INTC | 5 | $22.85 | N/A | 70 |
| 2025-07-01 21:16:50 | BUY | C | 2 | $86.27 | N/A | 75 |
| 2025-07-01 21:16:50 | BUY | T | 9 | $28.88 | N/A | 85 |
| 2025-07-01 21:03:48 | SELL | C | 3 | $86.27 | $5.85 | 65 |
| 2025-07-01 21:03:48 | SELL | T | 9 | $28.88 | $3.21 | 75 |
| 2025-07-01 20:55:20 | SELL | NKE | 3 | $73.41 | $7.27 | 75 |
| 2025-07-01 20:55:20 | BUY | AMD | 1 | $136.11 | N/A | 85 |
| 2025-07-01 20:48:31 | SELL | AMD | 1 | $136.11 | $-2.68 | 75 |
| 2025-07-01 20:48:31 | SELL | KO | 1 | $71.67 | $1.19 | 65 |
| 2025-07-01 20:48:31 | SELL | DIS | 3 | $123.49 | $1.56 | 65 |
| 2025-07-01 20:48:31 | BUY | XOM | 2 | $109.24 | N/A | 85 |
| 2025-07-01 20:48:31 | BUY | NKE | 4 | $73.41 | N/A | 85 |
| 2025-07-01 20:40:29 | SELL | KO | 3 | $71.67 | $3.21 | 65 |
| 2025-07-01 20:40:29 | SELL | C | 3 | $86.27 | $5.22 | 75 |
| 2025-07-01 20:40:29 | BUY | DIS | 4 | $123.49 | N/A | 85 |
| 2025-07-01 20:40:29 | BUY | TGT | 2 | $103.85 | N/A | 85 |
| 2025-07-01 20:30:35 | SELL | XOM | 2 | $109.24 | $-0.26 | 75 |

<!--TRADE_LOG_END--> 
