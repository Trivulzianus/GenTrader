# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 14:40:37**

| Metric | Value |
|---|---|
| **Total Value** | **$100,872.74** |
| Cash | $1,746.18 |
| Holdings Value | $99,126.56 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.06 | $2,090.60 | 65 |
| ADBE | 5 | $377.60 | $378.98 | $1,894.90 | 65 |
| AMD | 15 | $135.39 | $139.10 | $2,086.50 | 70 |
| AMZN | 10 | $221.61 | $222.47 | $2,224.70 | 75 |
| AVGO | 8 | $275.34 | $275.37 | $2,202.96 | 70 |
| AXP | 7 | $325.28 | $318.68 | $2,230.76 | 70 |
| BA | 10 | $212.43 | $224.91 | $2,249.10 | 70 |
| BAC | 47 | $48.71 | $46.95 | $2,206.65 | 70 |
| C | 27 | $86.71 | $86.10 | $2,324.70 | 75 |
| CAT | 6 | $397.86 | $398.76 | $2,392.59 | 75 |
| COST | 2 | $979.83 | $976.70 | $1,953.40 | 65 |
| CRM | 8 | $268.33 | $272.06 | $2,176.48 | 65 |
| CSCO | 34 | $68.35 | $68.77 | $2,338.18 | 75 |
| CVX | 15 | $146.26 | $152.92 | $2,293.80 | 70 |
| DIS | 18 | $122.80 | $121.41 | $2,185.29 | 70 |
| GOOGL | 13 | $179.50 | $177.92 | $2,312.96 | 70 |
| GS | 3 | $717.52 | $696.23 | $2,088.69 | 70 |
| HD | 6 | $372.64 | $366.32 | $2,197.92 | 75 |
| INTC | 87 | $22.33 | $23.30 | $2,027.10 | 65 |
| JNJ | 13 | $155.89 | $155.68 | $2,023.84 | 65 |
| JPM | 9 | $291.61 | $283.52 | $2,551.68 | 75 |
| KO | 29 | $71.03 | $69.53 | $2,016.23 | 65 |
| LLY | 2 | $776.66 | $786.70 | $1,573.40 | 70 |
| MA | 4 | $563.08 | $563.71 | $2,254.84 | 65 |
| META | 3 | $717.12 | $734.11 | $2,202.32 | 85 |
| MRK | 29 | $82.50 | $83.15 | $2,411.35 | 75 |
| MSFT | 5 | $498.84 | $503.37 | $2,516.85 | 70 |
| NFLX | 1 | $1,279.00 | $1,277.12 | $1,277.12 | 65 |
| NKE | 29 | $75.97 | $74.07 | $2,148.02 | 70 |
| NVDA | 16 | $157.22 | $163.11 | $2,609.76 | 85 |
| ORCL | 9 | $233.41 | $233.72 | $2,103.48 | 70 |
| PEP | 15 | $136.57 | $134.10 | $2,011.57 | 65 |
| PFE | 80 | $25.20 | $25.50 | $2,040.40 | 65 |
| PG | 13 | $160.77 | $157.30 | $2,044.90 | 65 |
| PYPL | 30 | $76.71 | $74.78 | $2,243.40 | 70 |
| QCOM | 16 | $161.53 | $159.77 | $2,556.32 | 85 |
| T | 72 | $28.56 | $28.16 | $2,027.16 | 65 |
| TGT | 20 | $104.89 | $102.33 | $2,046.60 | 65 |
| TSLA | 6 | $288.62 | $296.38 | $1,778.28 | 65 |
| UNH | 7 | $314.75 | $300.61 | $2,104.30 | 65 |
| UNP | 9 | $236.60 | $236.99 | $2,132.91 | 75 |
| V | 6 | $355.95 | $355.57 | $2,133.42 | 70 |
| VZ | 48 | $43.15 | $42.73 | $2,050.80 | 65 |
| WFC | 29 | $82.27 | $81.70 | $2,369.30 | 75 |
| WMT | 21 | $97.35 | $96.93 | $2,035.53 | 65 |
| XOM | 21 | $110.03 | $113.59 | $2,385.49 | 80 |

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
| 2025-07-09 14:40:32 | SELL | PYPL | 1 | $74.77 | $-1.87 | 70 |
| 2025-07-09 14:40:32 | SELL | PFE | 5 | $25.50 | $1.39 | 65 |
| 2025-07-09 14:40:32 | BUY | QCOM | 1 | $159.82 | N/A | 85 |
| 2025-07-09 14:26:02 | SELL | BAC | 3 | $47.10 | $-4.51 | 70 |
| 2025-07-09 14:26:02 | SELL | AMD | 1 | $140.20 | $4.51 | 65 |
| 2025-07-09 14:26:02 | SELL | DIS | 1 | $121.69 | $-1.05 | 70 |
| 2025-07-09 14:26:02 | SELL | WMT | 1 | $97.18 | $-0.17 | 65 |
| 2025-07-09 14:26:02 | SELL | T | 1 | $28.23 | $-0.32 | 65 |
| 2025-07-09 14:26:02 | SELL | CVX | 2 | $152.88 | $11.69 | 70 |
| 2025-07-09 14:26:02 | BUY | NVDA | 2 | $163.39 | N/A | 85 |
| 2025-07-09 14:26:02 | BUY | PYPL | 2 | $75.46 | N/A | 75 |
| 2025-07-09 14:26:02 | BUY | PFE | 4 | $25.58 | N/A | 70 |
| 2025-07-09 14:08:18 | SELL | NVDA | 2 | $163.34 | $12.24 | 70 |
| 2025-07-09 14:08:18 | SELL | XOM | 1 | $113.63 | $3.43 | 75 |
| 2025-07-09 14:08:18 | SELL | QCOM | 1 | $160.52 | $-1.05 | 75 |
| 2025-07-09 14:08:18 | SELL | TGT | 1 | $103.17 | $-1.64 | 65 |
| 2025-07-09 14:08:18 | BUY | GOOGL | 1 | $178.32 | N/A | 75 |
| 2025-07-09 14:08:18 | BUY | INTC | 6 | $23.33 | N/A | 65 |
| 2025-07-09 14:08:18 | BUY | AMD | 1 | $137.82 | N/A | 70 |
| 2025-07-09 14:08:18 | BUY | BAC | 6 | $47.10 | N/A | 75 |
| 2025-07-09 14:08:18 | BUY | PYPL | 1 | $75.67 | N/A | 70 |
| 2025-07-09 14:08:18 | BUY | CSCO | 1 | $68.59 | N/A | 75 |
| 2025-07-09 14:08:18 | BUY | VZ | 1 | $42.69 | N/A | 65 |
| 2025-07-09 13:46:32 | SELL | BAC | 6 | $47.26 | $-8.24 | 65 |
| 2025-07-09 13:46:32 | SELL | INTC | 5 | $23.45 | $5.64 | 60 |

<!--TRADE_LOG_END--> 
