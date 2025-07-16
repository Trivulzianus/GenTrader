# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 19:24:56**

| Metric | Value |
|---|---|
| **Total Value** | **$100,710.43** |
| Cash | $1,448.55 |
| Holdings Value | $99,261.87 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.17 | $2,101.70 | 70 |
| ADBE | 6 | $375.23 | $363.44 | $2,180.64 | 65 |
| AMD | 15 | $145.40 | $158.46 | $2,376.83 | 70 |
| AMZN | 10 | $221.65 | $223.03 | $2,230.25 | 75 |
| AVGO | 8 | $275.34 | $279.43 | $2,235.44 | 70 |
| AXP | 6 | $308.37 | $311.82 | $1,870.92 | 65 |
| BA | 9 | $210.81 | $229.64 | $2,066.76 | 70 |
| BAC | 49 | $46.24 | $46.02 | $2,255.22 | 70 |
| C | 30 | $86.85 | $90.07 | $2,702.10 | 85 |
| CAT | 6 | $397.74 | $411.69 | $2,470.14 | 85 |
| COST | 2 | $979.83 | $950.89 | $1,901.78 | 65 |
| CRM | 8 | $267.44 | $257.87 | $2,062.96 | 65 |
| CSCO | 31 | $68.46 | $67.30 | $2,086.30 | 65 |
| CVX | 16 | $146.84 | $150.53 | $2,408.56 | 75 |
| DIS | 18 | $122.77 | $119.94 | $2,158.87 | 65 |
| GOOGL | 13 | $179.34 | $183.21 | $2,381.73 | 70 |
| GS | 3 | $717.52 | $705.99 | $2,117.97 | 85 |
| HD | 5 | $353.54 | $357.12 | $1,785.60 | 65 |
| INTC | 91 | $22.37 | $22.55 | $2,051.60 | 65 |
| JNJ | 13 | $155.43 | $164.65 | $2,140.45 | 70 |
| JPM | 9 | $291.86 | $285.44 | $2,568.91 | 75 |
| KO | 30 | $70.97 | $69.29 | $2,078.70 | 65 |
| LLY | 3 | $781.32 | $787.32 | $2,361.96 | 65 |
| MA | 4 | $563.08 | $554.13 | $2,216.52 | 65 |
| META | 3 | $717.12 | $702.99 | $2,108.97 | 65 |
| MRK | 29 | $82.56 | $82.28 | $2,385.98 | 75 |
| MSFT | 5 | $498.84 | $505.57 | $2,527.85 | 70 |
| NFLX | 1 | $1,279.00 | $1,257.00 | $1,257.00 | 65 |
| NKE | 29 | $71.99 | $72.03 | $2,088.73 | 65 |
| NVDA | 14 | $171.52 | $170.86 | $2,392.04 | 70 |
| ORCL | 9 | $232.99 | $240.32 | $2,162.88 | 70 |
| PEP | 15 | $136.57 | $135.03 | $2,025.38 | 65 |
| PFE | 84 | $25.28 | $24.64 | $2,069.76 | 65 |
| PG | 13 | $152.06 | $153.45 | $1,994.85 | 65 |
| PYPL | 29 | $72.15 | $72.97 | $2,116.13 | 65 |
| QCOM | 14 | $153.83 | $153.93 | $2,155.02 | 65 |
| T | 82 | $27.09 | $26.98 | $2,212.77 | 70 |
| TGT | 20 | $104.94 | $101.58 | $2,031.50 | 65 |
| TSLA | 6 | $318.51 | $322.36 | $1,934.16 | 65 |
| UNH | 7 | $298.51 | $292.36 | $2,046.52 | 65 |
| UNP | 9 | $236.79 | $231.03 | $2,079.27 | 65 |
| V | 6 | $355.85 | $350.57 | $2,103.45 | 70 |
| VZ | 50 | $43.08 | $41.29 | $2,064.37 | 65 |
| WFC | 28 | $78.82 | $80.03 | $2,240.98 | 70 |
| WMT | 22 | $97.29 | $94.88 | $2,087.36 | 65 |
| XOM | 21 | $109.98 | $112.62 | $2,365.02 | 75 |

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
| 2025-07-16 19:24:51 | SELL | AMD | 2 | $155.61 | $18.02 | 70 |
| 2025-07-16 19:24:51 | SELL | PFE | 1 | $24.65 | $-0.63 | 65 |
| 2025-07-16 19:24:51 | SELL | WFC | 1 | $80.04 | $1.17 | 70 |
| 2025-07-16 19:24:51 | BUY | INTC | 6 | $22.55 | N/A | 65 |
| 2025-07-16 19:24:51 | BUY | XOM | 1 | $112.62 | N/A | 75 |
| 2025-07-16 19:24:51 | BUY | T | 5 | $26.99 | N/A | 70 |
| 2025-07-16 19:10:44 | SELL | BAC | 9 | $46.02 | $-1.67 | 70 |
| 2025-07-16 19:10:44 | SELL | PFE | 5 | $24.64 | $-2.99 | 65 |
| 2025-07-16 19:10:44 | SELL | UNP | 1 | $231.12 | $-5.09 | 65 |
| 2025-07-16 19:10:44 | SELL | CVX | 1 | $150.90 | $3.82 | 75 |
| 2025-07-16 19:10:44 | BUY | GOOGL | 1 | $183.61 | N/A | 75 |
| 2025-07-16 19:10:44 | BUY | AMD | 3 | $158.07 | N/A | 85 |
| 2025-07-16 18:59:06 | SELL | AMD | 1 | $157.43 | $12.40 | 65 |
| 2025-07-16 18:59:06 | SELL | INTC | 1 | $22.55 | $0.19 | 60 |
| 2025-07-16 18:59:06 | SELL | XOM | 1 | $112.81 | $2.82 | 70 |
| 2025-07-16 18:59:06 | SELL | NKE | 4 | $72.07 | $0.27 | 65 |
| 2025-07-16 18:59:06 | SELL | T | 5 | $27.00 | $-0.44 | 65 |
| 2025-07-16 18:59:06 | BUY | BAC | 9 | $46.01 | N/A | 85 |
| 2025-07-16 18:59:06 | BUY | PFE | 5 | $24.67 | N/A | 70 |
| 2025-07-16 18:59:06 | BUY | WFC | 2 | $79.89 | N/A | 75 |
| 2025-07-16 18:59:06 | BUY | CVX | 1 | $151.08 | N/A | 85 |
| 2025-07-16 18:46:09 | SELL | GOOGL | 1 | $183.56 | $4.22 | 65 |
| 2025-07-16 18:46:09 | SELL | WFC | 1 | $79.79 | $0.96 | 65 |
| 2025-07-16 18:46:09 | BUY | NKE | 4 | $72.14 | N/A | 75 |
| 2025-07-16 18:46:09 | BUY | MRK | 3 | $82.33 | N/A | 75 |

<!--TRADE_LOG_END--> 
