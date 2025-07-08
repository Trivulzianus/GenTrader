# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 18:27:49**

| Metric | Value |
|---|---|
| **Total Value** | **$100,809.71** |
| Cash | $688.64 |
| Holdings Value | $100,121.07 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.03 | $2,100.35 | 65 |
| ADBE | 5 | $377.60 | $381.95 | $1,909.75 | 65 |
| AMD | 16 | $135.69 | $138.47 | $2,215.46 | 70 |
| AMZN | 10 | $221.61 | $220.60 | $2,206.00 | 65 |
| AVGO | 8 | $275.34 | $273.54 | $2,188.28 | 75 |
| AXP | 8 | $324.24 | $319.02 | $2,552.16 | 85 |
| BA | 10 | $212.43 | $218.55 | $2,185.50 | 65 |
| BAC | 50 | $48.63 | $47.35 | $2,367.75 | 75 |
| C | 30 | $86.58 | $85.95 | $2,578.55 | 85 |
| CAT | 6 | $397.86 | $395.39 | $2,372.37 | 70 |
| COST | 2 | $979.83 | $986.96 | $1,973.91 | 65 |
| CRM | 8 | $268.33 | $273.87 | $2,190.96 | 65 |
| CSCO | 32 | $68.34 | $68.70 | $2,198.56 | 70 |
| CVX | 16 | $146.71 | $152.69 | $2,442.96 | 75 |
| DIS | 17 | $122.85 | $122.09 | $2,075.53 | 70 |
| GOOGL | 12 | $179.60 | $173.84 | $2,086.08 | 65 |
| GS | 3 | $717.52 | $697.01 | $2,091.05 | 70 |
| HD | 6 | $372.64 | $368.00 | $2,208.00 | 65 |
| INTC | 86 | $22.32 | $23.68 | $2,036.30 | 65 |
| JNJ | 13 | $155.89 | $155.53 | $2,021.83 | 65 |
| JPM | 9 | $291.61 | $282.39 | $2,541.51 | 75 |
| KO | 29 | $71.03 | $70.36 | $2,040.58 | 65 |
| LLY | 2 | $776.66 | $781.02 | $1,562.04 | 65 |
| MA | 4 | $563.08 | $561.38 | $2,245.52 | 65 |
| META | 3 | $717.12 | $719.76 | $2,159.28 | 75 |
| MRK | 29 | $82.50 | $81.34 | $2,359.01 | 75 |
| MSFT | 5 | $498.84 | $496.07 | $2,480.35 | 85 |
| NFLX | 1 | $1,279.00 | $1,273.03 | $1,273.03 | 65 |
| NKE | 29 | $75.97 | $74.00 | $2,145.86 | 70 |
| NVDA | 17 | $157.07 | $159.59 | $2,713.11 | 85 |
| ORCL | 9 | $233.41 | $235.11 | $2,115.99 | 65 |
| PEP | 15 | $136.57 | $135.10 | $2,026.50 | 65 |
| PFE | 85 | $25.24 | $25.57 | $2,173.25 | 70 |
| PG | 13 | $160.77 | $158.71 | $2,063.23 | 65 |
| PYPL | 31 | $76.65 | $74.89 | $2,321.43 | 75 |
| QCOM | 15 | $161.62 | $160.29 | $2,404.40 | 75 |
| T | 72 | $28.55 | $28.41 | $2,045.52 | 65 |
| TGT | 20 | $104.90 | $101.87 | $2,037.40 | 65 |
| TSLA | 6 | $288.62 | $302.97 | $1,817.82 | 65 |
| UNH | 7 | $314.75 | $306.43 | $2,144.97 | 65 |
| UNP | 10 | $236.66 | $237.06 | $2,370.55 | 75 |
| V | 6 | $355.95 | $354.24 | $2,125.44 | 65 |
| VZ | 47 | $43.16 | $43.12 | $2,026.41 | 65 |
| WFC | 29 | $82.34 | $81.64 | $2,367.56 | 75 |
| WMT | 21 | $97.35 | $97.55 | $2,048.55 | 65 |
| XOM | 22 | $110.20 | $114.11 | $2,510.42 | 80 |

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
| 2025-07-08 17:51:41 | SELL | C | 3 | $86.25 | $-0.96 | 75 |
| 2025-07-08 17:51:41 | BUY | NVDA | 1 | $159.76 | N/A | 85 |
| 2025-07-08 17:51:41 | BUY | BAC | 1 | $47.24 | N/A | 75 |

<!--TRADE_LOG_END--> 
