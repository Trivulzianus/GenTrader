# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 15:26:33**

| Metric | Value |
|---|---|
| **Total Value** | **$100,672.17** |
| Cash | $516.58 |
| Holdings Value | $100,155.59 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.67 | $2,086.70 | 65 |
| ADBE | 6 | $375.23 | $364.89 | $2,189.32 | 65 |
| AMD | 14 | $133.89 | $145.43 | $2,036.02 | 65 |
| AMZN | 11 | $221.92 | $225.82 | $2,484.02 | 75 |
| AVGO | 8 | $275.34 | $275.71 | $2,205.68 | 70 |
| AXP | 7 | $325.34 | $320.52 | $2,243.64 | 75 |
| BA | 10 | $212.59 | $229.14 | $2,291.40 | 75 |
| BAC | 46 | $48.75 | $46.81 | $2,153.18 | 70 |
| C | 31 | $86.64 | $87.00 | $2,696.85 | 85 |
| CAT | 6 | $397.74 | $402.89 | $2,417.34 | 70 |
| COST | 2 | $979.83 | $974.56 | $1,949.12 | 65 |
| CRM | 7 | $268.68 | $260.00 | $1,820.00 | 65 |
| CSCO | 31 | $68.48 | $67.31 | $2,086.46 | 65 |
| CVX | 17 | $147.10 | $152.32 | $2,589.44 | 85 |
| DIS | 18 | $122.79 | $120.00 | $2,159.91 | 70 |
| GOOGL | 13 | $179.57 | $180.71 | $2,349.23 | 75 |
| GS | 3 | $717.52 | $711.04 | $2,133.11 | 75 |
| HD | 6 | $372.64 | $368.17 | $2,209.02 | 65 |
| INTC | 82 | $22.33 | $23.14 | $1,897.07 | 60 |
| JNJ | 13 | $155.95 | $156.01 | $2,028.19 | 65 |
| JPM | 9 | $291.63 | $287.85 | $2,590.61 | 85 |
| KO | 29 | $71.03 | $69.79 | $2,023.91 | 65 |
| LLY | 3 | $781.32 | $794.83 | $2,384.48 | 75 |
| MA | 4 | $563.08 | $555.72 | $2,222.88 | 65 |
| META | 3 | $717.12 | $724.60 | $2,173.78 | 70 |
| MRK | 29 | $82.52 | $83.57 | $2,423.47 | 75 |
| MSFT | 5 | $498.84 | $502.88 | $2,514.39 | 85 |
| NFLX | 1 | $1,279.00 | $1,266.64 | $1,266.64 | 65 |
| NKE | 32 | $72.08 | $72.44 | $2,318.08 | 75 |
| NVDA | 16 | $157.68 | $164.79 | $2,636.64 | 85 |
| ORCL | 9 | $233.26 | $228.51 | $2,056.59 | 65 |
| PEP | 15 | $136.57 | $134.72 | $2,020.80 | 65 |
| PFE | 87 | $25.21 | $25.46 | $2,215.02 | 70 |
| PG | 13 | $160.78 | $153.63 | $1,997.19 | 65 |
| PYPL | 30 | $72.23 | $73.69 | $2,210.70 | 70 |
| QCOM | 13 | $153.79 | $153.71 | $1,998.23 | 65 |
| T | 75 | $27.10 | $27.25 | $2,043.75 | 65 |
| TGT | 20 | $104.94 | $104.53 | $2,090.50 | 65 |
| TSLA | 6 | $288.62 | $314.20 | $1,885.20 | 60 |
| UNH | 7 | $298.51 | $299.71 | $2,097.97 | 65 |
| UNP | 9 | $236.60 | $232.40 | $2,091.60 | 65 |
| V | 6 | $355.85 | $351.68 | $2,110.08 | 65 |
| VZ | 49 | $43.12 | $41.70 | $2,043.30 | 65 |
| WFC | 28 | $82.26 | $82.97 | $2,323.30 | 75 |
| WMT | 21 | $97.38 | $95.39 | $2,003.29 | 65 |
| XOM | 21 | $110.01 | $113.69 | $2,387.49 | 75 |

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
| 2025-07-14 15:26:28 | SELL | PYPL | 1 | $73.74 | $1.46 | 70 |
| 2025-07-14 15:26:28 | SELL | PFE | 5 | $25.46 | $1.18 | 70 |
| 2025-07-14 15:26:28 | SELL | UNP | 1 | $232.40 | $-3.78 | 65 |
| 2025-07-14 15:26:28 | SELL | CSCO | 1 | $67.31 | $-1.14 | 65 |
| 2025-07-14 15:26:28 | BUY | BAC | 2 | $46.81 | N/A | 70 |
| 2025-07-14 15:26:28 | BUY | CVX | 1 | $152.33 | N/A | 85 |
| 2025-07-14 15:09:27 | SELL | INTC | 6 | $23.11 | $4.39 | 60 |
| 2025-07-14 15:09:27 | SELL | BAC | 3 | $46.76 | $-5.84 | 65 |
| 2025-07-14 15:09:27 | BUY | PFE | 6 | $25.44 | N/A | 75 |
| 2025-07-14 15:09:27 | BUY | CSCO | 2 | $67.95 | N/A | 70 |
| 2025-07-14 14:53:08 | SELL | GOOGL | 1 | $180.70 | $1.05 | 75 |
| 2025-07-14 14:53:08 | SELL | AMD | 1 | $144.98 | $10.35 | 65 |
| 2025-07-14 14:53:08 | SELL | INTC | 1 | $23.10 | $0.71 | 65 |
| 2025-07-14 14:53:08 | SELL | TGT | 1 | $103.82 | $-1.06 | 65 |
| 2025-07-14 14:53:08 | BUY | NVDA | 3 | $164.12 | N/A | 85 |
| 2025-07-14 14:53:08 | BUY | DIS | 1 | $119.82 | N/A | 70 |
| 2025-07-14 14:53:08 | BUY | PYPL | 1 | $73.98 | N/A | 75 |
| 2025-07-14 14:53:08 | BUY | MRK | 1 | $83.46 | N/A | 80 |
| 2025-07-14 14:53:08 | BUY | NKE | 3 | $72.06 | N/A | 75 |
| 2025-07-14 14:53:08 | BUY | CAT | 1 | $404.48 | N/A | 85 |
| 2025-07-14 14:53:08 | BUY | QCOM | 13 | $153.79 | N/A | 65 |
| 2025-07-14 14:52:53 | SELL | QCOM | 14 | $153.75 | $-116.71 | 65 |
| 2025-07-14 14:41:26 | SELL | NVDA | 2 | $163.70 | $13.00 | 65 |
| 2025-07-14 14:41:26 | SELL | NKE | 1 | $72.14 | $0.06 | 65 |
| 2025-07-14 14:41:26 | SELL | PYPL | 1 | $74.27 | $1.99 | 70 |

<!--TRADE_LOG_END--> 
