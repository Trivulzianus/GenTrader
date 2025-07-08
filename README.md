# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 15:26:30**

| Metric | Value |
|---|---|
| **Total Value** | **$100,736.20** |
| Cash | $1,201.98 |
| Holdings Value | $99,534.22 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $210.19 | $2,101.89 | 65 |
| ADBE | 5 | $377.60 | $383.68 | $1,918.38 | 65 |
| AMD | 16 | $135.69 | $137.52 | $2,200.32 | 70 |
| AMZN | 10 | $221.61 | $219.64 | $2,196.40 | 65 |
| AVGO | 8 | $275.34 | $273.99 | $2,191.92 | 65 |
| AXP | 8 | $324.24 | $320.56 | $2,564.48 | 85 |
| BA | 9 | $211.84 | $216.12 | $1,945.07 | 65 |
| BAC | 47 | $48.73 | $47.18 | $2,217.58 | 70 |
| C | 28 | $86.61 | $85.97 | $2,407.30 | 75 |
| CAT | 6 | $397.86 | $393.53 | $2,361.18 | 65 |
| COST | 2 | $979.83 | $992.07 | $1,984.13 | 65 |
| CRM | 8 | $268.33 | $274.43 | $2,195.45 | 65 |
| CSCO | 33 | $68.37 | $68.56 | $2,262.32 | 70 |
| CVX | 16 | $146.69 | $151.09 | $2,417.52 | 75 |
| DIS | 17 | $122.85 | $122.27 | $2,078.51 | 65 |
| GOOGL | 12 | $179.60 | $172.95 | $2,075.40 | 65 |
| GS | 3 | $717.52 | $699.47 | $2,098.39 | 70 |
| HD | 6 | $372.64 | $369.25 | $2,215.53 | 70 |
| INTC | 88 | $22.28 | $23.25 | $2,046.00 | 65 |
| JNJ | 13 | $155.81 | $156.11 | $2,029.43 | 65 |
| JPM | 9 | $291.61 | $283.48 | $2,551.32 | 75 |
| KO | 29 | $71.03 | $70.22 | $2,036.24 | 65 |
| LLY | 2 | $776.66 | $789.08 | $1,578.16 | 65 |
| MA | 4 | $563.08 | $563.04 | $2,252.18 | 65 |
| META | 3 | $717.12 | $716.18 | $2,148.54 | 70 |
| MRK | 29 | $82.43 | $81.86 | $2,373.94 | 75 |
| MSFT | 5 | $498.84 | $494.30 | $2,471.47 | 75 |
| NFLX | 1 | $1,279.00 | $1,269.24 | $1,269.24 | 65 |
| NKE | 30 | $75.91 | $74.00 | $2,219.85 | 70 |
| NVDA | 16 | $156.63 | $158.99 | $2,543.76 | 85 |
| ORCL | 9 | $233.41 | $234.72 | $2,112.43 | 70 |
| PEP | 15 | $136.57 | $135.03 | $2,025.45 | 65 |
| PFE | 81 | $25.26 | $25.75 | $2,086.15 | 65 |
| PG | 13 | $160.77 | $158.62 | $2,062.06 | 65 |
| PYPL | 31 | $76.64 | $75.04 | $2,326.24 | 75 |
| QCOM | 14 | $161.75 | $160.49 | $2,246.86 | 75 |
| T | 73 | $28.54 | $28.26 | $2,062.69 | 65 |
| TGT | 20 | $104.90 | $101.20 | $2,024.00 | 65 |
| TSLA | 6 | $288.62 | $301.80 | $1,810.80 | 65 |
| UNH | 7 | $314.75 | $306.33 | $2,144.31 | 65 |
| UNP | 11 | $236.72 | $237.78 | $2,615.58 | 75 |
| V | 6 | $355.95 | $356.07 | $2,136.45 | 65 |
| VZ | 47 | $43.72 | $43.15 | $2,027.82 | 65 |
| WFC | 29 | $82.34 | $81.54 | $2,364.66 | 75 |
| WMT | 21 | $97.43 | $97.48 | $2,047.08 | 65 |
| XOM | 22 | $110.14 | $113.17 | $2,489.74 | 75 |

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
| 2025-07-08 15:26:24 | SELL | XOM | 1 | $113.18 | $2.90 | 75 |
| 2025-07-08 15:26:24 | SELL | DIS | 1 | $122.26 | $-0.55 | 65 |
| 2025-07-08 15:26:24 | SELL | PFE | 4 | $25.75 | $1.90 | 65 |
| 2025-07-08 15:26:24 | SELL | C | 2 | $86.00 | $-1.14 | 75 |
| 2025-07-08 15:26:24 | SELL | CSCO | 1 | $68.57 | $0.19 | 70 |
| 2025-07-08 15:26:24 | SELL | CVX | 1 | $151.10 | $4.15 | 75 |
| 2025-07-08 15:26:24 | BUY | NVDA | 2 | $159.00 | N/A | 85 |
| 2025-07-08 15:26:24 | BUY | INTC | 1 | $23.26 | N/A | 65 |
| 2025-07-08 15:26:24 | BUY | NKE | 1 | $74.01 | N/A | 70 |
| 2025-07-08 15:08:40 | SELL | BAC | 3 | $47.21 | $-4.29 | 70 |
| 2025-07-08 15:08:40 | SELL | INTC | 1 | $23.42 | $1.15 | 65 |
| 2025-07-08 15:08:40 | SELL | WMT | 1 | $96.97 | $-0.44 | 65 |
| 2025-07-08 15:08:40 | SELL | PFE | 1 | $25.92 | $0.64 | 70 |
| 2025-07-08 15:08:40 | SELL | BA | 2 | $215.10 | $5.32 | 60 |
| 2025-07-08 15:08:40 | BUY | XOM | 2 | $113.91 | N/A | 85 |
| 2025-07-08 15:08:40 | BUY | C | 3 | $85.85 | N/A | 85 |
| 2025-07-08 15:08:40 | BUY | CSCO | 2 | $68.39 | N/A | 75 |
| 2025-07-08 15:08:40 | BUY | CVX | 1 | $151.76 | N/A | 85 |
| 2025-07-08 15:08:40 | BUY | UNP | 1 | $238.57 | N/A | 85 |
| 2025-07-08 14:52:28 | SELL | NVDA | 2 | $158.90 | $4.55 | 70 |
| 2025-07-08 14:52:28 | SELL | XOM | 1 | $113.88 | $3.77 | 75 |
| 2025-07-08 14:52:28 | SELL | WMT | 1 | $96.75 | $-0.63 | 65 |
| 2025-07-08 14:52:28 | SELL | PFE | 4 | $25.80 | $1.96 | 70 |
| 2025-07-08 14:52:28 | BUY | BAC | 3 | $47.14 | N/A | 75 |
| 2025-07-08 14:52:28 | BUY | INTC | 1 | $23.32 | N/A | 65 |

<!--TRADE_LOG_END--> 
