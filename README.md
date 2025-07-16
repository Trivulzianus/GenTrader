# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 16:10:30**

| Metric | Value |
|---|---|
| **Total Value** | **$100,369.22** |
| Cash | $1,905.18 |
| Holdings Value | $98,464.04 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $209.75 | $2,097.50 | 70 |
| ADBE | 6 | $375.23 | $361.39 | $2,168.37 | 65 |
| AMD | 15 | $145.06 | $154.87 | $2,323.05 | 75 |
| AMZN | 10 | $221.65 | $223.53 | $2,235.30 | 75 |
| AVGO | 8 | $275.34 | $277.90 | $2,223.20 | 70 |
| AXP | 6 | $308.37 | $309.10 | $1,854.57 | 65 |
| BA | 9 | $210.81 | $229.17 | $2,062.53 | 70 |
| BAC | 52 | $46.17 | $45.48 | $2,364.97 | 75 |
| C | 29 | $86.76 | $89.13 | $2,584.77 | 85 |
| CAT | 6 | $397.74 | $408.39 | $2,450.37 | 85 |
| COST | 2 | $979.83 | $955.13 | $1,910.26 | 65 |
| CRM | 8 | $267.44 | $256.09 | $2,048.72 | 65 |
| CSCO | 31 | $68.46 | $67.28 | $2,085.84 | 65 |
| CVX | 16 | $146.82 | $150.62 | $2,410.00 | 75 |
| DIS | 18 | $122.77 | $119.61 | $2,152.98 | 65 |
| GOOGL | 12 | $179.03 | $183.54 | $2,202.48 | 65 |
| GS | 3 | $717.52 | $701.11 | $2,103.33 | 85 |
| HD | 5 | $353.54 | $356.44 | $1,782.20 | 65 |
| INTC | 85 | $22.36 | $22.45 | $1,908.67 | 60 |
| JNJ | 13 | $155.43 | $165.87 | $2,156.31 | 65 |
| JPM | 8 | $292.60 | $285.83 | $2,286.64 | 70 |
| KO | 30 | $70.97 | $69.15 | $2,074.64 | 65 |
| LLY | 3 | $781.32 | $791.25 | $2,373.75 | 70 |
| MA | 4 | $563.08 | $552.39 | $2,209.58 | 65 |
| META | 3 | $717.12 | $703.16 | $2,109.48 | 75 |
| MRK | 29 | $82.47 | $81.94 | $2,376.26 | 75 |
| MSFT | 5 | $498.84 | $503.88 | $2,519.40 | 75 |
| NFLX | 1 | $1,279.00 | $1,263.66 | $1,263.66 | 65 |
| NKE | 29 | $72.01 | $71.77 | $2,081.33 | 65 |
| NVDA | 15 | $171.45 | $170.28 | $2,554.12 | 85 |
| ORCL | 9 | $232.99 | $236.24 | $2,126.16 | 65 |
| PEP | 15 | $136.57 | $134.50 | $2,017.50 | 65 |
| PFE | 84 | $25.28 | $24.75 | $2,078.64 | 65 |
| PG | 14 | $152.15 | $152.89 | $2,140.46 | 65 |
| PYPL | 29 | $72.15 | $72.17 | $2,092.79 | 65 |
| QCOM | 14 | $153.83 | $153.03 | $2,142.42 | 65 |
| T | 77 | $27.09 | $27.04 | $2,081.70 | 65 |
| TGT | 20 | $104.94 | $100.84 | $2,016.73 | 65 |
| TSLA | 6 | $318.51 | $319.53 | $1,917.18 | 65 |
| UNH | 7 | $298.51 | $293.05 | $2,051.35 | 65 |
| UNP | 9 | $236.78 | $230.72 | $2,076.48 | 65 |
| V | 6 | $355.85 | $348.83 | $2,092.98 | 65 |
| VZ | 50 | $43.08 | $41.32 | $2,066.00 | 65 |
| WFC | 27 | $78.80 | $78.99 | $2,132.73 | 65 |
| WMT | 22 | $97.29 | $94.94 | $2,088.68 | 65 |
| XOM | 21 | $109.99 | $112.76 | $2,367.96 | 75 |

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
| 2025-07-16 15:52:09 | BUY | WFC | 2 | $78.71 | N/A | 70 |
| 2025-07-16 15:40:59 | SELL | JPM | 1 | $283.89 | $-7.74 | 70 |
| 2025-07-16 15:40:59 | SELL | C | 1 | $88.51 | $2.24 | 65 |
| 2025-07-16 15:40:59 | BUY | NVDA | 2 | $169.67 | N/A | 85 |
| 2025-07-16 15:40:59 | BUY | BAC | 1 | $45.12 | N/A | 65 |
| 2025-07-16 15:40:59 | BUY | INTC | 1 | $22.30 | N/A | 60 |
| 2025-07-16 15:40:59 | BUY | HD | 5 | $353.54 | N/A | 65 |
| 2025-07-16 15:40:59 | BUY | PFE | 1 | $24.73 | N/A | 65 |
| 2025-07-16 15:40:59 | BUY | ORCL | 1 | $234.42 | N/A | 75 |
| 2025-07-16 15:40:59 | BUY | CVX | 2 | $150.69 | N/A | 85 |
| 2025-07-16 15:40:36 | SELL | HD | 6 | $353.78 | $-113.15 | 65 |
| 2025-07-16 15:26:58 | SELL | NVDA | 1 | $170.30 | $-1.19 | 70 |

<!--TRADE_LOG_END--> 
