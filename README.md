# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 15:26:56**

| Metric | Value |
|---|---|
| **Total Value** | **$100,735.63** |
| Cash | $1,796.48 |
| Holdings Value | $98,939.15 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $207.73 | $2,077.30 | 65 |
| ADBE | 5 | $377.60 | $376.35 | $1,881.75 | 65 |
| AMD | 15 | $135.39 | $138.10 | $2,071.50 | 70 |
| AMZN | 10 | $221.83 | $222.28 | $2,222.80 | 70 |
| AVGO | 8 | $275.34 | $275.93 | $2,207.44 | 70 |
| AXP | 7 | $325.28 | $318.36 | $2,228.49 | 75 |
| BA | 9 | $210.79 | $227.60 | $2,048.40 | 65 |
| BAC | 47 | $48.71 | $46.74 | $2,197.01 | 70 |
| C | 26 | $86.78 | $85.94 | $2,234.57 | 70 |
| CAT | 6 | $397.86 | $398.42 | $2,390.49 | 75 |
| COST | 2 | $979.83 | $977.46 | $1,954.92 | 65 |
| CRM | 8 | $268.33 | $270.49 | $2,163.93 | 65 |
| CSCO | 32 | $68.33 | $68.66 | $2,196.96 | 70 |
| CVX | 17 | $147.01 | $152.74 | $2,596.58 | 85 |
| DIS | 19 | $122.72 | $121.19 | $2,302.61 | 70 |
| GOOGL | 13 | $179.50 | $177.94 | $2,313.22 | 70 |
| GS | 3 | $717.52 | $697.20 | $2,091.60 | 70 |
| HD | 6 | $372.64 | $365.49 | $2,192.94 | 65 |
| INTC | 86 | $22.33 | $23.30 | $2,003.37 | 65 |
| JNJ | 13 | $155.89 | $155.42 | $2,020.50 | 65 |
| JPM | 9 | $291.61 | $284.02 | $2,556.14 | 75 |
| KO | 29 | $71.03 | $69.11 | $2,004.33 | 65 |
| LLY | 2 | $776.66 | $786.22 | $1,572.43 | 65 |
| MA | 4 | $563.08 | $561.92 | $2,247.68 | 65 |
| META | 3 | $717.12 | $734.34 | $2,203.02 | 85 |
| MRK | 29 | $82.50 | $83.26 | $2,414.54 | 75 |
| MSFT | 5 | $498.84 | $501.62 | $2,508.10 | 70 |
| NFLX | 1 | $1,279.00 | $1,284.20 | $1,284.20 | 65 |
| NKE | 28 | $76.05 | $73.78 | $2,065.84 | 65 |
| NVDA | 16 | $157.22 | $163.28 | $2,612.40 | 85 |
| ORCL | 9 | $233.41 | $234.35 | $2,109.19 | 65 |
| PEP | 15 | $136.57 | $133.19 | $1,997.85 | 65 |
| PFE | 86 | $25.22 | $25.41 | $2,184.83 | 70 |
| PG | 14 | $160.48 | $156.78 | $2,194.92 | 70 |
| PYPL | 31 | $76.64 | $74.66 | $2,314.46 | 75 |
| QCOM | 14 | $161.87 | $158.86 | $2,224.04 | 75 |
| T | 72 | $28.56 | $28.25 | $2,034.00 | 65 |
| TGT | 20 | $104.89 | $101.86 | $2,037.20 | 65 |
| TSLA | 6 | $288.62 | $295.31 | $1,771.83 | 60 |
| UNH | 7 | $314.75 | $300.06 | $2,100.39 | 65 |
| UNP | 9 | $236.60 | $236.92 | $2,132.28 | 75 |
| V | 6 | $355.95 | $354.61 | $2,127.63 | 70 |
| VZ | 48 | $43.15 | $42.62 | $2,046.00 | 65 |
| WFC | 29 | $82.27 | $81.82 | $2,372.88 | 75 |
| WMT | 21 | $97.35 | $97.12 | $2,039.52 | 65 |
| XOM | 21 | $110.02 | $113.67 | $2,387.07 | 75 |

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
| 2025-07-09 15:26:48 | SELL | NKE | 1 | $73.75 | $-2.22 | 65 |
| 2025-07-09 15:26:48 | SELL | C | 4 | $85.93 | $-2.92 | 70 |
| 2025-07-09 15:26:48 | BUY | INTC | 5 | $23.59 | N/A | 65 |
| 2025-07-09 15:26:48 | BUY | PG | 1 | $156.78 | N/A | 70 |
| 2025-07-09 15:26:48 | BUY | CSCO | 1 | $68.65 | N/A | 70 |
| 2025-07-09 15:26:48 | BUY | CVX | 2 | $152.68 | N/A | 85 |
| 2025-07-09 15:09:06 | SELL | AMZN | 1 | $219.36 | $-2.25 | 70 |
| 2025-07-09 15:09:06 | SELL | XOM | 1 | $113.82 | $3.62 | 75 |
| 2025-07-09 15:09:06 | SELL | BA | 1 | $227.19 | $14.76 | 65 |
| 2025-07-09 15:09:06 | BUY | PFE | 1 | $25.47 | N/A | 70 |
| 2025-07-09 15:09:06 | BUY | C | 4 | $86.19 | N/A | 85 |
| 2025-07-09 15:09:06 | BUY | CSCO | 1 | $68.60 | N/A | 70 |
| 2025-07-09 14:52:38 | SELL | INTC | 6 | $23.30 | $5.84 | 60 |
| 2025-07-09 14:52:38 | SELL | C | 1 | $85.94 | $-0.77 | 70 |
| 2025-07-09 14:52:38 | SELL | QCOM | 2 | $159.13 | $-4.79 | 70 |
| 2025-07-09 14:52:38 | SELL | CSCO | 4 | $68.63 | $1.11 | 65 |
| 2025-07-09 14:52:38 | BUY | AMZN | 1 | $221.62 | N/A | 85 |
| 2025-07-09 14:52:38 | BUY | XOM | 1 | $113.65 | N/A | 80 |
| 2025-07-09 14:52:38 | BUY | DIS | 1 | $121.29 | N/A | 75 |
| 2025-07-09 14:52:38 | BUY | PYPL | 1 | $74.64 | N/A | 75 |
| 2025-07-09 14:52:38 | BUY | PFE | 5 | $25.45 | N/A | 70 |
| 2025-07-09 14:40:32 | SELL | PYPL | 1 | $74.77 | $-1.87 | 70 |
| 2025-07-09 14:40:32 | SELL | PFE | 5 | $25.50 | $1.39 | 65 |
| 2025-07-09 14:40:32 | BUY | QCOM | 1 | $159.82 | N/A | 85 |
| 2025-07-09 14:26:02 | SELL | BAC | 3 | $47.10 | $-4.51 | 70 |

<!--TRADE_LOG_END--> 
