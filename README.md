# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 15:40:25**

| Metric | Value |
|---|---|
| **Total Value** | **$100,771.68** |
| Cash | $602.74 |
| Holdings Value | $100,168.94 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.97 | $2,089.70 | 65 |
| ADBE | 6 | $375.23 | $364.95 | $2,189.70 | 65 |
| AMD | 14 | $133.89 | $145.75 | $2,040.50 | 70 |
| AMZN | 11 | $221.92 | $225.77 | $2,483.47 | 75 |
| AVGO | 8 | $275.34 | $275.50 | $2,204.04 | 70 |
| AXP | 7 | $325.34 | $320.89 | $2,246.23 | 75 |
| BA | 10 | $212.59 | $230.23 | $2,302.30 | 75 |
| BAC | 44 | $48.83 | $46.80 | $2,059.42 | 65 |
| C | 31 | $86.64 | $87.03 | $2,697.93 | 85 |
| CAT | 6 | $397.74 | $404.17 | $2,425.04 | 70 |
| COST | 2 | $979.83 | $973.90 | $1,947.80 | 65 |
| CRM | 7 | $268.68 | $260.28 | $1,821.96 | 65 |
| CSCO | 31 | $68.48 | $67.37 | $2,088.47 | 65 |
| CVX | 17 | $147.10 | $152.51 | $2,592.67 | 85 |
| DIS | 18 | $122.79 | $120.11 | $2,161.98 | 70 |
| GOOGL | 13 | $179.57 | $180.76 | $2,349.84 | 75 |
| GS | 3 | $717.52 | $711.25 | $2,133.75 | 70 |
| HD | 6 | $372.64 | $369.13 | $2,214.81 | 65 |
| INTC | 87 | $22.38 | $23.11 | $2,010.69 | 65 |
| JNJ | 13 | $155.95 | $156.60 | $2,035.80 | 65 |
| JPM | 9 | $291.63 | $287.76 | $2,589.86 | 85 |
| KO | 29 | $71.03 | $69.80 | $2,024.14 | 65 |
| LLY | 3 | $781.32 | $795.39 | $2,386.16 | 70 |
| MA | 4 | $563.08 | $555.80 | $2,223.20 | 65 |
| META | 3 | $717.12 | $725.42 | $2,176.26 | 85 |
| MRK | 28 | $82.48 | $83.71 | $2,343.88 | 75 |
| MSFT | 5 | $498.84 | $502.66 | $2,513.30 | 85 |
| NFLX | 1 | $1,279.00 | $1,266.36 | $1,266.36 | 65 |
| NKE | 31 | $72.07 | $72.42 | $2,245.02 | 70 |
| NVDA | 16 | $157.68 | $164.86 | $2,637.68 | 85 |
| ORCL | 9 | $233.26 | $229.14 | $2,062.26 | 65 |
| PEP | 15 | $136.57 | $135.25 | $2,028.75 | 65 |
| PFE | 86 | $25.21 | $25.53 | $2,195.58 | 70 |
| PG | 13 | $160.78 | $153.94 | $2,001.22 | 65 |
| PYPL | 31 | $72.27 | $73.55 | $2,280.05 | 75 |
| QCOM | 13 | $153.79 | $153.91 | $2,000.77 | 65 |
| T | 75 | $27.10 | $27.23 | $2,042.62 | 65 |
| TGT | 20 | $104.94 | $104.88 | $2,097.50 | 65 |
| TSLA | 6 | $288.62 | $315.00 | $1,890.00 | 65 |
| UNH | 7 | $298.51 | $299.94 | $2,099.58 | 65 |
| UNP | 9 | $236.60 | $233.10 | $2,097.94 | 70 |
| V | 6 | $355.85 | $351.12 | $2,106.72 | 70 |
| VZ | 49 | $43.12 | $41.71 | $2,043.79 | 65 |
| WFC | 28 | $82.26 | $83.06 | $2,325.82 | 75 |
| WMT | 21 | $97.38 | $95.41 | $2,003.51 | 65 |
| XOM | 21 | $110.01 | $113.85 | $2,390.85 | 75 |

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
| 2025-07-14 15:40:20 | SELL | BAC | 2 | $46.81 | $-3.88 | 65 |
| 2025-07-14 15:40:20 | SELL | NKE | 1 | $72.42 | $0.34 | 70 |
| 2025-07-14 15:40:20 | SELL | MRK | 1 | $83.70 | $1.18 | 75 |
| 2025-07-14 15:40:20 | SELL | PFE | 1 | $25.53 | $0.31 | 70 |
| 2025-07-14 15:40:20 | BUY | INTC | 5 | $23.11 | N/A | 65 |
| 2025-07-14 15:40:20 | BUY | PYPL | 1 | $73.52 | N/A | 75 |
| 2025-07-14 15:26:28 | SELL | PYPL | 1 | $73.74 | $1.46 | 70 |
| 2025-07-14 15:26:28 | SELL | PFE | 5 | $25.46 | $1.18 | 70 |
| 2025-07-14 15:26:28 | SELL | UNP | 1 | $232.40 | $-3.78 | 65 |
| 2025-07-14 15:26:28 | SELL | CSCO | 1 | $67.31 | $-1.14 | 65 |
| 2025-07-14 15:26:28 | BUY | BAC | 2 | $46.81 | N/A | 70 |
| 2025-07-14 15:26:28 | BUY | CVX | 1 | $152.33 | N/A | 85 |
| 2025-07-14 15:09:27 | SELL | INTC | 6 | $23.11 | $4.39 | 60 |
| 2025-07-14 15:09:27 | SELL | BAC | 3 | $46.76 | $-5.84 | 65 |
| 2025-07-14 15:09:27 | BUY | PFE | 6 | $25.44 | N/A | 75 |
| 2025-07-14 15:09:27 | BUY | CSCO | 2 | $67.95 | N/A | 70 |
| 2025-07-14 14:53:08 | SELL | GOOGL | 1 | $180.70 | $1.05 | 75 |
| 2025-07-14 14:53:08 | SELL | AMD | 1 | $144.98 | $10.35 | 65 |
| 2025-07-14 14:53:08 | SELL | INTC | 1 | $23.10 | $0.71 | 65 |
| 2025-07-14 14:53:08 | SELL | TGT | 1 | $103.82 | $-1.06 | 65 |
| 2025-07-14 14:53:08 | BUY | NVDA | 3 | $164.12 | N/A | 85 |
| 2025-07-14 14:53:08 | BUY | DIS | 1 | $119.82 | N/A | 70 |
| 2025-07-14 14:53:08 | BUY | PYPL | 1 | $73.98 | N/A | 75 |
| 2025-07-14 14:53:08 | BUY | MRK | 1 | $83.46 | N/A | 80 |
| 2025-07-14 14:53:08 | BUY | NKE | 3 | $72.06 | N/A | 75 |

<!--TRADE_LOG_END--> 
