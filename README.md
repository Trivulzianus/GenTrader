# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 14:41:34**

| Metric | Value |
|---|---|
| **Total Value** | **$100,597.67** |
| Cash | $1,055.91 |
| Holdings Value | $99,541.76 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.47 | $2,084.75 | 65 |
| ADBE | 6 | $375.23 | $365.15 | $2,190.90 | 65 |
| AMD | 15 | $134.63 | $144.61 | $2,169.18 | 65 |
| AMZN | 11 | $221.92 | $225.83 | $2,484.13 | 75 |
| AVGO | 8 | $275.34 | $273.55 | $2,188.42 | 65 |
| AXP | 7 | $325.34 | $319.11 | $2,233.77 | 75 |
| BA | 10 | $212.59 | $227.87 | $2,278.70 | 70 |
| BAC | 47 | $48.70 | $46.72 | $2,195.61 | 70 |
| C | 31 | $86.64 | $86.76 | $2,689.56 | 85 |
| CAT | 5 | $396.39 | $405.24 | $2,026.20 | 70 |
| COST | 2 | $979.83 | $973.70 | $1,947.40 | 65 |
| CRM | 7 | $268.68 | $260.39 | $1,822.73 | 65 |
| CSCO | 30 | $68.48 | $67.33 | $2,020.05 | 65 |
| CVX | 16 | $146.77 | $153.40 | $2,454.40 | 75 |
| DIS | 17 | $122.97 | $119.85 | $2,037.45 | 65 |
| GOOGL | 14 | $179.65 | $179.98 | $2,519.72 | 85 |
| GS | 3 | $717.52 | $708.34 | $2,125.03 | 75 |
| HD | 6 | $372.64 | $369.17 | $2,215.02 | 65 |
| INTC | 89 | $22.39 | $23.11 | $2,057.23 | 65 |
| JNJ | 13 | $155.95 | $156.57 | $2,035.41 | 65 |
| JPM | 9 | $291.63 | $286.89 | $2,582.05 | 85 |
| KO | 29 | $71.03 | $69.69 | $2,020.87 | 65 |
| LLY | 3 | $781.32 | $794.67 | $2,384.00 | 70 |
| MA | 4 | $563.08 | $555.67 | $2,222.70 | 65 |
| META | 3 | $717.12 | $719.00 | $2,157.00 | 70 |
| MRK | 28 | $82.49 | $83.84 | $2,347.66 | 75 |
| MSFT | 5 | $498.84 | $501.66 | $2,508.28 | 70 |
| NFLX | 1 | $1,279.00 | $1,258.72 | $1,258.72 | 65 |
| NKE | 29 | $72.08 | $72.19 | $2,093.65 | 65 |
| NVDA | 13 | $156.20 | $163.63 | $2,127.19 | 65 |
| ORCL | 9 | $233.26 | $226.57 | $2,039.13 | 70 |
| PEP | 15 | $136.57 | $134.39 | $2,015.85 | 65 |
| PFE | 86 | $25.21 | $25.56 | $2,198.16 | 70 |
| PG | 13 | $160.78 | $153.78 | $1,999.14 | 65 |
| PYPL | 30 | $72.22 | $74.27 | $2,228.12 | 70 |
| QCOM | 14 | $162.09 | $154.09 | $2,157.33 | 65 |
| T | 75 | $27.10 | $27.25 | $2,043.38 | 65 |
| TGT | 21 | $104.88 | $104.28 | $2,189.88 | 70 |
| TSLA | 6 | $288.62 | $314.18 | $1,885.05 | 65 |
| UNH | 7 | $298.51 | $300.25 | $2,101.75 | 65 |
| UNP | 10 | $236.18 | $233.89 | $2,338.90 | 70 |
| V | 6 | $355.85 | $351.30 | $2,107.80 | 65 |
| VZ | 49 | $43.12 | $41.77 | $2,046.97 | 65 |
| WFC | 28 | $82.26 | $82.83 | $2,319.10 | 75 |
| WMT | 21 | $97.38 | $94.92 | $1,993.32 | 65 |
| XOM | 21 | $110.01 | $114.29 | $2,400.09 | 75 |

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
| 2025-07-14 14:41:26 | SELL | NVDA | 2 | $163.70 | $13.00 | 65 |
| 2025-07-14 14:41:26 | SELL | NKE | 1 | $72.14 | $0.06 | 65 |
| 2025-07-14 14:41:26 | SELL | PYPL | 1 | $74.27 | $1.99 | 70 |
| 2025-07-14 14:41:26 | SELL | CVX | 1 | $153.43 | $6.27 | 75 |
| 2025-07-14 14:41:26 | BUY | INTC | 8 | $23.12 | N/A | 65 |
| 2025-07-14 14:41:26 | BUY | PFE | 1 | $25.55 | N/A | 70 |
| 2025-07-14 14:41:26 | BUY | C | 1 | $86.73 | N/A | 85 |
| 2025-07-14 14:41:26 | BUY | VZ | 4 | $41.78 | N/A | 65 |
| 2025-07-14 14:41:26 | BUY | TGT | 1 | $104.26 | N/A | 70 |
| 2025-07-14 14:26:30 | SELL | AMZN | 1 | $225.53 | $3.31 | 75 |
| 2025-07-14 14:26:30 | SELL | JNJ | 1 | $156.57 | $0.58 | 65 |
| 2025-07-14 14:26:30 | SELL | INTC | 7 | $23.03 | $4.61 | 60 |
| 2025-07-14 14:26:30 | SELL | XOM | 1 | $113.52 | $3.35 | 75 |
| 2025-07-14 14:26:30 | SELL | DIS | 1 | $120.04 | $-2.77 | 65 |
| 2025-07-14 14:26:30 | SELL | PFE | 1 | $25.65 | $0.44 | 70 |
| 2025-07-14 14:26:30 | SELL | CSCO | 3 | $67.64 | $-2.30 | 65 |
| 2025-07-14 14:26:30 | SELL | VZ | 1 | $41.76 | $-1.45 | 60 |
| 2025-07-14 14:26:30 | BUY | NVDA | 2 | $163.91 | N/A | 80 |
| 2025-07-14 14:26:30 | BUY | PYPL | 3 | $74.12 | N/A | 75 |
| 2025-07-14 14:26:30 | BUY | NKE | 2 | $71.85 | N/A | 70 |
| 2025-07-14 14:26:30 | BUY | C | 3 | $86.65 | N/A | 85 |
| 2025-07-14 14:09:17 | SELL | PYPL | 4 | $73.70 | $5.64 | 65 |
| 2025-07-14 14:09:17 | SELL | VZ | 3 | $41.74 | $-4.11 | 60 |
| 2025-07-14 14:09:17 | SELL | T | 1 | $27.40 | $0.29 | 65 |
| 2025-07-14 14:09:17 | BUY | XOM | 1 | $114.01 | N/A | 80 |

<!--TRADE_LOG_END--> 
