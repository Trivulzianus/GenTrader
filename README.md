# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 16:56:57**

| Metric | Value |
|---|---|
| **Total Value** | **$100,785.19** |
| Cash | $1,687.25 |
| Holdings Value | $99,097.94 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $208.26 | $2,082.60 | 65 |
| ADBE | 5 | $377.60 | $373.20 | $1,866.00 | 65 |
| AMD | 15 | $135.39 | $138.57 | $2,078.55 | 65 |
| AMZN | 10 | $221.83 | $222.81 | $2,228.05 | 75 |
| AVGO | 8 | $275.34 | $277.95 | $2,223.64 | 65 |
| AXP | 7 | $325.28 | $317.95 | $2,225.65 | 75 |
| BA | 10 | $212.53 | $229.24 | $2,292.40 | 70 |
| BAC | 46 | $48.75 | $46.74 | $2,150.25 | 70 |
| C | 31 | $86.66 | $85.75 | $2,658.10 | 85 |
| CAT | 6 | $397.86 | $400.92 | $2,405.52 | 85 |
| COST | 2 | $979.83 | $976.62 | $1,953.24 | 65 |
| CRM | 8 | $268.33 | $269.87 | $2,158.96 | 65 |
| CSCO | 32 | $68.33 | $68.85 | $2,203.07 | 70 |
| CVX | 17 | $147.03 | $153.11 | $2,602.87 | 85 |
| DIS | 18 | $122.81 | $121.02 | $2,178.27 | 70 |
| GOOGL | 13 | $179.50 | $177.56 | $2,308.28 | 70 |
| GS | 3 | $717.52 | $696.10 | $2,088.30 | 70 |
| HD | 6 | $372.64 | $365.55 | $2,193.30 | 65 |
| INTC | 87 | $22.34 | $23.28 | $2,025.74 | 65 |
| JNJ | 13 | $155.89 | $155.44 | $2,020.65 | 65 |
| JPM | 9 | $291.61 | $282.83 | $2,545.47 | 75 |
| KO | 29 | $71.03 | $69.16 | $2,005.50 | 65 |
| LLY | 2 | $776.66 | $785.82 | $1,571.64 | 65 |
| MA | 4 | $563.08 | $560.02 | $2,240.08 | 65 |
| META | 3 | $717.12 | $734.76 | $2,204.28 | 85 |
| MRK | 28 | $82.45 | $83.86 | $2,348.08 | 75 |
| MSFT | 5 | $498.84 | $500.68 | $2,503.39 | 70 |
| NFLX | 1 | $1,279.00 | $1,280.50 | $1,280.50 | 65 |
| NKE | 28 | $76.06 | $73.83 | $2,067.24 | 65 |
| NVDA | 16 | $157.22 | $163.24 | $2,611.84 | 85 |
| ORCL | 9 | $233.31 | $234.94 | $2,114.51 | 65 |
| PEP | 15 | $136.57 | $133.62 | $2,004.30 | 65 |
| PFE | 87 | $25.22 | $25.44 | $2,213.28 | 70 |
| PG | 13 | $160.75 | $156.48 | $2,034.24 | 65 |
| PYPL | 30 | $76.69 | $74.84 | $2,245.20 | 70 |
| QCOM | 14 | $161.87 | $158.99 | $2,225.79 | 75 |
| T | 72 | $28.56 | $28.06 | $2,020.32 | 65 |
| TGT | 20 | $104.89 | $102.31 | $2,046.20 | 65 |
| TSLA | 6 | $288.62 | $295.57 | $1,773.44 | 65 |
| UNH | 7 | $314.75 | $302.18 | $2,115.26 | 65 |
| UNP | 9 | $236.60 | $237.06 | $2,133.54 | 75 |
| V | 6 | $355.95 | $354.34 | $2,126.04 | 70 |
| VZ | 48 | $43.15 | $42.66 | $2,047.68 | 65 |
| WFC | 29 | $82.28 | $81.64 | $2,367.41 | 75 |
| WMT | 21 | $97.35 | $97.01 | $2,037.17 | 65 |
| XOM | 20 | $109.83 | $113.61 | $2,272.10 | 75 |

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
| 2025-07-09 16:56:47 | SELL | PYPL | 1 | $74.84 | $-1.79 | 70 |
| 2025-07-09 16:56:47 | SELL | PFE | 5 | $25.44 | $1.02 | 70 |
| 2025-07-09 16:56:47 | SELL | ORCL | 1 | $234.93 | $1.46 | 65 |
| 2025-07-09 16:56:47 | BUY | BAC | 2 | $46.74 | N/A | 70 |
| 2025-07-09 16:56:47 | BUY | C | 3 | $85.75 | N/A | 85 |
| 2025-07-09 16:43:39 | SELL | NKE | 1 | $73.73 | $-2.24 | 65 |
| 2025-07-09 16:43:39 | SELL | MRK | 1 | $83.84 | $1.35 | 75 |
| 2025-07-09 16:43:39 | SELL | C | 3 | $85.68 | $-2.94 | 75 |
| 2025-07-09 16:43:39 | SELL | WFC | 1 | $81.47 | $-0.78 | 75 |
| 2025-07-09 16:43:39 | BUY | NVDA | 2 | $163.10 | N/A | 85 |
| 2025-07-09 16:43:39 | BUY | DIS | 1 | $121.03 | N/A | 70 |
| 2025-07-09 16:43:39 | BUY | PFE | 6 | $25.42 | N/A | 75 |
| 2025-07-09 16:43:39 | BUY | CVX | 1 | $152.71 | N/A | 85 |
| 2025-07-09 16:26:59 | SELL | NVDA | 1 | $163.21 | $6.37 | 70 |
| 2025-07-09 16:26:59 | SELL | BAC | 6 | $46.79 | $-10.79 | 65 |
| 2025-07-09 16:26:59 | SELL | DIS | 2 | $121.05 | $-3.34 | 65 |
| 2025-07-09 16:26:59 | SELL | CVX | 1 | $152.81 | $5.77 | 75 |
| 2025-07-09 16:26:59 | BUY | PYPL | 3 | $74.68 | N/A | 75 |
| 2025-07-09 16:26:59 | BUY | NKE | 1 | $73.87 | N/A | 70 |
| 2025-07-09 16:26:59 | BUY | WFC | 1 | $81.67 | N/A | 80 |
| 2025-07-09 16:26:59 | BUY | BA | 1 | $228.20 | N/A | 75 |
| 2025-07-09 16:26:59 | BUY | C | 1 | $85.85 | N/A | 85 |
| 2025-07-09 16:08:18 | SELL | NVDA | 1 | $163.02 | $5.80 | 75 |
| 2025-07-09 16:08:18 | SELL | XOM | 1 | $113.87 | $3.85 | 70 |
| 2025-07-09 16:08:18 | SELL | NKE | 1 | $73.90 | $-2.07 | 65 |

<!--TRADE_LOG_END--> 
