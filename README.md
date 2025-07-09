# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 15:52:06**

| Metric | Value |
|---|---|
| **Total Value** | **$100,731.01** |
| Cash | $1,477.54 |
| Holdings Value | $99,253.47 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $207.40 | $2,074.00 | 65 |
| ADBE | 5 | $377.60 | $375.23 | $1,876.15 | 65 |
| AMD | 15 | $135.39 | $138.04 | $2,070.60 | 65 |
| AMZN | 10 | $221.83 | $222.63 | $2,226.35 | 75 |
| AVGO | 8 | $275.34 | $276.07 | $2,208.56 | 70 |
| AXP | 7 | $325.28 | $318.67 | $2,230.69 | 70 |
| BA | 9 | $210.79 | $228.24 | $2,054.16 | 70 |
| BAC | 46 | $48.74 | $46.84 | $2,154.64 | 70 |
| C | 30 | $86.68 | $86.04 | $2,581.20 | 85 |
| CAT | 6 | $397.86 | $400.25 | $2,401.47 | 65 |
| COST | 2 | $979.83 | $976.82 | $1,953.64 | 65 |
| CRM | 8 | $268.33 | $271.01 | $2,168.12 | 65 |
| CSCO | 32 | $68.33 | $68.73 | $2,199.52 | 70 |
| CVX | 16 | $146.66 | $153.10 | $2,449.60 | 75 |
| DIS | 19 | $122.72 | $121.11 | $2,301.09 | 75 |
| GOOGL | 13 | $179.50 | $177.56 | $2,308.28 | 70 |
| GS | 3 | $717.52 | $698.00 | $2,094.00 | 70 |
| HD | 6 | $372.64 | $365.83 | $2,194.98 | 65 |
| INTC | 87 | $22.34 | $23.23 | $2,020.58 | 65 |
| JNJ | 13 | $155.89 | $155.22 | $2,017.92 | 65 |
| JPM | 9 | $291.61 | $283.99 | $2,555.91 | 75 |
| KO | 29 | $71.03 | $69.01 | $2,001.29 | 65 |
| LLY | 2 | $776.66 | $786.32 | $1,572.64 | 70 |
| MA | 4 | $563.08 | $561.73 | $2,246.90 | 65 |
| META | 3 | $717.12 | $735.69 | $2,207.06 | 85 |
| MRK | 29 | $82.50 | $83.50 | $2,421.50 | 75 |
| MSFT | 5 | $498.84 | $500.95 | $2,504.75 | 85 |
| NFLX | 1 | $1,279.00 | $1,279.50 | $1,279.50 | 65 |
| NKE | 29 | $75.98 | $73.72 | $2,137.88 | 70 |
| NVDA | 16 | $157.22 | $163.24 | $2,611.84 | 85 |
| ORCL | 10 | $233.47 | $234.09 | $2,340.90 | 75 |
| PEP | 15 | $136.57 | $133.09 | $1,996.35 | 65 |
| PFE | 86 | $25.22 | $25.41 | $2,185.45 | 70 |
| PG | 13 | $160.75 | $156.81 | $2,038.53 | 65 |
| PYPL | 31 | $76.64 | $74.70 | $2,315.86 | 75 |
| QCOM | 14 | $161.87 | $158.69 | $2,221.66 | 75 |
| T | 72 | $28.56 | $27.99 | $2,015.33 | 65 |
| TGT | 20 | $104.89 | $102.14 | $2,042.80 | 65 |
| TSLA | 6 | $288.62 | $295.00 | $1,770.00 | 65 |
| UNH | 7 | $314.75 | $299.54 | $2,096.78 | 65 |
| UNP | 9 | $236.60 | $237.35 | $2,136.15 | 65 |
| V | 6 | $355.95 | $354.41 | $2,126.46 | 65 |
| VZ | 48 | $43.15 | $42.48 | $2,038.80 | 65 |
| WFC | 29 | $82.27 | $81.77 | $2,371.33 | 75 |
| WMT | 21 | $97.35 | $97.12 | $2,039.52 | 65 |
| XOM | 21 | $110.02 | $113.94 | $2,392.74 | 75 |

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
| 2025-07-09 15:51:57 | SELL | WFC | 1 | $81.78 | $-0.48 | 75 |
| 2025-07-09 15:51:57 | SELL | CSCO | 2 | $68.74 | $0.76 | 70 |
| 2025-07-09 15:51:57 | BUY | BAC | 2 | $46.85 | N/A | 70 |
| 2025-07-09 15:51:57 | BUY | PFE | 5 | $25.42 | N/A | 70 |
| 2025-07-09 15:51:57 | BUY | C | 4 | $86.07 | N/A | 85 |
| 2025-07-09 15:51:57 | BUY | ORCL | 1 | $234.05 | N/A | 75 |
| 2025-07-09 15:40:22 | SELL | BAC | 3 | $46.88 | $-5.46 | 65 |
| 2025-07-09 15:40:22 | SELL | PFE | 5 | $25.40 | $0.87 | 65 |
| 2025-07-09 15:40:22 | SELL | PG | 1 | $156.94 | $-3.54 | 65 |
| 2025-07-09 15:40:22 | SELL | CVX | 1 | $152.64 | $5.63 | 75 |
| 2025-07-09 15:40:22 | BUY | INTC | 1 | $23.25 | N/A | 65 |
| 2025-07-09 15:40:22 | BUY | NKE | 1 | $73.84 | N/A | 70 |
| 2025-07-09 15:40:22 | BUY | WFC | 1 | $81.85 | N/A | 80 |
| 2025-07-09 15:40:22 | BUY | CSCO | 2 | $68.68 | N/A | 75 |
| 2025-07-09 15:26:48 | SELL | NKE | 1 | $73.75 | $-2.22 | 65 |
| 2025-07-09 15:26:48 | SELL | C | 4 | $85.93 | $-2.92 | 70 |
| 2025-07-09 15:26:48 | BUY | INTC | 5 | $23.59 | N/A | 65 |
| 2025-07-09 15:26:48 | BUY | PG | 1 | $156.78 | N/A | 70 |
| 2025-07-09 15:26:48 | BUY | CSCO | 1 | $68.65 | N/A | 70 |
| 2025-07-09 15:26:48 | BUY | CVX | 2 | $152.68 | N/A | 85 |
| 2025-07-09 15:09:06 | SELL | AMZN | 1 | $219.36 | $-2.25 | 70 |
| 2025-07-09 15:09:06 | SELL | XOM | 1 | $113.82 | $3.62 | 75 |
| 2025-07-09 15:09:06 | SELL | BA | 1 | $227.19 | $14.76 | 65 |
| 2025-07-09 15:09:06 | BUY | PFE | 1 | $25.47 | N/A | 70 |
| 2025-07-09 15:09:06 | BUY | C | 4 | $86.19 | N/A | 85 |

<!--TRADE_LOG_END--> 
