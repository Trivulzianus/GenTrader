# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 19:10:51**

| Metric | Value |
|---|---|
| **Total Value** | **$100,761.01** |
| Cash | $1,415.47 |
| Holdings Value | $99,345.54 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.29 | $2,102.95 | 65 |
| ADBE | 6 | $375.23 | $363.42 | $2,180.52 | 65 |
| AMD | 17 | $146.60 | $158.18 | $2,689.06 | 85 |
| AMZN | 10 | $221.65 | $223.30 | $2,233.00 | 75 |
| AVGO | 8 | $275.34 | $279.75 | $2,238.04 | 70 |
| AXP | 6 | $308.37 | $312.06 | $1,872.36 | 65 |
| BA | 9 | $210.81 | $229.61 | $2,066.49 | 65 |
| BAC | 49 | $46.24 | $46.02 | $2,255.22 | 70 |
| C | 30 | $86.85 | $90.11 | $2,703.15 | 85 |
| CAT | 6 | $397.74 | $411.84 | $2,471.04 | 85 |
| COST | 2 | $979.83 | $951.79 | $1,903.58 | 65 |
| CRM | 8 | $267.44 | $258.03 | $2,064.24 | 65 |
| CSCO | 31 | $68.46 | $67.35 | $2,087.85 | 65 |
| CVX | 16 | $146.84 | $150.90 | $2,414.44 | 75 |
| DIS | 18 | $122.77 | $120.02 | $2,160.27 | 65 |
| GOOGL | 13 | $179.34 | $183.47 | $2,385.05 | 75 |
| GS | 3 | $717.52 | $706.96 | $2,120.88 | 70 |
| HD | 5 | $353.54 | $357.33 | $1,786.67 | 65 |
| INTC | 85 | $22.36 | $22.55 | $1,916.75 | 60 |
| JNJ | 13 | $155.43 | $164.31 | $2,136.03 | 65 |
| JPM | 9 | $291.86 | $285.17 | $2,566.53 | 85 |
| KO | 30 | $70.97 | $69.34 | $2,080.35 | 65 |
| LLY | 3 | $781.32 | $789.76 | $2,369.29 | 65 |
| MA | 4 | $563.08 | $554.25 | $2,217.00 | 65 |
| META | 3 | $717.12 | $702.97 | $2,108.89 | 65 |
| MRK | 29 | $82.56 | $82.33 | $2,387.43 | 75 |
| MSFT | 5 | $498.84 | $506.15 | $2,530.75 | 85 |
| NFLX | 1 | $1,279.00 | $1,259.13 | $1,259.13 | 65 |
| NKE | 29 | $71.99 | $72.01 | $2,088.29 | 65 |
| NVDA | 14 | $171.52 | $170.82 | $2,391.48 | 70 |
| ORCL | 9 | $232.99 | $240.99 | $2,168.91 | 65 |
| PEP | 15 | $136.57 | $135.04 | $2,025.64 | 65 |
| PFE | 85 | $25.27 | $24.66 | $2,096.10 | 65 |
| PG | 13 | $152.06 | $153.33 | $1,993.29 | 65 |
| PYPL | 29 | $72.15 | $72.96 | $2,115.84 | 65 |
| QCOM | 14 | $153.83 | $154.01 | $2,156.21 | 65 |
| T | 77 | $27.09 | $27.01 | $2,079.95 | 65 |
| TGT | 20 | $104.94 | $101.53 | $2,030.70 | 65 |
| TSLA | 6 | $318.51 | $322.02 | $1,932.12 | 60 |
| UNH | 7 | $298.51 | $292.80 | $2,049.60 | 65 |
| UNP | 9 | $236.79 | $231.09 | $2,079.81 | 65 |
| V | 6 | $355.85 | $350.31 | $2,101.83 | 65 |
| VZ | 50 | $43.08 | $41.32 | $2,066.01 | 65 |
| WFC | 29 | $78.86 | $79.94 | $2,318.12 | 75 |
| WMT | 22 | $97.29 | $94.94 | $2,088.79 | 65 |
| XOM | 20 | $109.85 | $112.79 | $2,255.87 | 70 |

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
| 2025-07-16 18:59:06 | BUY | BAC | 9 | $46.01 | N/A | 85 |
| 2025-07-16 18:59:06 | BUY | PFE | 5 | $24.67 | N/A | 70 |
| 2025-07-16 18:59:06 | BUY | WFC | 2 | $79.89 | N/A | 75 |
| 2025-07-16 18:59:06 | BUY | CVX | 1 | $151.08 | N/A | 85 |
| 2025-07-16 18:46:09 | SELL | GOOGL | 1 | $183.56 | $4.22 | 65 |
| 2025-07-16 18:46:09 | SELL | WFC | 1 | $79.79 | $0.96 | 65 |
| 2025-07-16 18:46:09 | BUY | NKE | 4 | $72.14 | N/A | 75 |
| 2025-07-16 18:46:09 | BUY | MRK | 3 | $82.33 | N/A | 75 |
| 2025-07-16 18:46:09 | BUY | T | 5 | $26.97 | N/A | 70 |
| 2025-07-16 18:27:21 | SELL | NVDA | 1 | $170.99 | $-0.49 | 70 |
| 2025-07-16 18:27:21 | SELL | MRK | 3 | $81.52 | $-2.86 | 65 |
| 2025-07-16 18:27:21 | BUY | BAC | 3 | $45.85 | N/A | 70 |
| 2025-07-16 18:27:21 | BUY | INTC | 1 | $22.50 | N/A | 60 |
| 2025-07-16 18:27:21 | BUY | XOM | 1 | $112.69 | N/A | 75 |

<!--TRADE_LOG_END--> 
