# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 17:09:26**

| Metric | Value |
|---|---|
| **Total Value** | **$100,526.27** |
| Cash | $435.93 |
| Holdings Value | $100,090.34 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.84 | $2,108.40 | 65 |
| ADBE | 6 | $375.23 | $365.25 | $2,191.47 | 65 |
| AMD | 17 | $146.29 | $155.21 | $2,638.59 | 85 |
| AMZN | 10 | $221.63 | $225.98 | $2,259.80 | 70 |
| AVGO | 8 | $275.34 | $280.26 | $2,242.08 | 70 |
| AXP | 7 | $325.34 | $311.81 | $2,182.70 | 65 |
| BA | 10 | $212.82 | $229.66 | $2,296.64 | 70 |
| BAC | 48 | $48.64 | $46.36 | $2,225.28 | 70 |
| C | 30 | $86.78 | $90.11 | $2,703.30 | 85 |
| CAT | 6 | $397.74 | $403.66 | $2,421.96 | 65 |
| COST | 2 | $979.83 | $969.25 | $1,938.50 | 65 |
| CRM | 8 | $267.44 | $258.75 | $2,070.04 | 65 |
| CSCO | 31 | $68.46 | $67.36 | $2,088.01 | 65 |
| CVX | 18 | $147.21 | $150.43 | $2,707.74 | 85 |
| DIS | 18 | $122.77 | $119.27 | $2,146.86 | 65 |
| GOOGL | 14 | $179.71 | $183.29 | $2,566.06 | 85 |
| GS | 3 | $717.52 | $701.42 | $2,104.26 | 70 |
| HD | 6 | $372.64 | $361.84 | $2,171.04 | 65 |
| INTC | 83 | $22.34 | $23.23 | $1,927.68 | 60 |
| JNJ | 13 | $155.95 | $155.22 | $2,017.92 | 65 |
| JPM | 9 | $291.63 | $286.10 | $2,574.86 | 75 |
| KO | 30 | $70.97 | $69.34 | $2,080.20 | 65 |
| LLY | 3 | $781.32 | $778.61 | $2,335.83 | 65 |
| MA | 4 | $563.08 | $551.96 | $2,207.84 | 65 |
| META | 3 | $717.12 | $715.23 | $2,145.69 | 65 |
| MRK | 25 | $82.54 | $81.59 | $2,039.72 | 65 |
| MSFT | 5 | $498.84 | $506.69 | $2,533.45 | 85 |
| NFLX | 1 | $1,279.00 | $1,255.77 | $1,255.77 | 65 |
| NKE | 29 | $72.04 | $71.97 | $2,087.27 | 65 |
| NVDA | 13 | $171.78 | $170.71 | $2,219.25 | 70 |
| ORCL | 9 | $233.27 | $232.46 | $2,092.10 | 65 |
| PEP | 15 | $136.57 | $134.09 | $2,011.35 | 65 |
| PFE | 83 | $25.22 | $24.73 | $2,052.18 | 65 |
| PG | 14 | $152.15 | $152.54 | $2,135.56 | 70 |
| PYPL | 29 | $72.18 | $73.66 | $2,136.14 | 65 |
| QCOM | 14 | $153.83 | $154.31 | $2,160.34 | 70 |
| T | 77 | $27.09 | $26.88 | $2,069.77 | 65 |
| TGT | 20 | $104.94 | $102.45 | $2,049.00 | 65 |
| TSLA | 6 | $318.51 | $314.75 | $1,888.50 | 60 |
| UNH | 7 | $298.51 | $293.74 | $2,056.18 | 65 |
| UNP | 10 | $236.12 | $232.19 | $2,321.90 | 75 |
| V | 6 | $355.85 | $347.41 | $2,084.46 | 65 |
| VZ | 50 | $43.08 | $41.15 | $2,057.50 | 65 |
| WFC | 27 | $78.88 | $78.50 | $2,119.37 | 65 |
| WMT | 21 | $97.38 | $95.30 | $2,001.30 | 65 |
| XOM | 21 | $109.99 | $112.69 | $2,366.49 | 75 |

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
| 2025-07-15 17:09:19 | SELL | INTC | 6 | $23.23 | $4.98 | 60 |
| 2025-07-15 17:09:19 | BUY | PG | 1 | $152.54 | N/A | 70 |
| 2025-07-15 17:09:19 | BUY | UNP | 1 | $232.19 | N/A | 75 |
| 2025-07-15 17:09:19 | BUY | CVX | 2 | $150.43 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
