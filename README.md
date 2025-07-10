# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 14:09:22**

| Metric | Value |
|---|---|
| **Total Value** | **$101,182.69** |
| Cash | $1,715.34 |
| Holdings Value | $99,467.35 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.08 | $210.87 | $2,319.52 | 70 |
| ADBE | 5 | $377.60 | $370.50 | $1,852.47 | 65 |
| AMD | 15 | $135.39 | $142.69 | $2,140.33 | 65 |
| AMZN | 11 | $221.90 | $219.93 | $2,419.18 | 75 |
| AVGO | 8 | $275.34 | $273.51 | $2,188.08 | 70 |
| AXP | 7 | $325.28 | $321.90 | $2,253.30 | 75 |
| BA | 9 | $210.97 | $227.21 | $2,044.89 | 65 |
| BAC | 50 | $48.57 | $47.16 | $2,358.00 | 75 |
| C | 27 | $86.82 | $86.57 | $2,337.32 | 75 |
| CAT | 6 | $397.86 | $408.02 | $2,448.11 | 75 |
| COST | 2 | $979.83 | $972.80 | $1,945.60 | 65 |
| CRM | 8 | $268.33 | $265.23 | $2,121.84 | 65 |
| CSCO | 34 | $68.38 | $69.02 | $2,346.51 | 75 |
| CVX | 17 | $147.15 | $153.81 | $2,614.68 | 85 |
| DIS | 18 | $122.80 | $121.67 | $2,190.15 | 70 |
| GOOGL | 12 | $179.86 | $174.94 | $2,099.28 | 70 |
| GS | 3 | $717.52 | $700.32 | $2,100.96 | 70 |
| HD | 6 | $372.64 | $375.13 | $2,250.78 | 65 |
| INTC | 86 | $22.31 | $23.62 | $2,031.72 | 65 |
| JNJ | 13 | $155.89 | $158.18 | $2,056.28 | 65 |
| JPM | 9 | $291.61 | $285.62 | $2,570.58 | 85 |
| KO | 29 | $71.03 | $69.56 | $2,017.24 | 65 |
| LLY | 2 | $776.66 | $792.57 | $1,585.14 | 65 |
| MA | 4 | $563.08 | $564.22 | $2,256.86 | 65 |
| META | 3 | $717.12 | $721.54 | $2,164.61 | 75 |
| MRK | 28 | $82.46 | $84.14 | $2,355.92 | 75 |
| MSFT | 5 | $498.84 | $499.45 | $2,497.25 | 85 |
| NFLX | 1 | $1,279.00 | $1,270.11 | $1,270.11 | 65 |
| NKE | 32 | $75.73 | $74.45 | $2,382.40 | 75 |
| NVDA | 14 | $156.64 | $162.27 | $2,271.78 | 70 |
| ORCL | 9 | $233.31 | $235.41 | $2,118.74 | 65 |
| PEP | 15 | $136.57 | $135.54 | $2,033.17 | 65 |
| PFE | 85 | $25.20 | $25.89 | $2,200.65 | 70 |
| PG | 12 | $160.96 | $158.38 | $1,900.50 | 60 |
| PYPL | 31 | $76.64 | $75.13 | $2,329.03 | 75 |
| QCOM | 13 | $162.06 | $158.79 | $2,064.27 | 70 |
| T | 73 | $28.55 | $27.78 | $2,027.94 | 65 |
| TGT | 20 | $104.89 | $104.56 | $2,091.10 | 65 |
| TSLA | 6 | $288.62 | $304.81 | $1,828.83 | 65 |
| UNH | 6 | $298.34 | $299.90 | $1,799.40 | 65 |
| UNP | 10 | $236.59 | $239.42 | $2,394.20 | 75 |
| V | 6 | $355.85 | $356.77 | $2,140.65 | 65 |
| VZ | 48 | $43.15 | $42.10 | $2,020.90 | 65 |
| WFC | 29 | $82.30 | $82.14 | $2,381.91 | 75 |
| WMT | 21 | $97.35 | $95.73 | $2,010.28 | 65 |
| XOM | 23 | $110.31 | $114.56 | $2,634.88 | 85 |

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
| 2025-07-10 14:09:15 | SELL | NVDA | 2 | $162.34 | $9.98 | 70 |
| 2025-07-10 14:09:15 | SELL | PFE | 1 | $25.90 | $0.68 | 70 |
| 2025-07-10 14:09:15 | SELL | MRK | 1 | $84.14 | $1.63 | 75 |
| 2025-07-10 14:09:15 | SELL | PG | 1 | $158.32 | $-2.43 | 60 |
| 2025-07-10 14:09:15 | BUY | PYPL | 1 | $75.14 | N/A | 75 |
| 2025-07-10 14:09:15 | BUY | C | 1 | $86.58 | N/A | 75 |
| 2025-07-10 14:09:15 | BUY | CVX | 2 | $153.73 | N/A | 85 |
| 2025-07-10 13:47:19 | SELL | GOOGL | 1 | $175.33 | $-4.18 | 65 |
| 2025-07-10 13:47:19 | SELL | MRK | 2 | $83.42 | $1.68 | 75 |
| 2025-07-10 13:47:19 | SELL | PYPL | 1 | $74.64 | $-1.98 | 70 |
| 2025-07-10 13:47:19 | SELL | PFE | 5 | $25.68 | $2.24 | 70 |
| 2025-07-10 13:47:19 | BUY | NVDA | 2 | $163.90 | N/A | 85 |
| 2025-07-10 13:47:19 | BUY | UNH | 6 | $298.34 | N/A | 65 |
| 2025-07-10 13:47:19 | BUY | XOM | 3 | $113.46 | N/A | 85 |
| 2025-07-10 13:47:19 | BUY | NKE | 1 | $73.76 | N/A | 75 |
| 2025-07-10 13:47:19 | BUY | T | 1 | $27.73 | N/A | 65 |
| 2025-07-10 13:46:52 | SELL | UNH | 7 | $298.55 | $-113.40 | 65 |
| 2025-07-10 13:03:45 | SELL | NVDA | 2 | $162.88 | $11.32 | 70 |
| 2025-07-10 13:03:45 | SELL | C | 1 | $85.79 | $-1.00 | 70 |
| 2025-07-10 13:03:45 | BUY | BAC | 3 | $46.84 | N/A | 75 |
| 2025-07-10 13:03:45 | BUY | INTC | 1 | $23.44 | N/A | 65 |
| 2025-07-10 13:03:45 | BUY | PFE | 1 | $25.56 | N/A | 75 |
| 2025-07-10 12:32:03 | SELL | BAC | 2 | $46.84 | $-3.54 | 70 |
| 2025-07-10 12:32:03 | SELL | T | 5 | $28.10 | $-2.13 | 65 |
| 2025-07-10 12:32:03 | BUY | PFE | 5 | $25.56 | N/A | 75 |

<!--TRADE_LOG_END--> 
