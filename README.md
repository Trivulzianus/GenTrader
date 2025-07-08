# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 18:45:18**

| Metric | Value |
|---|---|
| **Total Value** | **$100,712.33** |
| Cash | $513.42 |
| Holdings Value | $100,198.92 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.67 | $2,096.70 | 65 |
| ADBE | 5 | $377.60 | $381.47 | $1,907.34 | 65 |
| AMD | 16 | $135.69 | $138.20 | $2,211.20 | 70 |
| AMZN | 10 | $221.61 | $220.04 | $2,200.40 | 70 |
| AVGO | 8 | $275.34 | $272.69 | $2,181.56 | 70 |
| AXP | 8 | $324.24 | $318.89 | $2,551.12 | 85 |
| BA | 10 | $212.43 | $218.79 | $2,187.90 | 70 |
| BAC | 50 | $48.63 | $47.38 | $2,368.75 | 75 |
| C | 28 | $86.63 | $85.95 | $2,406.74 | 75 |
| CAT | 6 | $397.86 | $395.09 | $2,370.54 | 70 |
| COST | 2 | $979.83 | $984.60 | $1,969.20 | 65 |
| CRM | 8 | $268.33 | $273.71 | $2,189.68 | 65 |
| CSCO | 32 | $68.34 | $68.64 | $2,196.32 | 70 |
| CVX | 17 | $147.05 | $152.42 | $2,591.14 | 85 |
| DIS | 17 | $122.85 | $122.00 | $2,073.91 | 65 |
| GOOGL | 12 | $179.60 | $173.58 | $2,082.96 | 65 |
| GS | 3 | $717.52 | $697.81 | $2,093.43 | 70 |
| HD | 6 | $372.64 | $367.35 | $2,204.10 | 65 |
| INTC | 86 | $22.32 | $23.64 | $2,033.04 | 65 |
| JNJ | 13 | $155.89 | $155.28 | $2,018.58 | 65 |
| JPM | 9 | $291.61 | $282.71 | $2,544.39 | 85 |
| KO | 29 | $71.03 | $70.25 | $2,037.25 | 65 |
| LLY | 2 | $776.66 | $781.51 | $1,563.02 | 65 |
| MA | 4 | $563.08 | $561.20 | $2,244.80 | 65 |
| META | 3 | $717.12 | $718.91 | $2,156.73 | 85 |
| MRK | 29 | $82.50 | $81.35 | $2,359.15 | 75 |
| MSFT | 5 | $498.84 | $495.94 | $2,479.68 | 70 |
| NFLX | 1 | $1,279.00 | $1,271.41 | $1,271.41 | 65 |
| NKE | 29 | $75.97 | $73.77 | $2,139.18 | 70 |
| NVDA | 17 | $157.07 | $159.68 | $2,714.53 | 85 |
| ORCL | 9 | $233.41 | $234.96 | $2,114.64 | 65 |
| PEP | 15 | $136.57 | $134.92 | $2,023.80 | 65 |
| PFE | 85 | $25.24 | $25.57 | $2,173.03 | 70 |
| PG | 13 | $160.77 | $158.06 | $2,054.82 | 70 |
| PYPL | 31 | $76.65 | $74.73 | $2,316.63 | 75 |
| QCOM | 15 | $161.62 | $159.88 | $2,398.20 | 75 |
| T | 72 | $28.55 | $28.39 | $2,044.44 | 65 |
| TGT | 20 | $104.90 | $101.88 | $2,037.60 | 65 |
| TSLA | 6 | $288.62 | $302.26 | $1,813.59 | 65 |
| UNH | 7 | $314.75 | $306.31 | $2,144.20 | 65 |
| UNP | 10 | $236.66 | $236.99 | $2,369.90 | 75 |
| V | 6 | $355.95 | $354.15 | $2,124.90 | 65 |
| VZ | 47 | $43.16 | $43.05 | $2,023.12 | 65 |
| WFC | 29 | $82.34 | $81.59 | $2,366.26 | 75 |
| WMT | 23 | $97.35 | $97.38 | $2,239.74 | 75 |
| XOM | 22 | $110.20 | $114.06 | $2,509.32 | 80 |

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
| 2025-07-08 18:45:11 | SELL | C | 2 | $85.97 | $-1.22 | 75 |
| 2025-07-08 18:45:11 | BUY | WMT | 2 | $97.38 | N/A | 75 |
| 2025-07-08 18:45:11 | BUY | CVX | 1 | $152.41 | N/A | 85 |
| 2025-07-08 18:27:39 | SELL | WMT | 2 | $97.54 | $0.37 | 65 |
| 2025-07-08 18:27:39 | SELL | XOM | 1 | $114.14 | $3.77 | 80 |
| 2025-07-08 18:27:39 | SELL | MRK | 1 | $81.34 | $-1.12 | 75 |
| 2025-07-08 18:27:39 | SELL | CSCO | 1 | $68.71 | $0.35 | 70 |
| 2025-07-08 18:27:39 | SELL | T | 9 | $28.40 | $-1.18 | 65 |
| 2025-07-08 18:27:39 | BUY | NKE | 1 | $74.00 | N/A | 70 |
| 2025-07-08 18:27:39 | BUY | VZ | 1 | $43.12 | N/A | 65 |
| 2025-07-08 18:10:59 | SELL | JNJ | 1 | $155.35 | $-0.50 | 65 |
| 2025-07-08 18:10:59 | SELL | INTC | 2 | $23.68 | $2.67 | 65 |
| 2025-07-08 18:10:59 | SELL | BAC | 1 | $47.35 | $-1.26 | 75 |
| 2025-07-08 18:10:59 | SELL | NKE | 2 | $74.03 | $-3.76 | 65 |
| 2025-07-08 18:10:59 | SELL | PFE | 9 | $25.57 | $2.72 | 70 |
| 2025-07-08 18:10:59 | SELL | WFC | 2 | $81.79 | $-1.03 | 75 |
| 2025-07-08 18:10:59 | SELL | CVX | 1 | $152.79 | $5.72 | 75 |
| 2025-07-08 18:10:59 | BUY | WMT | 2 | $97.56 | N/A | 75 |
| 2025-07-08 18:10:59 | BUY | XOM | 2 | $114.27 | N/A | 85 |
| 2025-07-08 18:10:59 | BUY | PYPL | 1 | $74.88 | N/A | 75 |
| 2025-07-08 18:10:59 | BUY | MRK | 2 | $81.26 | N/A | 80 |
| 2025-07-08 18:10:59 | BUY | C | 2 | $86.23 | N/A | 85 |
| 2025-07-08 18:10:59 | BUY | VZ | 46 | $43.16 | N/A | 65 |
| 2025-07-08 18:10:59 | BUY | T | 8 | $28.44 | N/A | 75 |
| 2025-07-08 17:51:41 | SELL | VZ | 47 | $43.06 | $-30.99 | 65 |

<!--TRADE_LOG_END--> 
