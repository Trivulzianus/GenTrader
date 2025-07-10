# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 16:09:47**

| Metric | Value |
|---|---|
| **Total Value** | **$101,476.82** |
| Cash | $1,572.23 |
| Holdings Value | $99,904.59 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.20 | $2,122.00 | 70 |
| ADBE | 5 | $377.60 | $371.14 | $1,855.70 | 65 |
| AMD | 15 | $134.94 | $143.83 | $2,157.45 | 65 |
| AMZN | 10 | $221.91 | $221.95 | $2,219.48 | 75 |
| AVGO | 8 | $275.34 | $274.09 | $2,192.72 | 65 |
| AXP | 7 | $325.28 | $323.98 | $2,267.83 | 75 |
| BA | 9 | $210.97 | $224.77 | $2,022.93 | 65 |
| BAC | 47 | $48.67 | $47.12 | $2,214.88 | 70 |
| C | 30 | $86.81 | $86.92 | $2,607.75 | 85 |
| CAT | 6 | $397.86 | $410.88 | $2,465.31 | 70 |
| COST | 2 | $979.83 | $975.00 | $1,950.00 | 65 |
| CRM | 8 | $268.33 | $266.63 | $2,133.07 | 65 |
| CSCO | 34 | $68.39 | $68.95 | $2,344.30 | 75 |
| CVX | 17 | $147.16 | $153.69 | $2,612.64 | 85 |
| DIS | 18 | $122.80 | $121.36 | $2,184.39 | 70 |
| GOOGL | 13 | $179.61 | $176.43 | $2,293.59 | 70 |
| GS | 3 | $717.52 | $707.55 | $2,122.66 | 70 |
| HD | 6 | $372.64 | $376.11 | $2,256.66 | 70 |
| INTC | 80 | $22.19 | $23.75 | $1,900.00 | 60 |
| JNJ | 13 | $155.89 | $158.17 | $2,056.21 | 65 |
| JPM | 9 | $291.61 | $287.10 | $2,583.90 | 85 |
| KO | 29 | $71.03 | $69.52 | $2,016.08 | 65 |
| LLY | 2 | $776.66 | $793.11 | $1,586.22 | 65 |
| MA | 4 | $563.08 | $563.95 | $2,255.78 | 70 |
| META | 3 | $717.12 | $726.15 | $2,178.45 | 85 |
| MRK | 31 | $82.65 | $84.52 | $2,620.12 | 85 |
| MSFT | 5 | $498.84 | $499.74 | $2,498.70 | 75 |
| NFLX | 1 | $1,279.00 | $1,262.92 | $1,262.92 | 65 |
| NKE | 29 | $75.82 | $75.21 | $2,181.09 | 70 |
| NVDA | 14 | $156.62 | $162.83 | $2,279.62 | 70 |
| ORCL | 9 | $233.31 | $235.51 | $2,119.62 | 70 |
| PEP | 15 | $136.57 | $136.34 | $2,045.10 | 65 |
| PFE | 79 | $25.16 | $25.89 | $2,045.70 | 65 |
| PG | 13 | $160.77 | $159.05 | $2,067.65 | 65 |
| PYPL | 31 | $76.64 | $75.94 | $2,354.14 | 75 |
| QCOM | 15 | $161.72 | $159.89 | $2,398.35 | 75 |
| T | 74 | $28.53 | $27.61 | $2,043.51 | 65 |
| TGT | 20 | $104.91 | $105.72 | $2,114.40 | 65 |
| TSLA | 6 | $288.62 | $304.12 | $1,824.74 | 60 |
| UNH | 6 | $298.34 | $301.32 | $1,807.92 | 65 |
| UNP | 9 | $236.20 | $238.74 | $2,148.66 | 75 |
| V | 6 | $355.85 | $356.16 | $2,136.96 | 65 |
| VZ | 49 | $43.12 | $42.02 | $2,058.74 | 65 |
| WFC | 32 | $82.33 | $82.53 | $2,641.12 | 85 |
| WMT | 21 | $97.36 | $95.92 | $2,014.22 | 65 |
| XOM | 23 | $110.31 | $114.84 | $2,641.32 | 85 |

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
| 2025-07-10 15:52:49 | BUY | NKE | 2 | $75.04 | N/A | 70 |
| 2025-07-10 15:52:49 | BUY | CSCO | 1 | $68.96 | N/A | 75 |
| 2025-07-10 15:40:57 | SELL | MRK | 1 | $84.34 | $1.83 | 75 |
| 2025-07-10 15:40:57 | SELL | NKE | 1 | $75.13 | $-0.73 | 65 |
| 2025-07-10 15:40:57 | SELL | CSCO | 1 | $68.93 | $0.55 | 70 |
| 2025-07-10 15:40:57 | SELL | T | 1 | $27.53 | $-0.98 | 65 |
| 2025-07-10 15:40:57 | SELL | TGT | 1 | $105.33 | $0.41 | 65 |
| 2025-07-10 15:40:57 | BUY | NVDA | 2 | $162.68 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | BAC | 1 | $47.15 | N/A | 75 |
| 2025-07-10 15:40:57 | BUY | XOM | 2 | $114.72 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | PFE | 4 | $25.91 | N/A | 70 |
| 2025-07-10 15:40:57 | BUY | C | 3 | $86.85 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | QCOM | 1 | $159.79 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | WMT | 1 | $95.80 | N/A | 65 |
| 2025-07-10 15:26:42 | SELL | BAC | 2 | $47.16 | $-2.84 | 70 |

<!--TRADE_LOG_END--> 
