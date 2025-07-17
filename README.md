# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 18:11:26**

| Metric | Value |
|---|---|
| **Total Value** | **$101,296.67** |
| Cash | $346.82 |
| Holdings Value | $100,949.85 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.24 | $2,112.40 | 65 |
| ADBE | 6 | $375.23 | $366.03 | $2,196.18 | 65 |
| AMD | 14 | $160.03 | $159.19 | $2,228.66 | 70 |
| AMZN | 10 | $221.65 | $223.81 | $2,238.15 | 75 |
| AVGO | 8 | $275.34 | $286.24 | $2,289.92 | 65 |
| AXP | 7 | $309.18 | $315.27 | $2,206.92 | 75 |
| BA | 9 | $210.81 | $230.82 | $2,077.38 | 65 |
| BAC | 45 | $46.25 | $47.01 | $2,115.46 | 65 |
| C | 30 | $86.85 | $92.67 | $2,779.95 | 85 |
| CAT | 6 | $397.74 | $418.26 | $2,509.56 | 70 |
| COST | 2 | $979.83 | $951.89 | $1,903.78 | 65 |
| CRM | 8 | $267.44 | $258.72 | $2,069.76 | 65 |
| CSCO | 31 | $68.58 | $68.27 | $2,116.37 | 65 |
| CVX | 16 | $146.82 | $151.00 | $2,416.00 | 75 |
| DIS | 20 | $122.61 | $121.46 | $2,429.20 | 75 |
| GOOGL | 13 | $179.34 | $183.64 | $2,387.32 | 70 |
| GS | 3 | $717.52 | $709.39 | $2,128.17 | 70 |
| HD | 6 | $354.18 | $358.70 | $2,152.20 | 65 |
| INTC | 84 | $22.34 | $22.82 | $1,916.71 | 60 |
| JNJ | 13 | $155.43 | $163.50 | $2,125.43 | 70 |
| JPM | 9 | $291.90 | $288.68 | $2,598.12 | 85 |
| KO | 30 | $70.97 | $69.80 | $2,093.85 | 65 |
| LLY | 3 | $781.32 | $760.61 | $2,281.83 | 65 |
| MA | 4 | $563.08 | $553.88 | $2,215.53 | 65 |
| META | 3 | $717.12 | $701.14 | $2,103.42 | 70 |
| MRK | 29 | $82.56 | $81.42 | $2,361.04 | 75 |
| MSFT | 5 | $498.84 | $512.04 | $2,560.20 | 70 |
| NFLX | 1 | $1,279.00 | $1,270.79 | $1,270.79 | 65 |
| NKE | 31 | $71.96 | $72.97 | $2,262.13 | 70 |
| NVDA | 15 | $171.77 | $173.23 | $2,598.45 | 85 |
| ORCL | 9 | $232.91 | $246.88 | $2,221.97 | 65 |
| PEP | 16 | $136.49 | $144.62 | $2,313.92 | 75 |
| PFE | 85 | $25.27 | $24.49 | $2,081.36 | 65 |
| PG | 14 | $152.18 | $155.03 | $2,170.36 | 65 |
| PYPL | 30 | $72.23 | $73.72 | $2,211.60 | 70 |
| QCOM | 14 | $153.83 | $152.85 | $2,139.90 | 65 |
| T | 77 | $27.09 | $27.00 | $2,078.62 | 65 |
| TGT | 20 | $104.83 | $103.60 | $2,071.99 | 65 |
| TSLA | 6 | $318.51 | $318.41 | $1,910.47 | 65 |
| UNH | 7 | $298.51 | $288.55 | $2,019.85 | 65 |
| UNP | 10 | $236.33 | $227.74 | $2,277.40 | 65 |
| V | 6 | $355.85 | $349.67 | $2,098.02 | 65 |
| VZ | 50 | $40.87 | $40.98 | $2,048.85 | 65 |
| WFC | 28 | $78.77 | $79.72 | $2,232.02 | 70 |
| WMT | 22 | $97.29 | $95.22 | $2,094.84 | 65 |
| XOM | 20 | $109.89 | $111.69 | $2,233.80 | 70 |

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
| 2025-07-17 18:11:19 | SELL | DIS | 2 | $121.50 | $-2.02 | 75 |
| 2025-07-17 18:11:19 | SELL | NKE | 1 | $72.98 | $0.99 | 70 |
| 2025-07-17 18:11:19 | SELL | CSCO | 2 | $68.28 | $-0.57 | 65 |
| 2025-07-17 18:11:19 | BUY | XOM | 1 | $111.70 | N/A | 70 |
| 2025-07-17 18:11:19 | BUY | PFE | 1 | $24.49 | N/A | 65 |
| 2025-07-17 18:11:19 | BUY | WFC | 2 | $79.68 | N/A | 70 |
| 2025-07-17 18:11:19 | BUY | PYPL | 2 | $73.74 | N/A | 70 |
| 2025-07-17 17:51:42 | SELL | XOM | 2 | $111.62 | $3.31 | 65 |
| 2025-07-17 17:51:42 | SELL | WFC | 2 | $79.84 | $2.13 | 65 |
| 2025-07-17 17:51:42 | BUY | NVDA | 2 | $173.15 | N/A | 85 |
| 2025-07-17 17:51:42 | BUY | NKE | 3 | $73.08 | N/A | 75 |
| 2025-07-17 17:51:42 | BUY | MRK | 1 | $81.60 | N/A | 75 |
| 2025-07-17 17:40:27 | SELL | MRK | 1 | $81.55 | $-1.01 | 70 |
| 2025-07-17 17:40:27 | BUY | WFC | 1 | $79.77 | N/A | 70 |
| 2025-07-17 17:26:16 | SELL | NKE | 1 | $72.96 | $1.05 | 65 |
| 2025-07-17 17:26:16 | SELL | CSCO | 2 | $68.18 | $-0.70 | 70 |
| 2025-07-17 17:26:16 | SELL | T | 1 | $26.90 | $-0.20 | 65 |
| 2025-07-17 17:26:16 | BUY | XOM | 2 | $111.64 | N/A | 75 |
| 2025-07-17 17:09:24 | SELL | NVDA | 2 | $173.65 | $3.62 | 70 |
| 2025-07-17 17:09:24 | SELL | XOM | 2 | $111.69 | $3.43 | 65 |
| 2025-07-17 17:09:24 | SELL | T | 5 | $26.86 | $-1.09 | 65 |
| 2025-07-17 17:09:24 | BUY | WFC | 1 | $80.10 | N/A | 70 |
| 2025-07-17 17:09:24 | BUY | CSCO | 4 | $68.19 | N/A | 75 |
| 2025-07-17 16:56:39 | SELL | INTC | 6 | $22.99 | $3.60 | 60 |
| 2025-07-17 16:56:39 | SELL | CSCO | 1 | $68.29 | $-0.29 | 65 |

<!--TRADE_LOG_END--> 
