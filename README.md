# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 20:09:22**

| Metric | Value |
|---|---|
| **Total Value** | **$100,764.16** |
| Cash | $2,241.55 |
| Holdings Value | $98,522.61 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.16 | $2,101.60 | 65 |
| ADBE | 6 | $375.23 | $361.77 | $2,170.62 | 65 |
| AMD | 13 | $160.08 | $160.08 | $2,081.04 | 70 |
| AMZN | 10 | $221.65 | $223.19 | $2,231.90 | 75 |
| AVGO | 8 | $275.34 | $280.81 | $2,246.48 | 70 |
| AXP | 6 | $308.37 | $311.84 | $1,871.03 | 65 |
| BA | 9 | $210.81 | $229.74 | $2,067.66 | 70 |
| BAC | 49 | $46.24 | $46.00 | $2,254.00 | 70 |
| C | 30 | $86.85 | $90.02 | $2,700.60 | 85 |
| CAT | 6 | $397.74 | $412.86 | $2,477.16 | 70 |
| COST | 2 | $979.83 | $951.37 | $1,902.74 | 65 |
| CRM | 8 | $267.44 | $257.89 | $2,063.12 | 65 |
| CSCO | 31 | $68.46 | $67.37 | $2,088.47 | 65 |
| CVX | 16 | $146.83 | $149.92 | $2,398.72 | 75 |
| DIS | 18 | $122.77 | $119.81 | $2,156.58 | 65 |
| GOOGL | 13 | $179.34 | $182.97 | $2,378.61 | 75 |
| GS | 3 | $717.52 | $708.28 | $2,124.83 | 70 |
| HD | 5 | $353.54 | $357.36 | $1,786.80 | 65 |
| INTC | 85 | $22.35 | $22.69 | $1,928.65 | 60 |
| JNJ | 13 | $155.43 | $164.77 | $2,142.01 | 70 |
| JPM | 8 | $292.65 | $285.66 | $2,285.28 | 75 |
| KO | 30 | $70.97 | $69.27 | $2,078.10 | 65 |
| LLY | 3 | $781.32 | $789.64 | $2,368.93 | 70 |
| MA | 4 | $563.08 | $555.36 | $2,221.44 | 65 |
| META | 3 | $717.12 | $702.91 | $2,108.73 | 70 |
| MRK | 29 | $82.56 | $82.44 | $2,390.76 | 75 |
| MSFT | 5 | $498.84 | $505.62 | $2,528.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,250.31 | $1,250.31 | 65 |
| NKE | 29 | $71.97 | $72.08 | $2,090.32 | 65 |
| NVDA | 15 | $171.51 | $171.37 | $2,570.55 | 85 |
| ORCL | 9 | $232.99 | $241.19 | $2,170.71 | 75 |
| PEP | 15 | $136.57 | $135.35 | $2,030.25 | 65 |
| PFE | 85 | $25.27 | $24.59 | $2,090.15 | 65 |
| PG | 13 | $152.06 | $153.71 | $1,998.23 | 65 |
| PYPL | 29 | $72.15 | $72.97 | $2,116.13 | 65 |
| QCOM | 14 | $153.83 | $154.07 | $2,156.98 | 70 |
| T | 77 | $27.10 | $26.95 | $2,074.76 | 65 |
| TGT | 20 | $104.94 | $101.36 | $2,027.20 | 65 |
| TSLA | 6 | $318.51 | $321.67 | $1,930.02 | 65 |
| UNH | 7 | $298.51 | $292.46 | $2,047.22 | 65 |
| UNP | 9 | $236.79 | $231.15 | $2,080.39 | 65 |
| V | 6 | $355.85 | $349.85 | $2,099.10 | 70 |
| VZ | 50 | $43.08 | $41.24 | $2,062.25 | 65 |
| WFC | 28 | $78.82 | $79.89 | $2,236.92 | 70 |
| WMT | 22 | $97.29 | $95.12 | $2,092.75 | 65 |
| XOM | 20 | $109.87 | $112.22 | $2,244.40 | 70 |

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
| 2025-07-16 20:09:15 | SELL | XOM | 1 | $112.22 | $2.24 | 70 |
| 2025-07-16 20:09:15 | SELL | NKE | 4 | $72.08 | $0.37 | 65 |
| 2025-07-16 20:09:15 | SELL | WFC | 1 | $79.89 | $1.03 | 70 |
| 2025-07-16 20:09:15 | BUY | NVDA | 1 | $171.37 | N/A | 85 |
| 2025-07-16 20:09:15 | BUY | AMD | 13 | $160.08 | N/A | 70 |
| 2025-07-16 20:09:01 | SELL | AMD | 15 | $160.08 | $220.20 | 70 |
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

<!--TRADE_LOG_END--> 
