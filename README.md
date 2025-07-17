# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 17:09:30**

| Metric | Value |
|---|---|
| **Total Value** | **$101,218.67** |
| Cash | $586.81 |
| Holdings Value | $100,631.86 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.00 | $2,110.00 | 65 |
| ADBE | 6 | $375.23 | $366.18 | $2,197.08 | 65 |
| AMD | 14 | $160.03 | $159.65 | $2,235.10 | 70 |
| AMZN | 10 | $221.65 | $223.77 | $2,237.70 | 75 |
| AVGO | 8 | $275.34 | $287.30 | $2,298.40 | 70 |
| AXP | 7 | $309.18 | $313.83 | $2,196.81 | 70 |
| BA | 9 | $210.81 | $228.65 | $2,057.85 | 70 |
| BAC | 45 | $46.25 | $46.67 | $2,100.38 | 65 |
| C | 30 | $86.85 | $92.52 | $2,775.60 | 85 |
| CAT | 6 | $397.74 | $416.45 | $2,498.70 | 75 |
| COST | 2 | $979.83 | $952.62 | $1,905.24 | 65 |
| CRM | 8 | $267.44 | $258.91 | $2,071.28 | 65 |
| CSCO | 35 | $68.54 | $68.19 | $2,386.65 | 75 |
| CVX | 16 | $146.82 | $150.18 | $2,402.80 | 75 |
| DIS | 22 | $122.51 | $121.62 | $2,675.75 | 85 |
| GOOGL | 13 | $179.34 | $182.43 | $2,371.59 | 70 |
| GS | 3 | $717.52 | $709.21 | $2,127.63 | 80 |
| HD | 6 | $354.18 | $356.83 | $2,141.01 | 65 |
| INTC | 84 | $22.34 | $22.96 | $1,929.06 | 60 |
| JNJ | 13 | $155.43 | $163.08 | $2,120.04 | 70 |
| JPM | 9 | $291.90 | $287.34 | $2,586.06 | 75 |
| KO | 30 | $70.97 | $69.67 | $2,090.05 | 65 |
| LLY | 3 | $781.32 | $765.49 | $2,296.47 | 60 |
| MA | 4 | $563.08 | $553.38 | $2,213.52 | 70 |
| META | 3 | $717.12 | $702.12 | $2,106.36 | 75 |
| MRK | 29 | $82.56 | $81.44 | $2,361.62 | 75 |
| MSFT | 5 | $498.84 | $512.56 | $2,562.80 | 70 |
| NFLX | 1 | $1,279.00 | $1,260.69 | $1,260.69 | 65 |
| NKE | 30 | $71.91 | $72.94 | $2,188.20 | 70 |
| NVDA | 13 | $171.56 | $173.68 | $2,257.78 | 70 |
| ORCL | 9 | $232.91 | $247.43 | $2,226.87 | 70 |
| PEP | 16 | $136.49 | $144.42 | $2,310.72 | 70 |
| PFE | 84 | $25.28 | $24.54 | $2,060.94 | 65 |
| PG | 14 | $152.18 | $154.55 | $2,163.70 | 65 |
| PYPL | 28 | $72.12 | $73.59 | $2,060.52 | 65 |
| QCOM | 14 | $153.83 | $153.06 | $2,142.84 | 70 |
| T | 78 | $27.09 | $26.85 | $2,094.31 | 65 |
| TGT | 20 | $104.83 | $103.32 | $2,066.40 | 65 |
| TSLA | 6 | $318.51 | $320.64 | $1,923.87 | 65 |
| UNH | 7 | $298.51 | $288.94 | $2,022.55 | 65 |
| UNP | 10 | $236.33 | $227.73 | $2,277.30 | 65 |
| V | 6 | $355.85 | $349.95 | $2,099.70 | 65 |
| VZ | 50 | $40.87 | $40.86 | $2,043.00 | 65 |
| WFC | 27 | $78.74 | $80.09 | $2,162.43 | 70 |
| WMT | 22 | $97.29 | $95.14 | $2,092.97 | 65 |
| XOM | 19 | $109.79 | $111.66 | $2,121.54 | 65 |

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
| 2025-07-17 17:09:24 | SELL | NVDA | 2 | $173.65 | $3.62 | 70 |
| 2025-07-17 17:09:24 | SELL | XOM | 2 | $111.69 | $3.43 | 65 |
| 2025-07-17 17:09:24 | SELL | T | 5 | $26.86 | $-1.09 | 65 |
| 2025-07-17 17:09:24 | BUY | WFC | 1 | $80.10 | N/A | 70 |
| 2025-07-17 17:09:24 | BUY | CSCO | 4 | $68.19 | N/A | 75 |
| 2025-07-17 16:56:39 | SELL | INTC | 6 | $22.99 | $3.60 | 60 |
| 2025-07-17 16:56:39 | SELL | CSCO | 1 | $68.29 | $-0.29 | 65 |
| 2025-07-17 16:56:39 | BUY | NVDA | 2 | $173.66 | N/A | 85 |
| 2025-07-17 16:56:39 | BUY | NKE | 1 | $73.01 | N/A | 70 |
| 2025-07-17 16:56:39 | BUY | VZ | 50 | $40.87 | N/A | 65 |
| 2025-07-17 16:56:39 | BUY | T | 6 | $26.84 | N/A | 70 |
| 2025-07-17 16:56:16 | SELL | VZ | 51 | $40.86 | $-111.01 | 65 |
| 2025-07-17 16:44:33 | SELL | NKE | 2 | $73.14 | $2.38 | 65 |
| 2025-07-17 16:44:33 | SELL | WFC | 2 | $80.17 | $2.74 | 65 |
| 2025-07-17 16:44:33 | BUY | XOM | 2 | $111.66 | N/A | 75 |
| 2025-07-17 16:44:33 | BUY | INTC | 6 | $22.92 | N/A | 65 |
| 2025-07-17 16:27:10 | SELL | NVDA | 2 | $174.01 | $4.26 | 70 |
| 2025-07-17 16:27:10 | SELL | BAC | 3 | $46.61 | $1.01 | 65 |
| 2025-07-17 16:27:10 | SELL | INTC | 6 | $22.94 | $3.32 | 60 |
| 2025-07-17 16:27:10 | SELL | XOM | 2 | $111.70 | $3.44 | 65 |
| 2025-07-17 16:27:10 | SELL | NKE | 1 | $72.97 | $0.98 | 70 |
| 2025-07-17 16:27:10 | SELL | WFC | 1 | $80.18 | $1.33 | 70 |
| 2025-07-17 16:27:10 | BUY | DIS | 3 | $121.40 | N/A | 85 |
| 2025-07-17 16:27:10 | BUY | CSCO | 1 | $68.29 | N/A | 70 |
| 2025-07-17 16:10:07 | SELL | CSCO | 1 | $68.43 | $-0.15 | 65 |

<!--TRADE_LOG_END--> 
