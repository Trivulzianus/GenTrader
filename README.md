# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 15:07:52**

| Metric | Value |
|---|---|
| **Total Value** | **$100,895.01** |
| Cash | $1,351.29 |
| Holdings Value | $99,543.72 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $212.07 | $2,120.75 | 70 |
| ADBE | 5 | $377.60 | $377.92 | $1,889.59 | 65 |
| AMD | 15 | $135.79 | $133.99 | $2,009.80 | 65 |
| AMZN | 11 | $221.66 | $223.59 | $2,459.49 | 75 |
| AVGO | 8 | $269.90 | $275.49 | $2,203.92 | 70 |
| AXP | 8 | $324.34 | $324.63 | $2,597.08 | 75 |
| BA | 10 | $212.15 | $214.94 | $2,149.43 | 65 |
| BAC | 54 | $48.71 | $49.06 | $2,649.51 | 85 |
| C | 26 | $86.48 | $88.08 | $2,289.95 | 75 |
| CAT | 6 | $397.86 | $393.14 | $2,358.84 | 70 |
| COST | 2 | $979.83 | $980.78 | $1,961.56 | 65 |
| CRM | 8 | $268.33 | $272.23 | $2,177.84 | 65 |
| CSCO | 32 | $68.34 | $68.98 | $2,207.41 | 70 |
| CVX | 16 | $146.70 | $147.19 | $2,355.04 | 75 |
| DIS | 18 | $122.89 | $123.51 | $2,223.23 | 70 |
| GOOGL | 13 | $179.40 | $176.97 | $2,300.61 | 70 |
| GS | 3 | $717.52 | $719.10 | $2,157.31 | 75 |
| HD | 6 | $372.64 | $369.47 | $2,216.82 | 70 |
| INTC | 85 | $22.27 | $22.05 | $1,873.83 | 60 |
| JNJ | 13 | $155.80 | $155.95 | $2,027.35 | 65 |
| JPM | 9 | $292.50 | $293.82 | $2,644.38 | 85 |
| KO | 28 | $71.03 | $70.97 | $1,987.02 | 65 |
| LLY | 2 | $776.66 | $770.66 | $1,541.32 | 65 |
| MA | 4 | $563.08 | $564.48 | $2,257.90 | 65 |
| META | 3 | $717.12 | $725.23 | $2,175.69 | 75 |
| MRK | 29 | $82.33 | $81.28 | $2,357.12 | 75 |
| MSFT | 5 | $498.84 | $497.60 | $2,488.00 | 85 |
| NFLX | 1 | $1,279.00 | $1,282.49 | $1,282.49 | 70 |
| NKE | 27 | $75.86 | $75.94 | $2,050.38 | 65 |
| NVDA | 14 | $156.19 | $157.66 | $2,207.24 | 70 |
| ORCL | 9 | $226.04 | $232.49 | $2,092.37 | 70 |
| PEP | 15 | $136.59 | $134.70 | $2,020.44 | 65 |
| PFE | 86 | $25.30 | $25.39 | $2,183.11 | 70 |
| PG | 13 | $160.77 | $160.16 | $2,082.08 | 65 |
| PYPL | 30 | $76.81 | $76.60 | $2,298.00 | 75 |
| QCOM | 14 | $161.69 | $157.91 | $2,210.74 | 75 |
| T | 72 | $28.54 | $28.34 | $2,040.84 | 65 |
| TGT | 20 | $104.92 | $101.47 | $2,029.37 | 65 |
| TSLA | 6 | $288.90 | $291.77 | $1,750.65 | 65 |
| UNH | 7 | $314.75 | $303.51 | $2,124.61 | 65 |
| UNP | 10 | $236.48 | $236.94 | $2,369.40 | 75 |
| V | 6 | $352.90 | $355.50 | $2,132.97 | 70 |
| VZ | 47 | $43.72 | $42.98 | $2,020.30 | 65 |
| WFC | 30 | $82.26 | $82.72 | $2,481.50 | 80 |
| WMT | 23 | $97.36 | $98.05 | $2,255.19 | 75 |
| XOM | 20 | $109.91 | $111.56 | $2,231.30 | 70 |

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
| 2025-07-07 14:52:46 | BUY | XOM | 1 | $111.84 | N/A | 75 |
| 2025-07-07 14:52:46 | BUY | NKE | 1 | $76.10 | N/A | 75 |
| 2025-07-07 14:52:46 | BUY | MRK | 1 | $81.18 | N/A | 75 |
| 2025-07-07 14:52:46 | BUY | CSCO | 1 | $69.11 | N/A | 75 |
| 2025-07-07 14:52:46 | BUY | VZ | 1 | $42.97 | N/A | 65 |
| 2025-07-07 14:52:46 | BUY | CVX | 2 | $147.73 | N/A | 85 |

<!--TRADE_LOG_END--> 
