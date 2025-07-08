# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 14:26:11**

| Metric | Value |
|---|---|
| **Total Value** | **$100,677.59** |
| Cash | $835.17 |
| Holdings Value | $99,842.41 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.45 | $2,094.46 | 65 |
| ADBE | 5 | $377.60 | $381.00 | $1,905.00 | 65 |
| AMD | 16 | $135.69 | $136.63 | $2,186.08 | 70 |
| AMZN | 10 | $221.61 | $221.11 | $2,211.10 | 70 |
| AVGO | 8 | $275.34 | $273.14 | $2,185.12 | 70 |
| AXP | 8 | $324.24 | $320.25 | $2,562.00 | 85 |
| BA | 10 | $212.15 | $215.88 | $2,158.75 | 65 |
| BAC | 47 | $48.73 | $47.44 | $2,229.51 | 70 |
| C | 26 | $86.67 | $86.01 | $2,236.26 | 70 |
| CAT | 6 | $397.86 | $392.67 | $2,356.02 | 65 |
| COST | 2 | $979.83 | $989.88 | $1,979.77 | 65 |
| CRM | 8 | $268.33 | $274.26 | $2,194.08 | 65 |
| CSCO | 33 | $68.38 | $68.47 | $2,259.35 | 70 |
| CVX | 16 | $146.65 | $150.34 | $2,405.52 | 75 |
| DIS | 18 | $122.81 | $122.40 | $2,203.20 | 70 |
| GOOGL | 12 | $179.60 | $174.86 | $2,098.32 | 65 |
| GS | 3 | $717.52 | $698.32 | $2,094.96 | 70 |
| HD | 6 | $372.64 | $367.26 | $2,203.59 | 65 |
| INTC | 89 | $22.29 | $22.94 | $2,041.76 | 65 |
| JNJ | 14 | $155.86 | $156.58 | $2,192.12 | 70 |
| JPM | 9 | $291.61 | $284.24 | $2,558.16 | 85 |
| KO | 29 | $71.03 | $70.31 | $2,038.85 | 65 |
| LLY | 2 | $776.66 | $787.68 | $1,575.36 | 65 |
| MA | 4 | $563.08 | $563.50 | $2,254.00 | 65 |
| META | 3 | $717.12 | $716.87 | $2,150.61 | 65 |
| MRK | 29 | $82.43 | $81.83 | $2,373.07 | 75 |
| MSFT | 5 | $498.84 | $495.95 | $2,479.75 | 75 |
| NFLX | 1 | $1,279.00 | $1,271.57 | $1,271.57 | 65 |
| NKE | 28 | $76.04 | $74.34 | $2,081.40 | 65 |
| NVDA | 15 | $156.45 | $158.68 | $2,380.27 | 75 |
| ORCL | 9 | $233.41 | $237.20 | $2,134.80 | 65 |
| PEP | 15 | $136.57 | $134.79 | $2,021.85 | 65 |
| PFE | 86 | $25.29 | $25.74 | $2,213.28 | 70 |
| PG | 13 | $160.77 | $158.38 | $2,058.94 | 65 |
| PYPL | 31 | $76.64 | $75.10 | $2,328.10 | 75 |
| QCOM | 14 | $161.75 | $159.11 | $2,227.54 | 75 |
| T | 73 | $28.54 | $28.17 | $2,056.21 | 65 |
| TGT | 20 | $104.90 | $101.43 | $2,028.60 | 65 |
| TSLA | 6 | $288.62 | $299.24 | $1,795.44 | 60 |
| UNH | 7 | $314.75 | $306.10 | $2,142.70 | 65 |
| UNP | 10 | $236.53 | $236.61 | $2,366.10 | 75 |
| V | 6 | $355.95 | $356.14 | $2,136.87 | 65 |
| VZ | 47 | $43.72 | $42.99 | $2,020.52 | 65 |
| WFC | 32 | $82.29 | $81.64 | $2,612.64 | 85 |
| WMT | 23 | $97.38 | $97.87 | $2,251.07 | 75 |
| XOM | 22 | $110.11 | $113.08 | $2,487.76 | 80 |

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
| 2025-07-08 14:26:03 | SELL | BAC | 2 | $47.44 | $-2.47 | 70 |
| 2025-07-08 14:26:03 | SELL | NVDA | 1 | $158.69 | $2.10 | 75 |
| 2025-07-08 14:26:03 | SELL | PFE | 1 | $25.74 | $0.44 | 70 |
| 2025-07-08 14:26:03 | SELL | C | 4 | $86.01 | $-2.27 | 70 |
| 2025-07-08 14:26:03 | SELL | CVX | 1 | $150.30 | $3.44 | 75 |
| 2025-07-08 14:26:03 | BUY | JNJ | 1 | $156.58 | N/A | 70 |
| 2025-07-08 14:26:03 | BUY | JPM | 1 | $284.00 | N/A | 85 |
| 2025-07-08 14:26:03 | BUY | AMD | 1 | $136.73 | N/A | 70 |
| 2025-07-08 14:26:03 | BUY | XOM | 1 | $113.11 | N/A | 80 |
| 2025-07-08 14:26:03 | BUY | DIS | 1 | $122.42 | N/A | 70 |
| 2025-07-08 14:26:03 | BUY | WFC | 3 | $81.67 | N/A | 85 |
| 2025-07-08 14:08:44 | SELL | AMD | 1 | $136.47 | $0.79 | 65 |
| 2025-07-08 14:08:44 | SELL | NKE | 3 | $73.92 | $-5.75 | 65 |
| 2025-07-08 14:08:44 | SELL | T | 4 | $28.22 | $-1.23 | 65 |
| 2025-07-08 14:08:44 | BUY | BAC | 2 | $47.51 | N/A | 75 |
| 2025-07-08 14:08:44 | BUY | PYPL | 4 | $75.20 | N/A | 75 |
| 2025-07-08 14:08:44 | BUY | MRK | 1 | $81.14 | N/A | 75 |
| 2025-07-08 14:08:44 | BUY | CVX | 1 | $149.45 | N/A | 85 |
| 2025-07-08 13:48:02 | SELL | AMZN | 1 | $222.81 | $1.09 | 70 |
| 2025-07-08 13:48:02 | SELL | BAC | 1 | $47.74 | $-0.97 | 70 |
| 2025-07-08 13:48:02 | SELL | CSCO | 1 | $68.65 | $0.26 | 70 |
| 2025-07-08 13:48:02 | BUY | NVDA | 3 | $158.83 | N/A | 85 |
| 2025-07-08 13:48:02 | BUY | INTC | 3 | $22.81 | N/A | 65 |
| 2025-07-08 13:48:02 | BUY | NKE | 1 | $75.03 | N/A | 75 |
| 2025-07-08 13:48:02 | BUY | MRK | 2 | $81.68 | N/A | 75 |

<!--TRADE_LOG_END--> 
