# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-08 13:48:12**

| Metric | Value |
|---|---|
| **Total Value** | **$100,912.72** |
| Cash | $1,274.66 |
| Holdings Value | $99,638.05 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $208.98 | $2,089.80 | 65 |
| ADBE | 5 | $377.60 | $378.24 | $1,891.20 | 65 |
| AMD | 16 | $135.68 | $136.74 | $2,187.84 | 70 |
| AMZN | 10 | $221.61 | $222.79 | $2,227.95 | 70 |
| AVGO | 8 | $275.34 | $275.02 | $2,200.20 | 70 |
| AXP | 8 | $324.24 | $323.13 | $2,585.04 | 85 |
| BA | 10 | $212.15 | $219.33 | $2,193.30 | 65 |
| BAC | 47 | $48.73 | $47.73 | $2,243.30 | 70 |
| C | 30 | $86.58 | $86.84 | $2,605.20 | 85 |
| CAT | 6 | $397.86 | $394.41 | $2,366.44 | 70 |
| COST | 2 | $979.83 | $991.38 | $1,982.75 | 65 |
| CRM | 8 | $268.33 | $270.26 | $2,162.08 | 65 |
| CSCO | 33 | $68.38 | $68.66 | $2,265.78 | 70 |
| CVX | 16 | $146.70 | $149.37 | $2,389.88 | 80 |
| DIS | 17 | $122.84 | $123.32 | $2,096.47 | 70 |
| GOOGL | 12 | $179.60 | $176.41 | $2,116.92 | 65 |
| GS | 3 | $717.52 | $705.52 | $2,116.56 | 70 |
| HD | 6 | $372.64 | $368.35 | $2,210.07 | 65 |
| INTC | 89 | $22.29 | $22.79 | $2,028.23 | 65 |
| JNJ | 13 | $155.80 | $155.75 | $2,024.75 | 65 |
| JPM | 8 | $292.56 | $286.49 | $2,291.92 | 70 |
| KO | 29 | $71.03 | $70.44 | $2,042.62 | 65 |
| LLY | 2 | $776.66 | $784.40 | $1,568.80 | 65 |
| MA | 4 | $563.08 | $563.84 | $2,255.36 | 65 |
| META | 3 | $717.12 | $719.27 | $2,157.81 | 75 |
| MRK | 28 | $82.47 | $81.64 | $2,285.78 | 75 |
| MSFT | 5 | $498.84 | $496.69 | $2,483.43 | 75 |
| NFLX | 1 | $1,279.00 | $1,281.60 | $1,281.60 | 65 |
| NKE | 31 | $75.84 | $75.02 | $2,325.47 | 75 |
| NVDA | 16 | $156.59 | $158.83 | $2,541.28 | 85 |
| ORCL | 9 | $233.41 | $238.99 | $2,150.91 | 70 |
| PEP | 15 | $136.57 | $134.46 | $2,016.90 | 65 |
| PFE | 87 | $25.29 | $25.52 | $2,220.12 | 70 |
| PG | 13 | $160.77 | $158.88 | $2,065.44 | 65 |
| PYPL | 27 | $76.85 | $75.85 | $2,047.95 | 65 |
| QCOM | 14 | $161.75 | $159.60 | $2,234.40 | 70 |
| T | 77 | $28.53 | $28.32 | $2,181.03 | 70 |
| TGT | 20 | $104.90 | $101.75 | $2,035.10 | 65 |
| TSLA | 6 | $288.62 | $297.46 | $1,784.76 | 60 |
| UNH | 7 | $314.75 | $306.61 | $2,146.24 | 65 |
| UNP | 10 | $236.53 | $236.18 | $2,361.80 | 75 |
| V | 6 | $355.95 | $357.43 | $2,144.58 | 65 |
| VZ | 47 | $43.72 | $42.98 | $2,019.83 | 65 |
| WFC | 29 | $82.35 | $82.15 | $2,382.35 | 75 |
| WMT | 23 | $97.38 | $98.63 | $2,268.44 | 70 |
| XOM | 21 | $109.97 | $112.40 | $2,360.40 | 75 |

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
| 2025-07-08 12:32:02 | SELL | T | 5 | $28.41 | $-0.62 | 65 |
| 2025-07-08 12:32:02 | BUY | NKE | 1 | $76.53 | N/A | 75 |
| 2025-07-08 12:13:58 | SELL | PYPL | 1 | $76.18 | $-0.65 | 65 |
| 2025-07-08 12:13:58 | SELL | MRK | 1 | $80.90 | $-1.57 | 65 |
| 2025-07-08 12:13:58 | BUY | C | 4 | $87.60 | N/A | 85 |
| 2025-07-08 11:50:06 | SELL | BAC | 2 | $48.66 | $-0.09 | 75 |
| 2025-07-08 11:50:06 | SELL | C | 3 | $87.60 | $3.17 | 70 |

<!--TRADE_LOG_END--> 
