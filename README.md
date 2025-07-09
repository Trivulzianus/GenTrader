# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 16:08:25**

| Metric | Value |
|---|---|
| **Total Value** | **$100,778.41** |
| Cash | $1,712.14 |
| Holdings Value | $99,066.27 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $208.13 | $2,081.30 | 65 |
| ADBE | 5 | $377.60 | $374.82 | $1,874.10 | 65 |
| AMD | 15 | $135.39 | $137.75 | $2,066.25 | 70 |
| AMZN | 10 | $221.83 | $222.48 | $2,224.80 | 75 |
| AVGO | 8 | $275.34 | $276.30 | $2,210.40 | 70 |
| AXP | 7 | $325.28 | $318.84 | $2,231.88 | 70 |
| BA | 9 | $210.79 | $227.69 | $2,049.16 | 70 |
| BAC | 50 | $48.59 | $46.85 | $2,342.50 | 75 |
| C | 30 | $86.68 | $86.04 | $2,581.20 | 85 |
| CAT | 6 | $397.86 | $400.45 | $2,402.72 | 80 |
| COST | 2 | $979.83 | $976.61 | $1,953.22 | 65 |
| CRM | 8 | $268.33 | $270.70 | $2,165.60 | 65 |
| CSCO | 32 | $68.33 | $68.72 | $2,198.88 | 70 |
| CVX | 17 | $147.04 | $153.09 | $2,602.45 | 85 |
| DIS | 19 | $122.72 | $121.07 | $2,300.33 | 70 |
| GOOGL | 13 | $179.50 | $177.07 | $2,301.91 | 75 |
| GS | 3 | $717.52 | $697.85 | $2,093.53 | 70 |
| HD | 6 | $372.64 | $366.58 | $2,199.51 | 65 |
| INTC | 87 | $22.34 | $23.21 | $2,019.27 | 65 |
| JNJ | 13 | $155.89 | $155.41 | $2,020.33 | 65 |
| JPM | 9 | $291.61 | $283.80 | $2,554.20 | 75 |
| KO | 29 | $71.03 | $69.38 | $2,012.02 | 65 |
| LLY | 2 | $776.66 | $787.19 | $1,574.38 | 70 |
| MA | 4 | $563.08 | $561.52 | $2,246.08 | 70 |
| META | 3 | $717.12 | $735.84 | $2,207.52 | 85 |
| MRK | 29 | $82.50 | $83.75 | $2,428.75 | 75 |
| MSFT | 5 | $498.84 | $500.21 | $2,501.05 | 70 |
| NFLX | 1 | $1,279.00 | $1,276.50 | $1,276.50 | 65 |
| NKE | 28 | $76.05 | $73.93 | $2,070.04 | 65 |
| NVDA | 15 | $156.84 | $163.06 | $2,445.83 | 75 |
| ORCL | 10 | $233.47 | $233.94 | $2,339.42 | 70 |
| PEP | 15 | $136.57 | $133.49 | $2,002.35 | 65 |
| PFE | 86 | $25.22 | $25.46 | $2,189.55 | 70 |
| PG | 13 | $160.75 | $156.99 | $2,040.87 | 65 |
| PYPL | 28 | $76.84 | $74.83 | $2,095.24 | 65 |
| QCOM | 14 | $161.87 | $158.78 | $2,222.99 | 75 |
| T | 72 | $28.56 | $27.98 | $2,014.92 | 65 |
| TGT | 20 | $104.89 | $102.56 | $2,051.20 | 65 |
| TSLA | 6 | $288.62 | $295.00 | $1,769.99 | 60 |
| UNH | 7 | $314.75 | $300.71 | $2,105.00 | 65 |
| UNP | 9 | $236.60 | $237.53 | $2,137.72 | 70 |
| V | 6 | $355.95 | $355.12 | $2,130.72 | 70 |
| VZ | 48 | $43.15 | $42.51 | $2,040.24 | 65 |
| WFC | 29 | $82.27 | $81.82 | $2,372.78 | 75 |
| WMT | 21 | $97.35 | $97.16 | $2,040.35 | 65 |
| XOM | 20 | $109.83 | $113.86 | $2,277.20 | 70 |

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
| 2025-07-09 16:08:18 | SELL | NVDA | 1 | $163.02 | $5.80 | 75 |
| 2025-07-09 16:08:18 | SELL | XOM | 1 | $113.87 | $3.85 | 70 |
| 2025-07-09 16:08:18 | SELL | NKE | 1 | $73.90 | $-2.07 | 65 |
| 2025-07-09 16:08:18 | SELL | PYPL | 3 | $74.78 | $-5.58 | 65 |
| 2025-07-09 16:08:18 | BUY | BAC | 4 | $46.86 | N/A | 75 |
| 2025-07-09 16:08:18 | BUY | CVX | 1 | $153.09 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
