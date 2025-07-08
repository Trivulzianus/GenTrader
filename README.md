# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 17:51:52**

| Metric | Value |
|---|---|
| **Total Value** | **$100,765.50** |
| Cash | $2,192.54 |
| Holdings Value | $98,572.97 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.44 | $2,094.41 | 70 |
| ADBE | 5 | $377.60 | $381.53 | $1,907.65 | 65 |
| AMD | 16 | $135.69 | $138.11 | $2,209.76 | 70 |
| AMZN | 10 | $221.61 | $220.41 | $2,204.10 | 65 |
| AVGO | 8 | $275.34 | $274.36 | $2,194.85 | 65 |
| AXP | 8 | $324.24 | $319.85 | $2,558.80 | 85 |
| BA | 10 | $212.43 | $218.62 | $2,186.21 | 70 |
| BAC | 51 | $48.61 | $47.23 | $2,408.74 | 75 |
| C | 28 | $86.61 | $86.27 | $2,415.56 | 75 |
| CAT | 6 | $397.86 | $394.67 | $2,367.99 | 65 |
| COST | 2 | $979.83 | $986.52 | $1,973.05 | 65 |
| CRM | 8 | $268.33 | $273.54 | $2,188.28 | 65 |
| CSCO | 33 | $68.36 | $68.62 | $2,264.46 | 70 |
| CVX | 17 | $147.07 | $152.75 | $2,596.75 | 85 |
| DIS | 17 | $122.85 | $122.08 | $2,075.44 | 65 |
| GOOGL | 12 | $179.60 | $174.06 | $2,088.70 | 65 |
| GS | 3 | $717.52 | $699.21 | $2,097.63 | 70 |
| HD | 6 | $372.64 | $366.94 | $2,201.64 | 65 |
| INTC | 88 | $22.35 | $23.59 | $2,076.36 | 65 |
| JNJ | 14 | $155.85 | $155.28 | $2,173.92 | 65 |
| JPM | 9 | $291.61 | $282.31 | $2,540.74 | 75 |
| KO | 29 | $71.03 | $70.33 | $2,039.71 | 65 |
| LLY | 2 | $776.66 | $781.78 | $1,563.56 | 65 |
| MA | 4 | $563.08 | $560.65 | $2,242.60 | 65 |
| META | 3 | $717.12 | $720.36 | $2,161.08 | 75 |
| MRK | 28 | $82.54 | $81.09 | $2,270.52 | 70 |
| MSFT | 5 | $498.84 | $496.10 | $2,480.50 | 75 |
| NFLX | 1 | $1,279.00 | $1,277.79 | $1,277.79 | 65 |
| NKE | 30 | $75.91 | $73.78 | $2,213.25 | 70 |
| NVDA | 17 | $157.07 | $159.79 | $2,716.43 | 85 |
| ORCL | 9 | $233.41 | $237.76 | $2,139.84 | 70 |
| PEP | 15 | $136.57 | $134.73 | $2,021.01 | 65 |
| PFE | 94 | $25.27 | $25.53 | $2,399.81 | 75 |
| PG | 13 | $160.77 | $158.23 | $2,056.99 | 65 |
| PYPL | 30 | $76.71 | $74.72 | $2,241.57 | 70 |
| QCOM | 15 | $161.62 | $159.84 | $2,397.53 | 75 |
| T | 73 | $28.54 | $28.41 | $2,073.92 | 65 |
| TGT | 20 | $104.90 | $101.58 | $2,031.50 | 65 |
| TSLA | 6 | $288.62 | $301.27 | $1,807.64 | 65 |
| UNH | 7 | $314.75 | $305.94 | $2,141.61 | 65 |
| UNP | 10 | $236.66 | $236.46 | $2,364.60 | 75 |
| V | 6 | $355.95 | $354.08 | $2,124.48 | 65 |
| WFC | 31 | $82.30 | $81.78 | $2,535.34 | 80 |
| WMT | 21 | $97.34 | $97.58 | $2,049.28 | 65 |
| XOM | 21 | $110.00 | $114.16 | $2,397.36 | 75 |

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
| 2025-07-08 17:51:41 | SELL | VZ | 47 | $43.06 | $-30.99 | 65 |
| 2025-07-08 17:51:41 | SELL | C | 3 | $86.25 | $-0.96 | 75 |
| 2025-07-08 17:51:41 | BUY | NVDA | 1 | $159.76 | N/A | 85 |
| 2025-07-08 17:51:41 | BUY | BAC | 1 | $47.24 | N/A | 75 |
| 2025-07-08 17:51:41 | BUY | INTC | 1 | $23.57 | N/A | 65 |
| 2025-07-08 17:51:41 | BUY | PFE | 7 | $25.52 | N/A | 75 |
| 2025-07-08 17:51:41 | BUY | WFC | 2 | $81.75 | N/A | 80 |
| 2025-07-08 17:51:41 | BUY | QCOM | 1 | $159.84 | N/A | 75 |
| 2025-07-08 17:51:41 | BUY | CVX | 1 | $152.75 | N/A | 85 |
| 2025-07-08 17:51:41 | BUY | T | 1 | $28.39 | N/A | 65 |
| 2025-07-08 17:39:36 | SELL | MRK | 1 | $81.13 | $-1.36 | 70 |
| 2025-07-08 17:39:36 | SELL | PYPL | 1 | $74.66 | $-1.98 | 70 |
| 2025-07-08 17:39:36 | SELL | CSCO | 1 | $68.54 | $0.17 | 70 |
| 2025-07-08 17:39:36 | SELL | CVX | 1 | $152.51 | $5.46 | 75 |
| 2025-07-08 17:39:36 | BUY | NVDA | 1 | $159.55 | N/A | 85 |
| 2025-07-08 17:39:36 | BUY | BAC | 1 | $47.31 | N/A | 75 |
| 2025-07-08 17:39:36 | BUY | INTC | 1 | $23.57 | N/A | 65 |
| 2025-07-08 17:39:36 | BUY | NKE | 2 | $73.79 | N/A | 70 |
| 2025-07-08 17:39:36 | BUY | C | 1 | $86.31 | N/A | 85 |
| 2025-07-08 17:25:32 | SELL | NVDA | 1 | $159.57 | $2.66 | 75 |
| 2025-07-08 17:25:32 | SELL | NKE | 2 | $73.86 | $-4.12 | 65 |
| 2025-07-08 17:25:32 | SELL | WMT | 3 | $97.97 | $1.64 | 65 |
| 2025-07-08 17:25:32 | BUY | INTC | 5 | $23.53 | N/A | 65 |
| 2025-07-08 17:25:32 | BUY | C | 4 | $86.25 | N/A | 85 |
| 2025-07-08 17:25:32 | BUY | CVX | 1 | $152.88 | N/A | 85 |

<!--TRADE_LOG_END--> 
