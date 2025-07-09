# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 14:52:46**

| Metric | Value |
|---|---|
| **Total Value** | **$100,730.47** |
| Cash | $1,906.21 |
| Holdings Value | $98,824.26 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $208.11 | $2,081.10 | 65 |
| ADBE | 5 | $377.60 | $377.64 | $1,888.22 | 65 |
| AMD | 15 | $135.39 | $138.42 | $2,076.28 | 65 |
| AMZN | 11 | $221.61 | $221.57 | $2,437.27 | 85 |
| AVGO | 8 | $275.34 | $274.73 | $2,197.83 | 70 |
| AXP | 7 | $325.28 | $318.30 | $2,228.07 | 65 |
| BA | 10 | $212.43 | $224.94 | $2,249.40 | 70 |
| BAC | 47 | $48.71 | $46.88 | $2,203.59 | 70 |
| C | 26 | $86.74 | $85.95 | $2,234.83 | 70 |
| CAT | 6 | $397.86 | $399.29 | $2,395.74 | 70 |
| COST | 2 | $979.83 | $976.73 | $1,953.45 | 65 |
| CRM | 8 | $268.33 | $271.25 | $2,170.04 | 65 |
| CSCO | 30 | $68.31 | $68.64 | $2,059.20 | 65 |
| CVX | 15 | $146.26 | $152.87 | $2,293.05 | 70 |
| DIS | 19 | $122.72 | $121.28 | $2,304.32 | 75 |
| GOOGL | 13 | $179.50 | $177.43 | $2,306.59 | 70 |
| GS | 3 | $717.52 | $696.25 | $2,088.75 | 70 |
| HD | 6 | $372.64 | $366.31 | $2,197.86 | 70 |
| INTC | 81 | $22.25 | $23.30 | $1,886.90 | 60 |
| JNJ | 13 | $155.89 | $155.56 | $2,022.28 | 65 |
| JPM | 9 | $291.61 | $283.76 | $2,553.88 | 75 |
| KO | 29 | $71.03 | $69.35 | $2,011.15 | 65 |
| LLY | 2 | $776.66 | $785.43 | $1,570.87 | 75 |
| MA | 4 | $563.08 | $562.67 | $2,250.68 | 65 |
| META | 3 | $717.12 | $730.47 | $2,191.41 | 85 |
| MRK | 29 | $82.50 | $83.39 | $2,418.31 | 75 |
| MSFT | 5 | $498.84 | $502.45 | $2,512.27 | 85 |
| NFLX | 1 | $1,279.00 | $1,277.24 | $1,277.24 | 65 |
| NKE | 29 | $75.97 | $73.94 | $2,144.26 | 70 |
| NVDA | 16 | $157.22 | $162.82 | $2,605.12 | 85 |
| ORCL | 9 | $233.41 | $233.48 | $2,101.32 | 65 |
| PEP | 15 | $136.57 | $133.42 | $2,001.30 | 65 |
| PFE | 85 | $25.22 | $25.45 | $2,163.67 | 70 |
| PG | 13 | $160.77 | $156.94 | $2,040.28 | 65 |
| PYPL | 31 | $76.64 | $74.63 | $2,313.53 | 75 |
| QCOM | 14 | $161.87 | $159.12 | $2,227.71 | 70 |
| T | 72 | $28.56 | $28.20 | $2,030.76 | 65 |
| TGT | 20 | $104.89 | $102.15 | $2,042.93 | 65 |
| TSLA | 6 | $288.62 | $295.31 | $1,771.88 | 65 |
| UNH | 7 | $314.75 | $299.75 | $2,098.25 | 70 |
| UNP | 9 | $236.60 | $236.65 | $2,129.81 | 75 |
| V | 6 | $355.95 | $355.15 | $2,130.93 | 70 |
| VZ | 48 | $43.15 | $42.77 | $2,052.72 | 65 |
| WFC | 29 | $82.27 | $81.84 | $2,373.36 | 75 |
| WMT | 21 | $97.35 | $96.93 | $2,035.53 | 65 |
| XOM | 22 | $110.20 | $113.65 | $2,500.30 | 80 |

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
| 2025-07-09 14:52:38 | SELL | INTC | 6 | $23.30 | $5.84 | 60 |
| 2025-07-09 14:52:38 | SELL | C | 1 | $85.94 | $-0.77 | 70 |
| 2025-07-09 14:52:38 | SELL | QCOM | 2 | $159.13 | $-4.79 | 70 |
| 2025-07-09 14:52:38 | SELL | CSCO | 4 | $68.63 | $1.11 | 65 |
| 2025-07-09 14:52:38 | BUY | AMZN | 1 | $221.62 | N/A | 85 |
| 2025-07-09 14:52:38 | BUY | XOM | 1 | $113.65 | N/A | 80 |
| 2025-07-09 14:52:38 | BUY | DIS | 1 | $121.29 | N/A | 75 |
| 2025-07-09 14:52:38 | BUY | PYPL | 1 | $74.64 | N/A | 75 |
| 2025-07-09 14:52:38 | BUY | PFE | 5 | $25.45 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
