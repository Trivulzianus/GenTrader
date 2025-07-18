# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 15:09:04**

| Metric | Value |
|---|---|
| **Total Value** | **$101,165.21** |
| Cash | $556.80 |
| Holdings Value | $100,608.40 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.94 | $2,109.35 | 65 |
| ADBE | 6 | $375.23 | $365.68 | $2,194.08 | 65 |
| AMD | 14 | $159.84 | $156.85 | $2,195.90 | 65 |
| AMZN | 11 | $221.89 | $224.01 | $2,464.11 | 75 |
| AVGO | 8 | $275.34 | $281.64 | $2,253.12 | 70 |
| AXP | 7 | $309.18 | $305.71 | $2,139.97 | 65 |
| BA | 10 | $232.01 | $228.95 | $2,289.50 | 65 |
| BAC | 48 | $46.30 | $47.14 | $2,262.49 | 70 |
| C | 29 | $86.64 | $93.18 | $2,702.22 | 85 |
| CAT | 6 | $397.74 | $414.34 | $2,486.03 | 70 |
| COST | 2 | $979.83 | $958.60 | $1,917.20 | 65 |
| CRM | 8 | $267.44 | $260.07 | $2,080.56 | 65 |
| CSCO | 33 | $68.56 | $68.36 | $2,256.04 | 70 |
| CVX | 17 | $147.14 | $150.65 | $2,560.97 | 75 |
| DIS | 18 | $122.74 | $121.08 | $2,179.44 | 70 |
| GOOGL | 13 | $179.34 | $184.76 | $2,401.88 | 70 |
| GS | 3 | $717.52 | $705.43 | $2,116.29 | 75 |
| HD | 6 | $354.18 | $359.62 | $2,157.74 | 65 |
| INTC | 90 | $22.41 | $23.39 | $2,105.11 | 65 |
| JNJ | 14 | $155.97 | $164.52 | $2,303.28 | 70 |
| JPM | 8 | $292.14 | $290.44 | $2,323.52 | 70 |
| KO | 34 | $70.90 | $70.39 | $2,393.09 | 75 |
| LLY | 3 | $781.32 | $773.75 | $2,321.24 | 65 |
| MA | 4 | $563.08 | $552.96 | $2,211.84 | 65 |
| META | 3 | $717.12 | $698.29 | $2,094.87 | 70 |
| MRK | 26 | $82.73 | $81.15 | $2,109.87 | 65 |
| MSFT | 5 | $498.84 | $510.07 | $2,550.35 | 75 |
| NFLX | 1 | $1,208.39 | $1,204.82 | $1,204.82 | 65 |
| NKE | 33 | $72.04 | $72.40 | $2,389.20 | 75 |
| NVDA | 13 | $171.84 | $171.32 | $2,227.22 | 65 |
| ORCL | 9 | $232.91 | $245.41 | $2,208.64 | 75 |
| PEP | 15 | $135.89 | $144.74 | $2,171.10 | 65 |
| PFE | 85 | $25.27 | $24.59 | $2,090.57 | 65 |
| PG | 13 | $151.91 | $155.36 | $2,019.68 | 65 |
| PYPL | 29 | $72.18 | $73.88 | $2,142.52 | 65 |
| QCOM | 14 | $153.83 | $155.12 | $2,171.72 | 65 |
| T | 78 | $27.10 | $27.00 | $2,105.61 | 65 |
| TGT | 20 | $104.82 | $103.37 | $2,067.40 | 65 |
| TSLA | 6 | $318.51 | $327.84 | $1,967.04 | 65 |
| UNH | 7 | $298.51 | $285.80 | $2,000.60 | 60 |
| UNP | 9 | $225.02 | $224.34 | $2,019.02 | 65 |
| V | 6 | $355.85 | $348.60 | $2,091.60 | 65 |
| VZ | 51 | $40.87 | $40.98 | $2,090.24 | 65 |
| WFC | 27 | $78.72 | $80.00 | $2,159.87 | 65 |
| WMT | 22 | $97.29 | $95.31 | $2,096.71 | 65 |
| XOM | 20 | $109.90 | $110.24 | $2,204.80 | 65 |

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
| 2025-07-18 14:26:10 | SELL | PFE | 6 | $24.58 | $-4.18 | 60 |
| 2025-07-18 14:26:10 | BUY | NVDA | 1 | $173.00 | N/A | 85 |
| 2025-07-18 14:26:10 | BUY | KO | 1 | $70.65 | N/A | 70 |
| 2025-07-18 14:09:21 | SELL | NVDA | 1 | $173.35 | $1.44 | 70 |

<!--TRADE_LOG_END--> 
