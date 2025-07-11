# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 15:08:32**

| Metric | Value |
|---|---|
| **Total Value** | **$100,665.82** |
| Cash | $1,125.63 |
| Holdings Value | $99,540.19 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.94 | $2,109.35 | 70 |
| ADBE | 5 | $377.60 | $367.05 | $1,835.25 | 65 |
| AMD | 18 | $136.72 | $144.47 | $2,600.46 | 85 |
| AMZN | 11 | $221.97 | $224.56 | $2,470.16 | 75 |
| AVGO | 8 | $275.34 | $273.90 | $2,191.22 | 70 |
| AXP | 7 | $325.34 | $322.73 | $2,259.11 | 70 |
| BA | 9 | $210.85 | $227.95 | $2,051.54 | 65 |
| BAC | 44 | $48.85 | $46.46 | $2,044.24 | 65 |
| C | 24 | $86.69 | $86.28 | $2,070.84 | 65 |
| CAT | 6 | $397.86 | $405.32 | $2,431.92 | 65 |
| COST | 2 | $979.83 | $969.83 | $1,939.66 | 65 |
| CRM | 7 | $268.68 | $259.31 | $1,815.17 | 65 |
| CSCO | 32 | $68.37 | $68.22 | $2,183.20 | 70 |
| CVX | 17 | $147.16 | $155.10 | $2,636.78 | 85 |
| DIS | 17 | $122.96 | $120.30 | $2,045.02 | 65 |
| GOOGL | 13 | $179.61 | $178.28 | $2,317.70 | 75 |
| GS | 3 | $717.52 | $704.32 | $2,112.96 | 75 |
| HD | 6 | $372.64 | $367.38 | $2,204.30 | 70 |
| INTC | 87 | $22.35 | $23.33 | $2,029.72 | 65 |
| JNJ | 13 | $155.89 | $155.23 | $2,018.05 | 65 |
| JPM | 9 | $291.61 | $286.42 | $2,577.78 | 75 |
| KO | 29 | $71.03 | $69.90 | $2,027.10 | 65 |
| LLY | 3 | $781.32 | $780.71 | $2,342.13 | 70 |
| MA | 4 | $563.08 | $554.01 | $2,216.02 | 65 |
| META | 3 | $717.12 | $716.71 | $2,150.12 | 85 |
| MRK | 26 | $82.30 | $82.32 | $2,140.32 | 70 |
| MSFT | 5 | $498.84 | $502.67 | $2,513.35 | 75 |
| NFLX | 1 | $1,279.00 | $1,240.50 | $1,240.50 | 65 |
| NKE | 29 | $75.98 | $72.56 | $2,104.24 | 65 |
| NVDA | 16 | $157.38 | $166.69 | $2,667.12 | 85 |
| ORCL | 9 | $233.26 | $233.11 | $2,097.96 | 65 |
| PEP | 15 | $136.57 | $134.51 | $2,017.65 | 65 |
| PFE | 81 | $25.18 | $25.45 | $2,061.86 | 65 |
| PG | 14 | $160.52 | $157.01 | $2,198.14 | 65 |
| PYPL | 28 | $76.84 | $74.53 | $2,086.84 | 65 |
| QCOM | 13 | $162.18 | $157.57 | $2,048.41 | 65 |
| T | 76 | $27.10 | $26.88 | $2,043.02 | 65 |
| TGT | 20 | $104.92 | $103.92 | $2,078.50 | 65 |
| TSLA | 6 | $288.62 | $308.22 | $1,849.32 | 65 |
| UNH | 7 | $298.51 | $299.75 | $2,098.22 | 65 |
| UNP | 10 | $236.18 | $234.60 | $2,346.00 | 75 |
| V | 6 | $355.85 | $349.45 | $2,096.70 | 70 |
| VZ | 49 | $43.12 | $41.65 | $2,040.85 | 65 |
| WFC | 29 | $82.28 | $82.34 | $2,388.01 | 75 |
| WMT | 22 | $97.25 | $94.99 | $2,089.78 | 65 |
| XOM | 23 | $110.39 | $115.38 | $2,653.62 | 85 |

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
| 2025-07-11 15:08:26 | SELL | BAC | 3 | $46.47 | $-6.67 | 65 |
| 2025-07-11 15:08:26 | SELL | DIS | 1 | $120.31 | $-2.50 | 65 |
| 2025-07-11 15:08:26 | SELL | PFE | 6 | $25.45 | $1.54 | 65 |
| 2025-07-11 15:08:26 | SELL | PYPL | 3 | $74.53 | $-6.25 | 65 |
| 2025-07-11 15:08:26 | SELL | NKE | 2 | $72.54 | $-6.44 | 65 |
| 2025-07-11 15:08:26 | SELL | C | 1 | $86.31 | $-0.37 | 65 |
| 2025-07-11 15:08:26 | BUY | AMD | 2 | $144.16 | N/A | 85 |
| 2025-07-11 15:08:26 | BUY | INTC | 5 | $23.33 | N/A | 65 |
| 2025-07-11 15:08:26 | BUY | XOM | 2 | $115.38 | N/A | 85 |
| 2025-07-11 15:08:26 | BUY | MRK | 1 | $82.32 | N/A | 70 |
| 2025-07-11 15:08:26 | BUY | CSCO | 1 | $68.23 | N/A | 70 |
| 2025-07-11 15:08:26 | BUY | VZ | 3 | $41.64 | N/A | 65 |
| 2025-07-11 14:52:03 | SELL | INTC | 6 | $23.35 | $5.94 | 60 |
| 2025-07-11 14:52:03 | SELL | XOM | 2 | $115.08 | $9.45 | 75 |
| 2025-07-11 14:52:03 | SELL | NKE | 1 | $72.81 | $-2.86 | 70 |
| 2025-07-11 14:52:03 | SELL | CSCO | 3 | $68.11 | $-0.75 | 65 |
| 2025-07-11 14:52:03 | SELL | VZ | 3 | $41.62 | $-4.48 | 60 |
| 2025-07-11 14:52:03 | BUY | BAC | 2 | $46.43 | N/A | 70 |
| 2025-07-11 14:52:03 | BUY | PYPL | 2 | $74.69 | N/A | 75 |
| 2025-07-11 14:52:03 | BUY | C | 2 | $86.21 | N/A | 70 |
| 2025-07-11 14:52:03 | BUY | CVX | 1 | $154.60 | N/A | 85 |
| 2025-07-11 14:40:54 | SELL | C | 2 | $86.14 | $-1.05 | 60 |
| 2025-07-11 14:40:54 | SELL | ORCL | 1 | $232.82 | $-0.39 | 65 |
| 2025-07-11 14:40:54 | SELL | CVX | 1 | $154.49 | $7.34 | 75 |
| 2025-07-11 14:40:54 | BUY | INTC | 6 | $23.38 | N/A | 65 |

<!--TRADE_LOG_END--> 
