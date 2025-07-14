# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 14:09:25**

| Metric | Value |
|---|---|
| **Total Value** | **$100,540.94** |
| Cash | $903.87 |
| Holdings Value | $99,637.07 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.05 | $2,080.50 | 65 |
| ADBE | 6 | $375.23 | $363.44 | $2,180.64 | 65 |
| AMD | 15 | $134.63 | $143.82 | $2,157.38 | 70 |
| AMZN | 12 | $222.22 | $225.86 | $2,710.32 | 80 |
| AVGO | 8 | $275.34 | $273.16 | $2,185.28 | 65 |
| AXP | 7 | $325.34 | $318.26 | $2,227.82 | 75 |
| BA | 10 | $212.59 | $227.68 | $2,276.75 | 70 |
| BAC | 47 | $48.70 | $46.58 | $2,189.03 | 70 |
| C | 27 | $86.64 | $86.30 | $2,330.10 | 75 |
| CAT | 5 | $396.39 | $405.44 | $2,027.22 | 70 |
| COST | 2 | $979.83 | $976.32 | $1,952.64 | 70 |
| CRM | 7 | $268.68 | $259.90 | $1,819.33 | 65 |
| CSCO | 33 | $68.40 | $67.69 | $2,233.61 | 70 |
| CVX | 17 | $147.16 | $153.00 | $2,601.00 | 80 |
| DIS | 18 | $122.80 | $119.98 | $2,159.64 | 70 |
| GOOGL | 14 | $179.65 | $180.22 | $2,523.08 | 75 |
| GS | 3 | $717.52 | $705.32 | $2,115.95 | 70 |
| HD | 6 | $372.64 | $369.74 | $2,218.43 | 70 |
| INTC | 88 | $22.38 | $22.96 | $2,020.92 | 65 |
| JNJ | 14 | $155.99 | $156.94 | $2,197.16 | 65 |
| JPM | 9 | $291.63 | $286.23 | $2,576.07 | 85 |
| KO | 29 | $71.03 | $69.89 | $2,026.81 | 65 |
| LLY | 3 | $781.32 | $796.09 | $2,388.27 | 70 |
| MA | 4 | $563.08 | $557.88 | $2,231.52 | 65 |
| META | 3 | $717.12 | $719.52 | $2,158.56 | 70 |
| MRK | 28 | $82.49 | $83.58 | $2,340.24 | 75 |
| MSFT | 5 | $498.84 | $501.97 | $2,509.86 | 85 |
| NFLX | 1 | $1,279.00 | $1,263.43 | $1,263.43 | 65 |
| NKE | 28 | $72.10 | $71.88 | $2,012.64 | 65 |
| NVDA | 13 | $156.17 | $163.51 | $2,125.69 | 65 |
| ORCL | 9 | $233.26 | $225.62 | $2,030.62 | 65 |
| PEP | 15 | $136.57 | $134.71 | $2,020.65 | 65 |
| PFE | 86 | $25.21 | $25.53 | $2,195.58 | 70 |
| PG | 13 | $160.78 | $154.72 | $2,011.36 | 65 |
| PYPL | 28 | $72.09 | $73.74 | $2,064.72 | 65 |
| QCOM | 14 | $162.09 | $154.32 | $2,160.48 | 65 |
| T | 75 | $27.10 | $27.39 | $2,054.62 | 65 |
| TGT | 20 | $104.91 | $103.74 | $2,074.80 | 65 |
| TSLA | 6 | $288.62 | $315.25 | $1,891.50 | 60 |
| UNH | 7 | $298.51 | $302.75 | $2,119.28 | 65 |
| UNP | 10 | $236.18 | $233.44 | $2,334.45 | 75 |
| V | 6 | $355.85 | $349.52 | $2,097.15 | 65 |
| VZ | 46 | $43.21 | $41.74 | $1,920.27 | 60 |
| WFC | 28 | $82.26 | $82.58 | $2,312.24 | 75 |
| WMT | 21 | $97.38 | $95.26 | $2,000.46 | 65 |
| XOM | 22 | $110.17 | $114.05 | $2,508.99 | 80 |

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
| 2025-07-14 14:09:17 | SELL | PYPL | 4 | $73.70 | $5.64 | 65 |
| 2025-07-14 14:09:17 | SELL | VZ | 3 | $41.74 | $-4.11 | 60 |
| 2025-07-14 14:09:17 | SELL | T | 1 | $27.40 | $0.29 | 65 |
| 2025-07-14 14:09:17 | BUY | XOM | 1 | $114.01 | N/A | 80 |
| 2025-07-14 14:09:17 | BUY | C | 1 | $86.29 | N/A | 75 |
| 2025-07-14 14:09:17 | BUY | WFC | 1 | $82.58 | N/A | 75 |
| 2025-07-14 13:48:21 | SELL | NVDA | 3 | $162.65 | $15.79 | 65 |
| 2025-07-14 13:48:21 | SELL | WFC | 1 | $82.75 | $0.48 | 70 |
| 2025-07-14 13:48:21 | SELL | CSCO | 1 | $67.74 | $-0.64 | 70 |
| 2025-07-14 13:48:21 | SELL | QCOM | 1 | $154.02 | $-7.52 | 65 |
| 2025-07-14 13:48:21 | BUY | JNJ | 1 | $157.31 | N/A | 70 |
| 2025-07-14 13:48:21 | BUY | AMZN | 1 | $225.02 | N/A | 85 |
| 2025-07-14 13:48:21 | BUY | INTC | 1 | $23.43 | N/A | 65 |
| 2025-07-14 13:48:21 | BUY | NKE | 28 | $72.10 | N/A | 65 |
| 2025-07-14 13:48:21 | BUY | PYPL | 3 | $74.08 | N/A | 75 |
| 2025-07-14 13:48:21 | BUY | MRK | 3 | $84.08 | N/A | 75 |
| 2025-07-14 13:48:21 | BUY | T | 1 | $26.97 | N/A | 65 |
| 2025-07-14 13:48:02 | SELL | NKE | 29 | $72.07 | $-113.39 | 65 |
| 2025-07-14 13:29:35 | SELL | NKE | 1 | $72.63 | $-3.24 | 65 |
| 2025-07-14 13:29:35 | SELL | C | 1 | $86.73 | $0.08 | 70 |
| 2025-07-14 13:29:35 | SELL | BA | 1 | $226.84 | $12.95 | 65 |
| 2025-07-14 13:29:35 | BUY | GOOGL | 1 | $180.19 | N/A | 85 |
| 2025-07-14 13:29:35 | BUY | AMD | 1 | $146.42 | N/A | 70 |
| 2025-07-14 13:29:35 | BUY | PFE | 7 | $25.65 | N/A | 70 |
| 2025-07-14 13:29:35 | BUY | CSCO | 2 | $67.95 | N/A | 75 |

<!--TRADE_LOG_END--> 
