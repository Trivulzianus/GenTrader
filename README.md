# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 17:51:45**

| Metric | Value |
|---|---|
| **Total Value** | **$101,548.23** |
| Cash | $1,876.98 |
| Holdings Value | $99,671.25 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.55 | $2,125.46 | 75 |
| ADBE | 5 | $377.60 | $372.50 | $1,862.50 | 65 |
| AMD | 16 | $135.49 | $144.41 | $2,310.64 | 75 |
| AMZN | 11 | $221.97 | $222.43 | $2,446.73 | 85 |
| AVGO | 8 | $275.34 | $274.80 | $2,198.40 | 70 |
| AXP | 7 | $325.28 | $324.73 | $2,273.11 | 75 |
| BA | 9 | $210.97 | $224.97 | $2,024.68 | 70 |
| BAC | 49 | $48.60 | $47.03 | $2,304.71 | 75 |
| C | 30 | $86.81 | $86.86 | $2,605.80 | 85 |
| CAT | 6 | $397.86 | $409.47 | $2,456.82 | 75 |
| COST | 2 | $979.83 | $974.41 | $1,948.83 | 70 |
| CRM | 8 | $268.33 | $266.71 | $2,133.72 | 65 |
| CSCO | 33 | $68.38 | $68.85 | $2,272.05 | 75 |
| CVX | 17 | $147.16 | $153.71 | $2,613.07 | 85 |
| DIS | 18 | $122.80 | $121.36 | $2,184.48 | 70 |
| GOOGL | 13 | $179.61 | $177.62 | $2,309.05 | 70 |
| GS | 3 | $717.52 | $707.79 | $2,123.38 | 70 |
| HD | 6 | $372.64 | $377.44 | $2,264.67 | 65 |
| INTC | 84 | $22.27 | $23.82 | $2,001.30 | 65 |
| JNJ | 13 | $155.89 | $157.57 | $2,048.41 | 65 |
| JPM | 9 | $291.61 | $287.36 | $2,586.24 | 85 |
| KO | 29 | $71.03 | $69.52 | $2,015.93 | 65 |
| LLY | 2 | $776.66 | $795.23 | $1,590.46 | 65 |
| MA | 4 | $563.08 | $564.38 | $2,257.50 | 65 |
| META | 3 | $717.12 | $725.54 | $2,176.63 | 75 |
| MRK | 28 | $82.46 | $84.68 | $2,371.04 | 75 |
| MSFT | 5 | $498.84 | $501.24 | $2,506.22 | 70 |
| NFLX | 1 | $1,279.00 | $1,250.58 | $1,250.58 | 65 |
| NKE | 29 | $75.83 | $75.20 | $2,180.95 | 70 |
| NVDA | 16 | $157.54 | $164.16 | $2,626.56 | 85 |
| ORCL | 9 | $233.31 | $236.77 | $2,130.93 | 75 |
| PEP | 15 | $136.57 | $136.15 | $2,042.25 | 70 |
| PFE | 83 | $25.20 | $25.88 | $2,147.62 | 70 |
| PG | 12 | $160.91 | $158.83 | $1,905.96 | 65 |
| PYPL | 30 | $76.66 | $76.10 | $2,283.00 | 75 |
| QCOM | 15 | $161.71 | $159.83 | $2,397.45 | 75 |
| T | 73 | $28.55 | $27.64 | $2,017.72 | 65 |
| TGT | 19 | $104.85 | $106.27 | $2,019.13 | 65 |
| TSLA | 6 | $288.62 | $304.00 | $1,824.00 | 60 |
| UNH | 6 | $298.34 | $302.80 | $1,816.80 | 65 |
| UNP | 9 | $236.20 | $238.22 | $2,143.93 | 75 |
| V | 6 | $355.85 | $356.96 | $2,141.76 | 70 |
| VZ | 48 | $43.15 | $41.98 | $2,015.28 | 65 |
| WFC | 28 | $82.32 | $82.47 | $2,309.02 | 75 |
| WMT | 21 | $97.36 | $95.34 | $2,002.16 | 65 |
| XOM | 21 | $109.91 | $114.49 | $2,404.29 | 75 |

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
| 2025-07-10 17:39:54 | BUY | QCOM | 1 | $159.84 | N/A | 85 |
| 2025-07-10 17:39:54 | BUY | CVX | 1 | $153.91 | N/A | 85 |
| 2025-07-10 17:25:53 | SELL | NVDA | 2 | $163.37 | $11.84 | 70 |
| 2025-07-10 17:25:53 | SELL | XOM | 1 | $114.53 | $4.41 | 75 |
| 2025-07-10 17:25:53 | SELL | PYPL | 2 | $76.08 | $-1.11 | 70 |
| 2025-07-10 17:25:53 | SELL | CVX | 2 | $153.84 | $13.36 | 75 |
| 2025-07-10 17:25:53 | BUY | INTC | 5 | $23.72 | N/A | 65 |

<!--TRADE_LOG_END--> 
