# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 14:41:00**

| Metric | Value |
|---|---|
| **Total Value** | **$100,751.82** |
| Cash | $966.35 |
| Holdings Value | $99,785.47 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.32 | $2,113.20 | 70 |
| ADBE | 5 | $377.60 | $368.73 | $1,843.62 | 65 |
| AMD | 16 | $135.79 | $144.54 | $2,312.64 | 70 |
| AMZN | 11 | $221.97 | $224.33 | $2,467.63 | 75 |
| AVGO | 8 | $275.34 | $273.25 | $2,186.00 | 70 |
| AXP | 7 | $325.34 | $323.60 | $2,265.20 | 75 |
| BA | 9 | $210.85 | $228.20 | $2,053.83 | 70 |
| BAC | 45 | $48.80 | $46.48 | $2,091.60 | 65 |
| C | 23 | $86.72 | $86.17 | $1,982.02 | 60 |
| CAT | 6 | $397.86 | $404.48 | $2,426.88 | 70 |
| COST | 2 | $979.83 | $970.47 | $1,940.94 | 65 |
| CRM | 7 | $268.68 | $260.41 | $1,822.87 | 65 |
| CSCO | 34 | $68.35 | $68.31 | $2,322.54 | 75 |
| CVX | 16 | $146.69 | $154.52 | $2,472.32 | 75 |
| DIS | 18 | $122.81 | $120.63 | $2,171.34 | 65 |
| GOOGL | 13 | $179.61 | $177.82 | $2,311.67 | 75 |
| GS | 3 | $717.52 | $704.54 | $2,113.62 | 65 |
| HD | 6 | $372.64 | $367.43 | $2,204.58 | 75 |
| INTC | 88 | $22.37 | $23.36 | $2,055.68 | 65 |
| JNJ | 13 | $155.89 | $155.65 | $2,023.45 | 65 |
| JPM | 9 | $291.61 | $286.02 | $2,574.18 | 75 |
| KO | 29 | $71.03 | $69.95 | $2,028.55 | 65 |
| LLY | 3 | $781.32 | $779.95 | $2,339.85 | 70 |
| MA | 4 | $563.08 | $554.88 | $2,219.53 | 65 |
| META | 3 | $717.12 | $715.25 | $2,145.75 | 75 |
| MRK | 25 | $82.30 | $82.46 | $2,061.50 | 65 |
| MSFT | 5 | $498.84 | $501.79 | $2,508.95 | 70 |
| NFLX | 1 | $1,279.00 | $1,248.27 | $1,248.27 | 65 |
| NKE | 32 | $75.67 | $73.05 | $2,337.60 | 75 |
| NVDA | 16 | $157.38 | $167.34 | $2,677.44 | 85 |
| ORCL | 9 | $233.26 | $232.89 | $2,096.01 | 65 |
| PEP | 15 | $136.57 | $134.83 | $2,022.45 | 65 |
| PFE | 87 | $25.20 | $25.47 | $2,216.18 | 70 |
| PG | 14 | $160.52 | $157.20 | $2,200.80 | 65 |
| PYPL | 29 | $76.75 | $74.77 | $2,168.42 | 70 |
| QCOM | 13 | $162.18 | $158.06 | $2,054.78 | 65 |
| T | 76 | $27.10 | $26.98 | $2,050.86 | 65 |
| TGT | 20 | $104.92 | $104.17 | $2,083.30 | 65 |
| TSLA | 6 | $288.62 | $309.78 | $1,858.68 | 65 |
| UNH | 7 | $298.51 | $299.43 | $2,096.01 | 65 |
| UNP | 10 | $236.18 | $235.46 | $2,354.56 | 75 |
| V | 6 | $355.85 | $350.00 | $2,099.97 | 65 |
| VZ | 49 | $43.11 | $41.62 | $2,039.13 | 65 |
| WFC | 29 | $82.28 | $82.14 | $2,382.06 | 75 |
| WMT | 22 | $97.25 | $95.14 | $2,093.08 | 65 |
| XOM | 23 | $110.36 | $115.04 | $2,645.92 | 85 |

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
| 2025-07-11 14:40:54 | SELL | C | 2 | $86.14 | $-1.05 | 60 |
| 2025-07-11 14:40:54 | SELL | ORCL | 1 | $232.82 | $-0.39 | 65 |
| 2025-07-11 14:40:54 | SELL | CVX | 1 | $154.49 | $7.34 | 75 |
| 2025-07-11 14:40:54 | BUY | INTC | 6 | $23.38 | N/A | 65 |
| 2025-07-11 14:40:54 | BUY | XOM | 2 | $115.05 | N/A | 85 |
| 2025-07-11 14:40:54 | BUY | PFE | 1 | $25.48 | N/A | 70 |
| 2025-07-11 14:40:54 | BUY | CSCO | 2 | $68.32 | N/A | 75 |
| 2025-07-11 14:40:54 | BUY | VZ | 3 | $41.60 | N/A | 65 |
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

<!--TRADE_LOG_END--> 
