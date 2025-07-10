# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 03:50:51**

| Metric | Value |
|---|---|
| **Total Value** | **$100,978.85** |
| Cash | $1,069.46 |
| Holdings Value | $99,909.39 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.08 | $211.14 | $2,322.54 | 75 |
| ADBE | 5 | $377.60 | $373.38 | $1,866.90 | 65 |
| AMD | 15 | $135.39 | $138.41 | $2,076.15 | 70 |
| AMZN | 11 | $221.90 | $222.54 | $2,447.94 | 75 |
| AVGO | 8 | $275.34 | $277.90 | $2,223.20 | 70 |
| AXP | 7 | $325.28 | $317.35 | $2,221.45 | 75 |
| BA | 9 | $210.97 | $226.60 | $2,039.40 | 65 |
| BAC | 47 | $48.68 | $46.84 | $2,201.48 | 70 |
| C | 30 | $86.69 | $85.79 | $2,573.70 | 85 |
| CAT | 6 | $397.86 | $402.18 | $2,413.08 | 75 |
| COST | 2 | $979.83 | $982.09 | $1,964.18 | 65 |
| CRM | 8 | $268.33 | $270.92 | $2,167.36 | 65 |
| CSCO | 34 | $68.38 | $69.27 | $2,355.18 | 75 |
| CVX | 15 | $146.28 | $153.02 | $2,295.30 | 70 |
| DIS | 17 | $122.93 | $120.61 | $2,050.37 | 70 |
| GOOGL | 13 | $179.51 | $176.62 | $2,296.06 | 75 |
| GS | 3 | $717.52 | $696.56 | $2,089.68 | 70 |
| HD | 6 | $372.64 | $371.04 | $2,226.24 | 70 |
| INTC | 86 | $22.31 | $23.44 | $2,015.84 | 65 |
| JNJ | 13 | $155.89 | $156.28 | $2,031.64 | 65 |
| JPM | 9 | $291.61 | $283.16 | $2,548.44 | 75 |
| KO | 29 | $71.03 | $69.48 | $2,014.92 | 65 |
| LLY | 2 | $776.66 | $786.92 | $1,573.84 | 65 |
| MA | 4 | $563.08 | $565.11 | $2,260.44 | 70 |
| META | 3 | $717.12 | $732.78 | $2,198.34 | 85 |
| MRK | 31 | $82.57 | $83.71 | $2,595.01 | 85 |
| MSFT | 5 | $498.84 | $503.51 | $2,517.55 | 85 |
| NFLX | 1 | $1,279.00 | $1,288.28 | $1,288.28 | 65 |
| NKE | 30 | $75.86 | $73.56 | $2,206.80 | 70 |
| NVDA | 16 | $157.22 | $162.88 | $2,606.08 | 85 |
| ORCL | 9 | $233.31 | $235.81 | $2,122.29 | 65 |
| PEP | 15 | $136.57 | $134.48 | $2,017.20 | 65 |
| PFE | 91 | $25.24 | $25.56 | $2,325.96 | 75 |
| PG | 13 | $160.75 | $157.52 | $2,047.76 | 70 |
| PYPL | 31 | $76.62 | $74.83 | $2,319.73 | 75 |
| QCOM | 13 | $162.06 | $159.35 | $2,071.55 | 70 |
| T | 76 | $28.53 | $28.10 | $2,135.60 | 70 |
| TGT | 20 | $104.89 | $102.43 | $2,048.60 | 65 |
| TSLA | 6 | $288.62 | $295.88 | $1,775.28 | 65 |
| UNH | 7 | $314.75 | $302.91 | $2,120.37 | 65 |
| UNP | 10 | $236.59 | $236.49 | $2,364.90 | 75 |
| V | 6 | $355.85 | $357.76 | $2,146.56 | 65 |
| VZ | 48 | $43.15 | $42.61 | $2,045.28 | 65 |
| WFC | 29 | $82.30 | $81.79 | $2,371.91 | 75 |
| WMT | 21 | $97.35 | $96.81 | $2,033.01 | 65 |
| XOM | 20 | $109.83 | $113.80 | $2,276.00 | 75 |

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
| 2025-07-10 03:50:46 | SELL | NKE | 1 | $73.56 | $-2.23 | 70 |
| 2025-07-10 03:50:46 | BUY | T | 4 | $28.10 | N/A | 70 |
| 2025-07-10 03:17:09 | SELL | INTC | 1 | $23.44 | $1.12 | 65 |
| 2025-07-10 03:17:09 | SELL | PFE | 1 | $25.56 | $0.32 | 75 |
| 2025-07-10 03:17:09 | BUY | NKE | 2 | $73.56 | N/A | 75 |
| 2025-07-10 03:17:09 | BUY | C | 5 | $85.79 | N/A | 85 |
| 2025-07-10 02:43:23 | SELL | DIS | 1 | $120.61 | $-2.19 | 65 |
| 2025-07-10 02:43:23 | BUY | AAPL | 1 | $211.14 | N/A | 75 |
| 2025-07-10 02:43:23 | BUY | PFE | 12 | $25.56 | N/A | 75 |
| 2025-07-10 02:43:23 | BUY | C | 1 | $85.79 | N/A | 70 |
| 2025-07-10 01:59:00 | SELL | PFE | 6 | $25.56 | $2.05 | 65 |
| 2025-07-10 01:59:00 | SELL | C | 2 | $85.79 | $-2.08 | 65 |
| 2025-07-10 01:59:00 | BUY | DIS | 1 | $120.61 | N/A | 70 |
| 2025-07-10 01:59:00 | BUY | NKE | 1 | $73.56 | N/A | 70 |
| 2025-07-10 01:59:00 | BUY | PYPL | 3 | $74.83 | N/A | 75 |
| 2025-07-10 01:13:00 | SELL | DIS | 1 | $120.61 | $-2.19 | 65 |
| 2025-07-10 01:13:00 | SELL | PYPL | 2 | $74.83 | $-3.70 | 65 |
| 2025-07-10 01:13:00 | SELL | C | 5 | $85.79 | $-4.36 | 70 |
| 2025-07-10 01:13:00 | BUY | MRK | 2 | $83.71 | N/A | 85 |
| 2025-07-10 00:34:04 | SELL | MRK | 1 | $83.71 | $1.18 | 75 |
| 2025-07-10 00:34:04 | SELL | CVX | 1 | $153.02 | $6.32 | 70 |
| 2025-07-10 00:34:04 | BUY | C | 5 | $85.79 | N/A | 85 |
| 2025-07-09 23:50:27 | BUY | MRK | 2 | $83.71 | N/A | 80 |
| 2025-07-09 23:37:53 | SELL | PYPL | 1 | $74.83 | $-1.79 | 70 |
| 2025-07-09 23:37:53 | SELL | C | 2 | $85.79 | $-1.93 | 70 |

<!--TRADE_LOG_END--> 
