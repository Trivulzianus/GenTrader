# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 19:07:35**

| Metric | Value |
|---|---|
| **Total Value** | **$101,150.89** |
| Cash | $3,395.90 |
| Holdings Value | $97,754.98 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $212.75 | $2,127.50 | 70 |
| ADBE | 5 | $377.60 | $377.25 | $1,886.25 | 65 |
| AMD | 15 | $135.93 | $138.96 | $2,084.33 | 70 |
| AMZN | 10 | $221.48 | $220.21 | $2,202.10 | 70 |
| AVGO | 8 | $269.38 | $270.02 | $2,160.16 | 70 |
| AXP | 8 | $324.40 | $326.16 | $2,609.32 | 85 |
| BA | 10 | $212.15 | $210.75 | $2,107.50 | 65 |
| BAC | 45 | $48.69 | $48.60 | $2,187.00 | 70 |
| C | 25 | $86.83 | $86.56 | $2,164.12 | 70 |
| CAT | 6 | $396.45 | $397.87 | $2,387.20 | 75 |
| COST | 2 | $979.83 | $981.85 | $1,963.71 | 65 |
| CRM | 7 | $267.51 | $268.23 | $1,877.58 | 65 |
| CSCO | 34 | $68.37 | $68.53 | $2,330.19 | 75 |
| CVX | 16 | $146.54 | $147.70 | $2,363.20 | 75 |
| DIS | 17 | $122.83 | $122.95 | $2,090.15 | 70 |
| GOOGL | 13 | $177.85 | $178.05 | $2,314.65 | 70 |
| GS | 3 | $717.52 | $713.54 | $2,140.62 | 70 |
| HD | 5 | $372.57 | $373.40 | $1,867.00 | 65 |
| INTC | 92 | $22.33 | $21.98 | $2,022.62 | 65 |
| JNJ | 13 | $155.80 | $155.73 | $2,024.54 | 65 |
| JPM | 9 | $292.49 | $291.25 | $2,621.20 | 85 |
| KO | 29 | $71.03 | $70.91 | $2,056.24 | 65 |
| LLY | 2 | $776.66 | $778.35 | $1,556.70 | 65 |
| MA | 3 | $561.03 | $559.50 | $1,678.50 | 65 |
| META | 3 | $717.12 | $713.81 | $2,141.43 | 85 |
| MRK | 28 | $82.40 | $82.30 | $2,304.26 | 75 |
| MSFT | 4 | $491.43 | $490.18 | $1,960.70 | 70 |
| NFLX | 1 | $1,279.00 | $1,280.99 | $1,280.99 | 70 |
| NKE | 29 | $75.72 | $76.74 | $2,225.47 | 70 |
| NVDA | 16 | $156.09 | $156.62 | $2,506.00 | 85 |
| ORCL | 10 | $225.04 | $226.25 | $2,262.50 | 75 |
| PEP | 15 | $136.59 | $136.44 | $2,046.60 | 65 |
| PFE | 86 | $25.33 | $25.29 | $2,174.94 | 70 |
| PG | 12 | $160.76 | $160.79 | $1,929.48 | 65 |
| PYPL | 30 | $76.82 | $76.24 | $2,287.20 | 75 |
| QCOM | 16 | $161.59 | $162.70 | $2,603.20 | 85 |
| T | 80 | $28.51 | $28.43 | $2,274.00 | 75 |
| TGT | 20 | $105.06 | $105.43 | $2,108.60 | 65 |
| TSLA | 6 | $313.02 | $315.77 | $1,894.60 | 65 |
| UNH | 6 | $315.70 | $308.69 | $1,852.14 | 65 |
| UNP | 9 | $236.50 | $237.30 | $2,135.70 | 70 |
| V | 5 | $352.10 | $352.71 | $1,763.57 | 65 |
| VZ | 47 | $43.74 | $43.73 | $2,055.31 | 65 |
| WFC | 31 | $82.28 | $82.17 | $2,547.12 | 80 |
| WMT | 23 | $97.33 | $97.59 | $2,244.68 | 70 |
| XOM | 21 | $109.93 | $111.15 | $2,334.10 | 75 |

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
| 2025-07-02 18:44:32 | SELL | VZ | 6 | $43.73 | $-0.08 | 65 |
| 2025-07-02 18:44:32 | BUY | PFE | 6 | $25.29 | N/A | 70 |
| 2025-07-02 18:44:32 | BUY | WFC | 3 | $82.04 | N/A | 85 |
| 2025-07-02 18:44:32 | BUY | T | 6 | $28.41 | N/A | 70 |
| 2025-07-02 18:27:27 | SELL | PFE | 6 | $25.32 | $-0.02 | 65 |
| 2025-07-02 18:27:27 | BUY | INTC | 6 | $21.93 | N/A | 65 |
| 2025-07-02 18:27:27 | BUY | NKE | 5 | $76.44 | N/A | 85 |
| 2025-07-02 18:27:27 | BUY | VZ | 6 | $43.68 | N/A | 75 |
| 2025-07-02 18:27:27 | BUY | CSCO | 2 | $68.47 | N/A | 75 |

<!--TRADE_LOG_END--> 
