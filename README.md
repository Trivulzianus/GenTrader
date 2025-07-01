# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 16:48:17**

| Metric | Value |
|---|---|
| **Total Value** | **$101,014.98** |
| Cash | $305.56 |
| Holdings Value | $100,709.42 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.07 | $2,496.88 | 85 |
| ADBE | 5 | $385.76 | $390.97 | $1,954.85 | 65 |
| AMD | 14 | $140.68 | $137.08 | $1,919.12 | 65 |
| AMZN | 11 | $226.78 | $219.87 | $2,418.57 | 85 |
| AVGO | 7 | $274.91 | $267.29 | $1,871.00 | 85 |
| AXP | 6 | $315.94 | $321.63 | $1,929.78 | 65 |
| BA | 9 | $215.30 | $209.13 | $1,882.17 | 65 |
| BAC | 51 | $47.30 | $47.98 | $2,446.97 | 85 |
| C | 22 | $84.08 | $85.55 | $1,882.10 | 65 |
| CAT | 5 | $381.20 | $390.98 | $1,954.90 | 65 |
| COST | 2 | $991.47 | $984.57 | $1,969.14 | 65 |
| CRM | 9 | $274.64 | $273.19 | $2,458.71 | 85 |
| CSCO | 35 | $68.88 | $68.91 | $2,411.85 | 85 |
| CVX | 17 | $143.81 | $145.15 | $2,467.55 | 85 |
| DIS | 16 | $122.90 | $122.88 | $1,966.08 | 65 |
| GOOGL | 14 | $175.62 | $174.99 | $2,449.86 | 85 |
| GS | 3 | $706.65 | $706.46 | $2,119.38 | 65 |
| HD | 7 | $369.90 | $376.25 | $2,633.75 | 85 |
| INTC | 83 | $22.23 | $22.93 | $1,903.60 | 65 |
| JNJ | 12 | $151.63 | $155.79 | $1,869.48 | 65 |
| JPM | 7 | $285.02 | $288.89 | $2,022.26 | 65 |
| KO | 26 | $70.42 | $71.77 | $1,866.08 | 65 |
| LLY | 3 | $767.33 | $779.70 | $2,339.09 | 65 |
| MA | 4 | $537.87 | $562.70 | $2,250.80 | 65 |
| META | 3 | $712.71 | $719.98 | $2,159.93 | 85 |
| MRK | 30 | $79.35 | $81.92 | $2,457.75 | 85 |
| MSFT | 4 | $492.89 | $493.48 | $1,973.92 | 65 |
| NFLX | 1 | $1,334.07 | $1,295.74 | $1,295.74 | 85 |
| NKE | 33 | $70.93 | $73.17 | $2,414.45 | 85 |
| NVDA | 16 | $154.76 | $154.12 | $2,465.84 | 85 |
| ORCL | 9 | $219.56 | $219.93 | $1,979.37 | 65 |
| PEP | 16 | $131.60 | $135.34 | $2,165.44 | 75 |
| PFE | 99 | $24.30 | $25.02 | $2,476.91 | 85 |
| PG | 12 | $159.73 | $161.04 | $1,932.48 | 65 |
| PYPL | 32 | $73.86 | $75.31 | $2,410.08 | 85 |
| QCOM | 15 | $159.12 | $160.16 | $2,402.40 | 85 |
| T | 85 | $28.52 | $28.79 | $2,446.72 | 85 |
| TGT | 21 | $98.42 | $104.36 | $2,191.56 | 75 |
| TSLA | 7 | $290.03 | $303.89 | $2,127.23 | 75 |
| UNH | 8 | $306.63 | $322.49 | $2,579.92 | 85 |
| UNP | 11 | $232.22 | $235.40 | $2,589.40 | 85 |
| V | 6 | $344.95 | $354.81 | $2,128.86 | 65 |
| VZ | 50 | $42.73 | $43.68 | $2,183.82 | 75 |
| WFC | 30 | $79.85 | $80.92 | $2,427.75 | 85 |
| WMT | 25 | $97.07 | $98.27 | $2,456.75 | 85 |
| XOM | 18 | $109.48 | $108.84 | $1,959.12 | 65 |

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
| 2025-07-01 16:48:11 | SELL | AMD | 3 | $141.90 | $3.02 | 65 |
| 2025-07-01 16:48:11 | SELL | XOM | 4 | $108.77 | $-2.32 | 65 |
| 2025-07-01 16:48:11 | SELL | INTC | 12 | $22.94 | $7.39 | 65 |
| 2025-07-01 16:48:11 | BUY | CRM | 1 | $273.07 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | PFE | 3 | $25.00 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | CSCO | 8 | $68.88 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | CVX | 1 | $145.12 | N/A | 85 |
| 2025-07-01 16:48:11 | BUY | VZ | 1 | $43.67 | N/A | 75 |
| 2025-07-01 16:48:11 | BUY | T | 1 | $28.78 | N/A | 85 |
| 2025-07-01 16:32:02 | SELL | JNJ | 1 | $156.45 | $4.44 | 65 |
| 2025-07-01 16:32:02 | SELL | PYPL | 1 | $75.43 | $1.52 | 85 |
| 2025-07-01 16:32:02 | SELL | NKE | 1 | $73.48 | $2.47 | 85 |
| 2025-07-01 16:32:02 | SELL | PFE | 1 | $25.17 | $0.89 | 85 |
| 2025-07-01 16:32:02 | SELL | KO | 3 | $71.72 | $3.51 | 65 |
| 2025-07-01 16:32:02 | SELL | WFC | 1 | $81.15 | $1.26 | 85 |
| 2025-07-01 16:32:02 | SELL | QCOM | 1 | $161.04 | $1.79 | 85 |
| 2025-07-01 16:32:02 | SELL | VZ | 1 | $43.66 | $0.93 | 75 |
| 2025-07-01 16:32:02 | SELL | T | 1 | $28.73 | $0.21 | 85 |
| 2025-07-01 16:32:02 | BUY | TSLA | 1 | $303.60 | N/A | 75 |
| 2025-07-01 16:32:02 | BUY | INTC | 14 | $22.40 | N/A | 75 |
| 2025-07-01 16:17:47 | SELL | AVGO | 2 | $275.65 | $1.15 | 65 |
| 2025-07-01 16:17:47 | BUY | JNJ | 1 | $157.22 | N/A | 75 |
| 2025-07-01 16:17:47 | BUY | AMD | 2 | $136.79 | N/A | 85 |
| 2025-07-01 16:17:47 | BUY | XOM | 2 | $109.36 | N/A | 85 |
| 2025-07-01 16:04:41 | SELL | XOM | 2 | $109.26 | $-0.15 | 75 |

<!--TRADE_LOG_END--> 
