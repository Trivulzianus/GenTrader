# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 18:11:36**

| Metric | Value |
|---|---|
| **Total Value** | **$100,692.70** |
| Cash | $334.11 |
| Holdings Value | $100,358.58 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.47 | $2,114.70 | 70 |
| ADBE | 6 | $375.23 | $365.56 | $2,193.36 | 65 |
| AMD | 17 | $146.29 | $155.63 | $2,645.80 | 85 |
| AMZN | 11 | $222.06 | $226.88 | $2,495.68 | 75 |
| AVGO | 8 | $275.34 | $282.07 | $2,256.56 | 65 |
| AXP | 7 | $325.34 | $311.98 | $2,183.83 | 65 |
| BA | 10 | $212.82 | $232.16 | $2,321.63 | 75 |
| BAC | 44 | $46.24 | $46.22 | $2,033.46 | 65 |
| C | 30 | $86.78 | $90.59 | $2,717.70 | 85 |
| CAT | 6 | $397.74 | $404.88 | $2,429.28 | 75 |
| COST | 2 | $979.83 | $969.86 | $1,939.71 | 65 |
| CRM | 8 | $267.44 | $258.46 | $2,067.68 | 65 |
| CSCO | 31 | $68.46 | $67.49 | $2,092.19 | 65 |
| CVX | 17 | $147.05 | $151.10 | $2,568.70 | 85 |
| DIS | 18 | $122.77 | $119.42 | $2,149.56 | 65 |
| GOOGL | 14 | $179.71 | $183.70 | $2,571.80 | 85 |
| GS | 3 | $717.52 | $702.88 | $2,108.64 | 70 |
| HD | 6 | $372.64 | $360.78 | $2,164.69 | 65 |
| INTC | 89 | $22.39 | $23.31 | $2,074.59 | 65 |
| JNJ | 13 | $155.95 | $155.43 | $2,020.59 | 65 |
| JPM | 9 | $291.63 | $286.01 | $2,574.09 | 85 |
| KO | 30 | $70.97 | $69.36 | $2,080.65 | 65 |
| LLY | 3 | $781.32 | $776.00 | $2,328.00 | 65 |
| MA | 4 | $563.08 | $553.48 | $2,213.92 | 65 |
| META | 3 | $717.12 | $718.03 | $2,154.09 | 80 |
| MRK | 25 | $82.54 | $81.61 | $2,040.25 | 65 |
| MSFT | 5 | $498.84 | $508.04 | $2,540.20 | 75 |
| NFLX | 1 | $1,279.00 | $1,258.20 | $1,258.20 | 65 |
| NKE | 31 | $72.02 | $71.81 | $2,226.11 | 70 |
| NVDA | 13 | $171.77 | $170.84 | $2,220.92 | 70 |
| ORCL | 10 | $233.25 | $233.57 | $2,335.70 | 75 |
| PEP | 15 | $136.57 | $134.16 | $2,012.40 | 65 |
| PFE | 83 | $25.22 | $24.68 | $2,048.03 | 65 |
| PG | 14 | $152.15 | $152.72 | $2,138.15 | 65 |
| PYPL | 28 | $72.12 | $73.82 | $2,067.00 | 65 |
| QCOM | 14 | $153.83 | $155.15 | $2,172.10 | 65 |
| T | 77 | $27.09 | $27.03 | $2,081.69 | 65 |
| TGT | 20 | $104.94 | $102.63 | $2,052.60 | 65 |
| TSLA | 6 | $318.51 | $313.80 | $1,882.78 | 65 |
| UNH | 7 | $298.51 | $292.96 | $2,050.72 | 65 |
| UNP | 9 | $236.60 | $232.19 | $2,089.66 | 65 |
| V | 6 | $355.85 | $348.28 | $2,089.68 | 65 |
| VZ | 50 | $43.08 | $41.28 | $2,064.25 | 65 |
| WFC | 27 | $78.89 | $77.86 | $2,102.35 | 65 |
| WMT | 21 | $97.38 | $95.63 | $2,008.23 | 65 |
| XOM | 21 | $109.99 | $113.18 | $2,376.68 | 75 |

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
| 2025-07-15 18:11:30 | BUY | CVX | 1 | $151.10 | N/A | 85 |
| 2025-07-15 17:51:39 | SELL | WFC | 1 | $78.10 | $-0.77 | 65 |
| 2025-07-15 17:51:39 | SELL | UNP | 1 | $231.92 | $-4.21 | 65 |
| 2025-07-15 17:51:39 | SELL | CVX | 1 | $150.41 | $3.40 | 75 |
| 2025-07-15 17:51:39 | BUY | BAC | 44 | $46.24 | N/A | 65 |
| 2025-07-15 17:51:39 | BUY | NKE | 1 | $71.61 | N/A | 70 |
| 2025-07-15 17:51:17 | SELL | BAC | 45 | $46.24 | $-115.05 | 65 |
| 2025-07-15 17:40:07 | SELL | NVDA | 2 | $170.66 | $-1.93 | 70 |
| 2025-07-15 17:40:07 | SELL | PYPL | 1 | $73.84 | $1.66 | 65 |
| 2025-07-15 17:40:07 | BUY | AMZN | 1 | $226.36 | N/A | 85 |
| 2025-07-15 17:40:07 | BUY | NKE | 1 | $71.86 | N/A | 70 |
| 2025-07-15 17:40:07 | BUY | WFC | 1 | $78.48 | N/A | 70 |
| 2025-07-15 17:40:07 | BUY | UNP | 1 | $232.34 | N/A | 75 |
| 2025-07-15 17:40:07 | BUY | ORCL | 1 | $233.15 | N/A | 75 |
| 2025-07-15 17:40:07 | BUY | CVX | 1 | $150.49 | N/A | 85 |
| 2025-07-15 17:25:36 | SELL | BAC | 3 | $46.31 | $-6.97 | 65 |
| 2025-07-15 17:25:36 | SELL | UNP | 1 | $232.23 | $-3.89 | 65 |
| 2025-07-15 17:25:36 | SELL | CVX | 2 | $150.52 | $6.62 | 75 |
| 2025-07-15 17:25:36 | BUY | NVDA | 2 | $170.62 | N/A | 85 |
| 2025-07-15 17:25:36 | BUY | INTC | 6 | $23.20 | N/A | 65 |
| 2025-07-15 17:09:19 | SELL | INTC | 6 | $23.23 | $4.98 | 60 |
| 2025-07-15 17:09:19 | BUY | PG | 1 | $152.54 | N/A | 70 |
| 2025-07-15 17:09:19 | BUY | UNP | 1 | $232.19 | N/A | 75 |
| 2025-07-15 17:09:19 | BUY | CVX | 2 | $150.43 | N/A | 85 |
| 2025-07-15 16:57:02 | SELL | NKE | 1 | $71.99 | $-0.05 | 65 |

<!--TRADE_LOG_END--> 
