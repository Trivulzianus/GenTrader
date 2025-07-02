# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 18:11:33**

| Metric | Value |
|---|---|
| **Total Value** | **$101,034.77** |
| Cash | $3,949.10 |
| Holdings Value | $97,085.67 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $211.56 | $2,115.65 | 70 |
| ADBE | 5 | $377.60 | $374.17 | $1,870.83 | 65 |
| AMD | 16 | $136.11 | $138.62 | $2,217.92 | 70 |
| AMZN | 10 | $221.48 | $220.28 | $2,202.80 | 75 |
| AVGO | 8 | $269.38 | $271.24 | $2,169.88 | 70 |
| AXP | 8 | $324.40 | $325.31 | $2,602.48 | 85 |
| BA | 10 | $212.15 | $211.11 | $2,111.10 | 65 |
| BAC | 54 | $48.67 | $48.48 | $2,617.65 | 85 |
| C | 24 | $86.84 | $86.32 | $2,071.68 | 65 |
| CAT | 6 | $396.45 | $396.27 | $2,377.62 | 85 |
| COST | 2 | $979.83 | $982.51 | $1,965.02 | 65 |
| CRM | 7 | $267.51 | $267.33 | $1,871.30 | 65 |
| CSCO | 32 | $68.36 | $68.55 | $2,193.44 | 70 |
| CVX | 15 | $146.48 | $147.19 | $2,207.85 | 75 |
| DIS | 17 | $122.83 | $122.59 | $2,084.03 | 65 |
| GOOGL | 14 | $177.86 | $178.59 | $2,500.33 | 75 |
| GS | 3 | $717.52 | $713.50 | $2,140.50 | 85 |
| HD | 5 | $372.57 | $372.54 | $1,862.70 | 65 |
| INTC | 86 | $22.35 | $21.94 | $1,886.84 | 60 |
| JNJ | 13 | $155.80 | $155.69 | $2,023.90 | 65 |
| JPM | 9 | $292.49 | $291.08 | $2,619.72 | 85 |
| KO | 29 | $71.03 | $70.94 | $2,057.40 | 65 |
| LLY | 2 | $776.66 | $777.61 | $1,555.22 | 65 |
| MA | 3 | $561.03 | $558.61 | $1,675.83 | 65 |
| META | 3 | $717.12 | $716.27 | $2,148.81 | 75 |
| MRK | 28 | $82.40 | $82.12 | $2,299.50 | 75 |
| MSFT | 4 | $491.43 | $490.37 | $1,961.48 | 70 |
| NFLX | 1 | $1,279.00 | $1,279.62 | $1,279.62 | 65 |
| NKE | 29 | $75.76 | $76.47 | $2,217.77 | 70 |
| NVDA | 16 | $156.31 | $156.92 | $2,510.80 | 85 |
| ORCL | 9 | $224.91 | $224.70 | $2,022.30 | 65 |
| PEP | 15 | $136.59 | $136.62 | $2,049.33 | 65 |
| PFE | 86 | $25.33 | $25.29 | $2,174.51 | 70 |
| PG | 12 | $160.76 | $160.89 | $1,930.68 | 65 |
| PYPL | 30 | $76.82 | $76.10 | $2,283.00 | 75 |
| QCOM | 15 | $161.52 | $162.16 | $2,432.32 | 75 |
| T | 71 | $28.50 | $28.41 | $2,017.11 | 65 |
| TGT | 20 | $105.06 | $105.14 | $2,102.70 | 65 |
| TSLA | 6 | $313.02 | $315.01 | $1,890.09 | 65 |
| UNH | 6 | $315.70 | $312.77 | $1,876.65 | 65 |
| UNP | 9 | $236.50 | $235.93 | $2,123.33 | 65 |
| V | 5 | $352.10 | $351.96 | $1,759.80 | 65 |
| VZ | 47 | $43.75 | $43.63 | $2,050.84 | 65 |
| WFC | 29 | $82.30 | $81.96 | $2,376.84 | 75 |
| WMT | 23 | $97.33 | $97.79 | $2,249.17 | 70 |
| XOM | 21 | $109.93 | $110.83 | $2,327.33 | 75 |

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
| 2025-07-02 18:11:25 | SELL | INTC | 6 | $21.93 | $-2.37 | 60 |
| 2025-07-02 18:11:25 | SELL | NKE | 5 | $76.38 | $2.60 | 70 |
| 2025-07-02 18:11:25 | SELL | C | 2 | $86.29 | $-1.00 | 65 |
| 2025-07-02 18:11:25 | BUY | NVDA | 2 | $157.03 | N/A | 85 |
| 2025-07-02 18:11:25 | BUY | BAC | 5 | $48.49 | N/A | 85 |
| 2025-07-02 17:51:22 | SELL | NVDA | 2 | $157.23 | $1.77 | 70 |
| 2025-07-02 17:51:22 | SELL | BAC | 5 | $48.47 | $-0.99 | 75 |
| 2025-07-02 17:51:22 | SELL | WFC | 3 | $81.96 | $-0.91 | 75 |
| 2025-07-02 17:51:22 | SELL | ORCL | 1 | $225.57 | $0.60 | 65 |
| 2025-07-02 17:51:22 | SELL | CVX | 1 | $146.91 | $0.40 | 70 |
| 2025-07-02 17:51:22 | BUY | GOOGL | 1 | $178.42 | N/A | 85 |
| 2025-07-02 17:51:22 | BUY | QCOM | 1 | $161.93 | N/A | 80 |
| 2025-07-02 17:39:14 | SELL | KO | 1 | $71.01 | $-0.01 | 65 |
| 2025-07-02 17:39:14 | SELL | CSCO | 2 | $68.53 | $0.33 | 70 |
| 2025-07-02 17:39:14 | BUY | BAC | 9 | $48.46 | N/A | 85 |
| 2025-07-02 17:39:14 | BUY | C | 1 | $86.39 | N/A | 75 |
| 2025-07-02 17:39:14 | BUY | WFC | 3 | $81.89 | N/A | 85 |
| 2025-07-02 17:25:50 | SELL | BAC | 9 | $48.44 | $-2.07 | 70 |
| 2025-07-02 17:25:50 | SELL | WFC | 3 | $82.00 | $-0.83 | 75 |
| 2025-07-02 17:25:50 | BUY | NVDA | 1 | $157.29 | N/A | 85 |
| 2025-07-02 17:25:50 | BUY | INTC | 7 | $21.91 | N/A | 65 |
| 2025-07-02 17:25:50 | BUY | KO | 2 | $71.03 | N/A | 70 |
| 2025-07-02 17:25:50 | BUY | XOM | 1 | $110.32 | N/A | 75 |
| 2025-07-02 17:25:50 | BUY | WMT | 2 | $97.74 | N/A | 75 |
| 2025-07-02 17:25:50 | BUY | C | 1 | $86.56 | N/A | 70 |

<!--TRADE_LOG_END--> 
