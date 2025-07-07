# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 16:09:39**

| Metric | Value |
|---|---|
| **Total Value** | **$100,923.26** |
| Cash | $627.85 |
| Holdings Value | $100,295.40 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $211.93 | $2,119.30 | 70 |
| ADBE | 5 | $377.60 | $377.98 | $1,889.90 | 65 |
| AMD | 15 | $135.76 | $135.38 | $2,030.70 | 65 |
| AMZN | 11 | $221.66 | $224.12 | $2,465.38 | 75 |
| AVGO | 8 | $269.90 | $276.74 | $2,213.92 | 70 |
| AXP | 7 | $324.46 | $323.93 | $2,267.51 | 75 |
| BA | 10 | $212.15 | $215.55 | $2,155.50 | 70 |
| BAC | 54 | $48.71 | $48.85 | $2,638.01 | 85 |
| C | 30 | $86.68 | $87.99 | $2,639.70 | 85 |
| CAT | 6 | $397.86 | $393.53 | $2,361.18 | 75 |
| COST | 2 | $979.83 | $985.42 | $1,970.84 | 65 |
| CRM | 8 | $268.33 | $271.39 | $2,171.12 | 65 |
| CSCO | 33 | $68.37 | $69.09 | $2,279.97 | 75 |
| CVX | 16 | $146.70 | $146.42 | $2,342.72 | 75 |
| DIS | 17 | $122.86 | $123.38 | $2,097.46 | 70 |
| GOOGL | 12 | $179.64 | $177.37 | $2,128.44 | 65 |
| GS | 3 | $717.52 | $715.40 | $2,146.20 | 70 |
| HD | 6 | $372.64 | $367.70 | $2,206.20 | 65 |
| INTC | 84 | $22.27 | $22.10 | $1,856.69 | 60 |
| JNJ | 13 | $155.80 | $155.47 | $2,021.11 | 65 |
| JPM | 9 | $292.50 | $292.36 | $2,631.20 | 85 |
| KO | 28 | $71.03 | $70.93 | $1,986.04 | 65 |
| LLY | 2 | $776.66 | $772.00 | $1,544.00 | 65 |
| MA | 4 | $563.08 | $564.11 | $2,256.44 | 65 |
| META | 3 | $717.12 | $722.75 | $2,168.25 | 70 |
| MRK | 29 | $82.38 | $81.35 | $2,359.15 | 75 |
| MSFT | 5 | $498.84 | $498.23 | $2,491.15 | 85 |
| NFLX | 1 | $1,279.00 | $1,288.56 | $1,288.56 | 65 |
| NKE | 29 | $75.85 | $76.50 | $2,218.36 | 70 |
| NVDA | 16 | $156.42 | $158.41 | $2,534.57 | 85 |
| ORCL | 10 | $226.85 | $234.39 | $2,343.90 | 70 |
| PEP | 15 | $136.59 | $134.53 | $2,017.95 | 65 |
| PFE | 85 | $25.31 | $25.25 | $2,146.25 | 70 |
| PG | 13 | $160.77 | $159.94 | $2,079.21 | 70 |
| PYPL | 30 | $76.81 | $76.45 | $2,293.65 | 75 |
| QCOM | 15 | $161.55 | $159.59 | $2,393.85 | 80 |
| T | 76 | $28.53 | $28.27 | $2,148.90 | 70 |
| TGT | 20 | $104.92 | $101.40 | $2,028.00 | 65 |
| TSLA | 6 | $288.90 | $294.17 | $1,765.00 | 65 |
| UNH | 7 | $314.75 | $305.00 | $2,134.97 | 65 |
| UNP | 10 | $236.52 | $235.75 | $2,357.50 | 75 |
| V | 6 | $355.95 | $356.29 | $2,137.71 | 65 |
| VZ | 47 | $43.72 | $42.80 | $2,011.84 | 65 |
| WFC | 30 | $82.25 | $82.34 | $2,470.20 | 80 |
| WMT | 23 | $97.35 | $98.20 | $2,258.52 | 70 |
| XOM | 20 | $109.91 | $111.42 | $2,228.40 | 70 |

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
| 2025-07-07 15:51:00 | BUY | WMT | 2 | $98.05 | N/A | 75 |
| 2025-07-07 15:51:00 | BUY | CVX | 1 | $146.38 | N/A | 85 |
| 2025-07-07 15:39:15 | SELL | V | 6 | $356.17 | $19.60 | 65 |
| 2025-07-07 15:39:15 | SELL | DIS | 1 | $123.32 | $0.44 | 65 |
| 2025-07-07 15:39:15 | SELL | WMT | 2 | $98.19 | $1.67 | 65 |
| 2025-07-07 15:39:15 | SELL | PYPL | 1 | $76.31 | $-0.50 | 70 |

<!--TRADE_LOG_END--> 
