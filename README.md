# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 17:51:35**

| Metric | Value |
|---|---|
| **Total Value** | **$100,880.68** |
| Cash | $1,452.64 |
| Holdings Value | $99,428.05 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.09 | $2,090.90 | 70 |
| ADBE | 5 | $377.60 | $372.01 | $1,860.07 | 65 |
| AMD | 15 | $135.39 | $139.07 | $2,086.05 | 70 |
| AMZN | 10 | $221.83 | $221.83 | $2,218.30 | 75 |
| AVGO | 8 | $275.34 | $278.06 | $2,224.48 | 65 |
| AXP | 7 | $325.28 | $319.18 | $2,234.26 | 75 |
| BA | 10 | $212.53 | $229.28 | $2,292.75 | 70 |
| BAC | 47 | $48.69 | $47.00 | $2,209.00 | 70 |
| C | 31 | $86.66 | $86.00 | $2,666.15 | 85 |
| CAT | 6 | $397.86 | $402.84 | $2,417.04 | 75 |
| COST | 2 | $979.83 | $975.25 | $1,950.50 | 65 |
| CRM | 8 | $268.33 | $270.23 | $2,161.84 | 65 |
| CSCO | 34 | $68.37 | $68.94 | $2,343.82 | 75 |
| CVX | 16 | $146.67 | $152.91 | $2,446.56 | 75 |
| DIS | 18 | $122.81 | $120.89 | $2,176.02 | 70 |
| GOOGL | 13 | $179.50 | $177.26 | $2,304.38 | 70 |
| GS | 3 | $717.52 | $698.86 | $2,096.59 | 70 |
| HD | 6 | $372.64 | $366.84 | $2,201.04 | 65 |
| INTC | 87 | $22.32 | $23.36 | $2,032.10 | 65 |
| JNJ | 13 | $155.89 | $155.48 | $2,021.24 | 65 |
| JPM | 9 | $291.61 | $283.45 | $2,551.05 | 75 |
| KO | 29 | $71.03 | $69.25 | $2,008.25 | 65 |
| LLY | 2 | $776.66 | $785.61 | $1,571.22 | 65 |
| MA | 4 | $563.08 | $562.63 | $2,250.52 | 65 |
| META | 3 | $717.12 | $733.90 | $2,201.70 | 85 |
| MRK | 28 | $82.45 | $83.91 | $2,349.48 | 75 |
| MSFT | 5 | $498.84 | $501.63 | $2,508.15 | 70 |
| NFLX | 1 | $1,279.00 | $1,276.05 | $1,276.05 | 65 |
| NKE | 29 | $75.98 | $73.69 | $2,136.96 | 70 |
| NVDA | 16 | $157.22 | $162.81 | $2,604.93 | 85 |
| ORCL | 9 | $233.31 | $235.41 | $2,118.69 | 65 |
| PEP | 15 | $136.57 | $133.82 | $2,007.30 | 65 |
| PFE | 86 | $25.22 | $25.45 | $2,188.71 | 70 |
| PG | 13 | $160.75 | $156.43 | $2,033.59 | 60 |
| PYPL | 31 | $76.63 | $74.97 | $2,324.07 | 75 |
| QCOM | 14 | $161.87 | $159.27 | $2,229.78 | 70 |
| T | 72 | $28.56 | $28.10 | $2,023.20 | 65 |
| TGT | 20 | $104.89 | $102.27 | $2,045.40 | 65 |
| TSLA | 6 | $288.62 | $295.32 | $1,771.92 | 65 |
| UNH | 7 | $314.75 | $302.60 | $2,118.20 | 65 |
| UNP | 9 | $236.60 | $237.57 | $2,138.14 | 75 |
| V | 6 | $355.95 | $355.48 | $2,132.88 | 70 |
| VZ | 48 | $43.15 | $42.63 | $2,046.48 | 65 |
| WFC | 30 | $82.27 | $81.89 | $2,456.70 | 80 |
| WMT | 21 | $97.35 | $96.78 | $2,032.28 | 65 |
| XOM | 20 | $109.83 | $113.47 | $2,269.30 | 75 |

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
| 2025-07-09 17:51:26 | BUY | INTC | 1 | $23.35 | N/A | 65 |
| 2025-07-09 17:51:26 | BUY | PYPL | 1 | $74.97 | N/A | 75 |
| 2025-07-09 17:51:26 | BUY | NKE | 1 | $73.70 | N/A | 70 |
| 2025-07-09 17:51:26 | BUY | PFE | 1 | $25.45 | N/A | 70 |
| 2025-07-09 17:51:26 | BUY | WFC | 1 | $81.89 | N/A | 80 |
| 2025-07-09 17:51:26 | BUY | CSCO | 2 | $68.93 | N/A | 75 |
| 2025-07-09 17:39:18 | SELL | PYPL | 1 | $74.88 | $-1.75 | 70 |
| 2025-07-09 17:39:18 | SELL | MRK | 1 | $83.78 | $1.29 | 75 |
| 2025-07-09 17:39:18 | SELL | CSCO | 1 | $68.88 | $0.53 | 70 |
| 2025-07-09 17:39:18 | SELL | CVX | 1 | $152.81 | $5.78 | 75 |
| 2025-07-09 17:39:18 | BUY | INTC | 6 | $23.33 | N/A | 65 |
| 2025-07-09 17:25:41 | SELL | BAC | 3 | $47.03 | $-4.69 | 70 |
| 2025-07-09 17:25:41 | SELL | NKE | 1 | $73.92 | $-2.06 | 65 |
| 2025-07-09 17:25:41 | BUY | PFE | 4 | $25.48 | N/A | 70 |
| 2025-07-09 17:25:41 | BUY | CSCO | 1 | $68.89 | N/A | 75 |
| 2025-07-09 17:25:41 | BUY | CVX | 1 | $153.27 | N/A | 85 |
| 2025-07-09 17:10:02 | SELL | INTC | 7 | $23.59 | $8.73 | 60 |
| 2025-07-09 17:10:02 | SELL | PFE | 6 | $25.44 | $1.30 | 65 |
| 2025-07-09 17:10:02 | SELL | CVX | 1 | $153.25 | $6.22 | 75 |
| 2025-07-09 17:10:02 | BUY | BAC | 4 | $46.78 | N/A | 75 |
| 2025-07-09 17:10:02 | BUY | NKE | 1 | $73.95 | N/A | 70 |
| 2025-07-09 17:10:02 | BUY | PYPL | 1 | $74.82 | N/A | 75 |
| 2025-07-09 17:10:02 | BUY | MRK | 1 | $83.86 | N/A | 80 |
| 2025-07-09 16:56:47 | SELL | PYPL | 1 | $74.84 | $-1.79 | 70 |
| 2025-07-09 16:56:47 | SELL | PFE | 5 | $25.44 | $1.02 | 70 |

<!--TRADE_LOG_END--> 
