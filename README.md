# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 19:50:11**

| Metric | Value |
|---|---|
| **Total Value** | **$100,859.79** |
| Cash | $367.58 |
| Holdings Value | $100,492.21 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.73 | $2,087.30 | 65 |
| ADBE | 6 | $375.23 | $366.88 | $2,201.28 | 65 |
| AMD | 14 | $133.89 | $146.29 | $2,048.06 | 65 |
| AMZN | 10 | $221.60 | $225.33 | $2,253.30 | 70 |
| AVGO | 8 | $275.34 | $275.39 | $2,203.12 | 70 |
| AXP | 7 | $325.34 | $320.69 | $2,244.83 | 70 |
| BA | 10 | $212.67 | $231.25 | $2,312.45 | 75 |
| BAC | 53 | $48.51 | $47.02 | $2,492.15 | 80 |
| C | 30 | $86.60 | $87.34 | $2,620.27 | 85 |
| CAT | 6 | $397.74 | $406.13 | $2,436.78 | 70 |
| COST | 2 | $979.83 | $979.50 | $1,959.00 | 70 |
| CRM | 7 | $268.68 | $259.55 | $1,816.85 | 65 |
| CSCO | 31 | $68.47 | $67.70 | $2,098.70 | 65 |
| CVX | 16 | $146.79 | $151.65 | $2,426.40 | 80 |
| DIS | 18 | $122.79 | $120.13 | $2,162.28 | 70 |
| GOOGL | 14 | $179.74 | $181.73 | $2,544.22 | 85 |
| GS | 3 | $717.52 | $712.84 | $2,138.51 | 85 |
| HD | 6 | $372.64 | $370.17 | $2,220.99 | 65 |
| INTC | 87 | $22.38 | $23.27 | $2,024.34 | 65 |
| JNJ | 13 | $155.95 | $156.82 | $2,038.66 | 65 |
| JPM | 9 | $291.63 | $288.82 | $2,599.36 | 85 |
| KO | 29 | $71.03 | $69.41 | $2,012.84 | 65 |
| LLY | 3 | $781.32 | $798.89 | $2,396.67 | 70 |
| MA | 4 | $563.08 | $553.69 | $2,214.77 | 65 |
| META | 3 | $717.12 | $720.13 | $2,160.39 | 70 |
| MRK | 28 | $82.50 | $83.71 | $2,343.88 | 75 |
| MSFT | 5 | $498.84 | $503.18 | $2,515.88 | 70 |
| NFLX | 1 | $1,279.00 | $1,261.62 | $1,261.62 | 65 |
| NKE | 29 | $72.04 | $72.28 | $2,096.12 | 65 |
| NVDA | 16 | $157.66 | $164.22 | $2,627.49 | 85 |
| ORCL | 9 | $233.27 | $229.18 | $2,062.62 | 65 |
| PEP | 15 | $136.57 | $135.50 | $2,032.43 | 65 |
| PFE | 86 | $25.21 | $25.39 | $2,183.11 | 70 |
| PG | 14 | $160.31 | $154.09 | $2,157.33 | 70 |
| PYPL | 28 | $72.07 | $73.86 | $2,068.22 | 65 |
| QCOM | 14 | $153.83 | $154.20 | $2,158.80 | 65 |
| T | 75 | $27.10 | $27.14 | $2,035.13 | 65 |
| TGT | 20 | $104.94 | $104.66 | $2,093.10 | 65 |
| TSLA | 6 | $288.62 | $316.62 | $1,899.74 | 60 |
| UNH | 7 | $298.51 | $299.77 | $2,098.39 | 65 |
| UNP | 9 | $236.56 | $233.63 | $2,102.67 | 65 |
| V | 6 | $355.85 | $351.00 | $2,106.03 | 65 |
| VZ | 49 | $43.12 | $41.63 | $2,040.12 | 65 |
| WFC | 31 | $82.36 | $83.45 | $2,587.03 | 85 |
| WMT | 20 | $97.46 | $95.74 | $1,914.80 | 60 |
| XOM | 21 | $110.01 | $114.01 | $2,394.21 | 75 |

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
| 2025-07-14 19:50:04 | SELL | AMD | 1 | $146.39 | $11.67 | 65 |
| 2025-07-14 19:50:04 | SELL | NKE | 1 | $72.34 | $0.29 | 65 |
| 2025-07-14 19:50:04 | SELL | WMT | 1 | $95.75 | $-1.63 | 60 |
| 2025-07-14 19:50:04 | SELL | UNP | 1 | $233.79 | $-2.49 | 65 |
| 2025-07-14 19:50:04 | BUY | INTC | 7 | $23.27 | N/A | 65 |
| 2025-07-14 19:50:04 | BUY | BAC | 2 | $47.03 | N/A | 80 |
| 2025-07-14 19:50:04 | BUY | WFC | 1 | $83.43 | N/A | 85 |
| 2025-07-14 19:50:04 | BUY | PG | 1 | $154.15 | N/A | 70 |
| 2025-07-14 19:36:53 | SELL | BAC | 5 | $46.97 | $-7.26 | 75 |
| 2025-07-14 19:36:53 | SELL | PYPL | 1 | $73.89 | $1.75 | 65 |
| 2025-07-14 19:36:53 | SELL | CSCO | 1 | $67.72 | $-0.72 | 65 |
| 2025-07-14 19:36:53 | BUY | GOOGL | 2 | $181.69 | N/A | 85 |
| 2025-07-14 19:36:53 | BUY | AMD | 1 | $146.24 | N/A | 70 |
| 2025-07-14 19:36:53 | BUY | NKE | 2 | $72.30 | N/A | 70 |
| 2025-07-14 19:36:53 | BUY | DIS | 1 | $120.17 | N/A | 70 |
| 2025-07-14 19:36:53 | BUY | WFC | 2 | $83.28 | N/A | 80 |
| 2025-07-14 19:36:53 | BUY | UNP | 1 | $233.67 | N/A | 75 |
| 2025-07-14 19:25:06 | SELL | GOOGL | 2 | $181.36 | $3.33 | 70 |
| 2025-07-14 19:25:06 | SELL | AMZN | 1 | $225.28 | $3.35 | 70 |
| 2025-07-14 19:25:06 | SELL | DIS | 1 | $120.17 | $-2.63 | 65 |
| 2025-07-14 19:25:06 | SELL | MRK | 3 | $83.75 | $3.38 | 75 |
| 2025-07-14 19:25:06 | SELL | CVX | 1 | $152.24 | $5.13 | 75 |
| 2025-07-14 19:25:06 | BUY | BAC | 6 | $46.97 | N/A | 85 |
| 2025-07-14 19:25:06 | BUY | PYPL | 1 | $73.72 | N/A | 70 |
| 2025-07-14 19:25:06 | BUY | C | 4 | $87.22 | N/A | 85 |

<!--TRADE_LOG_END--> 
