# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 16:43:21**

| Metric | Value |
|---|---|
| **Total Value** | **$102,001.63** |
| Cash | $1,925.74 |
| Holdings Value | $100,075.88 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.55 | $213.93 | $2,353.23 | 75 |
| ADBE | 5 | $377.60 | $380.92 | $1,904.60 | 65 |
| AMD | 15 | $135.93 | $138.07 | $2,071.12 | 70 |
| AMZN | 10 | $221.48 | $223.20 | $2,232.00 | 75 |
| AVGO | 8 | $269.90 | $274.64 | $2,197.16 | 70 |
| AXP | 8 | $324.40 | $329.01 | $2,632.08 | 85 |
| BA | 10 | $212.15 | $215.64 | $2,156.40 | 65 |
| BAC | 54 | $48.71 | $49.03 | $2,647.38 | 85 |
| C | 30 | $86.80 | $88.72 | $2,661.60 | 85 |
| CAT | 6 | $396.45 | $399.14 | $2,394.84 | 65 |
| COST | 2 | $979.83 | $986.81 | $1,973.63 | 65 |
| CRM | 8 | $268.33 | $273.39 | $2,187.12 | 65 |
| CSCO | 33 | $68.36 | $69.30 | $2,286.74 | 75 |
| CVX | 16 | $146.55 | $148.88 | $2,382.00 | 75 |
| DIS | 18 | $122.90 | $124.23 | $2,236.14 | 70 |
| GOOGL | 13 | $177.86 | $179.17 | $2,329.21 | 75 |
| GS | 3 | $717.52 | $722.88 | $2,168.64 | 70 |
| HD | 6 | $372.64 | $372.99 | $2,237.94 | 65 |
| INTC | 84 | $22.34 | $22.46 | $1,886.30 | 60 |
| JNJ | 13 | $155.80 | $156.20 | $2,030.65 | 65 |
| JPM | 9 | $292.50 | $296.23 | $2,666.07 | 85 |
| KO | 30 | $71.05 | $71.36 | $2,140.65 | 70 |
| LLY | 2 | $776.66 | $779.07 | $1,558.13 | 65 |
| MA | 3 | $561.03 | $569.38 | $1,708.14 | 65 |
| META | 3 | $717.12 | $719.53 | $2,158.59 | 85 |
| MRK | 25 | $82.46 | $81.46 | $2,036.46 | 65 |
| MSFT | 5 | $491.36 | $498.85 | $2,494.25 | 85 |
| NFLX | 1 | $1,279.00 | $1,298.73 | $1,298.73 | 70 |
| NKE | 28 | $75.74 | $76.53 | $2,142.98 | 70 |
| NVDA | 14 | $155.97 | $159.19 | $2,228.69 | 70 |
| ORCL | 10 | $226.06 | $237.22 | $2,372.15 | 75 |
| PEP | 15 | $136.59 | $135.68 | $2,035.13 | 65 |
| PFE | 80 | $25.30 | $25.50 | $2,040.00 | 65 |
| PG | 12 | $160.76 | $160.90 | $1,930.80 | 65 |
| PYPL | 30 | $76.81 | $76.84 | $2,305.20 | 75 |
| QCOM | 15 | $161.52 | $162.48 | $2,437.20 | 75 |
| T | 77 | $28.52 | $28.36 | $2,183.72 | 70 |
| TGT | 19 | $105.07 | $104.31 | $1,981.89 | 65 |
| TSLA | 6 | $313.02 | $317.15 | $1,902.90 | 60 |
| UNH | 7 | $314.75 | $310.18 | $2,171.26 | 65 |
| UNP | 9 | $236.50 | $237.93 | $2,141.37 | 70 |
| V | 6 | $352.90 | $358.88 | $2,153.28 | 70 |
| VZ | 46 | $43.73 | $43.55 | $2,003.53 | 65 |
| WFC | 31 | $82.32 | $83.61 | $2,591.91 | 85 |
| WMT | 21 | $97.28 | $98.28 | $2,063.78 | 65 |
| XOM | 21 | $109.97 | $112.39 | $2,360.30 | 75 |

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
| 2025-07-03 16:43:14 | SELL | INTC | 6 | $22.44 | $0.61 | 60 |
| 2025-07-03 16:43:14 | SELL | WMT | 2 | $98.26 | $1.79 | 65 |
| 2025-07-03 16:43:14 | SELL | QCOM | 1 | $162.53 | $0.95 | 75 |
| 2025-07-03 16:43:14 | SELL | ORCL | 1 | $237.29 | $10.21 | 75 |
| 2025-07-03 16:43:14 | BUY | GOOGL | 1 | $179.18 | N/A | 75 |
| 2025-07-03 16:43:14 | BUY | AAPL | 1 | $212.44 | N/A | 75 |
| 2025-07-03 16:43:14 | BUY | BAC | 7 | $49.03 | N/A | 85 |
| 2025-07-03 16:43:14 | BUY | KO | 1 | $71.35 | N/A | 70 |
| 2025-07-03 16:43:14 | BUY | PYPL | 1 | $76.84 | N/A | 75 |
| 2025-07-03 16:43:14 | BUY | NKE | 1 | $76.53 | N/A | 70 |
| 2025-07-03 16:43:14 | BUY | WFC | 2 | $83.61 | N/A | 85 |
| 2025-07-03 16:43:14 | BUY | CSCO | 3 | $69.32 | N/A | 75 |
| 2025-07-03 16:26:50 | SELL | KO | 1 | $71.25 | $0.20 | 65 |
| 2025-07-03 16:26:50 | SELL | NKE | 6 | $76.33 | $3.05 | 65 |
| 2025-07-03 16:26:50 | SELL | PYPL | 1 | $76.76 | $-0.04 | 70 |
| 2025-07-03 16:26:50 | SELL | CSCO | 2 | $69.36 | $2.06 | 65 |
| 2025-07-03 16:26:50 | SELL | PFE | 11 | $25.50 | $1.91 | 65 |
| 2025-07-03 16:26:50 | BUY | BAC | 2 | $48.98 | N/A | 75 |
| 2025-07-03 16:26:50 | BUY | INTC | 1 | $22.45 | N/A | 65 |
| 2025-07-03 16:26:50 | BUY | WMT | 2 | $98.07 | N/A | 75 |
| 2025-07-03 16:26:50 | BUY | WFC | 1 | $83.44 | N/A | 80 |
| 2025-07-03 16:26:50 | BUY | DIS | 1 | $123.83 | N/A | 75 |
| 2025-07-03 16:26:50 | BUY | QCOM | 2 | $162.78 | N/A | 85 |
| 2025-07-03 16:26:50 | BUY | ORCL | 2 | $237.69 | N/A | 85 |
| 2025-07-03 16:26:50 | BUY | T | 1 | $28.31 | N/A | 70 |

<!--TRADE_LOG_END--> 
