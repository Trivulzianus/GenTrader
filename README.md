# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 17:40:07**

| Metric | Value |
|---|---|
| **Total Value** | **$100,885.48** |
| Cash | $713.88 |
| Holdings Value | $100,171.60 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.12 | $2,091.20 | 65 |
| ADBE | 6 | $375.23 | $365.87 | $2,195.22 | 65 |
| AMD | 16 | $135.48 | $147.55 | $2,360.84 | 75 |
| AMZN | 11 | $221.92 | $225.95 | $2,485.45 | 75 |
| AVGO | 8 | $275.34 | $276.81 | $2,214.44 | 70 |
| AXP | 7 | $325.34 | $320.65 | $2,244.55 | 75 |
| BA | 10 | $212.67 | $229.61 | $2,296.10 | 70 |
| BAC | 47 | $48.71 | $46.99 | $2,208.76 | 70 |
| C | 27 | $86.54 | $87.32 | $2,357.64 | 75 |
| CAT | 6 | $397.74 | $404.57 | $2,427.42 | 85 |
| COST | 2 | $979.83 | $976.04 | $1,952.08 | 70 |
| CRM | 7 | $268.68 | $261.26 | $1,828.82 | 65 |
| CSCO | 30 | $68.49 | $67.85 | $2,035.50 | 65 |
| CVX | 16 | $146.79 | $151.85 | $2,429.60 | 75 |
| DIS | 18 | $122.80 | $120.46 | $2,168.24 | 70 |
| GOOGL | 14 | $179.69 | $181.25 | $2,537.57 | 85 |
| GS | 3 | $717.52 | $712.61 | $2,137.84 | 70 |
| HD | 6 | $372.64 | $368.45 | $2,210.73 | 70 |
| INTC | 86 | $22.37 | $23.26 | $2,000.35 | 65 |
| JNJ | 13 | $155.95 | $156.37 | $2,032.75 | 65 |
| JPM | 9 | $291.63 | $289.16 | $2,602.44 | 85 |
| KO | 29 | $71.03 | $69.39 | $2,012.45 | 65 |
| LLY | 3 | $781.32 | $797.46 | $2,392.38 | 75 |
| MA | 4 | $563.08 | $554.82 | $2,219.26 | 65 |
| META | 3 | $717.12 | $724.88 | $2,174.62 | 85 |
| MRK | 28 | $82.49 | $83.74 | $2,344.72 | 75 |
| MSFT | 5 | $498.84 | $502.81 | $2,514.03 | 85 |
| NFLX | 1 | $1,279.00 | $1,268.73 | $1,268.73 | 65 |
| NKE | 28 | $72.03 | $72.27 | $2,023.56 | 65 |
| NVDA | 14 | $156.62 | $165.17 | $2,312.44 | 70 |
| ORCL | 10 | $232.94 | $230.04 | $2,300.40 | 75 |
| PEP | 15 | $136.57 | $135.59 | $2,033.92 | 65 |
| PFE | 79 | $25.18 | $25.48 | $2,012.53 | 65 |
| PG | 13 | $160.78 | $153.77 | $1,999.01 | 65 |
| PYPL | 31 | $72.27 | $73.74 | $2,285.94 | 75 |
| QCOM | 14 | $153.83 | $154.48 | $2,162.72 | 70 |
| T | 74 | $27.10 | $27.16 | $2,009.47 | 65 |
| TGT | 20 | $104.94 | $104.70 | $2,094.00 | 70 |
| TSLA | 6 | $288.62 | $314.33 | $1,885.98 | 65 |
| UNH | 7 | $298.51 | $299.86 | $2,099.02 | 65 |
| UNP | 10 | $236.29 | $233.49 | $2,334.90 | 75 |
| V | 6 | $355.85 | $351.10 | $2,106.57 | 70 |
| VZ | 49 | $43.12 | $41.57 | $2,036.93 | 65 |
| WFC | 28 | $82.26 | $83.48 | $2,337.58 | 75 |
| WMT | 21 | $97.38 | $95.56 | $2,006.87 | 65 |
| XOM | 21 | $110.01 | $113.62 | $2,386.02 | 75 |

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
| 2025-07-14 17:40:02 | SELL | NKE | 1 | $72.27 | $0.23 | 65 |
| 2025-07-14 17:40:02 | SELL | PFE | 7 | $25.48 | $1.89 | 65 |
| 2025-07-14 17:40:02 | SELL | C | 4 | $87.31 | $2.67 | 75 |
| 2025-07-14 17:40:02 | SELL | CSCO | 2 | $67.84 | $-1.23 | 65 |
| 2025-07-14 17:40:02 | SELL | T | 1 | $27.16 | $0.05 | 65 |
| 2025-07-14 17:40:02 | BUY | GOOGL | 1 | $181.31 | N/A | 85 |
| 2025-07-14 17:40:02 | BUY | INTC | 4 | $23.25 | N/A | 65 |
| 2025-07-14 17:40:02 | BUY | PYPL | 3 | $73.75 | N/A | 75 |
| 2025-07-14 17:40:02 | BUY | WMT | 1 | $95.57 | N/A | 65 |
| 2025-07-14 17:40:02 | BUY | ORCL | 1 | $230.07 | N/A | 75 |
| 2025-07-14 17:26:00 | SELL | PYPL | 4 | $73.79 | $5.89 | 65 |
| 2025-07-14 17:26:00 | SELL | WMT | 1 | $95.60 | $-1.79 | 60 |
| 2025-07-14 17:26:00 | BUY | AMD | 1 | $146.83 | N/A | 75 |
| 2025-07-14 17:09:36 | SELL | NVDA | 2 | $165.10 | $14.84 | 70 |
| 2025-07-14 17:09:36 | SELL | INTC | 6 | $23.15 | $4.58 | 60 |
| 2025-07-14 17:09:36 | BUY | PYPL | 4 | $73.64 | N/A | 75 |
| 2025-07-14 17:09:36 | BUY | QCOM | 1 | $154.25 | N/A | 70 |
| 2025-07-14 17:09:36 | BUY | CSCO | 1 | $67.62 | N/A | 70 |
| 2025-07-14 16:56:14 | SELL | NKE | 3 | $72.29 | $0.69 | 65 |
| 2025-07-14 16:56:14 | SELL | CSCO | 1 | $67.55 | $-0.90 | 65 |
| 2025-07-14 16:56:14 | BUY | INTC | 7 | $23.15 | N/A | 65 |
| 2025-07-14 16:56:14 | BUY | MRK | 1 | $83.74 | N/A | 75 |
| 2025-07-14 16:43:44 | SELL | INTC | 7 | $23.15 | $5.33 | 60 |
| 2025-07-14 16:43:44 | SELL | PYPL | 1 | $73.69 | $1.51 | 65 |
| 2025-07-14 16:43:44 | SELL | PFE | 6 | $25.49 | $1.56 | 70 |

<!--TRADE_LOG_END--> 
