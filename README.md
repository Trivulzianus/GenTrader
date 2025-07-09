# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 16:27:06**

| Metric | Value |
|---|---|
| **Total Value** | **$100,716.69** |
| Cash | $1,857.40 |
| Holdings Value | $98,859.29 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $207.80 | $2,078.00 | 70 |
| ADBE | 5 | $377.60 | $374.18 | $1,870.90 | 65 |
| AMD | 15 | $135.39 | $138.15 | $2,072.18 | 70 |
| AMZN | 10 | $221.83 | $222.35 | $2,223.47 | 75 |
| AVGO | 8 | $275.34 | $277.17 | $2,217.36 | 65 |
| AXP | 7 | $325.28 | $318.29 | $2,228.03 | 75 |
| BA | 10 | $212.53 | $228.21 | $2,282.07 | 75 |
| BAC | 44 | $48.84 | $46.80 | $2,058.98 | 65 |
| C | 31 | $86.65 | $85.85 | $2,661.35 | 85 |
| CAT | 6 | $397.86 | $400.46 | $2,402.76 | 75 |
| COST | 2 | $979.83 | $976.21 | $1,952.42 | 65 |
| CRM | 8 | $268.33 | $270.32 | $2,162.56 | 65 |
| CSCO | 32 | $68.33 | $68.66 | $2,197.01 | 70 |
| CVX | 16 | $146.68 | $152.81 | $2,444.96 | 75 |
| DIS | 17 | $122.91 | $121.06 | $2,057.93 | 65 |
| GOOGL | 13 | $179.50 | $176.88 | $2,299.51 | 75 |
| GS | 3 | $717.52 | $696.65 | $2,089.95 | 70 |
| HD | 6 | $372.64 | $365.64 | $2,193.84 | 65 |
| INTC | 87 | $22.34 | $23.25 | $2,023.18 | 65 |
| JNJ | 13 | $155.89 | $155.37 | $2,019.81 | 65 |
| JPM | 9 | $291.61 | $283.41 | $2,550.66 | 75 |
| KO | 29 | $71.03 | $69.38 | $2,011.88 | 65 |
| LLY | 2 | $776.66 | $785.70 | $1,571.39 | 70 |
| MA | 4 | $563.08 | $560.51 | $2,242.04 | 65 |
| META | 3 | $717.12 | $735.65 | $2,206.95 | 85 |
| MRK | 29 | $82.50 | $83.71 | $2,427.59 | 75 |
| MSFT | 5 | $498.84 | $500.81 | $2,504.07 | 70 |
| NFLX | 1 | $1,279.00 | $1,278.06 | $1,278.06 | 65 |
| NKE | 29 | $75.98 | $73.86 | $2,141.80 | 70 |
| NVDA | 14 | $156.38 | $163.22 | $2,285.06 | 70 |
| ORCL | 10 | $233.47 | $234.31 | $2,343.15 | 70 |
| PEP | 15 | $136.57 | $133.50 | $2,002.50 | 65 |
| PFE | 86 | $25.22 | $25.44 | $2,187.44 | 70 |
| PG | 13 | $160.75 | $156.51 | $2,034.63 | 65 |
| PYPL | 31 | $76.63 | $74.67 | $2,314.77 | 75 |
| QCOM | 14 | $161.87 | $158.78 | $2,222.92 | 75 |
| T | 72 | $28.56 | $28.02 | $2,017.43 | 65 |
| TGT | 20 | $104.89 | $102.27 | $2,045.40 | 65 |
| TSLA | 6 | $288.62 | $294.98 | $1,769.89 | 65 |
| UNH | 7 | $314.75 | $300.85 | $2,105.93 | 65 |
| UNP | 9 | $236.60 | $237.06 | $2,133.49 | 75 |
| V | 6 | $355.95 | $354.24 | $2,125.41 | 65 |
| VZ | 48 | $43.15 | $42.52 | $2,041.20 | 65 |
| WFC | 30 | $82.25 | $81.67 | $2,450.25 | 80 |
| WMT | 21 | $97.35 | $97.00 | $2,037.11 | 65 |
| XOM | 20 | $109.83 | $113.60 | $2,272.00 | 75 |

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
| 2025-07-09 16:26:59 | SELL | NVDA | 1 | $163.21 | $6.37 | 70 |
| 2025-07-09 16:26:59 | SELL | BAC | 6 | $46.79 | $-10.79 | 65 |
| 2025-07-09 16:26:59 | SELL | DIS | 2 | $121.05 | $-3.34 | 65 |
| 2025-07-09 16:26:59 | SELL | CVX | 1 | $152.81 | $5.77 | 75 |
| 2025-07-09 16:26:59 | BUY | PYPL | 3 | $74.68 | N/A | 75 |
| 2025-07-09 16:26:59 | BUY | NKE | 1 | $73.87 | N/A | 70 |
| 2025-07-09 16:26:59 | BUY | WFC | 1 | $81.67 | N/A | 80 |
| 2025-07-09 16:26:59 | BUY | BA | 1 | $228.20 | N/A | 75 |
| 2025-07-09 16:26:59 | BUY | C | 1 | $85.85 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
