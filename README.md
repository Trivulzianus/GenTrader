# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 19:07:58**

| Metric | Value |
|---|---|
| **Total Value** | **$101,487.52** |
| Cash | $2,109.03 |
| Holdings Value | $99,378.49 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.93 | $2,129.26 | 70 |
| ADBE | 5 | $377.60 | $372.64 | $1,863.22 | 65 |
| AMD | 16 | $135.55 | $143.61 | $2,297.78 | 70 |
| AMZN | 11 | $221.97 | $222.19 | $2,444.03 | 75 |
| AVGO | 8 | $275.34 | $275.39 | $2,203.12 | 70 |
| AXP | 7 | $325.28 | $325.32 | $2,277.28 | 75 |
| BA | 10 | $212.37 | $225.46 | $2,254.55 | 70 |
| BAC | 49 | $48.61 | $46.89 | $2,297.61 | 75 |
| C | 30 | $86.80 | $86.75 | $2,602.65 | 85 |
| CAT | 6 | $397.86 | $409.03 | $2,454.18 | 70 |
| COST | 2 | $979.83 | $978.32 | $1,956.64 | 65 |
| CRM | 7 | $268.68 | $265.65 | $1,859.55 | 60 |
| CSCO | 33 | $68.37 | $68.72 | $2,267.92 | 75 |
| CVX | 17 | $147.15 | $153.88 | $2,615.96 | 85 |
| DIS | 18 | $122.80 | $121.05 | $2,178.90 | 70 |
| GOOGL | 13 | $179.61 | $177.63 | $2,309.19 | 75 |
| GS | 3 | $717.52 | $708.90 | $2,126.70 | 75 |
| HD | 6 | $372.64 | $376.51 | $2,259.06 | 70 |
| INTC | 74 | $22.11 | $23.90 | $1,768.50 | 55 |
| JNJ | 13 | $155.89 | $157.58 | $2,048.54 | 65 |
| JPM | 9 | $291.61 | $287.86 | $2,590.74 | 85 |
| KO | 29 | $71.03 | $69.66 | $2,020.14 | 65 |
| LLY | 2 | $776.66 | $793.03 | $1,586.06 | 70 |
| MA | 4 | $563.08 | $563.48 | $2,253.90 | 65 |
| META | 3 | $717.12 | $724.98 | $2,174.94 | 85 |
| MRK | 28 | $82.46 | $84.68 | $2,371.04 | 75 |
| MSFT | 5 | $498.84 | $501.64 | $2,508.20 | 85 |
| NFLX | 1 | $1,279.00 | $1,252.68 | $1,252.68 | 65 |
| NKE | 29 | $75.83 | $74.72 | $2,166.88 | 70 |
| NVDA | 14 | $156.60 | $163.79 | $2,293.06 | 70 |
| ORCL | 9 | $233.31 | $236.61 | $2,129.47 | 70 |
| PEP | 15 | $136.57 | $135.97 | $2,039.62 | 65 |
| PFE | 84 | $25.18 | $25.84 | $2,170.14 | 70 |
| PG | 13 | $160.78 | $158.69 | $2,062.97 | 65 |
| PYPL | 30 | $76.66 | $75.73 | $2,271.91 | 75 |
| QCOM | 15 | $161.72 | $159.56 | $2,393.40 | 75 |
| T | 73 | $28.55 | $27.62 | $2,016.62 | 65 |
| TGT | 20 | $104.92 | $105.55 | $2,111.00 | 65 |
| TSLA | 6 | $288.62 | $309.40 | $1,856.43 | 65 |
| UNH | 6 | $298.34 | $301.46 | $1,808.76 | 65 |
| UNP | 9 | $236.20 | $238.00 | $2,142.05 | 75 |
| V | 6 | $355.85 | $356.23 | $2,137.38 | 65 |
| VZ | 48 | $43.15 | $42.03 | $2,017.44 | 65 |
| WFC | 29 | $82.30 | $82.28 | $2,386.26 | 75 |
| WMT | 21 | $97.36 | $95.06 | $1,996.37 | 65 |
| XOM | 21 | $109.91 | $114.59 | $2,406.39 | 80 |

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
| 2025-07-10 18:44:41 | SELL | AMD | 2 | $143.91 | $14.87 | 70 |
| 2025-07-10 18:44:41 | SELL | C | 1 | $86.80 | $-0.01 | 80 |
| 2025-07-10 18:44:41 | SELL | CSCO | 2 | $68.75 | $0.78 | 65 |
| 2025-07-10 18:44:41 | BUY | INTC | 6 | $23.95 | N/A | 65 |
| 2025-07-10 18:44:41 | BUY | PFE | 6 | $25.85 | N/A | 70 |
| 2025-07-10 18:44:41 | BUY | NKE | 2 | $74.89 | N/A | 70 |
| 2025-07-10 18:44:41 | BUY | QCOM | 1 | $159.70 | N/A | 85 |
| 2025-07-10 18:27:27 | SELL | NKE | 2 | $75.06 | $-1.55 | 65 |
| 2025-07-10 18:27:27 | SELL | INTC | 6 | $23.91 | $9.83 | 60 |
| 2025-07-10 18:27:27 | SELL | PFE | 12 | $25.90 | $8.03 | 65 |
| 2025-07-10 18:27:27 | SELL | CSCO | 1 | $68.85 | $0.47 | 70 |
| 2025-07-10 18:27:27 | SELL | QCOM | 1 | $159.75 | $-1.83 | 75 |

<!--TRADE_LOG_END--> 
