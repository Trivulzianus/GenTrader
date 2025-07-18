# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 14:09:31**

| Metric | Value |
|---|---|
| **Total Value** | **$101,258.12** |
| Cash | $1,339.35 |
| Holdings Value | $99,918.77 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.77 | $2,097.70 | 65 |
| ADBE | 6 | $375.23 | $365.73 | $2,194.35 | 65 |
| AMD | 13 | $160.00 | $159.39 | $2,072.07 | 65 |
| AMZN | 11 | $221.89 | $223.82 | $2,462.02 | 75 |
| AVGO | 8 | $275.34 | $284.83 | $2,278.68 | 70 |
| AXP | 7 | $309.18 | $303.92 | $2,127.41 | 65 |
| BA | 10 | $232.01 | $231.31 | $2,313.10 | 70 |
| BAC | 48 | $46.30 | $47.10 | $2,260.80 | 70 |
| C | 29 | $86.64 | $93.22 | $2,703.24 | 85 |
| CAT | 6 | $397.74 | $416.81 | $2,500.83 | 85 |
| COST | 2 | $979.83 | $957.18 | $1,914.37 | 65 |
| CRM | 8 | $267.44 | $260.00 | $2,080.00 | 65 |
| CSCO | 31 | $68.57 | $68.50 | $2,123.65 | 65 |
| CVX | 16 | $146.84 | $152.76 | $2,444.16 | 75 |
| DIS | 18 | $122.74 | $120.96 | $2,177.28 | 65 |
| GOOGL | 13 | $179.34 | $184.31 | $2,396.03 | 70 |
| GS | 3 | $717.52 | $704.20 | $2,112.60 | 75 |
| HD | 6 | $354.18 | $358.04 | $2,148.24 | 65 |
| INTC | 84 | $22.34 | $23.09 | $1,939.56 | 60 |
| JNJ | 14 | $155.97 | $164.37 | $2,301.18 | 70 |
| JPM | 8 | $292.14 | $290.54 | $2,324.32 | 70 |
| KO | 30 | $70.96 | $70.61 | $2,118.15 | 65 |
| LLY | 3 | $781.32 | $770.49 | $2,311.45 | 65 |
| MA | 4 | $563.08 | $552.22 | $2,208.88 | 65 |
| META | 3 | $717.12 | $694.17 | $2,082.51 | 70 |
| MRK | 29 | $82.56 | $81.36 | $2,359.53 | 75 |
| MSFT | 5 | $498.84 | $511.64 | $2,558.20 | 85 |
| NFLX | 1 | $1,208.39 | $1,207.45 | $1,207.45 | 65 |
| NKE | 30 | $71.99 | $72.38 | $2,171.25 | 65 |
| NVDA | 14 | $171.81 | $173.31 | $2,426.41 | 70 |
| ORCL | 9 | $232.91 | $248.41 | $2,235.66 | 65 |
| PEP | 15 | $135.89 | $145.22 | $2,178.30 | 65 |
| PFE | 85 | $25.27 | $24.63 | $2,093.55 | 65 |
| PG | 13 | $151.91 | $155.13 | $2,016.69 | 65 |
| PYPL | 29 | $72.18 | $73.64 | $2,135.41 | 65 |
| QCOM | 14 | $153.83 | $153.83 | $2,153.62 | 65 |
| T | 78 | $27.10 | $26.87 | $2,095.98 | 65 |
| TGT | 20 | $104.82 | $103.78 | $2,075.60 | 65 |
| TSLA | 6 | $318.51 | $328.66 | $1,971.96 | 65 |
| UNH | 7 | $298.51 | $283.66 | $1,985.62 | 60 |
| UNP | 9 | $225.02 | $225.03 | $2,025.32 | 65 |
| V | 6 | $355.85 | $348.18 | $2,089.05 | 65 |
| VZ | 51 | $40.87 | $41.02 | $2,092.28 | 65 |
| WFC | 27 | $78.73 | $79.78 | $2,154.06 | 65 |
| WMT | 22 | $97.29 | $95.14 | $2,092.97 | 65 |
| XOM | 19 | $109.80 | $110.91 | $2,107.29 | 65 |

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
| 2025-07-18 14:09:21 | SELL | NVDA | 1 | $173.35 | $1.44 | 70 |
| 2025-07-18 14:09:21 | SELL | KO | 1 | $70.61 | $-0.35 | 65 |
| 2025-07-18 14:09:21 | SELL | DIS | 1 | $120.96 | $-1.68 | 65 |
| 2025-07-18 14:09:21 | SELL | NKE | 3 | $72.34 | $0.95 | 65 |
| 2025-07-18 14:09:21 | SELL | CSCO | 2 | $68.51 | $-0.11 | 65 |
| 2025-07-18 14:09:21 | BUY | NFLX | 1 | $1,208.39 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | PFE | 1 | $24.62 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | UNP | 9 | $225.02 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | TGT | 1 | $103.78 | N/A | 65 |
| 2025-07-18 14:08:57 | SELL | UNP | 9 | $225.04 | $-110.44 | 65 |
| 2025-07-18 14:08:51 | SELL | NFLX | 1 | $1,207.30 | $-71.70 | 65 |
| 2025-07-18 13:49:22 | SELL | WFC | 2 | $79.81 | $2.01 | 65 |
| 2025-07-18 13:49:22 | SELL | T | 5 | $26.84 | $-1.21 | 65 |
| 2025-07-18 13:49:22 | SELL | TGT | 1 | $103.98 | $-0.85 | 60 |
| 2025-07-18 13:49:22 | BUY | NVDA | 2 | $173.85 | N/A | 85 |
| 2025-07-18 13:49:22 | BUY | KO | 1 | $70.39 | N/A | 70 |
| 2025-07-18 13:49:22 | BUY | MRK | 1 | $81.42 | N/A | 75 |
| 2025-07-18 13:49:22 | BUY | NKE | 4 | $72.58 | N/A | 75 |
| 2025-07-18 13:29:45 | SELL | JPM | 1 | $289.90 | $-2.00 | 70 |
| 2025-07-18 13:29:45 | SELL | KO | 2 | $70.59 | $-0.71 | 65 |
| 2025-07-18 13:29:45 | SELL | PYPL | 3 | $73.86 | $4.56 | 65 |
| 2025-07-18 13:29:45 | SELL | MRK | 1 | $81.52 | $-1.04 | 70 |
| 2025-07-18 13:29:45 | SELL | CSCO | 2 | $68.30 | $-0.50 | 70 |
| 2025-07-18 13:29:45 | BUY | T | 6 | $26.99 | N/A | 70 |
| 2025-07-18 13:05:06 | SELL | INTC | 6 | $22.80 | $2.56 | 60 |

<!--TRADE_LOG_END--> 
