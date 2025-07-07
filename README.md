# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 16:43:20**

| Metric | Value |
|---|---|
| **Total Value** | **$100,684.53** |
| Cash | $1,013.30 |
| Holdings Value | $99,671.23 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.30 | $210.50 | $2,315.50 | 75 |
| ADBE | 5 | $377.60 | $378.52 | $1,892.60 | 65 |
| AMD | 15 | $135.76 | $135.34 | $2,030.10 | 70 |
| AMZN | 11 | $221.66 | $223.29 | $2,456.24 | 75 |
| AVGO | 8 | $269.90 | $276.00 | $2,208.00 | 70 |
| AXP | 7 | $324.46 | $322.99 | $2,260.89 | 75 |
| BA | 10 | $212.15 | $215.07 | $2,150.70 | 70 |
| BAC | 54 | $48.71 | $48.66 | $2,627.74 | 85 |
| C | 25 | $86.45 | $87.69 | $2,192.12 | 70 |
| CAT | 6 | $397.86 | $390.49 | $2,342.94 | 75 |
| COST | 2 | $979.83 | $987.62 | $1,975.23 | 65 |
| CRM | 8 | $268.33 | $270.09 | $2,160.72 | 65 |
| CSCO | 33 | $68.37 | $68.91 | $2,273.87 | 75 |
| CVX | 17 | $146.67 | $146.23 | $2,485.91 | 85 |
| DIS | 17 | $122.86 | $123.04 | $2,091.69 | 65 |
| GOOGL | 12 | $179.64 | $176.98 | $2,123.76 | 75 |
| GS | 3 | $717.52 | $712.37 | $2,137.11 | 75 |
| HD | 6 | $372.64 | $366.49 | $2,198.94 | 70 |
| INTC | 84 | $22.27 | $22.09 | $1,855.14 | 60 |
| JNJ | 13 | $155.80 | $155.25 | $2,018.18 | 65 |
| JPM | 9 | $292.50 | $291.47 | $2,623.23 | 85 |
| KO | 28 | $71.03 | $70.89 | $1,984.78 | 65 |
| LLY | 2 | $776.66 | $771.19 | $1,542.37 | 65 |
| MA | 4 | $563.08 | $563.54 | $2,254.16 | 65 |
| META | 3 | $717.12 | $722.22 | $2,166.66 | 70 |
| MRK | 29 | $82.38 | $81.11 | $2,352.34 | 75 |
| MSFT | 5 | $498.84 | $497.58 | $2,487.90 | 85 |
| NFLX | 1 | $1,279.00 | $1,287.42 | $1,287.42 | 65 |
| NKE | 29 | $75.85 | $76.28 | $2,212.12 | 70 |
| NVDA | 16 | $156.42 | $158.37 | $2,533.84 | 85 |
| ORCL | 9 | $226.15 | $233.12 | $2,098.08 | 70 |
| PEP | 15 | $136.59 | $134.31 | $2,014.58 | 65 |
| PFE | 85 | $25.31 | $25.23 | $2,144.12 | 70 |
| PG | 13 | $160.77 | $159.44 | $2,072.72 | 70 |
| PYPL | 30 | $76.81 | $76.16 | $2,284.80 | 75 |
| QCOM | 15 | $161.55 | $158.89 | $2,383.35 | 75 |
| T | 71 | $28.55 | $28.29 | $2,008.23 | 65 |
| TGT | 20 | $104.92 | $101.29 | $2,025.80 | 65 |
| TSLA | 6 | $288.90 | $292.53 | $1,755.18 | 65 |
| UNH | 7 | $314.75 | $303.91 | $2,127.38 | 65 |
| UNP | 11 | $236.41 | $235.33 | $2,588.63 | 85 |
| V | 6 | $355.95 | $355.86 | $2,135.16 | 70 |
| VZ | 47 | $43.72 | $42.73 | $2,008.08 | 65 |
| WFC | 28 | $82.27 | $82.04 | $2,297.12 | 75 |
| WMT | 23 | $97.35 | $98.33 | $2,261.59 | 75 |
| XOM | 20 | $109.91 | $111.21 | $2,224.20 | 75 |

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
| 2025-07-07 16:43:14 | SELL | NKE | 1 | $76.29 | $0.43 | 70 |
| 2025-07-07 16:43:14 | SELL | WFC | 3 | $82.06 | $-0.57 | 75 |
| 2025-07-07 16:43:14 | SELL | T | 1 | $28.29 | $-0.25 | 65 |
| 2025-07-07 16:43:14 | BUY | UNP | 1 | $235.30 | N/A | 85 |
| 2025-07-07 16:43:14 | BUY | CVX | 1 | $146.25 | N/A | 85 |
| 2025-07-07 16:27:04 | SELL | C | 5 | $87.86 | $5.92 | 70 |
| 2025-07-07 16:27:04 | SELL | ORCL | 1 | $233.19 | $6.34 | 65 |
| 2025-07-07 16:27:04 | SELL | T | 4 | $28.24 | $-1.16 | 65 |
| 2025-07-07 16:27:04 | BUY | AAPL | 1 | $210.76 | N/A | 75 |
| 2025-07-07 16:27:04 | BUY | NKE | 1 | $76.30 | N/A | 75 |
| 2025-07-07 16:27:04 | BUY | WFC | 1 | $82.15 | N/A | 85 |
| 2025-07-07 16:09:30 | SELL | XOM | 1 | $111.44 | $1.46 | 70 |
| 2025-07-07 16:09:30 | SELL | NKE | 2 | $76.50 | $1.23 | 70 |
| 2025-07-07 16:09:30 | SELL | CVX | 1 | $146.43 | $-0.25 | 75 |
| 2025-07-07 16:09:30 | BUY | PFE | 5 | $25.25 | N/A | 70 |
| 2025-07-07 16:09:30 | BUY | WFC | 1 | $82.34 | N/A | 80 |
| 2025-07-07 16:09:30 | BUY | CSCO | 1 | $69.08 | N/A | 75 |
| 2025-07-07 16:09:30 | BUY | QCOM | 1 | $159.59 | N/A | 80 |
| 2025-07-07 16:09:30 | BUY | T | 5 | $28.27 | N/A | 70 |
| 2025-07-07 15:51:00 | SELL | GOOGL | 1 | $177.02 | $-2.42 | 65 |
| 2025-07-07 15:51:00 | SELL | AMD | 1 | $134.68 | $-1.01 | 65 |
| 2025-07-07 15:51:00 | SELL | INTC | 9 | $22.05 | $-1.85 | 60 |
| 2025-07-07 15:51:00 | SELL | XOM | 1 | $111.22 | $1.18 | 75 |
| 2025-07-07 15:51:00 | SELL | PFE | 7 | $25.25 | $-0.40 | 65 |
| 2025-07-07 15:51:00 | SELL | AXP | 1 | $323.56 | $-0.78 | 70 |

<!--TRADE_LOG_END--> 
