# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 15:52:15**

| Metric | Value |
|---|---|
| **Total Value** | **$100,149.82** |
| Cash | $2,426.58 |
| Holdings Value | $97,723.24 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.68 | $2,096.80 | 70 |
| ADBE | 6 | $375.23 | $360.64 | $2,163.84 | 65 |
| AMD | 14 | $144.36 | $154.37 | $2,161.22 | 70 |
| AMZN | 10 | $221.65 | $222.91 | $2,229.10 | 75 |
| AVGO | 8 | $275.34 | $277.65 | $2,221.20 | 65 |
| AXP | 6 | $308.37 | $308.18 | $1,849.08 | 65 |
| BA | 9 | $210.81 | $228.44 | $2,055.96 | 65 |
| BAC | 46 | $46.25 | $45.31 | $2,084.26 | 65 |
| C | 27 | $86.47 | $88.79 | $2,397.33 | 75 |
| CAT | 6 | $397.74 | $406.30 | $2,437.80 | 85 |
| COST | 2 | $979.83 | $954.20 | $1,908.39 | 65 |
| CRM | 8 | $267.44 | $255.45 | $2,043.60 | 65 |
| CSCO | 31 | $68.46 | $67.19 | $2,083.04 | 65 |
| CVX | 16 | $146.82 | $150.25 | $2,404.00 | 75 |
| DIS | 18 | $122.77 | $119.23 | $2,146.14 | 65 |
| GOOGL | 13 | $179.38 | $182.66 | $2,374.64 | 75 |
| GS | 3 | $717.52 | $698.14 | $2,094.42 | 75 |
| HD | 5 | $353.54 | $354.95 | $1,774.75 | 65 |
| INTC | 86 | $22.36 | $22.34 | $1,920.81 | 60 |
| JNJ | 13 | $155.43 | $165.52 | $2,151.76 | 70 |
| JPM | 8 | $292.60 | $284.79 | $2,278.32 | 75 |
| KO | 30 | $70.97 | $69.19 | $2,075.70 | 65 |
| LLY | 3 | $781.32 | $790.25 | $2,370.74 | 70 |
| MA | 4 | $563.08 | $551.78 | $2,207.14 | 65 |
| META | 3 | $717.12 | $701.50 | $2,104.50 | 70 |
| MRK | 29 | $82.47 | $82.09 | $2,380.61 | 75 |
| MSFT | 5 | $498.84 | $503.61 | $2,518.05 | 75 |
| NFLX | 1 | $1,279.00 | $1,262.09 | $1,262.09 | 65 |
| NKE | 31 | $71.99 | $71.43 | $2,214.33 | 70 |
| NVDA | 13 | $171.62 | $169.94 | $2,209.27 | 65 |
| ORCL | 9 | $232.99 | $234.98 | $2,114.84 | 65 |
| PEP | 15 | $136.57 | $134.57 | $2,018.55 | 65 |
| PFE | 84 | $25.28 | $24.77 | $2,080.68 | 65 |
| PG | 14 | $152.15 | $152.58 | $2,136.12 | 65 |
| PYPL | 29 | $72.15 | $72.10 | $2,090.90 | 65 |
| QCOM | 14 | $153.83 | $152.46 | $2,134.44 | 65 |
| T | 77 | $27.09 | $27.02 | $2,080.16 | 65 |
| TGT | 20 | $104.94 | $100.77 | $2,015.30 | 65 |
| TSLA | 6 | $318.51 | $319.34 | $1,916.06 | 65 |
| UNH | 7 | $298.51 | $291.32 | $2,039.21 | 65 |
| UNP | 9 | $236.78 | $230.46 | $2,074.10 | 65 |
| V | 6 | $355.85 | $348.07 | $2,088.45 | 65 |
| VZ | 50 | $43.08 | $41.28 | $2,064.25 | 65 |
| WFC | 28 | $78.80 | $78.63 | $2,201.64 | 70 |
| WMT | 22 | $97.29 | $94.88 | $2,087.36 | 65 |
| XOM | 21 | $109.99 | $112.49 | $2,362.29 | 75 |

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
| 2025-07-16 15:52:09 | SELL | NVDA | 3 | $170.08 | $-3.74 | 65 |
| 2025-07-16 15:52:09 | SELL | ORCL | 1 | $235.34 | $2.11 | 65 |
| 2025-07-16 15:52:09 | SELL | CVX | 2 | $150.21 | $6.01 | 75 |
| 2025-07-16 15:52:09 | BUY | NKE | 2 | $71.46 | N/A | 70 |
| 2025-07-16 15:52:09 | BUY | C | 3 | $88.84 | N/A | 75 |
| 2025-07-16 15:52:09 | BUY | WFC | 2 | $78.71 | N/A | 70 |
| 2025-07-16 15:40:59 | SELL | JPM | 1 | $283.89 | $-7.74 | 70 |
| 2025-07-16 15:40:59 | SELL | C | 1 | $88.51 | $2.24 | 65 |
| 2025-07-16 15:40:59 | BUY | NVDA | 2 | $169.67 | N/A | 85 |
| 2025-07-16 15:40:59 | BUY | BAC | 1 | $45.12 | N/A | 65 |
| 2025-07-16 15:40:59 | BUY | INTC | 1 | $22.30 | N/A | 60 |
| 2025-07-16 15:40:59 | BUY | HD | 5 | $353.54 | N/A | 65 |
| 2025-07-16 15:40:59 | BUY | PFE | 1 | $24.73 | N/A | 65 |
| 2025-07-16 15:40:59 | BUY | ORCL | 1 | $234.42 | N/A | 75 |
| 2025-07-16 15:40:59 | BUY | CVX | 2 | $150.69 | N/A | 85 |
| 2025-07-16 15:40:36 | SELL | HD | 6 | $353.78 | $-113.15 | 65 |
| 2025-07-16 15:26:58 | SELL | NVDA | 1 | $170.30 | $-1.19 | 70 |
| 2025-07-16 15:26:58 | SELL | C | 2 | $89.00 | $5.06 | 70 |
| 2025-07-16 15:26:58 | BUY | INTC | 1 | $22.42 | N/A | 60 |
| 2025-07-16 15:26:58 | BUY | AXP | 6 | $308.37 | N/A | 65 |
| 2025-07-16 15:26:33 | SELL | AXP | 7 | $308.53 | $-117.64 | 65 |
| 2025-07-16 15:08:56 | SELL | GOOGL | 1 | $184.08 | $4.37 | 75 |
| 2025-07-16 15:08:56 | SELL | C | 3 | $89.61 | $8.46 | 75 |
| 2025-07-16 15:08:56 | BUY | NVDA | 1 | $170.18 | N/A | 85 |
| 2025-07-16 14:52:56 | SELL | ORCL | 1 | $234.96 | $1.68 | 65 |

<!--TRADE_LOG_END--> 
