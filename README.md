# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 15:26:40**

| Metric | Value |
|---|---|
| **Total Value** | **$100,862.88** |
| Cash | $1,747.10 |
| Holdings Value | $99,115.77 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $212.03 | $2,120.25 | 70 |
| ADBE | 5 | $377.60 | $378.01 | $1,890.05 | 65 |
| AMD | 15 | $135.79 | $134.10 | $2,011.50 | 65 |
| AMZN | 11 | $221.66 | $223.88 | $2,462.62 | 85 |
| AVGO | 8 | $269.90 | $276.55 | $2,212.36 | 70 |
| AXP | 8 | $324.34 | $324.92 | $2,599.32 | 85 |
| BA | 10 | $212.15 | $214.83 | $2,148.31 | 70 |
| BAC | 54 | $48.71 | $48.94 | $2,642.49 | 85 |
| C | 29 | $86.64 | $87.99 | $2,551.71 | 85 |
| CAT | 6 | $397.86 | $392.45 | $2,354.70 | 85 |
| COST | 2 | $979.83 | $984.00 | $1,968.00 | 65 |
| CRM | 8 | $268.33 | $271.51 | $2,172.12 | 65 |
| CSCO | 32 | $68.34 | $69.02 | $2,208.48 | 70 |
| CVX | 16 | $146.70 | $146.74 | $2,347.78 | 75 |
| DIS | 18 | $122.89 | $123.45 | $2,222.10 | 70 |
| GOOGL | 12 | $179.59 | $177.33 | $2,127.96 | 65 |
| GS | 3 | $717.52 | $717.56 | $2,152.68 | 85 |
| HD | 6 | $372.64 | $368.61 | $2,211.66 | 65 |
| INTC | 85 | $22.27 | $22.05 | $1,874.66 | 60 |
| JNJ | 13 | $155.80 | $155.65 | $2,023.45 | 65 |
| JPM | 9 | $292.50 | $293.34 | $2,640.06 | 85 |
| KO | 28 | $71.03 | $71.01 | $1,988.28 | 65 |
| LLY | 2 | $776.66 | $768.49 | $1,536.97 | 60 |
| MA | 4 | $563.08 | $565.66 | $2,262.64 | 65 |
| META | 3 | $717.12 | $723.88 | $2,171.62 | 70 |
| MRK | 25 | $82.54 | $81.04 | $2,026.00 | 65 |
| MSFT | 5 | $498.84 | $497.98 | $2,489.88 | 85 |
| NFLX | 1 | $1,279.00 | $1,283.43 | $1,283.43 | 65 |
| NKE | 28 | $75.87 | $76.03 | $2,128.84 | 70 |
| NVDA | 14 | $156.19 | $158.15 | $2,214.10 | 70 |
| ORCL | 9 | $226.04 | $234.11 | $2,106.99 | 70 |
| PEP | 15 | $136.59 | $134.37 | $2,015.55 | 65 |
| PFE | 80 | $25.30 | $25.32 | $2,025.20 | 65 |
| PG | 13 | $160.77 | $159.74 | $2,076.56 | 65 |
| PYPL | 30 | $76.81 | $76.48 | $2,294.46 | 75 |
| QCOM | 14 | $161.69 | $158.31 | $2,216.34 | 75 |
| T | 72 | $28.54 | $28.33 | $2,039.76 | 65 |
| TGT | 20 | $104.92 | $101.19 | $2,023.80 | 65 |
| TSLA | 6 | $288.90 | $292.25 | $1,753.50 | 65 |
| UNH | 7 | $314.75 | $303.72 | $2,126.04 | 65 |
| UNP | 10 | $236.48 | $236.34 | $2,363.45 | 75 |
| V | 6 | $352.90 | $356.52 | $2,139.15 | 65 |
| VZ | 47 | $43.72 | $42.88 | $2,015.36 | 65 |
| WFC | 29 | $82.25 | $82.57 | $2,394.53 | 75 |
| WMT | 23 | $97.36 | $98.08 | $2,255.95 | 75 |
| XOM | 20 | $109.91 | $111.25 | $2,225.10 | 75 |

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
| 2025-07-07 15:26:23 | SELL | GOOGL | 1 | $177.19 | $-2.21 | 65 |
| 2025-07-07 15:26:23 | SELL | PFE | 6 | $25.31 | $0.00 | 65 |
| 2025-07-07 15:26:23 | SELL | MRK | 4 | $81.06 | $-5.11 | 65 |
| 2025-07-07 15:26:23 | SELL | WFC | 1 | $82.57 | $0.31 | 75 |
| 2025-07-07 15:26:23 | BUY | NKE | 1 | $76.03 | N/A | 70 |
| 2025-07-07 15:26:23 | BUY | C | 3 | $87.99 | N/A | 85 |
| 2025-07-07 15:07:46 | SELL | NVDA | 2 | $157.80 | $2.81 | 70 |
| 2025-07-07 15:07:46 | SELL | INTC | 1 | $22.05 | $-0.22 | 60 |
| 2025-07-07 15:07:46 | SELL | XOM | 1 | $111.52 | $1.53 | 70 |
| 2025-07-07 15:07:46 | SELL | NKE | 3 | $76.06 | $0.53 | 65 |
| 2025-07-07 15:07:46 | SELL | CSCO | 2 | $69.00 | $1.23 | 70 |
| 2025-07-07 15:07:46 | SELL | CVX | 2 | $147.13 | $0.77 | 75 |
| 2025-07-07 15:07:46 | SELL | T | 5 | $28.33 | $-0.95 | 65 |
| 2025-07-07 15:07:46 | BUY | WMT | 2 | $98.10 | N/A | 75 |
| 2025-07-07 15:07:46 | BUY | PFE | 5 | $25.39 | N/A | 70 |
| 2025-07-07 15:07:46 | BUY | C | 1 | $88.06 | N/A | 75 |
| 2025-07-07 15:07:46 | BUY | WFC | 5 | $82.73 | N/A | 80 |
| 2025-07-07 14:52:46 | SELL | INTC | 5 | $22.15 | $-0.58 | 60 |
| 2025-07-07 14:52:46 | SELL | PFE | 4 | $25.36 | $0.25 | 65 |
| 2025-07-07 14:52:46 | SELL | WMT | 2 | $97.87 | $1.06 | 65 |
| 2025-07-07 14:52:46 | SELL | C | 4 | $88.40 | $6.82 | 70 |
| 2025-07-07 14:52:46 | SELL | WFC | 3 | $83.01 | $2.26 | 65 |
| 2025-07-07 14:52:46 | SELL | ORCL | 1 | $232.30 | $5.64 | 65 |
| 2025-07-07 14:52:46 | BUY | NVDA | 2 | $158.33 | N/A | 85 |
| 2025-07-07 14:52:46 | BUY | BAC | 1 | $49.15 | N/A | 85 |

<!--TRADE_LOG_END--> 
