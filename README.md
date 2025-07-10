# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 16:44:10**

| Metric | Value |
|---|---|
| **Total Value** | **$101,487.62** |
| Cash | $2,492.83 |
| Holdings Value | $98,994.79 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.24 | $2,122.35 | 70 |
| ADBE | 5 | $377.60 | $372.21 | $1,861.05 | 65 |
| AMD | 15 | $134.94 | $144.41 | $2,166.15 | 70 |
| AMZN | 10 | $221.91 | $221.97 | $2,219.70 | 75 |
| AVGO | 8 | $275.34 | $274.48 | $2,195.84 | 70 |
| AXP | 7 | $325.28 | $323.49 | $2,264.43 | 75 |
| BA | 9 | $210.97 | $224.11 | $2,016.99 | 70 |
| BAC | 46 | $48.71 | $47.06 | $2,164.76 | 70 |
| C | 26 | $86.81 | $86.78 | $2,256.28 | 70 |
| CAT | 6 | $397.86 | $410.25 | $2,461.50 | 75 |
| COST | 2 | $979.83 | $975.10 | $1,950.20 | 65 |
| CRM | 8 | $268.33 | $266.53 | $2,132.24 | 65 |
| CSCO | 34 | $68.39 | $68.86 | $2,341.07 | 75 |
| CVX | 17 | $147.16 | $153.75 | $2,613.66 | 85 |
| DIS | 18 | $122.80 | $121.24 | $2,182.32 | 70 |
| GOOGL | 13 | $179.61 | $177.10 | $2,302.30 | 70 |
| GS | 3 | $717.52 | $707.20 | $2,121.59 | 75 |
| HD | 6 | $372.64 | $376.87 | $2,261.22 | 70 |
| INTC | 79 | $22.17 | $23.72 | $1,874.14 | 60 |
| JNJ | 13 | $155.89 | $157.92 | $2,052.96 | 65 |
| JPM | 9 | $291.61 | $287.04 | $2,583.36 | 85 |
| KO | 29 | $71.03 | $69.53 | $2,016.25 | 65 |
| LLY | 2 | $776.66 | $792.22 | $1,584.44 | 70 |
| MA | 4 | $563.08 | $563.08 | $2,252.32 | 70 |
| META | 3 | $717.12 | $725.87 | $2,177.61 | 75 |
| MRK | 28 | $82.46 | $84.53 | $2,366.98 | 75 |
| MSFT | 5 | $498.84 | $500.29 | $2,501.43 | 85 |
| NFLX | 1 | $1,279.00 | $1,255.89 | $1,255.89 | 65 |
| NKE | 30 | $75.81 | $75.45 | $2,263.50 | 75 |
| NVDA | 14 | $156.61 | $163.48 | $2,288.77 | 70 |
| ORCL | 9 | $233.31 | $236.02 | $2,124.18 | 70 |
| PEP | 15 | $136.57 | $136.37 | $2,045.48 | 65 |
| PFE | 78 | $25.16 | $25.82 | $2,013.95 | 65 |
| PG | 13 | $160.77 | $159.28 | $2,070.64 | 65 |
| PYPL | 31 | $76.64 | $76.11 | $2,359.41 | 75 |
| QCOM | 15 | $161.71 | $159.96 | $2,399.40 | 75 |
| T | 73 | $28.55 | $27.56 | $2,011.88 | 65 |
| TGT | 20 | $104.91 | $105.98 | $2,119.60 | 70 |
| TSLA | 6 | $288.62 | $304.74 | $1,828.46 | 65 |
| UNH | 6 | $298.34 | $302.46 | $1,814.76 | 65 |
| UNP | 9 | $236.20 | $238.71 | $2,148.39 | 75 |
| V | 6 | $355.85 | $355.94 | $2,135.64 | 70 |
| VZ | 48 | $43.15 | $41.94 | $2,013.00 | 65 |
| WFC | 32 | $82.33 | $82.58 | $2,642.72 | 85 |
| WMT | 21 | $97.36 | $95.78 | $2,011.28 | 65 |
| XOM | 21 | $109.91 | $114.51 | $2,404.71 | 75 |

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
| 2025-07-10 16:44:03 | SELL | NVDA | 1 | $163.45 | $6.38 | 70 |
| 2025-07-10 16:44:03 | SELL | INTC | 4 | $23.73 | $5.91 | 60 |
| 2025-07-10 16:44:03 | SELL | XOM | 2 | $114.51 | $8.41 | 75 |
| 2025-07-10 16:44:03 | SELL | C | 4 | $86.78 | $-0.13 | 70 |
| 2025-07-10 16:44:03 | SELL | QCOM | 1 | $159.93 | $-1.67 | 75 |
| 2025-07-10 16:44:03 | BUY | PFE | 1 | $25.82 | N/A | 65 |
| 2025-07-10 16:27:11 | SELL | BAC | 1 | $47.10 | $-1.58 | 70 |
| 2025-07-10 16:27:11 | SELL | PFE | 2 | $25.82 | $1.31 | 65 |
| 2025-07-10 16:27:11 | SELL | MRK | 3 | $84.41 | $5.29 | 75 |
| 2025-07-10 16:27:11 | SELL | VZ | 1 | $41.99 | $-1.13 | 65 |
| 2025-07-10 16:27:11 | SELL | T | 1 | $27.58 | $-0.96 | 65 |
| 2025-07-10 16:27:11 | BUY | NVDA | 1 | $163.26 | N/A | 85 |
| 2025-07-10 16:27:11 | BUY | INTC | 3 | $23.72 | N/A | 65 |
| 2025-07-10 16:27:11 | BUY | NKE | 1 | $75.41 | N/A | 75 |
| 2025-07-10 16:27:11 | BUY | QCOM | 1 | $159.70 | N/A | 85 |
| 2025-07-10 16:09:41 | SELL | NVDA | 2 | $162.90 | $10.99 | 70 |
| 2025-07-10 16:09:41 | SELL | INTC | 6 | $23.75 | $8.66 | 60 |
| 2025-07-10 16:09:41 | BUY | MRK | 3 | $84.54 | N/A | 85 |
| 2025-07-10 16:09:41 | BUY | WFC | 3 | $82.56 | N/A | 85 |
| 2025-07-10 16:09:41 | BUY | CSCO | 1 | $68.98 | N/A | 75 |
| 2025-07-10 15:52:49 | SELL | AMZN | 1 | $221.79 | $-0.11 | 70 |
| 2025-07-10 15:52:49 | SELL | AMD | 1 | $144.29 | $8.77 | 65 |
| 2025-07-10 15:52:49 | SELL | BAC | 2 | $47.06 | $-3.10 | 70 |
| 2025-07-10 15:52:49 | SELL | PFE | 5 | $25.83 | $3.11 | 65 |
| 2025-07-10 15:52:49 | SELL | QCOM | 1 | $159.69 | $-1.91 | 75 |

<!--TRADE_LOG_END--> 
