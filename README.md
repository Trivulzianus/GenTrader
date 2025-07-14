# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 16:43:50**

| Metric | Value |
|---|---|
| **Total Value** | **$100,734.36** |
| Cash | $537.11 |
| Holdings Value | $100,197.25 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.05 | $2,090.53 | 65 |
| ADBE | 6 | $375.23 | $364.92 | $2,189.49 | 60 |
| AMD | 15 | $134.72 | $146.52 | $2,197.80 | 70 |
| AMZN | 11 | $221.92 | $225.94 | $2,485.28 | 85 |
| AVGO | 8 | $275.34 | $275.95 | $2,207.60 | 70 |
| AXP | 7 | $325.34 | $320.43 | $2,243.01 | 75 |
| BA | 10 | $212.67 | $229.39 | $2,293.90 | 70 |
| BAC | 47 | $48.71 | $46.80 | $2,199.60 | 70 |
| C | 31 | $86.64 | $86.89 | $2,693.43 | 85 |
| CAT | 6 | $397.74 | $403.71 | $2,422.29 | 70 |
| COST | 2 | $979.83 | $974.15 | $1,948.30 | 65 |
| CRM | 7 | $268.68 | $261.02 | $1,827.17 | 65 |
| CSCO | 32 | $68.45 | $67.48 | $2,159.52 | 70 |
| CVX | 16 | $146.79 | $151.73 | $2,427.68 | 75 |
| DIS | 18 | $122.80 | $120.21 | $2,163.78 | 70 |
| GOOGL | 13 | $179.57 | $180.62 | $2,348.12 | 70 |
| GS | 3 | $717.52 | $711.21 | $2,133.62 | 75 |
| HD | 6 | $372.64 | $367.76 | $2,206.56 | 70 |
| INTC | 81 | $22.32 | $23.14 | $1,874.34 | 60 |
| JNJ | 13 | $155.95 | $156.11 | $2,029.43 | 65 |
| JPM | 9 | $291.63 | $288.04 | $2,592.32 | 85 |
| KO | 29 | $71.03 | $69.67 | $2,020.29 | 65 |
| LLY | 3 | $781.32 | $796.52 | $2,389.56 | 75 |
| MA | 4 | $563.08 | $555.53 | $2,222.12 | 65 |
| META | 3 | $717.12 | $725.18 | $2,175.54 | 70 |
| MRK | 27 | $82.45 | $83.55 | $2,255.85 | 70 |
| MSFT | 5 | $498.84 | $502.91 | $2,514.55 | 85 |
| NFLX | 1 | $1,279.00 | $1,265.10 | $1,265.10 | 65 |
| NKE | 32 | $72.06 | $72.20 | $2,310.56 | 75 |
| NVDA | 16 | $157.68 | $164.88 | $2,638.08 | 85 |
| ORCL | 9 | $233.26 | $230.31 | $2,072.74 | 70 |
| PEP | 15 | $136.57 | $135.60 | $2,034.00 | 65 |
| PFE | 86 | $25.21 | $25.48 | $2,191.71 | 70 |
| PG | 13 | $160.78 | $153.62 | $1,997.06 | 65 |
| PYPL | 28 | $72.13 | $73.70 | $2,063.60 | 65 |
| QCOM | 13 | $153.79 | $153.89 | $2,000.57 | 65 |
| T | 75 | $27.10 | $27.18 | $2,038.12 | 65 |
| TGT | 20 | $104.94 | $104.74 | $2,094.80 | 65 |
| TSLA | 6 | $288.62 | $315.69 | $1,894.14 | 65 |
| UNH | 7 | $298.51 | $299.70 | $2,097.90 | 65 |
| UNP | 10 | $236.29 | $233.19 | $2,331.90 | 75 |
| V | 6 | $355.85 | $350.85 | $2,105.07 | 70 |
| VZ | 49 | $43.12 | $41.58 | $2,037.42 | 65 |
| WFC | 28 | $82.26 | $83.15 | $2,328.20 | 75 |
| WMT | 21 | $97.38 | $95.49 | $2,005.29 | 65 |
| XOM | 21 | $110.01 | $113.30 | $2,379.30 | 75 |

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
| 2025-07-14 16:27:18 | BUY | NKE | 3 | $72.23 | N/A | 75 |
| 2025-07-14 16:27:18 | BUY | PFE | 6 | $25.49 | N/A | 75 |
| 2025-07-14 16:09:59 | SELL | PYPL | 2 | $73.56 | $2.66 | 65 |
| 2025-07-14 16:09:59 | SELL | NKE | 2 | $72.37 | $0.60 | 65 |
| 2025-07-14 16:09:59 | SELL | CVX | 1 | $152.08 | $4.98 | 75 |
| 2025-07-14 16:09:59 | BUY | BAC | 1 | $46.73 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | AMD | 1 | $146.40 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | DIS | 1 | $120.31 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | MRK | 1 | $83.47 | N/A | 70 |
| 2025-07-14 16:09:59 | BUY | UNP | 1 | $233.26 | N/A | 75 |
| 2025-07-14 15:52:17 | SELL | DIS | 1 | $120.24 | $-2.56 | 65 |
| 2025-07-14 15:52:17 | SELL | MRK | 3 | $83.36 | $2.65 | 65 |

<!--TRADE_LOG_END--> 
