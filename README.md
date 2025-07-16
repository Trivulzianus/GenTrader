# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 14:53:05**

| Metric | Value |
|---|---|
| **Total Value** | **$100,599.67** |
| Cash | $1,269.24 |
| Holdings Value | $99,330.44 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.96 | $2,109.55 | 70 |
| ADBE | 6 | $375.23 | $361.67 | $2,170.02 | 65 |
| AMD | 14 | $144.36 | $154.69 | $2,165.73 | 65 |
| AMZN | 10 | $221.65 | $225.28 | $2,252.80 | 75 |
| AVGO | 8 | $275.34 | $278.55 | $2,228.40 | 70 |
| AXP | 7 | $325.34 | $311.17 | $2,178.16 | 65 |
| BA | 9 | $210.81 | $230.00 | $2,070.00 | 70 |
| BAC | 45 | $46.28 | $45.65 | $2,054.25 | 65 |
| C | 30 | $86.78 | $90.14 | $2,704.35 | 85 |
| CAT | 6 | $397.74 | $408.88 | $2,453.28 | 85 |
| COST | 2 | $979.83 | $957.93 | $1,915.86 | 65 |
| CRM | 8 | $267.44 | $257.19 | $2,057.52 | 65 |
| CSCO | 31 | $68.46 | $67.48 | $2,091.88 | 65 |
| CVX | 16 | $146.76 | $150.13 | $2,402.08 | 75 |
| DIS | 18 | $122.77 | $120.01 | $2,160.18 | 65 |
| GOOGL | 14 | $179.71 | $183.66 | $2,571.31 | 75 |
| GS | 3 | $717.52 | $701.25 | $2,103.76 | 85 |
| HD | 6 | $372.64 | $358.18 | $2,149.06 | 65 |
| INTC | 84 | $22.36 | $22.70 | $1,906.38 | 60 |
| JNJ | 13 | $155.43 | $163.95 | $2,131.35 | 65 |
| JPM | 9 | $291.63 | $286.72 | $2,580.50 | 75 |
| KO | 30 | $70.97 | $69.08 | $2,072.31 | 65 |
| LLY | 3 | $781.32 | $792.08 | $2,376.24 | 70 |
| MA | 4 | $563.08 | $553.52 | $2,214.10 | 65 |
| META | 3 | $717.12 | $708.02 | $2,124.06 | 70 |
| MRK | 29 | $82.47 | $82.58 | $2,394.82 | 75 |
| MSFT | 5 | $498.84 | $504.63 | $2,523.15 | 75 |
| NFLX | 1 | $1,279.00 | $1,261.86 | $1,261.86 | 65 |
| NKE | 29 | $72.03 | $72.11 | $2,091.28 | 65 |
| NVDA | 14 | $171.58 | $170.03 | $2,380.40 | 70 |
| ORCL | 9 | $233.10 | $234.96 | $2,114.60 | 65 |
| PEP | 15 | $136.57 | $134.52 | $2,017.80 | 65 |
| PFE | 83 | $25.29 | $24.90 | $2,066.70 | 65 |
| PG | 14 | $152.15 | $152.92 | $2,140.88 | 65 |
| PYPL | 29 | $72.15 | $72.36 | $2,098.30 | 65 |
| QCOM | 14 | $153.83 | $153.47 | $2,148.51 | 65 |
| T | 77 | $27.09 | $26.98 | $2,077.84 | 65 |
| TGT | 20 | $104.94 | $101.79 | $2,035.77 | 65 |
| TSLA | 6 | $318.51 | $320.01 | $1,920.06 | 65 |
| UNH | 7 | $298.51 | $293.33 | $2,053.28 | 65 |
| UNP | 9 | $236.78 | $231.66 | $2,084.89 | 65 |
| V | 6 | $355.85 | $348.66 | $2,091.96 | 65 |
| VZ | 50 | $43.08 | $41.30 | $2,064.75 | 65 |
| WFC | 26 | $78.81 | $79.43 | $2,065.18 | 65 |
| WMT | 22 | $97.29 | $95.01 | $2,090.26 | 65 |
| XOM | 21 | $109.99 | $112.62 | $2,365.02 | 75 |

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
| 2025-07-16 14:52:56 | SELL | ORCL | 1 | $234.96 | $1.68 | 65 |
| 2025-07-16 14:52:56 | BUY | XOM | 1 | $112.65 | N/A | 75 |
| 2025-07-16 14:40:59 | SELL | NVDA | 1 | $170.23 | $-1.26 | 70 |
| 2025-07-16 14:40:59 | BUY | ORCL | 1 | $234.45 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
