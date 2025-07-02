# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 20:09:09**

| Metric | Value |
|---|---|
| **Total Value** | **$101,222.56** |
| Cash | $2,532.82 |
| Holdings Value | $98,689.74 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.44 | $2,124.40 | 70 |
| ADBE | 5 | $377.60 | $378.47 | $1,892.35 | 65 |
| AMD | 15 | $135.93 | $138.52 | $2,077.80 | 70 |
| AMZN | 10 | $221.48 | $219.92 | $2,199.20 | 70 |
| AVGO | 8 | $269.38 | $269.90 | $2,159.20 | 70 |
| AXP | 8 | $324.40 | $325.63 | $2,605.04 | 75 |
| BA | 10 | $212.15 | $211.93 | $2,119.30 | 65 |
| BAC | 54 | $48.69 | $48.69 | $2,628.99 | 85 |
| C | 26 | $86.81 | $86.74 | $2,255.24 | 70 |
| CAT | 6 | $396.45 | $398.40 | $2,390.40 | 85 |
| COST | 2 | $979.83 | $982.36 | $1,964.72 | 65 |
| CRM | 7 | $267.51 | $269.13 | $1,883.91 | 65 |
| CSCO | 34 | $68.37 | $68.59 | $2,332.06 | 75 |
| CVX | 16 | $146.54 | $147.96 | $2,367.36 | 75 |
| DIS | 17 | $122.83 | $123.00 | $2,091.00 | 70 |
| GOOGL | 14 | $177.88 | $178.64 | $2,500.96 | 75 |
| GS | 3 | $717.52 | $716.07 | $2,148.21 | 75 |
| HD | 6 | $372.64 | $371.93 | $2,231.58 | 65 |
| INTC | 92 | $22.32 | $21.88 | $2,012.96 | 65 |
| JNJ | 13 | $155.80 | $155.55 | $2,022.15 | 65 |
| JPM | 8 | $292.56 | $291.94 | $2,335.52 | 75 |
| KO | 29 | $71.03 | $70.94 | $2,057.12 | 65 |
| LLY | 2 | $776.66 | $779.15 | $1,558.30 | 65 |
| MA | 3 | $561.03 | $561.59 | $1,684.77 | 65 |
| META | 3 | $717.12 | $713.57 | $2,140.71 | 75 |
| MRK | 28 | $82.40 | $82.38 | $2,306.64 | 75 |
| MSFT | 4 | $491.43 | $491.09 | $1,964.36 | 75 |
| NFLX | 1 | $1,279.00 | $1,284.86 | $1,284.86 | 70 |
| NKE | 34 | $75.86 | $76.43 | $2,598.62 | 85 |
| NVDA | 14 | $155.93 | $157.25 | $2,201.50 | 70 |
| ORCL | 11 | $225.68 | $229.98 | $2,529.78 | 85 |
| PEP | 15 | $136.59 | $136.48 | $2,047.20 | 65 |
| PFE | 86 | $25.33 | $25.33 | $2,178.38 | 70 |
| PG | 12 | $160.76 | $161.09 | $1,933.08 | 65 |
| PYPL | 30 | $76.82 | $76.31 | $2,289.30 | 75 |
| QCOM | 15 | $161.52 | $162.32 | $2,434.80 | 75 |
| T | 71 | $28.53 | $28.31 | $2,010.01 | 65 |
| TGT | 20 | $105.06 | $105.45 | $2,109.00 | 70 |
| TSLA | 6 | $313.02 | $315.65 | $1,893.90 | 60 |
| UNH | 7 | $314.75 | $307.64 | $2,153.48 | 65 |
| UNP | 9 | $236.50 | $237.08 | $2,133.72 | 65 |
| V | 5 | $352.10 | $354.38 | $1,771.90 | 65 |
| VZ | 47 | $43.74 | $43.59 | $2,048.97 | 65 |
| WFC | 32 | $82.28 | $82.34 | $2,635.04 | 85 |
| WMT | 21 | $97.32 | $97.60 | $2,049.60 | 65 |
| XOM | 21 | $109.93 | $111.06 | $2,332.36 | 75 |

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
| 2025-07-02 20:09:02 | SELL | JPM | 1 | $291.94 | $-0.55 | 75 |
| 2025-07-02 20:09:02 | SELL | NVDA | 1 | $157.25 | $1.23 | 70 |
| 2025-07-02 20:09:02 | SELL | WMT | 1 | $97.60 | $0.27 | 65 |
| 2025-07-02 20:09:02 | SELL | C | 4 | $86.74 | $-0.24 | 70 |
| 2025-07-02 20:09:02 | BUY | INTC | 7 | $21.88 | N/A | 65 |
| 2025-07-02 20:09:02 | BUY | WFC | 1 | $82.35 | N/A | 85 |
| 2025-07-02 20:09:02 | BUY | CSCO | 1 | $68.59 | N/A | 75 |
| 2025-07-02 20:09:02 | BUY | ORCL | 2 | $229.98 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
