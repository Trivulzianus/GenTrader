# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 14:26:16**

| Metric | Value |
|---|---|
| **Total Value** | **$100,450.79** |
| Cash | $1,211.16 |
| Holdings Value | $99,239.64 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $212.00 | $2,119.98 | 70 |
| ADBE | 6 | $375.23 | $360.22 | $2,161.32 | 65 |
| AMD | 14 | $144.36 | $154.96 | $2,169.39 | 70 |
| AMZN | 10 | $221.65 | $225.08 | $2,250.80 | 75 |
| AVGO | 8 | $275.34 | $278.35 | $2,226.80 | 70 |
| AXP | 7 | $325.34 | $310.55 | $2,173.85 | 65 |
| BA | 9 | $210.81 | $229.76 | $2,067.84 | 70 |
| BAC | 45 | $46.28 | $45.77 | $2,059.43 | 65 |
| C | 30 | $86.78 | $89.97 | $2,698.95 | 85 |
| CAT | 6 | $397.74 | $407.36 | $2,444.16 | 85 |
| COST | 2 | $979.83 | $954.00 | $1,908.00 | 65 |
| CRM | 8 | $267.44 | $256.85 | $2,054.80 | 65 |
| CSCO | 31 | $68.46 | $67.42 | $2,090.17 | 65 |
| CVX | 16 | $146.76 | $150.66 | $2,410.56 | 80 |
| DIS | 18 | $122.77 | $120.36 | $2,166.48 | 70 |
| GOOGL | 14 | $179.71 | $183.64 | $2,570.96 | 75 |
| GS | 3 | $717.52 | $694.74 | $2,084.20 | 70 |
| HD | 6 | $372.64 | $358.14 | $2,148.87 | 70 |
| INTC | 84 | $22.36 | $22.73 | $1,908.90 | 60 |
| JNJ | 13 | $155.43 | $162.74 | $2,115.62 | 65 |
| JPM | 9 | $291.63 | $286.41 | $2,577.69 | 85 |
| KO | 30 | $70.97 | $69.01 | $2,070.30 | 65 |
| LLY | 3 | $781.32 | $781.68 | $2,345.04 | 65 |
| MA | 4 | $563.08 | $553.04 | $2,212.16 | 65 |
| META | 3 | $717.12 | $708.90 | $2,126.70 | 75 |
| MRK | 29 | $82.47 | $82.09 | $2,380.61 | 75 |
| MSFT | 5 | $498.84 | $503.34 | $2,516.70 | 75 |
| NFLX | 1 | $1,279.00 | $1,257.24 | $1,257.24 | 65 |
| NKE | 29 | $72.03 | $72.16 | $2,092.49 | 65 |
| NVDA | 15 | $171.49 | $169.62 | $2,544.37 | 85 |
| ORCL | 9 | $233.15 | $234.40 | $2,109.56 | 65 |
| PEP | 15 | $136.57 | $134.24 | $2,013.60 | 65 |
| PFE | 83 | $25.29 | $24.80 | $2,057.99 | 65 |
| PG | 14 | $152.15 | $153.04 | $2,142.56 | 65 |
| PYPL | 29 | $72.15 | $72.41 | $2,099.89 | 65 |
| QCOM | 14 | $153.83 | $153.52 | $2,149.28 | 65 |
| T | 77 | $27.09 | $26.99 | $2,078.04 | 65 |
| TGT | 20 | $104.94 | $101.88 | $2,037.50 | 65 |
| TSLA | 6 | $318.51 | $317.54 | $1,905.23 | 65 |
| UNH | 7 | $298.51 | $293.82 | $2,056.74 | 65 |
| UNP | 9 | $236.78 | $230.72 | $2,076.43 | 65 |
| V | 6 | $355.85 | $347.95 | $2,087.70 | 65 |
| VZ | 50 | $43.08 | $41.30 | $2,064.75 | 65 |
| WFC | 26 | $78.81 | $79.33 | $2,062.45 | 65 |
| WMT | 22 | $97.29 | $94.84 | $2,086.53 | 65 |
| XOM | 20 | $109.86 | $112.85 | $2,257.00 | 70 |

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
| 2025-07-16 14:26:09 | SELL | XOM | 1 | $112.84 | $2.84 | 70 |
| 2025-07-16 14:26:09 | SELL | NKE | 1 | $72.13 | $0.10 | 65 |
| 2025-07-16 14:26:09 | BUY | NVDA | 1 | $169.74 | N/A | 85 |
| 2025-07-16 14:08:31 | SELL | INTC | 7 | $22.69 | $2.16 | 60 |
| 2025-07-16 14:08:31 | SELL | AMD | 1 | $154.68 | $9.64 | 65 |
| 2025-07-16 14:08:31 | SELL | PFE | 1 | $24.86 | $-0.42 | 65 |
| 2025-07-16 14:08:31 | SELL | WFC | 1 | $79.43 | $0.60 | 65 |
| 2025-07-16 14:08:31 | SELL | UNP | 1 | $230.54 | $-5.61 | 65 |
| 2025-07-16 14:08:31 | BUY | XOM | 1 | $112.48 | N/A | 75 |
| 2025-07-16 14:08:31 | BUY | NKE | 1 | $72.00 | N/A | 70 |
| 2025-07-16 13:50:09 | SELL | NVDA | 1 | $170.74 | $-0.81 | 70 |
| 2025-07-16 13:50:09 | SELL | JNJ | 1 | $161.91 | $6.02 | 65 |
| 2025-07-16 13:50:09 | SELL | XOM | 1 | $112.87 | $2.85 | 70 |
| 2025-07-16 13:50:09 | SELL | PFE | 1 | $24.92 | $-0.36 | 65 |
| 2025-07-16 13:50:09 | SELL | BA | 1 | $230.91 | $18.09 | 65 |
| 2025-07-16 13:50:09 | SELL | WFC | 3 | $79.46 | $1.71 | 65 |
| 2025-07-16 13:50:09 | SELL | CVX | 1 | $150.89 | $3.88 | 75 |
| 2025-07-16 13:50:09 | BUY | INTC | 7 | $22.65 | N/A | 65 |
| 2025-07-16 13:50:09 | BUY | MRK | 3 | $82.21 | N/A | 75 |
| 2025-07-16 13:50:09 | BUY | UNP | 1 | $231.38 | N/A | 75 |
| 2025-07-16 13:30:02 | SELL | BAC | 3 | $46.15 | $-0.37 | 65 |
| 2025-07-16 13:30:02 | BUY | NVDA | 1 | $170.70 | N/A | 85 |
| 2025-07-16 13:30:02 | BUY | WFC | 2 | $78.86 | N/A | 75 |
| 2025-07-16 13:04:56 | SELL | UNP | 1 | $231.14 | $-4.99 | 65 |
| 2025-07-16 13:04:56 | SELL | T | 1 | $27.02 | $-0.07 | 65 |

<!--TRADE_LOG_END--> 
