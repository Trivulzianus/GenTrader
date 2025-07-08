# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 19:24:31**

| Metric | Value |
|---|---|
| **Total Value** | **$100,653.61** |
| Cash | $284.76 |
| Holdings Value | $100,368.85 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.47 | $2,094.75 | 65 |
| ADBE | 5 | $377.60 | $381.13 | $1,905.67 | 65 |
| AMD | 16 | $135.69 | $137.65 | $2,202.40 | 70 |
| AMZN | 10 | $221.61 | $219.90 | $2,198.95 | 70 |
| AVGO | 8 | $275.34 | $272.30 | $2,178.41 | 65 |
| AXP | 8 | $324.24 | $318.39 | $2,547.12 | 85 |
| BA | 10 | $212.43 | $218.69 | $2,186.90 | 70 |
| BAC | 49 | $48.66 | $47.30 | $2,317.95 | 75 |
| C | 30 | $86.59 | $85.88 | $2,576.40 | 85 |
| CAT | 6 | $397.86 | $394.56 | $2,367.39 | 65 |
| COST | 2 | $979.83 | $987.52 | $1,975.05 | 65 |
| CRM | 8 | $268.33 | $272.78 | $2,182.24 | 65 |
| CSCO | 32 | $68.34 | $68.63 | $2,196.16 | 70 |
| CVX | 17 | $147.04 | $152.36 | $2,590.12 | 85 |
| DIS | 17 | $122.85 | $121.97 | $2,073.53 | 65 |
| GOOGL | 12 | $179.60 | $173.66 | $2,083.86 | 70 |
| GS | 3 | $717.52 | $697.51 | $2,092.53 | 70 |
| HD | 6 | $372.64 | $367.95 | $2,207.73 | 65 |
| INTC | 85 | $22.31 | $23.55 | $2,001.75 | 65 |
| JNJ | 13 | $155.89 | $155.43 | $2,020.59 | 65 |
| JPM | 9 | $291.61 | $282.44 | $2,541.96 | 85 |
| KO | 29 | $71.03 | $70.50 | $2,044.36 | 65 |
| LLY | 2 | $776.66 | $779.22 | $1,558.44 | 65 |
| MA | 4 | $563.08 | $561.34 | $2,245.36 | 65 |
| META | 3 | $717.12 | $718.18 | $2,154.55 | 80 |
| MRK | 29 | $82.50 | $81.26 | $2,356.54 | 75 |
| MSFT | 5 | $498.84 | $495.88 | $2,479.40 | 85 |
| NFLX | 1 | $1,279.00 | $1,270.20 | $1,270.20 | 65 |
| NKE | 29 | $75.97 | $73.86 | $2,141.94 | 70 |
| NVDA | 17 | $157.07 | $159.72 | $2,715.16 | 85 |
| ORCL | 9 | $233.41 | $233.81 | $2,104.29 | 75 |
| PEP | 15 | $136.57 | $135.19 | $2,027.85 | 65 |
| PFE | 90 | $25.26 | $25.59 | $2,302.82 | 75 |
| PG | 13 | $160.77 | $158.06 | $2,054.84 | 70 |
| PYPL | 31 | $76.65 | $74.83 | $2,319.58 | 75 |
| QCOM | 15 | $161.62 | $159.66 | $2,394.90 | 75 |
| T | 76 | $28.54 | $28.44 | $2,161.44 | 70 |
| TGT | 20 | $104.90 | $102.21 | $2,044.18 | 65 |
| TSLA | 6 | $288.62 | $297.69 | $1,786.17 | 65 |
| UNH | 7 | $314.75 | $305.78 | $2,140.46 | 65 |
| UNP | 10 | $236.66 | $237.06 | $2,370.60 | 75 |
| V | 6 | $355.95 | $354.01 | $2,124.06 | 65 |
| VZ | 47 | $43.16 | $43.13 | $2,027.34 | 65 |
| WFC | 29 | $82.33 | $81.65 | $2,367.85 | 75 |
| WMT | 23 | $97.35 | $97.57 | $2,244.11 | 75 |
| XOM | 21 | $110.03 | $113.86 | $2,390.95 | 75 |

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
| 2025-07-08 19:24:24 | SELL | BAC | 1 | $47.31 | $-1.33 | 75 |
| 2025-07-08 19:24:24 | SELL | INTC | 1 | $23.54 | $1.22 | 65 |
| 2025-07-08 19:24:24 | SELL | XOM | 2 | $113.85 | $6.97 | 75 |
| 2025-07-08 19:24:24 | SELL | T | 5 | $28.43 | $-0.52 | 70 |
| 2025-07-08 19:24:24 | BUY | PFE | 5 | $25.58 | N/A | 75 |
| 2025-07-08 19:24:24 | BUY | CVX | 1 | $152.33 | N/A | 85 |
| 2025-07-08 19:08:41 | SELL | PFE | 6 | $25.62 | $2.17 | 70 |
| 2025-07-08 19:08:41 | SELL | WFC | 1 | $81.80 | $-0.51 | 75 |
| 2025-07-08 19:08:41 | SELL | CSCO | 2 | $68.71 | $0.69 | 70 |
| 2025-07-08 19:08:41 | BUY | XOM | 2 | $113.96 | N/A | 85 |
| 2025-07-08 19:08:41 | BUY | C | 4 | $86.01 | N/A | 85 |
| 2025-07-08 19:08:41 | BUY | T | 5 | $28.43 | N/A | 75 |
| 2025-07-08 18:57:14 | SELL | XOM | 1 | $114.01 | $3.81 | 75 |
| 2025-07-08 18:57:14 | SELL | C | 2 | $85.92 | $-1.43 | 70 |
| 2025-07-08 18:57:14 | SELL | CVX | 1 | $152.49 | $5.44 | 75 |
| 2025-07-08 18:57:14 | BUY | WFC | 1 | $81.60 | N/A | 80 |
| 2025-07-08 18:57:14 | BUY | CSCO | 2 | $68.67 | N/A | 75 |
| 2025-07-08 18:57:14 | BUY | PFE | 6 | $25.62 | N/A | 75 |
| 2025-07-08 18:57:14 | BUY | T | 4 | $28.41 | N/A | 70 |
| 2025-07-08 18:45:11 | SELL | C | 2 | $85.97 | $-1.22 | 75 |
| 2025-07-08 18:45:11 | BUY | WMT | 2 | $97.38 | N/A | 75 |
| 2025-07-08 18:45:11 | BUY | CVX | 1 | $152.41 | N/A | 85 |
| 2025-07-08 18:27:39 | SELL | WMT | 2 | $97.54 | $0.37 | 65 |
| 2025-07-08 18:27:39 | SELL | XOM | 1 | $114.14 | $3.77 | 80 |
| 2025-07-08 18:27:39 | SELL | MRK | 1 | $81.34 | $-1.12 | 75 |

<!--TRADE_LOG_END--> 
