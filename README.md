# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 18:59:14**

| Metric | Value |
|---|---|
| **Total Value** | **$100,760.12** |
| Cash | $1,153.88 |
| Holdings Value | $99,606.23 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.44 | $2,104.40 | 65 |
| ADBE | 6 | $375.23 | $362.76 | $2,176.57 | 65 |
| AMD | 14 | $144.14 | $157.54 | $2,205.56 | 65 |
| AMZN | 10 | $221.65 | $223.36 | $2,233.60 | 75 |
| AVGO | 8 | $275.34 | $279.53 | $2,236.24 | 65 |
| AXP | 6 | $308.37 | $312.24 | $1,873.41 | 65 |
| BA | 9 | $210.81 | $229.35 | $2,064.15 | 65 |
| BAC | 58 | $46.20 | $46.02 | $2,669.16 | 85 |
| C | 30 | $86.85 | $90.12 | $2,703.75 | 85 |
| CAT | 6 | $397.74 | $411.71 | $2,470.29 | 85 |
| COST | 2 | $979.83 | $951.66 | $1,903.32 | 65 |
| CRM | 8 | $267.44 | $257.59 | $2,060.72 | 65 |
| CSCO | 31 | $68.46 | $67.34 | $2,087.70 | 65 |
| CVX | 17 | $147.08 | $151.09 | $2,568.53 | 85 |
| DIS | 18 | $122.77 | $120.17 | $2,163.13 | 65 |
| GOOGL | 12 | $178.99 | $183.69 | $2,204.28 | 75 |
| GS | 3 | $717.52 | $706.93 | $2,120.79 | 70 |
| HD | 5 | $353.54 | $357.76 | $1,788.80 | 65 |
| INTC | 85 | $22.36 | $22.55 | $1,916.33 | 60 |
| JNJ | 13 | $155.43 | $164.44 | $2,137.66 | 70 |
| JPM | 9 | $291.86 | $285.19 | $2,566.70 | 75 |
| KO | 30 | $70.97 | $69.39 | $2,081.55 | 65 |
| LLY | 3 | $781.32 | $789.28 | $2,367.85 | 65 |
| MA | 4 | $563.08 | $554.44 | $2,217.76 | 65 |
| META | 3 | $717.12 | $703.64 | $2,110.92 | 65 |
| MRK | 29 | $82.56 | $82.40 | $2,389.60 | 75 |
| MSFT | 5 | $498.84 | $506.10 | $2,530.50 | 85 |
| NFLX | 1 | $1,279.00 | $1,259.69 | $1,259.69 | 65 |
| NKE | 29 | $71.99 | $72.07 | $2,090.03 | 65 |
| NVDA | 14 | $171.52 | $171.08 | $2,395.12 | 70 |
| ORCL | 9 | $232.99 | $240.50 | $2,164.50 | 65 |
| PEP | 15 | $136.57 | $135.00 | $2,025.07 | 65 |
| PFE | 90 | $25.24 | $24.66 | $2,218.95 | 70 |
| PG | 13 | $152.06 | $153.39 | $1,994.07 | 65 |
| PYPL | 29 | $72.15 | $72.89 | $2,113.95 | 65 |
| QCOM | 14 | $153.83 | $153.87 | $2,154.18 | 65 |
| T | 77 | $27.09 | $27.00 | $2,079.38 | 65 |
| TGT | 20 | $104.94 | $101.65 | $2,033.00 | 65 |
| TSLA | 6 | $318.51 | $320.60 | $1,923.60 | 60 |
| UNH | 7 | $298.51 | $293.93 | $2,057.51 | 65 |
| UNP | 10 | $236.22 | $231.32 | $2,313.20 | 75 |
| V | 6 | $355.85 | $350.17 | $2,101.02 | 65 |
| VZ | 50 | $43.08 | $41.33 | $2,066.50 | 65 |
| WFC | 29 | $78.86 | $79.89 | $2,316.81 | 75 |
| WMT | 22 | $97.29 | $94.99 | $2,089.78 | 65 |
| XOM | 20 | $109.85 | $112.83 | $2,256.60 | 70 |

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
| 2025-07-16 18:27:21 | BUY | PFE | 1 | $24.62 | N/A | 65 |
| 2025-07-16 18:11:26 | SELL | AMD | 2 | $156.45 | $20.15 | 70 |
| 2025-07-16 18:11:26 | SELL | NKE | 4 | $72.14 | $0.57 | 65 |
| 2025-07-16 18:11:26 | BUY | NVDA | 1 | $170.68 | N/A | 85 |
| 2025-07-16 18:11:26 | BUY | WFC | 1 | $79.57 | N/A | 70 |
| 2025-07-16 17:52:21 | SELL | INTC | 1 | $22.52 | $0.17 | 60 |

<!--TRADE_LOG_END--> 
