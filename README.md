# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 16:44:44**

| Metric | Value |
|---|---|
| **Total Value** | **$100,403.13** |
| Cash | $1,759.38 |
| Holdings Value | $98,643.75 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.81 | $2,098.12 | 65 |
| ADBE | 6 | $375.23 | $360.76 | $2,164.59 | 65 |
| AMD | 15 | $145.06 | $154.78 | $2,321.70 | 70 |
| AMZN | 10 | $221.65 | $223.58 | $2,235.80 | 75 |
| AVGO | 8 | $275.34 | $278.06 | $2,224.48 | 65 |
| AXP | 6 | $308.37 | $309.52 | $1,857.12 | 65 |
| BA | 9 | $210.81 | $229.00 | $2,061.00 | 65 |
| BAC | 46 | $46.27 | $45.59 | $2,097.37 | 65 |
| C | 30 | $86.85 | $89.14 | $2,674.35 | 85 |
| CAT | 6 | $397.74 | $408.85 | $2,453.07 | 85 |
| COST | 2 | $979.83 | $955.30 | $1,910.61 | 65 |
| CRM | 8 | $267.44 | $255.86 | $2,046.88 | 65 |
| CSCO | 31 | $68.46 | $67.39 | $2,089.09 | 65 |
| CVX | 16 | $146.82 | $150.99 | $2,415.84 | 75 |
| DIS | 18 | $122.77 | $119.48 | $2,150.73 | 65 |
| GOOGL | 13 | $179.34 | $183.45 | $2,384.85 | 70 |
| GS | 3 | $717.52 | $703.10 | $2,109.30 | 70 |
| HD | 5 | $353.54 | $356.38 | $1,781.92 | 65 |
| INTC | 85 | $22.36 | $22.52 | $1,913.78 | 60 |
| JNJ | 13 | $155.43 | $165.24 | $2,148.12 | 65 |
| JPM | 9 | $291.86 | $285.92 | $2,573.28 | 85 |
| KO | 30 | $70.97 | $69.17 | $2,075.10 | 65 |
| LLY | 3 | $781.32 | $791.86 | $2,375.57 | 70 |
| MA | 4 | $563.08 | $552.26 | $2,209.04 | 65 |
| META | 3 | $717.12 | $702.80 | $2,108.40 | 75 |
| MRK | 29 | $82.47 | $81.91 | $2,375.39 | 75 |
| MSFT | 5 | $498.84 | $503.96 | $2,519.80 | 75 |
| NFLX | 1 | $1,279.00 | $1,262.14 | $1,262.14 | 65 |
| NKE | 31 | $71.99 | $71.66 | $2,221.46 | 70 |
| NVDA | 14 | $171.51 | $170.60 | $2,388.47 | 70 |
| ORCL | 9 | $232.99 | $236.59 | $2,129.31 | 70 |
| PEP | 15 | $136.57 | $134.59 | $2,018.85 | 65 |
| PFE | 84 | $25.28 | $24.64 | $2,069.76 | 65 |
| PG | 14 | $152.15 | $152.89 | $2,140.46 | 65 |
| PYPL | 29 | $72.15 | $72.46 | $2,101.34 | 65 |
| QCOM | 14 | $153.83 | $153.03 | $2,142.42 | 65 |
| T | 77 | $27.09 | $27.03 | $2,081.31 | 65 |
| TGT | 20 | $104.94 | $100.88 | $2,017.60 | 65 |
| TSLA | 6 | $318.51 | $320.72 | $1,924.33 | 65 |
| UNH | 7 | $298.51 | $292.85 | $2,049.95 | 65 |
| UNP | 9 | $236.78 | $230.75 | $2,076.80 | 65 |
| V | 6 | $355.85 | $348.90 | $2,093.40 | 65 |
| VZ | 50 | $43.08 | $41.32 | $2,066.00 | 65 |
| WFC | 27 | $78.80 | $79.21 | $2,138.67 | 65 |
| WMT | 22 | $97.29 | $94.90 | $2,087.80 | 65 |
| XOM | 20 | $109.85 | $112.92 | $2,258.40 | 70 |

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
| 2025-07-16 16:44:38 | SELL | NVDA | 1 | $170.57 | $-0.88 | 70 |
| 2025-07-16 16:44:38 | BUY | JPM | 1 | $285.90 | N/A | 85 |
| 2025-07-16 16:27:27 | SELL | BAC | 6 | $45.40 | $-4.57 | 65 |
| 2025-07-16 16:27:27 | SELL | XOM | 1 | $112.82 | $2.82 | 70 |
| 2025-07-16 16:27:27 | BUY | GOOGL | 1 | $183.03 | N/A | 75 |
| 2025-07-16 16:27:27 | BUY | NKE | 2 | $71.71 | N/A | 70 |
| 2025-07-16 16:27:27 | BUY | C | 1 | $89.26 | N/A | 85 |
| 2025-07-16 16:10:20 | SELL | GOOGL | 1 | $183.52 | $4.15 | 65 |
| 2025-07-16 16:10:20 | SELL | INTC | 1 | $22.47 | $0.11 | 60 |
| 2025-07-16 16:10:20 | SELL | NKE | 2 | $71.78 | $-0.42 | 65 |
| 2025-07-16 16:10:20 | SELL | WFC | 1 | $78.95 | $0.15 | 65 |
| 2025-07-16 16:10:20 | BUY | NVDA | 2 | $170.34 | N/A | 85 |
| 2025-07-16 16:10:20 | BUY | AMD | 1 | $154.88 | N/A | 75 |
| 2025-07-16 16:10:20 | BUY | BAC | 6 | $45.49 | N/A | 75 |
| 2025-07-16 16:10:20 | BUY | C | 2 | $90.72 | N/A | 85 |
| 2025-07-16 15:52:09 | SELL | NVDA | 3 | $170.08 | $-3.74 | 65 |
| 2025-07-16 15:52:09 | SELL | ORCL | 1 | $235.34 | $2.11 | 65 |
| 2025-07-16 15:52:09 | SELL | CVX | 2 | $150.21 | $6.01 | 75 |
| 2025-07-16 15:52:09 | BUY | NKE | 2 | $71.46 | N/A | 70 |
| 2025-07-16 15:52:09 | BUY | C | 3 | $88.84 | N/A | 75 |
| 2025-07-16 15:52:09 | BUY | WFC | 2 | $78.71 | N/A | 70 |
| 2025-07-16 15:40:59 | SELL | JPM | 1 | $283.89 | $-7.74 | 70 |
| 2025-07-16 15:40:59 | SELL | C | 1 | $88.51 | $2.24 | 65 |
| 2025-07-16 15:40:59 | BUY | NVDA | 2 | $169.67 | N/A | 85 |
| 2025-07-16 15:40:59 | BUY | BAC | 1 | $45.12 | N/A | 65 |

<!--TRADE_LOG_END--> 
