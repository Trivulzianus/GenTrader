# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 15:26:50**

| Metric | Value |
|---|---|
| **Total Value** | **$101,497.72** |
| Cash | $2,004.73 |
| Holdings Value | $99,492.99 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $213.16 | $2,131.60 | 70 |
| ADBE | 5 | $377.60 | $370.63 | $1,853.15 | 65 |
| AMD | 16 | $135.52 | $143.68 | $2,298.88 | 70 |
| AMZN | 11 | $221.90 | $221.55 | $2,437.05 | 70 |
| AVGO | 8 | $275.34 | $274.46 | $2,195.69 | 70 |
| AXP | 7 | $325.28 | $323.57 | $2,265.01 | 75 |
| BA | 9 | $210.97 | $225.28 | $2,027.57 | 65 |
| BAC | 48 | $48.64 | $47.16 | $2,263.44 | 70 |
| C | 27 | $86.80 | $86.75 | $2,342.12 | 75 |
| CAT | 6 | $397.86 | $411.43 | $2,468.58 | 70 |
| COST | 2 | $979.83 | $974.56 | $1,949.11 | 65 |
| CRM | 8 | $268.33 | $267.39 | $2,139.10 | 65 |
| CSCO | 33 | $68.37 | $68.75 | $2,268.91 | 70 |
| CVX | 17 | $147.16 | $154.31 | $2,623.27 | 85 |
| DIS | 18 | $122.80 | $121.43 | $2,185.74 | 70 |
| GOOGL | 13 | $179.61 | $176.42 | $2,293.41 | 75 |
| GS | 3 | $717.52 | $705.16 | $2,115.48 | 70 |
| HD | 6 | $372.64 | $375.84 | $2,255.04 | 65 |
| INTC | 86 | $22.30 | $23.82 | $2,048.95 | 65 |
| JNJ | 13 | $155.89 | $158.51 | $2,060.63 | 65 |
| JPM | 9 | $291.61 | $286.93 | $2,582.37 | 85 |
| KO | 29 | $71.03 | $69.42 | $2,013.15 | 65 |
| LLY | 2 | $776.66 | $793.47 | $1,586.95 | 70 |
| MA | 4 | $563.08 | $564.64 | $2,258.56 | 70 |
| META | 3 | $717.12 | $727.12 | $2,181.36 | 75 |
| MRK | 29 | $82.51 | $84.47 | $2,449.63 | 75 |
| MSFT | 5 | $498.84 | $500.36 | $2,501.80 | 70 |
| NFLX | 1 | $1,279.00 | $1,254.83 | $1,254.83 | 65 |
| NKE | 28 | $75.86 | $75.19 | $2,105.32 | 65 |
| NVDA | 14 | $156.66 | $162.50 | $2,274.93 | 70 |
| ORCL | 9 | $233.31 | $235.51 | $2,119.59 | 65 |
| PEP | 15 | $136.57 | $136.25 | $2,043.75 | 65 |
| PFE | 80 | $25.17 | $25.96 | $2,076.58 | 65 |
| PG | 13 | $160.77 | $158.54 | $2,061.02 | 65 |
| PYPL | 31 | $76.64 | $76.07 | $2,358.17 | 75 |
| QCOM | 15 | $161.72 | $160.16 | $2,402.47 | 75 |
| T | 75 | $28.52 | $27.52 | $2,064.38 | 65 |
| TGT | 21 | $104.93 | $105.65 | $2,218.65 | 70 |
| TSLA | 6 | $288.62 | $305.16 | $1,830.96 | 60 |
| UNH | 6 | $298.34 | $303.22 | $1,819.32 | 65 |
| UNP | 9 | $236.20 | $239.41 | $2,154.74 | 75 |
| V | 6 | $355.85 | $356.49 | $2,138.94 | 65 |
| VZ | 49 | $43.12 | $42.02 | $2,058.98 | 65 |
| WFC | 29 | $82.30 | $82.25 | $2,385.39 | 75 |
| WMT | 20 | $97.44 | $95.61 | $1,912.17 | 60 |
| XOM | 21 | $109.89 | $115.06 | $2,416.25 | 75 |

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
| 2025-07-10 15:26:42 | SELL | BAC | 2 | $47.16 | $-2.84 | 70 |
| 2025-07-10 15:26:42 | SELL | WMT | 1 | $95.58 | $-1.78 | 60 |
| 2025-07-10 15:26:42 | SELL | PFE | 10 | $25.96 | $7.04 | 65 |
| 2025-07-10 15:26:42 | SELL | NKE | 2 | $75.12 | $-1.37 | 65 |
| 2025-07-10 15:26:42 | SELL | MRK | 1 | $84.43 | $1.85 | 75 |
| 2025-07-10 15:26:42 | BUY | INTC | 1 | $23.83 | N/A | 65 |
| 2025-07-10 15:26:42 | BUY | AMD | 1 | $138.41 | N/A | 70 |
| 2025-07-10 15:26:42 | BUY | C | 1 | $86.74 | N/A | 75 |
| 2025-07-10 15:26:42 | BUY | PG | 1 | $158.56 | N/A | 65 |
| 2025-07-10 15:26:42 | BUY | T | 1 | $27.51 | N/A | 65 |
| 2025-07-10 15:26:42 | BUY | VZ | 1 | $42.01 | N/A | 65 |
| 2025-07-10 15:26:42 | BUY | TGT | 1 | $105.65 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
