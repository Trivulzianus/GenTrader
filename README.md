# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 20:09:27**

| Metric | Value |
|---|---|
| **Total Value** | **$100,860.96** |
| Cash | $215.12 |
| Holdings Value | $100,645.85 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.62 | $2,086.20 | 65 |
| ADBE | 6 | $375.23 | $366.99 | $2,201.94 | 65 |
| AMD | 15 | $134.71 | $146.24 | $2,193.60 | 75 |
| AMZN | 11 | $221.97 | $225.69 | $2,482.59 | 80 |
| AVGO | 8 | $275.34 | $275.60 | $2,204.80 | 65 |
| AXP | 7 | $325.34 | $320.73 | $2,245.11 | 70 |
| BA | 10 | $212.67 | $230.44 | $2,304.40 | 70 |
| BAC | 47 | $48.70 | $47.04 | $2,210.88 | 70 |
| C | 30 | $86.60 | $87.46 | $2,623.80 | 85 |
| CAT | 6 | $397.74 | $405.57 | $2,433.42 | 85 |
| COST | 2 | $979.83 | $980.91 | $1,961.82 | 65 |
| CRM | 7 | $268.68 | $259.55 | $1,816.85 | 65 |
| CSCO | 32 | $68.45 | $67.82 | $2,170.24 | 70 |
| CVX | 16 | $146.79 | $151.66 | $2,426.56 | 75 |
| DIS | 18 | $122.79 | $119.99 | $2,159.81 | 70 |
| GOOGL | 14 | $179.74 | $181.56 | $2,541.84 | 85 |
| GS | 3 | $717.52 | $712.92 | $2,138.76 | 85 |
| HD | 6 | $372.64 | $370.06 | $2,220.39 | 65 |
| INTC | 87 | $22.38 | $23.30 | $2,027.10 | 65 |
| JNJ | 13 | $155.95 | $156.83 | $2,038.79 | 65 |
| JPM | 9 | $291.63 | $288.63 | $2,597.72 | 85 |
| KO | 29 | $71.03 | $69.48 | $2,014.78 | 65 |
| LLY | 3 | $781.32 | $799.26 | $2,397.77 | 70 |
| MA | 4 | $563.08 | $553.15 | $2,212.62 | 65 |
| META | 3 | $717.12 | $720.92 | $2,162.76 | 70 |
| MRK | 28 | $82.50 | $83.70 | $2,343.60 | 75 |
| MSFT | 5 | $498.84 | $503.02 | $2,515.10 | 75 |
| NFLX | 1 | $1,279.00 | $1,261.95 | $1,261.95 | 65 |
| NKE | 28 | $72.03 | $72.28 | $2,023.70 | 65 |
| NVDA | 16 | $157.66 | $164.07 | $2,625.12 | 80 |
| ORCL | 9 | $233.27 | $229.25 | $2,063.25 | 70 |
| PEP | 15 | $136.57 | $135.57 | $2,033.55 | 65 |
| PFE | 86 | $25.21 | $25.36 | $2,180.96 | 70 |
| PG | 14 | $160.31 | $153.78 | $2,152.92 | 65 |
| PYPL | 31 | $72.25 | $73.89 | $2,290.59 | 75 |
| QCOM | 14 | $153.83 | $154.29 | $2,160.06 | 65 |
| T | 75 | $27.10 | $27.17 | $2,037.75 | 65 |
| TGT | 20 | $104.94 | $104.88 | $2,097.60 | 65 |
| TSLA | 6 | $288.62 | $316.90 | $1,901.40 | 65 |
| UNH | 7 | $298.51 | $300.52 | $2,103.64 | 65 |
| UNP | 9 | $236.56 | $233.35 | $2,100.19 | 75 |
| V | 6 | $355.85 | $350.44 | $2,102.64 | 65 |
| VZ | 49 | $43.12 | $41.59 | $2,038.15 | 65 |
| WFC | 28 | $82.25 | $83.40 | $2,335.20 | 75 |
| WMT | 21 | $97.38 | $95.76 | $2,010.96 | 65 |
| XOM | 21 | $110.01 | $113.95 | $2,392.95 | 75 |

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
| 2025-07-14 20:09:20 | SELL | BAC | 6 | $47.04 | $-8.83 | 70 |
| 2025-07-14 20:09:20 | SELL | NKE | 1 | $72.28 | $0.24 | 65 |
| 2025-07-14 20:09:20 | SELL | WFC | 3 | $83.40 | $3.11 | 75 |
| 2025-07-14 20:09:20 | BUY | AMZN | 1 | $225.69 | N/A | 80 |
| 2025-07-14 20:09:20 | BUY | AMD | 1 | $146.24 | N/A | 75 |
| 2025-07-14 20:09:20 | BUY | PYPL | 3 | $73.89 | N/A | 75 |
| 2025-07-14 20:09:20 | BUY | WMT | 1 | $95.76 | N/A | 65 |
| 2025-07-14 20:09:20 | BUY | CSCO | 1 | $67.82 | N/A | 70 |
| 2025-07-14 19:50:04 | SELL | AMD | 1 | $146.39 | $11.67 | 65 |
| 2025-07-14 19:50:04 | SELL | NKE | 1 | $72.34 | $0.29 | 65 |
| 2025-07-14 19:50:04 | SELL | WMT | 1 | $95.75 | $-1.63 | 60 |
| 2025-07-14 19:50:04 | SELL | UNP | 1 | $233.79 | $-2.49 | 65 |
| 2025-07-14 19:50:04 | BUY | INTC | 7 | $23.27 | N/A | 65 |
| 2025-07-14 19:50:04 | BUY | BAC | 2 | $47.03 | N/A | 80 |
| 2025-07-14 19:50:04 | BUY | WFC | 1 | $83.43 | N/A | 85 |
| 2025-07-14 19:50:04 | BUY | PG | 1 | $154.15 | N/A | 70 |
| 2025-07-14 19:36:53 | SELL | BAC | 5 | $46.97 | $-7.26 | 75 |
| 2025-07-14 19:36:53 | SELL | PYPL | 1 | $73.89 | $1.75 | 65 |
| 2025-07-14 19:36:53 | SELL | CSCO | 1 | $67.72 | $-0.72 | 65 |
| 2025-07-14 19:36:53 | BUY | GOOGL | 2 | $181.69 | N/A | 85 |
| 2025-07-14 19:36:53 | BUY | AMD | 1 | $146.24 | N/A | 70 |
| 2025-07-14 19:36:53 | BUY | NKE | 2 | $72.30 | N/A | 70 |
| 2025-07-14 19:36:53 | BUY | DIS | 1 | $120.17 | N/A | 70 |
| 2025-07-14 19:36:53 | BUY | WFC | 2 | $83.28 | N/A | 80 |
| 2025-07-14 19:36:53 | BUY | UNP | 1 | $233.67 | N/A | 75 |

<!--TRADE_LOG_END--> 
