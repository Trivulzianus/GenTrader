# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 16:27:14**

| Metric | Value |
|---|---|
| **Total Value** | **$100,692.07** |
| Cash | $1,044.09 |
| Holdings Value | $99,647.98 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.30 | $210.87 | $2,319.59 | 75 |
| ADBE | 5 | $377.60 | $378.00 | $1,890.00 | 65 |
| AMD | 15 | $135.76 | $135.36 | $2,030.40 | 65 |
| AMZN | 11 | $221.66 | $222.97 | $2,452.67 | 75 |
| AVGO | 8 | $269.90 | $276.12 | $2,208.93 | 70 |
| AXP | 7 | $324.46 | $323.24 | $2,262.68 | 80 |
| BA | 10 | $212.15 | $215.26 | $2,152.60 | 70 |
| BAC | 54 | $48.71 | $48.75 | $2,632.50 | 85 |
| C | 25 | $86.45 | $87.88 | $2,197.00 | 70 |
| CAT | 6 | $397.86 | $391.81 | $2,350.86 | 75 |
| COST | 2 | $979.83 | $985.10 | $1,970.20 | 65 |
| CRM | 8 | $268.33 | $270.73 | $2,165.83 | 65 |
| CSCO | 33 | $68.37 | $68.93 | $2,274.69 | 75 |
| CVX | 16 | $146.70 | $146.03 | $2,336.48 | 75 |
| DIS | 17 | $122.86 | $123.14 | $2,093.30 | 65 |
| GOOGL | 12 | $179.64 | $176.68 | $2,120.16 | 70 |
| GS | 3 | $717.52 | $713.73 | $2,141.18 | 75 |
| HD | 6 | $372.64 | $366.73 | $2,200.35 | 65 |
| INTC | 84 | $22.27 | $22.02 | $1,850.10 | 60 |
| JNJ | 13 | $155.80 | $155.15 | $2,016.95 | 65 |
| JPM | 9 | $292.50 | $291.99 | $2,627.95 | 85 |
| KO | 28 | $71.03 | $70.86 | $1,984.22 | 65 |
| LLY | 2 | $776.66 | $771.45 | $1,542.89 | 65 |
| MA | 4 | $563.08 | $563.11 | $2,252.44 | 65 |
| META | 3 | $717.12 | $721.99 | $2,165.98 | 70 |
| MRK | 29 | $82.38 | $81.06 | $2,350.60 | 75 |
| MSFT | 5 | $498.84 | $497.36 | $2,486.80 | 70 |
| NFLX | 1 | $1,279.00 | $1,287.03 | $1,287.03 | 65 |
| NKE | 30 | $75.86 | $76.32 | $2,289.60 | 75 |
| NVDA | 16 | $156.42 | $158.11 | $2,529.76 | 85 |
| ORCL | 9 | $226.15 | $233.08 | $2,097.72 | 65 |
| PEP | 15 | $136.59 | $134.30 | $2,014.50 | 65 |
| PFE | 85 | $25.31 | $25.21 | $2,142.95 | 70 |
| PG | 13 | $160.77 | $159.39 | $2,072.07 | 70 |
| PYPL | 30 | $76.81 | $76.25 | $2,287.65 | 75 |
| QCOM | 15 | $161.55 | $159.07 | $2,386.05 | 75 |
| T | 72 | $28.54 | $28.25 | $2,033.66 | 65 |
| TGT | 20 | $104.92 | $101.11 | $2,022.10 | 65 |
| TSLA | 6 | $288.90 | $292.62 | $1,755.72 | 65 |
| UNH | 7 | $314.75 | $303.87 | $2,127.10 | 65 |
| UNP | 10 | $236.52 | $235.40 | $2,354.00 | 75 |
| V | 6 | $355.95 | $356.32 | $2,137.95 | 70 |
| VZ | 47 | $43.72 | $42.69 | $2,006.65 | 65 |
| WFC | 31 | $82.25 | $82.16 | $2,546.80 | 85 |
| WMT | 23 | $97.35 | $98.11 | $2,256.53 | 75 |
| XOM | 20 | $109.91 | $111.14 | $2,222.80 | 75 |

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
| 2025-07-07 15:51:00 | SELL | UNP | 1 | $235.89 | $-0.57 | 75 |
| 2025-07-07 15:51:00 | SELL | T | 6 | $28.30 | $-1.38 | 65 |
| 2025-07-07 15:51:00 | BUY | V | 6 | $355.95 | N/A | 70 |
| 2025-07-07 15:51:00 | BUY | NVDA | 2 | $157.97 | N/A | 85 |
| 2025-07-07 15:51:00 | BUY | PYPL | 1 | $76.19 | N/A | 75 |

<!--TRADE_LOG_END--> 
