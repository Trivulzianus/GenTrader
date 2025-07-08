# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 14:08:50**

| Metric | Value |
|---|---|
| **Total Value** | **$100,613.03** |
| Cash | $1,119.36 |
| Holdings Value | $99,493.68 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.33 | $2,093.30 | 65 |
| ADBE | 5 | $377.60 | $378.45 | $1,892.27 | 65 |
| AMD | 15 | $135.62 | $136.37 | $2,045.55 | 65 |
| AMZN | 10 | $221.61 | $221.12 | $2,211.18 | 70 |
| AVGO | 8 | $275.34 | $274.23 | $2,193.84 | 70 |
| AXP | 8 | $324.24 | $321.57 | $2,572.56 | 75 |
| BA | 10 | $212.15 | $218.10 | $2,181.00 | 70 |
| BAC | 49 | $48.68 | $47.51 | $2,327.75 | 75 |
| C | 30 | $86.58 | $86.42 | $2,592.45 | 85 |
| CAT | 6 | $397.86 | $393.11 | $2,358.66 | 65 |
| COST | 2 | $979.83 | $993.73 | $1,987.45 | 65 |
| CRM | 8 | $268.33 | $272.02 | $2,176.20 | 65 |
| CSCO | 33 | $68.38 | $68.75 | $2,268.59 | 70 |
| CVX | 17 | $146.86 | $149.48 | $2,541.16 | 85 |
| DIS | 17 | $122.84 | $123.06 | $2,091.93 | 70 |
| GOOGL | 12 | $179.60 | $175.07 | $2,100.90 | 65 |
| GS | 3 | $717.52 | $700.80 | $2,102.41 | 70 |
| HD | 6 | $372.64 | $365.95 | $2,195.70 | 65 |
| INTC | 89 | $22.29 | $22.86 | $2,034.98 | 65 |
| JNJ | 13 | $155.80 | $155.74 | $2,024.56 | 65 |
| JPM | 8 | $292.56 | $285.65 | $2,285.24 | 70 |
| KO | 29 | $71.03 | $70.32 | $2,039.28 | 65 |
| LLY | 2 | $776.66 | $783.02 | $1,566.04 | 65 |
| MA | 4 | $563.08 | $563.93 | $2,255.72 | 65 |
| META | 3 | $717.12 | $717.82 | $2,153.46 | 65 |
| MRK | 29 | $82.43 | $81.13 | $2,352.77 | 75 |
| MSFT | 5 | $498.84 | $496.07 | $2,480.35 | 85 |
| NFLX | 1 | $1,279.00 | $1,280.79 | $1,280.79 | 65 |
| NKE | 28 | $76.04 | $73.88 | $2,068.63 | 65 |
| NVDA | 16 | $156.59 | $159.14 | $2,546.22 | 85 |
| ORCL | 9 | $233.41 | $237.22 | $2,134.98 | 65 |
| PEP | 15 | $136.57 | $133.88 | $2,008.20 | 65 |
| PFE | 87 | $25.29 | $25.50 | $2,218.07 | 70 |
| PG | 13 | $160.77 | $158.38 | $2,058.98 | 65 |
| PYPL | 31 | $76.64 | $75.19 | $2,330.89 | 75 |
| QCOM | 14 | $161.75 | $158.76 | $2,222.64 | 75 |
| T | 73 | $28.54 | $28.21 | $2,059.50 | 65 |
| TGT | 20 | $104.90 | $100.75 | $2,015.00 | 65 |
| TSLA | 6 | $288.62 | $296.76 | $1,780.56 | 65 |
| UNH | 7 | $314.75 | $304.23 | $2,129.58 | 65 |
| UNP | 10 | $236.53 | $235.69 | $2,356.91 | 75 |
| V | 6 | $355.95 | $356.66 | $2,139.95 | 70 |
| VZ | 47 | $43.72 | $42.91 | $2,016.87 | 65 |
| WFC | 29 | $82.35 | $81.78 | $2,371.48 | 75 |
| WMT | 23 | $97.38 | $98.34 | $2,261.82 | 70 |
| XOM | 21 | $109.97 | $112.73 | $2,367.33 | 75 |

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
| 2025-07-08 14:08:44 | SELL | AMD | 1 | $136.47 | $0.79 | 65 |
| 2025-07-08 14:08:44 | SELL | NKE | 3 | $73.92 | $-5.75 | 65 |
| 2025-07-08 14:08:44 | SELL | T | 4 | $28.22 | $-1.23 | 65 |
| 2025-07-08 14:08:44 | BUY | BAC | 2 | $47.51 | N/A | 75 |
| 2025-07-08 14:08:44 | BUY | PYPL | 4 | $75.20 | N/A | 75 |
| 2025-07-08 14:08:44 | BUY | MRK | 1 | $81.14 | N/A | 75 |
| 2025-07-08 14:08:44 | BUY | CVX | 1 | $149.45 | N/A | 85 |
| 2025-07-08 13:48:02 | SELL | AMZN | 1 | $222.81 | $1.09 | 70 |
| 2025-07-08 13:48:02 | SELL | BAC | 1 | $47.74 | $-0.97 | 70 |
| 2025-07-08 13:48:02 | SELL | CSCO | 1 | $68.65 | $0.26 | 70 |
| 2025-07-08 13:48:02 | BUY | NVDA | 3 | $158.83 | N/A | 85 |
| 2025-07-08 13:48:02 | BUY | INTC | 3 | $22.81 | N/A | 65 |
| 2025-07-08 13:48:02 | BUY | NKE | 1 | $75.03 | N/A | 75 |
| 2025-07-08 13:48:02 | BUY | MRK | 2 | $81.68 | N/A | 75 |
| 2025-07-08 13:48:02 | BUY | T | 5 | $28.33 | N/A | 70 |
| 2025-07-08 13:29:02 | SELL | TGT | 1 | $101.60 | $-3.15 | 65 |
| 2025-07-08 13:29:02 | SELL | T | 5 | $28.41 | $-0.62 | 65 |
| 2025-07-08 13:29:02 | BUY | BAC | 2 | $48.66 | N/A | 75 |
| 2025-07-08 13:29:02 | BUY | NKE | 1 | $76.53 | N/A | 75 |
| 2025-07-08 13:03:18 | SELL | BAC | 3 | $48.66 | $-0.14 | 70 |
| 2025-07-08 13:03:18 | SELL | NKE | 1 | $76.53 | $0.66 | 70 |
| 2025-07-08 13:03:18 | SELL | QCOM | 1 | $158.09 | $-3.41 | 70 |
| 2025-07-08 13:03:18 | BUY | BA | 1 | $218.63 | N/A | 70 |
| 2025-07-08 13:03:18 | BUY | T | 5 | $28.41 | N/A | 70 |
| 2025-07-08 12:32:02 | SELL | BA | 1 | $218.63 | $6.48 | 60 |

<!--TRADE_LOG_END--> 
