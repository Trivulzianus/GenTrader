# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 18:11:17**

| Metric | Value |
|---|---|
| **Total Value** | **$101,562.17** |
| Cash | $1,772.82 |
| Holdings Value | $99,789.35 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.51 | $2,125.10 | 70 |
| ADBE | 5 | $377.60 | $372.45 | $1,862.25 | 65 |
| AMD | 18 | $136.48 | $144.25 | $2,596.50 | 85 |
| AMZN | 11 | $221.97 | $222.72 | $2,449.87 | 85 |
| AVGO | 8 | $275.34 | $274.69 | $2,197.52 | 70 |
| AXP | 7 | $325.28 | $324.16 | $2,269.11 | 75 |
| BA | 10 | $212.37 | $224.93 | $2,249.30 | 75 |
| BAC | 49 | $48.60 | $46.97 | $2,301.53 | 75 |
| C | 30 | $86.81 | $86.76 | $2,602.80 | 85 |
| CAT | 6 | $397.86 | $409.75 | $2,458.50 | 75 |
| COST | 2 | $979.83 | $977.36 | $1,954.72 | 65 |
| CRM | 7 | $268.68 | $265.92 | $1,861.41 | 60 |
| CSCO | 33 | $68.38 | $68.86 | $2,272.28 | 75 |
| CVX | 16 | $146.72 | $154.06 | $2,464.96 | 80 |
| DIS | 18 | $122.80 | $121.24 | $2,182.32 | 70 |
| GOOGL | 13 | $179.61 | $177.74 | $2,310.62 | 70 |
| GS | 3 | $717.52 | $708.44 | $2,125.32 | 65 |
| HD | 6 | $372.64 | $377.66 | $2,265.96 | 70 |
| INTC | 84 | $22.27 | $23.89 | $2,007.18 | 65 |
| JNJ | 13 | $155.89 | $157.79 | $2,051.27 | 65 |
| JPM | 9 | $291.61 | $287.54 | $2,587.86 | 85 |
| KO | 29 | $71.03 | $69.62 | $2,018.98 | 65 |
| LLY | 2 | $776.66 | $794.43 | $1,588.86 | 70 |
| MA | 4 | $563.08 | $564.48 | $2,257.90 | 65 |
| META | 3 | $717.12 | $724.54 | $2,173.62 | 85 |
| MRK | 28 | $82.46 | $84.57 | $2,367.96 | 75 |
| MSFT | 5 | $498.84 | $501.53 | $2,507.65 | 85 |
| NFLX | 1 | $1,279.00 | $1,255.69 | $1,255.69 | 65 |
| NKE | 29 | $75.83 | $74.95 | $2,173.70 | 70 |
| NVDA | 14 | $156.60 | $164.02 | $2,296.28 | 70 |
| ORCL | 9 | $233.31 | $237.29 | $2,135.61 | 70 |
| PEP | 15 | $136.57 | $136.19 | $2,042.85 | 65 |
| PFE | 90 | $25.23 | $25.88 | $2,329.20 | 75 |
| PG | 12 | $160.91 | $159.12 | $1,909.44 | 65 |
| PYPL | 30 | $76.66 | $75.86 | $2,275.65 | 75 |
| QCOM | 16 | $161.58 | $159.74 | $2,555.84 | 85 |
| T | 73 | $28.55 | $27.69 | $2,021.09 | 65 |
| TGT | 19 | $104.85 | $106.05 | $2,014.95 | 65 |
| TSLA | 6 | $288.62 | $305.10 | $1,830.60 | 60 |
| UNH | 6 | $298.34 | $302.64 | $1,815.84 | 65 |
| UNP | 9 | $236.20 | $238.06 | $2,142.59 | 75 |
| V | 6 | $355.85 | $356.67 | $2,140.02 | 65 |
| VZ | 48 | $43.15 | $42.06 | $2,019.12 | 65 |
| WFC | 28 | $82.32 | $82.28 | $2,303.98 | 75 |
| WMT | 21 | $97.36 | $95.53 | $2,006.23 | 65 |
| XOM | 21 | $109.91 | $114.73 | $2,409.33 | 80 |

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
| 2025-07-10 18:11:08 | SELL | NVDA | 2 | $164.14 | $13.19 | 70 |
| 2025-07-10 18:11:08 | SELL | CRM | 1 | $265.90 | $-2.43 | 60 |
| 2025-07-10 18:11:08 | SELL | CVX | 1 | $154.09 | $6.93 | 80 |
| 2025-07-10 18:11:08 | BUY | AMD | 2 | $144.40 | N/A | 85 |
| 2025-07-10 18:11:08 | BUY | PFE | 7 | $25.56 | N/A | 75 |
| 2025-07-10 18:11:08 | BUY | BA | 1 | $224.96 | N/A | 75 |
| 2025-07-10 18:11:08 | BUY | QCOM | 1 | $159.74 | N/A | 85 |
| 2025-07-10 17:51:39 | SELL | XOM | 1 | $114.54 | $4.42 | 75 |
| 2025-07-10 17:51:39 | SELL | NKE | 1 | $75.21 | $-0.60 | 70 |
| 2025-07-10 17:51:39 | SELL | QCOM | 1 | $159.84 | $-1.76 | 75 |
| 2025-07-10 17:51:39 | BUY | NVDA | 2 | $164.08 | N/A | 85 |
| 2025-07-10 17:51:39 | BUY | PFE | 5 | $25.88 | N/A | 70 |
| 2025-07-10 17:51:39 | BUY | CSCO | 1 | $68.85 | N/A | 75 |
| 2025-07-10 17:51:39 | BUY | CVX | 1 | $153.77 | N/A | 85 |
| 2025-07-10 17:39:54 | SELL | PFE | 5 | $25.83 | $3.20 | 65 |
| 2025-07-10 17:39:54 | SELL | WFC | 4 | $82.40 | $0.31 | 75 |
| 2025-07-10 17:39:54 | SELL | AMD | 2 | $144.39 | $15.83 | 75 |
| 2025-07-10 17:39:54 | SELL | PG | 1 | $159.08 | $-1.69 | 60 |
| 2025-07-10 17:39:54 | SELL | CSCO | 2 | $68.84 | $0.91 | 70 |
| 2025-07-10 17:39:54 | SELL | TGT | 1 | $106.18 | $1.27 | 65 |
| 2025-07-10 17:39:54 | BUY | AMZN | 1 | $222.60 | N/A | 85 |
| 2025-07-10 17:39:54 | BUY | BAC | 1 | $46.84 | N/A | 75 |
| 2025-07-10 17:39:54 | BUY | XOM | 1 | $114.62 | N/A | 85 |
| 2025-07-10 17:39:54 | BUY | NKE | 1 | $75.40 | N/A | 75 |
| 2025-07-10 17:39:54 | BUY | PYPL | 1 | $76.17 | N/A | 75 |

<!--TRADE_LOG_END--> 
