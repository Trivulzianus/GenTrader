# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 18:56:38**

| Metric | Value |
|---|---|
| **Total Value** | **$101,435.93** |
| Cash | $1,925.44 |
| Holdings Value | $99,510.49 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $213.07 | $2,130.70 | 65 |
| ADBE | 5 | $377.60 | $372.77 | $1,863.85 | 65 |
| AMD | 16 | $135.55 | $143.51 | $2,296.16 | 75 |
| AMZN | 11 | $221.97 | $222.16 | $2,443.70 | 75 |
| AVGO | 8 | $275.34 | $275.46 | $2,203.68 | 70 |
| AXP | 7 | $325.28 | $324.69 | $2,272.80 | 75 |
| BA | 10 | $212.37 | $225.22 | $2,252.16 | 70 |
| BAC | 47 | $48.68 | $46.85 | $2,201.95 | 70 |
| C | 30 | $86.80 | $86.66 | $2,599.65 | 85 |
| CAT | 6 | $397.86 | $408.34 | $2,450.04 | 75 |
| COST | 2 | $979.83 | $977.76 | $1,955.52 | 65 |
| CRM | 7 | $268.68 | $265.71 | $1,859.97 | 65 |
| CSCO | 33 | $68.37 | $68.71 | $2,267.59 | 75 |
| CVX | 17 | $147.15 | $153.81 | $2,614.77 | 85 |
| DIS | 18 | $122.80 | $121.06 | $2,178.99 | 70 |
| GOOGL | 13 | $179.61 | $177.37 | $2,305.74 | 70 |
| GS | 3 | $717.52 | $708.06 | $2,124.18 | 75 |
| HD | 6 | $372.64 | $375.90 | $2,255.43 | 65 |
| INTC | 84 | $22.27 | $23.89 | $2,006.34 | 65 |
| JNJ | 13 | $155.89 | $157.40 | $2,046.20 | 65 |
| JPM | 9 | $291.61 | $287.66 | $2,588.94 | 85 |
| KO | 29 | $71.03 | $69.62 | $2,018.98 | 65 |
| LLY | 2 | $776.66 | $792.40 | $1,584.80 | 65 |
| MA | 4 | $563.08 | $563.46 | $2,253.84 | 65 |
| META | 3 | $717.12 | $724.80 | $2,174.40 | 85 |
| MRK | 28 | $82.46 | $84.47 | $2,365.02 | 75 |
| MSFT | 5 | $498.84 | $501.76 | $2,508.80 | 75 |
| NFLX | 1 | $1,279.00 | $1,252.06 | $1,252.06 | 65 |
| NKE | 28 | $75.87 | $74.57 | $2,087.96 | 65 |
| NVDA | 14 | $156.60 | $163.81 | $2,293.41 | 70 |
| ORCL | 9 | $233.31 | $236.83 | $2,131.44 | 75 |
| PEP | 15 | $136.57 | $135.98 | $2,039.70 | 65 |
| PFE | 79 | $25.13 | $25.80 | $2,038.60 | 65 |
| PG | 13 | $160.78 | $158.62 | $2,062.06 | 65 |
| PYPL | 30 | $76.66 | $75.73 | $2,271.90 | 75 |
| QCOM | 15 | $161.72 | $159.45 | $2,391.75 | 75 |
| T | 73 | $28.55 | $27.66 | $2,019.54 | 65 |
| TGT | 20 | $104.92 | $105.54 | $2,110.80 | 65 |
| TSLA | 6 | $288.62 | $309.06 | $1,854.33 | 65 |
| UNH | 6 | $298.34 | $301.37 | $1,808.22 | 65 |
| UNP | 9 | $236.20 | $237.78 | $2,140.02 | 75 |
| V | 6 | $355.85 | $356.13 | $2,136.81 | 65 |
| VZ | 48 | $43.15 | $42.02 | $2,016.72 | 65 |
| WFC | 32 | $82.30 | $82.14 | $2,628.32 | 85 |
| WMT | 21 | $97.36 | $95.06 | $1,996.26 | 65 |
| XOM | 21 | $109.91 | $114.59 | $2,406.39 | 80 |

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
| 2025-07-10 18:56:32 | SELL | BAC | 2 | $46.85 | $-3.51 | 70 |
| 2025-07-10 18:56:32 | SELL | NKE | 1 | $74.57 | $-1.25 | 65 |
| 2025-07-10 18:56:32 | SELL | PFE | 5 | $25.81 | $3.15 | 65 |
| 2025-07-10 18:56:32 | SELL | QCOM | 1 | $159.48 | $-2.10 | 75 |
| 2025-07-10 18:56:32 | BUY | C | 1 | $86.67 | N/A | 85 |
| 2025-07-10 18:56:32 | BUY | WFC | 1 | $82.15 | N/A | 85 |
| 2025-07-10 18:56:32 | BUY | CSCO | 3 | $68.71 | N/A | 75 |
| 2025-07-10 18:44:41 | SELL | NVDA | 2 | $163.76 | $12.54 | 70 |
| 2025-07-10 18:44:41 | SELL | AMD | 2 | $143.91 | $14.87 | 70 |
| 2025-07-10 18:44:41 | SELL | C | 1 | $86.80 | $-0.01 | 80 |
| 2025-07-10 18:44:41 | SELL | CSCO | 2 | $68.75 | $0.78 | 65 |
| 2025-07-10 18:44:41 | BUY | INTC | 6 | $23.95 | N/A | 65 |
| 2025-07-10 18:44:41 | BUY | PFE | 6 | $25.85 | N/A | 70 |
| 2025-07-10 18:44:41 | BUY | NKE | 2 | $74.89 | N/A | 70 |
| 2025-07-10 18:44:41 | BUY | QCOM | 1 | $159.70 | N/A | 85 |
| 2025-07-10 18:27:27 | SELL | NKE | 2 | $75.06 | $-1.55 | 65 |
| 2025-07-10 18:27:27 | SELL | INTC | 6 | $23.91 | $9.83 | 60 |
| 2025-07-10 18:27:27 | SELL | PFE | 12 | $25.90 | $8.03 | 65 |
| 2025-07-10 18:27:27 | SELL | CSCO | 1 | $68.85 | $0.47 | 70 |
| 2025-07-10 18:27:27 | SELL | QCOM | 1 | $159.75 | $-1.83 | 75 |
| 2025-07-10 18:27:27 | BUY | NVDA | 2 | $163.74 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | PG | 1 | $159.16 | N/A | 70 |
| 2025-07-10 18:27:27 | BUY | WFC | 3 | $82.21 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | CVX | 1 | $153.99 | N/A | 85 |
| 2025-07-10 18:27:27 | BUY | TGT | 1 | $106.22 | N/A | 70 |

<!--TRADE_LOG_END--> 
