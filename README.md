# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 14:26:38**

| Metric | Value |
|---|---|
| **Total Value** | **$101,195.76** |
| Cash | $1,804.47 |
| Holdings Value | $99,391.29 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $211.55 | $2,115.49 | 65 |
| ADBE | 5 | $377.60 | $370.12 | $1,850.60 | 65 |
| AMD | 15 | $135.39 | $144.02 | $2,160.30 | 65 |
| AMZN | 11 | $221.90 | $220.08 | $2,420.88 | 75 |
| AVGO | 8 | $275.34 | $272.88 | $2,183.04 | 65 |
| AXP | 7 | $325.28 | $321.73 | $2,252.11 | 75 |
| BA | 9 | $210.97 | $225.40 | $2,028.60 | 65 |
| BAC | 50 | $48.57 | $47.13 | $2,356.50 | 75 |
| C | 26 | $86.83 | $86.39 | $2,246.14 | 70 |
| CAT | 6 | $397.86 | $408.12 | $2,448.72 | 75 |
| COST | 2 | $979.83 | $975.50 | $1,951.00 | 60 |
| CRM | 8 | $268.33 | $265.83 | $2,126.68 | 65 |
| CSCO | 33 | $68.37 | $68.72 | $2,267.76 | 70 |
| CVX | 17 | $147.15 | $154.77 | $2,631.09 | 85 |
| DIS | 18 | $122.80 | $121.27 | $2,182.77 | 70 |
| GOOGL | 12 | $179.86 | $175.04 | $2,100.48 | 70 |
| GS | 3 | $717.52 | $699.18 | $2,097.54 | 70 |
| HD | 6 | $372.64 | $375.30 | $2,251.80 | 70 |
| INTC | 86 | $22.31 | $23.64 | $2,033.47 | 65 |
| JNJ | 13 | $155.89 | $158.23 | $2,057.03 | 65 |
| JPM | 9 | $291.61 | $285.59 | $2,570.31 | 85 |
| KO | 29 | $71.03 | $69.50 | $2,015.36 | 65 |
| LLY | 2 | $776.66 | $790.16 | $1,580.32 | 65 |
| MA | 4 | $563.08 | $562.97 | $2,251.88 | 65 |
| META | 3 | $717.12 | $720.49 | $2,161.47 | 75 |
| MRK | 28 | $82.46 | $84.61 | $2,369.08 | 75 |
| MSFT | 5 | $498.84 | $498.78 | $2,493.90 | 75 |
| NFLX | 1 | $1,279.00 | $1,251.09 | $1,251.09 | 65 |
| NKE | 28 | $75.88 | $74.67 | $2,090.76 | 65 |
| NVDA | 16 | $157.42 | $162.24 | $2,595.76 | 85 |
| ORCL | 9 | $233.31 | $234.94 | $2,114.46 | 65 |
| PEP | 15 | $136.57 | $135.91 | $2,038.65 | 65 |
| PFE | 79 | $25.15 | $25.94 | $2,049.26 | 65 |
| PG | 12 | $160.96 | $158.37 | $1,900.44 | 65 |
| PYPL | 31 | $76.64 | $75.30 | $2,334.30 | 75 |
| QCOM | 14 | $161.87 | $159.40 | $2,231.60 | 75 |
| T | 73 | $28.55 | $27.66 | $2,019.54 | 65 |
| TGT | 20 | $104.89 | $104.98 | $2,099.60 | 65 |
| TSLA | 6 | $288.62 | $303.36 | $1,820.16 | 65 |
| UNH | 6 | $298.34 | $300.46 | $1,802.78 | 65 |
| UNP | 10 | $236.59 | $239.58 | $2,395.80 | 75 |
| V | 6 | $355.85 | $356.14 | $2,136.84 | 65 |
| VZ | 48 | $43.15 | $42.05 | $2,018.64 | 65 |
| WFC | 32 | $82.29 | $82.13 | $2,628.16 | 85 |
| WMT | 21 | $97.35 | $95.90 | $2,013.90 | 65 |
| XOM | 23 | $110.31 | $115.01 | $2,645.23 | 85 |

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
| 2025-07-10 14:26:27 | SELL | AAPL | 1 | $211.51 | $0.43 | 65 |
| 2025-07-10 14:26:27 | SELL | NKE | 4 | $74.62 | $-4.42 | 65 |
| 2025-07-10 14:26:27 | SELL | PFE | 6 | $25.94 | $4.42 | 65 |
| 2025-07-10 14:26:27 | SELL | C | 1 | $86.44 | $-0.38 | 70 |
| 2025-07-10 14:26:27 | SELL | CSCO | 1 | $68.72 | $0.35 | 70 |
| 2025-07-10 14:26:27 | BUY | NVDA | 2 | $162.88 | N/A | 85 |
| 2025-07-10 14:26:27 | BUY | WFC | 3 | $82.17 | N/A | 85 |
| 2025-07-10 14:26:27 | BUY | QCOM | 1 | $159.40 | N/A | 75 |
| 2025-07-10 14:09:15 | SELL | NVDA | 2 | $162.34 | $9.98 | 70 |
| 2025-07-10 14:09:15 | SELL | PFE | 1 | $25.90 | $0.68 | 70 |
| 2025-07-10 14:09:15 | SELL | MRK | 1 | $84.14 | $1.63 | 75 |
| 2025-07-10 14:09:15 | SELL | PG | 1 | $158.32 | $-2.43 | 60 |
| 2025-07-10 14:09:15 | BUY | PYPL | 1 | $75.14 | N/A | 75 |
| 2025-07-10 14:09:15 | BUY | C | 1 | $86.58 | N/A | 75 |
| 2025-07-10 14:09:15 | BUY | CVX | 2 | $153.73 | N/A | 85 |
| 2025-07-10 13:47:19 | SELL | GOOGL | 1 | $175.33 | $-4.18 | 65 |
| 2025-07-10 13:47:19 | SELL | MRK | 2 | $83.42 | $1.68 | 75 |
| 2025-07-10 13:47:19 | SELL | PYPL | 1 | $74.64 | $-1.98 | 70 |
| 2025-07-10 13:47:19 | SELL | PFE | 5 | $25.68 | $2.24 | 70 |
| 2025-07-10 13:47:19 | BUY | NVDA | 2 | $163.90 | N/A | 85 |
| 2025-07-10 13:47:19 | BUY | UNH | 6 | $298.34 | N/A | 65 |
| 2025-07-10 13:47:19 | BUY | XOM | 3 | $113.46 | N/A | 85 |
| 2025-07-10 13:47:19 | BUY | NKE | 1 | $73.76 | N/A | 75 |
| 2025-07-10 13:47:19 | BUY | T | 1 | $27.73 | N/A | 65 |
| 2025-07-10 13:46:52 | SELL | UNH | 7 | $298.55 | $-113.40 | 65 |

<!--TRADE_LOG_END--> 
