# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 15:08:46**

| Metric | Value |
|---|---|
| **Total Value** | **$100,941.71** |
| Cash | $887.12 |
| Holdings Value | $100,054.59 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $211.10 | $2,111.00 | 70 |
| ADBE | 5 | $377.60 | $386.43 | $1,932.12 | 65 |
| AMD | 16 | $135.69 | $138.95 | $2,223.20 | 70 |
| AMZN | 10 | $221.61 | $220.81 | $2,208.10 | 70 |
| AVGO | 8 | $275.34 | $273.98 | $2,191.80 | 70 |
| AXP | 8 | $324.24 | $320.81 | $2,566.48 | 85 |
| BA | 9 | $211.84 | $215.57 | $1,940.13 | 60 |
| BAC | 47 | $48.73 | $47.21 | $2,218.87 | 70 |
| C | 30 | $86.57 | $85.86 | $2,575.80 | 85 |
| CAT | 6 | $397.86 | $394.93 | $2,369.55 | 75 |
| COST | 2 | $979.83 | $987.67 | $1,975.34 | 65 |
| CRM | 8 | $268.33 | $276.10 | $2,208.80 | 65 |
| CSCO | 34 | $68.37 | $68.42 | $2,326.45 | 75 |
| CVX | 17 | $146.95 | $151.68 | $2,578.48 | 85 |
| DIS | 18 | $122.81 | $122.45 | $2,204.10 | 70 |
| GOOGL | 12 | $179.60 | $175.14 | $2,101.68 | 65 |
| GS | 3 | $717.52 | $697.37 | $2,092.10 | 75 |
| HD | 6 | $372.64 | $368.74 | $2,212.44 | 65 |
| INTC | 87 | $22.26 | $23.45 | $2,039.74 | 65 |
| JNJ | 13 | $155.81 | $156.54 | $2,035.08 | 65 |
| JPM | 9 | $291.61 | $282.87 | $2,545.83 | 75 |
| KO | 29 | $71.03 | $70.04 | $2,031.16 | 65 |
| LLY | 2 | $776.66 | $791.25 | $1,582.51 | 65 |
| MA | 4 | $563.08 | $562.73 | $2,250.90 | 65 |
| META | 3 | $717.12 | $717.28 | $2,151.84 | 65 |
| MRK | 29 | $82.43 | $82.16 | $2,382.64 | 75 |
| MSFT | 5 | $498.84 | $495.58 | $2,477.92 | 85 |
| NFLX | 1 | $1,279.00 | $1,262.08 | $1,262.08 | 65 |
| NKE | 29 | $75.98 | $74.52 | $2,160.93 | 70 |
| NVDA | 14 | $156.29 | $159.15 | $2,228.10 | 70 |
| ORCL | 9 | $233.41 | $235.10 | $2,115.90 | 70 |
| PEP | 15 | $136.57 | $135.48 | $2,032.20 | 65 |
| PFE | 85 | $25.28 | $25.93 | $2,204.47 | 70 |
| PG | 13 | $160.77 | $158.57 | $2,061.41 | 65 |
| PYPL | 31 | $76.64 | $75.24 | $2,332.44 | 75 |
| QCOM | 14 | $161.75 | $161.40 | $2,259.60 | 75 |
| T | 73 | $28.54 | $28.11 | $2,051.66 | 65 |
| TGT | 20 | $104.90 | $101.92 | $2,038.40 | 65 |
| TSLA | 6 | $288.62 | $302.17 | $1,812.99 | 65 |
| UNH | 7 | $314.75 | $308.25 | $2,157.75 | 65 |
| UNP | 11 | $236.72 | $238.63 | $2,624.93 | 85 |
| V | 6 | $355.95 | $355.83 | $2,135.01 | 65 |
| VZ | 47 | $43.72 | $43.09 | $2,025.23 | 65 |
| WFC | 29 | $82.34 | $81.40 | $2,360.60 | 75 |
| WMT | 21 | $97.43 | $97.06 | $2,038.26 | 65 |
| XOM | 23 | $110.28 | $113.85 | $2,618.55 | 85 |

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
| 2025-07-08 15:08:40 | SELL | BAC | 3 | $47.21 | $-4.29 | 70 |
| 2025-07-08 15:08:40 | SELL | INTC | 1 | $23.42 | $1.15 | 65 |
| 2025-07-08 15:08:40 | SELL | WMT | 1 | $96.97 | $-0.44 | 65 |
| 2025-07-08 15:08:40 | SELL | PFE | 1 | $25.92 | $0.64 | 70 |
| 2025-07-08 15:08:40 | SELL | BA | 2 | $215.10 | $5.32 | 60 |
| 2025-07-08 15:08:40 | BUY | XOM | 2 | $113.91 | N/A | 85 |
| 2025-07-08 15:08:40 | BUY | C | 3 | $85.85 | N/A | 85 |
| 2025-07-08 15:08:40 | BUY | CSCO | 2 | $68.39 | N/A | 75 |
| 2025-07-08 15:08:40 | BUY | CVX | 1 | $151.76 | N/A | 85 |
| 2025-07-08 15:08:40 | BUY | UNP | 1 | $238.57 | N/A | 85 |
| 2025-07-08 14:52:28 | SELL | NVDA | 2 | $158.90 | $4.55 | 70 |
| 2025-07-08 14:52:28 | SELL | XOM | 1 | $113.88 | $3.77 | 75 |
| 2025-07-08 14:52:28 | SELL | WMT | 1 | $96.75 | $-0.63 | 65 |
| 2025-07-08 14:52:28 | SELL | PFE | 4 | $25.80 | $1.96 | 70 |
| 2025-07-08 14:52:28 | BUY | BAC | 3 | $47.14 | N/A | 75 |
| 2025-07-08 14:52:28 | BUY | INTC | 1 | $23.32 | N/A | 65 |
| 2025-07-08 14:52:28 | BUY | NKE | 1 | $74.18 | N/A | 70 |
| 2025-07-08 14:52:28 | BUY | BA | 1 | $215.26 | N/A | 75 |
| 2025-07-08 14:52:28 | BUY | T | 1 | $28.15 | N/A | 65 |
| 2025-07-08 14:40:40 | SELL | JNJ | 1 | $156.44 | $0.58 | 65 |
| 2025-07-08 14:40:40 | SELL | INTC | 2 | $23.32 | $2.06 | 65 |
| 2025-07-08 14:40:40 | SELL | WFC | 3 | $81.74 | $-1.65 | 75 |
| 2025-07-08 14:40:40 | SELL | T | 1 | $28.41 | $-0.13 | 65 |
| 2025-07-08 14:40:40 | SELL | CSCO | 1 | $68.69 | $0.31 | 70 |
| 2025-07-08 14:40:40 | BUY | NVDA | 1 | $159.12 | N/A | 85 |

<!--TRADE_LOG_END--> 
