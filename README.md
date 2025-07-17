# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 15:52:46**

| Metric | Value |
|---|---|
| **Total Value** | **$101,344.96** |
| Cash | $631.71 |
| Holdings Value | $100,713.25 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.22 | $2,102.15 | 65 |
| ADBE | 6 | $375.23 | $364.65 | $2,187.90 | 65 |
| AMD | 14 | $160.03 | $159.83 | $2,237.62 | 70 |
| AMZN | 10 | $221.65 | $223.39 | $2,233.90 | 75 |
| AVGO | 8 | $275.34 | $286.89 | $2,295.09 | 65 |
| AXP | 7 | $309.18 | $314.02 | $2,198.14 | 75 |
| BA | 9 | $210.81 | $229.51 | $2,065.59 | 70 |
| BAC | 48 | $46.27 | $46.48 | $2,231.28 | 70 |
| C | 30 | $86.85 | $92.53 | $2,776.05 | 85 |
| CAT | 6 | $397.74 | $416.31 | $2,497.89 | 75 |
| COST | 2 | $979.83 | $952.46 | $1,904.92 | 65 |
| CRM | 8 | $267.44 | $259.25 | $2,074.00 | 65 |
| CSCO | 32 | $68.58 | $68.33 | $2,186.56 | 70 |
| CVX | 16 | $146.82 | $150.32 | $2,405.12 | 75 |
| DIS | 19 | $122.69 | $121.36 | $2,305.74 | 70 |
| GOOGL | 13 | $179.34 | $182.48 | $2,372.24 | 75 |
| GS | 3 | $717.52 | $712.71 | $2,138.12 | 85 |
| HD | 6 | $354.18 | $356.50 | $2,139.03 | 65 |
| INTC | 90 | $22.39 | $23.02 | $2,071.35 | 65 |
| JNJ | 13 | $155.43 | $163.05 | $2,119.65 | 70 |
| JPM | 9 | $291.90 | $288.24 | $2,594.16 | 75 |
| KO | 30 | $70.97 | $69.77 | $2,092.95 | 65 |
| LLY | 3 | $781.32 | $784.66 | $2,353.99 | 70 |
| MA | 4 | $563.08 | $553.97 | $2,215.86 | 65 |
| META | 3 | $717.12 | $702.26 | $2,106.78 | 70 |
| MRK | 29 | $82.56 | $82.02 | $2,378.58 | 75 |
| MSFT | 5 | $498.84 | $512.60 | $2,563.00 | 70 |
| NFLX | 1 | $1,279.00 | $1,257.83 | $1,257.83 | 65 |
| NKE | 29 | $71.89 | $72.81 | $2,111.35 | 65 |
| NVDA | 13 | $171.63 | $173.40 | $2,254.20 | 70 |
| ORCL | 9 | $232.91 | $249.21 | $2,242.89 | 65 |
| PEP | 16 | $136.49 | $144.73 | $2,315.68 | 75 |
| PFE | 84 | $25.28 | $24.69 | $2,074.08 | 65 |
| PG | 14 | $152.18 | $154.65 | $2,165.10 | 65 |
| PYPL | 28 | $72.12 | $73.33 | $2,053.24 | 65 |
| QCOM | 14 | $153.83 | $153.05 | $2,142.70 | 65 |
| T | 77 | $27.10 | $26.88 | $2,069.93 | 65 |
| TGT | 20 | $104.83 | $103.22 | $2,064.40 | 65 |
| TSLA | 6 | $318.51 | $321.19 | $1,927.13 | 60 |
| UNH | 7 | $298.51 | $289.58 | $2,027.06 | 65 |
| UNP | 10 | $236.33 | $227.84 | $2,278.40 | 65 |
| V | 6 | $355.85 | $349.78 | $2,098.69 | 65 |
| VZ | 51 | $43.04 | $40.97 | $2,089.26 | 65 |
| WFC | 28 | $78.79 | $80.23 | $2,246.44 | 70 |
| WMT | 22 | $97.29 | $95.28 | $2,096.05 | 65 |
| XOM | 21 | $109.98 | $111.96 | $2,351.16 | 70 |

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
| 2025-07-17 15:52:40 | SELL | NVDA | 2 | $173.43 | $3.11 | 70 |
| 2025-07-17 15:52:40 | SELL | NKE | 3 | $72.80 | $2.46 | 65 |
| 2025-07-17 15:52:40 | SELL | WFC | 1 | $80.25 | $1.41 | 70 |
| 2025-07-17 15:52:40 | BUY | BAC | 3 | $46.51 | N/A | 70 |
| 2025-07-17 15:52:40 | BUY | INTC | 6 | $23.01 | N/A | 65 |
| 2025-07-17 15:52:40 | BUY | CSCO | 1 | $68.32 | N/A | 70 |
| 2025-07-17 15:41:13 | SELL | AMD | 1 | $159.85 | $-0.16 | 70 |
| 2025-07-17 15:41:13 | SELL | PFE | 1 | $24.69 | $-0.58 | 65 |
| 2025-07-17 15:41:13 | SELL | CSCO | 4 | $67.37 | $-4.30 | 65 |
| 2025-07-17 15:41:13 | SELL | T | 1 | $26.88 | $-0.22 | 65 |
| 2025-07-17 15:41:13 | SELL | TGT | 1 | $103.42 | $-1.35 | 65 |
| 2025-07-17 15:41:13 | BUY | NVDA | 2 | $173.33 | N/A | 85 |
| 2025-07-17 15:41:13 | BUY | XOM | 2 | $111.93 | N/A | 75 |
| 2025-07-17 15:41:13 | BUY | NKE | 3 | $73.00 | N/A | 75 |
| 2025-07-17 15:41:13 | BUY | WFC | 3 | $80.32 | N/A | 75 |
| 2025-07-17 15:26:56 | SELL | NVDA | 2 | $173.08 | $2.49 | 70 |
| 2025-07-17 15:26:56 | SELL | XOM | 2 | $111.78 | $3.63 | 65 |
| 2025-07-17 15:26:56 | SELL | NKE | 1 | $72.99 | $1.08 | 65 |
| 2025-07-17 15:26:56 | SELL | WFC | 2 | $80.14 | $2.73 | 65 |
| 2025-07-17 15:26:56 | BUY | AMD | 1 | $159.26 | N/A | 75 |
| 2025-07-17 15:26:56 | BUY | CSCO | 3 | $68.11 | N/A | 75 |
| 2025-07-17 15:09:30 | SELL | DIS | 1 | $121.64 | $-1.00 | 70 |
| 2025-07-17 15:09:30 | BUY | NVDA | 2 | $173.26 | N/A | 85 |
| 2025-07-17 15:09:30 | BUY | MRK | 1 | $82.01 | N/A | 75 |
| 2025-07-17 15:09:30 | BUY | CSCO | 1 | $68.25 | N/A | 70 |

<!--TRADE_LOG_END--> 
