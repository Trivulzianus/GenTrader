# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 19:08:44**

| Metric | Value |
|---|---|
| **Total Value** | **$100,910.25** |
| Cash | $1,423.90 |
| Holdings Value | $99,486.34 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.76 | $2,097.61 | 65 |
| ADBE | 5 | $377.60 | $373.38 | $1,866.91 | 65 |
| AMD | 15 | $135.39 | $139.12 | $2,086.80 | 65 |
| AMZN | 11 | $221.90 | $222.57 | $2,448.27 | 75 |
| AVGO | 8 | $275.34 | $277.97 | $2,223.73 | 70 |
| AXP | 7 | $325.28 | $318.03 | $2,226.19 | 75 |
| BA | 9 | $210.97 | $226.52 | $2,038.68 | 65 |
| BAC | 46 | $48.73 | $46.89 | $2,156.94 | 70 |
| C | 31 | $86.66 | $85.78 | $2,659.03 | 85 |
| CAT | 6 | $397.86 | $402.69 | $2,416.11 | 75 |
| COST | 2 | $979.83 | $976.57 | $1,953.13 | 65 |
| CRM | 8 | $268.33 | $270.85 | $2,166.84 | 65 |
| CSCO | 32 | $68.32 | $69.25 | $2,216.16 | 70 |
| CVX | 17 | $147.06 | $153.19 | $2,604.32 | 85 |
| DIS | 18 | $122.80 | $120.63 | $2,171.34 | 70 |
| GOOGL | 13 | $179.49 | $176.41 | $2,293.33 | 75 |
| GS | 3 | $717.52 | $697.47 | $2,092.41 | 70 |
| HD | 6 | $372.64 | $369.10 | $2,214.60 | 70 |
| INTC | 87 | $22.32 | $23.43 | $2,037.98 | 65 |
| JNJ | 13 | $155.89 | $155.54 | $2,022.02 | 65 |
| JPM | 9 | $291.61 | $282.90 | $2,546.14 | 75 |
| KO | 29 | $71.03 | $69.36 | $2,011.58 | 65 |
| LLY | 2 | $776.66 | $785.33 | $1,570.66 | 65 |
| MA | 4 | $563.08 | $562.92 | $2,251.68 | 65 |
| META | 3 | $717.12 | $735.50 | $2,206.50 | 85 |
| MRK | 28 | $82.45 | $83.64 | $2,341.92 | 75 |
| MSFT | 5 | $498.84 | $502.60 | $2,513.00 | 70 |
| NFLX | 1 | $1,279.00 | $1,282.47 | $1,282.47 | 65 |
| NKE | 31 | $75.82 | $73.66 | $2,283.30 | 75 |
| NVDA | 16 | $157.22 | $162.78 | $2,604.48 | 85 |
| ORCL | 9 | $233.31 | $234.26 | $2,108.34 | 65 |
| PEP | 15 | $136.57 | $134.23 | $2,013.40 | 65 |
| PFE | 86 | $25.22 | $25.43 | $2,187.04 | 70 |
| PG | 13 | $160.75 | $157.16 | $2,043.14 | 65 |
| PYPL | 31 | $76.62 | $74.73 | $2,316.78 | 75 |
| QCOM | 14 | $161.87 | $159.19 | $2,228.60 | 75 |
| T | 72 | $28.56 | $28.18 | $2,029.32 | 65 |
| TGT | 20 | $104.89 | $102.41 | $2,048.12 | 65 |
| TSLA | 6 | $288.62 | $296.80 | $1,780.80 | 65 |
| UNH | 7 | $314.75 | $302.99 | $2,120.89 | 65 |
| UNP | 9 | $236.60 | $237.50 | $2,137.55 | 75 |
| V | 6 | $355.95 | $356.32 | $2,137.92 | 65 |
| VZ | 48 | $43.15 | $42.72 | $2,050.56 | 65 |
| WFC | 29 | $82.30 | $81.81 | $2,372.35 | 75 |
| WMT | 21 | $97.35 | $96.81 | $2,032.91 | 65 |
| XOM | 20 | $109.83 | $113.72 | $2,274.50 | 75 |

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
| 2025-07-09 18:27:27 | SELL | BAC | 3 | $46.96 | $-5.20 | 65 |
| 2025-07-09 18:27:27 | SELL | WFC | 2 | $81.72 | $-1.05 | 75 |
| 2025-07-09 18:27:27 | SELL | CSCO | 4 | $69.18 | $3.26 | 65 |
| 2025-07-09 18:27:27 | SELL | CVX | 1 | $152.91 | $6.24 | 70 |
| 2025-07-09 18:27:27 | BUY | INTC | 1 | $23.33 | N/A | 65 |
| 2025-07-09 18:27:27 | BUY | NKE | 2 | $73.62 | N/A | 70 |
| 2025-07-09 18:27:27 | BUY | PYPL | 1 | $74.72 | N/A | 70 |

<!--TRADE_LOG_END--> 
