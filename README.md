# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 17:51:01**

| Metric | Value |
|---|---|
| **Total Value** | **$100,825.51** |
| Cash | $1,491.83 |
| Holdings Value | $99,333.69 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.17 | $2,111.70 | 70 |
| ADBE | 5 | $377.60 | $364.45 | $1,822.24 | 65 |
| AMD | 16 | $135.44 | $146.48 | $2,343.68 | 75 |
| AMZN | 11 | $221.97 | $225.58 | $2,481.38 | 75 |
| AVGO | 8 | $275.34 | $273.90 | $2,191.20 | 70 |
| AXP | 7 | $325.34 | $320.71 | $2,244.97 | 75 |
| BA | 10 | $212.47 | $227.48 | $2,274.80 | 75 |
| BAC | 47 | $48.70 | $46.58 | $2,189.03 | 70 |
| C | 25 | $86.67 | $86.61 | $2,165.12 | 70 |
| CAT | 5 | $396.39 | $404.96 | $2,024.80 | 70 |
| COST | 2 | $979.83 | $969.54 | $1,939.07 | 65 |
| CRM | 7 | $268.68 | $259.24 | $1,814.68 | 65 |
| CSCO | 31 | $68.42 | $67.80 | $2,101.64 | 65 |
| CVX | 17 | $147.16 | $155.53 | $2,644.09 | 80 |
| DIS | 17 | $122.96 | $120.42 | $2,047.14 | 65 |
| GOOGL | 13 | $179.61 | $180.33 | $2,344.29 | 75 |
| GS | 3 | $717.52 | $702.40 | $2,107.21 | 85 |
| HD | 6 | $372.64 | $369.64 | $2,217.84 | 65 |
| INTC | 87 | $22.36 | $23.50 | $2,044.07 | 65 |
| JNJ | 13 | $155.89 | $156.77 | $2,038.01 | 65 |
| JPM | 9 | $291.61 | $286.76 | $2,580.84 | 80 |
| KO | 29 | $71.02 | $70.12 | $2,033.62 | 65 |
| LLY | 3 | $781.32 | $783.68 | $2,351.04 | 70 |
| MA | 4 | $563.08 | $548.90 | $2,195.62 | 65 |
| META | 3 | $717.12 | $717.75 | $2,153.26 | 75 |
| MRK | 25 | $82.29 | $83.09 | $2,077.25 | 65 |
| MSFT | 5 | $498.84 | $504.15 | $2,520.77 | 85 |
| NFLX | 1 | $1,279.00 | $1,236.81 | $1,236.81 | 65 |
| NKE | 32 | $75.67 | $72.72 | $2,326.93 | 75 |
| NVDA | 16 | $157.38 | $166.00 | $2,656.08 | 85 |
| ORCL | 9 | $233.26 | $231.39 | $2,082.51 | 65 |
| PEP | 15 | $136.57 | $134.68 | $2,020.20 | 65 |
| PFE | 80 | $25.17 | $25.65 | $2,051.90 | 65 |
| PG | 13 | $160.78 | $157.15 | $2,042.89 | 65 |
| PYPL | 31 | $76.58 | $74.49 | $2,309.30 | 75 |
| QCOM | 13 | $162.18 | $158.13 | $2,055.69 | 65 |
| T | 76 | $27.11 | $27.00 | $2,052.36 | 65 |
| TGT | 20 | $104.91 | $104.60 | $2,092.00 | 65 |
| TSLA | 6 | $288.62 | $310.57 | $1,863.43 | 65 |
| UNH | 7 | $298.51 | $301.89 | $2,113.23 | 65 |
| UNP | 10 | $236.18 | $234.68 | $2,346.75 | 75 |
| V | 6 | $355.85 | $347.04 | $2,082.21 | 65 |
| VZ | 49 | $43.12 | $41.75 | $2,045.99 | 65 |
| WFC | 29 | $82.28 | $82.33 | $2,387.63 | 75 |
| WMT | 22 | $97.25 | $94.61 | $2,081.53 | 65 |
| XOM | 21 | $109.97 | $115.57 | $2,426.87 | 75 |

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
| 2025-07-11 17:50:55 | SELL | DIS | 1 | $120.42 | $-2.40 | 65 |
| 2025-07-11 17:50:55 | SELL | PG | 1 | $157.15 | $-3.37 | 65 |
| 2025-07-11 17:50:55 | SELL | CSCO | 2 | $67.79 | $-1.18 | 65 |
| 2025-07-11 17:50:55 | BUY | AMD | 1 | $146.52 | N/A | 75 |
| 2025-07-11 17:50:55 | BUY | NKE | 1 | $72.71 | N/A | 75 |
| 2025-07-11 17:50:55 | BUY | PYPL | 2 | $74.49 | N/A | 75 |
| 2025-07-11 17:39:21 | SELL | PFE | 6 | $25.67 | $2.77 | 65 |
| 2025-07-11 17:39:21 | BUY | AMD | 1 | $146.68 | N/A | 70 |
| 2025-07-11 17:39:21 | BUY | INTC | 1 | $23.49 | N/A | 65 |
| 2025-07-11 17:39:21 | BUY | PG | 1 | $156.99 | N/A | 70 |
| 2025-07-11 17:39:21 | BUY | T | 1 | $26.92 | N/A | 65 |
| 2025-07-11 17:25:53 | SELL | XOM | 2 | $115.33 | $9.80 | 75 |
| 2025-07-11 17:25:53 | SELL | CSCO | 1 | $67.88 | $-0.49 | 70 |
| 2025-07-11 17:25:53 | BUY | INTC | 5 | $23.55 | N/A | 65 |
| 2025-07-11 17:25:53 | BUY | DIS | 1 | $120.27 | N/A | 70 |
| 2025-07-11 17:25:53 | BUY | PYPL | 1 | $74.60 | N/A | 70 |
| 2025-07-11 17:25:53 | BUY | C | 1 | $86.52 | N/A | 70 |
| 2025-07-11 17:25:53 | BUY | T | 5 | $26.97 | N/A | 65 |
| 2025-07-11 17:08:48 | SELL | INTC | 5 | $23.48 | $5.67 | 60 |
| 2025-07-11 17:08:48 | SELL | AMD | 4 | $147.03 | $41.02 | 65 |
| 2025-07-11 17:08:48 | SELL | NKE | 1 | $72.68 | $-3.00 | 70 |
| 2025-07-11 17:08:48 | SELL | PYPL | 3 | $74.58 | $-6.01 | 65 |
| 2025-07-11 17:08:48 | SELL | WFC | 1 | $82.36 | $0.07 | 75 |
| 2025-07-11 17:08:48 | SELL | C | 1 | $86.60 | $-0.08 | 65 |
| 2025-07-11 17:08:48 | BUY | XOM | 2 | $115.29 | N/A | 85 |

<!--TRADE_LOG_END--> 
