# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 19:36:18**

| Metric | Value |
|---|---|
| **Total Value** | **$101,463.37** |
| Cash | $2,197.73 |
| Holdings Value | $99,265.64 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.86 | $2,128.60 | 70 |
| ADBE | 5 | $377.60 | $371.56 | $1,857.80 | 65 |
| AMD | 16 | $135.55 | $143.44 | $2,295.08 | 70 |
| AMZN | 11 | $221.97 | $222.28 | $2,445.08 | 75 |
| AVGO | 8 | $275.34 | $275.72 | $2,205.76 | 70 |
| AXP | 7 | $325.28 | $325.82 | $2,280.74 | 75 |
| BA | 10 | $212.37 | $225.59 | $2,255.95 | 70 |
| BAC | 47 | $48.68 | $46.88 | $2,203.12 | 70 |
| C | 30 | $86.81 | $86.93 | $2,607.90 | 85 |
| CAT | 6 | $397.86 | $408.73 | $2,452.38 | 85 |
| COST | 2 | $979.83 | $976.53 | $1,953.06 | 65 |
| CRM | 7 | $268.68 | $264.71 | $1,853.00 | 65 |
| CSCO | 32 | $68.35 | $68.87 | $2,203.79 | 70 |
| CVX | 17 | $147.15 | $153.79 | $2,614.51 | 85 |
| DIS | 18 | $122.80 | $121.28 | $2,182.95 | 70 |
| GOOGL | 13 | $179.61 | $177.62 | $2,309.12 | 75 |
| GS | 3 | $717.52 | $710.06 | $2,130.17 | 65 |
| HD | 6 | $372.64 | $375.34 | $2,252.04 | 65 |
| INTC | 85 | $22.34 | $23.77 | $2,020.87 | 65 |
| JNJ | 13 | $155.89 | $157.61 | $2,048.93 | 65 |
| JPM | 9 | $291.61 | $288.19 | $2,593.67 | 85 |
| KO | 29 | $71.03 | $69.73 | $2,022.17 | 65 |
| LLY | 2 | $776.66 | $792.32 | $1,584.64 | 65 |
| MA | 4 | $563.08 | $565.02 | $2,260.07 | 65 |
| META | 3 | $717.12 | $726.33 | $2,178.99 | 85 |
| MRK | 28 | $82.46 | $84.33 | $2,361.24 | 75 |
| MSFT | 5 | $498.84 | $501.92 | $2,509.60 | 75 |
| NFLX | 1 | $1,279.00 | $1,254.05 | $1,254.05 | 65 |
| NKE | 29 | $75.83 | $74.67 | $2,165.43 | 70 |
| NVDA | 14 | $156.42 | $164.06 | $2,296.91 | 70 |
| ORCL | 9 | $233.31 | $235.99 | $2,123.91 | 70 |
| PEP | 15 | $136.57 | $135.97 | $2,039.55 | 65 |
| PFE | 80 | $25.15 | $25.76 | $2,060.80 | 65 |
| PG | 13 | $160.78 | $158.49 | $2,060.37 | 65 |
| PYPL | 31 | $76.64 | $75.83 | $2,350.58 | 75 |
| QCOM | 14 | $161.90 | $159.20 | $2,228.80 | 70 |
| T | 73 | $28.55 | $27.67 | $2,019.91 | 65 |
| TGT | 20 | $104.92 | $105.26 | $2,105.20 | 65 |
| TSLA | 6 | $288.62 | $308.87 | $1,853.22 | 65 |
| UNH | 6 | $298.34 | $301.08 | $1,806.51 | 65 |
| UNP | 9 | $236.20 | $237.59 | $2,138.31 | 70 |
| V | 6 | $355.85 | $356.72 | $2,140.32 | 65 |
| VZ | 48 | $43.15 | $42.03 | $2,017.29 | 65 |
| WFC | 29 | $82.30 | $82.36 | $2,388.30 | 75 |
| WMT | 21 | $97.36 | $95.17 | $1,998.47 | 65 |
| XOM | 21 | $109.91 | $114.59 | $2,406.49 | 75 |

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
| 2025-07-10 19:36:09 | SELL | NVDA | 2 | $164.12 | $13.47 | 70 |
| 2025-07-10 19:36:09 | SELL | PFE | 4 | $25.76 | $2.34 | 65 |
| 2025-07-10 19:36:09 | SELL | QCOM | 1 | $159.17 | $-2.55 | 70 |
| 2025-07-10 19:36:09 | SELL | CSCO | 2 | $68.87 | $0.98 | 70 |
| 2025-07-10 19:36:09 | BUY | PYPL | 4 | $75.79 | N/A | 75 |
| 2025-07-10 19:36:09 | BUY | C | 3 | $86.94 | N/A | 85 |
| 2025-07-10 19:24:29 | SELL | BAC | 2 | $46.88 | $-3.46 | 70 |
| 2025-07-10 19:24:29 | SELL | PYPL | 3 | $75.69 | $-2.90 | 65 |
| 2025-07-10 19:24:29 | SELL | C | 3 | $86.83 | $0.10 | 75 |
| 2025-07-10 19:24:29 | BUY | NVDA | 2 | $162.88 | N/A | 85 |
| 2025-07-10 19:24:29 | BUY | INTC | 11 | $23.84 | N/A | 65 |
| 2025-07-10 19:24:29 | BUY | CSCO | 1 | $68.81 | N/A | 75 |
| 2025-07-10 19:07:51 | SELL | INTC | 10 | $23.44 | $11.70 | 55 |
| 2025-07-10 19:07:51 | SELL | WFC | 3 | $82.28 | $-0.06 | 75 |
| 2025-07-10 19:07:51 | BUY | BAC | 2 | $46.89 | N/A | 75 |
| 2025-07-10 19:07:51 | BUY | NKE | 1 | $74.72 | N/A | 70 |
| 2025-07-10 19:07:51 | BUY | PFE | 5 | $25.83 | N/A | 70 |
| 2025-07-10 18:56:32 | SELL | BAC | 2 | $46.85 | $-3.51 | 70 |
| 2025-07-10 18:56:32 | SELL | NKE | 1 | $74.57 | $-1.25 | 65 |
| 2025-07-10 18:56:32 | SELL | PFE | 5 | $25.81 | $3.15 | 65 |
| 2025-07-10 18:56:32 | SELL | QCOM | 1 | $159.48 | $-2.10 | 75 |
| 2025-07-10 18:56:32 | BUY | C | 1 | $86.67 | N/A | 85 |
| 2025-07-10 18:56:32 | BUY | WFC | 1 | $82.15 | N/A | 85 |
| 2025-07-10 18:56:32 | BUY | CSCO | 3 | $68.71 | N/A | 75 |
| 2025-07-10 18:44:41 | SELL | NVDA | 2 | $163.76 | $12.54 | 70 |

<!--TRADE_LOG_END--> 
