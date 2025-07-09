# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 19:36:24**

| Metric | Value |
|---|---|
| **Total Value** | **$100,963.36** |
| Cash | $1,948.53 |
| Holdings Value | $99,014.83 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.03 | $2,100.30 | 70 |
| ADBE | 5 | $377.60 | $373.72 | $1,868.60 | 65 |
| AMD | 15 | $135.39 | $138.80 | $2,082.00 | 65 |
| AMZN | 11 | $221.90 | $222.49 | $2,447.34 | 85 |
| AVGO | 8 | $275.34 | $277.50 | $2,220.00 | 65 |
| AXP | 7 | $325.28 | $318.00 | $2,226.00 | 75 |
| BA | 9 | $210.97 | $226.56 | $2,039.04 | 65 |
| BAC | 46 | $48.73 | $46.81 | $2,153.26 | 70 |
| C | 31 | $86.66 | $85.78 | $2,659.03 | 85 |
| CAT | 6 | $397.86 | $402.44 | $2,414.64 | 70 |
| COST | 2 | $979.83 | $979.23 | $1,958.46 | 65 |
| CRM | 8 | $268.33 | $270.98 | $2,167.84 | 65 |
| CSCO | 33 | $68.35 | $69.23 | $2,284.76 | 75 |
| CVX | 17 | $147.07 | $153.41 | $2,607.97 | 85 |
| DIS | 17 | $122.91 | $120.94 | $2,055.89 | 65 |
| GOOGL | 12 | $179.74 | $176.51 | $2,118.12 | 65 |
| GS | 3 | $717.52 | $697.48 | $2,092.43 | 70 |
| HD | 6 | $372.64 | $369.97 | $2,219.82 | 70 |
| INTC | 87 | $22.32 | $23.45 | $2,040.15 | 65 |
| JNJ | 13 | $155.89 | $155.77 | $2,025.01 | 65 |
| JPM | 9 | $291.61 | $282.88 | $2,545.92 | 75 |
| KO | 29 | $71.03 | $69.51 | $2,015.79 | 65 |
| LLY | 2 | $776.66 | $786.42 | $1,572.84 | 65 |
| MA | 4 | $563.08 | $563.97 | $2,255.88 | 65 |
| META | 3 | $717.12 | $733.91 | $2,201.73 | 85 |
| MRK | 28 | $82.45 | $83.90 | $2,349.20 | 75 |
| MSFT | 5 | $498.84 | $502.37 | $2,511.85 | 85 |
| NFLX | 1 | $1,279.00 | $1,283.69 | $1,283.69 | 65 |
| NKE | 28 | $76.02 | $73.72 | $2,064.30 | 65 |
| NVDA | 16 | $157.22 | $162.79 | $2,604.64 | 85 |
| ORCL | 9 | $233.31 | $234.87 | $2,113.83 | 65 |
| PEP | 15 | $136.57 | $134.34 | $2,015.10 | 65 |
| PFE | 86 | $25.22 | $25.48 | $2,191.71 | 70 |
| PG | 13 | $160.75 | $156.96 | $2,040.44 | 65 |
| PYPL | 30 | $76.68 | $74.84 | $2,245.14 | 70 |
| QCOM | 14 | $161.87 | $159.34 | $2,230.83 | 70 |
| T | 72 | $28.56 | $28.14 | $2,025.72 | 65 |
| TGT | 20 | $104.89 | $102.57 | $2,051.40 | 65 |
| TSLA | 6 | $288.62 | $297.10 | $1,782.60 | 65 |
| UNH | 7 | $314.75 | $303.19 | $2,122.33 | 65 |
| UNP | 9 | $236.60 | $237.34 | $2,136.01 | 75 |
| V | 6 | $355.95 | $357.09 | $2,142.54 | 65 |
| VZ | 48 | $43.15 | $42.70 | $2,049.84 | 65 |
| WFC | 29 | $82.30 | $81.73 | $2,370.32 | 75 |
| WMT | 21 | $97.35 | $96.87 | $2,034.27 | 65 |
| XOM | 20 | $109.83 | $113.81 | $2,276.27 | 75 |

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
| 2025-07-09 19:36:16 | SELL | GOOGL | 1 | $176.47 | $-3.02 | 65 |
| 2025-07-09 19:36:16 | SELL | NKE | 3 | $73.92 | $-5.69 | 65 |
| 2025-07-09 19:36:16 | BUY | CVX | 1 | $153.36 | N/A | 85 |
| 2025-07-09 19:24:35 | SELL | DIS | 1 | $120.95 | $-1.85 | 65 |
| 2025-07-09 19:24:35 | SELL | PYPL | 1 | $74.80 | $-1.82 | 70 |
| 2025-07-09 19:24:35 | SELL | CVX | 1 | $153.29 | $6.23 | 75 |
| 2025-07-09 19:24:35 | BUY | CSCO | 1 | $69.28 | N/A | 75 |
| 2025-07-09 19:08:38 | SELL | CSCO | 1 | $69.25 | $0.91 | 70 |
| 2025-07-09 19:08:38 | BUY | DIS | 1 | $120.63 | N/A | 70 |
| 2025-07-09 19:08:38 | BUY | NKE | 1 | $73.64 | N/A | 75 |
| 2025-07-09 19:08:38 | BUY | CVX | 1 | $153.20 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
