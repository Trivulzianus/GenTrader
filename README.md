# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 17:25:42**

| Metric | Value |
|---|---|
| **Total Value** | **$100,572.28** |
| Cash | $627.67 |
| Holdings Value | $99,944.60 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.65 | $2,106.50 | 65 |
| ADBE | 6 | $375.23 | $365.26 | $2,191.56 | 65 |
| AMD | 17 | $146.29 | $155.35 | $2,641.02 | 85 |
| AMZN | 10 | $221.63 | $225.97 | $2,259.70 | 70 |
| AVGO | 8 | $275.34 | $279.84 | $2,238.72 | 65 |
| AXP | 7 | $325.34 | $311.76 | $2,182.36 | 65 |
| BA | 10 | $212.82 | $229.84 | $2,298.40 | 70 |
| BAC | 45 | $48.79 | $46.30 | $2,083.72 | 65 |
| C | 30 | $86.78 | $90.16 | $2,704.80 | 85 |
| CAT | 6 | $397.74 | $403.72 | $2,422.32 | 65 |
| COST | 2 | $979.83 | $970.31 | $1,940.62 | 65 |
| CRM | 8 | $267.44 | $258.90 | $2,071.24 | 65 |
| CSCO | 31 | $68.46 | $67.34 | $2,087.70 | 65 |
| CVX | 16 | $146.80 | $150.52 | $2,408.32 | 75 |
| DIS | 18 | $122.77 | $119.06 | $2,143.08 | 65 |
| GOOGL | 14 | $179.71 | $183.51 | $2,569.14 | 85 |
| GS | 3 | $717.52 | $702.21 | $2,106.63 | 70 |
| HD | 6 | $372.64 | $362.37 | $2,174.22 | 65 |
| INTC | 89 | $22.39 | $23.19 | $2,063.92 | 65 |
| JNJ | 13 | $155.95 | $155.38 | $2,019.88 | 65 |
| JPM | 9 | $291.63 | $286.22 | $2,575.98 | 85 |
| KO | 30 | $70.97 | $69.47 | $2,084.10 | 65 |
| LLY | 3 | $781.32 | $777.50 | $2,332.50 | 65 |
| MA | 4 | $563.08 | $552.47 | $2,209.88 | 65 |
| META | 3 | $717.12 | $715.00 | $2,145.00 | 85 |
| MRK | 25 | $82.54 | $81.59 | $2,039.84 | 65 |
| MSFT | 5 | $498.84 | $506.74 | $2,533.70 | 85 |
| NFLX | 1 | $1,279.00 | $1,255.75 | $1,255.75 | 65 |
| NKE | 29 | $72.04 | $71.85 | $2,083.51 | 65 |
| NVDA | 15 | $171.62 | $170.64 | $2,559.67 | 85 |
| ORCL | 9 | $233.27 | $232.59 | $2,093.26 | 65 |
| PEP | 15 | $136.57 | $134.33 | $2,014.95 | 65 |
| PFE | 83 | $25.22 | $24.72 | $2,051.82 | 65 |
| PG | 14 | $152.15 | $152.72 | $2,138.01 | 65 |
| PYPL | 29 | $72.18 | $73.74 | $2,138.46 | 65 |
| QCOM | 14 | $153.83 | $154.79 | $2,167.06 | 65 |
| T | 77 | $27.09 | $26.93 | $2,073.22 | 65 |
| TGT | 20 | $104.94 | $102.56 | $2,051.20 | 65 |
| TSLA | 6 | $318.51 | $314.06 | $1,884.33 | 65 |
| UNH | 7 | $298.51 | $294.24 | $2,059.64 | 65 |
| UNP | 9 | $236.55 | $232.23 | $2,090.07 | 65 |
| V | 6 | $355.85 | $348.19 | $2,089.14 | 65 |
| VZ | 50 | $43.08 | $41.20 | $2,059.75 | 65 |
| WFC | 27 | $78.88 | $78.55 | $2,120.85 | 65 |
| WMT | 21 | $97.38 | $95.55 | $2,006.44 | 65 |
| XOM | 21 | $109.99 | $112.98 | $2,372.61 | 75 |

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
| 2025-07-15 17:25:36 | SELL | BAC | 3 | $46.31 | $-6.97 | 65 |
| 2025-07-15 17:25:36 | SELL | UNP | 1 | $232.23 | $-3.89 | 65 |
| 2025-07-15 17:25:36 | SELL | CVX | 2 | $150.52 | $6.62 | 75 |
| 2025-07-15 17:25:36 | BUY | NVDA | 2 | $170.62 | N/A | 85 |
| 2025-07-15 17:25:36 | BUY | INTC | 6 | $23.20 | N/A | 65 |
| 2025-07-15 17:09:19 | SELL | INTC | 6 | $23.23 | $4.98 | 60 |
| 2025-07-15 17:09:19 | BUY | PG | 1 | $152.54 | N/A | 70 |
| 2025-07-15 17:09:19 | BUY | UNP | 1 | $232.19 | N/A | 75 |
| 2025-07-15 17:09:19 | BUY | CVX | 2 | $150.43 | N/A | 85 |
| 2025-07-15 16:57:02 | SELL | NKE | 1 | $71.99 | $-0.05 | 65 |
| 2025-07-15 16:57:02 | SELL | WFC | 1 | $78.58 | $-0.28 | 65 |
| 2025-07-15 16:57:02 | SELL | BA | 1 | $230.25 | $15.84 | 70 |
| 2025-07-15 16:57:02 | SELL | CVX | 1 | $150.56 | $3.53 | 75 |
| 2025-07-15 16:57:02 | BUY | BAC | 4 | $46.47 | N/A | 70 |
| 2025-07-15 16:57:02 | BUY | INTC | 1 | $23.25 | N/A | 65 |
| 2025-07-15 16:57:02 | BUY | DIS | 1 | $119.46 | N/A | 70 |
| 2025-07-15 16:44:17 | SELL | AMZN | 1 | $226.16 | $4.11 | 70 |
| 2025-07-15 16:44:17 | SELL | UNP | 1 | $232.39 | $-3.75 | 65 |
| 2025-07-15 16:44:17 | BUY | PYPL | 1 | $73.66 | N/A | 70 |
| 2025-07-15 16:44:17 | BUY | WFC | 1 | $83.43 | N/A | 75 |
| 2025-07-15 16:44:17 | BUY | CVX | 1 | $150.73 | N/A | 85 |
| 2025-07-15 16:27:20 | SELL | WFC | 1 | $78.93 | $0.22 | 65 |
| 2025-07-15 16:27:20 | BUY | AMZN | 1 | $226.51 | N/A | 85 |
| 2025-07-15 16:27:20 | BUY | INTC | 1 | $23.31 | N/A | 65 |
| 2025-07-15 16:27:20 | BUY | UNP | 1 | $232.51 | N/A | 75 |

<!--TRADE_LOG_END--> 
