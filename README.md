# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 14:53:27**

| Metric | Value |
|---|---|
| **Total Value** | **$101,112.54** |
| Cash | $714.06 |
| Holdings Value | $100,398.49 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.19 | $2,101.95 | 65 |
| ADBE | 6 | $375.23 | $362.94 | $2,177.64 | 65 |
| AMD | 14 | $160.07 | $159.97 | $2,239.54 | 70 |
| AMZN | 10 | $221.65 | $223.26 | $2,232.65 | 70 |
| AVGO | 8 | $275.34 | $285.67 | $2,285.36 | 65 |
| AXP | 7 | $309.18 | $312.34 | $2,186.38 | 65 |
| BA | 9 | $210.81 | $229.76 | $2,067.88 | 65 |
| BAC | 45 | $46.26 | $46.17 | $2,077.60 | 65 |
| C | 30 | $86.85 | $90.83 | $2,725.05 | 85 |
| CAT | 6 | $397.74 | $416.13 | $2,496.81 | 85 |
| COST | 2 | $979.83 | $949.38 | $1,898.76 | 65 |
| CRM | 8 | $267.44 | $257.69 | $2,061.52 | 65 |
| CSCO | 31 | $68.48 | $68.22 | $2,114.97 | 65 |
| CVX | 16 | $146.82 | $149.96 | $2,399.36 | 75 |
| DIS | 20 | $122.64 | $121.27 | $2,425.40 | 75 |
| GOOGL | 13 | $179.34 | $181.97 | $2,365.60 | 75 |
| GS | 3 | $717.52 | $708.59 | $2,125.77 | 85 |
| HD | 6 | $354.18 | $355.86 | $2,135.13 | 65 |
| INTC | 84 | $22.34 | $22.82 | $1,917.30 | 60 |
| JNJ | 13 | $155.43 | $162.64 | $2,114.32 | 65 |
| JPM | 9 | $291.90 | $287.69 | $2,589.26 | 75 |
| KO | 30 | $70.97 | $69.68 | $2,090.40 | 65 |
| LLY | 3 | $781.32 | $788.66 | $2,365.98 | 70 |
| MA | 4 | $563.08 | $552.83 | $2,211.32 | 65 |
| META | 3 | $717.12 | $700.82 | $2,102.45 | 85 |
| MRK | 28 | $82.58 | $82.00 | $2,296.14 | 70 |
| MSFT | 5 | $498.84 | $510.96 | $2,554.82 | 85 |
| NFLX | 1 | $1,279.00 | $1,258.72 | $1,258.72 | 65 |
| NKE | 30 | $71.91 | $73.09 | $2,192.70 | 70 |
| NVDA | 13 | $171.62 | $172.81 | $2,246.47 | 70 |
| ORCL | 9 | $232.91 | $249.91 | $2,249.19 | 65 |
| PEP | 16 | $136.49 | $144.28 | $2,308.56 | 70 |
| PFE | 85 | $25.27 | $24.57 | $2,088.03 | 65 |
| PG | 14 | $152.18 | $154.23 | $2,159.27 | 65 |
| PYPL | 28 | $72.12 | $72.88 | $2,040.64 | 65 |
| QCOM | 14 | $153.83 | $152.90 | $2,140.60 | 65 |
| T | 78 | $27.09 | $26.87 | $2,095.86 | 65 |
| TGT | 21 | $104.77 | $102.97 | $2,162.47 | 65 |
| TSLA | 6 | $318.51 | $322.45 | $1,934.70 | 60 |
| UNH | 7 | $298.51 | $287.81 | $2,014.67 | 60 |
| UNP | 10 | $236.33 | $227.60 | $2,276.05 | 65 |
| V | 6 | $355.85 | $349.55 | $2,097.30 | 65 |
| VZ | 51 | $43.04 | $40.93 | $2,087.43 | 65 |
| WFC | 28 | $78.77 | $80.16 | $2,244.48 | 70 |
| WMT | 22 | $97.29 | $95.08 | $2,091.87 | 65 |
| XOM | 21 | $109.96 | $111.91 | $2,350.11 | 75 |

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
| 2025-07-17 14:53:19 | SELL | NVDA | 1 | $172.82 | $1.11 | 70 |
| 2025-07-17 14:53:19 | SELL | AMD | 1 | $160.08 | $0.01 | 70 |
| 2025-07-17 14:53:19 | SELL | INTC | 2 | $22.80 | $0.89 | 60 |
| 2025-07-17 14:53:19 | SELL | DIS | 1 | $121.26 | $-1.31 | 75 |
| 2025-07-17 14:53:19 | SELL | MRK | 1 | $81.96 | $-0.60 | 70 |
| 2025-07-17 14:53:19 | SELL | ORCL | 1 | $249.93 | $15.33 | 65 |
| 2025-07-17 14:53:19 | BUY | XOM | 2 | $111.89 | N/A | 75 |
| 2025-07-17 14:53:19 | BUY | NKE | 1 | $73.09 | N/A | 70 |
| 2025-07-17 14:41:28 | SELL | NVDA | 1 | $171.37 | $-0.31 | 70 |
| 2025-07-17 14:41:28 | SELL | AMD | 1 | $160.24 | $0.16 | 70 |
| 2025-07-17 14:41:28 | SELL | INTC | 5 | $22.69 | $1.60 | 60 |
| 2025-07-17 14:41:28 | SELL | NKE | 3 | $72.86 | $2.69 | 65 |
| 2025-07-17 14:41:28 | SELL | DIS | 1 | $120.84 | $-1.65 | 75 |
| 2025-07-17 14:41:28 | BUY | PFE | 1 | $24.62 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | WFC | 2 | $79.96 | N/A | 70 |
| 2025-07-17 14:41:28 | BUY | VZ | 1 | $40.96 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | ORCL | 1 | $249.18 | N/A | 80 |
| 2025-07-17 14:41:28 | BUY | T | 1 | $26.91 | N/A | 65 |
| 2025-07-17 14:41:28 | BUY | CVX | 1 | $149.46 | N/A | 75 |
| 2025-07-17 14:26:31 | SELL | XOM | 1 | $112.23 | $2.35 | 65 |
| 2025-07-17 14:26:31 | BUY | NVDA | 2 | $172.63 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | AMD | 2 | $160.08 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | DIS | 3 | $121.17 | N/A | 85 |
| 2025-07-17 14:26:31 | BUY | NKE | 3 | $72.73 | N/A | 75 |
| 2025-07-17 14:26:31 | BUY | UNP | 1 | $231.18 | N/A | 75 |

<!--TRADE_LOG_END--> 
