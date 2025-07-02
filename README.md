# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 17:39:20**

| Metric | Value |
|---|---|
| **Total Value** | **$100,999.33** |
| Cash | $2,984.69 |
| Holdings Value | $98,014.64 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $210.85 | $2,108.52 | 70 |
| ADBE | 5 | $377.60 | $374.18 | $1,870.90 | 65 |
| AMD | 16 | $136.11 | $138.78 | $2,220.56 | 70 |
| AMZN | 10 | $221.48 | $220.21 | $2,202.10 | 75 |
| AVGO | 8 | $269.38 | $270.51 | $2,164.12 | 70 |
| AXP | 8 | $324.40 | $325.14 | $2,601.12 | 80 |
| BA | 10 | $212.15 | $211.68 | $2,116.80 | 65 |
| BAC | 54 | $48.67 | $48.47 | $2,617.11 | 85 |
| C | 26 | $86.80 | $86.39 | $2,246.01 | 75 |
| CAT | 6 | $396.45 | $396.26 | $2,377.56 | 85 |
| COST | 2 | $979.83 | $984.02 | $1,968.05 | 65 |
| CRM | 7 | $267.51 | $266.90 | $1,868.33 | 65 |
| CSCO | 32 | $68.36 | $68.52 | $2,192.64 | 70 |
| CVX | 16 | $146.51 | $146.85 | $2,349.58 | 75 |
| DIS | 17 | $122.83 | $122.62 | $2,084.54 | 70 |
| GOOGL | 13 | $177.82 | $178.44 | $2,319.66 | 75 |
| GS | 3 | $717.52 | $714.67 | $2,144.02 | 70 |
| HD | 5 | $372.57 | $372.36 | $1,861.80 | 65 |
| INTC | 92 | $22.33 | $21.89 | $2,013.88 | 65 |
| JNJ | 13 | $155.80 | $155.78 | $2,025.20 | 65 |
| JPM | 9 | $292.49 | $291.59 | $2,624.31 | 85 |
| KO | 29 | $71.03 | $71.00 | $2,059.00 | 65 |
| LLY | 2 | $776.66 | $778.66 | $1,557.33 | 65 |
| MA | 3 | $561.03 | $560.01 | $1,680.05 | 65 |
| META | 3 | $717.12 | $715.62 | $2,146.85 | 70 |
| MRK | 28 | $82.40 | $82.25 | $2,303.00 | 75 |
| MSFT | 4 | $491.43 | $490.44 | $1,961.76 | 70 |
| NFLX | 1 | $1,279.00 | $1,277.48 | $1,277.48 | 65 |
| NKE | 34 | $75.85 | $75.97 | $2,582.81 | 85 |
| NVDA | 16 | $156.34 | $157.07 | $2,513.15 | 85 |
| ORCL | 10 | $224.98 | $225.28 | $2,252.80 | 70 |
| PEP | 15 | $136.59 | $136.63 | $2,049.45 | 65 |
| PFE | 86 | $25.33 | $25.25 | $2,171.91 | 70 |
| PG | 12 | $160.76 | $160.91 | $1,930.92 | 65 |
| PYPL | 30 | $76.82 | $76.02 | $2,280.46 | 75 |
| QCOM | 14 | $161.49 | $161.67 | $2,263.38 | 75 |
| T | 71 | $28.50 | $28.43 | $2,018.71 | 65 |
| TGT | 20 | $105.06 | $104.58 | $2,091.60 | 65 |
| TSLA | 6 | $313.02 | $314.36 | $1,886.16 | 65 |
| UNH | 6 | $315.70 | $313.31 | $1,879.86 | 65 |
| UNP | 9 | $236.50 | $236.19 | $2,125.76 | 65 |
| V | 5 | $352.10 | $352.62 | $1,763.08 | 65 |
| VZ | 47 | $43.75 | $43.67 | $2,052.72 | 65 |
| WFC | 32 | $82.27 | $81.89 | $2,620.48 | 85 |
| WMT | 23 | $97.33 | $97.72 | $2,247.56 | 75 |
| XOM | 21 | $109.93 | $110.55 | $2,321.55 | 75 |

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
| 2025-07-02 17:08:18 | SELL | INTC | 7 | $22.10 | $-1.65 | 60 |
| 2025-07-02 17:08:18 | SELL | WMT | 2 | $97.50 | $0.36 | 65 |
| 2025-07-02 17:08:18 | SELL | C | 6 | $86.64 | $-0.86 | 65 |
| 2025-07-02 17:08:18 | SELL | VZ | 2 | $43.60 | $-0.29 | 65 |
| 2025-07-02 17:08:18 | BUY | NVDA | 1 | $153.30 | N/A | 75 |
| 2025-07-02 17:08:18 | BUY | NKE | 2 | $76.04 | N/A | 85 |
| 2025-07-02 17:08:18 | BUY | PFE | 5 | $25.22 | N/A | 70 |
| 2025-07-02 17:08:18 | BUY | MRK | 3 | $81.81 | N/A | 75 |
| 2025-07-02 16:55:51 | SELL | NVDA | 2 | $157.33 | $1.47 | 70 |
| 2025-07-02 16:55:51 | SELL | MRK | 3 | $82.13 | $-0.91 | 65 |
| 2025-07-02 16:55:51 | SELL | T | 1 | $28.52 | $0.02 | 65 |
| 2025-07-02 16:55:51 | SELL | CVX | 1 | $146.48 | $-0.03 | 75 |

<!--TRADE_LOG_END--> 
