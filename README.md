# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 17:26:09**

| Metric | Value |
|---|---|
| **Total Value** | **$100,831.88** |
| Cash | $772.38 |
| Holdings Value | $100,059.50 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.15 | $2,091.50 | 65 |
| ADBE | 6 | $375.23 | $365.67 | $2,193.99 | 65 |
| AMD | 16 | $135.48 | $146.77 | $2,348.32 | 75 |
| AMZN | 11 | $221.92 | $225.75 | $2,483.20 | 85 |
| AVGO | 8 | $275.34 | $276.33 | $2,210.68 | 70 |
| AXP | 7 | $325.34 | $320.37 | $2,242.59 | 75 |
| BA | 10 | $212.67 | $229.62 | $2,296.25 | 70 |
| BAC | 47 | $48.71 | $46.95 | $2,206.65 | 70 |
| C | 31 | $86.64 | $87.27 | $2,705.22 | 85 |
| CAT | 6 | $397.74 | $403.96 | $2,423.76 | 70 |
| COST | 2 | $979.83 | $976.09 | $1,952.17 | 70 |
| CRM | 7 | $268.68 | $260.86 | $1,826.02 | 65 |
| CSCO | 32 | $68.45 | $67.68 | $2,165.90 | 70 |
| CVX | 16 | $146.79 | $151.62 | $2,425.92 | 75 |
| DIS | 18 | $122.80 | $120.31 | $2,165.62 | 70 |
| GOOGL | 13 | $179.57 | $181.16 | $2,355.08 | 70 |
| GS | 3 | $717.52 | $712.10 | $2,136.30 | 70 |
| HD | 6 | $372.64 | $368.21 | $2,209.26 | 65 |
| INTC | 82 | $22.33 | $23.13 | $1,896.71 | 60 |
| JNJ | 13 | $155.95 | $156.54 | $2,035.02 | 65 |
| JPM | 9 | $291.63 | $288.90 | $2,600.10 | 85 |
| KO | 29 | $71.03 | $69.52 | $2,015.93 | 65 |
| LLY | 3 | $781.32 | $798.75 | $2,396.25 | 75 |
| MA | 4 | $563.08 | $554.79 | $2,219.16 | 65 |
| META | 3 | $717.12 | $724.00 | $2,172.00 | 85 |
| MRK | 28 | $82.49 | $83.81 | $2,346.82 | 75 |
| MSFT | 5 | $498.84 | $502.82 | $2,514.10 | 75 |
| NFLX | 1 | $1,279.00 | $1,269.13 | $1,269.13 | 70 |
| NKE | 29 | $72.04 | $72.27 | $2,095.80 | 65 |
| NVDA | 14 | $156.62 | $165.16 | $2,312.17 | 75 |
| ORCL | 9 | $233.26 | $229.93 | $2,069.37 | 65 |
| PEP | 15 | $136.57 | $135.80 | $2,037.00 | 65 |
| PFE | 86 | $25.21 | $25.48 | $2,191.29 | 70 |
| PG | 13 | $160.78 | $154.01 | $2,002.13 | 65 |
| PYPL | 28 | $72.11 | $73.79 | $2,066.12 | 65 |
| QCOM | 14 | $153.83 | $154.14 | $2,157.96 | 65 |
| T | 75 | $27.10 | $27.14 | $2,035.88 | 65 |
| TGT | 20 | $104.94 | $104.58 | $2,091.60 | 65 |
| TSLA | 6 | $288.62 | $315.62 | $1,893.69 | 65 |
| UNH | 7 | $298.51 | $299.86 | $2,099.02 | 65 |
| UNP | 10 | $236.29 | $233.57 | $2,335.75 | 75 |
| V | 6 | $355.85 | $351.02 | $2,106.15 | 65 |
| VZ | 49 | $43.12 | $41.51 | $2,033.99 | 65 |
| WFC | 28 | $82.26 | $83.32 | $2,332.96 | 75 |
| WMT | 20 | $97.47 | $95.58 | $1,911.70 | 60 |
| XOM | 21 | $110.01 | $113.49 | $2,383.29 | 75 |

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
| 2025-07-14 17:26:00 | SELL | PYPL | 4 | $73.79 | $5.89 | 65 |
| 2025-07-14 17:26:00 | SELL | WMT | 1 | $95.60 | $-1.79 | 60 |
| 2025-07-14 17:26:00 | BUY | AMD | 1 | $146.83 | N/A | 75 |
| 2025-07-14 17:09:36 | SELL | NVDA | 2 | $165.10 | $14.84 | 70 |
| 2025-07-14 17:09:36 | SELL | INTC | 6 | $23.15 | $4.58 | 60 |
| 2025-07-14 17:09:36 | BUY | PYPL | 4 | $73.64 | N/A | 75 |
| 2025-07-14 17:09:36 | BUY | QCOM | 1 | $154.25 | N/A | 70 |
| 2025-07-14 17:09:36 | BUY | CSCO | 1 | $67.62 | N/A | 70 |
| 2025-07-14 16:56:14 | SELL | NKE | 3 | $72.29 | $0.69 | 65 |
| 2025-07-14 16:56:14 | SELL | CSCO | 1 | $67.55 | $-0.90 | 65 |
| 2025-07-14 16:56:14 | BUY | INTC | 7 | $23.15 | N/A | 65 |
| 2025-07-14 16:56:14 | BUY | MRK | 1 | $83.74 | N/A | 75 |
| 2025-07-14 16:43:44 | SELL | INTC | 7 | $23.15 | $5.33 | 60 |
| 2025-07-14 16:43:44 | SELL | PYPL | 1 | $73.69 | $1.51 | 65 |
| 2025-07-14 16:43:44 | SELL | PFE | 6 | $25.49 | $1.56 | 70 |
| 2025-07-14 16:43:44 | SELL | MRK | 1 | $83.53 | $1.04 | 70 |
| 2025-07-14 16:43:44 | BUY | WFC | 1 | $83.14 | N/A | 75 |
| 2025-07-14 16:43:44 | BUY | UNP | 1 | $233.19 | N/A | 75 |
| 2025-07-14 16:43:44 | BUY | CSCO | 1 | $67.48 | N/A | 70 |
| 2025-07-14 16:27:18 | SELL | WFC | 1 | $83.16 | $0.90 | 70 |
| 2025-07-14 16:27:18 | SELL | BA | 1 | $229.86 | $15.63 | 70 |
| 2025-07-14 16:27:18 | SELL | UNP | 1 | $232.96 | $-3.31 | 65 |
| 2025-07-14 16:27:18 | BUY | INTC | 1 | $23.12 | N/A | 65 |
| 2025-07-14 16:27:18 | BUY | PYPL | 1 | $73.61 | N/A | 70 |
| 2025-07-14 16:27:18 | BUY | MRK | 2 | $83.43 | N/A | 75 |

<!--TRADE_LOG_END--> 
