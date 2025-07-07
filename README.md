# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 14:09:25**

| Metric | Value |
|---|---|
| **Total Value** | **$101,158.18** |
| Cash | $863.46 |
| Holdings Value | $100,294.72 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $212.69 | $2,126.95 | 65 |
| ADBE | 5 | $377.60 | $380.07 | $1,900.35 | 65 |
| AMD | 15 | $135.79 | $135.61 | $2,034.15 | 65 |
| AMZN | 11 | $221.66 | $223.15 | $2,454.65 | 75 |
| AVGO | 8 | $269.90 | $275.26 | $2,202.10 | 70 |
| AXP | 8 | $324.34 | $327.02 | $2,616.16 | 85 |
| BA | 10 | $212.15 | $215.20 | $2,152.00 | 70 |
| BAC | 53 | $48.70 | $49.06 | $2,600.18 | 85 |
| C | 25 | $86.43 | $88.31 | $2,207.62 | 70 |
| CAT | 6 | $397.86 | $396.19 | $2,377.17 | 70 |
| COST | 2 | $979.83 | $977.03 | $1,954.06 | 65 |
| CRM | 8 | $268.33 | $273.46 | $2,187.68 | 65 |
| CSCO | 33 | $68.36 | $68.96 | $2,275.68 | 75 |
| CVX | 15 | $146.54 | $148.14 | $2,222.10 | 75 |
| DIS | 17 | $122.82 | $123.82 | $2,104.94 | 70 |
| GOOGL | 13 | $179.40 | $177.77 | $2,311.00 | 70 |
| GS | 3 | $717.52 | $718.78 | $2,156.36 | 75 |
| HD | 6 | $372.64 | $371.32 | $2,227.92 | 65 |
| INTC | 90 | $22.27 | $22.27 | $2,004.75 | 65 |
| JNJ | 13 | $155.80 | $156.10 | $2,029.30 | 65 |
| JPM | 9 | $292.50 | $293.61 | $2,642.49 | 85 |
| KO | 28 | $71.03 | $71.00 | $1,987.86 | 65 |
| LLY | 2 | $776.66 | $766.10 | $1,532.19 | 65 |
| MA | 4 | $563.08 | $566.86 | $2,267.44 | 65 |
| META | 3 | $717.12 | $722.59 | $2,167.77 | 75 |
| MRK | 29 | $82.33 | $81.43 | $2,361.47 | 75 |
| MSFT | 5 | $498.84 | $496.93 | $2,484.65 | 85 |
| NFLX | 1 | $1,279.00 | $1,280.70 | $1,280.70 | 70 |
| NKE | 32 | $75.92 | $76.70 | $2,454.40 | 80 |
| NVDA | 16 | $156.39 | $158.21 | $2,531.33 | 85 |
| ORCL | 10 | $226.66 | $230.53 | $2,305.30 | 70 |
| PEP | 15 | $136.59 | $134.66 | $2,019.83 | 65 |
| PFE | 79 | $25.30 | $25.48 | $2,013.32 | 65 |
| PG | 13 | $160.77 | $160.21 | $2,082.73 | 70 |
| PYPL | 30 | $76.81 | $76.69 | $2,300.55 | 75 |
| QCOM | 14 | $161.69 | $159.33 | $2,230.62 | 75 |
| T | 71 | $28.54 | $28.28 | $2,008.21 | 65 |
| TGT | 19 | $105.09 | $102.96 | $1,956.24 | 65 |
| TSLA | 6 | $288.90 | $294.98 | $1,769.88 | 65 |
| UNH | 7 | $314.75 | $305.57 | $2,138.99 | 65 |
| UNP | 11 | $236.50 | $237.23 | $2,609.53 | 85 |
| V | 6 | $352.90 | $356.82 | $2,140.95 | 65 |
| VZ | 46 | $43.73 | $43.06 | $1,980.99 | 65 |
| WFC | 30 | $82.30 | $83.06 | $2,491.85 | 80 |
| WMT | 22 | $97.31 | $97.75 | $2,150.61 | 70 |
| XOM | 20 | $109.90 | $111.98 | $2,239.70 | 75 |

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
| 2025-07-07 14:09:13 | SELL | MRK | 3 | $81.42 | $-2.49 | 75 |
| 2025-07-07 14:09:13 | SELL | PFE | 11 | $25.48 | $1.80 | 65 |
| 2025-07-07 14:09:13 | SELL | WFC | 1 | $83.07 | $0.74 | 80 |
| 2025-07-07 14:09:13 | SELL | T | 4 | $28.36 | $-0.68 | 65 |
| 2025-07-07 14:09:13 | BUY | WMT | 1 | $97.79 | N/A | 70 |
| 2025-07-07 14:09:13 | BUY | PYPL | 1 | $76.65 | N/A | 75 |
| 2025-07-07 14:09:13 | BUY | NKE | 3 | $76.68 | N/A | 80 |
| 2025-07-07 13:56:10 | SELL | AMD | 1 | $137.91 | $1.99 | 65 |
| 2025-07-07 13:56:10 | SELL | WMT | 1 | $98.00 | $0.68 | 65 |
| 2025-07-07 13:56:10 | BUY | TSLA | 6 | $288.90 | N/A | 65 |
| 2025-07-07 13:56:10 | BUY | NKE | 1 | $76.93 | N/A | 75 |
| 2025-07-07 13:56:10 | BUY | PFE | 10 | $25.44 | N/A | 75 |
| 2025-07-07 13:56:10 | BUY | MRK | 8 | $81.08 | N/A | 85 |
| 2025-07-07 13:56:10 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-07 13:56:10 | BUY | T | 5 | $28.46 | N/A | 70 |
| 2025-07-07 13:55:59 | SELL | TSLA | 5 | $288.88 | $-132.35 | 60 |
| 2025-07-07 13:46:03 | SELL | XOM | 1 | $111.39 | $1.42 | 70 |
| 2025-07-07 13:46:03 | SELL | PYPL | 1 | $76.46 | $-0.34 | 70 |
| 2025-07-07 13:46:03 | SELL | PFE | 4 | $25.45 | $0.55 | 65 |
| 2025-07-07 13:46:03 | SELL | C | 4 | $88.65 | $7.67 | 70 |
| 2025-07-07 13:46:03 | SELL | WFC | 1 | $83.47 | $1.15 | 80 |
| 2025-07-07 13:46:03 | SELL | ORCL | 1 | $231.60 | $4.49 | 70 |
| 2025-07-07 13:46:03 | SELL | QCOM | 1 | $159.20 | $-2.32 | 70 |
| 2025-07-07 13:46:03 | SELL | CVX | 2 | $147.30 | $1.34 | 70 |
| 2025-07-07 13:46:03 | BUY | TSLA | 5 | $315.35 | N/A | 60 |

<!--TRADE_LOG_END--> 
