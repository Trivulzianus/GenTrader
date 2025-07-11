# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 14:26:02**

| Metric | Value |
|---|---|
| **Total Value** | **$100,791.72** |
| Cash | $1,064.00 |
| Holdings Value | $99,727.72 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.84 | $2,118.45 | 70 |
| ADBE | 5 | $377.60 | $368.64 | $1,843.22 | 65 |
| AMD | 16 | $135.79 | $143.72 | $2,299.52 | 75 |
| AMZN | 11 | $221.97 | $224.44 | $2,468.84 | 75 |
| AVGO | 8 | $275.34 | $273.56 | $2,188.52 | 65 |
| AXP | 7 | $325.34 | $323.46 | $2,264.25 | 75 |
| BA | 9 | $210.85 | $227.75 | $2,049.76 | 65 |
| BAC | 45 | $48.80 | $46.45 | $2,090.47 | 65 |
| C | 25 | $86.67 | $86.00 | $2,150.12 | 70 |
| CAT | 6 | $397.86 | $404.33 | $2,426.00 | 65 |
| COST | 2 | $979.83 | $968.98 | $1,937.96 | 65 |
| CRM | 7 | $268.68 | $261.09 | $1,827.63 | 65 |
| CSCO | 32 | $68.36 | $68.38 | $2,188.00 | 70 |
| CVX | 17 | $147.15 | $154.59 | $2,628.03 | 85 |
| DIS | 18 | $122.81 | $120.71 | $2,172.78 | 65 |
| GOOGL | 13 | $179.61 | $177.55 | $2,308.15 | 70 |
| GS | 3 | $717.52 | $705.01 | $2,115.02 | 70 |
| HD | 6 | $372.64 | $367.93 | $2,207.58 | 70 |
| INTC | 82 | $22.29 | $23.45 | $1,923.31 | 60 |
| JNJ | 13 | $155.89 | $155.97 | $2,027.61 | 65 |
| JPM | 9 | $291.61 | $285.31 | $2,567.79 | 75 |
| KO | 29 | $71.03 | $69.79 | $2,023.91 | 65 |
| LLY | 3 | $781.32 | $783.65 | $2,350.95 | 70 |
| MA | 4 | $563.08 | $556.28 | $2,225.12 | 65 |
| META | 3 | $717.12 | $716.60 | $2,149.80 | 85 |
| MRK | 25 | $82.30 | $83.00 | $2,075.12 | 65 |
| MSFT | 5 | $498.84 | $502.04 | $2,510.18 | 75 |
| NFLX | 1 | $1,279.00 | $1,249.88 | $1,249.88 | 65 |
| NKE | 32 | $75.67 | $73.20 | $2,342.40 | 75 |
| NVDA | 16 | $157.38 | $167.04 | $2,672.56 | 85 |
| ORCL | 10 | $233.21 | $232.43 | $2,324.30 | 70 |
| PEP | 15 | $136.57 | $134.73 | $2,020.95 | 65 |
| PFE | 86 | $25.20 | $25.55 | $2,197.73 | 70 |
| PG | 14 | $160.52 | $157.10 | $2,199.40 | 65 |
| PYPL | 29 | $76.75 | $74.83 | $2,170.07 | 70 |
| QCOM | 13 | $162.18 | $157.83 | $2,051.79 | 65 |
| T | 76 | $27.10 | $26.96 | $2,048.96 | 65 |
| TGT | 20 | $104.92 | $103.95 | $2,079.00 | 65 |
| TSLA | 6 | $288.62 | $311.54 | $1,869.24 | 65 |
| UNH | 7 | $298.51 | $299.77 | $2,098.39 | 65 |
| UNP | 10 | $236.18 | $235.32 | $2,353.20 | 75 |
| V | 6 | $355.85 | $350.83 | $2,105.01 | 65 |
| VZ | 46 | $43.21 | $41.70 | $1,918.20 | 60 |
| WFC | 29 | $82.28 | $81.98 | $2,377.42 | 75 |
| WMT | 22 | $97.25 | $95.12 | $2,092.64 | 65 |
| XOM | 21 | $109.91 | $115.17 | $2,418.47 | 75 |

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
| 2025-07-11 14:25:53 | SELL | BAC | 2 | $46.44 | $-4.51 | 65 |
| 2025-07-11 14:25:53 | SELL | VZ | 3 | $41.69 | $-4.28 | 60 |
| 2025-07-11 14:25:53 | BUY | C | 2 | $86.00 | N/A | 70 |
| 2025-07-11 14:25:53 | BUY | WFC | 1 | $81.96 | N/A | 75 |
| 2025-07-11 14:25:53 | BUY | CSCO | 1 | $68.38 | N/A | 70 |
| 2025-07-11 14:25:53 | BUY | T | 6 | $26.95 | N/A | 65 |
| 2025-07-11 14:09:16 | SELL | INTC | 6 | $23.27 | $5.47 | 60 |
| 2025-07-11 14:09:16 | SELL | XOM | 1 | $114.67 | $4.54 | 75 |
| 2025-07-11 14:09:16 | SELL | WFC | 1 | $81.79 | $-0.49 | 70 |
| 2025-07-11 14:09:16 | SELL | T | 5 | $27.16 | $0.20 | 60 |
| 2025-07-11 14:09:16 | BUY | NKE | 1 | $73.15 | N/A | 75 |
| 2025-07-11 14:09:16 | BUY | PYPL | 1 | $74.76 | N/A | 70 |
| 2025-07-11 14:09:16 | BUY | ORCL | 1 | $232.34 | N/A | 75 |
| 2025-07-11 13:55:56 | SELL | PYPL | 2 | $74.62 | $-4.10 | 65 |
| 2025-07-11 13:55:56 | SELL | QCOM | 1 | $158.34 | $-3.56 | 65 |
| 2025-07-11 13:55:56 | SELL | CSCO | 1 | $68.18 | $-0.17 | 65 |
| 2025-07-11 13:55:56 | BUY | BAC | 2 | $46.38 | N/A | 70 |
| 2025-07-11 13:55:56 | BUY | XOM | 1 | $114.69 | N/A | 80 |
| 2025-07-11 13:55:56 | BUY | PFE | 5 | $25.57 | N/A | 70 |
| 2025-07-11 13:55:56 | BUY | PG | 1 | $157.15 | N/A | 70 |
| 2025-07-11 13:55:56 | BUY | T | 75 | $27.11 | N/A | 65 |
| 2025-07-11 13:55:42 | SELL | T | 70 | $27.11 | $-104.64 | 60 |
| 2025-07-11 13:45:51 | SELL | AAPL | 1 | $209.92 | $-1.24 | 65 |
| 2025-07-11 13:45:51 | SELL | BAC | 4 | $46.38 | $-8.89 | 65 |
| 2025-07-11 13:45:51 | SELL | AMD | 2 | $142.25 | $11.49 | 70 |

<!--TRADE_LOG_END--> 
