# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 14:41:42**

| Metric | Value |
|---|---|
| **Total Value** | **$101,442.51** |
| Cash | $1,559.13 |
| Holdings Value | $99,883.38 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $213.26 | $2,132.60 | 65 |
| ADBE | 5 | $377.60 | $371.14 | $1,855.70 | 65 |
| AMD | 15 | $135.39 | $145.32 | $2,179.80 | 65 |
| AMZN | 11 | $221.90 | $220.65 | $2,427.15 | 75 |
| AVGO | 8 | $275.34 | $273.55 | $2,188.40 | 70 |
| AXP | 7 | $325.28 | $322.94 | $2,260.55 | 75 |
| BA | 9 | $210.97 | $226.22 | $2,035.93 | 65 |
| BAC | 50 | $48.57 | $47.19 | $2,359.41 | 75 |
| C | 26 | $86.83 | $86.64 | $2,252.51 | 70 |
| CAT | 6 | $397.86 | $409.43 | $2,456.58 | 75 |
| COST | 2 | $979.83 | $979.11 | $1,958.22 | 65 |
| CRM | 8 | $268.33 | $265.96 | $2,127.68 | 65 |
| CSCO | 33 | $68.37 | $68.85 | $2,271.95 | 70 |
| CVX | 17 | $147.15 | $155.13 | $2,637.22 | 85 |
| DIS | 18 | $122.80 | $121.44 | $2,185.92 | 70 |
| GOOGL | 12 | $179.86 | $175.44 | $2,105.34 | 70 |
| GS | 3 | $717.52 | $701.60 | $2,104.80 | 65 |
| HD | 6 | $372.64 | $376.04 | $2,256.24 | 65 |
| INTC | 80 | $22.19 | $23.87 | $1,909.96 | 60 |
| JNJ | 13 | $155.89 | $158.62 | $2,062.06 | 65 |
| JPM | 9 | $291.61 | $286.26 | $2,576.34 | 85 |
| KO | 29 | $71.03 | $69.56 | $2,017.38 | 65 |
| LLY | 2 | $776.66 | $792.69 | $1,585.38 | 65 |
| MA | 4 | $563.08 | $562.05 | $2,248.20 | 60 |
| META | 3 | $717.12 | $723.00 | $2,169.01 | 75 |
| MRK | 28 | $82.46 | $84.83 | $2,375.35 | 75 |
| MSFT | 5 | $498.84 | $499.21 | $2,496.05 | 75 |
| NFLX | 1 | $1,279.00 | $1,250.83 | $1,250.83 | 65 |
| NKE | 29 | $75.85 | $74.87 | $2,171.23 | 70 |
| NVDA | 16 | $157.42 | $162.56 | $2,600.88 | 85 |
| ORCL | 9 | $233.31 | $234.52 | $2,110.68 | 65 |
| PEP | 15 | $136.57 | $136.15 | $2,042.25 | 65 |
| PFE | 90 | $25.25 | $26.00 | $2,340.45 | 75 |
| PG | 12 | $160.96 | $158.56 | $1,902.72 | 65 |
| PYPL | 31 | $76.64 | $75.47 | $2,339.57 | 75 |
| QCOM | 14 | $161.87 | $160.01 | $2,240.14 | 75 |
| T | 74 | $28.53 | $27.64 | $2,045.73 | 65 |
| TGT | 20 | $104.89 | $105.50 | $2,110.07 | 70 |
| TSLA | 6 | $288.62 | $304.85 | $1,829.10 | 60 |
| UNH | 6 | $298.34 | $303.00 | $1,818.00 | 65 |
| UNP | 10 | $236.59 | $240.38 | $2,403.75 | 75 |
| V | 6 | $355.85 | $354.37 | $2,126.19 | 65 |
| VZ | 48 | $43.15 | $42.16 | $2,023.59 | 65 |
| WFC | 32 | $82.29 | $82.22 | $2,631.20 | 85 |
| WMT | 21 | $97.35 | $95.86 | $2,013.16 | 65 |
| XOM | 23 | $110.31 | $115.14 | $2,648.11 | 85 |

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
| 2025-07-10 14:41:37 | SELL | INTC | 6 | $23.87 | $9.37 | 60 |
| 2025-07-10 14:41:37 | BUY | NKE | 1 | $74.86 | N/A | 70 |
| 2025-07-10 14:41:37 | BUY | PFE | 11 | $26.00 | N/A | 75 |
| 2025-07-10 14:41:37 | BUY | T | 1 | $27.65 | N/A | 65 |
| 2025-07-10 14:26:27 | SELL | AAPL | 1 | $211.51 | $0.43 | 65 |
| 2025-07-10 14:26:27 | SELL | NKE | 4 | $74.62 | $-4.42 | 65 |
| 2025-07-10 14:26:27 | SELL | PFE | 6 | $25.94 | $4.42 | 65 |
| 2025-07-10 14:26:27 | SELL | C | 1 | $86.44 | $-0.38 | 70 |
| 2025-07-10 14:26:27 | SELL | CSCO | 1 | $68.72 | $0.35 | 70 |
| 2025-07-10 14:26:27 | BUY | NVDA | 2 | $162.88 | N/A | 85 |
| 2025-07-10 14:26:27 | BUY | WFC | 3 | $82.17 | N/A | 85 |
| 2025-07-10 14:26:27 | BUY | QCOM | 1 | $159.40 | N/A | 75 |
| 2025-07-10 14:09:15 | SELL | NVDA | 2 | $162.34 | $9.98 | 70 |
| 2025-07-10 14:09:15 | SELL | PFE | 1 | $25.90 | $0.68 | 70 |
| 2025-07-10 14:09:15 | SELL | MRK | 1 | $84.14 | $1.63 | 75 |
| 2025-07-10 14:09:15 | SELL | PG | 1 | $158.32 | $-2.43 | 60 |
| 2025-07-10 14:09:15 | BUY | PYPL | 1 | $75.14 | N/A | 75 |
| 2025-07-10 14:09:15 | BUY | C | 1 | $86.58 | N/A | 75 |
| 2025-07-10 14:09:15 | BUY | CVX | 2 | $153.73 | N/A | 85 |
| 2025-07-10 13:47:19 | SELL | GOOGL | 1 | $175.33 | $-4.18 | 65 |
| 2025-07-10 13:47:19 | SELL | MRK | 2 | $83.42 | $1.68 | 75 |
| 2025-07-10 13:47:19 | SELL | PYPL | 1 | $74.64 | $-1.98 | 70 |
| 2025-07-10 13:47:19 | SELL | PFE | 5 | $25.68 | $2.24 | 70 |
| 2025-07-10 13:47:19 | BUY | NVDA | 2 | $163.90 | N/A | 85 |
| 2025-07-10 13:47:19 | BUY | UNH | 6 | $298.34 | N/A | 65 |

<!--TRADE_LOG_END--> 
