# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 15:09:38**

| Metric | Value |
|---|---|
| **Total Value** | **$101,210.62** |
| Cash | $338.92 |
| Holdings Value | $100,871.70 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.62 | $2,106.15 | 65 |
| ADBE | 6 | $375.23 | $363.62 | $2,181.72 | 65 |
| AMD | 14 | $160.07 | $159.77 | $2,236.83 | 70 |
| AMZN | 10 | $221.65 | $223.76 | $2,237.60 | 75 |
| AVGO | 8 | $275.34 | $287.65 | $2,301.20 | 70 |
| AXP | 7 | $309.18 | $313.23 | $2,192.61 | 65 |
| BA | 9 | $210.81 | $228.99 | $2,060.91 | 65 |
| BAC | 45 | $46.26 | $46.23 | $2,080.12 | 65 |
| C | 30 | $86.85 | $91.56 | $2,746.65 | 85 |
| CAT | 6 | $397.74 | $416.33 | $2,497.98 | 85 |
| COST | 2 | $979.83 | $951.13 | $1,902.26 | 65 |
| CRM | 8 | $267.44 | $257.87 | $2,062.92 | 65 |
| CSCO | 32 | $68.48 | $68.26 | $2,184.32 | 70 |
| CVX | 16 | $146.82 | $149.88 | $2,398.08 | 75 |
| DIS | 19 | $122.69 | $121.67 | $2,311.80 | 70 |
| GOOGL | 13 | $179.34 | $182.02 | $2,366.26 | 70 |
| GS | 3 | $717.52 | $709.25 | $2,127.75 | 85 |
| HD | 6 | $354.18 | $355.84 | $2,135.04 | 65 |
| INTC | 84 | $22.34 | $22.86 | $1,919.82 | 60 |
| JNJ | 13 | $155.43 | $162.48 | $2,112.24 | 65 |
| JPM | 9 | $291.90 | $287.92 | $2,591.24 | 75 |
| KO | 30 | $70.97 | $69.55 | $2,086.50 | 65 |
| LLY | 3 | $781.32 | $789.37 | $2,368.11 | 70 |
| MA | 4 | $563.08 | $552.91 | $2,211.66 | 65 |
| META | 3 | $717.12 | $702.98 | $2,108.94 | 70 |
| MRK | 29 | $82.56 | $82.00 | $2,378.14 | 75 |
| MSFT | 5 | $498.84 | $512.02 | $2,560.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,258.52 | $1,258.52 | 60 |
| NKE | 30 | $71.91 | $73.10 | $2,193.00 | 70 |
| NVDA | 15 | $171.84 | $173.21 | $2,598.08 | 85 |
| ORCL | 9 | $232.91 | $250.65 | $2,255.81 | 65 |
| PEP | 16 | $136.49 | $143.97 | $2,303.52 | 70 |
| PFE | 85 | $25.27 | $24.58 | $2,089.60 | 65 |
| PG | 14 | $152.18 | $154.08 | $2,157.12 | 65 |
| PYPL | 28 | $72.12 | $73.01 | $2,044.28 | 65 |
| QCOM | 14 | $153.83 | $153.22 | $2,145.01 | 65 |
| T | 78 | $27.09 | $26.86 | $2,095.08 | 65 |
| TGT | 21 | $104.77 | $102.91 | $2,161.01 | 65 |
| TSLA | 6 | $318.51 | $322.96 | $1,937.76 | 65 |
| UNH | 7 | $298.51 | $288.54 | $2,019.78 | 65 |
| UNP | 10 | $236.33 | $228.19 | $2,281.90 | 65 |
| V | 6 | $355.85 | $349.08 | $2,094.48 | 65 |
| VZ | 51 | $43.04 | $40.94 | $2,087.68 | 65 |
| WFC | 28 | $78.77 | $80.19 | $2,245.46 | 70 |
| WMT | 22 | $97.29 | $94.92 | $2,088.13 | 65 |
| XOM | 21 | $109.96 | $111.83 | $2,348.53 | 75 |

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
| 2025-07-17 14:41:28 | BUY | VZ | 1 | $40.96 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | ORCL | 1 | $249.18 | N/A | 80 |
| 2025-07-17 14:41:28 | BUY | T | 1 | $26.91 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | CVX | 1 | $149.46 | N/A | 75 |
| 2025-07-17 14:26:31 | SELL | XOM | 1 | $112.23 | $2.35 | 65 |
| 2025-07-17 14:26:31 | BUY | NVDA | 2 | $172.63 | N/A | 85 |

<!--TRADE_LOG_END--> 
