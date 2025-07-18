# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 15:26:26**

| Metric | Value |
|---|---|
| **Total Value** | **$101,113.09** |
| Cash | $1,061.64 |
| Holdings Value | $100,051.44 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.69 | $2,106.90 | 65 |
| ADBE | 6 | $375.23 | $364.95 | $2,189.70 | 65 |
| AMD | 14 | $159.84 | $157.07 | $2,198.92 | 70 |
| AMZN | 11 | $221.89 | $224.43 | $2,468.73 | 75 |
| AVGO | 8 | $275.34 | $282.05 | $2,256.36 | 70 |
| AXP | 7 | $309.18 | $305.75 | $2,140.25 | 65 |
| BA | 10 | $232.01 | $229.06 | $2,290.60 | 65 |
| BAC | 45 | $46.25 | $47.08 | $2,118.60 | 65 |
| C | 29 | $86.64 | $93.26 | $2,704.54 | 85 |
| CAT | 6 | $397.74 | $414.31 | $2,485.86 | 70 |
| COST | 2 | $979.83 | $957.68 | $1,915.36 | 65 |
| CRM | 8 | $267.44 | $259.80 | $2,078.41 | 65 |
| CSCO | 33 | $68.56 | $68.28 | $2,253.08 | 70 |
| CVX | 17 | $147.14 | $150.35 | $2,555.95 | 75 |
| DIS | 18 | $122.74 | $121.12 | $2,180.16 | 70 |
| GOOGL | 13 | $179.34 | $184.50 | $2,398.43 | 70 |
| GS | 3 | $717.52 | $706.83 | $2,120.49 | 70 |
| HD | 6 | $354.18 | $358.33 | $2,149.98 | 65 |
| INTC | 90 | $22.41 | $23.36 | $2,101.95 | 65 |
| JNJ | 14 | $155.97 | $164.79 | $2,307.06 | 75 |
| JPM | 8 | $292.14 | $291.02 | $2,328.16 | 70 |
| KO | 30 | $70.97 | $70.36 | $2,110.95 | 65 |
| LLY | 3 | $781.32 | $774.27 | $2,322.81 | 65 |
| MA | 4 | $563.08 | $552.02 | $2,208.09 | 65 |
| META | 3 | $717.12 | $699.05 | $2,097.15 | 70 |
| MRK | 26 | $82.73 | $81.03 | $2,106.78 | 65 |
| MSFT | 5 | $498.84 | $510.45 | $2,552.25 | 85 |
| NFLX | 1 | $1,208.39 | $1,212.26 | $1,212.26 | 65 |
| NKE | 30 | $72.01 | $72.33 | $2,169.90 | 65 |
| NVDA | 13 | $171.84 | $172.00 | $2,235.94 | 70 |
| ORCL | 9 | $232.91 | $246.21 | $2,215.89 | 70 |
| PEP | 15 | $135.89 | $144.48 | $2,167.26 | 65 |
| PFE | 85 | $25.27 | $24.53 | $2,085.21 | 65 |
| PG | 13 | $151.91 | $155.44 | $2,020.72 | 65 |
| PYPL | 29 | $72.18 | $73.81 | $2,140.49 | 65 |
| QCOM | 14 | $153.83 | $155.09 | $2,171.26 | 65 |
| T | 83 | $27.09 | $26.98 | $2,238.93 | 70 |
| TGT | 20 | $104.82 | $102.79 | $2,055.80 | 65 |
| TSLA | 6 | $318.51 | $327.51 | $1,965.06 | 65 |
| UNH | 7 | $298.51 | $284.74 | $1,993.18 | 65 |
| UNP | 9 | $225.02 | $223.53 | $2,011.78 | 65 |
| V | 6 | $355.85 | $348.43 | $2,090.58 | 65 |
| VZ | 51 | $40.87 | $40.91 | $2,086.16 | 65 |
| WFC | 27 | $78.72 | $80.03 | $2,160.72 | 65 |
| WMT | 22 | $97.29 | $95.30 | $2,096.60 | 65 |
| XOM | 20 | $109.90 | $109.31 | $2,186.20 | 70 |

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
| 2025-07-18 15:26:20 | SELL | BAC | 3 | $47.08 | $2.33 | 65 |
| 2025-07-18 15:26:20 | SELL | NKE | 3 | $72.32 | $0.86 | 65 |
| 2025-07-18 15:26:20 | SELL | KO | 4 | $70.38 | $-2.08 | 65 |
| 2025-07-18 15:26:20 | BUY | T | 5 | $26.98 | N/A | 70 |
| 2025-07-18 15:08:54 | SELL | WFC | 1 | $80.03 | $1.26 | 65 |
| 2025-07-18 15:08:54 | SELL | CVX | 1 | $150.64 | $3.31 | 75 |
| 2025-07-18 15:08:54 | BUY | BAC | 1 | $47.13 | N/A | 70 |
| 2025-07-18 15:08:54 | BUY | INTC | 1 | $23.39 | N/A | 65 |
| 2025-07-18 15:08:54 | BUY | KO | 4 | $70.37 | N/A | 75 |
| 2025-07-18 15:08:54 | BUY | NKE | 4 | $72.42 | N/A | 75 |
| 2025-07-18 14:53:25 | SELL | NVDA | 1 | $172.34 | $0.46 | 70 |
| 2025-07-18 14:53:25 | SELL | CSCO | 2 | $68.38 | $-0.35 | 70 |
| 2025-07-18 14:53:25 | BUY | BAC | 2 | $47.15 | N/A | 70 |
| 2025-07-18 14:53:25 | BUY | INTC | 5 | $23.30 | N/A | 65 |
| 2025-07-18 14:53:25 | BUY | WFC | 1 | $79.94 | N/A | 70 |
| 2025-07-18 14:40:53 | SELL | NVDA | 1 | $172.07 | $0.18 | 70 |
| 2025-07-18 14:40:53 | SELL | BAC | 3 | $47.08 | $2.34 | 65 |
| 2025-07-18 14:40:53 | SELL | KO | 1 | $70.44 | $-0.51 | 65 |
| 2025-07-18 14:40:53 | SELL | MRK | 3 | $81.06 | $-4.49 | 65 |
| 2025-07-18 14:40:53 | BUY | AMD | 1 | $157.83 | N/A | 70 |
| 2025-07-18 14:40:53 | BUY | XOM | 1 | $111.66 | N/A | 70 |
| 2025-07-18 14:40:53 | BUY | PFE | 6 | $24.53 | N/A | 65 |
| 2025-07-18 14:40:53 | BUY | CSCO | 4 | $68.41 | N/A | 75 |
| 2025-07-18 14:40:53 | BUY | CVX | 2 | $151.30 | N/A | 85 |
| 2025-07-18 14:26:10 | SELL | NKE | 1 | $72.27 | $0.28 | 65 |

<!--TRADE_LOG_END--> 
