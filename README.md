# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 19:24:16**

| Metric | Value |
|---|---|
| **Total Value** | **$101,167.17** |
| Cash | $3,085.19 |
| Holdings Value | $98,081.97 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.38 | $2,123.75 | 70 |
| ADBE | 5 | $377.60 | $378.02 | $1,890.12 | 65 |
| AMD | 15 | $135.93 | $138.99 | $2,084.85 | 70 |
| AMZN | 10 | $221.48 | $220.13 | $2,201.30 | 75 |
| AVGO | 8 | $269.38 | $269.38 | $2,155.04 | 70 |
| AXP | 8 | $324.40 | $326.34 | $2,610.72 | 80 |
| BA | 10 | $212.15 | $211.42 | $2,114.17 | 65 |
| BAC | 55 | $48.69 | $48.66 | $2,676.57 | 85 |
| C | 27 | $86.81 | $86.67 | $2,340.03 | 75 |
| CAT | 6 | $396.45 | $398.11 | $2,388.63 | 65 |
| COST | 2 | $979.83 | $981.33 | $1,962.65 | 65 |
| CRM | 7 | $267.51 | $268.88 | $1,882.19 | 65 |
| CSCO | 34 | $68.37 | $68.46 | $2,327.73 | 75 |
| CVX | 16 | $146.54 | $147.79 | $2,364.64 | 75 |
| DIS | 17 | $122.83 | $122.83 | $2,088.03 | 65 |
| GOOGL | 13 | $177.85 | $178.28 | $2,317.64 | 75 |
| GS | 3 | $717.52 | $714.40 | $2,143.20 | 75 |
| HD | 6 | $372.64 | $372.95 | $2,237.70 | 75 |
| INTC | 86 | $22.35 | $22.00 | $1,892.43 | 60 |
| JNJ | 13 | $155.80 | $155.49 | $2,021.37 | 65 |
| JPM | 9 | $292.49 | $291.68 | $2,625.08 | 85 |
| KO | 29 | $71.03 | $70.80 | $2,053.05 | 65 |
| LLY | 2 | $776.66 | $777.83 | $1,555.65 | 65 |
| MA | 3 | $561.03 | $559.93 | $1,679.79 | 65 |
| META | 3 | $717.12 | $714.16 | $2,142.48 | 70 |
| MRK | 28 | $82.40 | $82.25 | $2,303.00 | 75 |
| MSFT | 4 | $491.43 | $490.12 | $1,960.50 | 70 |
| NFLX | 1 | $1,279.00 | $1,281.37 | $1,281.37 | 65 |
| NKE | 29 | $75.72 | $76.55 | $2,219.80 | 70 |
| NVDA | 15 | $156.03 | $156.88 | $2,353.27 | 70 |
| ORCL | 10 | $225.04 | $227.56 | $2,275.60 | 70 |
| PEP | 15 | $136.59 | $136.25 | $2,043.68 | 65 |
| PFE | 87 | $25.33 | $25.30 | $2,200.93 | 70 |
| PG | 12 | $160.76 | $160.59 | $1,927.08 | 65 |
| PYPL | 30 | $76.82 | $76.35 | $2,290.50 | 75 |
| QCOM | 15 | $161.52 | $162.68 | $2,440.20 | 75 |
| T | 73 | $28.53 | $28.36 | $2,069.91 | 65 |
| TGT | 20 | $105.06 | $105.34 | $2,106.83 | 65 |
| TSLA | 6 | $313.02 | $315.70 | $1,894.20 | 65 |
| UNH | 6 | $315.70 | $309.94 | $1,859.61 | 65 |
| UNP | 9 | $236.50 | $237.16 | $2,134.44 | 65 |
| V | 5 | $352.10 | $352.68 | $1,763.40 | 65 |
| VZ | 47 | $43.74 | $43.66 | $2,052.02 | 65 |
| WFC | 31 | $82.28 | $82.19 | $2,547.74 | 80 |
| WMT | 22 | $97.33 | $97.46 | $2,144.08 | 65 |
| XOM | 21 | $109.93 | $111.19 | $2,334.99 | 75 |

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
| 2025-07-02 19:24:10 | SELL | NVDA | 1 | $156.90 | $0.81 | 70 |
| 2025-07-02 19:24:10 | SELL | INTC | 6 | $22.00 | $-1.92 | 60 |
| 2025-07-02 19:24:10 | SELL | WMT | 1 | $97.45 | $0.11 | 65 |
| 2025-07-02 19:24:10 | SELL | T | 7 | $28.36 | $-1.06 | 65 |
| 2025-07-02 19:24:10 | SELL | QCOM | 1 | $162.67 | $1.08 | 75 |
| 2025-07-02 19:24:10 | BUY | BAC | 10 | $48.67 | N/A | 85 |
| 2025-07-02 19:24:10 | BUY | HD | 1 | $373.00 | N/A | 75 |
| 2025-07-02 19:24:10 | BUY | PFE | 1 | $25.30 | N/A | 70 |
| 2025-07-02 19:24:10 | BUY | C | 2 | $86.64 | N/A | 75 |
| 2025-07-02 19:07:25 | SELL | GOOGL | 1 | $178.06 | $0.20 | 70 |
| 2025-07-02 19:07:25 | SELL | BAC | 4 | $48.60 | $-0.33 | 70 |
| 2025-07-02 19:07:25 | SELL | NKE | 2 | $76.76 | $1.94 | 70 |
| 2025-07-02 19:07:25 | SELL | WFC | 1 | $82.15 | $-0.12 | 80 |
| 2025-07-02 19:07:25 | SELL | CVX | 1 | $147.71 | $1.10 | 75 |
| 2025-07-02 19:07:25 | BUY | NVDA | 1 | $156.65 | N/A | 85 |
| 2025-07-02 19:07:25 | BUY | C | 1 | $86.57 | N/A | 70 |
| 2025-07-02 19:07:25 | BUY | ORCL | 1 | $226.20 | N/A | 75 |
| 2025-07-02 19:07:25 | BUY | QCOM | 1 | $162.73 | N/A | 85 |
| 2025-07-02 19:07:25 | BUY | T | 3 | $28.88 | N/A | 75 |
| 2025-07-02 18:56:13 | SELL | AMD | 1 | $138.74 | $2.63 | 65 |
| 2025-07-02 18:56:13 | BUY | NVDA | 1 | $153.30 | N/A | 75 |
| 2025-07-02 18:56:13 | BUY | CVX | 1 | $147.60 | N/A | 85 |
| 2025-07-02 18:44:32 | SELL | NVDA | 2 | $156.80 | $0.97 | 70 |
| 2025-07-02 18:44:32 | SELL | BAC | 5 | $48.55 | $-0.62 | 75 |
| 2025-07-02 18:44:32 | SELL | NKE | 3 | $76.62 | $2.27 | 75 |

<!--TRADE_LOG_END--> 
