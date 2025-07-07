# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 17:08:16**

| Metric | Value |
|---|---|
| **Total Value** | **$100,577.02** |
| Cash | $2,185.68 |
| Holdings Value | $98,391.34 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.00 | $210.28 | $2,313.08 | 75 |
| ADBE | 5 | $377.60 | $377.45 | $1,887.25 | 65 |
| AMD | 16 | $135.70 | $134.97 | $2,159.57 | 70 |
| AMZN | 11 | $221.66 | $222.78 | $2,450.58 | 75 |
| AXP | 7 | $324.46 | $321.94 | $2,253.55 | 75 |
| BA | 10 | $212.15 | $214.91 | $2,149.15 | 70 |
| BAC | 55 | $48.71 | $48.49 | $2,667.04 | 85 |
| C | 30 | $86.59 | $87.44 | $2,623.05 | 85 |
| CAT | 6 | $397.86 | $390.04 | $2,340.24 | 75 |
| COST | 2 | $979.83 | $988.59 | $1,977.18 | 65 |
| CRM | 8 | $268.33 | $269.68 | $2,157.40 | 65 |
| CSCO | 34 | $68.38 | $68.84 | $2,340.56 | 75 |
| CVX | 16 | $146.72 | $145.82 | $2,333.12 | 75 |
| DIS | 18 | $122.86 | $122.99 | $2,213.82 | 70 |
| GOOGL | 13 | $179.38 | $176.19 | $2,290.47 | 75 |
| GS | 3 | $717.52 | $710.14 | $2,130.41 | 85 |
| HD | 6 | $372.64 | $366.17 | $2,197.02 | 65 |
| INTC | 85 | $22.27 | $22.05 | $1,874.24 | 60 |
| JNJ | 13 | $155.80 | $155.37 | $2,019.81 | 65 |
| JPM | 9 | $292.50 | $290.99 | $2,618.92 | 85 |
| KO | 28 | $71.03 | $71.00 | $1,988.00 | 65 |
| LLY | 2 | $776.66 | $768.69 | $1,537.38 | 65 |
| MA | 4 | $563.08 | $562.38 | $2,249.50 | 65 |
| META | 3 | $717.12 | $721.74 | $2,165.22 | 70 |
| MRK | 29 | $82.38 | $81.22 | $2,355.38 | 75 |
| MSFT | 5 | $498.84 | $497.03 | $2,485.15 | 70 |
| NFLX | 1 | $1,279.00 | $1,288.57 | $1,288.57 | 65 |
| NKE | 29 | $75.85 | $76.35 | $2,214.15 | 70 |
| NVDA | 14 | $156.16 | $158.32 | $2,216.54 | 70 |
| ORCL | 9 | $226.15 | $232.87 | $2,095.85 | 70 |
| PEP | 16 | $136.46 | $134.56 | $2,152.88 | 65 |
| PFE | 87 | $25.31 | $25.24 | $2,195.87 | 70 |
| PG | 13 | $160.77 | $159.76 | $2,076.94 | 70 |
| PYPL | 31 | $76.78 | $76.00 | $2,356.15 | 75 |
| QCOM | 15 | $161.55 | $158.72 | $2,380.80 | 75 |
| T | 73 | $28.54 | $28.29 | $2,064.80 | 65 |
| TGT | 20 | $104.92 | $101.33 | $2,026.50 | 65 |
| TSLA | 7 | $289.38 | $292.21 | $2,045.47 | 65 |
| UNH | 7 | $314.75 | $302.89 | $2,120.23 | 65 |
| UNP | 10 | $236.56 | $234.88 | $2,348.80 | 75 |
| V | 6 | $355.95 | $355.27 | $2,131.62 | 70 |
| VZ | 47 | $43.72 | $42.74 | $2,009.01 | 65 |
| WFC | 28 | $82.27 | $81.93 | $2,294.04 | 75 |
| WMT | 23 | $97.35 | $98.70 | $2,270.07 | 70 |
| XOM | 21 | $109.95 | $110.76 | $2,325.96 | 75 |

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
| 2025-07-07 17:08:10 | SELL | AVGO | 8 | $275.33 | $43.44 | 70 |
| 2025-07-07 17:08:10 | SELL | NVDA | 1 | $158.34 | $2.03 | 70 |
| 2025-07-07 17:08:10 | SELL | T | 3 | $28.28 | $-0.74 | 65 |
| 2025-07-07 17:08:10 | BUY | AAPL | 1 | $210.29 | N/A | 75 |
| 2025-07-07 17:08:10 | BUY | TSLA | 1 | $292.27 | N/A | 65 |
| 2025-07-07 17:08:10 | BUY | GOOGL | 1 | $176.22 | N/A | 75 |
| 2025-07-07 17:08:10 | BUY | INTC | 1 | $22.05 | N/A | 60 |
| 2025-07-07 17:08:10 | BUY | BAC | 1 | $48.49 | N/A | 85 |
| 2025-07-07 17:08:10 | BUY | PYPL | 1 | $76.00 | N/A | 75 |
| 2025-07-07 17:08:10 | BUY | PFE | 7 | $25.24 | N/A | 70 |
| 2025-07-07 17:08:10 | BUY | XOM | 1 | $110.76 | N/A | 75 |
| 2025-07-07 17:08:10 | BUY | CSCO | 2 | $68.85 | N/A | 75 |
| 2025-07-07 16:55:21 | SELL | NVDA | 1 | $158.06 | $1.64 | 75 |
| 2025-07-07 16:55:21 | SELL | AAPL | 1 | $213.55 | $2.25 | 65 |
| 2025-07-07 16:55:21 | SELL | PFE | 5 | $25.23 | $-0.39 | 65 |
| 2025-07-07 16:55:21 | SELL | UNP | 1 | $234.91 | $-1.49 | 75 |
| 2025-07-07 16:55:21 | SELL | CSCO | 1 | $68.81 | $0.44 | 70 |
| 2025-07-07 16:55:21 | SELL | CVX | 1 | $145.85 | $-0.82 | 75 |
| 2025-07-07 16:55:21 | BUY | AMD | 1 | $134.82 | N/A | 70 |
| 2025-07-07 16:55:21 | BUY | DIS | 1 | $122.92 | N/A | 75 |
| 2025-07-07 16:55:21 | BUY | C | 5 | $87.30 | N/A | 85 |
| 2025-07-07 16:55:21 | BUY | PEP | 1 | $134.46 | N/A | 70 |
| 2025-07-07 16:55:21 | BUY | T | 5 | $28.33 | N/A | 70 |
| 2025-07-07 16:43:14 | SELL | NKE | 1 | $76.29 | $0.43 | 70 |
| 2025-07-07 16:43:14 | SELL | WFC | 3 | $82.06 | $-0.57 | 75 |

<!--TRADE_LOG_END--> 
