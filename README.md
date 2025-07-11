# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 18:56:22**

| Metric | Value |
|---|---|
| **Total Value** | **$100,829.80** |
| Cash | $1,406.45 |
| Holdings Value | $99,423.35 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $211.17 | $2,111.65 | 70 |
| ADBE | 5 | $377.60 | $363.54 | $1,817.70 | 65 |
| AMD | 15 | $134.66 | $146.88 | $2,203.20 | 70 |
| AMZN | 11 | $221.97 | $225.78 | $2,483.53 | 85 |
| AVGO | 8 | $275.34 | $274.74 | $2,197.92 | 70 |
| AXP | 7 | $325.34 | $320.72 | $2,245.04 | 70 |
| BA | 11 | $213.84 | $227.40 | $2,501.40 | 75 |
| BAC | 47 | $48.70 | $46.79 | $2,199.01 | 70 |
| C | 26 | $86.66 | $86.92 | $2,260.05 | 70 |
| CAT | 5 | $396.39 | $406.64 | $2,033.20 | 70 |
| COST | 2 | $979.83 | $966.68 | $1,933.36 | 65 |
| CRM | 7 | $268.68 | $258.52 | $1,809.67 | 65 |
| CSCO | 33 | $68.39 | $68.04 | $2,245.32 | 70 |
| CVX | 17 | $147.16 | $155.78 | $2,648.26 | 85 |
| DIS | 17 | $122.96 | $120.38 | $2,046.46 | 65 |
| GOOGL | 13 | $179.61 | $180.61 | $2,347.93 | 75 |
| GS | 3 | $717.52 | $705.06 | $2,115.18 | 70 |
| HD | 6 | $372.64 | $369.83 | $2,218.97 | 65 |
| INTC | 87 | $22.36 | $23.66 | $2,058.00 | 65 |
| JNJ | 13 | $155.89 | $156.87 | $2,039.31 | 65 |
| JPM | 8 | $292.23 | $287.07 | $2,296.56 | 75 |
| KO | 29 | $71.03 | $70.01 | $2,030.29 | 65 |
| LLY | 3 | $781.32 | $784.49 | $2,353.46 | 65 |
| MA | 4 | $563.08 | $548.54 | $2,194.18 | 65 |
| META | 3 | $717.12 | $719.00 | $2,157.00 | 75 |
| MRK | 25 | $82.29 | $83.20 | $2,080.12 | 65 |
| MSFT | 5 | $498.84 | $503.02 | $2,515.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,243.19 | $1,243.19 | 65 |
| NKE | 31 | $75.77 | $72.73 | $2,254.63 | 70 |
| NVDA | 16 | $157.38 | $165.62 | $2,649.92 | 85 |
| ORCL | 9 | $233.26 | $230.81 | $2,077.34 | 70 |
| PEP | 15 | $136.57 | $134.86 | $2,022.90 | 65 |
| PFE | 85 | $25.20 | $25.66 | $2,181.10 | 70 |
| PG | 13 | $160.78 | $157.01 | $2,041.14 | 65 |
| PYPL | 28 | $72.13 | $72.17 | $2,020.90 | 65 |
| QCOM | 13 | $162.18 | $158.36 | $2,058.70 | 65 |
| T | 76 | $27.11 | $27.02 | $2,053.90 | 65 |
| TGT | 20 | $104.91 | $104.61 | $2,092.30 | 65 |
| TSLA | 6 | $288.62 | $311.73 | $1,870.39 | 65 |
| UNH | 7 | $298.51 | $301.42 | $2,109.94 | 65 |
| UNP | 10 | $236.18 | $235.03 | $2,350.25 | 70 |
| V | 6 | $355.85 | $345.90 | $2,075.40 | 65 |
| VZ | 49 | $43.12 | $41.73 | $2,044.53 | 65 |
| WFC | 29 | $82.28 | $82.64 | $2,396.41 | 75 |
| WMT | 22 | $97.25 | $94.45 | $2,078.01 | 65 |
| XOM | 23 | $110.46 | $115.67 | $2,660.53 | 85 |

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
| 2025-07-11 18:56:16 | SELL | AMD | 2 | $146.87 | $21.55 | 70 |
| 2025-07-11 18:56:16 | SELL | CSCO | 1 | $68.04 | $-0.34 | 70 |
| 2025-07-11 18:56:16 | SELL | TGT | 1 | $104.61 | $-0.29 | 65 |
| 2025-07-11 18:56:16 | BUY | XOM | 2 | $115.69 | N/A | 85 |
| 2025-07-11 18:56:16 | BUY | PFE | 5 | $25.66 | N/A | 70 |
| 2025-07-11 18:56:16 | BUY | CVX | 1 | $155.79 | N/A | 85 |
| 2025-07-11 18:44:46 | SELL | AMD | 1 | $146.93 | $10.23 | 75 |
| 2025-07-11 18:44:46 | SELL | C | 4 | $86.81 | $0.52 | 70 |
| 2025-07-11 18:44:46 | SELL | CVX | 1 | $155.67 | $8.51 | 75 |
| 2025-07-11 18:44:46 | BUY | KO | 2 | $70.01 | N/A | 65 |
| 2025-07-11 18:44:46 | BUY | CSCO | 3 | $68.04 | N/A | 75 |
| 2025-07-11 18:44:46 | BUY | TGT | 1 | $104.63 | N/A | 70 |
| 2025-07-11 18:27:16 | SELL | JPM | 1 | $286.65 | $-4.96 | 70 |
| 2025-07-11 18:27:16 | SELL | KO | 2 | $70.00 | $-2.06 | 60 |
| 2025-07-11 18:27:16 | SELL | NKE | 1 | $72.65 | $-3.03 | 70 |
| 2025-07-11 18:27:16 | SELL | PFE | 5 | $25.64 | $2.19 | 65 |
| 2025-07-11 18:27:16 | SELL | CSCO | 3 | $67.87 | $-1.50 | 65 |
| 2025-07-11 18:27:16 | BUY | AMD | 3 | $146.78 | N/A | 85 |
| 2025-07-11 18:27:16 | BUY | PYPL | 28 | $72.13 | N/A | 65 |
| 2025-07-11 18:27:16 | BUY | C | 5 | $86.68 | N/A | 85 |
| 2025-07-11 18:27:16 | BUY | BA | 1 | $227.60 | N/A | 85 |
| 2025-07-11 18:27:00 | SELL | PYPL | 31 | $72.18 | $-136.62 | 75 |
| 2025-07-11 18:10:51 | SELL | AMD | 1 | $146.83 | $11.39 | 70 |
| 2025-07-11 18:10:51 | BUY | PFE | 5 | $25.64 | N/A | 70 |
| 2025-07-11 18:10:51 | BUY | CSCO | 3 | $67.85 | N/A | 75 |

<!--TRADE_LOG_END--> 
