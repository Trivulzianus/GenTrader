# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 14:08:32**

| Metric | Value |
|---|---|
| **Total Value** | **$101,219.59** |
| Cash | $1,411.92 |
| Holdings Value | $99,807.67 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.34 | $2,103.38 | 65 |
| ADBE | 6 | $375.23 | $361.58 | $2,169.48 | 65 |
| AMD | 14 | $160.08 | $160.38 | $2,245.25 | 70 |
| AMZN | 10 | $221.65 | $223.52 | $2,235.21 | 70 |
| AVGO | 8 | $275.34 | $284.38 | $2,275.04 | 65 |
| AXP | 7 | $309.18 | $313.65 | $2,195.59 | 75 |
| BA | 9 | $210.81 | $230.34 | $2,073.06 | 65 |
| BAC | 45 | $46.26 | $46.17 | $2,077.88 | 65 |
| C | 30 | $86.85 | $90.82 | $2,724.60 | 85 |
| CAT | 6 | $397.74 | $418.21 | $2,509.25 | 75 |
| COST | 2 | $979.83 | $950.30 | $1,900.60 | 65 |
| CRM | 8 | $267.44 | $258.33 | $2,066.64 | 65 |
| CSCO | 31 | $68.48 | $68.12 | $2,111.88 | 65 |
| CVX | 15 | $146.65 | $149.56 | $2,243.40 | 70 |
| DIS | 19 | $122.70 | $121.62 | $2,310.78 | 75 |
| GOOGL | 13 | $179.34 | $181.74 | $2,362.62 | 75 |
| GS | 3 | $717.52 | $712.48 | $2,137.43 | 80 |
| HD | 6 | $354.18 | $357.43 | $2,144.58 | 65 |
| INTC | 91 | $22.37 | $22.66 | $2,061.87 | 65 |
| JNJ | 13 | $155.43 | $163.06 | $2,119.78 | 70 |
| JPM | 9 | $291.90 | $289.09 | $2,601.81 | 85 |
| KO | 30 | $70.97 | $69.70 | $2,091.15 | 65 |
| LLY | 3 | $781.32 | $785.00 | $2,355.00 | 65 |
| MA | 4 | $563.08 | $551.55 | $2,206.20 | 65 |
| META | 3 | $717.12 | $701.12 | $2,103.36 | 75 |
| MRK | 29 | $82.56 | $82.41 | $2,389.74 | 75 |
| MSFT | 5 | $498.84 | $510.34 | $2,551.70 | 85 |
| NFLX | 1 | $1,279.00 | $1,258.14 | $1,258.14 | 65 |
| NKE | 29 | $71.88 | $73.11 | $2,120.34 | 65 |
| NVDA | 13 | $171.54 | $172.80 | $2,246.34 | 70 |
| ORCL | 9 | $232.99 | $249.99 | $2,249.92 | 75 |
| PEP | 16 | $136.49 | $144.44 | $2,310.96 | 70 |
| PFE | 84 | $25.28 | $24.65 | $2,070.59 | 65 |
| PG | 14 | $152.18 | $154.71 | $2,165.87 | 65 |
| PYPL | 28 | $72.12 | $73.03 | $2,044.70 | 65 |
| QCOM | 14 | $153.83 | $152.74 | $2,138.36 | 65 |
| T | 77 | $27.10 | $26.99 | $2,078.23 | 65 |
| TGT | 21 | $104.77 | $103.27 | $2,168.67 | 65 |
| TSLA | 6 | $318.51 | $323.15 | $1,938.91 | 65 |
| UNH | 7 | $298.51 | $286.73 | $2,007.11 | 65 |
| UNP | 9 | $236.91 | $229.65 | $2,066.81 | 65 |
| V | 6 | $355.85 | $348.74 | $2,092.44 | 65 |
| VZ | 50 | $43.08 | $41.16 | $2,058.25 | 65 |
| WFC | 26 | $78.68 | $80.22 | $2,085.59 | 65 |
| WMT | 22 | $97.29 | $95.40 | $2,098.90 | 65 |
| XOM | 20 | $109.88 | $112.02 | $2,240.30 | 70 |

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
| 2025-07-17 14:08:25 | SELL | XOM | 1 | $112.00 | $2.02 | 70 |
| 2025-07-17 14:08:25 | SELL | WFC | 4 | $80.25 | $5.45 | 65 |
| 2025-07-17 14:08:25 | SELL | CSCO | 1 | $67.37 | $-1.08 | 65 |
| 2025-07-17 14:08:25 | SELL | CVX | 1 | $149.52 | $2.69 | 70 |
| 2025-07-17 14:08:25 | BUY | DIS | 1 | $121.55 | N/A | 75 |
| 2025-07-17 13:49:19 | SELL | NKE | 4 | $72.76 | $3.08 | 65 |
| 2025-07-17 13:49:19 | SELL | UNP | 1 | $230.08 | $-6.14 | 65 |
| 2025-07-17 13:49:19 | BUY | INTC | 7 | $22.67 | N/A | 65 |
| 2025-07-17 13:49:19 | BUY | AXP | 1 | $314.02 | N/A | 70 |
| 2025-07-17 13:49:19 | BUY | CSCO | 1 | $68.18 | N/A | 70 |
| 2025-07-17 13:30:02 | SELL | INTC | 6 | $22.69 | $1.93 | 60 |
| 2025-07-17 13:30:02 | BUY | UNP | 1 | $231.18 | N/A | 75 |
| 2025-07-17 13:04:44 | SELL | BAC | 3 | $46.03 | $-0.64 | 65 |
| 2025-07-17 13:04:44 | SELL | UNP | 1 | $231.18 | $-5.04 | 65 |
| 2025-07-17 13:04:44 | BUY | INTC | 5 | $22.69 | N/A | 65 |
| 2025-07-17 13:04:44 | BUY | NKE | 4 | $72.10 | N/A | 75 |
| 2025-07-17 13:04:44 | BUY | VZ | 3 | $41.25 | N/A | 65 |
| 2025-07-17 13:04:44 | BUY | TGT | 1 | $101.34 | N/A | 70 |
| 2025-07-17 12:32:27 | SELL | VZ | 3 | $41.25 | $-5.49 | 60 |
| 2025-07-17 12:14:03 | SELL | T | 5 | $26.95 | $-0.69 | 65 |
| 2025-07-17 12:14:03 | BUY | BAC | 3 | $46.03 | N/A | 70 |
| 2025-07-17 11:50:40 | SELL | INTC | 1 | $22.69 | $0.34 | 60 |
| 2025-07-17 11:50:40 | SELL | BAC | 1 | $46.03 | $-0.22 | 65 |
| 2025-07-17 11:50:40 | BUY | VZ | 3 | $41.25 | N/A | 65 |
| 2025-07-17 11:50:40 | BUY | T | 5 | $26.95 | N/A | 70 |

<!--TRADE_LOG_END--> 
