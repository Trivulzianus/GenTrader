# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 15:41:08**

| Metric | Value |
|---|---|
| **Total Value** | **$99,965.59** |
| Cash | $1,947.44 |
| Holdings Value | $98,018.15 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.21 | $2,092.06 | 70 |
| ADBE | 6 | $375.23 | $360.37 | $2,162.22 | 65 |
| AMD | 14 | $144.36 | $153.42 | $2,147.88 | 70 |
| AMZN | 10 | $221.65 | $222.54 | $2,225.39 | 75 |
| AVGO | 8 | $275.34 | $277.06 | $2,216.48 | 70 |
| AXP | 6 | $308.37 | $307.58 | $1,845.48 | 65 |
| BA | 9 | $210.81 | $227.57 | $2,048.13 | 65 |
| BAC | 46 | $46.25 | $45.17 | $2,077.60 | 65 |
| C | 24 | $86.17 | $88.57 | $2,125.68 | 65 |
| CAT | 6 | $397.74 | $404.58 | $2,427.48 | 75 |
| COST | 2 | $979.83 | $954.93 | $1,909.86 | 65 |
| CRM | 8 | $267.44 | $255.01 | $2,040.07 | 65 |
| CSCO | 31 | $68.46 | $67.12 | $2,080.72 | 65 |
| CVX | 18 | $147.20 | $149.90 | $2,698.15 | 85 |
| DIS | 18 | $122.77 | $119.02 | $2,142.36 | 65 |
| GOOGL | 13 | $179.38 | $182.58 | $2,373.54 | 75 |
| GS | 3 | $717.52 | $694.04 | $2,082.12 | 70 |
| HD | 5 | $353.54 | $353.54 | $1,767.70 | 65 |
| INTC | 86 | $22.36 | $22.29 | $1,916.75 | 60 |
| JNJ | 13 | $155.43 | $165.12 | $2,146.56 | 65 |
| JPM | 8 | $292.60 | $283.88 | $2,271.08 | 70 |
| KO | 30 | $70.97 | $69.17 | $2,074.95 | 65 |
| LLY | 3 | $781.32 | $790.81 | $2,372.43 | 70 |
| MA | 4 | $563.08 | $550.52 | $2,202.08 | 65 |
| META | 3 | $717.12 | $700.23 | $2,100.68 | 65 |
| MRK | 29 | $82.47 | $82.03 | $2,378.87 | 75 |
| MSFT | 5 | $498.84 | $502.62 | $2,513.12 | 75 |
| NFLX | 1 | $1,279.00 | $1,259.94 | $1,259.94 | 65 |
| NKE | 29 | $72.03 | $71.34 | $2,068.86 | 65 |
| NVDA | 16 | $171.33 | $169.76 | $2,716.16 | 85 |
| ORCL | 10 | $233.23 | $234.55 | $2,345.50 | 75 |
| PEP | 15 | $136.57 | $134.47 | $2,017.05 | 65 |
| PFE | 84 | $25.28 | $24.73 | $2,077.32 | 65 |
| PG | 14 | $152.15 | $152.71 | $2,137.94 | 65 |
| PYPL | 29 | $72.15 | $71.91 | $2,085.39 | 65 |
| QCOM | 14 | $153.83 | $151.97 | $2,127.58 | 65 |
| T | 77 | $27.09 | $27.00 | $2,079.00 | 65 |
| TGT | 20 | $104.94 | $100.55 | $2,011.00 | 65 |
| TSLA | 6 | $318.51 | $317.82 | $1,906.92 | 65 |
| UNH | 7 | $298.51 | $290.91 | $2,036.37 | 65 |
| UNP | 9 | $236.78 | $230.04 | $2,070.36 | 65 |
| V | 6 | $355.85 | $347.65 | $2,085.90 | 65 |
| VZ | 50 | $43.08 | $41.31 | $2,065.50 | 65 |
| WFC | 26 | $78.81 | $78.59 | $2,043.34 | 65 |
| WMT | 22 | $97.29 | $94.86 | $2,086.92 | 65 |
| XOM | 21 | $109.99 | $112.27 | $2,357.67 | 75 |

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
| 2025-07-16 14:52:56 | BUY | XOM | 1 | $112.65 | N/A | 75 |
| 2025-07-16 14:40:59 | SELL | NVDA | 1 | $170.23 | $-1.26 | 70 |
| 2025-07-16 14:40:59 | BUY | ORCL | 1 | $234.45 | N/A | 75 |
| 2025-07-16 14:26:09 | SELL | XOM | 1 | $112.84 | $2.84 | 70 |
| 2025-07-16 14:26:09 | SELL | NKE | 1 | $72.13 | $0.10 | 65 |
| 2025-07-16 14:26:09 | BUY | NVDA | 1 | $169.74 | N/A | 85 |

<!--TRADE_LOG_END--> 
