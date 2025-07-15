# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-15 19:08:28**

| Metric | Value |
|---|---|
| **Total Value** | **$100,519.40** |
| Cash | $770.87 |
| Holdings Value | $99,748.52 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.53 | $2,105.30 | 65 |
| ADBE | 6 | $375.23 | $365.24 | $2,191.41 | 65 |
| AMD | 17 | $146.29 | $154.51 | $2,626.67 | 85 |
| AMZN | 10 | $221.65 | $226.25 | $2,262.50 | 70 |
| AVGO | 8 | $275.34 | $281.06 | $2,248.48 | 65 |
| AXP | 7 | $325.34 | $311.43 | $2,180.01 | 65 |
| BA | 10 | $212.88 | $231.10 | $2,311.00 | 70 |
| BAC | 48 | $46.29 | $46.23 | $2,219.28 | 70 |
| C | 30 | $86.78 | $91.22 | $2,736.60 | 85 |
| CAT | 6 | $397.74 | $405.12 | $2,430.75 | 70 |
| COST | 2 | $979.83 | $968.31 | $1,936.62 | 65 |
| CRM | 8 | $267.44 | $258.34 | $2,066.72 | 65 |
| CSCO | 31 | $68.46 | $67.32 | $2,086.92 | 65 |
| CVX | 17 | $147.01 | $150.71 | $2,562.07 | 85 |
| DIS | 18 | $122.77 | $119.36 | $2,148.48 | 65 |
| GOOGL | 14 | $179.71 | $183.41 | $2,567.74 | 85 |
| GS | 3 | $717.52 | $702.73 | $2,108.19 | 70 |
| HD | 6 | $372.64 | $359.43 | $2,156.58 | 65 |
| INTC | 89 | $22.39 | $23.09 | $2,055.45 | 65 |
| JNJ | 13 | $155.95 | $155.35 | $2,019.55 | 65 |
| JPM | 9 | $291.63 | $286.23 | $2,576.07 | 85 |
| KO | 30 | $70.97 | $69.44 | $2,083.20 | 65 |
| LLY | 3 | $781.32 | $769.64 | $2,308.92 | 65 |
| MA | 4 | $563.08 | $552.47 | $2,209.86 | 65 |
| META | 3 | $717.12 | $714.19 | $2,142.57 | 70 |
| MRK | 26 | $82.50 | $81.49 | $2,118.74 | 65 |
| MSFT | 5 | $498.84 | $506.93 | $2,534.67 | 85 |
| NFLX | 1 | $1,279.00 | $1,258.85 | $1,258.85 | 65 |
| NKE | 30 | $72.03 | $71.85 | $2,155.50 | 70 |
| NVDA | 13 | $171.77 | $170.35 | $2,214.55 | 70 |
| ORCL | 9 | $233.15 | $234.40 | $2,109.60 | 65 |
| PEP | 15 | $136.57 | $134.25 | $2,013.75 | 60 |
| PFE | 88 | $25.25 | $24.55 | $2,160.84 | 70 |
| PG | 13 | $152.11 | $152.85 | $1,987.05 | 65 |
| PYPL | 28 | $72.12 | $73.58 | $2,060.10 | 65 |
| QCOM | 14 | $153.83 | $154.71 | $2,165.94 | 65 |
| T | 76 | $27.09 | $27.04 | $2,054.66 | 65 |
| TGT | 20 | $104.94 | $102.57 | $2,051.40 | 65 |
| TSLA | 6 | $318.51 | $312.33 | $1,873.98 | 65 |
| UNH | 7 | $298.51 | $291.74 | $2,042.18 | 65 |
| UNP | 9 | $236.66 | $231.50 | $2,083.50 | 65 |
| V | 6 | $355.85 | $348.19 | $2,089.17 | 65 |
| VZ | 47 | $43.19 | $41.32 | $1,941.91 | 60 |
| WFC | 27 | $78.89 | $78.34 | $2,115.32 | 65 |
| WMT | 21 | $97.38 | $95.54 | $2,006.34 | 65 |
| XOM | 21 | $110.02 | $112.83 | $2,369.53 | 75 |

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
| 2025-07-15 19:08:22 | SELL | AMZN | 1 | $226.20 | $4.14 | 70 |
| 2025-07-15 19:08:22 | SELL | MRK | 1 | $81.50 | $-0.97 | 65 |
| 2025-07-15 19:08:22 | SELL | BA | 1 | $231.14 | $16.60 | 70 |
| 2025-07-15 19:08:22 | SELL | WFC | 1 | $78.33 | $-0.54 | 65 |
| 2025-07-15 19:08:22 | SELL | UNP | 1 | $231.50 | $-4.64 | 65 |
| 2025-07-15 19:08:22 | SELL | VZ | 3 | $41.31 | $-5.29 | 60 |
| 2025-07-15 19:08:22 | BUY | BAC | 3 | $46.24 | N/A | 70 |
| 2025-07-15 19:08:22 | BUY | PFE | 4 | $25.35 | N/A | 70 |
| 2025-07-15 19:08:22 | BUY | CVX | 1 | $150.71 | N/A | 85 |
| 2025-07-15 18:47:03 | SELL | BAC | 2 | $46.28 | $-0.03 | 65 |
| 2025-07-15 18:47:03 | SELL | XOM | 2 | $113.09 | $5.61 | 75 |
| 2025-07-15 18:47:03 | SELL | PFE | 3 | $24.61 | $-1.85 | 65 |
| 2025-07-15 18:47:03 | SELL | PG | 1 | $152.73 | $0.58 | 60 |
| 2025-07-15 18:47:03 | SELL | ORCL | 1 | $234.16 | $0.91 | 65 |
| 2025-07-15 18:47:03 | SELL | T | 1 | $27.03 | $-0.06 | 65 |
| 2025-07-15 18:47:03 | BUY | NKE | 1 | $71.88 | N/A | 70 |
| 2025-07-15 18:47:03 | BUY | MRK | 2 | $81.54 | N/A | 70 |
| 2025-07-15 18:47:03 | BUY | WFC | 1 | $78.35 | N/A | 70 |
| 2025-07-15 18:47:03 | BUY | BA | 1 | $231.79 | N/A | 85 |
| 2025-07-15 18:47:03 | BUY | UNP | 1 | $232.04 | N/A | 75 |
| 2025-07-15 18:28:07 | SELL | NKE | 2 | $71.78 | $-0.49 | 65 |
| 2025-07-15 18:28:07 | SELL | CVX | 1 | $151.40 | $4.35 | 75 |
| 2025-07-15 18:28:07 | BUY | BAC | 3 | $47.07 | N/A | 70 |
| 2025-07-15 18:28:07 | BUY | XOM | 2 | $113.38 | N/A | 85 |
| 2025-07-15 18:28:07 | BUY | PFE | 4 | $25.35 | N/A | 70 |

<!--TRADE_LOG_END--> 
