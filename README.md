# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 16:56:21**

| Metric | Value |
|---|---|
| **Total Value** | **$100,780.98** |
| Cash | $575.79 |
| Holdings Value | $100,205.19 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.97 | $2,089.75 | 65 |
| ADBE | 6 | $375.23 | $365.23 | $2,191.38 | 65 |
| AMD | 15 | $134.72 | $146.33 | $2,194.95 | 70 |
| AMZN | 11 | $221.92 | $225.78 | $2,483.58 | 75 |
| AVGO | 8 | $275.34 | $276.41 | $2,211.28 | 70 |
| AXP | 7 | $325.34 | $320.56 | $2,243.89 | 70 |
| BA | 10 | $212.67 | $229.59 | $2,295.90 | 70 |
| BAC | 47 | $48.71 | $46.87 | $2,202.66 | 70 |
| C | 31 | $86.64 | $87.03 | $2,697.93 | 85 |
| CAT | 6 | $397.74 | $404.01 | $2,424.06 | 65 |
| COST | 2 | $979.83 | $973.89 | $1,947.78 | 65 |
| CRM | 7 | $268.68 | $260.80 | $1,825.57 | 65 |
| CSCO | 31 | $68.48 | $67.56 | $2,094.36 | 65 |
| CVX | 16 | $146.79 | $151.69 | $2,427.12 | 75 |
| DIS | 18 | $122.80 | $120.33 | $2,165.85 | 65 |
| GOOGL | 13 | $179.57 | $180.96 | $2,352.41 | 70 |
| GS | 3 | $717.52 | $711.18 | $2,133.54 | 70 |
| HD | 6 | $372.64 | $367.77 | $2,206.64 | 65 |
| INTC | 88 | $22.38 | $23.14 | $2,036.76 | 65 |
| JNJ | 13 | $155.95 | $156.17 | $2,030.21 | 65 |
| JPM | 9 | $291.63 | $288.60 | $2,597.40 | 80 |
| KO | 29 | $71.03 | $69.64 | $2,019.42 | 65 |
| LLY | 3 | $781.32 | $798.39 | $2,395.17 | 75 |
| MA | 4 | $563.08 | $554.94 | $2,219.76 | 65 |
| META | 3 | $717.12 | $724.42 | $2,173.27 | 85 |
| MRK | 28 | $82.49 | $83.75 | $2,344.86 | 75 |
| MSFT | 5 | $498.84 | $502.48 | $2,512.38 | 75 |
| NFLX | 1 | $1,279.00 | $1,265.37 | $1,265.37 | 65 |
| NKE | 29 | $72.04 | $72.30 | $2,096.70 | 65 |
| NVDA | 16 | $157.68 | $165.03 | $2,640.52 | 85 |
| ORCL | 9 | $233.26 | $230.21 | $2,071.89 | 65 |
| PEP | 15 | $136.57 | $135.63 | $2,034.45 | 65 |
| PFE | 86 | $25.21 | $25.50 | $2,192.57 | 70 |
| PG | 13 | $160.78 | $153.84 | $1,999.92 | 65 |
| PYPL | 28 | $72.13 | $73.74 | $2,064.72 | 65 |
| QCOM | 13 | $153.79 | $154.17 | $2,004.21 | 65 |
| T | 75 | $27.10 | $27.16 | $2,037.00 | 65 |
| TGT | 20 | $104.94 | $104.81 | $2,096.10 | 65 |
| TSLA | 6 | $288.62 | $315.58 | $1,893.51 | 65 |
| UNH | 7 | $298.51 | $299.73 | $2,098.11 | 65 |
| UNP | 10 | $236.29 | $233.52 | $2,335.20 | 75 |
| V | 6 | $355.85 | $350.97 | $2,105.82 | 70 |
| VZ | 49 | $43.12 | $41.55 | $2,035.71 | 65 |
| WFC | 28 | $82.26 | $83.27 | $2,331.42 | 75 |
| WMT | 21 | $97.38 | $95.43 | $2,004.06 | 65 |
| XOM | 21 | $110.01 | $113.34 | $2,380.04 | 75 |

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
| 2025-07-14 16:56:14 | SELL | NKE | 3 | $72.29 | $0.69 | 65 |
| 2025-07-14 16:56:14 | SELL | CSCO | 1 | $67.55 | $-0.90 | 65 |
| 2025-07-14 16:56:14 | BUY | INTC | 7 | $23.15 | N/A | 65 |
| 2025-07-14 16:56:14 | BUY | MRK | 1 | $83.74 | N/A | 75 |
| 2025-07-14 16:43:44 | SELL | INTC | 7 | $23.15 | $5.33 | 60 |
| 2025-07-14 16:43:44 | SELL | PYPL | 1 | $73.69 | $1.51 | 65 |
| 2025-07-14 16:43:44 | SELL | PFE | 6 | $25.49 | $1.56 | 70 |
| 2025-07-14 16:43:44 | SELL | MRK | 1 | $83.53 | $1.04 | 70 |
| 2025-07-14 16:43:44 | BUY | WFC | 1 | $83.14 | N/A | 75 |
| 2025-07-14 16:43:44 | BUY | UNP | 1 | $233.19 | N/A | 75 |
| 2025-07-14 16:43:44 | BUY | CSCO | 1 | $67.48 | N/A | 70 |
| 2025-07-14 16:27:18 | SELL | WFC | 1 | $83.16 | $0.90 | 70 |
| 2025-07-14 16:27:18 | SELL | BA | 1 | $229.86 | $15.63 | 70 |
| 2025-07-14 16:27:18 | SELL | UNP | 1 | $232.96 | $-3.31 | 65 |
| 2025-07-14 16:27:18 | BUY | INTC | 1 | $23.12 | N/A | 65 |
| 2025-07-14 16:27:18 | BUY | PYPL | 1 | $73.61 | N/A | 70 |
| 2025-07-14 16:27:18 | BUY | MRK | 2 | $83.43 | N/A | 75 |
| 2025-07-14 16:27:18 | BUY | NKE | 3 | $72.23 | N/A | 75 |
| 2025-07-14 16:27:18 | BUY | PFE | 6 | $25.49 | N/A | 75 |
| 2025-07-14 16:09:59 | SELL | PYPL | 2 | $73.56 | $2.66 | 65 |
| 2025-07-14 16:09:59 | SELL | NKE | 2 | $72.37 | $0.60 | 65 |
| 2025-07-14 16:09:59 | SELL | CVX | 1 | $152.08 | $4.98 | 75 |
| 2025-07-14 16:09:59 | BUY | BAC | 1 | $46.73 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | AMD | 1 | $146.40 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | DIS | 1 | $120.31 | N/A | 70 |

<!--TRADE_LOG_END--> 
