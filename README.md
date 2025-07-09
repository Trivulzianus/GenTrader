# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 18:27:36**

| Metric | Value |
|---|---|
| **Total Value** | **$100,855.57** |
| Cash | $2,198.70 |
| Holdings Value | $98,656.87 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.65 | $2,096.51 | 65 |
| ADBE | 5 | $377.60 | $372.09 | $1,860.45 | 65 |
| AMD | 15 | $135.39 | $138.78 | $2,081.70 | 65 |
| AMZN | 10 | $221.83 | $222.53 | $2,225.30 | 75 |
| AVGO | 8 | $275.34 | $277.85 | $2,222.80 | 70 |
| AXP | 7 | $325.28 | $318.52 | $2,229.64 | 65 |
| BA | 10 | $212.53 | $227.36 | $2,273.60 | 70 |
| BAC | 44 | $48.81 | $46.95 | $2,065.58 | 65 |
| C | 31 | $86.66 | $85.78 | $2,659.03 | 85 |
| CAT | 6 | $397.86 | $402.96 | $2,417.76 | 75 |
| COST | 2 | $979.83 | $974.79 | $1,949.58 | 65 |
| CRM | 8 | $268.33 | $270.58 | $2,164.64 | 65 |
| CSCO | 30 | $68.26 | $69.18 | $2,075.40 | 65 |
| CVX | 15 | $146.26 | $152.90 | $2,293.50 | 70 |
| DIS | 18 | $122.81 | $120.85 | $2,175.30 | 70 |
| GOOGL | 12 | $179.77 | $176.28 | $2,115.36 | 65 |
| GS | 3 | $717.52 | $698.28 | $2,094.84 | 70 |
| HD | 6 | $372.64 | $369.54 | $2,217.24 | 70 |
| INTC | 88 | $22.33 | $23.34 | $2,053.48 | 65 |
| JNJ | 13 | $155.89 | $155.49 | $2,021.37 | 65 |
| JPM | 9 | $291.61 | $283.06 | $2,547.54 | 75 |
| KO | 29 | $71.03 | $69.25 | $2,008.39 | 65 |
| LLY | 2 | $776.66 | $785.67 | $1,571.34 | 65 |
| MA | 4 | $563.08 | $562.31 | $2,249.24 | 65 |
| META | 3 | $717.12 | $735.00 | $2,205.01 | 85 |
| MRK | 28 | $82.45 | $83.72 | $2,344.02 | 75 |
| MSFT | 5 | $498.84 | $503.03 | $2,515.15 | 85 |
| NFLX | 1 | $1,279.00 | $1,279.93 | $1,279.93 | 65 |
| NKE | 30 | $75.89 | $73.61 | $2,208.45 | 70 |
| NVDA | 16 | $157.22 | $162.85 | $2,605.59 | 85 |
| ORCL | 9 | $233.31 | $235.19 | $2,116.66 | 65 |
| PEP | 15 | $136.57 | $133.81 | $2,007.10 | 65 |
| PFE | 87 | $25.22 | $25.39 | $2,209.36 | 70 |
| PG | 13 | $160.75 | $156.81 | $2,038.47 | 65 |
| PYPL | 29 | $76.76 | $74.72 | $2,166.88 | 70 |
| QCOM | 14 | $161.87 | $159.12 | $2,227.69 | 70 |
| T | 73 | $28.55 | $28.13 | $2,053.60 | 65 |
| TGT | 20 | $104.89 | $102.17 | $2,043.40 | 65 |
| TSLA | 6 | $288.62 | $296.63 | $1,779.81 | 65 |
| UNH | 7 | $314.75 | $301.72 | $2,112.04 | 65 |
| UNP | 9 | $236.60 | $237.28 | $2,135.52 | 65 |
| V | 6 | $355.95 | $355.93 | $2,135.58 | 65 |
| VZ | 48 | $43.15 | $42.66 | $2,047.68 | 65 |
| WFC | 30 | $82.28 | $81.72 | $2,451.75 | 75 |
| WMT | 21 | $97.35 | $96.86 | $2,033.96 | 65 |
| XOM | 20 | $109.83 | $113.48 | $2,269.65 | 75 |

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
| 2025-07-09 18:27:27 | SELL | GOOGL | 1 | $176.27 | $-3.23 | 65 |
| 2025-07-09 18:27:27 | SELL | BAC | 3 | $46.96 | $-5.20 | 65 |
| 2025-07-09 18:27:27 | SELL | WFC | 2 | $81.72 | $-1.05 | 75 |
| 2025-07-09 18:27:27 | SELL | CSCO | 4 | $69.18 | $3.26 | 65 |
| 2025-07-09 18:27:27 | SELL | CVX | 1 | $152.91 | $6.24 | 70 |
| 2025-07-09 18:27:27 | BUY | INTC | 1 | $23.33 | N/A | 65 |
| 2025-07-09 18:27:27 | BUY | NKE | 2 | $73.62 | N/A | 70 |
| 2025-07-09 18:27:27 | BUY | PYPL | 1 | $74.72 | N/A | 70 |
| 2025-07-09 18:27:27 | BUY | PFE | 7 | $25.39 | N/A | 70 |
| 2025-07-09 18:27:27 | BUY | T | 1 | $28.14 | N/A | 65 |
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

<!--TRADE_LOG_END--> 
