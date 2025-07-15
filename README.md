# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 15:08:25**

| Metric | Value |
|---|---|
| **Total Value** | **$100,691.36** |
| Cash | $1,113.97 |
| Holdings Value | $99,577.40 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.70 | $2,097.00 | 65 |
| ADBE | 6 | $375.23 | $364.58 | $2,187.48 | 65 |
| AMD | 17 | $146.29 | $155.77 | $2,648.13 | 85 |
| AMZN | 10 | $221.60 | $225.69 | $2,256.90 | 75 |
| AVGO | 8 | $275.34 | $280.67 | $2,245.36 | 65 |
| AXP | 7 | $325.34 | $314.28 | $2,199.96 | 65 |
| BA | 9 | $210.77 | $231.17 | $2,080.53 | 70 |
| BAC | 44 | $48.83 | $46.60 | $2,050.62 | 65 |
| C | 30 | $86.78 | $89.22 | $2,676.60 | 85 |
| CAT | 6 | $397.74 | $406.98 | $2,441.88 | 70 |
| COST | 2 | $979.83 | $969.55 | $1,939.11 | 70 |
| CRM | 8 | $267.44 | $258.91 | $2,071.28 | 65 |
| CSCO | 31 | $68.46 | $67.50 | $2,092.65 | 65 |
| CVX | 16 | $146.80 | $151.23 | $2,419.68 | 75 |
| DIS | 17 | $122.96 | $119.12 | $2,025.04 | 65 |
| GOOGL | 14 | $179.74 | $183.28 | $2,565.92 | 75 |
| GS | 3 | $717.52 | $706.66 | $2,119.98 | 75 |
| HD | 6 | $372.64 | $364.14 | $2,184.84 | 65 |
| INTC | 83 | $22.33 | $23.41 | $1,942.62 | 60 |
| JNJ | 13 | $155.95 | $155.40 | $2,020.20 | 65 |
| JPM | 9 | $291.63 | $287.00 | $2,583.00 | 85 |
| KO | 30 | $70.97 | $69.28 | $2,078.40 | 65 |
| LLY | 3 | $781.32 | $775.31 | $2,325.93 | 65 |
| MA | 4 | $563.08 | $550.36 | $2,201.44 | 65 |
| META | 3 | $717.12 | $714.53 | $2,143.59 | 65 |
| MRK | 25 | $82.54 | $81.89 | $2,047.25 | 65 |
| MSFT | 5 | $498.84 | $505.18 | $2,525.90 | 85 |
| NFLX | 1 | $1,279.00 | $1,261.33 | $1,261.33 | 65 |
| NKE | 31 | $72.05 | $72.27 | $2,240.48 | 70 |
| NVDA | 14 | $171.75 | $171.13 | $2,395.89 | 70 |
| ORCL | 9 | $233.27 | $231.41 | $2,082.64 | 65 |
| PEP | 15 | $136.57 | $134.07 | $2,011.05 | 65 |
| PFE | 83 | $25.22 | $24.84 | $2,062.13 | 65 |
| PG | 13 | $152.12 | $152.62 | $1,984.06 | 65 |
| PYPL | 29 | $72.19 | $73.38 | $2,128.02 | 65 |
| QCOM | 14 | $153.83 | $155.03 | $2,170.42 | 65 |
| T | 77 | $27.10 | $26.99 | $2,078.23 | 65 |
| TGT | 20 | $104.94 | $103.53 | $2,070.60 | 65 |
| TSLA | 6 | $318.51 | $313.64 | $1,881.84 | 60 |
| UNH | 7 | $298.51 | $292.79 | $2,049.53 | 65 |
| UNP | 10 | $236.16 | $232.66 | $2,326.60 | 75 |
| V | 6 | $355.85 | $348.01 | $2,088.06 | 65 |
| VZ | 50 | $43.08 | $41.35 | $2,067.75 | 65 |
| WFC | 27 | $82.92 | $79.05 | $2,134.22 | 65 |
| WMT | 21 | $97.38 | $95.15 | $1,998.15 | 65 |
| XOM | 21 | $109.99 | $113.10 | $2,375.10 | 75 |

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
| 2025-07-15 15:08:18 | SELL | CVX | 2 | $151.18 | $7.79 | 75 |
| 2025-07-15 15:08:18 | BUY | AMD | 1 | $155.67 | N/A | 85 |
| 2025-07-15 15:08:18 | BUY | C | 3 | $89.11 | N/A | 85 |
| 2025-07-15 15:08:18 | BUY | UNP | 1 | $232.60 | N/A | 75 |
| 2025-07-15 14:52:34 | SELL | NVDA | 1 | $171.28 | $-0.44 | 70 |
| 2025-07-15 14:52:34 | SELL | INTC | 5 | $23.39 | $5.02 | 60 |
| 2025-07-15 14:52:34 | SELL | WFC | 1 | $78.90 | $-3.87 | 65 |
| 2025-07-15 14:52:34 | SELL | C | 3 | $89.18 | $7.17 | 75 |
| 2025-07-15 14:52:34 | BUY | AMD | 1 | $146.24 | N/A | 75 |
| 2025-07-15 14:52:34 | BUY | CRM | 1 | $258.71 | N/A | 65 |
| 2025-07-15 14:52:34 | BUY | KO | 1 | $69.33 | N/A | 65 |
| 2025-07-15 14:52:34 | BUY | NKE | 1 | $72.17 | N/A | 70 |
| 2025-07-15 14:52:34 | BUY | CVX | 2 | $151.16 | N/A | 85 |
| 2025-07-15 14:52:34 | BUY | T | 1 | $26.91 | N/A | 65 |
| 2025-07-15 14:41:32 | SELL | AMZN | 1 | $226.26 | $4.24 | 70 |
| 2025-07-15 14:41:32 | SELL | PYPL | 3 | $73.44 | $3.40 | 65 |
| 2025-07-15 14:41:32 | SELL | BA | 2 | $230.57 | $32.40 | 65 |
| 2025-07-15 14:41:32 | SELL | CVX | 1 | $151.29 | $4.23 | 75 |
| 2025-07-15 14:41:32 | BUY | NVDA | 15 | $171.71 | N/A | 85 |
| 2025-07-15 14:41:32 | BUY | INTC | 7 | $23.40 | N/A | 65 |
| 2025-07-15 14:41:32 | BUY | XOM | 1 | $113.19 | N/A | 75 |
| 2025-07-15 14:41:32 | BUY | WFC | 2 | $79.06 | N/A | 70 |
| 2025-07-15 14:41:32 | BUY | PG | 13 | $152.12 | N/A | 65 |
| 2025-07-15 14:41:32 | BUY | VZ | 1 | $41.19 | N/A | 65 |
| 2025-07-15 14:40:44 | SELL | PG | 14 | $152.10 | $-114.93 | 65 |

<!--TRADE_LOG_END--> 
