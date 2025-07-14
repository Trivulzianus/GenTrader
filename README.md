# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 16:27:28**

| Metric | Value |
|---|---|
| **Total Value** | **$100,704.72** |
| Cash | $448.77 |
| Holdings Value | $100,255.95 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.88 | $2,088.85 | 70 |
| ADBE | 6 | $375.23 | $364.39 | $2,186.37 | 65 |
| AMD | 15 | $134.72 | $146.66 | $2,199.90 | 70 |
| AMZN | 11 | $221.92 | $226.00 | $2,486.00 | 75 |
| AVGO | 8 | $275.34 | $275.57 | $2,204.56 | 70 |
| AXP | 7 | $325.34 | $320.68 | $2,244.76 | 70 |
| BA | 10 | $212.67 | $229.86 | $2,298.60 | 70 |
| BAC | 47 | $48.71 | $46.84 | $2,201.48 | 70 |
| C | 31 | $86.64 | $87.05 | $2,698.55 | 85 |
| CAT | 6 | $397.74 | $404.05 | $2,424.30 | 70 |
| COST | 2 | $979.83 | $973.67 | $1,947.35 | 70 |
| CRM | 7 | $268.68 | $260.65 | $1,824.55 | 65 |
| CSCO | 31 | $68.48 | $67.46 | $2,091.13 | 65 |
| CVX | 16 | $146.79 | $152.07 | $2,433.12 | 75 |
| DIS | 18 | $122.80 | $120.27 | $2,164.86 | 65 |
| GOOGL | 13 | $179.57 | $180.56 | $2,347.22 | 75 |
| GS | 3 | $717.52 | $711.88 | $2,135.65 | 65 |
| HD | 6 | $372.64 | $366.79 | $2,200.74 | 65 |
| INTC | 88 | $22.38 | $23.12 | $2,035.00 | 65 |
| JNJ | 13 | $155.95 | $155.95 | $2,027.35 | 65 |
| JPM | 9 | $291.63 | $288.17 | $2,593.53 | 85 |
| KO | 29 | $71.03 | $69.62 | $2,019.12 | 65 |
| LLY | 3 | $781.32 | $795.54 | $2,386.62 | 70 |
| MA | 4 | $563.08 | $555.12 | $2,220.48 | 65 |
| META | 3 | $717.12 | $725.26 | $2,175.78 | 70 |
| MRK | 28 | $82.49 | $83.42 | $2,335.76 | 75 |
| MSFT | 5 | $498.84 | $502.47 | $2,512.34 | 75 |
| NFLX | 1 | $1,279.00 | $1,265.93 | $1,265.93 | 65 |
| NKE | 32 | $72.06 | $72.23 | $2,311.36 | 75 |
| NVDA | 16 | $157.68 | $164.93 | $2,638.88 | 85 |
| ORCL | 9 | $233.26 | $230.30 | $2,072.70 | 70 |
| PEP | 15 | $136.57 | $135.23 | $2,028.45 | 65 |
| PFE | 92 | $25.23 | $25.48 | $2,344.16 | 75 |
| PG | 13 | $160.78 | $153.40 | $1,994.20 | 65 |
| PYPL | 29 | $72.18 | $73.59 | $2,134.11 | 70 |
| QCOM | 13 | $153.79 | $153.88 | $2,000.44 | 65 |
| T | 75 | $27.10 | $27.12 | $2,034.38 | 65 |
| TGT | 20 | $104.94 | $104.78 | $2,095.60 | 65 |
| TSLA | 6 | $288.62 | $314.66 | $1,887.96 | 60 |
| UNH | 7 | $298.51 | $299.24 | $2,094.64 | 65 |
| UNP | 9 | $236.63 | $232.96 | $2,096.60 | 65 |
| V | 6 | $355.85 | $350.92 | $2,105.49 | 70 |
| VZ | 49 | $43.12 | $41.53 | $2,034.97 | 65 |
| WFC | 27 | $82.23 | $83.16 | $2,245.18 | 70 |
| WMT | 21 | $97.38 | $95.41 | $2,003.52 | 65 |
| XOM | 21 | $110.01 | $113.50 | $2,383.39 | 75 |

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
| 2025-07-14 16:27:18 | SELL | WFC | 1 | $83.16 | $0.90 | 70 |
| 2025-07-14 16:27:18 | SELL | BA | 1 | $229.86 | $15.63 | 70 |
| 2025-07-14 16:27:18 | SELL | UNP | 1 | $232.96 | $-3.31 | 65 |
| 2025-07-14 16:27:18 | BUY | INTC | 1 | $23.12 | N/A | 65 |
| 2025-07-14 16:27:18 | BUY | PYPL | 1 | $73.61 | N/A | 70 |
| 2025-07-14 16:27:18 | BUY | MRK | 2 | $83.43 | N/A | 75 |
| 2025-07-14 16:27:18 | BUY | NKE | 3 | $72.23 | N/A | 75 |
| 2025-07-14 16:27:18 | BUY | PFE | 6 | $25.49 | N/A | 75 |
| 2025-07-14 16:09:59 | SELL | PYPL | 2 | $73.56 | $2.66 | 65 |
| 2025-07-14 16:09:59 | SELL | NKE | 2 | $72.37 | $0.60 | 65 |
| 2025-07-14 16:09:59 | SELL | CVX | 1 | $152.08 | $4.98 | 75 |
| 2025-07-14 16:09:59 | BUY | BAC | 1 | $46.73 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | AMD | 1 | $146.40 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | DIS | 1 | $120.31 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | MRK | 1 | $83.47 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | UNP | 1 | $233.26 | N/A | 75 |
| 2025-07-14 15:52:17 | SELL | DIS | 1 | $120.24 | $-2.56 | 65 |
| 2025-07-14 15:52:17 | SELL | MRK | 3 | $83.36 | $2.65 | 65 |
| 2025-07-14 15:52:17 | SELL | PYPL | 1 | $73.48 | $1.21 | 70 |
| 2025-07-14 15:52:17 | BUY | BAC | 2 | $46.85 | N/A | 70 |
| 2025-07-14 15:52:17 | BUY | BA | 1 | $230.60 | N/A | 85 |
| 2025-07-14 15:40:20 | SELL | BAC | 2 | $46.81 | $-3.88 | 65 |
| 2025-07-14 15:40:20 | SELL | NKE | 1 | $72.42 | $0.34 | 70 |
| 2025-07-14 15:40:20 | SELL | MRK | 1 | $83.70 | $1.18 | 75 |
| 2025-07-14 15:40:20 | SELL | PFE | 1 | $25.53 | $0.31 | 70 |

<!--TRADE_LOG_END--> 
