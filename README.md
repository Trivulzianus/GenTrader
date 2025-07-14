# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 18:11:38**

| Metric | Value |
|---|---|
| **Total Value** | **$100,843.21** |
| Cash | $137.73 |
| Holdings Value | $100,705.48 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.18 | $2,091.77 | 65 |
| ADBE | 6 | $375.23 | $366.05 | $2,196.30 | 65 |
| AMD | 16 | $135.48 | $146.62 | $2,345.93 | 75 |
| AMZN | 11 | $221.92 | $225.46 | $2,480.06 | 85 |
| AVGO | 8 | $275.34 | $276.33 | $2,210.64 | 65 |
| AXP | 7 | $325.34 | $320.65 | $2,244.55 | 70 |
| BA | 10 | $212.67 | $229.54 | $2,295.44 | 70 |
| BAC | 47 | $48.71 | $46.97 | $2,207.36 | 70 |
| C | 30 | $86.62 | $87.28 | $2,618.40 | 85 |
| CAT | 6 | $397.74 | $404.79 | $2,428.74 | 70 |
| COST | 2 | $979.83 | $974.74 | $1,949.48 | 65 |
| CRM | 7 | $268.68 | $261.01 | $1,827.11 | 65 |
| CSCO | 30 | $68.50 | $67.86 | $2,035.95 | 65 |
| CVX | 17 | $147.10 | $152.13 | $2,586.21 | 85 |
| DIS | 18 | $122.80 | $120.33 | $2,165.85 | 70 |
| GOOGL | 14 | $179.69 | $181.65 | $2,543.10 | 85 |
| GS | 3 | $717.52 | $711.35 | $2,134.05 | 85 |
| HD | 6 | $372.64 | $368.82 | $2,212.92 | 70 |
| INTC | 86 | $22.37 | $23.32 | $2,005.95 | 65 |
| JNJ | 13 | $155.95 | $156.43 | $2,033.53 | 65 |
| JPM | 9 | $291.63 | $288.15 | $2,593.35 | 85 |
| KO | 29 | $71.03 | $69.44 | $2,013.90 | 65 |
| LLY | 3 | $781.32 | $795.82 | $2,387.46 | 70 |
| MA | 4 | $563.08 | $554.45 | $2,217.80 | 65 |
| META | 3 | $717.12 | $723.58 | $2,170.74 | 85 |
| MRK | 30 | $82.59 | $83.77 | $2,513.10 | 80 |
| MSFT | 5 | $498.84 | $502.48 | $2,512.40 | 75 |
| NFLX | 1 | $1,279.00 | $1,268.30 | $1,268.30 | 65 |
| NKE | 28 | $72.03 | $72.31 | $2,024.68 | 65 |
| NVDA | 15 | $157.18 | $164.83 | $2,472.42 | 85 |
| ORCL | 9 | $233.27 | $230.01 | $2,070.09 | 65 |
| PEP | 15 | $136.57 | $135.76 | $2,036.40 | 65 |
| PFE | 90 | $25.22 | $25.49 | $2,293.67 | 75 |
| PG | 13 | $160.78 | $153.93 | $2,001.09 | 65 |
| PYPL | 28 | $72.11 | $73.75 | $2,064.86 | 65 |
| QCOM | 14 | $153.83 | $154.38 | $2,161.32 | 65 |
| T | 74 | $27.10 | $27.12 | $2,007.25 | 65 |
| TGT | 20 | $104.94 | $104.57 | $2,091.40 | 65 |
| TSLA | 6 | $288.62 | $314.36 | $1,886.18 | 65 |
| UNH | 7 | $298.51 | $300.56 | $2,103.92 | 65 |
| UNP | 10 | $236.29 | $233.47 | $2,334.70 | 75 |
| V | 6 | $355.85 | $350.69 | $2,104.14 | 70 |
| VZ | 49 | $43.12 | $41.62 | $2,039.38 | 65 |
| WFC | 28 | $82.26 | $83.39 | $2,334.78 | 75 |
| WMT | 21 | $97.38 | $95.30 | $2,001.21 | 65 |
| XOM | 21 | $110.01 | $113.69 | $2,387.59 | 75 |

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
| 2025-07-14 18:11:32 | SELL | MRK | 1 | $83.78 | $1.15 | 80 |
| 2025-07-14 18:11:32 | SELL | ORCL | 1 | $229.99 | $-2.94 | 65 |
| 2025-07-14 18:11:32 | SELL | CSCO | 1 | $67.86 | $-0.61 | 65 |
| 2025-07-14 18:11:32 | BUY | PFE | 6 | $25.49 | N/A | 75 |
| 2025-07-14 18:11:32 | BUY | C | 3 | $87.28 | N/A | 85 |
| 2025-07-14 18:11:32 | BUY | CVX | 1 | $152.13 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
