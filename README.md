# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 19:36:22**

| Metric | Value |
|---|---|
| **Total Value** | **$101,115.28** |
| Cash | $2,595.81 |
| Holdings Value | $98,519.47 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.09 | $2,120.85 | 65 |
| ADBE | 5 | $377.60 | $377.79 | $1,888.95 | 65 |
| AMD | 15 | $135.93 | $138.50 | $2,077.50 | 70 |
| AMZN | 10 | $221.48 | $220.11 | $2,201.10 | 75 |
| AVGO | 8 | $269.38 | $269.40 | $2,155.20 | 65 |
| AXP | 8 | $324.40 | $326.53 | $2,612.24 | 85 |
| BA | 10 | $212.15 | $211.37 | $2,113.73 | 65 |
| BAC | 55 | $48.69 | $48.62 | $2,674.10 | 85 |
| C | 24 | $86.84 | $86.61 | $2,078.64 | 65 |
| CAT | 6 | $396.45 | $398.12 | $2,388.75 | 75 |
| COST | 2 | $979.83 | $982.36 | $1,964.72 | 65 |
| CRM | 7 | $267.51 | $268.98 | $1,882.86 | 65 |
| CSCO | 32 | $68.36 | $68.53 | $2,193.12 | 70 |
| CVX | 16 | $146.54 | $147.50 | $2,360.00 | 75 |
| DIS | 17 | $122.83 | $122.91 | $2,089.47 | 70 |
| GOOGL | 13 | $177.85 | $178.43 | $2,319.59 | 75 |
| GS | 3 | $717.52 | $715.93 | $2,147.79 | 70 |
| HD | 6 | $372.64 | $372.85 | $2,237.10 | 70 |
| INTC | 92 | $22.32 | $21.92 | $2,017.07 | 65 |
| JNJ | 13 | $155.80 | $155.56 | $2,022.28 | 65 |
| JPM | 9 | $292.49 | $291.92 | $2,627.28 | 85 |
| KO | 29 | $71.03 | $70.84 | $2,054.39 | 65 |
| LLY | 2 | $776.66 | $777.24 | $1,554.47 | 65 |
| MA | 3 | $561.03 | $560.34 | $1,681.01 | 65 |
| META | 3 | $717.12 | $714.20 | $2,142.60 | 75 |
| MRK | 27 | $82.41 | $82.05 | $2,215.22 | 70 |
| MSFT | 4 | $491.43 | $490.30 | $1,961.20 | 70 |
| NFLX | 1 | $1,279.00 | $1,284.81 | $1,284.81 | 65 |
| NKE | 34 | $75.86 | $76.54 | $2,602.36 | 85 |
| NVDA | 16 | $156.09 | $156.88 | $2,510.08 | 85 |
| ORCL | 10 | $225.04 | $227.16 | $2,271.60 | 65 |
| PEP | 15 | $136.59 | $136.17 | $2,042.55 | 65 |
| PFE | 87 | $25.33 | $25.27 | $2,198.92 | 70 |
| PG | 12 | $160.76 | $160.71 | $1,928.54 | 60 |
| PYPL | 30 | $76.82 | $76.34 | $2,290.23 | 75 |
| QCOM | 15 | $161.52 | $162.06 | $2,430.90 | 75 |
| T | 76 | $28.52 | $28.43 | $2,161.06 | 70 |
| TGT | 20 | $105.06 | $105.14 | $2,102.80 | 70 |
| TSLA | 6 | $313.02 | $313.06 | $1,878.36 | 65 |
| UNH | 7 | $314.75 | $308.86 | $2,162.02 | 70 |
| UNP | 9 | $236.50 | $236.76 | $2,130.84 | 70 |
| V | 5 | $352.10 | $353.75 | $1,768.78 | 65 |
| VZ | 47 | $43.74 | $43.63 | $2,050.84 | 65 |
| WFC | 31 | $82.28 | $82.18 | $2,547.43 | 80 |
| WMT | 21 | $97.32 | $97.61 | $2,049.85 | 65 |
| XOM | 21 | $109.93 | $110.78 | $2,326.28 | 75 |

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

<!--TRADE_LOG_END--> 
