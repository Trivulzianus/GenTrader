# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 17:09:45**

| Metric | Value |
|---|---|
| **Total Value** | **$100,819.53** |
| Cash | $528.45 |
| Holdings Value | $100,291.09 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.81 | $2,088.15 | 65 |
| ADBE | 6 | $375.23 | $365.53 | $2,193.18 | 65 |
| AMD | 15 | $134.72 | $146.93 | $2,204.02 | 70 |
| AMZN | 11 | $221.92 | $226.01 | $2,486.11 | 75 |
| AVGO | 8 | $275.34 | $276.15 | $2,209.20 | 65 |
| AXP | 7 | $325.34 | $320.40 | $2,242.80 | 70 |
| BA | 10 | $212.67 | $229.72 | $2,297.19 | 70 |
| BAC | 47 | $48.71 | $46.90 | $2,204.30 | 70 |
| C | 31 | $86.64 | $87.14 | $2,701.49 | 85 |
| CAT | 6 | $397.74 | $404.32 | $2,425.92 | 65 |
| COST | 2 | $979.83 | $974.07 | $1,948.13 | 65 |
| CRM | 7 | $268.68 | $260.79 | $1,825.53 | 65 |
| CSCO | 32 | $68.45 | $67.62 | $2,163.83 | 70 |
| CVX | 16 | $146.79 | $151.59 | $2,425.52 | 75 |
| DIS | 18 | $122.80 | $120.29 | $2,165.22 | 70 |
| GOOGL | 13 | $179.57 | $181.69 | $2,361.97 | 75 |
| GS | 3 | $717.52 | $711.76 | $2,135.30 | 75 |
| HD | 6 | $372.64 | $368.12 | $2,208.72 | 65 |
| INTC | 82 | $22.33 | $23.14 | $1,897.64 | 60 |
| JNJ | 13 | $155.95 | $156.44 | $2,033.72 | 65 |
| JPM | 9 | $291.63 | $288.63 | $2,597.72 | 85 |
| KO | 29 | $71.03 | $69.55 | $2,016.81 | 65 |
| LLY | 3 | $781.32 | $799.25 | $2,397.75 | 75 |
| MA | 4 | $563.08 | $553.72 | $2,214.88 | 65 |
| META | 3 | $717.12 | $725.09 | $2,175.27 | 85 |
| MRK | 28 | $82.49 | $83.80 | $2,346.40 | 75 |
| MSFT | 5 | $498.84 | $502.27 | $2,511.35 | 70 |
| NFLX | 1 | $1,279.00 | $1,266.77 | $1,266.77 | 65 |
| NKE | 29 | $72.04 | $72.34 | $2,097.86 | 65 |
| NVDA | 14 | $156.62 | $165.10 | $2,311.47 | 70 |
| ORCL | 9 | $233.26 | $230.15 | $2,071.35 | 65 |
| PEP | 15 | $136.57 | $135.78 | $2,036.70 | 65 |
| PFE | 86 | $25.21 | $25.49 | $2,192.54 | 70 |
| PG | 13 | $160.78 | $153.89 | $2,000.57 | 65 |
| PYPL | 32 | $72.32 | $73.65 | $2,356.95 | 75 |
| QCOM | 14 | $153.83 | $154.25 | $2,159.50 | 70 |
| T | 75 | $27.10 | $27.16 | $2,036.62 | 65 |
| TGT | 20 | $104.94 | $104.80 | $2,095.90 | 65 |
| TSLA | 6 | $288.62 | $316.24 | $1,897.42 | 65 |
| UNH | 7 | $298.51 | $300.10 | $2,100.70 | 65 |
| UNP | 10 | $236.29 | $233.54 | $2,335.45 | 75 |
| V | 6 | $355.85 | $350.48 | $2,102.85 | 70 |
| VZ | 49 | $43.12 | $41.55 | $2,035.71 | 65 |
| WFC | 28 | $82.26 | $83.22 | $2,330.02 | 75 |
| WMT | 21 | $97.38 | $95.41 | $2,003.61 | 65 |
| XOM | 21 | $110.01 | $113.38 | $2,380.98 | 75 |

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
| 2025-07-14 17:09:36 | SELL | NVDA | 2 | $165.10 | $14.84 | 70 |
| 2025-07-14 17:09:36 | SELL | INTC | 6 | $23.15 | $4.58 | 60 |
| 2025-07-14 17:09:36 | BUY | PYPL | 4 | $73.64 | N/A | 75 |
| 2025-07-14 17:09:36 | BUY | QCOM | 1 | $154.25 | N/A | 70 |
| 2025-07-14 17:09:36 | BUY | CSCO | 1 | $67.62 | N/A | 70 |
| 2025-07-14 16:56:14 | SELL | NKE | 3 | $72.29 | $0.69 | 65 |
| 2025-07-14 16:56:14 | SELL | CSCO | 1 | $67.55 | $-0.90 | 65 |
| 2025-07-14 16:56:14 | BUY | INTC | 7 | $23.15 | N/A | 65 |
| 2025-07-14 16:56:14 | BUY | MRK | 1 | $83.74 | N/A | 75 |
| 2025-07-14 16:43:44 | SELL | INTC | 7 | $23.15 | $5.33 | 60 |
| 2025-07-14 16:43:44 | SELL | PYPL | 1 | $73.69 | $1.51 | 65 |
| 2025-07-14 16:43:44 | SELL | PFE | 6 | $25.49 | $1.56 | 70 |
| 2025-07-14 16:43:44 | SELL | MRK | 1 | $83.53 | $1.04 | 70 |
| 2025-07-14 16:43:44 | BUY | WFC | 1 | $83.14 | N/A | 75 |
| 2025-07-14 16:43:44 | BUY | UNP | 1 | $233.19 | N/A | 75 |
| 2025-07-14 16:43:44 | BUY | CSCO | 1 | $67.48 | N/A | 70 |
| 2025-07-14 16:27:18 | SELL | WFC | 1 | $83.16 | $0.90 | 70 |
| 2025-07-14 16:27:18 | SELL | BA | 1 | $229.86 | $15.63 | 70 |
| 2025-07-14 16:27:18 | SELL | UNP | 1 | $232.96 | $-3.31 | 65 |
| 2025-07-14 16:27:18 | BUY | INTC | 1 | $23.12 | N/A | 65 |
| 2025-07-14 16:27:18 | BUY | PYPL | 1 | $73.61 | N/A | 70 |
| 2025-07-14 16:27:18 | BUY | MRK | 2 | $83.43 | N/A | 75 |
| 2025-07-14 16:27:18 | BUY | NKE | 3 | $72.23 | N/A | 75 |
| 2025-07-14 16:27:18 | BUY | PFE | 6 | $25.49 | N/A | 75 |
| 2025-07-14 16:09:59 | SELL | PYPL | 2 | $73.56 | $2.66 | 65 |

<!--TRADE_LOG_END--> 
