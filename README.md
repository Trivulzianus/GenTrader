# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 15:09:29**

| Metric | Value |
|---|---|
| **Total Value** | **$101,502.50** |
| Cash | $1,903.27 |
| Holdings Value | $99,599.23 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.80 | $2,128.00 | 70 |
| ADBE | 5 | $377.60 | $370.46 | $1,852.32 | 65 |
| AMD | 15 | $135.33 | $144.35 | $2,165.25 | 70 |
| AMZN | 11 | $221.90 | $221.15 | $2,432.65 | 75 |
| AVGO | 8 | $275.34 | $273.34 | $2,186.72 | 65 |
| AXP | 7 | $325.28 | $323.19 | $2,262.30 | 75 |
| BA | 9 | $210.97 | $225.89 | $2,033.01 | 65 |
| BAC | 50 | $48.58 | $47.19 | $2,359.49 | 75 |
| C | 26 | $86.81 | $86.70 | $2,254.20 | 70 |
| CAT | 6 | $397.86 | $410.53 | $2,463.18 | 75 |
| COST | 2 | $979.83 | $976.17 | $1,952.34 | 65 |
| CRM | 8 | $268.33 | $266.71 | $2,133.68 | 65 |
| CSCO | 33 | $68.37 | $68.61 | $2,263.97 | 70 |
| CVX | 17 | $147.16 | $154.16 | $2,620.72 | 85 |
| DIS | 18 | $122.80 | $121.74 | $2,191.32 | 70 |
| GOOGL | 13 | $179.61 | $175.63 | $2,283.19 | 75 |
| GS | 3 | $717.52 | $704.53 | $2,113.59 | 70 |
| HD | 6 | $372.64 | $376.26 | $2,257.56 | 65 |
| INTC | 85 | $22.28 | $23.83 | $2,025.55 | 65 |
| JNJ | 13 | $155.89 | $158.95 | $2,066.35 | 65 |
| JPM | 9 | $291.61 | $287.15 | $2,584.35 | 85 |
| KO | 29 | $71.03 | $69.56 | $2,017.10 | 65 |
| LLY | 2 | $776.66 | $798.10 | $1,596.20 | 70 |
| MA | 4 | $563.08 | $564.66 | $2,258.66 | 65 |
| META | 3 | $717.12 | $725.76 | $2,177.28 | 85 |
| MRK | 30 | $82.58 | $84.79 | $2,543.70 | 80 |
| MSFT | 5 | $498.84 | $499.67 | $2,498.36 | 75 |
| NFLX | 1 | $1,279.00 | $1,252.19 | $1,252.19 | 65 |
| NKE | 30 | $75.81 | $74.96 | $2,248.80 | 70 |
| NVDA | 14 | $156.66 | $162.39 | $2,273.46 | 70 |
| ORCL | 9 | $233.31 | $236.22 | $2,125.97 | 70 |
| PEP | 15 | $136.57 | $136.36 | $2,045.40 | 65 |
| PFE | 90 | $25.26 | $26.01 | $2,340.90 | 75 |
| PG | 12 | $160.96 | $158.47 | $1,901.64 | 65 |
| PYPL | 31 | $76.64 | $75.96 | $2,354.76 | 75 |
| QCOM | 15 | $161.72 | $159.69 | $2,395.28 | 75 |
| T | 74 | $28.53 | $27.53 | $2,037.22 | 65 |
| TGT | 20 | $104.89 | $105.81 | $2,116.20 | 65 |
| TSLA | 6 | $288.62 | $305.40 | $1,832.42 | 65 |
| UNH | 6 | $298.34 | $304.40 | $1,826.40 | 65 |
| UNP | 9 | $236.20 | $240.06 | $2,160.54 | 65 |
| V | 6 | $355.85 | $356.62 | $2,139.72 | 65 |
| VZ | 48 | $43.15 | $41.95 | $2,013.84 | 65 |
| WFC | 29 | $82.30 | $82.30 | $2,386.55 | 75 |
| WMT | 21 | $97.35 | $95.94 | $2,014.84 | 65 |
| XOM | 21 | $109.89 | $114.86 | $2,412.06 | 75 |

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
| 2025-07-10 15:09:22 | SELL | NKE | 1 | $74.96 | $-0.82 | 70 |
| 2025-07-10 15:09:22 | SELL | MRK | 1 | $84.80 | $2.15 | 80 |
| 2025-07-10 15:09:22 | SELL | C | 4 | $86.71 | $-0.31 | 70 |
| 2025-07-10 15:09:22 | SELL | CSCO | 1 | $68.58 | $0.21 | 70 |
| 2025-07-10 15:09:22 | SELL | QCOM | 1 | $159.68 | $-1.91 | 75 |
| 2025-07-10 15:09:22 | SELL | UNP | 1 | $240.06 | $3.47 | 65 |
| 2025-07-10 15:09:22 | BUY | GOOGL | 1 | $176.62 | N/A | 75 |
| 2025-07-10 15:09:22 | BUY | BAC | 3 | $47.19 | N/A | 75 |
| 2025-07-10 15:09:22 | BUY | AMD | 1 | $144.44 | N/A | 70 |
| 2025-07-10 15:09:22 | BUY | PFE | 5 | $26.00 | N/A | 75 |
| 2025-07-10 15:09:22 | BUY | CVX | 1 | $154.18 | N/A | 85 |
| 2025-07-10 14:53:46 | SELL | NVDA | 2 | $162.74 | $10.64 | 70 |
| 2025-07-10 14:53:46 | SELL | AMD | 1 | $145.38 | $9.99 | 65 |
| 2025-07-10 14:53:46 | SELL | XOM | 2 | $114.68 | $8.75 | 75 |
| 2025-07-10 14:53:46 | SELL | BAC | 3 | $47.12 | $-4.38 | 70 |
| 2025-07-10 14:53:46 | SELL | PFE | 5 | $25.93 | $3.39 | 70 |
| 2025-07-10 14:53:46 | SELL | WFC | 3 | $82.15 | $-0.42 | 75 |
| 2025-07-10 14:53:46 | SELL | CVX | 1 | $154.09 | $6.94 | 75 |
| 2025-07-10 14:53:46 | BUY | INTC | 5 | $23.76 | N/A | 65 |
| 2025-07-10 14:53:46 | BUY | NKE | 2 | $74.79 | N/A | 75 |
| 2025-07-10 14:53:46 | BUY | MRK | 3 | $84.43 | N/A | 85 |
| 2025-07-10 14:53:46 | BUY | C | 4 | $86.53 | N/A | 85 |
| 2025-07-10 14:53:46 | BUY | CSCO | 1 | $68.72 | N/A | 75 |
| 2025-07-10 14:53:46 | BUY | QCOM | 2 | $159.60 | N/A | 85 |
| 2025-07-10 14:41:37 | SELL | INTC | 6 | $23.87 | $9.37 | 60 |

<!--TRADE_LOG_END--> 
