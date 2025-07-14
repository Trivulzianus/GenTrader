# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 15:52:27**

| Metric | Value |
|---|---|
| **Total Value** | **$100,720.31** |
| Cash | $722.23 |
| Holdings Value | $99,998.08 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.65 | $2,086.50 | 65 |
| ADBE | 6 | $375.23 | $364.66 | $2,187.94 | 65 |
| AMD | 14 | $133.89 | $146.27 | $2,047.78 | 70 |
| AMZN | 11 | $221.92 | $225.52 | $2,480.72 | 85 |
| AVGO | 8 | $275.34 | $275.56 | $2,204.46 | 70 |
| AXP | 7 | $325.34 | $320.74 | $2,245.18 | 70 |
| BA | 11 | $214.23 | $230.58 | $2,536.38 | 85 |
| BAC | 46 | $48.75 | $46.85 | $2,155.33 | 70 |
| C | 31 | $86.64 | $87.12 | $2,700.72 | 85 |
| CAT | 6 | $397.74 | $403.37 | $2,420.19 | 70 |
| COST | 2 | $979.83 | $973.02 | $1,946.05 | 65 |
| CRM | 7 | $268.68 | $260.53 | $1,823.71 | 65 |
| CSCO | 31 | $68.48 | $67.39 | $2,088.93 | 65 |
| CVX | 17 | $147.10 | $152.01 | $2,584.25 | 85 |
| DIS | 17 | $122.94 | $120.23 | $2,043.99 | 65 |
| GOOGL | 13 | $179.57 | $180.49 | $2,346.37 | 80 |
| GS | 3 | $717.52 | $712.84 | $2,138.52 | 75 |
| HD | 6 | $372.64 | $367.78 | $2,206.68 | 65 |
| INTC | 87 | $22.38 | $23.11 | $2,010.57 | 65 |
| JNJ | 13 | $155.95 | $156.09 | $2,029.23 | 65 |
| JPM | 9 | $291.63 | $288.29 | $2,594.61 | 85 |
| KO | 29 | $71.03 | $69.70 | $2,021.30 | 65 |
| LLY | 3 | $781.32 | $794.17 | $2,382.52 | 65 |
| MA | 4 | $563.08 | $554.94 | $2,219.76 | 65 |
| META | 3 | $717.12 | $723.70 | $2,171.10 | 75 |
| MRK | 25 | $82.37 | $83.44 | $2,085.88 | 65 |
| MSFT | 5 | $498.84 | $502.82 | $2,514.12 | 85 |
| NFLX | 1 | $1,279.00 | $1,266.81 | $1,266.81 | 65 |
| NKE | 31 | $72.07 | $72.41 | $2,244.77 | 70 |
| NVDA | 16 | $157.68 | $164.99 | $2,639.78 | 85 |
| ORCL | 9 | $233.26 | $229.62 | $2,066.58 | 65 |
| PEP | 15 | $136.57 | $135.16 | $2,027.47 | 65 |
| PFE | 86 | $25.21 | $25.48 | $2,190.86 | 70 |
| PG | 13 | $160.78 | $153.70 | $1,998.10 | 65 |
| PYPL | 30 | $72.23 | $73.48 | $2,204.40 | 70 |
| QCOM | 13 | $153.79 | $153.73 | $1,998.49 | 65 |
| T | 75 | $27.10 | $27.25 | $2,043.61 | 65 |
| TGT | 20 | $104.94 | $104.67 | $2,093.40 | 65 |
| TSLA | 6 | $288.62 | $314.62 | $1,887.72 | 65 |
| UNH | 7 | $298.51 | $299.55 | $2,096.85 | 65 |
| UNP | 9 | $236.60 | $233.06 | $2,097.59 | 70 |
| V | 6 | $355.85 | $350.99 | $2,105.91 | 65 |
| VZ | 49 | $43.12 | $41.69 | $2,042.57 | 65 |
| WFC | 28 | $82.26 | $83.26 | $2,331.16 | 75 |
| WMT | 21 | $97.38 | $95.42 | $2,003.82 | 65 |
| XOM | 21 | $110.01 | $113.59 | $2,385.39 | 75 |

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
| 2025-07-14 15:52:17 | SELL | DIS | 1 | $120.24 | $-2.56 | 65 |
| 2025-07-14 15:52:17 | SELL | MRK | 3 | $83.36 | $2.65 | 65 |
| 2025-07-14 15:52:17 | SELL | PYPL | 1 | $73.48 | $1.21 | 70 |
| 2025-07-14 15:52:17 | BUY | BAC | 2 | $46.85 | N/A | 70 |
| 2025-07-14 15:52:17 | BUY | BA | 1 | $230.60 | N/A | 85 |
| 2025-07-14 15:40:20 | SELL | BAC | 2 | $46.81 | $-3.88 | 65 |
| 2025-07-14 15:40:20 | SELL | NKE | 1 | $72.42 | $0.34 | 70 |
| 2025-07-14 15:40:20 | SELL | MRK | 1 | $83.70 | $1.18 | 75 |
| 2025-07-14 15:40:20 | SELL | PFE | 1 | $25.53 | $0.31 | 70 |
| 2025-07-14 15:40:20 | BUY | INTC | 5 | $23.11 | N/A | 65 |
| 2025-07-14 15:40:20 | BUY | PYPL | 1 | $73.52 | N/A | 75 |
| 2025-07-14 15:26:28 | SELL | PYPL | 1 | $73.74 | $1.46 | 70 |
| 2025-07-14 15:26:28 | SELL | PFE | 5 | $25.46 | $1.18 | 70 |
| 2025-07-14 15:26:28 | SELL | UNP | 1 | $232.40 | $-3.78 | 65 |
| 2025-07-14 15:26:28 | SELL | CSCO | 1 | $67.31 | $-1.14 | 65 |
| 2025-07-14 15:26:28 | BUY | BAC | 2 | $46.81 | N/A | 70 |
| 2025-07-14 15:26:28 | BUY | CVX | 1 | $152.33 | N/A | 85 |
| 2025-07-14 15:09:27 | SELL | INTC | 6 | $23.11 | $4.39 | 60 |
| 2025-07-14 15:09:27 | SELL | BAC | 3 | $46.76 | $-5.84 | 65 |
| 2025-07-14 15:09:27 | BUY | PFE | 6 | $25.44 | N/A | 75 |
| 2025-07-14 15:09:27 | BUY | CSCO | 2 | $67.95 | N/A | 70 |
| 2025-07-14 14:53:08 | SELL | GOOGL | 1 | $180.70 | $1.05 | 75 |
| 2025-07-14 14:53:08 | SELL | AMD | 1 | $144.98 | $10.35 | 65 |
| 2025-07-14 14:53:08 | SELL | INTC | 1 | $23.10 | $0.71 | 65 |
| 2025-07-14 14:53:08 | SELL | TGT | 1 | $103.82 | $-1.06 | 65 |

<!--TRADE_LOG_END--> 
