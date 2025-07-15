# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 16:44:26**

| Metric | Value |
|---|---|
| **Total Value** | **$100,619.26** |
| Cash | $779.39 |
| Holdings Value | $99,839.86 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.46 | $2,104.60 | 70 |
| ADBE | 6 | $375.23 | $365.35 | $2,192.07 | 65 |
| AMD | 17 | $146.29 | $155.23 | $2,638.93 | 85 |
| AMZN | 10 | $221.63 | $226.18 | $2,261.81 | 70 |
| AVGO | 8 | $275.34 | $281.12 | $2,248.96 | 70 |
| AXP | 7 | $325.34 | $312.50 | $2,187.48 | 65 |
| BA | 11 | $214.40 | $230.49 | $2,535.34 | 75 |
| BAC | 44 | $48.83 | $46.56 | $2,048.86 | 65 |
| C | 30 | $86.78 | $90.40 | $2,712.00 | 85 |
| CAT | 6 | $397.74 | $404.43 | $2,426.58 | 70 |
| COST | 2 | $979.83 | $970.38 | $1,940.77 | 65 |
| CRM | 8 | $267.44 | $258.91 | $2,071.28 | 65 |
| CSCO | 31 | $68.46 | $67.42 | $2,090.17 | 65 |
| CVX | 17 | $147.03 | $150.75 | $2,562.75 | 85 |
| DIS | 17 | $122.96 | $119.41 | $2,029.88 | 65 |
| GOOGL | 14 | $179.71 | $182.93 | $2,560.95 | 85 |
| GS | 3 | $717.52 | $704.84 | $2,114.52 | 85 |
| HD | 6 | $372.64 | $362.63 | $2,175.78 | 65 |
| INTC | 88 | $22.39 | $23.26 | $2,046.88 | 65 |
| JNJ | 13 | $155.95 | $155.03 | $2,015.45 | 65 |
| JPM | 9 | $291.63 | $286.41 | $2,577.69 | 85 |
| KO | 30 | $70.97 | $69.39 | $2,081.85 | 65 |
| LLY | 3 | $781.32 | $775.96 | $2,327.87 | 65 |
| MA | 4 | $563.08 | $551.50 | $2,206.00 | 65 |
| META | 3 | $717.12 | $716.75 | $2,150.25 | 65 |
| MRK | 25 | $82.54 | $81.46 | $2,036.50 | 65 |
| MSFT | 5 | $498.84 | $506.62 | $2,533.12 | 85 |
| NFLX | 1 | $1,279.00 | $1,256.75 | $1,256.75 | 65 |
| NKE | 30 | $72.04 | $71.97 | $2,159.16 | 70 |
| NVDA | 13 | $171.78 | $171.25 | $2,226.32 | 70 |
| ORCL | 9 | $233.27 | $232.25 | $2,090.25 | 65 |
| PEP | 15 | $136.57 | $133.94 | $2,009.10 | 65 |
| PFE | 83 | $25.22 | $24.70 | $2,050.10 | 65 |
| PG | 13 | $152.12 | $152.59 | $1,983.73 | 65 |
| PYPL | 29 | $72.18 | $73.66 | $2,135.99 | 70 |
| QCOM | 14 | $153.83 | $154.71 | $2,165.94 | 65 |
| T | 77 | $27.09 | $26.86 | $2,068.61 | 65 |
| TGT | 20 | $104.94 | $102.88 | $2,057.60 | 65 |
| TSLA | 6 | $318.51 | $314.27 | $1,885.65 | 65 |
| UNH | 7 | $298.51 | $294.31 | $2,060.20 | 65 |
| UNP | 9 | $236.55 | $232.39 | $2,091.51 | 65 |
| V | 6 | $355.85 | $347.62 | $2,085.69 | 65 |
| VZ | 50 | $43.08 | $41.13 | $2,056.49 | 65 |
| WFC | 28 | $78.87 | $78.79 | $2,206.12 | 75 |
| WMT | 21 | $97.38 | $95.39 | $2,003.19 | 65 |
| XOM | 21 | $109.99 | $112.81 | $2,369.11 | 75 |

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
| 2025-07-15 15:40:17 | SELL | NVDA | 1 | $171.33 | $-0.42 | 70 |
| 2025-07-15 15:40:17 | SELL | INTC | 6 | $23.37 | $5.90 | 60 |
| 2025-07-15 15:40:17 | SELL | PYPL | 1 | $73.64 | $1.41 | 65 |
| 2025-07-15 15:40:17 | SELL | WFC | 1 | $78.91 | $0.19 | 65 |
| 2025-07-15 15:40:17 | BUY | GOOGL | 1 | $183.45 | N/A | 85 |
| 2025-07-15 15:40:17 | BUY | BAC | 3 | $46.65 | N/A | 70 |
| 2025-07-15 15:26:50 | SELL | GOOGL | 1 | $183.84 | $4.10 | 75 |

<!--TRADE_LOG_END--> 
