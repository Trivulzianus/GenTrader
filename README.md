# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 15:41:06**

| Metric | Value |
|---|---|
| **Total Value** | **$101,491.39** |
| Cash | $1,144.28 |
| Holdings Value | $100,347.11 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.88 | $2,128.80 | 70 |
| ADBE | 5 | $377.60 | $371.64 | $1,858.18 | 65 |
| AMD | 16 | $135.52 | $144.10 | $2,305.66 | 70 |
| AMZN | 11 | $221.90 | $221.30 | $2,434.30 | 75 |
| AVGO | 8 | $275.34 | $274.78 | $2,198.23 | 65 |
| AXP | 7 | $325.28 | $323.74 | $2,266.14 | 75 |
| BA | 9 | $210.97 | $225.50 | $2,029.50 | 65 |
| BAC | 49 | $48.61 | $47.15 | $2,310.35 | 75 |
| C | 30 | $86.81 | $86.83 | $2,605.05 | 85 |
| CAT | 6 | $397.86 | $410.79 | $2,464.74 | 70 |
| COST | 2 | $979.83 | $977.12 | $1,954.25 | 65 |
| CRM | 8 | $268.33 | $267.24 | $2,137.92 | 65 |
| CSCO | 32 | $68.35 | $68.93 | $2,205.61 | 70 |
| CVX | 17 | $147.16 | $153.78 | $2,614.26 | 85 |
| DIS | 18 | $122.80 | $121.51 | $2,187.18 | 70 |
| GOOGL | 13 | $179.61 | $176.19 | $2,290.47 | 70 |
| GS | 3 | $717.52 | $706.93 | $2,120.79 | 75 |
| HD | 6 | $372.64 | $375.70 | $2,254.20 | 65 |
| INTC | 86 | $22.30 | $23.83 | $2,049.38 | 65 |
| JNJ | 13 | $155.89 | $158.10 | $2,055.30 | 65 |
| JPM | 9 | $291.61 | $286.77 | $2,580.97 | 85 |
| KO | 29 | $71.03 | $69.45 | $2,014.05 | 65 |
| LLY | 2 | $776.66 | $793.69 | $1,587.38 | 65 |
| MA | 4 | $563.08 | $565.67 | $2,262.70 | 65 |
| META | 3 | $717.12 | $726.98 | $2,180.95 | 85 |
| MRK | 28 | $82.45 | $84.36 | $2,362.22 | 75 |
| MSFT | 5 | $498.84 | $500.08 | $2,500.40 | 75 |
| NFLX | 1 | $1,279.00 | $1,258.63 | $1,258.63 | 65 |
| NKE | 27 | $75.88 | $75.12 | $2,028.38 | 65 |
| NVDA | 16 | $157.41 | $162.66 | $2,602.64 | 85 |
| ORCL | 9 | $233.31 | $236.55 | $2,128.95 | 70 |
| PEP | 15 | $136.57 | $136.15 | $2,042.25 | 65 |
| PFE | 84 | $25.20 | $25.91 | $2,176.24 | 70 |
| PG | 13 | $160.77 | $158.56 | $2,061.34 | 65 |
| PYPL | 31 | $76.64 | $76.05 | $2,357.42 | 75 |
| QCOM | 16 | $161.60 | $159.79 | $2,556.72 | 85 |
| T | 74 | $28.53 | $27.54 | $2,037.59 | 65 |
| TGT | 20 | $104.91 | $105.36 | $2,107.18 | 65 |
| TSLA | 6 | $288.62 | $304.14 | $1,824.84 | 60 |
| UNH | 6 | $298.34 | $302.45 | $1,814.70 | 65 |
| UNP | 9 | $236.20 | $238.75 | $2,148.75 | 75 |
| V | 6 | $355.85 | $357.00 | $2,141.97 | 65 |
| VZ | 49 | $43.12 | $42.00 | $2,058.00 | 65 |
| WFC | 29 | $82.30 | $82.50 | $2,392.64 | 75 |
| WMT | 21 | $97.36 | $95.76 | $2,010.96 | 65 |
| XOM | 23 | $110.31 | $114.73 | $2,638.91 | 85 |

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
| 2025-07-10 15:40:57 | SELL | MRK | 1 | $84.34 | $1.83 | 75 |
| 2025-07-10 15:40:57 | SELL | NKE | 1 | $75.13 | $-0.73 | 65 |
| 2025-07-10 15:40:57 | SELL | CSCO | 1 | $68.93 | $0.55 | 70 |
| 2025-07-10 15:40:57 | SELL | T | 1 | $27.53 | $-0.98 | 65 |
| 2025-07-10 15:40:57 | SELL | TGT | 1 | $105.33 | $0.41 | 65 |
| 2025-07-10 15:40:57 | BUY | NVDA | 2 | $162.68 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | BAC | 1 | $47.15 | N/A | 75 |
| 2025-07-10 15:40:57 | BUY | XOM | 2 | $114.72 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | PFE | 4 | $25.91 | N/A | 70 |
| 2025-07-10 15:40:57 | BUY | C | 3 | $86.85 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | QCOM | 1 | $159.79 | N/A | 85 |
| 2025-07-10 15:40:57 | BUY | WMT | 1 | $95.80 | N/A | 65 |
| 2025-07-10 15:26:42 | SELL | BAC | 2 | $47.16 | $-2.84 | 70 |
| 2025-07-10 15:26:42 | SELL | WMT | 1 | $95.58 | $-1.78 | 60 |
| 2025-07-10 15:26:42 | SELL | PFE | 10 | $25.96 | $7.04 | 65 |
| 2025-07-10 15:26:42 | SELL | NKE | 2 | $75.12 | $-1.37 | 65 |
| 2025-07-10 15:26:42 | SELL | MRK | 1 | $84.43 | $1.85 | 75 |
| 2025-07-10 15:26:42 | BUY | INTC | 1 | $23.83 | N/A | 65 |
| 2025-07-10 15:26:42 | BUY | AMD | 1 | $138.41 | N/A | 70 |
| 2025-07-10 15:26:42 | BUY | C | 1 | $86.74 | N/A | 75 |
| 2025-07-10 15:26:42 | BUY | PG | 1 | $158.56 | N/A | 65 |
| 2025-07-10 15:26:42 | BUY | T | 1 | $27.51 | N/A | 65 |
| 2025-07-10 15:26:42 | BUY | VZ | 1 | $42.01 | N/A | 65 |
| 2025-07-10 15:26:42 | BUY | TGT | 1 | $105.65 | N/A | 70 |
| 2025-07-10 15:09:22 | SELL | NKE | 1 | $74.96 | $-0.82 | 70 |

<!--TRADE_LOG_END--> 
