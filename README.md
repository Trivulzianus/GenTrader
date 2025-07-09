# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 18:57:22**

| Metric | Value |
|---|---|
| **Total Value** | **$100,923.00** |
| Cash | $1,702.11 |
| Holdings Value | $99,220.89 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.95 | $2,099.50 | 70 |
| ADBE | 5 | $377.60 | $372.67 | $1,863.33 | 65 |
| AMD | 15 | $135.39 | $139.15 | $2,087.25 | 70 |
| AMZN | 11 | $221.90 | $222.49 | $2,447.39 | 85 |
| AVGO | 8 | $275.34 | $277.79 | $2,222.32 | 70 |
| AXP | 7 | $325.28 | $318.08 | $2,226.56 | 75 |
| BA | 9 | $210.97 | $226.89 | $2,042.01 | 65 |
| BAC | 46 | $48.73 | $46.92 | $2,158.32 | 70 |
| C | 31 | $86.66 | $85.76 | $2,658.56 | 85 |
| CAT | 6 | $397.86 | $402.94 | $2,417.64 | 75 |
| COST | 2 | $979.83 | $976.12 | $1,952.23 | 65 |
| CRM | 8 | $268.33 | $271.04 | $2,168.32 | 65 |
| CSCO | 33 | $68.35 | $69.27 | $2,285.91 | 75 |
| CVX | 16 | $146.68 | $153.04 | $2,448.64 | 80 |
| DIS | 17 | $122.93 | $120.84 | $2,054.26 | 70 |
| GOOGL | 13 | $179.49 | $176.69 | $2,296.97 | 75 |
| GS | 3 | $717.52 | $697.71 | $2,093.12 | 70 |
| HD | 6 | $372.64 | $369.87 | $2,219.22 | 70 |
| INTC | 87 | $22.32 | $23.41 | $2,036.67 | 65 |
| JNJ | 13 | $155.89 | $155.66 | $2,023.58 | 65 |
| JPM | 9 | $291.61 | $282.93 | $2,546.37 | 75 |
| KO | 29 | $71.03 | $69.29 | $2,009.41 | 65 |
| LLY | 2 | $776.66 | $785.39 | $1,570.78 | 65 |
| MA | 4 | $563.08 | $562.82 | $2,251.28 | 65 |
| META | 3 | $717.12 | $736.07 | $2,208.21 | 85 |
| MRK | 28 | $82.45 | $83.73 | $2,344.44 | 75 |
| MSFT | 5 | $498.84 | $502.70 | $2,513.50 | 70 |
| NFLX | 1 | $1,279.00 | $1,281.41 | $1,281.41 | 65 |
| NKE | 30 | $75.89 | $73.59 | $2,207.85 | 70 |
| NVDA | 16 | $157.22 | $162.99 | $2,607.84 | 85 |
| ORCL | 9 | $233.31 | $234.43 | $2,109.83 | 65 |
| PEP | 15 | $136.57 | $134.08 | $2,011.20 | 65 |
| PFE | 86 | $25.22 | $25.45 | $2,189.13 | 70 |
| PG | 13 | $160.75 | $157.08 | $2,042.04 | 65 |
| PYPL | 31 | $76.62 | $74.71 | $2,316.01 | 75 |
| QCOM | 14 | $161.87 | $159.34 | $2,230.76 | 70 |
| T | 72 | $28.56 | $28.16 | $2,027.53 | 65 |
| TGT | 20 | $104.89 | $102.27 | $2,045.40 | 65 |
| TSLA | 6 | $288.62 | $296.50 | $1,779.00 | 65 |
| UNH | 7 | $314.75 | $303.00 | $2,121.00 | 65 |
| UNP | 9 | $236.60 | $237.34 | $2,136.06 | 75 |
| V | 6 | $355.95 | $356.54 | $2,139.24 | 70 |
| VZ | 48 | $43.15 | $42.73 | $2,051.28 | 65 |
| WFC | 29 | $82.30 | $81.78 | $2,371.62 | 75 |
| WMT | 21 | $97.35 | $96.91 | $2,035.11 | 65 |
| XOM | 20 | $109.83 | $113.64 | $2,272.80 | 75 |

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
| 2025-07-09 18:57:16 | SELL | INTC | 1 | $23.40 | $1.07 | 65 |
| 2025-07-09 18:57:16 | SELL | PFE | 1 | $25.44 | $0.22 | 70 |
| 2025-07-09 18:57:16 | SELL | T | 1 | $28.15 | $-0.40 | 65 |
| 2025-07-09 18:57:16 | BUY | BAC | 2 | $46.92 | N/A | 70 |
| 2025-07-09 18:57:16 | BUY | CSCO | 2 | $69.26 | N/A | 75 |
| 2025-07-09 18:57:16 | BUY | CVX | 1 | $153.03 | N/A | 80 |
| 2025-07-09 18:45:21 | SELL | DIS | 1 | $120.70 | $-2.11 | 65 |
| 2025-07-09 18:45:21 | SELL | WFC | 1 | $81.69 | $-0.59 | 75 |
| 2025-07-09 18:45:21 | SELL | BA | 1 | $226.55 | $14.02 | 65 |
| 2025-07-09 18:45:21 | BUY | AMZN | 1 | $222.52 | N/A | 85 |
| 2025-07-09 18:45:21 | BUY | GOOGL | 1 | $176.15 | N/A | 75 |
| 2025-07-09 18:45:21 | BUY | PYPL | 2 | $74.62 | N/A | 75 |
| 2025-07-09 18:45:21 | BUY | CSCO | 1 | $69.21 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
