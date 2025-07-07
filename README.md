# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 19:50:21**

| Metric | Value |
|---|---|
| **Total Value** | **$100,652.37** |
| Cash | $206.64 |
| Holdings Value | $100,445.74 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.76 | $2,097.65 | 70 |
| ADBE | 5 | $377.60 | $376.46 | $1,882.32 | 65 |
| AMD | 15 | $135.73 | $134.75 | $2,021.25 | 65 |
| AMZN | 11 | $221.72 | $223.21 | $2,455.31 | 75 |
| AVGO | 8 | $275.34 | $274.35 | $2,194.80 | 70 |
| AXP | 7 | $324.46 | $321.69 | $2,251.83 | 70 |
| BA | 10 | $212.15 | $218.22 | $2,182.20 | 65 |
| BAC | 54 | $48.70 | $48.51 | $2,619.54 | 85 |
| C | 25 | $86.37 | $87.42 | $2,185.50 | 70 |
| CAT | 6 | $397.86 | $391.07 | $2,346.42 | 75 |
| COST | 2 | $979.83 | $989.43 | $1,978.86 | 65 |
| CRM | 8 | $268.33 | $268.94 | $2,151.56 | 65 |
| CSCO | 32 | $68.36 | $68.72 | $2,199.20 | 70 |
| CVX | 16 | $146.70 | $146.85 | $2,349.60 | 75 |
| DIS | 18 | $122.86 | $123.22 | $2,217.87 | 70 |
| GOOGL | 13 | $179.38 | $176.19 | $2,290.47 | 75 |
| GS | 3 | $717.52 | $709.61 | $2,128.83 | 70 |
| HD | 6 | $372.64 | $366.95 | $2,201.70 | 65 |
| INTC | 85 | $22.27 | $21.93 | $1,864.47 | 60 |
| JNJ | 13 | $155.80 | $155.21 | $2,017.73 | 65 |
| JPM | 9 | $292.50 | $291.38 | $2,622.42 | 85 |
| KO | 29 | $71.03 | $70.92 | $2,056.54 | 65 |
| LLY | 2 | $776.66 | $772.36 | $1,544.72 | 65 |
| MA | 4 | $563.08 | $563.84 | $2,255.36 | 65 |
| META | 3 | $717.12 | $718.85 | $2,156.55 | 85 |
| MRK | 28 | $82.42 | $80.96 | $2,266.88 | 75 |
| MSFT | 5 | $498.84 | $497.36 | $2,486.82 | 85 |
| NFLX | 1 | $1,279.00 | $1,289.45 | $1,289.45 | 65 |
| NKE | 34 | $75.95 | $76.61 | $2,604.57 | 85 |
| NVDA | 14 | $156.23 | $158.31 | $2,216.34 | 70 |
| ORCL | 10 | $233.29 | $233.13 | $2,331.30 | 75 |
| PEP | 15 | $136.57 | $134.35 | $2,015.25 | 65 |
| PFE | 85 | $25.29 | $25.21 | $2,142.85 | 70 |
| PG | 13 | $160.77 | $160.28 | $2,083.64 | 65 |
| PYPL | 31 | $76.77 | $76.10 | $2,359.10 | 75 |
| QCOM | 15 | $161.50 | $157.89 | $2,368.35 | 75 |
| T | 71 | $28.54 | $28.36 | $2,013.91 | 65 |
| TGT | 20 | $104.90 | $101.49 | $2,029.80 | 65 |
| TSLA | 7 | $289.38 | $295.09 | $2,065.63 | 65 |
| UNH | 7 | $314.75 | $302.75 | $2,119.25 | 65 |
| UNP | 11 | $236.43 | $235.25 | $2,587.70 | 85 |
| V | 6 | $355.95 | $356.68 | $2,140.05 | 70 |
| VZ | 47 | $43.72 | $42.81 | $2,012.30 | 65 |
| WFC | 31 | $82.35 | $82.08 | $2,544.48 | 85 |
| WMT | 23 | $97.38 | $99.08 | $2,278.95 | 75 |
| XOM | 20 | $109.91 | $110.82 | $2,216.40 | 75 |

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
| 2025-07-07 19:50:12 | SELL | NVDA | 2 | $158.18 | $3.42 | 70 |
| 2025-07-07 19:50:12 | SELL | CVX | 1 | $146.84 | $0.13 | 75 |
| 2025-07-07 19:50:12 | SELL | T | 1 | $28.36 | $-0.18 | 65 |
| 2025-07-07 19:50:12 | BUY | WMT | 2 | $99.08 | N/A | 75 |
| 2025-07-07 19:50:12 | BUY | NKE | 4 | $76.60 | N/A | 85 |
| 2025-07-07 19:50:12 | BUY | PFE | 4 | $25.22 | N/A | 70 |
| 2025-07-07 19:50:12 | BUY | WFC | 2 | $83.60 | N/A | 85 |
| 2025-07-07 19:50:12 | BUY | UNP | 1 | $235.25 | N/A | 85 |
| 2025-07-07 19:36:19 | SELL | PFE | 5 | $25.21 | $-0.42 | 65 |
| 2025-07-07 19:36:19 | SELL | T | 4 | $28.39 | $-0.59 | 65 |
| 2025-07-07 19:36:19 | BUY | NVDA | 2 | $158.40 | N/A | 85 |
| 2025-07-07 19:36:19 | BUY | NKE | 1 | $76.54 | N/A | 75 |
| 2025-07-07 19:36:19 | BUY | CVX | 1 | $146.75 | N/A | 85 |
| 2025-07-07 19:25:04 | SELL | AAPL | 1 | $209.43 | $-1.49 | 65 |
| 2025-07-07 19:25:04 | SELL | NKE | 1 | $76.50 | $0.64 | 70 |
| 2025-07-07 19:25:04 | SELL | C | 5 | $87.36 | $4.12 | 70 |
| 2025-07-07 19:25:04 | SELL | UNP | 1 | $234.88 | $-1.52 | 75 |
| 2025-07-07 19:25:04 | SELL | CSCO | 1 | $68.71 | $0.34 | 70 |
| 2025-07-07 19:25:04 | SELL | CVX | 1 | $146.66 | $-0.04 | 75 |
| 2025-07-07 19:25:04 | BUY | INTC | 1 | $21.92 | N/A | 60 |
| 2025-07-07 19:25:04 | BUY | MRK | 3 | $81.01 | N/A | 75 |
| 2025-07-07 19:25:04 | BUY | PFE | 2 | $25.23 | N/A | 70 |
| 2025-07-07 19:25:04 | BUY | ORCL | 1 | $233.21 | N/A | 75 |
| 2025-07-07 19:25:04 | BUY | T | 5 | $28.38 | N/A | 70 |
| 2025-07-07 19:07:47 | SELL | NVDA | 2 | $158.38 | $3.82 | 70 |

<!--TRADE_LOG_END--> 
