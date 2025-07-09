# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 17:10:11**

| Metric | Value |
|---|---|
| **Total Value** | **$100,808.38** |
| Cash | $1,738.54 |
| Holdings Value | $99,069.84 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $208.58 | $2,085.82 | 65 |
| ADBE | 5 | $377.60 | $372.00 | $1,860.03 | 65 |
| AMD | 15 | $135.39 | $138.76 | $2,081.40 | 65 |
| AMZN | 10 | $221.83 | $222.60 | $2,226.00 | 75 |
| AVGO | 8 | $275.34 | $277.90 | $2,223.24 | 70 |
| AXP | 7 | $325.28 | $317.92 | $2,225.41 | 75 |
| BA | 10 | $212.53 | $229.17 | $2,291.67 | 70 |
| BAC | 50 | $48.59 | $46.77 | $2,338.75 | 75 |
| C | 31 | $86.66 | $85.92 | $2,663.67 | 85 |
| CAT | 6 | $397.86 | $401.87 | $2,411.19 | 85 |
| COST | 2 | $979.83 | $975.74 | $1,951.48 | 65 |
| CRM | 8 | $268.33 | $270.02 | $2,160.16 | 65 |
| CSCO | 32 | $68.33 | $68.82 | $2,202.31 | 70 |
| CVX | 16 | $146.65 | $153.24 | $2,451.84 | 75 |
| DIS | 18 | $122.81 | $120.91 | $2,176.30 | 70 |
| GOOGL | 13 | $179.50 | $177.43 | $2,306.59 | 75 |
| GS | 3 | $717.52 | $697.16 | $2,091.48 | 70 |
| HD | 6 | $372.64 | $365.47 | $2,192.82 | 65 |
| INTC | 80 | $22.23 | $23.32 | $1,865.95 | 60 |
| JNJ | 13 | $155.89 | $155.50 | $2,021.50 | 65 |
| JPM | 9 | $291.61 | $283.25 | $2,549.20 | 75 |
| KO | 29 | $71.03 | $69.19 | $2,006.37 | 65 |
| LLY | 2 | $776.66 | $784.65 | $1,569.31 | 65 |
| MA | 4 | $563.08 | $560.11 | $2,240.44 | 65 |
| META | 3 | $717.12 | $735.18 | $2,205.54 | 85 |
| MRK | 29 | $82.50 | $83.86 | $2,431.94 | 80 |
| MSFT | 5 | $498.84 | $500.68 | $2,503.40 | 70 |
| NFLX | 1 | $1,279.00 | $1,277.05 | $1,277.05 | 65 |
| NKE | 29 | $75.98 | $73.94 | $2,144.40 | 70 |
| NVDA | 16 | $157.22 | $163.28 | $2,612.48 | 85 |
| ORCL | 9 | $233.31 | $235.06 | $2,115.54 | 70 |
| PEP | 15 | $136.57 | $133.64 | $2,004.59 | 65 |
| PFE | 81 | $25.21 | $25.45 | $2,061.05 | 65 |
| PG | 13 | $160.75 | $156.37 | $2,032.81 | 65 |
| PYPL | 31 | $76.63 | $74.83 | $2,319.73 | 75 |
| QCOM | 14 | $161.87 | $159.21 | $2,228.94 | 70 |
| T | 72 | $28.56 | $28.04 | $2,018.88 | 65 |
| TGT | 20 | $104.89 | $102.41 | $2,048.20 | 65 |
| TSLA | 6 | $288.62 | $295.36 | $1,772.13 | 65 |
| UNH | 7 | $314.75 | $302.15 | $2,115.05 | 65 |
| UNP | 9 | $236.60 | $237.12 | $2,134.03 | 65 |
| V | 6 | $355.95 | $354.38 | $2,126.31 | 70 |
| VZ | 48 | $43.15 | $42.63 | $2,046.48 | 65 |
| WFC | 29 | $82.28 | $81.78 | $2,371.62 | 75 |
| WMT | 21 | $97.35 | $96.84 | $2,033.64 | 65 |
| XOM | 20 | $109.83 | $113.66 | $2,273.10 | 75 |

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
| 2025-07-09 17:10:02 | SELL | INTC | 7 | $23.59 | $8.73 | 60 |
| 2025-07-09 17:10:02 | SELL | PFE | 6 | $25.44 | $1.30 | 65 |
| 2025-07-09 17:10:02 | SELL | CVX | 1 | $153.25 | $6.22 | 75 |
| 2025-07-09 17:10:02 | BUY | BAC | 4 | $46.78 | N/A | 75 |
| 2025-07-09 17:10:02 | BUY | NKE | 1 | $73.95 | N/A | 70 |
| 2025-07-09 17:10:02 | BUY | PYPL | 1 | $74.82 | N/A | 75 |
| 2025-07-09 17:10:02 | BUY | MRK | 1 | $83.86 | N/A | 80 |
| 2025-07-09 16:56:47 | SELL | PYPL | 1 | $74.84 | $-1.79 | 70 |
| 2025-07-09 16:56:47 | SELL | PFE | 5 | $25.44 | $1.02 | 70 |
| 2025-07-09 16:56:47 | SELL | ORCL | 1 | $234.93 | $1.46 | 65 |
| 2025-07-09 16:56:47 | BUY | BAC | 2 | $46.74 | N/A | 70 |
| 2025-07-09 16:56:47 | BUY | C | 3 | $85.75 | N/A | 85 |
| 2025-07-09 16:43:39 | SELL | NKE | 1 | $73.73 | $-2.24 | 65 |
| 2025-07-09 16:43:39 | SELL | MRK | 1 | $83.84 | $1.35 | 75 |
| 2025-07-09 16:43:39 | SELL | C | 3 | $85.68 | $-2.94 | 75 |
| 2025-07-09 16:43:39 | SELL | WFC | 1 | $81.47 | $-0.78 | 75 |
| 2025-07-09 16:43:39 | BUY | NVDA | 2 | $163.10 | N/A | 85 |
| 2025-07-09 16:43:39 | BUY | DIS | 1 | $121.03 | N/A | 70 |
| 2025-07-09 16:43:39 | BUY | PFE | 6 | $25.42 | N/A | 75 |
| 2025-07-09 16:43:39 | BUY | CVX | 1 | $152.71 | N/A | 85 |
| 2025-07-09 16:26:59 | SELL | NVDA | 1 | $163.21 | $6.37 | 70 |
| 2025-07-09 16:26:59 | SELL | BAC | 6 | $46.79 | $-10.79 | 65 |
| 2025-07-09 16:26:59 | SELL | DIS | 2 | $121.05 | $-3.34 | 65 |
| 2025-07-09 16:26:59 | SELL | CVX | 1 | $152.81 | $5.77 | 75 |
| 2025-07-09 16:26:59 | BUY | PYPL | 3 | $74.68 | N/A | 75 |

<!--TRADE_LOG_END--> 
