# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 18:28:28**

| Metric | Value |
|---|---|
| **Total Value** | **$101,410.84** |
| Cash | $433.40 |
| Holdings Value | $100,977.44 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.15 | $2,111.50 | 65 |
| ADBE | 6 | $375.23 | $364.86 | $2,189.16 | 65 |
| AMD | 14 | $160.03 | $159.05 | $2,226.70 | 70 |
| AMZN | 10 | $221.65 | $223.90 | $2,239.00 | 75 |
| AVGO | 8 | $275.34 | $285.82 | $2,286.60 | 65 |
| AXP | 7 | $309.18 | $315.24 | $2,206.68 | 75 |
| BA | 9 | $232.14 | $232.12 | $2,089.03 | 70 |
| BAC | 44 | $46.23 | $47.16 | $2,075.26 | 65 |
| C | 30 | $86.85 | $92.67 | $2,780.10 | 85 |
| CAT | 6 | $397.74 | $418.56 | $2,511.36 | 75 |
| COST | 2 | $979.83 | $952.22 | $1,904.44 | 65 |
| CRM | 8 | $267.44 | $258.59 | $2,068.72 | 65 |
| CSCO | 32 | $68.57 | $68.31 | $2,186.08 | 70 |
| CVX | 16 | $146.82 | $151.25 | $2,420.00 | 75 |
| DIS | 20 | $122.61 | $121.64 | $2,432.90 | 75 |
| GOOGL | 13 | $179.34 | $183.71 | $2,388.23 | 75 |
| GS | 3 | $717.52 | $711.23 | $2,133.69 | 70 |
| HD | 6 | $354.18 | $360.05 | $2,160.27 | 65 |
| INTC | 84 | $22.34 | $22.84 | $1,918.56 | 60 |
| JNJ | 13 | $155.43 | $163.94 | $2,131.22 | 70 |
| JPM | 9 | $291.90 | $289.69 | $2,607.16 | 85 |
| KO | 30 | $70.97 | $69.88 | $2,096.25 | 65 |
| LLY | 3 | $781.32 | $764.26 | $2,292.79 | 65 |
| MA | 4 | $563.08 | $554.29 | $2,217.16 | 65 |
| META | 3 | $717.12 | $701.27 | $2,103.81 | 70 |
| MRK | 29 | $82.56 | $81.63 | $2,367.27 | 75 |
| MSFT | 5 | $498.84 | $512.22 | $2,561.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,271.05 | $1,271.05 | 65 |
| NKE | 32 | $71.99 | $73.03 | $2,337.01 | 75 |
| NVDA | 13 | $171.55 | $173.23 | $2,251.99 | 70 |
| ORCL | 9 | $232.91 | $247.28 | $2,225.47 | 70 |
| PEP | 16 | $136.49 | $144.94 | $2,319.12 | 70 |
| PFE | 85 | $25.27 | $24.55 | $2,086.33 | 65 |
| PG | 14 | $152.18 | $155.17 | $2,172.38 | 65 |
| PYPL | 32 | $72.34 | $73.97 | $2,366.88 | 75 |
| QCOM | 14 | $153.83 | $152.91 | $2,140.67 | 65 |
| T | 77 | $27.09 | $27.00 | $2,078.99 | 65 |
| TGT | 20 | $104.83 | $103.71 | $2,074.20 | 65 |
| TSLA | 6 | $318.51 | $319.00 | $1,914.00 | 60 |
| UNH | 7 | $298.51 | $288.19 | $2,017.33 | 65 |
| UNP | 10 | $236.33 | $227.66 | $2,276.60 | 65 |
| V | 6 | $355.85 | $349.92 | $2,099.49 | 65 |
| VZ | 50 | $40.87 | $41.03 | $2,051.50 | 65 |
| WFC | 28 | $78.77 | $79.92 | $2,237.76 | 70 |
| WMT | 21 | $97.38 | $95.37 | $2,002.77 | 60 |
| XOM | 21 | $109.98 | $111.85 | $2,348.85 | 75 |

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
| 2025-07-17 18:28:18 | SELL | NVDA | 2 | $173.20 | $2.86 | 70 |
| 2025-07-17 18:28:18 | SELL | BAC | 1 | $47.17 | $0.91 | 65 |
| 2025-07-17 18:28:18 | SELL | WMT | 1 | $95.37 | $-1.92 | 60 |
| 2025-07-17 18:28:18 | BUY | XOM | 1 | $111.84 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | NKE | 1 | $73.01 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | PYPL | 2 | $73.96 | N/A | 75 |
| 2025-07-17 18:28:18 | BUY | BA | 9 | $232.14 | N/A | 70 |
| 2025-07-17 18:28:18 | BUY | CSCO | 1 | $68.31 | N/A | 70 |
| 2025-07-17 18:27:32 | SELL | BA | 9 | $232.00 | $190.71 | 65 |
| 2025-07-17 18:11:19 | SELL | DIS | 2 | $121.50 | $-2.02 | 75 |
| 2025-07-17 18:11:19 | SELL | NKE | 1 | $72.98 | $0.99 | 70 |
| 2025-07-17 18:11:19 | SELL | CSCO | 2 | $68.28 | $-0.57 | 65 |
| 2025-07-17 18:11:19 | BUY | XOM | 1 | $111.70 | N/A | 70 |
| 2025-07-17 18:11:19 | BUY | PFE | 1 | $24.49 | N/A | 65 |
| 2025-07-17 18:11:19 | BUY | WFC | 2 | $79.68 | N/A | 70 |
| 2025-07-17 18:11:19 | BUY | PYPL | 2 | $73.74 | N/A | 70 |
| 2025-07-17 17:51:42 | SELL | XOM | 2 | $111.62 | $3.31 | 65 |
| 2025-07-17 17:51:42 | SELL | WFC | 2 | $79.84 | $2.13 | 65 |
| 2025-07-17 17:51:42 | BUY | NVDA | 2 | $173.15 | N/A | 85 |
| 2025-07-17 17:51:42 | BUY | NKE | 3 | $73.08 | N/A | 75 |
| 2025-07-17 17:51:42 | BUY | MRK | 1 | $81.60 | N/A | 75 |
| 2025-07-17 17:40:27 | SELL | MRK | 1 | $81.55 | $-1.01 | 70 |
| 2025-07-17 17:40:27 | BUY | WFC | 1 | $79.77 | N/A | 70 |
| 2025-07-17 17:26:16 | SELL | NKE | 1 | $72.96 | $1.05 | 65 |
| 2025-07-17 17:26:16 | SELL | CSCO | 2 | $68.18 | $-0.70 | 70 |

<!--TRADE_LOG_END--> 
