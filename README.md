# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 16:26:57**

| Metric | Value |
|---|---|
| **Total Value** | **$100,674.30** |
| Cash | $700.55 |
| Holdings Value | $99,973.75 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.71 | $2,107.05 | 70 |
| ADBE | 5 | $377.60 | $365.93 | $1,829.65 | 65 |
| AMD | 18 | $136.77 | $145.60 | $2,620.75 | 85 |
| AMZN | 11 | $221.97 | $225.27 | $2,477.97 | 75 |
| AVGO | 8 | $275.34 | $276.12 | $2,208.96 | 70 |
| AXP | 7 | $325.34 | $321.19 | $2,248.33 | 75 |
| BA | 10 | $212.47 | $227.12 | $2,271.20 | 75 |
| BAC | 44 | $48.85 | $46.48 | $2,045.33 | 65 |
| C | 24 | $86.68 | $86.37 | $2,072.88 | 65 |
| CAT | 6 | $397.86 | $404.75 | $2,428.53 | 65 |
| COST | 2 | $979.83 | $967.12 | $1,934.24 | 65 |
| CRM | 7 | $268.68 | $259.97 | $1,819.79 | 65 |
| CSCO | 34 | $68.35 | $67.92 | $2,309.45 | 75 |
| CVX | 17 | $147.16 | $154.88 | $2,632.96 | 85 |
| DIS | 18 | $122.80 | $119.98 | $2,159.64 | 70 |
| GOOGL | 13 | $179.61 | $179.80 | $2,337.40 | 75 |
| GS | 3 | $717.52 | $702.28 | $2,106.84 | 70 |
| HD | 6 | $372.64 | $368.27 | $2,209.62 | 65 |
| INTC | 81 | $22.28 | $23.36 | $1,892.56 | 60 |
| JNJ | 13 | $155.89 | $156.16 | $2,030.08 | 65 |
| JPM | 9 | $291.61 | $286.05 | $2,574.45 | 75 |
| KO | 29 | $71.03 | $69.86 | $2,025.80 | 65 |
| LLY | 3 | $781.32 | $780.00 | $2,340.00 | 70 |
| MA | 4 | $563.08 | $550.25 | $2,201.02 | 65 |
| META | 3 | $717.12 | $721.14 | $2,163.42 | 70 |
| MRK | 25 | $82.29 | $82.81 | $2,070.25 | 65 |
| MSFT | 5 | $498.84 | $504.66 | $2,523.30 | 85 |
| NFLX | 1 | $1,279.00 | $1,238.97 | $1,238.97 | 65 |
| NKE | 32 | $75.67 | $72.50 | $2,319.84 | 75 |
| NVDA | 16 | $157.38 | $166.47 | $2,663.52 | 85 |
| ORCL | 9 | $233.26 | $232.43 | $2,091.87 | 65 |
| PEP | 15 | $136.57 | $133.94 | $2,009.03 | 65 |
| PFE | 85 | $25.20 | $25.55 | $2,172.18 | 70 |
| PG | 13 | $160.80 | $156.54 | $2,034.98 | 65 |
| PYPL | 28 | $76.82 | $74.40 | $2,083.15 | 65 |
| QCOM | 13 | $162.18 | $157.94 | $2,053.16 | 65 |
| T | 76 | $27.10 | $26.70 | $2,028.82 | 65 |
| TGT | 20 | $104.91 | $104.27 | $2,085.30 | 65 |
| TSLA | 6 | $288.62 | $309.64 | $1,857.84 | 65 |
| UNH | 7 | $298.51 | $301.12 | $2,107.88 | 65 |
| UNP | 10 | $236.18 | $234.26 | $2,342.60 | 75 |
| V | 6 | $355.85 | $347.79 | $2,086.71 | 65 |
| VZ | 49 | $43.12 | $41.52 | $2,034.72 | 65 |
| WFC | 29 | $82.28 | $82.14 | $2,382.20 | 75 |
| WMT | 22 | $97.25 | $94.84 | $2,086.48 | 65 |
| XOM | 23 | $110.40 | $115.35 | $2,653.05 | 85 |

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
| 2025-07-11 16:26:51 | SELL | INTC | 6 | $23.36 | $6.00 | 60 |
| 2025-07-11 16:26:51 | SELL | PYPL | 3 | $74.40 | $-6.56 | 65 |
| 2025-07-11 16:26:51 | SELL | C | 2 | $86.38 | $-0.56 | 65 |
| 2025-07-11 16:26:51 | BUY | XOM | 2 | $115.34 | N/A | 85 |
| 2025-07-11 16:26:51 | BUY | BA | 1 | $227.06 | N/A | 75 |
| 2025-07-11 16:09:13 | SELL | XOM | 1 | $115.30 | $5.13 | 75 |
| 2025-07-11 16:09:13 | SELL | MRK | 1 | $82.85 | $0.53 | 65 |
| 2025-07-11 16:09:13 | BUY | INTC | 1 | $23.44 | N/A | 65 |
| 2025-07-11 16:09:13 | BUY | PYPL | 4 | $74.32 | N/A | 75 |
| 2025-07-11 16:09:13 | BUY | NKE | 1 | $72.62 | N/A | 75 |
| 2025-07-11 15:51:23 | SELL | BAC | 3 | $46.45 | $-6.75 | 65 |
| 2025-07-11 15:51:23 | SELL | INTC | 1 | $23.42 | $1.06 | 65 |
| 2025-07-11 15:51:23 | SELL | PYPL | 1 | $74.56 | $-2.28 | 65 |
| 2025-07-11 15:51:23 | SELL | PFE | 1 | $25.59 | $0.39 | 70 |
| 2025-07-11 15:51:23 | SELL | PG | 1 | $156.91 | $-3.60 | 65 |
| 2025-07-11 15:51:23 | SELL | TGT | 1 | $104.49 | $-0.40 | 65 |
| 2025-07-11 15:51:23 | BUY | DIS | 1 | $120.05 | N/A | 70 |
| 2025-07-11 15:51:23 | BUY | XOM | 1 | $115.55 | N/A | 85 |
| 2025-07-11 15:51:23 | BUY | NKE | 2 | $72.60 | N/A | 75 |
| 2025-07-11 15:51:23 | BUY | MRK | 1 | $82.71 | N/A | 70 |
| 2025-07-11 15:51:23 | BUY | C | 2 | $86.34 | N/A | 75 |
| 2025-07-11 15:51:23 | BUY | CSCO | 3 | $68.04 | N/A | 75 |
| 2025-07-11 15:39:50 | SELL | NKE | 1 | $72.61 | $-3.27 | 65 |
| 2025-07-11 15:39:50 | SELL | PYPL | 1 | $74.61 | $-2.15 | 65 |
| 2025-07-11 15:39:50 | SELL | C | 1 | $86.40 | $-0.27 | 65 |

<!--TRADE_LOG_END--> 
