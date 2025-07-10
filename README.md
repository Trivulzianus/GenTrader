# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 15:52:55**

| Metric | Value |
|---|---|
| **Total Value** | **$101,440.63** |
| Cash | $1,674.25 |
| Holdings Value | $99,766.38 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.60 | $2,126.00 | 70 |
| ADBE | 5 | $377.60 | $371.20 | $1,856.00 | 65 |
| AMD | 15 | $134.94 | $144.28 | $2,164.15 | 65 |
| AMZN | 10 | $221.91 | $221.76 | $2,217.60 | 70 |
| AVGO | 8 | $275.34 | $275.04 | $2,200.32 | 70 |
| AXP | 7 | $325.28 | $323.49 | $2,264.43 | 75 |
| BA | 9 | $210.97 | $225.07 | $2,025.63 | 65 |
| BAC | 47 | $48.67 | $47.06 | $2,211.82 | 70 |
| C | 30 | $86.81 | $86.75 | $2,602.50 | 85 |
| CAT | 6 | $397.86 | $410.31 | $2,461.86 | 70 |
| COST | 2 | $979.83 | $979.00 | $1,958.00 | 65 |
| CRM | 8 | $268.33 | $267.46 | $2,139.68 | 65 |
| CSCO | 33 | $68.37 | $68.97 | $2,276.01 | 75 |
| CVX | 17 | $147.16 | $153.28 | $2,605.76 | 85 |
| DIS | 18 | $122.80 | $121.39 | $2,185.02 | 70 |
| GOOGL | 13 | $179.61 | $176.24 | $2,291.12 | 75 |
| GS | 3 | $717.52 | $705.32 | $2,115.96 | 70 |
| HD | 6 | $372.64 | $375.31 | $2,251.83 | 70 |
| INTC | 86 | $22.30 | $23.77 | $2,044.22 | 65 |
| JNJ | 13 | $155.89 | $158.25 | $2,057.32 | 65 |
| JPM | 9 | $291.61 | $286.81 | $2,581.29 | 85 |
| KO | 29 | $71.03 | $69.54 | $2,016.66 | 65 |
| LLY | 2 | $776.66 | $794.19 | $1,588.38 | 65 |
| MA | 4 | $563.08 | $564.72 | $2,258.86 | 70 |
| META | 3 | $717.12 | $726.72 | $2,180.17 | 80 |
| MRK | 28 | $82.45 | $84.30 | $2,360.26 | 75 |
| MSFT | 5 | $498.84 | $500.42 | $2,502.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,264.67 | $1,264.67 | 65 |
| NKE | 29 | $75.82 | $75.03 | $2,175.87 | 70 |
| NVDA | 16 | $157.41 | $163.01 | $2,608.24 | 85 |
| ORCL | 9 | $233.31 | $236.49 | $2,128.37 | 75 |
| PEP | 15 | $136.57 | $136.15 | $2,042.25 | 65 |
| PFE | 79 | $25.16 | $25.83 | $2,040.57 | 65 |
| PG | 13 | $160.77 | $158.72 | $2,063.32 | 65 |
| PYPL | 31 | $76.64 | $75.87 | $2,351.97 | 75 |
| QCOM | 15 | $161.72 | $159.74 | $2,396.10 | 75 |
| T | 74 | $28.53 | $27.59 | $2,041.29 | 65 |
| TGT | 20 | $104.91 | $105.27 | $2,105.30 | 65 |
| TSLA | 6 | $288.62 | $303.85 | $1,823.10 | 60 |
| UNH | 6 | $298.34 | $301.26 | $1,807.56 | 65 |
| UNP | 9 | $236.20 | $238.12 | $2,143.08 | 75 |
| V | 6 | $355.85 | $356.50 | $2,138.97 | 65 |
| VZ | 49 | $43.12 | $42.03 | $2,059.71 | 65 |
| WFC | 29 | $82.30 | $82.34 | $2,388.01 | 75 |
| WMT | 21 | $97.36 | $95.97 | $2,015.47 | 65 |
| XOM | 23 | $110.31 | $114.33 | $2,629.59 | 85 |

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
| 2025-07-10 15:52:49 | SELL | AMZN | 1 | $221.79 | $-0.11 | 70 |
| 2025-07-10 15:52:49 | SELL | AMD | 1 | $144.29 | $8.77 | 65 |
| 2025-07-10 15:52:49 | SELL | BAC | 2 | $47.06 | $-3.10 | 70 |
| 2025-07-10 15:52:49 | SELL | PFE | 5 | $25.83 | $3.11 | 65 |
| 2025-07-10 15:52:49 | SELL | QCOM | 1 | $159.69 | $-1.91 | 75 |
| 2025-07-10 15:52:49 | BUY | NKE | 2 | $75.04 | N/A | 70 |
| 2025-07-10 15:52:49 | BUY | CSCO | 1 | $68.96 | N/A | 75 |
| 2025-07-10 15:40:57 | SELL | MRK | 1 | $84.34 | $1.83 | 75 |
| 2025-07-10 15:40:57 | SELL | NKE | 1 | $75.13 | $-0.73 | 65 |
| 2025-07-10 15:40:57 | SELL | CSCO | 1 | $68.93 | $0.55 | 70 |
| 2025-07-10 15:40:57 | SELL | T | 1 | $27.53 | $-0.98 | 65 |
| 2025-07-10 15:40:57 | SELL | TGT | 1 | $105.33 | $0.41 | 65 |
| 2025-07-10 15:40:57 | BUY | NVDA | 2 | $162.68 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | BAC | 1 | $47.15 | N/A | 75 |
| 2025-07-10 15:40:57 | BUY | XOM | 2 | $114.72 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | PFE | 4 | $25.91 | N/A | 70 |
| 2025-07-10 15:40:57 | BUY | C | 3 | $86.85 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | QCOM | 1 | $159.79 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | WMT | 1 | $95.80 | N/A | 65 |
| 2025-07-10 15:26:42 | SELL | BAC | 2 | $47.16 | $-2.84 | 70 |
| 2025-07-10 15:26:42 | SELL | WMT | 1 | $95.58 | $-1.78 | 60 |
| 2025-07-10 15:26:42 | SELL | PFE | 10 | $25.96 | $7.04 | 65 |
| 2025-07-10 15:26:42 | SELL | NKE | 2 | $75.12 | $-1.37 | 65 |
| 2025-07-10 15:26:42 | SELL | MRK | 1 | $84.43 | $1.85 | 75 |
| 2025-07-10 15:26:42 | BUY | INTC | 1 | $23.83 | N/A | 65 |

<!--TRADE_LOG_END--> 
