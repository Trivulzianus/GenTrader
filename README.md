# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 16:43:44**

| Metric | Value |
|---|---|
| **Total Value** | **$100,719.74** |
| Cash | $1,601.01 |
| Holdings Value | $99,118.73 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $207.73 | $2,077.29 | 70 |
| ADBE | 5 | $377.60 | $374.23 | $1,871.15 | 65 |
| AMD | 15 | $135.39 | $138.15 | $2,072.18 | 70 |
| AMZN | 10 | $221.83 | $222.62 | $2,226.25 | 75 |
| AVGO | 8 | $275.34 | $278.10 | $2,224.76 | 70 |
| AXP | 7 | $325.28 | $317.48 | $2,222.36 | 75 |
| BA | 10 | $212.53 | $228.26 | $2,282.60 | 70 |
| BAC | 44 | $48.84 | $46.74 | $2,056.78 | 65 |
| C | 28 | $86.76 | $85.68 | $2,399.04 | 75 |
| CAT | 6 | $397.86 | $400.51 | $2,403.09 | 65 |
| COST | 2 | $979.83 | $976.47 | $1,952.93 | 65 |
| CRM | 8 | $268.33 | $269.98 | $2,159.80 | 65 |
| CSCO | 32 | $68.33 | $68.78 | $2,200.80 | 70 |
| CVX | 17 | $147.03 | $152.71 | $2,596.07 | 85 |
| DIS | 18 | $122.81 | $121.03 | $2,178.63 | 70 |
| GOOGL | 13 | $179.50 | $177.57 | $2,308.40 | 75 |
| GS | 3 | $717.52 | $695.58 | $2,086.74 | 70 |
| HD | 6 | $372.64 | $365.81 | $2,194.83 | 65 |
| INTC | 87 | $22.34 | $23.27 | $2,024.92 | 65 |
| JNJ | 13 | $155.89 | $155.53 | $2,021.83 | 65 |
| JPM | 9 | $291.61 | $282.60 | $2,543.40 | 75 |
| KO | 29 | $71.03 | $69.34 | $2,011.00 | 65 |
| LLY | 2 | $776.66 | $785.37 | $1,570.73 | 65 |
| MA | 4 | $563.08 | $560.14 | $2,240.56 | 65 |
| META | 3 | $717.12 | $736.08 | $2,208.24 | 85 |
| MRK | 28 | $82.45 | $83.84 | $2,347.64 | 75 |
| MSFT | 5 | $498.84 | $500.70 | $2,503.52 | 70 |
| NFLX | 1 | $1,279.00 | $1,280.55 | $1,280.55 | 65 |
| NKE | 28 | $76.06 | $73.74 | $2,064.72 | 65 |
| NVDA | 16 | $157.22 | $163.10 | $2,609.68 | 85 |
| ORCL | 10 | $233.47 | $234.50 | $2,344.95 | 70 |
| PEP | 15 | $136.57 | $133.72 | $2,005.80 | 65 |
| PFE | 92 | $25.24 | $25.42 | $2,338.92 | 75 |
| PG | 13 | $160.75 | $156.66 | $2,036.58 | 65 |
| PYPL | 31 | $76.63 | $74.69 | $2,315.54 | 75 |
| QCOM | 14 | $161.87 | $158.78 | $2,222.89 | 75 |
| T | 72 | $28.56 | $28.05 | $2,019.96 | 65 |
| TGT | 20 | $104.89 | $102.35 | $2,047.00 | 65 |
| TSLA | 6 | $288.62 | $295.34 | $1,772.07 | 65 |
| UNH | 7 | $314.75 | $300.55 | $2,103.85 | 65 |
| UNP | 9 | $236.60 | $237.07 | $2,133.63 | 75 |
| V | 6 | $355.95 | $353.88 | $2,123.28 | 70 |
| VZ | 48 | $43.15 | $42.59 | $2,044.32 | 65 |
| WFC | 29 | $82.28 | $81.47 | $2,362.63 | 75 |
| WMT | 21 | $97.35 | $97.06 | $2,038.23 | 65 |
| XOM | 20 | $109.83 | $113.43 | $2,268.60 | 75 |

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
| 2025-07-09 16:08:18 | SELL | PYPL | 3 | $74.78 | $-5.58 | 65 |
| 2025-07-09 16:08:18 | BUY | BAC | 4 | $46.86 | N/A | 75 |
| 2025-07-09 16:08:18 | BUY | CVX | 1 | $153.09 | N/A | 85 |
| 2025-07-09 15:51:57 | SELL | WFC | 1 | $81.78 | $-0.48 | 75 |
| 2025-07-09 15:51:57 | SELL | CSCO | 2 | $68.74 | $0.76 | 70 |

<!--TRADE_LOG_END--> 
