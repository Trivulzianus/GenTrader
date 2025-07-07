# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 16:55:28**

| Metric | Value |
|---|---|
| **Total Value** | **$100,531.72** |
| Cash | $990.30 |
| Holdings Value | $99,541.42 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.07 | $210.27 | $2,102.70 | 65 |
| ADBE | 5 | $377.60 | $378.10 | $1,890.48 | 65 |
| AMD | 16 | $135.70 | $134.88 | $2,158.08 | 70 |
| AMZN | 11 | $221.66 | $222.53 | $2,447.83 | 75 |
| AVGO | 8 | $269.90 | $275.12 | $2,200.95 | 70 |
| AXP | 7 | $324.46 | $321.87 | $2,253.09 | 75 |
| BA | 10 | $212.15 | $214.63 | $2,146.30 | 70 |
| BAC | 54 | $48.71 | $48.51 | $2,619.27 | 85 |
| C | 30 | $86.59 | $87.31 | $2,619.30 | 85 |
| CAT | 6 | $397.86 | $389.65 | $2,337.90 | 70 |
| COST | 2 | $979.83 | $988.15 | $1,976.30 | 65 |
| CRM | 8 | $268.33 | $269.67 | $2,157.36 | 65 |
| CSCO | 32 | $68.35 | $68.82 | $2,202.25 | 70 |
| CVX | 16 | $146.72 | $145.81 | $2,332.96 | 75 |
| DIS | 18 | $122.86 | $122.92 | $2,212.56 | 75 |
| GOOGL | 12 | $179.64 | $176.24 | $2,114.88 | 75 |
| GS | 3 | $717.52 | $709.12 | $2,127.37 | 75 |
| HD | 6 | $372.64 | $365.88 | $2,195.25 | 65 |
| INTC | 84 | $22.27 | $22.00 | $1,847.58 | 60 |
| JNJ | 13 | $155.80 | $155.45 | $2,020.85 | 65 |
| JPM | 9 | $292.50 | $290.54 | $2,614.82 | 85 |
| KO | 28 | $71.03 | $71.00 | $1,988.14 | 65 |
| LLY | 2 | $776.66 | $769.50 | $1,538.99 | 70 |
| MA | 4 | $563.08 | $562.21 | $2,248.84 | 65 |
| META | 3 | $717.12 | $720.73 | $2,162.19 | 70 |
| MRK | 29 | $82.38 | $81.17 | $2,354.00 | 75 |
| MSFT | 5 | $498.84 | $496.65 | $2,483.25 | 70 |
| NFLX | 1 | $1,279.00 | $1,288.07 | $1,288.07 | 65 |
| NKE | 29 | $75.85 | $76.17 | $2,208.93 | 70 |
| NVDA | 15 | $156.31 | $158.10 | $2,371.50 | 75 |
| ORCL | 9 | $226.15 | $232.29 | $2,090.61 | 65 |
| PEP | 16 | $136.46 | $134.46 | $2,151.36 | 70 |
| PFE | 80 | $25.31 | $25.23 | $2,018.80 | 65 |
| PG | 13 | $160.77 | $159.80 | $2,077.40 | 70 |
| PYPL | 30 | $76.81 | $75.96 | $2,278.80 | 75 |
| QCOM | 15 | $161.55 | $158.72 | $2,380.80 | 75 |
| T | 76 | $28.53 | $28.32 | $2,152.70 | 70 |
| TGT | 20 | $104.92 | $101.21 | $2,024.20 | 65 |
| TSLA | 6 | $288.90 | $291.71 | $1,750.29 | 65 |
| UNH | 7 | $314.75 | $303.60 | $2,125.20 | 65 |
| UNP | 10 | $236.56 | $234.91 | $2,349.15 | 75 |
| V | 6 | $355.95 | $355.19 | $2,131.11 | 70 |
| VZ | 47 | $43.72 | $42.82 | $2,012.68 | 65 |
| WFC | 28 | $82.27 | $81.83 | $2,291.10 | 75 |
| WMT | 23 | $97.35 | $98.55 | $2,266.65 | 75 |
| XOM | 20 | $109.91 | $110.93 | $2,218.60 | 75 |

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
| 2025-07-07 16:43:14 | SELL | T | 1 | $28.29 | $-0.25 | 65 |
| 2025-07-07 16:43:14 | BUY | UNP | 1 | $235.30 | N/A | 85 |
| 2025-07-07 16:43:14 | BUY | CVX | 1 | $146.25 | N/A | 85 |
| 2025-07-07 16:27:04 | SELL | C | 5 | $87.86 | $5.92 | 70 |
| 2025-07-07 16:27:04 | SELL | ORCL | 1 | $233.19 | $6.34 | 65 |
| 2025-07-07 16:27:04 | SELL | T | 4 | $28.24 | $-1.16 | 65 |
| 2025-07-07 16:27:04 | BUY | AAPL | 1 | $210.76 | N/A | 75 |
| 2025-07-07 16:27:04 | BUY | NKE | 1 | $76.30 | N/A | 75 |
| 2025-07-07 16:27:04 | BUY | WFC | 1 | $82.15 | N/A | 85 |
| 2025-07-07 16:09:30 | SELL | XOM | 1 | $111.44 | $1.46 | 70 |
| 2025-07-07 16:09:30 | SELL | NKE | 2 | $76.50 | $1.23 | 70 |
| 2025-07-07 16:09:30 | SELL | CVX | 1 | $146.43 | $-0.25 | 75 |

<!--TRADE_LOG_END--> 
