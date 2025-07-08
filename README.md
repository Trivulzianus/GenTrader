# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 16:55:28**

| Metric | Value |
|---|---|
| **Total Value** | **$100,853.28** |
| Cash | $996.08 |
| Holdings Value | $99,857.20 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.56 | $2,105.62 | 70 |
| ADBE | 5 | $377.60 | $382.42 | $1,912.10 | 65 |
| AMD | 16 | $135.69 | $138.10 | $2,209.60 | 70 |
| AMZN | 10 | $221.61 | $220.64 | $2,206.37 | 65 |
| AVGO | 8 | $275.34 | $275.49 | $2,203.92 | 70 |
| AXP | 8 | $324.24 | $320.06 | $2,560.48 | 85 |
| BA | 9 | $211.84 | $217.59 | $1,958.36 | 65 |
| BAC | 49 | $48.66 | $47.19 | $2,312.31 | 75 |
| C | 31 | $86.59 | $86.13 | $2,670.03 | 85 |
| CAT | 6 | $397.86 | $393.47 | $2,360.82 | 65 |
| COST | 2 | $979.83 | $989.88 | $1,979.77 | 65 |
| CRM | 8 | $268.33 | $274.45 | $2,195.64 | 65 |
| CSCO | 32 | $68.35 | $68.70 | $2,198.40 | 70 |
| CVX | 16 | $146.69 | $152.30 | $2,436.80 | 75 |
| DIS | 17 | $122.85 | $122.34 | $2,079.78 | 70 |
| GOOGL | 12 | $179.60 | $174.13 | $2,089.56 | 65 |
| GS | 3 | $717.52 | $699.23 | $2,097.69 | 70 |
| HD | 6 | $372.64 | $368.38 | $2,210.28 | 65 |
| INTC | 86 | $22.32 | $23.43 | $2,014.98 | 60 |
| JNJ | 14 | $155.85 | $155.94 | $2,183.16 | 65 |
| JPM | 9 | $291.61 | $281.63 | $2,534.72 | 80 |
| KO | 29 | $71.03 | $70.22 | $2,036.38 | 65 |
| LLY | 2 | $776.66 | $791.00 | $1,582.00 | 65 |
| MA | 4 | $563.08 | $563.00 | $2,252.00 | 65 |
| META | 3 | $717.12 | $720.73 | $2,162.19 | 75 |
| MRK | 29 | $82.49 | $81.90 | $2,375.10 | 75 |
| MSFT | 5 | $498.84 | $496.02 | $2,480.10 | 75 |
| NFLX | 1 | $1,279.00 | $1,276.35 | $1,276.35 | 65 |
| NKE | 30 | $75.91 | $73.99 | $2,219.70 | 70 |
| NVDA | 16 | $156.90 | $159.69 | $2,555.04 | 85 |
| ORCL | 9 | $233.41 | $236.93 | $2,132.33 | 70 |
| PEP | 15 | $136.57 | $134.93 | $2,023.95 | 65 |
| PFE | 87 | $25.25 | $25.64 | $2,231.11 | 70 |
| PG | 13 | $160.77 | $158.45 | $2,059.85 | 65 |
| PYPL | 31 | $76.64 | $74.77 | $2,317.87 | 75 |
| QCOM | 14 | $161.75 | $160.59 | $2,248.26 | 75 |
| T | 73 | $28.54 | $28.29 | $2,065.51 | 65 |
| TGT | 20 | $104.90 | $101.48 | $2,029.60 | 65 |
| TSLA | 6 | $288.62 | $301.33 | $1,807.95 | 65 |
| UNH | 7 | $314.75 | $305.96 | $2,141.70 | 65 |
| UNP | 10 | $236.66 | $236.77 | $2,367.72 | 75 |
| V | 6 | $355.95 | $355.24 | $2,131.44 | 65 |
| VZ | 47 | $43.72 | $43.02 | $2,021.70 | 65 |
| WFC | 29 | $82.34 | $81.78 | $2,371.76 | 75 |
| WMT | 21 | $97.39 | $97.78 | $2,053.28 | 65 |
| XOM | 21 | $110.00 | $114.00 | $2,393.89 | 75 |

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
| 2025-07-08 16:55:22 | SELL | INTC | 1 | $22.00 | $-0.32 | 60 |
| 2025-07-08 16:55:22 | SELL | WMT | 1 | $97.77 | $0.37 | 65 |
| 2025-07-08 16:55:22 | SELL | MRK | 3 | $81.90 | $-1.60 | 75 |
| 2025-07-08 16:55:22 | SELL | T | 5 | $28.30 | $-1.15 | 65 |
| 2025-07-08 16:55:22 | BUY | NVDA | 2 | $159.71 | N/A | 85 |
| 2025-07-08 16:55:22 | BUY | PFE | 7 | $25.24 | N/A | 70 |
| 2025-07-08 16:55:22 | BUY | C | 1 | $86.14 | N/A | 85 |
| 2025-07-08 16:43:31 | SELL | NVDA | 2 | $158.24 | $3.04 | 70 |
| 2025-07-08 16:43:31 | SELL | T | 4 | $28.33 | $-0.74 | 70 |
| 2025-07-08 16:43:31 | SELL | WFC | 1 | $81.65 | $-0.66 | 75 |
| 2025-07-08 16:43:31 | BUY | INTC | 1 | $23.38 | N/A | 65 |
| 2025-07-08 16:43:31 | BUY | BAC | 3 | $47.17 | N/A | 75 |
| 2025-07-08 16:28:46 | SELL | PFE | 12 | $25.68 | $4.43 | 65 |
| 2025-07-08 16:28:46 | SELL | CSCO | 2 | $68.78 | $0.81 | 70 |
| 2025-07-08 16:28:46 | BUY | NVDA | 2 | $159.84 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | INTC | 4 | $23.38 | N/A | 65 |
| 2025-07-08 16:28:46 | BUY | WMT | 1 | $97.81 | N/A | 70 |
| 2025-07-08 16:28:46 | BUY | MRK | 5 | $82.31 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | WFC | 1 | $81.61 | N/A | 80 |
| 2025-07-08 16:28:46 | BUY | C | 2 | $86.18 | N/A | 85 |
| 2025-07-08 16:28:46 | BUY | T | 5 | $28.36 | N/A | 75 |
| 2025-07-08 16:09:53 | SELL | XOM | 2 | $113.31 | $6.04 | 75 |
| 2025-07-08 16:09:53 | SELL | WMT | 3 | $97.66 | $0.72 | 65 |
| 2025-07-08 16:09:53 | SELL | MRK | 2 | $81.93 | $-0.99 | 70 |
| 2025-07-08 16:09:53 | SELL | C | 3 | $85.91 | $-1.96 | 75 |

<!--TRADE_LOG_END--> 
