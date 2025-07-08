# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 14:52:34**

| Metric | Value |
|---|---|
| **Total Value** | **$100,759.92** |
| Cash | $1,181.47 |
| Holdings Value | $99,578.45 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.46 | $2,104.64 | 65 |
| ADBE | 5 | $377.60 | $384.78 | $1,923.90 | 65 |
| AMD | 16 | $135.69 | $138.01 | $2,208.16 | 70 |
| AMZN | 10 | $221.61 | $220.04 | $2,200.40 | 65 |
| AVGO | 8 | $275.34 | $273.12 | $2,185.00 | 65 |
| AXP | 8 | $324.24 | $320.44 | $2,563.52 | 85 |
| BA | 11 | $212.44 | $215.28 | $2,368.04 | 75 |
| BAC | 50 | $48.63 | $47.11 | $2,355.51 | 75 |
| C | 27 | $86.65 | $85.65 | $2,312.55 | 75 |
| CAT | 6 | $397.86 | $393.68 | $2,362.05 | 70 |
| COST | 2 | $979.83 | $986.20 | $1,972.40 | 65 |
| CRM | 8 | $268.33 | $275.92 | $2,207.36 | 65 |
| CSCO | 32 | $68.37 | $68.41 | $2,189.12 | 70 |
| CVX | 16 | $146.65 | $151.74 | $2,427.76 | 75 |
| DIS | 18 | $122.81 | $122.30 | $2,201.40 | 70 |
| GOOGL | 12 | $179.60 | $174.93 | $2,099.16 | 65 |
| GS | 3 | $717.52 | $695.73 | $2,087.19 | 70 |
| HD | 6 | $372.64 | $368.04 | $2,208.21 | 65 |
| INTC | 88 | $22.28 | $23.31 | $2,051.28 | 65 |
| JNJ | 13 | $155.81 | $156.45 | $2,033.85 | 65 |
| JPM | 9 | $291.61 | $282.32 | $2,540.88 | 75 |
| KO | 29 | $71.03 | $69.90 | $2,027.10 | 65 |
| LLY | 2 | $776.66 | $792.31 | $1,584.62 | 65 |
| MA | 4 | $563.08 | $564.65 | $2,258.60 | 65 |
| META | 3 | $717.12 | $717.12 | $2,151.36 | 65 |
| MRK | 29 | $82.43 | $82.14 | $2,381.91 | 75 |
| MSFT | 5 | $498.84 | $495.16 | $2,475.82 | 85 |
| NFLX | 1 | $1,279.00 | $1,267.05 | $1,267.05 | 65 |
| NKE | 29 | $75.98 | $74.14 | $2,150.06 | 70 |
| NVDA | 14 | $156.29 | $158.87 | $2,224.11 | 70 |
| ORCL | 9 | $233.41 | $237.22 | $2,134.98 | 65 |
| PEP | 15 | $136.57 | $135.09 | $2,026.42 | 65 |
| PFE | 86 | $25.29 | $25.80 | $2,218.37 | 70 |
| PG | 13 | $160.77 | $158.30 | $2,057.90 | 65 |
| PYPL | 31 | $76.64 | $75.26 | $2,333.06 | 75 |
| QCOM | 14 | $161.75 | $159.97 | $2,239.65 | 70 |
| T | 73 | $28.54 | $28.15 | $2,054.95 | 65 |
| TGT | 20 | $104.90 | $101.12 | $2,022.40 | 65 |
| TSLA | 6 | $288.62 | $301.59 | $1,809.54 | 65 |
| UNH | 7 | $314.75 | $306.62 | $2,146.36 | 65 |
| UNP | 10 | $236.53 | $237.47 | $2,374.65 | 75 |
| V | 6 | $355.95 | $356.38 | $2,138.28 | 70 |
| VZ | 47 | $43.72 | $43.05 | $2,023.35 | 65 |
| WFC | 29 | $82.34 | $81.28 | $2,357.12 | 75 |
| WMT | 22 | $97.41 | $96.64 | $2,126.08 | 65 |
| XOM | 21 | $109.93 | $113.92 | $2,392.32 | 75 |

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
| 2025-07-08 14:52:28 | SELL | NVDA | 2 | $158.90 | $4.55 | 70 |
| 2025-07-08 14:52:28 | SELL | XOM | 1 | $113.88 | $3.77 | 75 |
| 2025-07-08 14:52:28 | SELL | WMT | 1 | $96.75 | $-0.63 | 65 |
| 2025-07-08 14:52:28 | SELL | PFE | 4 | $25.80 | $1.96 | 70 |
| 2025-07-08 14:52:28 | BUY | BAC | 3 | $47.14 | N/A | 75 |
| 2025-07-08 14:52:28 | BUY | INTC | 1 | $23.32 | N/A | 65 |
| 2025-07-08 14:52:28 | BUY | NKE | 1 | $74.18 | N/A | 70 |
| 2025-07-08 14:52:28 | BUY | BA | 1 | $215.26 | N/A | 75 |
| 2025-07-08 14:52:28 | BUY | T | 1 | $28.15 | N/A | 65 |
| 2025-07-08 14:40:40 | SELL | JNJ | 1 | $156.44 | $0.58 | 65 |
| 2025-07-08 14:40:40 | SELL | INTC | 2 | $23.32 | $2.06 | 65 |
| 2025-07-08 14:40:40 | SELL | WFC | 3 | $81.74 | $-1.65 | 75 |
| 2025-07-08 14:40:40 | SELL | T | 1 | $28.41 | $-0.13 | 65 |
| 2025-07-08 14:40:40 | SELL | CSCO | 1 | $68.69 | $0.31 | 70 |
| 2025-07-08 14:40:40 | BUY | NVDA | 1 | $159.12 | N/A | 85 |
| 2025-07-08 14:40:40 | BUY | PFE | 4 | $25.77 | N/A | 75 |
| 2025-07-08 14:40:40 | BUY | C | 1 | $86.14 | N/A | 75 |
| 2025-07-08 14:26:03 | SELL | BAC | 2 | $47.44 | $-2.47 | 70 |
| 2025-07-08 14:26:03 | SELL | NVDA | 1 | $158.69 | $2.10 | 75 |
| 2025-07-08 14:26:03 | SELL | PFE | 1 | $25.74 | $0.44 | 70 |
| 2025-07-08 14:26:03 | SELL | C | 4 | $86.01 | $-2.27 | 70 |
| 2025-07-08 14:26:03 | SELL | CVX | 1 | $150.30 | $3.44 | 75 |
| 2025-07-08 14:26:03 | BUY | JNJ | 1 | $156.58 | N/A | 70 |
| 2025-07-08 14:26:03 | BUY | JPM | 1 | $284.00 | N/A | 85 |
| 2025-07-08 14:26:03 | BUY | AMD | 1 | $136.73 | N/A | 70 |

<!--TRADE_LOG_END--> 
