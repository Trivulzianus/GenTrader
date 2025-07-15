# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 14:52:40**

| Metric | Value |
|---|---|
| **Total Value** | **$100,672.27** |
| Cash | $1,467.23 |
| Holdings Value | $99,205.04 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.41 | $2,094.10 | 65 |
| ADBE | 6 | $375.23 | $364.32 | $2,185.92 | 65 |
| AMD | 16 | $145.70 | $156.11 | $2,497.76 | 75 |
| AMZN | 10 | $221.60 | $226.21 | $2,262.10 | 70 |
| AVGO | 8 | $275.34 | $281.02 | $2,248.16 | 70 |
| AXP | 7 | $325.34 | $312.99 | $2,190.89 | 65 |
| BA | 9 | $210.77 | $231.00 | $2,078.95 | 70 |
| BAC | 44 | $48.83 | $46.59 | $2,050.18 | 65 |
| C | 27 | $86.52 | $89.21 | $2,408.67 | 75 |
| CAT | 6 | $397.74 | $407.72 | $2,446.32 | 70 |
| COST | 2 | $979.83 | $969.23 | $1,938.45 | 65 |
| CRM | 8 | $267.44 | $258.72 | $2,069.76 | 65 |
| CSCO | 31 | $68.46 | $67.41 | $2,089.71 | 65 |
| CVX | 18 | $147.28 | $151.06 | $2,719.08 | 85 |
| DIS | 17 | $122.96 | $119.18 | $2,026.06 | 65 |
| GOOGL | 14 | $179.74 | $183.11 | $2,563.54 | 85 |
| GS | 3 | $717.52 | $707.00 | $2,121.00 | 85 |
| HD | 6 | $372.64 | $365.26 | $2,191.56 | 65 |
| INTC | 83 | $22.33 | $23.39 | $1,941.37 | 60 |
| JNJ | 13 | $155.95 | $155.21 | $2,017.73 | 65 |
| JPM | 9 | $291.63 | $286.69 | $2,580.21 | 85 |
| KO | 30 | $70.97 | $69.33 | $2,080.05 | 65 |
| LLY | 3 | $781.32 | $775.95 | $2,327.85 | 65 |
| MA | 4 | $563.08 | $550.04 | $2,200.15 | 65 |
| META | 3 | $717.12 | $715.26 | $2,145.78 | 65 |
| MRK | 25 | $82.54 | $81.80 | $2,045.01 | 65 |
| MSFT | 5 | $498.84 | $504.77 | $2,523.85 | 75 |
| NFLX | 1 | $1,279.00 | $1,261.89 | $1,261.89 | 65 |
| NKE | 31 | $72.05 | $72.20 | $2,238.20 | 70 |
| NVDA | 14 | $171.75 | $171.17 | $2,396.38 | 70 |
| ORCL | 9 | $233.27 | $231.97 | $2,087.73 | 70 |
| PEP | 15 | $136.57 | $134.18 | $2,012.70 | 65 |
| PFE | 83 | $25.22 | $24.89 | $2,066.28 | 65 |
| PG | 13 | $152.12 | $152.27 | $1,979.51 | 65 |
| PYPL | 29 | $72.19 | $73.24 | $2,123.96 | 65 |
| QCOM | 14 | $153.83 | $154.60 | $2,164.40 | 65 |
| T | 77 | $27.10 | $26.92 | $2,072.84 | 65 |
| TGT | 20 | $104.94 | $103.64 | $2,072.74 | 65 |
| TSLA | 6 | $318.51 | $313.96 | $1,883.76 | 65 |
| UNH | 7 | $298.51 | $293.64 | $2,055.51 | 65 |
| UNP | 9 | $236.56 | $232.24 | $2,090.16 | 65 |
| V | 6 | $355.85 | $348.25 | $2,089.53 | 65 |
| VZ | 50 | $43.08 | $41.27 | $2,063.75 | 65 |
| WFC | 27 | $82.92 | $78.89 | $2,129.89 | 65 |
| WMT | 21 | $97.38 | $95.11 | $1,997.31 | 65 |
| XOM | 21 | $109.99 | $113.06 | $2,374.26 | 75 |

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
| 2025-07-15 14:40:39 | SELL | NVDA | 13 | $171.71 | $210.41 | 70 |
| 2025-07-15 14:26:51 | SELL | NVDA | 2 | $171.32 | $27.40 | 70 |
| 2025-07-15 14:26:51 | SELL | PFE | 3 | $25.00 | $-0.62 | 65 |
| 2025-07-15 14:26:51 | SELL | MRK | 4 | $82.50 | $-0.13 | 65 |

<!--TRADE_LOG_END--> 
