# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 18:11:08**

| Metric | Value |
|---|---|
| **Total Value** | **$100,872.95** |
| Cash | $90.88 |
| Holdings Value | $100,782.07 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.13 | $2,101.30 | 65 |
| ADBE | 5 | $377.60 | $381.62 | $1,908.10 | 65 |
| AMD | 16 | $135.69 | $138.57 | $2,217.10 | 70 |
| AMZN | 10 | $221.61 | $220.76 | $2,207.60 | 65 |
| AVGO | 8 | $275.34 | $274.30 | $2,194.36 | 70 |
| AXP | 8 | $324.24 | $319.67 | $2,557.32 | 85 |
| BA | 10 | $212.43 | $218.90 | $2,189.00 | 70 |
| BAC | 50 | $48.63 | $47.34 | $2,367.25 | 75 |
| C | 30 | $86.58 | $86.22 | $2,586.45 | 85 |
| CAT | 6 | $397.86 | $395.31 | $2,371.86 | 70 |
| COST | 2 | $979.83 | $987.65 | $1,975.29 | 65 |
| CRM | 8 | $268.33 | $273.94 | $2,191.56 | 65 |
| CSCO | 33 | $68.36 | $68.72 | $2,267.92 | 75 |
| CVX | 16 | $146.71 | $152.80 | $2,444.84 | 75 |
| DIS | 17 | $122.85 | $122.24 | $2,078.08 | 65 |
| GOOGL | 12 | $179.60 | $173.99 | $2,087.88 | 65 |
| GS | 3 | $717.52 | $699.40 | $2,098.20 | 70 |
| HD | 6 | $372.64 | $367.53 | $2,205.16 | 65 |
| INTC | 86 | $22.32 | $23.70 | $2,037.77 | 65 |
| JNJ | 13 | $155.89 | $155.31 | $2,019.03 | 65 |
| JPM | 9 | $291.61 | $283.16 | $2,548.44 | 85 |
| KO | 29 | $71.03 | $70.36 | $2,040.44 | 65 |
| LLY | 2 | $776.66 | $781.30 | $1,562.60 | 65 |
| MA | 4 | $563.08 | $561.51 | $2,246.04 | 65 |
| META | 3 | $717.12 | $720.73 | $2,162.19 | 75 |
| MRK | 30 | $82.46 | $81.26 | $2,437.80 | 80 |
| MSFT | 5 | $498.84 | $496.52 | $2,482.60 | 75 |
| NFLX | 1 | $1,279.00 | $1,277.56 | $1,277.56 | 65 |
| NKE | 28 | $76.04 | $74.00 | $2,072.14 | 65 |
| NVDA | 17 | $157.07 | $159.92 | $2,718.64 | 85 |
| ORCL | 9 | $233.41 | $236.76 | $2,130.84 | 70 |
| PEP | 15 | $136.57 | $134.90 | $2,023.50 | 65 |
| PFE | 85 | $25.24 | $25.57 | $2,173.45 | 70 |
| PG | 13 | $160.77 | $158.47 | $2,060.14 | 65 |
| PYPL | 31 | $76.65 | $74.86 | $2,320.66 | 75 |
| QCOM | 15 | $161.62 | $160.22 | $2,403.23 | 75 |
| T | 81 | $28.53 | $28.44 | $2,303.64 | 75 |
| TGT | 20 | $104.90 | $101.77 | $2,035.40 | 65 |
| TSLA | 6 | $288.62 | $302.40 | $1,814.40 | 60 |
| UNH | 7 | $314.75 | $305.65 | $2,139.53 | 70 |
| UNP | 10 | $236.66 | $236.90 | $2,368.95 | 75 |
| V | 6 | $355.95 | $354.29 | $2,125.74 | 70 |
| VZ | 46 | $43.16 | $43.16 | $1,985.13 | 65 |
| WFC | 29 | $82.34 | $81.78 | $2,371.76 | 75 |
| WMT | 23 | $97.36 | $97.53 | $2,243.30 | 75 |
| XOM | 23 | $110.37 | $114.25 | $2,627.86 | 85 |

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
| 2025-07-08 17:51:41 | BUY | INTC | 1 | $23.57 | N/A | 65 |
| 2025-07-08 17:51:41 | BUY | PFE | 7 | $25.52 | N/A | 75 |
| 2025-07-08 17:51:41 | BUY | WFC | 2 | $81.75 | N/A | 80 |
| 2025-07-08 17:51:41 | BUY | QCOM | 1 | $159.84 | N/A | 75 |
| 2025-07-08 17:51:41 | BUY | CVX | 1 | $152.75 | N/A | 85 |
| 2025-07-08 17:51:41 | BUY | T | 1 | $28.39 | N/A | 65 |
| 2025-07-08 17:39:36 | SELL | MRK | 1 | $81.13 | $-1.36 | 70 |

<!--TRADE_LOG_END--> 
