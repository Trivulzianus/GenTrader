# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 15:51:06**

| Metric | Value |
|---|---|
| **Total Value** | **$100,757.07** |
| Cash | $795.62 |
| Holdings Value | $99,961.45 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $211.81 | $2,118.10 | 70 |
| ADBE | 5 | $377.60 | $378.30 | $1,891.50 | 65 |
| AMD | 15 | $135.76 | $134.70 | $2,020.50 | 65 |
| AMZN | 11 | $221.66 | $223.73 | $2,461.03 | 75 |
| AVGO | 8 | $269.90 | $276.73 | $2,213.84 | 70 |
| AXP | 7 | $324.46 | $323.44 | $2,264.11 | 70 |
| BA | 10 | $212.15 | $215.00 | $2,150.05 | 70 |
| BAC | 54 | $48.71 | $48.78 | $2,634.12 | 85 |
| C | 30 | $86.68 | $87.82 | $2,634.60 | 85 |
| CAT | 6 | $397.86 | $391.89 | $2,351.37 | 85 |
| COST | 2 | $979.83 | $984.50 | $1,968.99 | 65 |
| CRM | 8 | $268.33 | $270.75 | $2,166.00 | 65 |
| CSCO | 32 | $68.34 | $68.93 | $2,205.76 | 70 |
| CVX | 17 | $146.68 | $146.39 | $2,488.63 | 85 |
| DIS | 17 | $122.86 | $123.34 | $2,096.78 | 70 |
| GOOGL | 12 | $179.64 | $177.08 | $2,124.96 | 65 |
| GS | 3 | $717.52 | $715.29 | $2,145.87 | 75 |
| HD | 6 | $372.64 | $367.10 | $2,202.60 | 65 |
| INTC | 84 | $22.27 | $22.04 | $1,851.36 | 60 |
| JNJ | 13 | $155.80 | $155.44 | $2,020.78 | 65 |
| JPM | 9 | $292.50 | $292.06 | $2,628.54 | 85 |
| KO | 28 | $71.03 | $70.96 | $1,986.88 | 65 |
| LLY | 2 | $776.66 | $770.76 | $1,541.53 | 65 |
| MA | 4 | $563.08 | $563.75 | $2,255.02 | 65 |
| META | 3 | $717.12 | $723.04 | $2,169.12 | 70 |
| MRK | 29 | $82.38 | $81.19 | $2,354.51 | 75 |
| MSFT | 5 | $498.84 | $497.71 | $2,488.56 | 85 |
| NFLX | 1 | $1,279.00 | $1,287.03 | $1,287.03 | 70 |
| NKE | 31 | $75.89 | $76.08 | $2,358.63 | 75 |
| NVDA | 16 | $156.42 | $158.01 | $2,528.16 | 85 |
| ORCL | 10 | $226.85 | $233.85 | $2,338.50 | 75 |
| PEP | 15 | $136.59 | $134.44 | $2,016.67 | 65 |
| PFE | 80 | $25.31 | $25.25 | $2,019.60 | 65 |
| PG | 13 | $160.77 | $159.77 | $2,077.01 | 65 |
| PYPL | 30 | $76.81 | $76.19 | $2,285.85 | 75 |
| QCOM | 14 | $161.69 | $158.71 | $2,221.94 | 75 |
| T | 71 | $28.54 | $28.29 | $2,008.59 | 65 |
| TGT | 20 | $104.92 | $101.00 | $2,020.00 | 65 |
| TSLA | 6 | $288.90 | $293.30 | $1,759.80 | 60 |
| UNH | 7 | $314.75 | $303.46 | $2,124.22 | 65 |
| UNP | 10 | $236.52 | $235.79 | $2,357.90 | 75 |
| V | 6 | $355.95 | $355.94 | $2,135.64 | 70 |
| VZ | 47 | $43.72 | $42.84 | $2,013.25 | 65 |
| WFC | 29 | $82.25 | $82.17 | $2,383.07 | 75 |
| WMT | 23 | $97.35 | $98.05 | $2,255.15 | 75 |
| XOM | 21 | $109.98 | $111.20 | $2,335.30 | 75 |

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
| 2025-07-07 15:51:00 | SELL | GOOGL | 1 | $177.02 | $-2.42 | 65 |
| 2025-07-07 15:51:00 | SELL | AMD | 1 | $134.68 | $-1.01 | 65 |
| 2025-07-07 15:51:00 | SELL | INTC | 9 | $22.05 | $-1.85 | 60 |
| 2025-07-07 15:51:00 | SELL | XOM | 1 | $111.22 | $1.18 | 75 |
| 2025-07-07 15:51:00 | SELL | PFE | 7 | $25.25 | $-0.40 | 65 |
| 2025-07-07 15:51:00 | SELL | AXP | 1 | $323.56 | $-0.78 | 70 |
| 2025-07-07 15:51:00 | SELL | UNP | 1 | $235.89 | $-0.57 | 75 |
| 2025-07-07 15:51:00 | SELL | T | 6 | $28.30 | $-1.38 | 65 |
| 2025-07-07 15:51:00 | BUY | V | 6 | $355.95 | N/A | 70 |
| 2025-07-07 15:51:00 | BUY | NVDA | 2 | $157.97 | N/A | 85 |
| 2025-07-07 15:51:00 | BUY | PYPL | 1 | $76.19 | N/A | 75 |
| 2025-07-07 15:51:00 | BUY | WMT | 2 | $98.05 | N/A | 75 |
| 2025-07-07 15:51:00 | BUY | CVX | 1 | $146.38 | N/A | 85 |
| 2025-07-07 15:39:15 | SELL | V | 6 | $356.17 | $19.60 | 65 |
| 2025-07-07 15:39:15 | SELL | DIS | 1 | $123.32 | $0.44 | 65 |
| 2025-07-07 15:39:15 | SELL | WMT | 2 | $98.19 | $1.67 | 65 |
| 2025-07-07 15:39:15 | SELL | PYPL | 1 | $76.31 | $-0.50 | 70 |
| 2025-07-07 15:39:15 | BUY | GOOGL | 1 | $177.71 | N/A | 75 |
| 2025-07-07 15:39:15 | BUY | AMD | 1 | $134.20 | N/A | 70 |
| 2025-07-07 15:39:15 | BUY | INTC | 8 | $22.01 | N/A | 65 |
| 2025-07-07 15:39:15 | BUY | NKE | 3 | $76.06 | N/A | 75 |
| 2025-07-07 15:39:15 | BUY | XOM | 2 | $111.28 | N/A | 80 |
| 2025-07-07 15:39:15 | BUY | PFE | 7 | $25.31 | N/A | 70 |
| 2025-07-07 15:39:15 | BUY | MRK | 4 | $81.38 | N/A | 75 |
| 2025-07-07 15:39:15 | BUY | C | 1 | $87.90 | N/A | 85 |

<!--TRADE_LOG_END--> 
