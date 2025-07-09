# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 14:26:08**

| Metric | Value |
|---|---|
| **Total Value** | **$101,117.47** |
| Cash | $1,703.73 |
| Holdings Value | $99,413.74 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.66 | $2,096.60 | 70 |
| ADBE | 5 | $377.60 | $380.81 | $1,904.08 | 65 |
| AMD | 15 | $135.39 | $140.19 | $2,102.85 | 65 |
| AMZN | 10 | $221.61 | $223.14 | $2,231.40 | 75 |
| AVGO | 8 | $275.34 | $277.13 | $2,217.02 | 70 |
| AXP | 7 | $325.28 | $319.61 | $2,237.27 | 75 |
| BA | 10 | $212.43 | $224.19 | $2,241.95 | 70 |
| BAC | 47 | $48.71 | $47.09 | $2,213.47 | 70 |
| C | 27 | $86.71 | $86.33 | $2,331.04 | 75 |
| CAT | 6 | $397.86 | $401.00 | $2,406.00 | 70 |
| COST | 2 | $979.83 | $979.42 | $1,958.84 | 65 |
| CRM | 8 | $268.33 | $272.41 | $2,179.28 | 65 |
| CSCO | 34 | $68.35 | $68.89 | $2,342.09 | 75 |
| CVX | 15 | $146.26 | $152.89 | $2,293.35 | 70 |
| DIS | 18 | $122.80 | $121.69 | $2,190.42 | 70 |
| GOOGL | 13 | $179.50 | $178.81 | $2,324.47 | 75 |
| GS | 3 | $717.52 | $699.13 | $2,097.39 | 70 |
| HD | 6 | $372.64 | $366.84 | $2,201.04 | 70 |
| INTC | 87 | $22.33 | $23.25 | $2,023.17 | 65 |
| JNJ | 13 | $155.89 | $155.80 | $2,025.37 | 65 |
| JPM | 9 | $291.61 | $284.21 | $2,557.89 | 75 |
| KO | 29 | $71.03 | $69.73 | $2,022.32 | 65 |
| LLY | 2 | $776.66 | $789.65 | $1,579.30 | 70 |
| MA | 4 | $563.08 | $563.78 | $2,255.12 | 70 |
| META | 3 | $717.12 | $735.05 | $2,205.15 | 85 |
| MRK | 29 | $82.50 | $83.24 | $2,413.96 | 75 |
| MSFT | 5 | $498.84 | $504.36 | $2,521.79 | 85 |
| NFLX | 1 | $1,279.00 | $1,280.38 | $1,280.38 | 65 |
| NKE | 29 | $75.97 | $74.15 | $2,150.36 | 70 |
| NVDA | 16 | $157.22 | $163.34 | $2,613.52 | 85 |
| ORCL | 9 | $233.41 | $234.07 | $2,106.64 | 70 |
| PEP | 15 | $136.57 | $134.49 | $2,017.35 | 65 |
| PFE | 85 | $25.22 | $25.57 | $2,173.88 | 70 |
| PG | 13 | $160.77 | $157.45 | $2,046.85 | 65 |
| PYPL | 31 | $76.64 | $75.45 | $2,339.11 | 75 |
| QCOM | 15 | $161.64 | $160.03 | $2,400.53 | 75 |
| T | 72 | $28.56 | $28.23 | $2,032.22 | 65 |
| TGT | 20 | $104.89 | $102.52 | $2,050.30 | 65 |
| TSLA | 6 | $288.62 | $297.73 | $1,786.35 | 65 |
| UNH | 7 | $314.75 | $301.46 | $2,110.22 | 65 |
| UNP | 9 | $236.60 | $237.40 | $2,136.56 | 70 |
| V | 6 | $355.95 | $356.49 | $2,138.94 | 65 |
| VZ | 48 | $43.15 | $42.88 | $2,058.00 | 65 |
| WFC | 29 | $82.27 | $81.93 | $2,375.97 | 75 |
| WMT | 21 | $97.35 | $97.15 | $2,040.15 | 65 |
| XOM | 21 | $110.03 | $113.52 | $2,383.82 | 75 |

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
| 2025-07-09 13:46:32 | SELL | PYPL | 3 | $75.58 | $-3.20 | 65 |
| 2025-07-09 13:46:32 | SELL | WMT | 2 | $96.98 | $-0.67 | 65 |
| 2025-07-09 13:46:32 | SELL | PFE | 22 | $25.68 | $8.25 | 65 |

<!--TRADE_LOG_END--> 
