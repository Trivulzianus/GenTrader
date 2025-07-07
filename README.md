# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 19:36:24**

| Metric | Value |
|---|---|
| **Total Value** | **$100,621.10** |
| Cash | $722.95 |
| Holdings Value | $99,898.14 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.39 | $2,093.90 | 70 |
| ADBE | 5 | $377.60 | $376.62 | $1,883.10 | 65 |
| AMD | 15 | $135.73 | $135.11 | $2,026.65 | 65 |
| AMZN | 11 | $221.72 | $223.28 | $2,456.13 | 80 |
| AVGO | 8 | $275.34 | $274.81 | $2,198.52 | 70 |
| AXP | 7 | $324.46 | $321.67 | $2,251.66 | 75 |
| BA | 10 | $212.15 | $217.74 | $2,177.35 | 70 |
| BAC | 54 | $48.70 | $48.47 | $2,617.11 | 85 |
| C | 25 | $86.37 | $87.32 | $2,183.04 | 70 |
| CAT | 6 | $397.86 | $390.20 | $2,341.20 | 75 |
| COST | 2 | $979.83 | $990.49 | $1,980.97 | 65 |
| CRM | 8 | $268.33 | $268.96 | $2,151.72 | 65 |
| CSCO | 32 | $68.36 | $68.70 | $2,198.56 | 70 |
| CVX | 17 | $146.71 | $146.79 | $2,495.43 | 85 |
| DIS | 18 | $122.86 | $123.02 | $2,214.36 | 70 |
| GOOGL | 13 | $179.38 | $176.39 | $2,293.07 | 75 |
| GS | 3 | $717.52 | $707.05 | $2,121.14 | 70 |
| HD | 6 | $372.64 | $366.21 | $2,197.29 | 65 |
| INTC | 85 | $22.27 | $21.98 | $1,867.88 | 60 |
| JNJ | 13 | $155.80 | $155.13 | $2,016.69 | 65 |
| JPM | 9 | $292.50 | $291.12 | $2,620.03 | 85 |
| KO | 29 | $71.03 | $70.92 | $2,056.82 | 65 |
| LLY | 2 | $776.66 | $771.78 | $1,543.56 | 65 |
| MA | 4 | $563.08 | $563.14 | $2,252.56 | 65 |
| META | 3 | $717.12 | $719.91 | $2,159.73 | 70 |
| MRK | 28 | $82.42 | $80.96 | $2,266.83 | 75 |
| MSFT | 5 | $498.84 | $496.81 | $2,484.05 | 85 |
| NFLX | 1 | $1,279.00 | $1,289.20 | $1,289.20 | 70 |
| NKE | 30 | $75.86 | $76.55 | $2,296.50 | 75 |
| NVDA | 16 | $156.47 | $158.42 | $2,534.72 | 85 |
| ORCL | 10 | $233.29 | $233.10 | $2,331.00 | 70 |
| PEP | 15 | $136.57 | $134.44 | $2,016.53 | 65 |
| PFE | 81 | $25.30 | $25.22 | $2,042.82 | 65 |
| PG | 13 | $160.77 | $160.31 | $2,083.97 | 65 |
| PYPL | 31 | $76.77 | $76.11 | $2,359.26 | 75 |
| QCOM | 15 | $161.50 | $158.19 | $2,372.78 | 75 |
| T | 72 | $28.54 | $28.39 | $2,043.72 | 65 |
| TGT | 20 | $104.90 | $101.36 | $2,027.20 | 65 |
| TSLA | 7 | $289.38 | $294.59 | $2,062.13 | 60 |
| UNH | 7 | $314.75 | $303.19 | $2,122.33 | 65 |
| UNP | 10 | $236.54 | $234.88 | $2,348.80 | 75 |
| V | 6 | $355.95 | $356.23 | $2,137.38 | 70 |
| VZ | 47 | $43.72 | $42.87 | $2,014.66 | 65 |
| WFC | 29 | $82.26 | $81.80 | $2,372.05 | 75 |
| WMT | 21 | $97.22 | $98.96 | $2,078.16 | 65 |
| XOM | 20 | $109.91 | $110.78 | $2,215.60 | 70 |

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
| 2025-07-07 19:36:19 | SELL | PFE | 5 | $25.21 | $-0.42 | 65 |
| 2025-07-07 19:36:19 | SELL | T | 4 | $28.39 | $-0.59 | 65 |
| 2025-07-07 19:36:19 | BUY | NVDA | 2 | $158.40 | N/A | 85 |
| 2025-07-07 19:36:19 | BUY | NKE | 1 | $76.54 | N/A | 75 |
| 2025-07-07 19:36:19 | BUY | CVX | 1 | $146.75 | N/A | 85 |
| 2025-07-07 19:25:04 | SELL | AAPL | 1 | $209.43 | $-1.49 | 65 |
| 2025-07-07 19:25:04 | SELL | NKE | 1 | $76.50 | $0.64 | 70 |
| 2025-07-07 19:25:04 | SELL | C | 5 | $87.36 | $4.12 | 70 |
| 2025-07-07 19:25:04 | SELL | UNP | 1 | $234.88 | $-1.52 | 75 |
| 2025-07-07 19:25:04 | SELL | CSCO | 1 | $68.71 | $0.34 | 70 |
| 2025-07-07 19:25:04 | SELL | CVX | 1 | $146.66 | $-0.04 | 75 |
| 2025-07-07 19:25:04 | BUY | INTC | 1 | $21.92 | N/A | 60 |
| 2025-07-07 19:25:04 | BUY | MRK | 3 | $81.01 | N/A | 75 |
| 2025-07-07 19:25:04 | BUY | PFE | 2 | $25.23 | N/A | 70 |
| 2025-07-07 19:25:04 | BUY | ORCL | 1 | $233.21 | N/A | 75 |
| 2025-07-07 19:25:04 | BUY | T | 5 | $28.38 | N/A | 70 |
| 2025-07-07 19:07:47 | SELL | NVDA | 2 | $158.38 | $3.82 | 70 |
| 2025-07-07 19:07:47 | SELL | MRK | 4 | $81.07 | $-5.20 | 65 |
| 2025-07-07 19:07:47 | SELL | T | 4 | $28.39 | $-0.58 | 65 |
| 2025-07-07 19:07:47 | BUY | UNP | 1 | $234.74 | N/A | 85 |
| 2025-07-07 19:07:47 | BUY | CSCO | 1 | $68.82 | N/A | 75 |
| 2025-07-07 19:07:47 | BUY | CVX | 1 | $146.43 | N/A | 85 |
| 2025-07-07 18:56:26 | SELL | INTC | 1 | $21.93 | $-0.34 | 60 |
| 2025-07-07 18:56:26 | SELL | XOM | 1 | $110.74 | $0.79 | 70 |
| 2025-07-07 18:56:26 | SELL | WMT | 1 | $98.36 | $1.09 | 65 |

<!--TRADE_LOG_END--> 
