# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 16:27:30**

| Metric | Value |
|---|---|
| **Total Value** | **$100,641.22** |
| Cash | $628.66 |
| Holdings Value | $100,012.56 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.52 | $2,105.20 | 65 |
| ADBE | 6 | $375.23 | $364.92 | $2,189.49 | 65 |
| AMD | 17 | $146.29 | $156.15 | $2,654.55 | 85 |
| AMZN | 11 | $222.05 | $226.57 | $2,492.31 | 85 |
| AVGO | 8 | $275.34 | $281.06 | $2,248.49 | 70 |
| AXP | 7 | $325.34 | $313.30 | $2,193.08 | 75 |
| BA | 11 | $214.40 | $231.27 | $2,543.97 | 75 |
| BAC | 44 | $48.83 | $46.55 | $2,047.98 | 65 |
| C | 30 | $86.78 | $89.65 | $2,689.50 | 85 |
| CAT | 6 | $397.74 | $404.64 | $2,427.83 | 70 |
| COST | 2 | $979.83 | $968.98 | $1,937.97 | 65 |
| CRM | 8 | $267.44 | $258.59 | $2,068.72 | 65 |
| CSCO | 31 | $68.46 | $67.37 | $2,088.41 | 65 |
| CVX | 16 | $146.80 | $150.77 | $2,412.32 | 75 |
| DIS | 17 | $122.96 | $119.38 | $2,029.38 | 65 |
| GOOGL | 14 | $179.71 | $183.18 | $2,564.52 | 85 |
| GS | 3 | $717.52 | $704.94 | $2,114.82 | 75 |
| HD | 6 | $372.64 | $362.34 | $2,174.04 | 65 |
| INTC | 88 | $22.39 | $23.32 | $2,052.16 | 65 |
| JNJ | 13 | $155.95 | $155.14 | $2,016.82 | 65 |
| JPM | 9 | $291.63 | $286.72 | $2,580.48 | 85 |
| KO | 30 | $70.97 | $69.28 | $2,078.25 | 65 |
| LLY | 3 | $781.32 | $775.47 | $2,326.42 | 65 |
| MA | 4 | $563.08 | $551.06 | $2,204.24 | 65 |
| META | 3 | $717.12 | $718.83 | $2,156.49 | 65 |
| MRK | 25 | $82.54 | $81.44 | $2,035.94 | 65 |
| MSFT | 5 | $498.84 | $506.97 | $2,534.85 | 70 |
| NFLX | 1 | $1,279.00 | $1,258.97 | $1,258.97 | 65 |
| NKE | 30 | $72.04 | $71.95 | $2,158.50 | 70 |
| NVDA | 13 | $171.78 | $171.41 | $2,228.30 | 70 |
| ORCL | 9 | $233.27 | $233.07 | $2,097.63 | 65 |
| PEP | 15 | $136.57 | $133.82 | $2,007.30 | 65 |
| PFE | 83 | $25.22 | $24.73 | $2,052.18 | 65 |
| PG | 13 | $152.12 | $152.43 | $1,981.56 | 65 |
| PYPL | 28 | $72.13 | $73.50 | $2,058.00 | 65 |
| QCOM | 14 | $153.83 | $154.58 | $2,164.12 | 65 |
| T | 77 | $27.09 | $26.86 | $2,068.22 | 65 |
| TGT | 20 | $104.94 | $102.84 | $2,056.90 | 65 |
| TSLA | 6 | $318.51 | $314.51 | $1,887.06 | 60 |
| UNH | 7 | $298.51 | $293.95 | $2,057.64 | 65 |
| UNP | 10 | $236.14 | $232.49 | $2,324.87 | 75 |
| V | 6 | $355.85 | $347.46 | $2,084.76 | 65 |
| VZ | 50 | $43.08 | $41.15 | $2,057.25 | 65 |
| WFC | 27 | $78.70 | $78.93 | $2,131.11 | 65 |
| WMT | 21 | $97.38 | $95.25 | $2,000.32 | 65 |
| XOM | 21 | $109.99 | $112.84 | $2,369.64 | 75 |

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
| 2025-07-15 16:27:20 | SELL | WFC | 1 | $78.93 | $0.22 | 65 |
| 2025-07-15 16:27:20 | BUY | AMZN | 1 | $226.51 | N/A | 85 |
| 2025-07-15 16:27:20 | BUY | INTC | 1 | $23.31 | N/A | 65 |
| 2025-07-15 16:27:20 | BUY | UNP | 1 | $232.51 | N/A | 75 |
| 2025-07-15 16:10:04 | SELL | BAC | 1 | $46.51 | $-2.28 | 65 |
| 2025-07-15 16:10:04 | SELL | T | 5 | $26.89 | $-0.98 | 65 |
| 2025-07-15 16:10:04 | BUY | INTC | 5 | $23.37 | N/A | 65 |
| 2025-07-15 16:10:04 | BUY | WFC | 1 | $78.69 | N/A | 70 |
| 2025-07-15 15:51:49 | SELL | BAC | 2 | $46.65 | $-4.09 | 65 |
| 2025-07-15 15:51:49 | SELL | PYPL | 1 | $73.72 | $1.53 | 65 |
| 2025-07-15 15:51:49 | BUY | NKE | 1 | $72.13 | N/A | 70 |
| 2025-07-15 15:51:49 | BUY | BA | 2 | $230.76 | N/A | 80 |
| 2025-07-15 15:51:49 | BUY | T | 5 | $26.86 | N/A | 70 |
| 2025-07-15 15:40:17 | SELL | NVDA | 1 | $171.33 | $-0.42 | 70 |
| 2025-07-15 15:40:17 | SELL | INTC | 6 | $23.37 | $5.90 | 60 |
| 2025-07-15 15:40:17 | SELL | PYPL | 1 | $73.64 | $1.41 | 65 |
| 2025-07-15 15:40:17 | SELL | WFC | 1 | $78.91 | $0.19 | 65 |
| 2025-07-15 15:40:17 | BUY | GOOGL | 1 | $183.45 | N/A | 85 |
| 2025-07-15 15:40:17 | BUY | BAC | 3 | $46.65 | N/A | 70 |
| 2025-07-15 15:26:50 | SELL | GOOGL | 1 | $183.84 | $4.10 | 75 |
| 2025-07-15 15:26:50 | SELL | NKE | 2 | $72.35 | $0.59 | 65 |
| 2025-07-15 15:26:50 | SELL | UNP | 1 | $232.75 | $-3.41 | 65 |
| 2025-07-15 15:26:50 | BUY | INTC | 5 | $23.38 | N/A | 65 |
| 2025-07-15 15:26:50 | BUY | PYPL | 1 | $73.56 | N/A | 70 |
| 2025-07-15 15:26:50 | BUY | WFC | 28 | $78.72 | N/A | 70 |

<!--TRADE_LOG_END--> 
