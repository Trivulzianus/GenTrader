# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-16 18:46:15**

| Metric | Value |
|---|---|
| **Total Value** | **$100,671.41** |
| Cash | $1,286.11 |
| Holdings Value | $99,385.30 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.28 | $2,102.80 | 65 |
| ADBE | 6 | $375.23 | $361.69 | $2,170.14 | 65 |
| AMD | 15 | $145.03 | $157.40 | $2,360.95 | 70 |
| AMZN | 10 | $221.65 | $223.24 | $2,232.40 | 75 |
| AVGO | 8 | $275.34 | $279.28 | $2,234.24 | 70 |
| AXP | 6 | $308.37 | $311.75 | $1,870.53 | 65 |
| BA | 9 | $210.81 | $229.50 | $2,065.55 | 65 |
| BAC | 49 | $46.24 | $45.87 | $2,247.63 | 70 |
| C | 30 | $86.85 | $89.91 | $2,697.15 | 85 |
| CAT | 6 | $397.74 | $411.57 | $2,469.42 | 85 |
| COST | 2 | $979.83 | $952.38 | $1,904.76 | 65 |
| CRM | 8 | $267.44 | $257.23 | $2,057.84 | 65 |
| CSCO | 31 | $68.46 | $67.33 | $2,087.08 | 65 |
| CVX | 16 | $146.83 | $150.97 | $2,415.44 | 75 |
| DIS | 18 | $122.77 | $119.93 | $2,158.74 | 65 |
| GOOGL | 12 | $178.99 | $183.58 | $2,202.96 | 65 |
| GS | 3 | $717.52 | $706.22 | $2,118.66 | 75 |
| HD | 5 | $353.54 | $357.33 | $1,786.67 | 65 |
| INTC | 86 | $22.36 | $22.52 | $1,936.85 | 60 |
| JNJ | 13 | $155.43 | $164.24 | $2,135.12 | 65 |
| JPM | 9 | $291.86 | $284.52 | $2,560.68 | 75 |
| KO | 30 | $70.97 | $69.38 | $2,081.25 | 65 |
| LLY | 3 | $781.32 | $789.66 | $2,368.99 | 70 |
| MA | 4 | $563.08 | $553.71 | $2,214.82 | 65 |
| META | 3 | $717.12 | $702.76 | $2,108.28 | 65 |
| MRK | 29 | $82.56 | $82.34 | $2,388.01 | 75 |
| MSFT | 5 | $498.84 | $505.83 | $2,529.15 | 75 |
| NFLX | 1 | $1,279.00 | $1,257.84 | $1,257.84 | 65 |
| NKE | 33 | $72.00 | $72.14 | $2,380.62 | 75 |
| NVDA | 14 | $171.52 | $171.05 | $2,394.65 | 70 |
| ORCL | 9 | $232.99 | $239.75 | $2,157.80 | 70 |
| PEP | 15 | $136.57 | $135.04 | $2,025.60 | 65 |
| PFE | 85 | $25.27 | $24.67 | $2,096.54 | 65 |
| PG | 13 | $152.06 | $153.21 | $1,991.69 | 65 |
| PYPL | 29 | $72.15 | $72.86 | $2,112.94 | 65 |
| QCOM | 14 | $153.83 | $153.62 | $2,150.71 | 65 |
| T | 82 | $27.09 | $26.98 | $2,211.95 | 70 |
| TGT | 20 | $104.94 | $101.59 | $2,031.90 | 65 |
| TSLA | 6 | $318.51 | $320.83 | $1,924.98 | 65 |
| UNH | 7 | $298.51 | $293.55 | $2,054.85 | 60 |
| UNP | 10 | $236.22 | $231.29 | $2,312.90 | 75 |
| V | 6 | $355.85 | $349.89 | $2,099.37 | 70 |
| VZ | 50 | $43.08 | $41.30 | $2,065.00 | 65 |
| WFC | 27 | $78.79 | $79.80 | $2,154.47 | 65 |
| WMT | 22 | $97.29 | $94.89 | $2,087.65 | 65 |
| XOM | 21 | $109.99 | $112.75 | $2,367.75 | 75 |

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
| 2025-07-16 18:46:09 | SELL | GOOGL | 1 | $183.56 | $4.22 | 65 |
| 2025-07-16 18:46:09 | SELL | WFC | 1 | $79.79 | $0.96 | 65 |
| 2025-07-16 18:46:09 | BUY | NKE | 4 | $72.14 | N/A | 75 |
| 2025-07-16 18:46:09 | BUY | MRK | 3 | $82.33 | N/A | 75 |
| 2025-07-16 18:46:09 | BUY | T | 5 | $26.97 | N/A | 70 |
| 2025-07-16 18:27:21 | SELL | NVDA | 1 | $170.99 | $-0.49 | 70 |
| 2025-07-16 18:27:21 | SELL | MRK | 3 | $81.52 | $-2.86 | 65 |
| 2025-07-16 18:27:21 | BUY | BAC | 3 | $45.85 | N/A | 70 |
| 2025-07-16 18:27:21 | BUY | INTC | 1 | $22.50 | N/A | 60 |
| 2025-07-16 18:27:21 | BUY | XOM | 1 | $112.69 | N/A | 75 |
| 2025-07-16 18:27:21 | BUY | PFE | 1 | $24.62 | N/A | 65 |
| 2025-07-16 18:11:26 | SELL | AMD | 2 | $156.45 | $20.15 | 70 |
| 2025-07-16 18:11:26 | SELL | NKE | 4 | $72.14 | $0.57 | 65 |
| 2025-07-16 18:11:26 | BUY | NVDA | 1 | $170.68 | N/A | 85 |
| 2025-07-16 18:11:26 | BUY | WFC | 1 | $79.57 | N/A | 70 |
| 2025-07-16 17:52:21 | SELL | INTC | 1 | $22.52 | $0.17 | 60 |
| 2025-07-16 17:52:21 | SELL | XOM | 1 | $112.98 | $2.97 | 70 |
| 2025-07-16 17:52:21 | SELL | PFE | 1 | $24.70 | $-0.57 | 65 |
| 2025-07-16 17:52:21 | BUY | AMD | 3 | $155.94 | N/A | 85 |
| 2025-07-16 17:52:21 | BUY | NKE | 4 | $71.99 | N/A | 75 |
| 2025-07-16 17:41:01 | SELL | T | 1 | $27.04 | $-0.05 | 65 |
| 2025-07-16 17:26:01 | SELL | NVDA | 1 | $171.06 | $-0.45 | 70 |
| 2025-07-16 17:26:01 | SELL | ORCL | 1 | $237.70 | $4.24 | 65 |
| 2025-07-16 17:26:01 | SELL | T | 4 | $27.06 | $-0.15 | 65 |
| 2025-07-16 17:26:01 | BUY | INTC | 1 | $22.62 | N/A | 60 |

<!--TRADE_LOG_END--> 
