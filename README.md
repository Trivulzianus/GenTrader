# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 16:10:13**

| Metric | Value |
|---|---|
| **Total Value** | **$101,398.02** |
| Cash | $54.10 |
| Holdings Value | $101,343.92 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.02 | $2,110.20 | 65 |
| ADBE | 6 | $375.23 | $365.29 | $2,191.71 | 65 |
| AMD | 14 | $160.03 | $159.46 | $2,232.37 | 70 |
| AMZN | 10 | $221.65 | $223.84 | $2,238.35 | 75 |
| AVGO | 8 | $275.34 | $287.33 | $2,298.64 | 70 |
| AXP | 7 | $309.18 | $314.11 | $2,198.74 | 75 |
| BA | 9 | $210.81 | $229.06 | $2,061.54 | 70 |
| BAC | 48 | $46.27 | $46.60 | $2,237.04 | 70 |
| C | 30 | $86.85 | $92.42 | $2,772.45 | 85 |
| CAT | 6 | $397.74 | $417.34 | $2,504.05 | 75 |
| COST | 2 | $979.83 | $952.90 | $1,905.80 | 70 |
| CRM | 8 | $267.44 | $259.82 | $2,078.56 | 65 |
| CSCO | 31 | $68.58 | $68.43 | $2,121.33 | 65 |
| CVX | 16 | $146.82 | $150.43 | $2,406.88 | 75 |
| DIS | 19 | $122.69 | $121.35 | $2,305.65 | 70 |
| GOOGL | 13 | $179.34 | $182.87 | $2,377.25 | 75 |
| GS | 3 | $717.52 | $712.80 | $2,138.40 | 75 |
| HD | 6 | $354.18 | $356.75 | $2,140.50 | 65 |
| INTC | 90 | $22.39 | $22.93 | $2,064.15 | 65 |
| JNJ | 13 | $155.43 | $163.48 | $2,125.24 | 65 |
| JPM | 9 | $291.90 | $288.06 | $2,592.54 | 75 |
| KO | 30 | $70.97 | $69.73 | $2,092.05 | 65 |
| LLY | 3 | $781.32 | $781.08 | $2,343.24 | 65 |
| MA | 4 | $563.08 | $553.88 | $2,215.52 | 65 |
| META | 3 | $717.12 | $704.14 | $2,112.43 | 65 |
| MRK | 29 | $82.56 | $82.11 | $2,381.19 | 75 |
| MSFT | 5 | $498.84 | $513.16 | $2,565.80 | 85 |
| NFLX | 1 | $1,279.00 | $1,259.32 | $1,259.32 | 65 |
| NKE | 32 | $71.99 | $72.90 | $2,332.80 | 75 |
| NVDA | 15 | $171.88 | $173.59 | $2,603.93 | 85 |
| ORCL | 9 | $232.91 | $248.63 | $2,237.67 | 70 |
| PEP | 16 | $136.49 | $144.80 | $2,316.80 | 75 |
| PFE | 84 | $25.28 | $24.70 | $2,075.22 | 65 |
| PG | 14 | $152.18 | $154.91 | $2,168.74 | 65 |
| PYPL | 28 | $72.12 | $73.35 | $2,053.80 | 65 |
| QCOM | 14 | $153.83 | $153.38 | $2,147.32 | 65 |
| T | 77 | $27.10 | $26.89 | $2,070.53 | 65 |
| TGT | 20 | $104.83 | $103.46 | $2,069.20 | 65 |
| TSLA | 6 | $318.51 | $321.09 | $1,926.54 | 65 |
| UNH | 7 | $298.51 | $290.01 | $2,030.07 | 65 |
| UNP | 10 | $236.33 | $227.53 | $2,275.25 | 65 |
| V | 6 | $355.85 | $350.17 | $2,100.99 | 65 |
| VZ | 51 | $43.04 | $40.97 | $2,089.22 | 65 |
| WFC | 29 | $78.84 | $80.31 | $2,329.13 | 75 |
| WMT | 22 | $97.29 | $95.31 | $2,096.71 | 65 |
| XOM | 21 | $109.98 | $111.86 | $2,349.06 | 75 |

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
| 2025-07-17 16:10:07 | SELL | CSCO | 1 | $68.43 | $-0.15 | 65 |
| 2025-07-17 16:10:07 | BUY | NVDA | 2 | $173.51 | N/A | 85 |
| 2025-07-17 16:10:07 | BUY | NKE | 3 | $72.90 | N/A | 75 |
| 2025-07-17 16:10:07 | BUY | WFC | 1 | $80.31 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
