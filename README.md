# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 14:52:56**

| Metric | Value |
|---|---|
| **Total Value** | **$101,008.46** |
| Cash | $924.84 |
| Holdings Value | $100,083.63 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $211.98 | $2,119.80 | 70 |
| ADBE | 5 | $377.60 | $377.85 | $1,889.25 | 65 |
| AMD | 15 | $135.79 | $134.36 | $2,015.40 | 65 |
| AMZN | 11 | $221.66 | $223.62 | $2,459.88 | 75 |
| AVGO | 8 | $269.90 | $276.29 | $2,210.32 | 70 |
| AXP | 8 | $324.34 | $326.16 | $2,609.28 | 85 |
| BA | 10 | $212.15 | $215.29 | $2,152.90 | 65 |
| BAC | 54 | $48.71 | $49.15 | $2,654.10 | 85 |
| C | 25 | $86.42 | $88.39 | $2,209.75 | 70 |
| CAT | 6 | $397.86 | $394.50 | $2,367.00 | 85 |
| COST | 2 | $979.83 | $979.12 | $1,958.25 | 60 |
| CRM | 8 | $268.33 | $272.53 | $2,180.24 | 65 |
| CSCO | 34 | $68.38 | $69.11 | $2,349.57 | 75 |
| CVX | 18 | $146.75 | $147.73 | $2,659.07 | 85 |
| DIS | 18 | $122.89 | $123.69 | $2,226.42 | 70 |
| GOOGL | 13 | $179.40 | $176.95 | $2,300.29 | 70 |
| GS | 3 | $717.52 | $721.42 | $2,164.26 | 70 |
| HD | 6 | $372.64 | $369.45 | $2,216.71 | 65 |
| INTC | 86 | $22.27 | $22.14 | $1,904.46 | 60 |
| JNJ | 13 | $155.80 | $155.88 | $2,026.50 | 65 |
| JPM | 9 | $292.50 | $294.17 | $2,647.53 | 85 |
| KO | 28 | $71.03 | $70.92 | $1,985.62 | 65 |
| LLY | 2 | $776.66 | $766.70 | $1,533.40 | 65 |
| MA | 4 | $563.08 | $564.45 | $2,257.78 | 65 |
| META | 3 | $717.12 | $724.83 | $2,174.49 | 75 |
| MRK | 29 | $82.33 | $81.18 | $2,354.22 | 75 |
| MSFT | 5 | $498.84 | $497.38 | $2,486.90 | 70 |
| NFLX | 1 | $1,279.00 | $1,283.76 | $1,283.76 | 65 |
| NKE | 30 | $75.88 | $76.11 | $2,283.30 | 75 |
| NVDA | 16 | $156.40 | $158.31 | $2,532.88 | 85 |
| ORCL | 9 | $226.04 | $232.25 | $2,090.26 | 65 |
| PEP | 15 | $136.59 | $134.32 | $2,014.80 | 60 |
| PFE | 81 | $25.30 | $25.36 | $2,054.57 | 65 |
| PG | 13 | $160.77 | $160.11 | $2,081.46 | 65 |
| PYPL | 30 | $76.81 | $76.78 | $2,303.40 | 75 |
| QCOM | 14 | $161.69 | $158.56 | $2,219.84 | 75 |
| T | 77 | $28.52 | $28.32 | $2,180.26 | 70 |
| TGT | 20 | $104.92 | $101.78 | $2,035.60 | 65 |
| TSLA | 6 | $288.90 | $293.05 | $1,758.27 | 55 |
| UNH | 7 | $314.75 | $304.12 | $2,128.81 | 65 |
| UNP | 10 | $236.48 | $236.90 | $2,369.03 | 75 |
| V | 6 | $352.90 | $355.76 | $2,134.59 | 65 |
| VZ | 47 | $43.72 | $42.98 | $2,020.06 | 65 |
| WFC | 25 | $82.17 | $83.02 | $2,075.50 | 65 |
| WMT | 21 | $97.29 | $97.89 | $2,055.59 | 65 |
| XOM | 21 | $109.99 | $111.82 | $2,348.29 | 75 |

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
| 2025-07-07 14:52:46 | BUY | T | 1 | $28.31 | N/A | 70 |
| 2025-07-07 14:52:46 | BUY | TGT | 1 | $101.75 | N/A | 65 |
| 2025-07-07 14:40:29 | SELL | NVDA | 2 | $158.33 | $3.87 | 70 |
| 2025-07-07 14:40:29 | SELL | DIS | 2 | $123.74 | $1.53 | 70 |
| 2025-07-07 14:40:29 | SELL | NKE | 1 | $76.17 | $0.28 | 70 |
| 2025-07-07 14:40:29 | SELL | UNP | 1 | $236.72 | $0.22 | 75 |
| 2025-07-07 14:40:29 | SELL | CVX | 1 | $147.39 | $0.72 | 75 |
| 2025-07-07 14:40:29 | BUY | INTC | 9 | $22.09 | N/A | 65 |
| 2025-07-07 14:40:29 | BUY | MRK | 1 | $80.83 | N/A | 75 |
| 2025-07-07 14:40:29 | BUY | PFE | 2 | $25.30 | N/A | 70 |
| 2025-07-07 14:40:29 | BUY | C | 5 | $88.32 | N/A | 85 |

<!--TRADE_LOG_END--> 
