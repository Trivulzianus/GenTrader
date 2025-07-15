# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 18:47:11**

| Metric | Value |
|---|---|
| **Total Value** | **$100,657.79** |
| Cash | $189.07 |
| Holdings Value | $100,468.72 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.98 | $2,109.79 | 65 |
| ADBE | 6 | $375.23 | $365.88 | $2,195.31 | 65 |
| AMD | 17 | $146.29 | $155.09 | $2,636.45 | 85 |
| AMZN | 11 | $222.06 | $226.85 | $2,495.35 | 85 |
| AVGO | 8 | $275.34 | $281.85 | $2,254.80 | 70 |
| AXP | 7 | $325.34 | $312.12 | $2,184.88 | 65 |
| BA | 11 | $214.54 | $231.82 | $2,550.02 | 85 |
| BAC | 45 | $46.29 | $46.27 | $2,081.93 | 65 |
| C | 30 | $86.78 | $91.09 | $2,732.70 | 85 |
| CAT | 6 | $397.74 | $405.34 | $2,432.04 | 70 |
| COST | 2 | $979.83 | $968.92 | $1,937.84 | 65 |
| CRM | 8 | $267.44 | $258.34 | $2,066.72 | 65 |
| CSCO | 31 | $68.46 | $67.44 | $2,090.49 | 65 |
| CVX | 16 | $146.78 | $151.03 | $2,416.40 | 75 |
| DIS | 18 | $122.77 | $119.54 | $2,151.72 | 65 |
| GOOGL | 14 | $179.71 | $184.01 | $2,576.14 | 85 |
| GS | 3 | $717.52 | $703.27 | $2,109.81 | 70 |
| HD | 6 | $372.64 | $360.51 | $2,163.09 | 65 |
| INTC | 89 | $22.39 | $23.11 | $2,056.79 | 65 |
| JNJ | 13 | $155.95 | $155.33 | $2,019.29 | 65 |
| JPM | 9 | $291.63 | $286.69 | $2,580.26 | 85 |
| KO | 30 | $70.97 | $69.38 | $2,081.46 | 65 |
| LLY | 3 | $781.32 | $771.93 | $2,315.79 | 65 |
| MA | 4 | $563.08 | $554.06 | $2,216.24 | 65 |
| META | 3 | $717.12 | $716.25 | $2,148.75 | 70 |
| MRK | 27 | $82.47 | $81.53 | $2,201.31 | 70 |
| MSFT | 5 | $498.84 | $507.91 | $2,539.57 | 85 |
| NFLX | 1 | $1,279.00 | $1,258.00 | $1,258.00 | 65 |
| NKE | 30 | $72.03 | $71.86 | $2,155.95 | 70 |
| NVDA | 13 | $171.77 | $170.64 | $2,218.32 | 70 |
| ORCL | 9 | $233.15 | $234.13 | $2,107.17 | 65 |
| PEP | 15 | $136.57 | $134.08 | $2,011.20 | 65 |
| PFE | 84 | $25.25 | $24.61 | $2,066.82 | 65 |
| PG | 13 | $152.11 | $152.75 | $1,985.68 | 60 |
| PYPL | 28 | $72.12 | $73.83 | $2,067.10 | 65 |
| QCOM | 14 | $153.83 | $155.13 | $2,171.82 | 65 |
| T | 76 | $27.09 | $27.04 | $2,054.66 | 65 |
| TGT | 20 | $104.94 | $102.47 | $2,049.40 | 65 |
| TSLA | 6 | $318.51 | $313.75 | $1,882.52 | 65 |
| UNH | 7 | $298.51 | $291.40 | $2,039.80 | 65 |
| UNP | 10 | $236.14 | $232.04 | $2,320.45 | 75 |
| V | 6 | $355.85 | $349.24 | $2,095.44 | 65 |
| VZ | 50 | $43.08 | $41.33 | $2,066.41 | 65 |
| WFC | 28 | $78.87 | $78.36 | $2,193.94 | 70 |
| WMT | 21 | $97.38 | $95.44 | $2,004.13 | 65 |
| XOM | 21 | $110.02 | $113.09 | $2,374.99 | 75 |

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
| 2025-07-15 18:47:03 | SELL | BAC | 2 | $46.28 | $-0.03 | 65 |
| 2025-07-15 18:47:03 | SELL | XOM | 2 | $113.09 | $5.61 | 75 |
| 2025-07-15 18:47:03 | SELL | PFE | 3 | $24.61 | $-1.85 | 65 |
| 2025-07-15 18:47:03 | SELL | PG | 1 | $152.73 | $0.58 | 60 |
| 2025-07-15 18:47:03 | SELL | ORCL | 1 | $234.16 | $0.91 | 65 |
| 2025-07-15 18:47:03 | SELL | T | 1 | $27.03 | $-0.06 | 65 |
| 2025-07-15 18:47:03 | BUY | NKE | 1 | $71.88 | N/A | 70 |
| 2025-07-15 18:47:03 | BUY | MRK | 2 | $81.54 | N/A | 70 |
| 2025-07-15 18:47:03 | BUY | WFC | 1 | $78.35 | N/A | 70 |
| 2025-07-15 18:47:03 | BUY | BA | 1 | $231.79 | N/A | 85 |
| 2025-07-15 18:47:03 | BUY | UNP | 1 | $232.04 | N/A | 75 |
| 2025-07-15 18:28:07 | SELL | NKE | 2 | $71.78 | $-0.49 | 65 |
| 2025-07-15 18:28:07 | SELL | CVX | 1 | $151.40 | $4.35 | 75 |
| 2025-07-15 18:28:07 | BUY | BAC | 3 | $47.07 | N/A | 70 |
| 2025-07-15 18:28:07 | BUY | XOM | 2 | $113.38 | N/A | 85 |
| 2025-07-15 18:28:07 | BUY | PFE | 4 | $25.35 | N/A | 70 |
| 2025-07-15 18:11:30 | BUY | CVX | 1 | $151.10 | N/A | 85 |
| 2025-07-15 17:51:39 | SELL | WFC | 1 | $78.10 | $-0.77 | 65 |
| 2025-07-15 17:51:39 | SELL | UNP | 1 | $231.92 | $-4.21 | 65 |
| 2025-07-15 17:51:39 | SELL | CVX | 1 | $150.41 | $3.40 | 75 |
| 2025-07-15 17:51:39 | BUY | BAC | 44 | $46.24 | N/A | 65 |
| 2025-07-15 17:51:39 | BUY | NKE | 1 | $71.61 | N/A | 70 |
| 2025-07-15 17:51:17 | SELL | BAC | 45 | $46.24 | $-115.05 | 65 |
| 2025-07-15 17:40:07 | SELL | NVDA | 2 | $170.66 | $-1.93 | 70 |
| 2025-07-15 17:40:07 | SELL | PYPL | 1 | $73.84 | $1.66 | 65 |

<!--TRADE_LOG_END--> 
