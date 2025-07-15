# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 20:09:25**

| Metric | Value |
|---|---|
| **Total Value** | **$100,349.78** |
| Cash | $648.21 |
| Holdings Value | $99,701.57 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.11 | $2,091.10 | 65 |
| ADBE | 6 | $375.23 | $364.18 | $2,185.08 | 65 |
| AMD | 17 | $146.29 | $155.61 | $2,645.37 | 85 |
| AMZN | 10 | $221.65 | $226.35 | $2,263.50 | 75 |
| AVGO | 8 | $275.34 | $280.94 | $2,247.52 | 70 |
| AXP | 7 | $325.34 | $310.50 | $2,173.50 | 65 |
| BA | 9 | $210.91 | $229.95 | $2,069.55 | 70 |
| BAC | 45 | $46.28 | $46.12 | $2,075.40 | 65 |
| C | 30 | $86.78 | $90.66 | $2,719.65 | 85 |
| CAT | 6 | $397.74 | $404.61 | $2,427.66 | 75 |
| COST | 2 | $979.83 | $967.68 | $1,935.36 | 65 |
| CRM | 8 | $267.44 | $257.23 | $2,057.84 | 65 |
| CSCO | 31 | $68.46 | $67.18 | $2,082.58 | 65 |
| CVX | 17 | $147.01 | $150.70 | $2,561.90 | 85 |
| DIS | 18 | $122.77 | $118.94 | $2,140.83 | 65 |
| GOOGL | 14 | $179.71 | $182.00 | $2,548.00 | 85 |
| GS | 3 | $717.52 | $701.75 | $2,105.25 | 70 |
| HD | 6 | $372.64 | $358.60 | $2,151.60 | 65 |
| INTC | 89 | $22.39 | $22.92 | $2,039.88 | 65 |
| JNJ | 13 | $155.95 | $155.18 | $2,017.34 | 65 |
| JPM | 9 | $291.63 | $286.30 | $2,576.70 | 85 |
| KO | 30 | $70.97 | $69.33 | $2,080.05 | 65 |
| LLY | 3 | $781.32 | $771.73 | $2,315.18 | 65 |
| MA | 4 | $563.08 | $550.00 | $2,200.00 | 65 |
| META | 3 | $717.12 | $710.39 | $2,131.17 | 70 |
| MRK | 26 | $82.50 | $81.54 | $2,120.10 | 65 |
| MSFT | 5 | $498.84 | $505.82 | $2,529.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,260.27 | $1,260.27 | 65 |
| NKE | 30 | $72.03 | $72.00 | $2,160.00 | 70 |
| NVDA | 13 | $171.69 | $170.70 | $2,219.10 | 70 |
| ORCL | 9 | $233.15 | $235.01 | $2,115.09 | 65 |
| PEP | 15 | $136.57 | $133.81 | $2,007.15 | 65 |
| PFE | 84 | $25.28 | $24.59 | $2,065.14 | 65 |
| PG | 13 | $152.11 | $152.60 | $1,983.86 | 65 |
| PYPL | 28 | $72.12 | $72.96 | $2,042.88 | 65 |
| QCOM | 14 | $153.83 | $154.30 | $2,160.20 | 65 |
| T | 76 | $27.09 | $27.00 | $2,052.00 | 65 |
| TGT | 20 | $104.94 | $102.22 | $2,044.40 | 65 |
| TSLA | 6 | $318.51 | $310.78 | $1,864.68 | 55 |
| UNH | 7 | $298.51 | $291.54 | $2,040.78 | 65 |
| UNP | 10 | $236.13 | $231.14 | $2,311.40 | 75 |
| V | 6 | $355.85 | $346.95 | $2,081.73 | 65 |
| VZ | 50 | $43.08 | $41.25 | $2,062.50 | 65 |
| WFC | 30 | $78.89 | $78.85 | $2,365.50 | 75 |
| WMT | 21 | $97.38 | $95.36 | $2,002.66 | 65 |
| XOM | 21 | $110.02 | $112.91 | $2,371.01 | 75 |

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
| 2025-07-15 20:09:19 | SELL | NVDA | 2 | $170.70 | $-1.71 | 70 |
| 2025-07-15 20:09:19 | BUY | WFC | 4 | $78.85 | N/A | 75 |
| 2025-07-15 19:50:51 | SELL | BA | 1 | $230.63 | $17.75 | 65 |
| 2025-07-15 19:50:51 | SELL | WFC | 2 | $78.74 | $-0.30 | 65 |
| 2025-07-15 19:50:51 | BUY | INTC | 6 | $22.96 | N/A | 65 |
| 2025-07-15 19:50:51 | BUY | UNP | 1 | $231.37 | N/A | 75 |
| 2025-07-15 19:36:59 | SELL | INTC | 6 | $23.00 | $3.61 | 60 |
| 2025-07-15 19:36:59 | SELL | PFE | 1 | $24.57 | $-0.71 | 65 |
| 2025-07-15 19:36:59 | BUY | NKE | 1 | $71.93 | N/A | 70 |
| 2025-07-15 19:36:59 | BUY | WFC | 1 | $78.79 | N/A | 70 |
| 2025-07-15 19:36:59 | BUY | CVX | 1 | $150.78 | N/A | 85 |
| 2025-07-15 19:25:11 | SELL | BAC | 3 | $46.37 | $0.24 | 65 |
| 2025-07-15 19:25:11 | SELL | NKE | 1 | $71.90 | $-0.13 | 65 |
| 2025-07-15 19:25:11 | SELL | PFE | 3 | $24.57 | $-2.06 | 65 |
| 2025-07-15 19:25:11 | SELL | CVX | 1 | $150.88 | $3.87 | 75 |
| 2025-07-15 19:25:11 | BUY | NVDA | 2 | $170.14 | N/A | 85 |
| 2025-07-15 19:25:11 | BUY | VZ | 3 | $41.33 | N/A | 65 |
| 2025-07-15 19:08:22 | SELL | AMZN | 1 | $226.20 | $4.14 | 70 |
| 2025-07-15 19:08:22 | SELL | MRK | 1 | $81.50 | $-0.97 | 65 |
| 2025-07-15 19:08:22 | SELL | BA | 1 | $231.14 | $16.60 | 70 |
| 2025-07-15 19:08:22 | SELL | WFC | 1 | $78.33 | $-0.54 | 65 |
| 2025-07-15 19:08:22 | SELL | UNP | 1 | $231.50 | $-4.64 | 65 |
| 2025-07-15 19:08:22 | SELL | VZ | 3 | $41.31 | $-5.29 | 60 |
| 2025-07-15 19:08:22 | BUY | BAC | 3 | $46.24 | N/A | 70 |
| 2025-07-15 19:08:22 | BUY | PFE | 4 | $25.35 | N/A | 70 |

<!--TRADE_LOG_END--> 
