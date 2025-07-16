# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 19:50:36**

| Metric | Value |
|---|---|
| **Total Value** | **$100,746.64** |
| Cash | $1,612.33 |
| Holdings Value | $99,134.31 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.46 | $2,104.55 | 65 |
| ADBE | 6 | $375.23 | $362.08 | $2,172.48 | 65 |
| AMD | 15 | $145.40 | $159.71 | $2,395.65 | 70 |
| AMZN | 10 | $221.65 | $223.10 | $2,231.00 | 70 |
| AVGO | 8 | $275.34 | $280.30 | $2,242.36 | 65 |
| AXP | 6 | $308.37 | $311.26 | $1,867.57 | 65 |
| BA | 9 | $210.81 | $229.25 | $2,063.25 | 70 |
| BAC | 49 | $46.24 | $45.94 | $2,250.82 | 70 |
| C | 30 | $86.85 | $90.00 | $2,700.00 | 85 |
| CAT | 6 | $397.74 | $412.94 | $2,477.64 | 85 |
| COST | 2 | $979.83 | $952.69 | $1,905.38 | 65 |
| CRM | 8 | $267.44 | $257.85 | $2,062.80 | 65 |
| CSCO | 31 | $68.46 | $67.42 | $2,089.87 | 65 |
| CVX | 16 | $146.83 | $150.30 | $2,404.80 | 75 |
| DIS | 18 | $122.77 | $119.72 | $2,154.96 | 65 |
| GOOGL | 13 | $179.34 | $183.13 | $2,380.69 | 70 |
| GS | 3 | $717.52 | $707.80 | $2,123.40 | 70 |
| HD | 5 | $353.54 | $357.14 | $1,785.70 | 65 |
| INTC | 85 | $22.35 | $22.66 | $1,926.52 | 60 |
| JNJ | 13 | $155.43 | $164.72 | $2,141.36 | 65 |
| JPM | 8 | $292.65 | $285.54 | $2,284.32 | 75 |
| KO | 30 | $70.97 | $69.22 | $2,076.60 | 65 |
| LLY | 3 | $781.32 | $789.69 | $2,369.07 | 65 |
| MA | 4 | $563.08 | $555.34 | $2,221.36 | 65 |
| META | 3 | $717.12 | $702.59 | $2,107.78 | 65 |
| MRK | 29 | $82.56 | $82.25 | $2,385.25 | 75 |
| MSFT | 5 | $498.84 | $506.06 | $2,530.28 | 85 |
| NFLX | 1 | $1,279.00 | $1,253.96 | $1,253.96 | 65 |
| NKE | 33 | $71.99 | $72.14 | $2,380.46 | 75 |
| NVDA | 14 | $171.52 | $171.29 | $2,398.13 | 70 |
| ORCL | 9 | $232.99 | $241.20 | $2,170.80 | 70 |
| PEP | 15 | $136.57 | $135.12 | $2,026.80 | 65 |
| PFE | 85 | $25.27 | $24.57 | $2,088.03 | 65 |
| PG | 13 | $152.06 | $153.45 | $1,994.85 | 65 |
| PYPL | 29 | $72.15 | $72.95 | $2,115.70 | 65 |
| QCOM | 14 | $153.83 | $154.11 | $2,157.54 | 65 |
| T | 77 | $27.10 | $26.96 | $2,076.30 | 65 |
| TGT | 20 | $104.94 | $101.40 | $2,028.00 | 65 |
| TSLA | 6 | $318.51 | $322.71 | $1,936.26 | 60 |
| UNH | 7 | $298.51 | $292.28 | $2,045.96 | 65 |
| UNP | 9 | $236.79 | $230.88 | $2,077.92 | 65 |
| V | 6 | $355.85 | $350.26 | $2,101.56 | 65 |
| VZ | 50 | $43.08 | $41.18 | $2,059.00 | 65 |
| WFC | 29 | $78.86 | $79.79 | $2,313.91 | 70 |
| WMT | 22 | $97.29 | $95.03 | $2,090.66 | 65 |
| XOM | 21 | $109.98 | $112.53 | $2,363.03 | 75 |

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
| 2025-07-16 19:50:23 | BUY | NKE | 4 | $71.99 | N/A | 75 |
| 2025-07-16 19:50:23 | BUY | PFE | 1 | $24.58 | N/A | 65 |
| 2025-07-16 19:50:23 | BUY | CVX | 1 | $150.40 | N/A | 75 |
| 2025-07-16 19:36:33 | SELL | JPM | 1 | $285.48 | $-6.38 | 70 |
| 2025-07-16 19:36:33 | SELL | INTC | 6 | $22.64 | $1.60 | 60 |
| 2025-07-16 19:36:33 | SELL | CVX | 1 | $150.55 | $3.71 | 70 |
| 2025-07-16 19:36:33 | SELL | T | 5 | $26.94 | $-0.71 | 65 |
| 2025-07-16 19:36:33 | BUY | WFC | 1 | $79.85 | N/A | 75 |
| 2025-07-16 19:24:51 | SELL | AMD | 2 | $155.61 | $18.02 | 70 |
| 2025-07-16 19:24:51 | SELL | PFE | 1 | $24.65 | $-0.63 | 65 |
| 2025-07-16 19:24:51 | SELL | WFC | 1 | $80.04 | $1.17 | 70 |
| 2025-07-16 19:24:51 | BUY | INTC | 6 | $22.55 | N/A | 65 |
| 2025-07-16 19:24:51 | BUY | XOM | 1 | $112.62 | N/A | 75 |
| 2025-07-16 19:24:51 | BUY | T | 5 | $26.99 | N/A | 70 |
| 2025-07-16 19:10:44 | SELL | BAC | 9 | $46.02 | $-1.67 | 70 |
| 2025-07-16 19:10:44 | SELL | PFE | 5 | $24.64 | $-2.99 | 65 |
| 2025-07-16 19:10:44 | SELL | UNP | 1 | $231.12 | $-5.09 | 65 |
| 2025-07-16 19:10:44 | SELL | CVX | 1 | $150.90 | $3.82 | 75 |
| 2025-07-16 19:10:44 | BUY | GOOGL | 1 | $183.61 | N/A | 75 |
| 2025-07-16 19:10:44 | BUY | AMD | 3 | $158.07 | N/A | 85 |
| 2025-07-16 18:59:06 | SELL | AMD | 1 | $157.43 | $12.40 | 65 |
| 2025-07-16 18:59:06 | SELL | INTC | 1 | $22.55 | $0.19 | 60 |
| 2025-07-16 18:59:06 | SELL | XOM | 1 | $112.81 | $2.82 | 70 |
| 2025-07-16 18:59:06 | SELL | NKE | 4 | $72.07 | $0.27 | 65 |
| 2025-07-16 18:59:06 | SELL | T | 5 | $27.00 | $-0.44 | 65 |

<!--TRADE_LOG_END--> 
