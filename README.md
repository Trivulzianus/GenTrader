# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 19:50:17**

| Metric | Value |
|---|---|
| **Total Value** | **$101,125.27** |
| Cash | $2,403.12 |
| Holdings Value | $98,722.15 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.32 | $2,123.25 | 70 |
| ADBE | 5 | $377.60 | $377.95 | $1,889.75 | 65 |
| AMD | 15 | $135.93 | $138.33 | $2,074.95 | 70 |
| AMZN | 10 | $221.48 | $219.93 | $2,199.25 | 70 |
| AVGO | 8 | $269.38 | $269.55 | $2,156.40 | 70 |
| AXP | 8 | $324.40 | $326.17 | $2,609.36 | 80 |
| BA | 10 | $212.15 | $211.70 | $2,116.97 | 65 |
| BAC | 54 | $48.69 | $48.67 | $2,628.45 | 85 |
| C | 30 | $86.80 | $86.67 | $2,599.96 | 85 |
| CAT | 6 | $396.45 | $398.07 | $2,388.42 | 75 |
| COST | 2 | $979.83 | $982.95 | $1,965.90 | 65 |
| CRM | 7 | $267.51 | $268.58 | $1,880.06 | 65 |
| CSCO | 33 | $68.36 | $68.58 | $2,263.14 | 75 |
| CVX | 16 | $146.54 | $147.86 | $2,365.76 | 75 |
| DIS | 17 | $122.83 | $123.02 | $2,091.34 | 70 |
| GOOGL | 14 | $177.88 | $178.20 | $2,494.80 | 85 |
| GS | 3 | $717.52 | $715.96 | $2,147.88 | 70 |
| HD | 6 | $372.64 | $372.67 | $2,236.02 | 65 |
| INTC | 85 | $22.36 | $21.84 | $1,856.82 | 60 |
| JNJ | 13 | $155.80 | $155.74 | $2,024.56 | 65 |
| JPM | 9 | $292.49 | $291.99 | $2,627.91 | 85 |
| KO | 29 | $71.03 | $70.89 | $2,055.81 | 65 |
| LLY | 2 | $776.66 | $777.49 | $1,554.97 | 65 |
| MA | 3 | $561.03 | $560.44 | $1,681.32 | 65 |
| META | 3 | $717.12 | $713.30 | $2,139.90 | 75 |
| MRK | 28 | $82.40 | $82.04 | $2,297.12 | 75 |
| MSFT | 4 | $491.43 | $491.04 | $1,964.16 | 75 |
| NFLX | 1 | $1,279.00 | $1,283.51 | $1,283.51 | 70 |
| NKE | 34 | $75.86 | $76.67 | $2,606.78 | 85 |
| NVDA | 15 | $156.02 | $157.19 | $2,357.92 | 75 |
| ORCL | 9 | $224.73 | $227.95 | $2,051.55 | 65 |
| PEP | 15 | $136.59 | $136.18 | $2,042.70 | 65 |
| PFE | 86 | $25.33 | $25.29 | $2,174.94 | 70 |
| PG | 12 | $160.76 | $161.02 | $1,932.26 | 65 |
| PYPL | 30 | $76.82 | $76.17 | $2,285.10 | 75 |
| QCOM | 15 | $161.52 | $161.76 | $2,426.40 | 75 |
| T | 71 | $28.53 | $28.36 | $2,013.91 | 65 |
| TGT | 20 | $105.06 | $105.16 | $2,103.10 | 70 |
| TSLA | 6 | $313.02 | $313.62 | $1,881.72 | 65 |
| UNH | 7 | $314.75 | $307.28 | $2,150.96 | 70 |
| UNP | 9 | $236.50 | $236.91 | $2,132.24 | 65 |
| V | 5 | $352.10 | $353.54 | $1,767.70 | 65 |
| VZ | 47 | $43.74 | $43.54 | $2,046.39 | 65 |
| WFC | 31 | $82.28 | $82.28 | $2,550.68 | 85 |
| WMT | 22 | $97.33 | $97.67 | $2,148.74 | 70 |
| XOM | 21 | $109.93 | $111.02 | $2,331.32 | 75 |

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
| 2025-07-02 19:50:11 | SELL | NVDA | 1 | $157.05 | $0.96 | 75 |
| 2025-07-02 19:50:11 | SELL | INTC | 7 | $21.85 | $-3.29 | 60 |
| 2025-07-02 19:50:11 | SELL | BAC | 1 | $48.69 | $-0.00 | 85 |
| 2025-07-02 19:50:11 | SELL | PFE | 1 | $25.28 | $-0.04 | 70 |
| 2025-07-02 19:50:11 | SELL | ORCL | 1 | $227.85 | $2.81 | 65 |
| 2025-07-02 19:50:11 | SELL | T | 5 | $28.38 | $-0.74 | 65 |
| 2025-07-02 19:50:11 | BUY | GOOGL | 1 | $178.27 | N/A | 85 |
| 2025-07-02 19:50:11 | BUY | WMT | 1 | $97.63 | N/A | 70 |
| 2025-07-02 19:50:11 | BUY | MRK | 1 | $82.01 | N/A | 75 |
| 2025-07-02 19:50:11 | BUY | C | 6 | $86.65 | N/A | 85 |
| 2025-07-02 19:50:11 | BUY | CSCO | 1 | $68.57 | N/A | 75 |
| 2025-07-02 19:36:16 | SELL | WMT | 1 | $97.60 | $0.27 | 65 |
| 2025-07-02 19:36:16 | SELL | C | 3 | $86.61 | $-0.60 | 65 |
| 2025-07-02 19:36:16 | SELL | MRK | 1 | $82.06 | $-0.34 | 70 |
| 2025-07-02 19:36:16 | SELL | CSCO | 2 | $68.53 | $0.33 | 70 |
| 2025-07-02 19:36:16 | BUY | UNH | 1 | $309.08 | N/A | 70 |
| 2025-07-02 19:36:16 | BUY | INTC | 6 | $21.92 | N/A | 65 |
| 2025-07-02 19:36:16 | BUY | NKE | 5 | $76.62 | N/A | 85 |
| 2025-07-02 19:36:16 | BUY | NVDA | 1 | $156.91 | N/A | 85 |
| 2025-07-02 19:36:16 | BUY | T | 3 | $28.43 | N/A | 70 |
| 2025-07-02 19:24:10 | SELL | NVDA | 1 | $156.90 | $0.81 | 70 |
| 2025-07-02 19:24:10 | SELL | INTC | 6 | $22.00 | $-1.92 | 60 |
| 2025-07-02 19:24:10 | SELL | WMT | 1 | $97.45 | $0.11 | 65 |
| 2025-07-02 19:24:10 | SELL | T | 7 | $28.36 | $-1.06 | 65 |
| 2025-07-02 19:24:10 | SELL | QCOM | 1 | $162.67 | $1.08 | 75 |

<!--TRADE_LOG_END--> 
