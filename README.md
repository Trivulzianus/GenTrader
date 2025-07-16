# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 19:36:41**

| Metric | Value |
|---|---|
| **Total Value** | **$100,696.49** |
| Cash | $2,075.26 |
| Holdings Value | $98,621.22 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.34 | $2,103.35 | 70 |
| ADBE | 6 | $375.23 | $362.97 | $2,177.82 | 70 |
| AMD | 15 | $145.40 | $159.28 | $2,389.20 | 70 |
| AMZN | 10 | $221.65 | $223.00 | $2,229.95 | 75 |
| AVGO | 8 | $275.34 | $279.58 | $2,236.65 | 70 |
| AXP | 6 | $308.37 | $311.54 | $1,869.24 | 65 |
| BA | 9 | $210.81 | $229.68 | $2,067.12 | 65 |
| BAC | 49 | $46.24 | $45.97 | $2,252.41 | 70 |
| C | 30 | $86.85 | $90.03 | $2,700.75 | 85 |
| CAT | 6 | $397.74 | $411.75 | $2,470.50 | 85 |
| COST | 2 | $979.83 | $951.28 | $1,902.57 | 65 |
| CRM | 8 | $267.44 | $257.59 | $2,060.72 | 65 |
| CSCO | 31 | $68.46 | $67.31 | $2,086.76 | 65 |
| CVX | 15 | $146.59 | $150.55 | $2,258.22 | 70 |
| DIS | 18 | $122.77 | $119.74 | $2,155.32 | 65 |
| GOOGL | 13 | $179.34 | $182.95 | $2,378.35 | 70 |
| GS | 3 | $717.52 | $706.75 | $2,120.24 | 85 |
| HD | 5 | $353.54 | $357.15 | $1,785.77 | 65 |
| INTC | 85 | $22.35 | $22.64 | $1,924.38 | 60 |
| JNJ | 13 | $155.43 | $164.50 | $2,138.50 | 70 |
| JPM | 8 | $292.65 | $285.46 | $2,283.68 | 70 |
| KO | 30 | $70.97 | $69.19 | $2,075.55 | 65 |
| LLY | 3 | $781.32 | $789.01 | $2,367.03 | 65 |
| MA | 4 | $563.08 | $554.39 | $2,217.56 | 65 |
| META | 3 | $717.12 | $702.44 | $2,107.32 | 70 |
| MRK | 29 | $82.56 | $82.22 | $2,384.24 | 75 |
| MSFT | 5 | $498.84 | $505.66 | $2,528.32 | 75 |
| NFLX | 1 | $1,279.00 | $1,254.55 | $1,254.55 | 65 |
| NKE | 29 | $71.99 | $72.13 | $2,091.77 | 65 |
| NVDA | 14 | $171.52 | $170.94 | $2,393.09 | 70 |
| ORCL | 9 | $232.99 | $240.43 | $2,163.83 | 70 |
| PEP | 15 | $136.57 | $134.90 | $2,023.43 | 65 |
| PFE | 84 | $25.28 | $24.61 | $2,066.82 | 65 |
| PG | 13 | $152.06 | $153.31 | $1,993.03 | 65 |
| PYPL | 29 | $72.15 | $72.89 | $2,113.81 | 65 |
| QCOM | 14 | $153.83 | $154.07 | $2,157.05 | 65 |
| T | 77 | $27.10 | $26.95 | $2,074.80 | 65 |
| TGT | 20 | $104.94 | $101.48 | $2,029.70 | 65 |
| TSLA | 6 | $318.51 | $322.11 | $1,932.66 | 65 |
| UNH | 7 | $298.51 | $292.34 | $2,046.38 | 65 |
| UNP | 9 | $236.79 | $230.90 | $2,078.10 | 65 |
| V | 6 | $355.85 | $350.21 | $2,101.26 | 70 |
| VZ | 50 | $43.08 | $41.24 | $2,061.86 | 65 |
| WFC | 29 | $78.86 | $79.82 | $2,314.85 | 75 |
| WMT | 22 | $97.29 | $94.89 | $2,087.58 | 65 |
| XOM | 21 | $109.98 | $112.62 | $2,365.12 | 75 |

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
| 2025-07-16 19:36:33 | SELL | JPM | 1 | $285.48 | $-6.38 | 70 |
| 2025-07-16 19:36:33 | SELL | INTC | 6 | $22.64 | $1.60 | 60 |
| 2025-07-16 19:36:33 | SELL | CVX | 1 | $150.55 | $3.71 | 70 |
| 2025-07-16 19:36:33 | SELL | T | 5 | $26.94 | $-0.71 | 65 |
| 2025-07-16 19:36:33 | BUY | WFC | 1 | $79.85 | N/A | 75 |
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

<!--TRADE_LOG_END--> 
