# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 16:57:12**

| Metric | Value |
|---|---|
| **Total Value** | **$100,555.54** |
| Cash | $982.17 |
| Holdings Value | $99,573.37 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.55 | $2,105.50 | 65 |
| ADBE | 6 | $375.23 | $365.25 | $2,191.47 | 65 |
| AMD | 17 | $146.29 | $155.06 | $2,635.93 | 85 |
| AMZN | 10 | $221.63 | $225.97 | $2,259.70 | 70 |
| AVGO | 8 | $275.34 | $280.36 | $2,242.88 | 65 |
| AXP | 7 | $325.34 | $312.07 | $2,184.49 | 65 |
| BA | 10 | $212.82 | $230.13 | $2,301.30 | 70 |
| BAC | 48 | $48.64 | $46.47 | $2,230.32 | 70 |
| C | 30 | $86.78 | $90.20 | $2,706.00 | 85 |
| CAT | 6 | $397.74 | $403.89 | $2,423.37 | 65 |
| COST | 2 | $979.83 | $970.11 | $1,940.22 | 65 |
| CRM | 8 | $267.44 | $259.13 | $2,073.04 | 65 |
| CSCO | 31 | $68.46 | $67.39 | $2,088.93 | 65 |
| CVX | 16 | $146.81 | $150.54 | $2,408.64 | 75 |
| DIS | 18 | $122.77 | $119.42 | $2,149.56 | 70 |
| GOOGL | 14 | $179.71 | $182.89 | $2,560.47 | 85 |
| GS | 3 | $717.52 | $703.16 | $2,109.48 | 75 |
| HD | 6 | $372.64 | $362.26 | $2,173.59 | 65 |
| INTC | 89 | $22.40 | $23.23 | $2,067.91 | 65 |
| JNJ | 13 | $155.95 | $155.21 | $2,017.73 | 65 |
| JPM | 9 | $291.63 | $286.85 | $2,581.61 | 85 |
| KO | 30 | $70.97 | $69.42 | $2,082.63 | 65 |
| LLY | 3 | $781.32 | $777.34 | $2,332.02 | 65 |
| MA | 4 | $563.08 | $551.53 | $2,206.14 | 65 |
| META | 3 | $717.12 | $715.58 | $2,146.74 | 65 |
| MRK | 25 | $82.54 | $81.52 | $2,037.88 | 65 |
| MSFT | 5 | $498.84 | $506.60 | $2,533.00 | 85 |
| NFLX | 1 | $1,279.00 | $1,255.31 | $1,255.31 | 65 |
| NKE | 29 | $72.04 | $72.03 | $2,088.87 | 65 |
| NVDA | 13 | $171.78 | $170.70 | $2,219.10 | 70 |
| ORCL | 9 | $233.27 | $232.29 | $2,090.61 | 65 |
| PEP | 15 | $136.57 | $133.97 | $2,009.62 | 65 |
| PFE | 83 | $25.22 | $24.73 | $2,053.01 | 65 |
| PG | 13 | $152.12 | $152.51 | $1,982.69 | 65 |
| PYPL | 29 | $72.18 | $73.63 | $2,135.27 | 65 |
| QCOM | 14 | $153.83 | $154.34 | $2,160.69 | 65 |
| T | 77 | $27.09 | $26.90 | $2,071.66 | 65 |
| TGT | 20 | $104.94 | $102.67 | $2,053.40 | 65 |
| TSLA | 6 | $318.51 | $313.53 | $1,881.19 | 65 |
| UNH | 7 | $298.51 | $294.10 | $2,058.70 | 65 |
| UNP | 9 | $236.55 | $232.15 | $2,089.31 | 70 |
| V | 6 | $355.85 | $347.24 | $2,083.43 | 70 |
| VZ | 50 | $43.08 | $41.18 | $2,058.87 | 65 |
| WFC | 27 | $78.88 | $78.56 | $2,121.12 | 65 |
| WMT | 21 | $97.38 | $95.34 | $2,002.23 | 65 |
| XOM | 21 | $109.99 | $112.75 | $2,367.75 | 75 |

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
| 2025-07-15 16:57:02 | SELL | NKE | 1 | $71.99 | $-0.05 | 65 |
| 2025-07-15 16:57:02 | SELL | WFC | 1 | $78.58 | $-0.28 | 65 |
| 2025-07-15 16:57:02 | SELL | BA | 1 | $230.25 | $15.84 | 70 |
| 2025-07-15 16:57:02 | SELL | CVX | 1 | $150.56 | $3.53 | 75 |
| 2025-07-15 16:57:02 | BUY | BAC | 4 | $46.47 | N/A | 70 |
| 2025-07-15 16:57:02 | BUY | INTC | 1 | $23.25 | N/A | 65 |
| 2025-07-15 16:57:02 | BUY | DIS | 1 | $119.46 | N/A | 70 |
| 2025-07-15 16:44:17 | SELL | AMZN | 1 | $226.16 | $4.11 | 70 |
| 2025-07-15 16:44:17 | SELL | UNP | 1 | $232.39 | $-3.75 | 65 |
| 2025-07-15 16:44:17 | BUY | PYPL | 1 | $73.66 | N/A | 70 |
| 2025-07-15 16:44:17 | BUY | WFC | 1 | $83.43 | N/A | 75 |
| 2025-07-15 16:44:17 | BUY | CVX | 1 | $150.73 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
