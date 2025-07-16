# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 16:57:36**

| Metric | Value |
|---|---|
| **Total Value** | **$100,477.55** |
| Cash | $2,283.70 |
| Holdings Value | $98,193.85 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.29 | $2,102.91 | 65 |
| ADBE | 6 | $375.23 | $361.10 | $2,166.62 | 65 |
| AMD | 14 | $144.32 | $155.33 | $2,174.62 | 65 |
| AMZN | 10 | $221.65 | $223.60 | $2,236.00 | 75 |
| AVGO | 8 | $275.34 | $278.64 | $2,229.16 | 70 |
| AXP | 6 | $308.37 | $309.60 | $1,857.57 | 65 |
| BA | 9 | $210.81 | $229.04 | $2,061.40 | 65 |
| BAC | 46 | $46.27 | $45.59 | $2,096.91 | 65 |
| C | 30 | $86.85 | $89.29 | $2,678.70 | 85 |
| CAT | 6 | $397.74 | $409.73 | $2,458.38 | 85 |
| COST | 2 | $979.83 | $954.78 | $1,909.56 | 65 |
| CRM | 8 | $267.44 | $256.22 | $2,049.76 | 65 |
| CSCO | 31 | $68.46 | $67.47 | $2,091.57 | 65 |
| CVX | 15 | $146.55 | $150.92 | $2,263.80 | 70 |
| DIS | 18 | $122.77 | $119.51 | $2,151.24 | 65 |
| GOOGL | 13 | $179.34 | $183.95 | $2,391.35 | 75 |
| GS | 3 | $717.52 | $703.02 | $2,109.06 | 75 |
| HD | 5 | $353.54 | $356.35 | $1,781.75 | 65 |
| INTC | 85 | $22.36 | $22.57 | $1,918.03 | 60 |
| JNJ | 13 | $155.43 | $165.06 | $2,145.72 | 65 |
| JPM | 9 | $291.86 | $286.11 | $2,574.99 | 75 |
| KO | 30 | $70.97 | $69.10 | $2,073.14 | 65 |
| LLY | 3 | $781.32 | $792.45 | $2,377.35 | 70 |
| MA | 4 | $563.08 | $552.00 | $2,208.00 | 65 |
| META | 3 | $717.12 | $704.00 | $2,112.00 | 75 |
| MRK | 29 | $82.47 | $82.02 | $2,378.43 | 75 |
| MSFT | 5 | $498.84 | $504.78 | $2,523.90 | 70 |
| NFLX | 1 | $1,279.00 | $1,260.79 | $1,260.79 | 65 |
| NKE | 30 | $72.00 | $71.65 | $2,149.50 | 65 |
| NVDA | 13 | $171.54 | $171.13 | $2,224.75 | 65 |
| ORCL | 9 | $232.99 | $237.20 | $2,134.80 | 65 |
| PEP | 15 | $136.57 | $134.54 | $2,018.10 | 65 |
| PFE | 85 | $25.27 | $24.69 | $2,098.51 | 65 |
| PG | 14 | $152.15 | $152.79 | $2,139.06 | 65 |
| PYPL | 29 | $72.15 | $72.49 | $2,102.21 | 65 |
| QCOM | 14 | $153.83 | $153.55 | $2,149.70 | 65 |
| T | 77 | $27.09 | $27.02 | $2,080.92 | 65 |
| TGT | 20 | $104.94 | $100.89 | $2,017.70 | 65 |
| TSLA | 6 | $318.51 | $320.08 | $1,920.49 | 65 |
| UNH | 7 | $298.51 | $293.26 | $2,052.82 | 65 |
| UNP | 9 | $236.78 | $231.03 | $2,079.32 | 65 |
| V | 6 | $355.85 | $348.81 | $2,092.88 | 65 |
| VZ | 50 | $43.08 | $41.31 | $2,065.41 | 65 |
| WFC | 27 | $78.80 | $79.33 | $2,141.91 | 65 |
| WMT | 22 | $97.29 | $94.78 | $2,085.27 | 65 |
| XOM | 20 | $109.85 | $112.89 | $2,257.80 | 70 |

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
| 2025-07-16 16:57:30 | SELL | NVDA | 1 | $171.12 | $-0.39 | 65 |
| 2025-07-16 16:57:30 | SELL | AMD | 1 | $155.31 | $10.25 | 65 |
| 2025-07-16 16:57:30 | SELL | NKE | 1 | $71.62 | $-0.37 | 65 |
| 2025-07-16 16:57:30 | SELL | CVX | 1 | $150.95 | $4.13 | 70 |
| 2025-07-16 16:57:30 | BUY | PFE | 1 | $24.68 | N/A | 65 |
| 2025-07-16 16:44:38 | SELL | NVDA | 1 | $170.57 | $-0.88 | 70 |
| 2025-07-16 16:44:38 | BUY | JPM | 1 | $285.90 | N/A | 85 |
| 2025-07-16 16:27:27 | SELL | BAC | 6 | $45.40 | $-4.57 | 65 |
| 2025-07-16 16:27:27 | SELL | XOM | 1 | $112.82 | $2.82 | 70 |
| 2025-07-16 16:27:27 | BUY | GOOGL | 1 | $183.03 | N/A | 75 |
| 2025-07-16 16:27:27 | BUY | NKE | 2 | $71.71 | N/A | 70 |
| 2025-07-16 16:27:27 | BUY | C | 1 | $89.26 | N/A | 85 |
| 2025-07-16 16:10:20 | SELL | GOOGL | 1 | $183.52 | $4.15 | 65 |
| 2025-07-16 16:10:20 | SELL | INTC | 1 | $22.47 | $0.11 | 60 |
| 2025-07-16 16:10:20 | SELL | NKE | 2 | $71.78 | $-0.42 | 65 |
| 2025-07-16 16:10:20 | SELL | WFC | 1 | $78.95 | $0.15 | 65 |
| 2025-07-16 16:10:20 | BUY | NVDA | 2 | $170.34 | N/A | 85 |
| 2025-07-16 16:10:20 | BUY | AMD | 1 | $154.88 | N/A | 75 |
| 2025-07-16 16:10:20 | BUY | BAC | 6 | $45.49 | N/A | 75 |
| 2025-07-16 16:10:20 | BUY | C | 2 | $90.72 | N/A | 85 |
| 2025-07-16 15:52:09 | SELL | NVDA | 3 | $170.08 | $-3.74 | 65 |
| 2025-07-16 15:52:09 | SELL | ORCL | 1 | $235.34 | $2.11 | 65 |
| 2025-07-16 15:52:09 | SELL | CVX | 2 | $150.21 | $6.01 | 75 |
| 2025-07-16 15:52:09 | BUY | NKE | 2 | $71.46 | N/A | 70 |
| 2025-07-16 15:52:09 | BUY | C | 3 | $88.84 | N/A | 75 |

<!--TRADE_LOG_END--> 
