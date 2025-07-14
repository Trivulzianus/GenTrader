# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 17:52:13**

| Metric | Value |
|---|---|
| **Total Value** | **$100,857.42** |
| Cash | $323.00 |
| Holdings Value | $100,534.42 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.12 | $2,091.20 | 65 |
| ADBE | 6 | $375.23 | $366.52 | $2,199.12 | 65 |
| AMD | 16 | $135.48 | $146.85 | $2,349.60 | 75 |
| AMZN | 11 | $221.92 | $225.80 | $2,483.80 | 85 |
| AVGO | 8 | $275.34 | $276.59 | $2,212.72 | 70 |
| AXP | 7 | $325.34 | $320.62 | $2,244.34 | 75 |
| BA | 10 | $212.67 | $229.29 | $2,292.90 | 70 |
| BAC | 47 | $48.71 | $46.91 | $2,204.77 | 70 |
| C | 27 | $86.54 | $87.27 | $2,356.42 | 75 |
| CAT | 6 | $397.74 | $404.73 | $2,428.35 | 75 |
| COST | 2 | $979.83 | $976.78 | $1,953.57 | 65 |
| CRM | 7 | $268.68 | $261.40 | $1,829.80 | 65 |
| CSCO | 31 | $68.48 | $67.91 | $2,105.05 | 70 |
| CVX | 16 | $146.79 | $151.64 | $2,426.24 | 75 |
| DIS | 18 | $122.80 | $120.39 | $2,167.02 | 70 |
| GOOGL | 14 | $179.69 | $181.19 | $2,536.66 | 85 |
| GS | 3 | $717.52 | $711.89 | $2,135.67 | 85 |
| HD | 6 | $372.64 | $368.35 | $2,210.11 | 70 |
| INTC | 86 | $22.37 | $23.28 | $2,002.08 | 65 |
| JNJ | 13 | $155.95 | $156.59 | $2,035.73 | 65 |
| JPM | 9 | $291.63 | $288.90 | $2,600.10 | 85 |
| KO | 29 | $71.03 | $69.42 | $2,013.04 | 65 |
| LLY | 3 | $781.32 | $797.40 | $2,392.20 | 70 |
| MA | 4 | $563.08 | $555.10 | $2,220.40 | 65 |
| META | 3 | $717.12 | $722.98 | $2,168.94 | 85 |
| MRK | 31 | $82.62 | $83.80 | $2,597.64 | 85 |
| MSFT | 5 | $498.84 | $502.58 | $2,512.90 | 75 |
| NFLX | 1 | $1,279.00 | $1,268.67 | $1,268.67 | 65 |
| NKE | 28 | $72.03 | $72.17 | $2,020.71 | 65 |
| NVDA | 15 | $157.18 | $164.98 | $2,474.70 | 85 |
| ORCL | 10 | $232.94 | $230.31 | $2,303.05 | 70 |
| PEP | 15 | $136.57 | $135.59 | $2,033.79 | 65 |
| PFE | 84 | $25.20 | $25.48 | $2,140.74 | 70 |
| PG | 13 | $160.78 | $153.99 | $2,001.87 | 65 |
| PYPL | 28 | $72.11 | $73.67 | $2,062.90 | 65 |
| QCOM | 14 | $153.83 | $154.25 | $2,159.50 | 70 |
| T | 74 | $27.10 | $27.16 | $2,009.47 | 65 |
| TGT | 20 | $104.94 | $104.74 | $2,094.80 | 65 |
| TSLA | 6 | $288.62 | $314.31 | $1,885.86 | 65 |
| UNH | 7 | $298.51 | $300.14 | $2,101.01 | 65 |
| UNP | 10 | $236.29 | $233.45 | $2,334.50 | 75 |
| V | 6 | $355.85 | $351.02 | $2,106.12 | 65 |
| VZ | 49 | $43.12 | $41.61 | $2,038.98 | 65 |
| WFC | 28 | $82.26 | $83.39 | $2,334.78 | 75 |
| WMT | 21 | $97.38 | $95.65 | $2,008.65 | 65 |
| XOM | 21 | $110.01 | $113.52 | $2,383.92 | 75 |

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
| 2025-07-14 17:52:02 | SELL | PYPL | 3 | $73.68 | $4.26 | 65 |
| 2025-07-14 17:52:02 | BUY | NVDA | 1 | $164.99 | N/A | 85 |
| 2025-07-14 17:52:02 | BUY | PFE | 5 | $25.51 | N/A | 70 |
| 2025-07-14 17:52:02 | BUY | MRK | 3 | $83.83 | N/A | 85 |
| 2025-07-14 17:52:02 | BUY | CSCO | 1 | $67.91 | N/A | 70 |
| 2025-07-14 17:40:02 | SELL | NKE | 1 | $72.27 | $0.23 | 65 |
| 2025-07-14 17:40:02 | SELL | PFE | 7 | $25.48 | $1.89 | 65 |
| 2025-07-14 17:40:02 | SELL | C | 4 | $87.31 | $2.67 | 75 |
| 2025-07-14 17:40:02 | SELL | CSCO | 2 | $67.84 | $-1.23 | 65 |
| 2025-07-14 17:40:02 | SELL | T | 1 | $27.16 | $0.05 | 65 |
| 2025-07-14 17:40:02 | BUY | GOOGL | 1 | $181.31 | N/A | 85 |
| 2025-07-14 17:40:02 | BUY | INTC | 4 | $23.25 | N/A | 65 |
| 2025-07-14 17:40:02 | BUY | PYPL | 3 | $73.75 | N/A | 75 |
| 2025-07-14 17:40:02 | BUY | WMT | 1 | $95.57 | N/A | 65 |
| 2025-07-14 17:40:02 | BUY | ORCL | 1 | $230.07 | N/A | 75 |
| 2025-07-14 17:26:00 | SELL | PYPL | 4 | $73.79 | $5.89 | 65 |
| 2025-07-14 17:26:00 | SELL | WMT | 1 | $95.60 | $-1.79 | 60 |
| 2025-07-14 17:26:00 | BUY | AMD | 1 | $146.83 | N/A | 75 |
| 2025-07-14 17:09:36 | SELL | NVDA | 2 | $165.10 | $14.84 | 70 |
| 2025-07-14 17:09:36 | SELL | INTC | 6 | $23.15 | $4.58 | 60 |
| 2025-07-14 17:09:36 | BUY | PYPL | 4 | $73.64 | N/A | 75 |
| 2025-07-14 17:09:36 | BUY | QCOM | 1 | $154.25 | N/A | 70 |
| 2025-07-14 17:09:36 | BUY | CSCO | 1 | $67.62 | N/A | 70 |
| 2025-07-14 16:56:14 | SELL | NKE | 3 | $72.29 | $0.69 | 65 |
| 2025-07-14 16:56:14 | SELL | CSCO | 1 | $67.55 | $-0.90 | 65 |

<!--TRADE_LOG_END--> 
