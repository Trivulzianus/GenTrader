# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 19:36:59**

| Metric | Value |
|---|---|
| **Total Value** | **$100,837.91** |
| Cash | $313.88 |
| Holdings Value | $100,524.03 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.99 | $2,089.91 | 65 |
| ADBE | 6 | $375.23 | $366.99 | $2,201.94 | 65 |
| AMD | 15 | $134.72 | $146.25 | $2,193.82 | 70 |
| AMZN | 10 | $221.60 | $225.08 | $2,250.80 | 75 |
| AVGO | 8 | $275.34 | $275.55 | $2,204.40 | 70 |
| AXP | 7 | $325.34 | $320.54 | $2,243.78 | 75 |
| BA | 10 | $212.67 | $230.62 | $2,306.20 | 70 |
| BAC | 51 | $48.57 | $46.97 | $2,395.47 | 75 |
| C | 30 | $86.60 | $87.27 | $2,617.95 | 85 |
| CAT | 6 | $397.74 | $405.58 | $2,433.48 | 70 |
| COST | 2 | $979.83 | $978.74 | $1,957.48 | 65 |
| CRM | 7 | $268.68 | $259.80 | $1,818.60 | 65 |
| CSCO | 31 | $68.47 | $67.72 | $2,099.47 | 65 |
| CVX | 16 | $146.79 | $151.57 | $2,425.12 | 75 |
| DIS | 18 | $122.79 | $120.17 | $2,162.97 | 70 |
| GOOGL | 14 | $179.74 | $181.69 | $2,543.73 | 85 |
| GS | 3 | $717.52 | $711.74 | $2,135.22 | 70 |
| HD | 6 | $372.64 | $369.81 | $2,218.83 | 70 |
| INTC | 80 | $22.30 | $23.25 | $1,859.60 | 60 |
| JNJ | 13 | $155.95 | $156.81 | $2,038.47 | 65 |
| JPM | 9 | $291.63 | $288.45 | $2,596.05 | 85 |
| KO | 29 | $71.03 | $69.42 | $2,013.04 | 65 |
| LLY | 3 | $781.32 | $797.49 | $2,392.45 | 70 |
| MA | 4 | $563.08 | $553.41 | $2,213.65 | 65 |
| META | 3 | $717.12 | $720.84 | $2,162.51 | 70 |
| MRK | 28 | $82.50 | $83.75 | $2,345.09 | 75 |
| MSFT | 5 | $498.84 | $503.06 | $2,515.30 | 75 |
| NFLX | 1 | $1,279.00 | $1,264.84 | $1,264.84 | 65 |
| NKE | 30 | $72.05 | $72.31 | $2,169.15 | 70 |
| NVDA | 16 | $157.66 | $164.17 | $2,626.72 | 85 |
| ORCL | 9 | $233.27 | $229.32 | $2,063.88 | 65 |
| PEP | 15 | $136.57 | $135.54 | $2,033.17 | 65 |
| PFE | 86 | $25.21 | $25.42 | $2,186.12 | 70 |
| PG | 13 | $160.78 | $154.20 | $2,004.60 | 65 |
| PYPL | 28 | $72.07 | $73.89 | $2,068.78 | 65 |
| QCOM | 14 | $153.83 | $154.16 | $2,158.24 | 65 |
| T | 75 | $27.10 | $27.19 | $2,039.25 | 65 |
| TGT | 20 | $104.94 | $104.68 | $2,093.60 | 65 |
| TSLA | 6 | $288.62 | $316.08 | $1,896.48 | 65 |
| UNH | 7 | $298.51 | $300.01 | $2,100.11 | 65 |
| UNP | 10 | $236.28 | $233.67 | $2,336.70 | 75 |
| V | 6 | $355.85 | $350.88 | $2,105.28 | 65 |
| VZ | 49 | $43.12 | $41.70 | $2,043.54 | 65 |
| WFC | 30 | $82.33 | $83.27 | $2,498.10 | 80 |
| WMT | 21 | $97.38 | $95.64 | $2,008.54 | 65 |
| XOM | 21 | $110.01 | $113.89 | $2,391.59 | 75 |

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
| 2025-07-14 19:25:06 | BUY | CSCO | 2 | $67.71 | N/A | 70 |
| 2025-07-14 19:08:29 | SELL | AMD | 2 | $146.57 | $22.17 | 65 |
| 2025-07-14 19:08:29 | SELL | PYPL | 3 | $73.81 | $4.67 | 65 |
| 2025-07-14 19:08:29 | SELL | C | 4 | $87.32 | $2.81 | 70 |
| 2025-07-14 19:08:29 | SELL | UNP | 1 | $233.77 | $-2.52 | 65 |
| 2025-07-14 19:08:29 | BUY | AMZN | 1 | $225.41 | N/A | 80 |
| 2025-07-14 19:08:29 | BUY | BAC | 3 | $46.99 | N/A | 75 |
| 2025-07-14 19:08:29 | BUY | MRK | 3 | $83.76 | N/A | 85 |

<!--TRADE_LOG_END--> 
