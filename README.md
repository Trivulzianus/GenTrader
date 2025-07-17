# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 15:27:03**

| Metric | Value |
|---|---|
| **Total Value** | **$101,262.54** |
| Cash | $778.31 |
| Holdings Value | $100,484.23 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.51 | $2,105.10 | 65 |
| ADBE | 6 | $375.23 | $364.55 | $2,187.30 | 65 |
| AMD | 15 | $160.01 | $159.29 | $2,389.39 | 75 |
| AMZN | 10 | $221.65 | $223.87 | $2,238.70 | 75 |
| AVGO | 8 | $275.34 | $287.37 | $2,298.96 | 65 |
| AXP | 7 | $309.18 | $313.48 | $2,194.38 | 70 |
| BA | 9 | $210.81 | $230.19 | $2,071.76 | 65 |
| BAC | 45 | $46.26 | $46.34 | $2,085.30 | 65 |
| C | 30 | $86.85 | $92.04 | $2,761.20 | 85 |
| CAT | 6 | $397.74 | $415.23 | $2,491.38 | 70 |
| COST | 2 | $979.83 | $950.04 | $1,900.09 | 65 |
| CRM | 8 | $267.44 | $258.69 | $2,069.56 | 65 |
| CSCO | 35 | $68.45 | $68.11 | $2,384.02 | 75 |
| CVX | 16 | $146.82 | $150.00 | $2,400.08 | 75 |
| DIS | 19 | $122.69 | $121.57 | $2,309.83 | 75 |
| GOOGL | 13 | $179.34 | $182.32 | $2,370.16 | 75 |
| GS | 3 | $717.52 | $710.21 | $2,130.63 | 85 |
| HD | 6 | $354.18 | $355.67 | $2,134.02 | 65 |
| INTC | 84 | $22.34 | $22.84 | $1,918.16 | 60 |
| JNJ | 13 | $155.43 | $162.74 | $2,115.62 | 70 |
| JPM | 9 | $291.90 | $287.44 | $2,586.96 | 75 |
| KO | 30 | $70.97 | $69.74 | $2,092.20 | 65 |
| LLY | 3 | $781.32 | $788.50 | $2,365.50 | 65 |
| MA | 4 | $563.08 | $552.75 | $2,211.00 | 65 |
| META | 3 | $717.12 | $703.22 | $2,109.66 | 75 |
| MRK | 29 | $82.56 | $82.28 | $2,385.98 | 75 |
| MSFT | 5 | $498.84 | $511.99 | $2,559.95 | 85 |
| NFLX | 1 | $1,279.00 | $1,257.93 | $1,257.93 | 65 |
| NKE | 29 | $71.87 | $72.99 | $2,116.71 | 65 |
| NVDA | 13 | $171.65 | $173.14 | $2,250.79 | 70 |
| ORCL | 9 | $232.91 | $250.21 | $2,251.89 | 70 |
| PEP | 16 | $136.49 | $144.44 | $2,311.04 | 75 |
| PFE | 85 | $25.27 | $24.72 | $2,101.20 | 65 |
| PG | 14 | $152.18 | $154.28 | $2,159.99 | 65 |
| PYPL | 28 | $72.12 | $73.17 | $2,048.76 | 65 |
| QCOM | 14 | $153.83 | $153.07 | $2,143.05 | 65 |
| T | 78 | $27.09 | $26.90 | $2,097.93 | 65 |
| TGT | 21 | $104.77 | $103.00 | $2,163.00 | 65 |
| TSLA | 6 | $318.51 | $321.72 | $1,930.32 | 60 |
| UNH | 7 | $298.51 | $289.25 | $2,024.73 | 65 |
| UNP | 10 | $236.33 | $227.95 | $2,279.50 | 65 |
| V | 6 | $355.85 | $349.14 | $2,094.87 | 65 |
| VZ | 51 | $43.04 | $40.94 | $2,087.94 | 65 |
| WFC | 26 | $78.67 | $80.14 | $2,083.77 | 65 |
| WMT | 22 | $97.29 | $95.00 | $2,090.11 | 65 |
| XOM | 19 | $109.77 | $111.78 | $2,123.82 | 65 |

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
| 2025-07-17 14:53:19 | SELL | NVDA | 1 | $172.82 | $1.11 | 70 |
| 2025-07-17 14:53:19 | SELL | AMD | 1 | $160.08 | $0.01 | 70 |
| 2025-07-17 14:53:19 | SELL | INTC | 2 | $22.80 | $0.89 | 60 |
| 2025-07-17 14:53:19 | SELL | DIS | 1 | $121.26 | $-1.31 | 75 |
| 2025-07-17 14:53:19 | SELL | MRK | 1 | $81.96 | $-0.60 | 70 |
| 2025-07-17 14:53:19 | SELL | ORCL | 1 | $249.93 | $15.33 | 65 |
| 2025-07-17 14:53:19 | BUY | XOM | 2 | $111.89 | N/A | 75 |
| 2025-07-17 14:53:19 | BUY | NKE | 1 | $73.09 | N/A | 70 |
| 2025-07-17 14:41:28 | SELL | NVDA | 1 | $171.37 | $-0.31 | 70 |
| 2025-07-17 14:41:28 | SELL | AMD | 1 | $160.24 | $0.16 | 70 |
| 2025-07-17 14:41:28 | SELL | INTC | 5 | $22.69 | $1.60 | 60 |
| 2025-07-17 14:41:28 | SELL | NKE | 3 | $72.86 | $2.69 | 65 |
| 2025-07-17 14:41:28 | SELL | DIS | 1 | $120.84 | $-1.65 | 75 |
| 2025-07-17 14:41:28 | BUY | PFE | 1 | $24.62 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | WFC | 2 | $79.96 | N/A | 70 |

<!--TRADE_LOG_END--> 
