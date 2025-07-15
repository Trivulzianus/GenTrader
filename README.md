# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 13:49:09**

| Metric | Value |
|---|---|
| **Total Value** | **$101,094.70** |
| Cash | $860.58 |
| Holdings Value | $100,234.12 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.91 | $2,099.05 | 65 |
| ADBE | 6 | $375.23 | $367.48 | $2,204.85 | 65 |
| AMD | 16 | $146.24 | $158.03 | $2,528.48 | 75 |
| AMZN | 10 | $221.56 | $226.13 | $2,261.30 | 70 |
| AVGO | 8 | $275.34 | $279.33 | $2,234.64 | 65 |
| AXP | 7 | $325.34 | $314.37 | $2,200.59 | 65 |
| BA | 10 | $212.74 | $230.07 | $2,300.75 | 70 |
| BAC | 47 | $48.69 | $46.41 | $2,181.51 | 70 |
| C | 30 | $86.79 | $88.60 | $2,658.00 | 85 |
| CAT | 6 | $397.74 | $405.66 | $2,433.96 | 70 |
| COST | 2 | $979.83 | $972.65 | $1,945.30 | 65 |
| CRM | 7 | $268.68 | $261.15 | $1,828.05 | 65 |
| CSCO | 32 | $68.43 | $67.42 | $2,157.28 | 70 |
| CVX | 16 | $146.79 | $151.69 | $2,427.10 | 75 |
| DIS | 17 | $122.96 | $119.65 | $2,034.05 | 65 |
| GOOGL | 14 | $179.74 | $181.86 | $2,546.04 | 85 |
| GS | 3 | $717.52 | $706.24 | $2,118.72 | 85 |
| HD | 6 | $372.64 | $366.88 | $2,201.25 | 65 |
| INTC | 87 | $22.38 | $23.55 | $2,048.73 | 65 |
| JNJ | 13 | $155.95 | $156.47 | $2,034.15 | 65 |
| JPM | 9 | $291.63 | $287.50 | $2,587.55 | 85 |
| KO | 29 | $71.03 | $69.34 | $2,010.89 | 65 |
| LLY | 3 | $781.32 | $801.11 | $2,403.34 | 85 |
| MA | 4 | $563.08 | $551.29 | $2,205.16 | 65 |
| META | 3 | $717.12 | $721.72 | $2,165.16 | 70 |
| MRK | 29 | $82.54 | $83.87 | $2,432.24 | 75 |
| MSFT | 5 | $498.84 | $505.04 | $2,525.18 | 85 |
| NFLX | 1 | $1,279.00 | $1,259.07 | $1,259.07 | 65 |
| NKE | 30 | $72.05 | $72.31 | $2,169.30 | 70 |
| NVDA | 13 | $155.65 | $171.06 | $2,223.78 | 70 |
| ORCL | 9 | $233.27 | $231.85 | $2,086.68 | 65 |
| PEP | 15 | $136.57 | $134.66 | $2,019.97 | 65 |
| PFE | 86 | $25.21 | $25.38 | $2,182.25 | 70 |
| PG | 14 | $160.31 | $153.50 | $2,149.00 | 65 |
| PYPL | 28 | $72.13 | $73.39 | $2,055.06 | 65 |
| QCOM | 14 | $153.83 | $155.78 | $2,180.92 | 65 |
| T | 75 | $27.10 | $27.00 | $2,025.38 | 65 |
| TGT | 20 | $104.94 | $104.34 | $2,086.86 | 65 |
| TSLA | 6 | $318.51 | $318.85 | $1,913.10 | 65 |
| UNH | 7 | $298.51 | $297.87 | $2,085.09 | 65 |
| UNP | 9 | $236.56 | $232.06 | $2,088.54 | 65 |
| V | 6 | $355.85 | $348.69 | $2,092.11 | 65 |
| VZ | 49 | $43.12 | $41.37 | $2,027.36 | 65 |
| WFC | 32 | $82.40 | $79.56 | $2,545.92 | 85 |
| WMT | 21 | $97.38 | $95.14 | $1,997.94 | 65 |
| XOM | 20 | $109.83 | $113.62 | $2,272.50 | 70 |

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
| 2025-07-15 13:49:01 | SELL | AMZN | 1 | $226.07 | $4.10 | 70 |
| 2025-07-15 13:49:01 | SELL | XOM | 1 | $113.65 | $3.64 | 70 |
| 2025-07-15 13:49:01 | SELL | PYPL | 3 | $73.38 | $3.39 | 65 |
| 2025-07-15 13:49:01 | SELL | NVDA | 1 | $170.90 | $14.16 | 70 |
| 2025-07-15 13:49:01 | SELL | MRK | 2 | $83.67 | $2.12 | 75 |
| 2025-07-15 13:49:01 | SELL | BA | 1 | $229.75 | $15.46 | 70 |
| 2025-07-15 13:49:01 | SELL | CVX | 1 | $151.68 | $4.60 | 75 |
| 2025-07-15 13:49:01 | BUY | TSLA | 6 | $318.51 | N/A | 65 |
| 2025-07-15 13:49:01 | BUY | AMD | 16 | $146.24 | N/A | 75 |
| 2025-07-15 13:49:01 | BUY | BAC | 1 | $46.42 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | NKE | 2 | $72.33 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | PFE | 5 | $25.38 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | C | 5 | $88.64 | N/A | 85 |
| 2025-07-15 13:49:01 | BUY | WFC | 4 | $83.43 | N/A | 85 |
| 2025-07-15 13:49:01 | BUY | CSCO | 2 | $67.42 | N/A | 70 |
| 2025-07-15 13:49:01 | BUY | T | 1 | $27.01 | N/A | 65 |
| 2025-07-15 13:48:44 | SELL | TSLA | 6 | $318.64 | $180.11 | 60 |
| 2025-07-15 13:48:38 | SELL | AMD | 15 | $158.18 | $351.98 | 70 |
| 2025-07-15 13:29:31 | SELL | PFE | 5 | $25.35 | $0.70 | 65 |
| 2025-07-15 13:29:31 | SELL | C | 5 | $87.50 | $4.50 | 70 |
| 2025-07-15 13:29:31 | BUY | GOOGL | 1 | $181.56 | N/A | 85 |
| 2025-07-15 13:29:31 | BUY | INTC | 1 | $23.30 | N/A | 65 |
| 2025-07-15 13:29:31 | BUY | PYPL | 3 | $73.89 | N/A | 75 |
| 2025-07-15 13:29:31 | BUY | MRK | 3 | $83.67 | N/A | 85 |
| 2025-07-15 13:05:01 | SELL | BAC | 1 | $47.07 | $-1.63 | 70 |

<!--TRADE_LOG_END--> 
