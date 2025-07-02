# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 15:51:33**

| Metric | Value |
|---|---|
| **Total Value** | **$101,111.07** |
| Cash | $6,232.54 |
| Holdings Value | $94,878.53 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.39 | $211.37 | $2,113.70 | 70 |
| ADBE | 5 | $377.60 | $377.60 | $1,888.00 | 65 |
| AMD | 16 | $136.11 | $138.55 | $2,216.80 | 70 |
| AMZN | 10 | $221.48 | $221.48 | $2,214.80 | 75 |
| AVGO | 8 | $269.38 | $269.32 | $2,154.56 | 70 |
| AXP | 6 | $324.35 | $324.23 | $1,945.38 | 70 |
| BA | 9 | $212.09 | $212.13 | $1,909.17 | 65 |
| BAC | 45 | $48.69 | $48.69 | $2,190.83 | 70 |
| C | 27 | $86.79 | $86.81 | $2,343.87 | 75 |
| CAT | 5 | $396.55 | $396.55 | $1,982.73 | 75 |
| COST | 2 | $979.83 | $979.83 | $1,959.66 | 65 |
| CRM | 7 | $267.51 | $267.54 | $1,872.78 | 65 |
| CSCO | 32 | $68.36 | $68.36 | $2,187.68 | 70 |
| CVX | 16 | $146.52 | $146.49 | $2,343.84 | 75 |
| DIS | 16 | $122.83 | $122.78 | $1,964.48 | 65 |
| GOOGL | 13 | $177.82 | $177.75 | $2,310.75 | 75 |
| GS | 3 | $717.52 | $717.52 | $2,152.56 | 70 |
| HD | 5 | $372.57 | $372.56 | $1,862.83 | 70 |
| INTC | 84 | $22.36 | $22.38 | $1,879.50 | 60 |
| JNJ | 13 | $155.80 | $155.81 | $2,025.53 | 65 |
| JPM | 9 | $292.49 | $292.45 | $2,632.09 | 85 |
| KO | 28 | $71.03 | $71.02 | $1,988.42 | 65 |
| LLY | 2 | $776.66 | $776.66 | $1,553.32 | 65 |
| MA | 3 | $561.03 | $560.77 | $1,682.32 | 65 |
| META | 3 | $717.12 | $717.55 | $2,152.65 | 75 |
| MRK | 28 | $82.43 | $82.41 | $2,307.51 | 75 |
| MSFT | 4 | $491.43 | $491.42 | $1,965.66 | 75 |
| NFLX | 1 | $1,279.00 | $1,279.00 | $1,279.00 | 65 |
| NKE | 33 | $75.85 | $75.80 | $2,501.40 | 80 |
| NVDA | 14 | $156.51 | $156.48 | $2,190.72 | 70 |
| ORCL | 9 | $225.00 | $224.84 | $2,023.56 | 70 |
| PEP | 15 | $136.59 | $136.58 | $2,048.75 | 65 |
| PFE | 81 | $25.33 | $25.33 | $2,051.88 | 65 |
| PG | 12 | $160.76 | $160.74 | $1,928.82 | 65 |
| PYPL | 30 | $76.82 | $76.83 | $2,304.75 | 75 |
| QCOM | 14 | $161.49 | $161.47 | $2,260.58 | 75 |
| T | 72 | $28.50 | $28.50 | $2,052.36 | 65 |
| TGT | 19 | $105.07 | $105.06 | $1,996.05 | 65 |
| TSLA | 6 | $313.02 | $312.88 | $1,877.28 | 65 |
| UNH | 6 | $315.70 | $315.86 | $1,895.16 | 65 |
| UNP | 8 | $236.59 | $236.57 | $1,892.56 | 65 |
| V | 5 | $352.10 | $352.00 | $1,760.00 | 65 |
| VZ | 46 | $43.75 | $43.73 | $2,011.81 | 65 |
| WFC | 30 | $82.29 | $82.29 | $2,468.70 | 80 |
| WMT | 24 | $97.30 | $97.32 | $2,335.63 | 75 |
| XOM | 20 | $109.91 | $109.91 | $2,198.10 | 70 |

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
| 2025-07-02 15:51:25 | BUY | MSFT | 4 | $491.43 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | GOOGL | 13 | $177.82 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | AMZN | 10 | $221.48 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | NVDA | 14 | $156.51 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | META | 3 | $717.12 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | JNJ | 13 | $155.80 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | AAPL | 10 | $211.39 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | TSLA | 6 | $313.02 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | JPM | 9 | $292.49 | N/A | 85 |
| 2025-07-02 15:51:25 | BUY | V | 5 | $352.10 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | UNH | 6 | $315.70 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | BAC | 45 | $48.69 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | ADBE | 5 | $377.60 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | MA | 3 | $561.03 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | CRM | 7 | $267.51 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | NFLX | 1 | $1,279.00 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | INTC | 84 | $22.36 | N/A | 60 |
| 2025-07-02 15:51:25 | BUY | GS | 3 | $717.52 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | XOM | 20 | $109.91 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | AMD | 16 | $136.11 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | KO | 28 | $71.03 | N/A | 65 |
| 2025-07-02 15:51:25 | BUY | NKE | 33 | $75.85 | N/A | 80 |
| 2025-07-02 15:51:25 | BUY | WMT | 24 | $97.30 | N/A | 75 |
| 2025-07-02 15:51:25 | BUY | HD | 5 | $372.57 | N/A | 70 |
| 2025-07-02 15:51:25 | BUY | PFE | 81 | $25.33 | N/A | 65 |

<!--TRADE_LOG_END--> 
