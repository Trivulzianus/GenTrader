# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 14:53:56**

| Metric | Value |
|---|---|
| **Total Value** | **$101,427.32** |
| Cash | $1,675.16 |
| Holdings Value | $99,752.16 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.58 | $2,125.80 | 70 |
| ADBE | 5 | $377.60 | $370.60 | $1,853.00 | 65 |
| AMD | 14 | $134.68 | $145.37 | $2,035.11 | 65 |
| AMZN | 11 | $221.90 | $221.29 | $2,434.19 | 75 |
| AVGO | 8 | $275.34 | $273.50 | $2,188.04 | 70 |
| AXP | 7 | $325.28 | $322.65 | $2,258.55 | 75 |
| BA | 9 | $210.97 | $225.90 | $2,033.10 | 65 |
| BAC | 47 | $48.67 | $47.12 | $2,214.41 | 70 |
| C | 30 | $86.79 | $86.54 | $2,596.20 | 85 |
| CAT | 6 | $397.86 | $409.71 | $2,458.26 | 75 |
| COST | 2 | $979.83 | $979.24 | $1,958.48 | 60 |
| CRM | 8 | $268.33 | $266.43 | $2,131.44 | 65 |
| CSCO | 34 | $68.38 | $68.72 | $2,336.48 | 75 |
| CVX | 16 | $146.72 | $154.01 | $2,464.16 | 75 |
| DIS | 18 | $122.80 | $121.58 | $2,188.44 | 70 |
| GOOGL | 12 | $179.86 | $175.59 | $2,107.08 | 65 |
| GS | 3 | $717.52 | $702.45 | $2,107.34 | 70 |
| HD | 6 | $372.64 | $376.04 | $2,256.21 | 70 |
| INTC | 85 | $22.28 | $23.77 | $2,020.03 | 65 |
| JNJ | 13 | $155.89 | $158.54 | $2,061.02 | 65 |
| JPM | 9 | $291.61 | $286.73 | $2,580.53 | 85 |
| KO | 29 | $71.03 | $69.59 | $2,018.25 | 65 |
| LLY | 2 | $776.66 | $795.28 | $1,590.56 | 65 |
| MA | 4 | $563.08 | $563.70 | $2,254.78 | 65 |
| META | 3 | $717.12 | $724.96 | $2,174.88 | 85 |
| MRK | 31 | $82.65 | $84.42 | $2,617.17 | 85 |
| MSFT | 5 | $498.84 | $499.87 | $2,499.35 | 85 |
| NFLX | 1 | $1,279.00 | $1,256.24 | $1,256.24 | 65 |
| NKE | 31 | $75.78 | $74.73 | $2,316.63 | 75 |
| NVDA | 14 | $156.66 | $162.75 | $2,278.48 | 70 |
| ORCL | 9 | $233.31 | $235.63 | $2,120.67 | 70 |
| PEP | 15 | $136.57 | $136.14 | $2,042.10 | 65 |
| PFE | 85 | $25.21 | $25.93 | $2,203.62 | 70 |
| PG | 12 | $160.96 | $158.47 | $1,901.64 | 65 |
| PYPL | 31 | $76.64 | $75.71 | $2,347.01 | 75 |
| QCOM | 16 | $161.59 | $159.68 | $2,554.82 | 85 |
| T | 74 | $28.53 | $27.64 | $2,044.99 | 65 |
| TGT | 20 | $104.89 | $105.47 | $2,109.50 | 70 |
| TSLA | 6 | $288.62 | $305.54 | $1,833.24 | 65 |
| UNH | 6 | $298.34 | $303.13 | $1,818.78 | 65 |
| UNP | 10 | $236.59 | $239.90 | $2,398.95 | 70 |
| V | 6 | $355.85 | $355.56 | $2,133.36 | 70 |
| VZ | 48 | $43.15 | $42.06 | $2,018.88 | 65 |
| WFC | 29 | $82.30 | $82.16 | $2,382.64 | 75 |
| WMT | 21 | $97.35 | $96.16 | $2,019.26 | 65 |
| XOM | 21 | $109.89 | $114.69 | $2,408.49 | 75 |

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
| 2025-07-10 14:53:46 | SELL | NVDA | 2 | $162.74 | $10.64 | 70 |
| 2025-07-10 14:53:46 | SELL | AMD | 1 | $145.38 | $9.99 | 65 |
| 2025-07-10 14:53:46 | SELL | XOM | 2 | $114.68 | $8.75 | 75 |
| 2025-07-10 14:53:46 | SELL | BAC | 3 | $47.12 | $-4.38 | 70 |
| 2025-07-10 14:53:46 | SELL | PFE | 5 | $25.93 | $3.39 | 70 |
| 2025-07-10 14:53:46 | SELL | WFC | 3 | $82.15 | $-0.42 | 75 |
| 2025-07-10 14:53:46 | SELL | CVX | 1 | $154.09 | $6.94 | 75 |
| 2025-07-10 14:53:46 | BUY | INTC | 5 | $23.76 | N/A | 65 |
| 2025-07-10 14:53:46 | BUY | NKE | 2 | $74.79 | N/A | 75 |
| 2025-07-10 14:53:46 | BUY | MRK | 3 | $84.43 | N/A | 85 |
| 2025-07-10 14:53:46 | BUY | C | 4 | $86.53 | N/A | 85 |
| 2025-07-10 14:53:46 | BUY | CSCO | 1 | $68.72 | N/A | 75 |
| 2025-07-10 14:53:46 | BUY | QCOM | 2 | $159.60 | N/A | 85 |
| 2025-07-10 14:41:37 | SELL | INTC | 6 | $23.87 | $9.37 | 60 |
| 2025-07-10 14:41:37 | BUY | NKE | 1 | $74.86 | N/A | 70 |
| 2025-07-10 14:41:37 | BUY | PFE | 11 | $26.00 | N/A | 75 |
| 2025-07-10 14:41:37 | BUY | T | 1 | $27.65 | N/A | 65 |
| 2025-07-10 14:26:27 | SELL | AAPL | 1 | $211.51 | $0.43 | 65 |
| 2025-07-10 14:26:27 | SELL | NKE | 4 | $74.62 | $-4.42 | 65 |
| 2025-07-10 14:26:27 | SELL | PFE | 6 | $25.94 | $4.42 | 65 |
| 2025-07-10 14:26:27 | SELL | C | 1 | $86.44 | $-0.38 | 70 |
| 2025-07-10 14:26:27 | SELL | CSCO | 1 | $68.72 | $0.35 | 70 |
| 2025-07-10 14:26:27 | BUY | NVDA | 2 | $162.88 | N/A | 85 |
| 2025-07-10 14:26:27 | BUY | WFC | 3 | $82.17 | N/A | 85 |
| 2025-07-10 14:26:27 | BUY | QCOM | 1 | $159.40 | N/A | 75 |

<!--TRADE_LOG_END--> 
