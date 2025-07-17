# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 14:26:41**

| Metric | Value |
|---|---|
| **Total Value** | **$100,987.64** |
| Cash | $45.85 |
| Holdings Value | $100,941.79 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.88 | $2,098.80 | 65 |
| ADBE | 6 | $375.23 | $360.64 | $2,163.87 | 65 |
| AMD | 16 | $160.08 | $159.96 | $2,559.36 | 85 |
| AMZN | 10 | $221.65 | $222.76 | $2,227.61 | 75 |
| AVGO | 8 | $275.34 | $284.26 | $2,274.08 | 65 |
| AXP | 7 | $309.18 | $311.62 | $2,181.34 | 65 |
| BA | 9 | $210.81 | $229.37 | $2,064.35 | 65 |
| BAC | 45 | $46.26 | $46.08 | $2,073.60 | 65 |
| C | 30 | $86.85 | $90.42 | $2,712.75 | 85 |
| CAT | 6 | $397.74 | $415.67 | $2,494.02 | 85 |
| COST | 2 | $979.83 | $949.95 | $1,899.89 | 65 |
| CRM | 8 | $267.44 | $256.93 | $2,055.48 | 65 |
| CSCO | 31 | $68.48 | $68.02 | $2,108.77 | 65 |
| CVX | 15 | $146.65 | $149.26 | $2,238.97 | 75 |
| DIS | 22 | $122.49 | $121.12 | $2,664.64 | 85 |
| GOOGL | 13 | $179.34 | $182.26 | $2,369.38 | 70 |
| GS | 3 | $717.52 | $709.27 | $2,127.82 | 70 |
| HD | 6 | $354.18 | $355.90 | $2,135.40 | 65 |
| INTC | 91 | $22.37 | $22.69 | $2,064.79 | 65 |
| JNJ | 13 | $155.43 | $163.07 | $2,119.91 | 65 |
| JPM | 9 | $291.90 | $287.81 | $2,590.34 | 75 |
| KO | 30 | $70.97 | $69.87 | $2,096.10 | 65 |
| LLY | 3 | $781.32 | $785.02 | $2,355.06 | 70 |
| MA | 4 | $563.08 | $550.72 | $2,202.88 | 65 |
| META | 3 | $717.12 | $698.81 | $2,096.43 | 65 |
| MRK | 29 | $82.56 | $82.21 | $2,384.11 | 75 |
| MSFT | 5 | $498.84 | $510.04 | $2,550.19 | 85 |
| NFLX | 1 | $1,279.00 | $1,255.31 | $1,255.31 | 65 |
| NKE | 32 | $71.96 | $72.75 | $2,328.00 | 75 |
| NVDA | 15 | $171.68 | $172.87 | $2,592.98 | 85 |
| ORCL | 9 | $232.99 | $249.44 | $2,244.94 | 65 |
| PEP | 16 | $136.49 | $143.65 | $2,298.40 | 70 |
| PFE | 84 | $25.28 | $24.64 | $2,070.18 | 65 |
| PG | 14 | $152.18 | $154.80 | $2,167.20 | 65 |
| PYPL | 28 | $72.12 | $72.62 | $2,033.36 | 65 |
| QCOM | 14 | $153.83 | $152.40 | $2,133.60 | 65 |
| T | 77 | $27.10 | $27.01 | $2,079.77 | 65 |
| TGT | 21 | $104.77 | $102.78 | $2,158.49 | 65 |
| TSLA | 6 | $318.51 | $321.12 | $1,926.74 | 65 |
| UNH | 7 | $298.51 | $287.25 | $2,010.75 | 65 |
| UNP | 10 | $236.33 | $227.82 | $2,278.25 | 75 |
| V | 6 | $355.85 | $348.90 | $2,093.43 | 65 |
| VZ | 50 | $43.08 | $41.07 | $2,053.50 | 65 |
| WFC | 26 | $78.68 | $80.05 | $2,081.17 | 65 |
| WMT | 22 | $97.29 | $95.42 | $2,099.13 | 65 |
| XOM | 19 | $109.76 | $111.93 | $2,126.67 | 65 |

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
| 2025-07-17 14:26:31 | SELL | XOM | 1 | $112.23 | $2.35 | 65 |
| 2025-07-17 14:26:31 | BUY | NVDA | 2 | $172.63 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | AMD | 2 | $160.08 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | DIS | 3 | $121.17 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | NKE | 3 | $72.73 | N/A | 75 |
| 2025-07-17 14:26:31 | BUY | UNP | 1 | $231.18 | N/A | 75 |
| 2025-07-17 14:08:25 | SELL | XOM | 1 | $112.00 | $2.02 | 70 |
| 2025-07-17 14:08:25 | SELL | WFC | 4 | $80.25 | $5.45 | 65 |
| 2025-07-17 14:08:25 | SELL | CSCO | 1 | $67.37 | $-1.08 | 65 |
| 2025-07-17 14:08:25 | SELL | CVX | 1 | $149.52 | $2.69 | 70 |
| 2025-07-17 14:08:25 | BUY | DIS | 1 | $121.55 | N/A | 75 |
| 2025-07-17 13:49:19 | SELL | NKE | 4 | $72.76 | $3.08 | 65 |
| 2025-07-17 13:49:19 | SELL | UNP | 1 | $230.08 | $-6.14 | 65 |
| 2025-07-17 13:49:19 | BUY | INTC | 7 | $22.67 | N/A | 65 |
| 2025-07-17 13:49:19 | BUY | AXP | 1 | $314.02 | N/A | 70 |
| 2025-07-17 13:49:19 | BUY | CSCO | 1 | $68.18 | N/A | 70 |
| 2025-07-17 13:30:02 | SELL | INTC | 6 | $22.69 | $1.93 | 60 |
| 2025-07-17 13:30:02 | BUY | UNP | 1 | $231.18 | N/A | 75 |
| 2025-07-17 13:04:44 | SELL | BAC | 3 | $46.03 | $-0.64 | 65 |
| 2025-07-17 13:04:44 | SELL | UNP | 1 | $231.18 | $-5.04 | 65 |
| 2025-07-17 13:04:44 | BUY | INTC | 5 | $22.69 | N/A | 65 |
| 2025-07-17 13:04:44 | BUY | NKE | 4 | $72.10 | N/A | 75 |
| 2025-07-17 13:04:44 | BUY | VZ | 3 | $41.25 | N/A | 65 |
| 2025-07-17 13:04:44 | BUY | TGT | 1 | $101.34 | N/A | 70 |
| 2025-07-17 12:32:27 | SELL | VZ | 3 | $41.25 | $-5.49 | 60 |

<!--TRADE_LOG_END--> 
