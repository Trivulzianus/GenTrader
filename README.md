# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 13:49:28**

| Metric | Value |
|---|---|
| **Total Value** | **$101,397.04** |
| Cash | $749.76 |
| Holdings Value | $100,647.29 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.18 | $2,101.76 | 65 |
| ADBE | 6 | $375.23 | $365.13 | $2,190.78 | 65 |
| AMD | 13 | $160.00 | $160.26 | $2,083.38 | 65 |
| AMZN | 11 | $221.89 | $225.15 | $2,476.60 | 75 |
| AVGO | 8 | $275.34 | $285.63 | $2,285.04 | 70 |
| AXP | 7 | $309.18 | $305.13 | $2,135.91 | 65 |
| BA | 10 | $232.01 | $231.22 | $2,312.20 | 65 |
| BAC | 48 | $46.30 | $47.05 | $2,258.40 | 70 |
| C | 29 | $86.64 | $93.75 | $2,718.75 | 85 |
| CAT | 6 | $397.74 | $417.61 | $2,505.63 | 85 |
| COST | 2 | $979.83 | $957.28 | $1,914.56 | 65 |
| CRM | 8 | $267.44 | $259.62 | $2,077.00 | 65 |
| CSCO | 33 | $68.56 | $68.77 | $2,269.24 | 70 |
| CVX | 16 | $146.84 | $151.25 | $2,419.92 | 75 |
| DIS | 19 | $122.64 | $121.40 | $2,306.53 | 70 |
| GOOGL | 13 | $179.34 | $185.05 | $2,405.65 | 70 |
| GS | 3 | $717.52 | $707.40 | $2,122.22 | 70 |
| HD | 6 | $354.18 | $358.67 | $2,152.02 | 65 |
| INTC | 84 | $22.34 | $23.12 | $1,942.50 | 60 |
| JNJ | 14 | $155.97 | $164.41 | $2,301.81 | 70 |
| JPM | 8 | $292.14 | $290.72 | $2,325.76 | 70 |
| KO | 31 | $70.95 | $70.40 | $2,182.40 | 70 |
| LLY | 3 | $781.32 | $769.26 | $2,307.78 | 65 |
| MA | 4 | $563.08 | $553.34 | $2,213.36 | 65 |
| META | 3 | $717.12 | $699.73 | $2,099.19 | 70 |
| MRK | 29 | $82.56 | $81.43 | $2,361.47 | 75 |
| MSFT | 5 | $498.84 | $512.20 | $2,560.98 | 85 |
| NFLX | 1 | $1,279.00 | $1,224.74 | $1,224.74 | 65 |
| NKE | 33 | $72.02 | $72.59 | $2,395.63 | 75 |
| NVDA | 15 | $171.91 | $173.92 | $2,608.80 | 85 |
| ORCL | 9 | $232.91 | $249.37 | $2,244.33 | 70 |
| PEP | 15 | $135.89 | $144.80 | $2,172.00 | 65 |
| PFE | 84 | $25.28 | $24.64 | $2,069.76 | 65 |
| PG | 13 | $151.91 | $155.06 | $2,015.78 | 65 |
| PYPL | 29 | $72.18 | $73.87 | $2,142.23 | 65 |
| QCOM | 14 | $153.83 | $153.60 | $2,150.40 | 65 |
| T | 78 | $27.10 | $26.86 | $2,094.69 | 65 |
| TGT | 19 | $104.88 | $103.97 | $1,975.34 | 60 |
| TSLA | 6 | $318.51 | $326.31 | $1,957.86 | 65 |
| UNH | 7 | $298.51 | $286.23 | $2,003.61 | 65 |
| UNP | 9 | $237.31 | $226.28 | $2,036.52 | 65 |
| V | 6 | $355.85 | $347.87 | $2,087.22 | 65 |
| VZ | 51 | $40.87 | $41.02 | $2,092.02 | 65 |
| WFC | 27 | $78.73 | $79.80 | $2,154.60 | 65 |
| WMT | 22 | $97.29 | $95.03 | $2,090.66 | 65 |
| XOM | 19 | $109.80 | $110.54 | $2,100.26 | 65 |

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
| 2025-07-18 13:49:22 | SELL | WFC | 2 | $79.81 | $2.01 | 65 |
| 2025-07-18 13:49:22 | SELL | T | 5 | $26.84 | $-1.21 | 65 |
| 2025-07-18 13:49:22 | SELL | TGT | 1 | $103.98 | $-0.85 | 60 |
| 2025-07-18 13:49:22 | BUY | NVDA | 2 | $173.85 | N/A | 85 |
| 2025-07-18 13:49:22 | BUY | KO | 1 | $70.39 | N/A | 70 |
| 2025-07-18 13:49:22 | BUY | MRK | 1 | $81.42 | N/A | 75 |
| 2025-07-18 13:49:22 | BUY | NKE | 4 | $72.58 | N/A | 75 |
| 2025-07-18 13:29:45 | SELL | JPM | 1 | $289.90 | $-2.00 | 70 |
| 2025-07-18 13:29:45 | SELL | KO | 2 | $70.59 | $-0.71 | 65 |
| 2025-07-18 13:29:45 | SELL | PYPL | 3 | $73.86 | $4.56 | 65 |
| 2025-07-18 13:29:45 | SELL | MRK | 1 | $81.52 | $-1.04 | 70 |
| 2025-07-18 13:29:45 | SELL | CSCO | 2 | $68.30 | $-0.50 | 70 |
| 2025-07-18 13:29:45 | BUY | T | 6 | $26.99 | N/A | 70 |
| 2025-07-18 13:05:06 | SELL | INTC | 6 | $22.80 | $2.56 | 60 |
| 2025-07-18 13:05:06 | SELL | BA | 1 | $231.00 | $-0.92 | 70 |
| 2025-07-18 13:05:06 | BUY | WFC | 1 | $79.71 | N/A | 75 |
| 2025-07-18 12:32:55 | SELL | BAC | 2 | $47.02 | $1.39 | 70 |
| 2025-07-18 12:32:55 | SELL | NKE | 1 | $72.98 | $1.00 | 65 |
| 2025-07-18 12:32:55 | BUY | INTC | 6 | $22.80 | N/A | 65 |
| 2025-07-18 12:32:55 | BUY | PYPL | 3 | $73.86 | N/A | 75 |
| 2025-07-18 12:32:55 | BUY | MRK | 3 | $81.52 | N/A | 75 |
| 2025-07-18 12:14:27 | SELL | INTC | 6 | $22.80 | $2.56 | 60 |
| 2025-07-18 12:14:27 | SELL | PYPL | 3 | $73.86 | $4.56 | 65 |
| 2025-07-18 12:14:27 | SELL | MRK | 3 | $81.52 | $-3.12 | 65 |
| 2025-07-18 12:14:27 | BUY | NKE | 1 | $72.98 | N/A | 70 |

<!--TRADE_LOG_END--> 
