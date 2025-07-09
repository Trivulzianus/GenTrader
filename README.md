# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 17:39:24**

| Metric | Value |
|---|---|
| **Total Value** | **$100,825.88** |
| Cash | $1,869.88 |
| Holdings Value | $98,956.00 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $208.89 | $2,088.90 | 70 |
| ADBE | 5 | $377.60 | $371.37 | $1,856.83 | 65 |
| AMD | 15 | $135.39 | $138.65 | $2,079.75 | 70 |
| AMZN | 10 | $221.83 | $222.60 | $2,226.00 | 75 |
| AVGO | 8 | $275.34 | $277.92 | $2,223.36 | 70 |
| AXP | 7 | $325.28 | $318.50 | $2,229.50 | 70 |
| BA | 10 | $212.53 | $229.88 | $2,298.80 | 70 |
| BAC | 47 | $48.69 | $46.95 | $2,206.41 | 70 |
| C | 31 | $86.66 | $85.91 | $2,663.21 | 85 |
| CAT | 6 | $397.86 | $402.32 | $2,413.95 | 85 |
| COST | 2 | $979.83 | $976.62 | $1,953.24 | 65 |
| CRM | 8 | $268.33 | $269.95 | $2,159.64 | 65 |
| CSCO | 32 | $68.33 | $68.88 | $2,204.00 | 70 |
| CVX | 16 | $146.67 | $152.83 | $2,445.28 | 75 |
| DIS | 18 | $122.81 | $120.68 | $2,172.24 | 70 |
| GOOGL | 13 | $179.50 | $177.54 | $2,308.02 | 70 |
| GS | 3 | $717.52 | $698.03 | $2,094.11 | 70 |
| HD | 6 | $372.64 | $366.30 | $2,197.77 | 70 |
| INTC | 86 | $22.31 | $23.32 | $2,005.95 | 65 |
| JNJ | 13 | $155.89 | $155.26 | $2,018.41 | 65 |
| JPM | 9 | $291.61 | $283.44 | $2,550.93 | 75 |
| KO | 29 | $71.03 | $69.20 | $2,006.80 | 65 |
| LLY | 2 | $776.66 | $785.08 | $1,570.15 | 65 |
| MA | 4 | $563.08 | $562.14 | $2,248.56 | 65 |
| META | 3 | $717.12 | $734.55 | $2,203.65 | 85 |
| MRK | 28 | $82.45 | $83.78 | $2,345.70 | 75 |
| MSFT | 5 | $498.84 | $501.87 | $2,509.32 | 85 |
| NFLX | 1 | $1,279.00 | $1,277.36 | $1,277.36 | 65 |
| NKE | 28 | $76.06 | $73.70 | $2,063.60 | 65 |
| NVDA | 16 | $157.22 | $162.88 | $2,606.00 | 85 |
| ORCL | 9 | $233.31 | $235.00 | $2,115.05 | 75 |
| PEP | 15 | $136.57 | $133.62 | $2,004.30 | 65 |
| PFE | 85 | $25.22 | $25.37 | $2,156.46 | 70 |
| PG | 13 | $160.75 | $156.32 | $2,032.22 | 65 |
| PYPL | 30 | $76.69 | $74.88 | $2,246.25 | 70 |
| QCOM | 14 | $161.87 | $159.38 | $2,231.25 | 75 |
| T | 72 | $28.56 | $28.11 | $2,024.28 | 65 |
| TGT | 20 | $104.89 | $102.30 | $2,046.00 | 65 |
| TSLA | 6 | $288.62 | $294.98 | $1,769.85 | 65 |
| UNH | 7 | $314.75 | $302.04 | $2,114.26 | 65 |
| UNP | 9 | $236.60 | $237.34 | $2,136.03 | 70 |
| V | 6 | $355.95 | $355.26 | $2,131.59 | 65 |
| VZ | 48 | $43.15 | $42.62 | $2,045.76 | 65 |
| WFC | 29 | $82.28 | $81.86 | $2,373.80 | 75 |
| WMT | 21 | $97.35 | $96.86 | $2,034.06 | 65 |
| XOM | 20 | $109.83 | $113.37 | $2,267.40 | 75 |

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
| 2025-07-09 17:39:18 | SELL | PYPL | 1 | $74.88 | $-1.75 | 70 |
| 2025-07-09 17:39:18 | SELL | MRK | 1 | $83.78 | $1.29 | 75 |
| 2025-07-09 17:39:18 | SELL | CSCO | 1 | $68.88 | $0.53 | 70 |
| 2025-07-09 17:39:18 | SELL | CVX | 1 | $152.81 | $5.78 | 75 |
| 2025-07-09 17:39:18 | BUY | INTC | 6 | $23.33 | N/A | 65 |
| 2025-07-09 17:25:41 | SELL | BAC | 3 | $47.03 | $-4.69 | 70 |
| 2025-07-09 17:25:41 | SELL | NKE | 1 | $73.92 | $-2.06 | 65 |
| 2025-07-09 17:25:41 | BUY | PFE | 4 | $25.48 | N/A | 70 |
| 2025-07-09 17:25:41 | BUY | CSCO | 1 | $68.89 | N/A | 75 |
| 2025-07-09 17:25:41 | BUY | CVX | 1 | $153.27 | N/A | 85 |
| 2025-07-09 17:10:02 | SELL | INTC | 7 | $23.59 | $8.73 | 60 |
| 2025-07-09 17:10:02 | SELL | PFE | 6 | $25.44 | $1.30 | 65 |
| 2025-07-09 17:10:02 | SELL | CVX | 1 | $153.25 | $6.22 | 75 |
| 2025-07-09 17:10:02 | BUY | BAC | 4 | $46.78 | N/A | 75 |
| 2025-07-09 17:10:02 | BUY | NKE | 1 | $73.95 | N/A | 70 |
| 2025-07-09 17:10:02 | BUY | PYPL | 1 | $74.82 | N/A | 75 |
| 2025-07-09 17:10:02 | BUY | MRK | 1 | $83.86 | N/A | 80 |
| 2025-07-09 16:56:47 | SELL | PYPL | 1 | $74.84 | $-1.79 | 70 |
| 2025-07-09 16:56:47 | SELL | PFE | 5 | $25.44 | $1.02 | 70 |
| 2025-07-09 16:56:47 | SELL | ORCL | 1 | $234.93 | $1.46 | 65 |
| 2025-07-09 16:56:47 | BUY | BAC | 2 | $46.74 | N/A | 70 |
| 2025-07-09 16:56:47 | BUY | C | 3 | $85.75 | N/A | 85 |
| 2025-07-09 16:43:39 | SELL | NKE | 1 | $73.73 | $-2.24 | 65 |
| 2025-07-09 16:43:39 | SELL | MRK | 1 | $83.84 | $1.35 | 75 |
| 2025-07-09 16:43:39 | SELL | C | 3 | $85.68 | $-2.94 | 75 |

<!--TRADE_LOG_END--> 
