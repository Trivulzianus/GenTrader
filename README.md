# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 13:56:17**

| Metric | Value |
|---|---|
| **Total Value** | **$101,255.95** |
| Cash | $546.85 |
| Holdings Value | $100,709.11 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $212.92 | $2,129.20 | 75 |
| ADBE | 5 | $377.60 | $380.15 | $1,900.75 | 65 |
| AMD | 15 | $135.79 | $136.03 | $2,040.45 | 65 |
| AMZN | 11 | $221.66 | $223.84 | $2,462.30 | 75 |
| AVGO | 8 | $269.90 | $276.44 | $2,211.52 | 70 |
| AXP | 8 | $324.34 | $327.65 | $2,621.20 | 75 |
| BA | 10 | $212.15 | $215.72 | $2,157.20 | 70 |
| BAC | 53 | $48.70 | $49.12 | $2,603.60 | 85 |
| C | 25 | $86.43 | $88.69 | $2,217.12 | 75 |
| CAT | 6 | $397.86 | $396.27 | $2,377.62 | 70 |
| COST | 2 | $979.83 | $982.11 | $1,964.21 | 65 |
| CRM | 8 | $268.33 | $273.11 | $2,184.84 | 65 |
| CSCO | 33 | $68.36 | $69.10 | $2,280.30 | 75 |
| CVX | 15 | $146.54 | $147.37 | $2,210.55 | 70 |
| DIS | 17 | $122.82 | $124.45 | $2,115.65 | 70 |
| GOOGL | 13 | $179.40 | $178.16 | $2,316.08 | 75 |
| GS | 3 | $717.52 | $720.84 | $2,162.52 | 75 |
| HD | 6 | $372.64 | $370.43 | $2,222.58 | 65 |
| INTC | 90 | $22.27 | $22.23 | $2,001.15 | 65 |
| JNJ | 13 | $155.80 | $156.09 | $2,029.17 | 65 |
| JPM | 9 | $292.50 | $294.98 | $2,654.82 | 85 |
| KO | 28 | $71.03 | $71.03 | $1,988.98 | 65 |
| LLY | 2 | $776.66 | $765.79 | $1,531.58 | 65 |
| MA | 4 | $563.08 | $569.19 | $2,276.76 | 65 |
| META | 3 | $717.12 | $723.99 | $2,171.97 | 85 |
| MRK | 32 | $82.25 | $80.94 | $2,590.08 | 85 |
| MSFT | 5 | $498.84 | $497.96 | $2,489.80 | 85 |
| NFLX | 1 | $1,279.00 | $1,288.37 | $1,288.37 | 65 |
| NKE | 29 | $75.84 | $76.89 | $2,229.81 | 75 |
| NVDA | 16 | $156.39 | $159.05 | $2,544.80 | 85 |
| ORCL | 10 | $226.66 | $231.46 | $2,314.60 | 70 |
| PEP | 15 | $136.59 | $134.40 | $2,016.00 | 65 |
| PFE | 90 | $25.32 | $25.41 | $2,286.45 | 75 |
| PG | 13 | $160.77 | $160.28 | $2,083.64 | 70 |
| PYPL | 29 | $76.82 | $76.64 | $2,222.56 | 75 |
| QCOM | 14 | $161.69 | $159.31 | $2,230.34 | 75 |
| T | 75 | $28.53 | $28.43 | $2,132.47 | 70 |
| TGT | 19 | $105.09 | $102.51 | $1,947.69 | 65 |
| TSLA | 6 | $288.90 | $290.66 | $1,743.96 | 65 |
| UNH | 7 | $314.75 | $306.51 | $2,145.57 | 65 |
| UNP | 11 | $236.50 | $236.40 | $2,600.40 | 85 |
| V | 6 | $352.90 | $358.43 | $2,150.55 | 65 |
| VZ | 46 | $43.73 | $43.24 | $1,989.27 | 65 |
| WFC | 31 | $82.33 | $83.38 | $2,584.78 | 85 |
| WMT | 21 | $97.28 | $97.94 | $2,056.84 | 65 |
| XOM | 20 | $109.90 | $111.45 | $2,229.01 | 70 |

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
| 2025-07-07 13:56:10 | SELL | AMD | 1 | $137.91 | $1.99 | 65 |
| 2025-07-07 13:56:10 | SELL | WMT | 1 | $98.00 | $0.68 | 65 |
| 2025-07-07 13:56:10 | BUY | TSLA | 6 | $288.90 | N/A | 65 |
| 2025-07-07 13:56:10 | BUY | NKE | 1 | $76.93 | N/A | 75 |
| 2025-07-07 13:56:10 | BUY | PFE | 10 | $25.44 | N/A | 75 |
| 2025-07-07 13:56:10 | BUY | MRK | 8 | $81.08 | N/A | 85 |
| 2025-07-07 13:56:10 | BUY | WFC | 1 | $83.60 | N/A | 85 |
| 2025-07-07 13:56:10 | BUY | T | 5 | $28.46 | N/A | 70 |
| 2025-07-07 13:55:59 | SELL | TSLA | 5 | $288.88 | $-132.35 | 60 |
| 2025-07-07 13:46:03 | SELL | XOM | 1 | $111.39 | $1.42 | 70 |
| 2025-07-07 13:46:03 | SELL | PYPL | 1 | $76.46 | $-0.34 | 70 |
| 2025-07-07 13:46:03 | SELL | PFE | 4 | $25.45 | $0.55 | 65 |
| 2025-07-07 13:46:03 | SELL | C | 4 | $88.65 | $7.67 | 70 |
| 2025-07-07 13:46:03 | SELL | WFC | 1 | $83.47 | $1.15 | 80 |
| 2025-07-07 13:46:03 | SELL | ORCL | 1 | $231.60 | $4.49 | 70 |
| 2025-07-07 13:46:03 | SELL | QCOM | 1 | $159.20 | $-2.32 | 70 |
| 2025-07-07 13:46:03 | SELL | CVX | 2 | $147.30 | $1.34 | 70 |
| 2025-07-07 13:46:03 | BUY | TSLA | 5 | $315.35 | N/A | 60 |
| 2025-07-07 13:46:03 | BUY | GOOGL | 1 | $177.86 | N/A | 75 |
| 2025-07-07 13:46:03 | BUY | AMD | 1 | $135.72 | N/A | 70 |
| 2025-07-07 13:46:03 | BUY | INTC | 8 | $22.21 | N/A | 65 |
| 2025-07-07 13:46:03 | BUY | NKE | 2 | $76.80 | N/A | 70 |
| 2025-07-07 13:46:03 | BUY | WMT | 1 | $98.00 | N/A | 70 |
| 2025-07-07 13:46:03 | BUY | AXP | 1 | $327.69 | N/A | 85 |
| 2025-07-07 13:46:03 | BUY | UNP | 1 | $236.73 | N/A | 85 |

<!--TRADE_LOG_END--> 
