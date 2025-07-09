# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 18:11:11**

| Metric | Value |
|---|---|
| **Total Value** | **$100,938.41** |
| Cash | $1,739.67 |
| Holdings Value | $99,198.74 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.78 | $2,097.81 | 70 |
| ADBE | 5 | $377.60 | $372.90 | $1,864.50 | 65 |
| AMD | 15 | $135.39 | $139.42 | $2,091.30 | 70 |
| AMZN | 10 | $221.83 | $222.73 | $2,227.30 | 75 |
| AVGO | 8 | $275.34 | $278.26 | $2,226.08 | 70 |
| AXP | 7 | $325.28 | $319.05 | $2,233.32 | 65 |
| BA | 10 | $212.53 | $227.65 | $2,276.50 | 65 |
| BAC | 47 | $48.69 | $47.02 | $2,210.17 | 70 |
| C | 31 | $86.66 | $86.00 | $2,665.85 | 85 |
| CAT | 6 | $397.86 | $402.96 | $2,417.79 | 75 |
| COST | 2 | $979.83 | $974.37 | $1,948.73 | 65 |
| CRM | 8 | $268.33 | $270.32 | $2,162.60 | 65 |
| CSCO | 34 | $68.37 | $69.12 | $2,350.08 | 75 |
| CVX | 16 | $146.67 | $152.97 | $2,447.52 | 75 |
| DIS | 18 | $122.81 | $121.02 | $2,178.36 | 70 |
| GOOGL | 13 | $179.50 | $175.84 | $2,285.95 | 70 |
| GS | 3 | $717.52 | $700.09 | $2,100.26 | 70 |
| HD | 6 | $372.64 | $367.59 | $2,205.54 | 70 |
| INTC | 87 | $22.32 | $23.41 | $2,036.67 | 65 |
| JNJ | 13 | $155.89 | $155.63 | $2,023.19 | 65 |
| JPM | 9 | $291.61 | $283.69 | $2,553.19 | 75 |
| KO | 29 | $71.03 | $69.25 | $2,008.19 | 65 |
| LLY | 2 | $776.66 | $786.04 | $1,572.08 | 65 |
| MA | 4 | $563.08 | $562.80 | $2,251.22 | 65 |
| META | 3 | $717.12 | $734.60 | $2,203.79 | 85 |
| MRK | 28 | $82.45 | $83.94 | $2,350.46 | 75 |
| MSFT | 5 | $498.84 | $502.29 | $2,511.43 | 85 |
| NFLX | 1 | $1,279.00 | $1,279.13 | $1,279.13 | 65 |
| NKE | 28 | $76.05 | $73.80 | $2,066.40 | 65 |
| NVDA | 16 | $157.22 | $162.85 | $2,605.68 | 85 |
| ORCL | 9 | $233.31 | $235.32 | $2,117.88 | 70 |
| PEP | 15 | $136.57 | $133.86 | $2,007.90 | 65 |
| PFE | 80 | $25.21 | $25.45 | $2,036.40 | 65 |
| PG | 13 | $160.75 | $156.70 | $2,037.10 | 65 |
| PYPL | 28 | $76.83 | $74.79 | $2,094.12 | 65 |
| QCOM | 14 | $161.87 | $159.37 | $2,231.20 | 70 |
| T | 72 | $28.56 | $28.12 | $2,025.00 | 65 |
| TGT | 20 | $104.89 | $102.45 | $2,049.00 | 65 |
| TSLA | 6 | $288.62 | $296.13 | $1,776.78 | 65 |
| UNH | 7 | $314.75 | $303.09 | $2,121.63 | 65 |
| UNP | 9 | $236.60 | $237.72 | $2,139.48 | 75 |
| V | 6 | $355.95 | $356.05 | $2,136.30 | 70 |
| VZ | 48 | $43.15 | $42.67 | $2,048.40 | 65 |
| WFC | 32 | $82.25 | $81.92 | $2,621.60 | 85 |
| WMT | 21 | $97.35 | $96.86 | $2,034.06 | 65 |
| XOM | 20 | $109.83 | $113.54 | $2,270.80 | 75 |

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
| 2025-07-09 18:11:03 | SELL | PYPL | 3 | $74.79 | $-5.53 | 65 |
| 2025-07-09 18:11:03 | SELL | PFE | 6 | $25.45 | $1.38 | 65 |
| 2025-07-09 18:11:03 | SELL | NKE | 1 | $73.82 | $-2.15 | 65 |
| 2025-07-09 18:11:03 | BUY | WFC | 2 | $81.94 | N/A | 85 |
| 2025-07-09 17:51:26 | BUY | INTC | 1 | $23.35 | N/A | 65 |
| 2025-07-09 17:51:26 | BUY | PYPL | 1 | $74.97 | N/A | 75 |
| 2025-07-09 17:51:26 | BUY | NKE | 1 | $73.70 | N/A | 70 |
| 2025-07-09 17:51:26 | BUY | PFE | 1 | $25.45 | N/A | 70 |
| 2025-07-09 17:51:26 | BUY | WFC | 1 | $81.89 | N/A | 80 |
| 2025-07-09 17:51:26 | BUY | CSCO | 2 | $68.93 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
