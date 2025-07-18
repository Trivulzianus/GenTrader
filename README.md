# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 14:40:58**

| Metric | Value |
|---|---|
| **Total Value** | **$101,070.13** |
| Cash | $949.41 |
| Holdings Value | $100,120.71 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.45 | $2,104.50 | 65 |
| ADBE | 6 | $375.23 | $364.69 | $2,188.14 | 65 |
| AMD | 14 | $159.84 | $157.77 | $2,208.78 | 70 |
| AMZN | 11 | $221.89 | $223.77 | $2,461.47 | 75 |
| AVGO | 8 | $275.34 | $282.42 | $2,259.32 | 70 |
| AXP | 7 | $309.18 | $303.19 | $2,122.33 | 65 |
| BA | 10 | $232.01 | $229.72 | $2,297.15 | 65 |
| BAC | 45 | $46.24 | $47.07 | $2,118.15 | 65 |
| C | 29 | $86.64 | $93.06 | $2,698.69 | 85 |
| CAT | 6 | $397.74 | $415.53 | $2,493.18 | 85 |
| COST | 2 | $979.83 | $958.87 | $1,917.74 | 65 |
| CRM | 8 | $267.44 | $259.62 | $2,076.96 | 65 |
| CSCO | 35 | $68.55 | $68.41 | $2,394.35 | 75 |
| CVX | 18 | $147.33 | $151.26 | $2,722.68 | 85 |
| DIS | 18 | $122.74 | $120.56 | $2,170.08 | 70 |
| GOOGL | 13 | $179.34 | $184.19 | $2,394.41 | 70 |
| GS | 3 | $717.52 | $703.71 | $2,111.13 | 70 |
| HD | 6 | $354.18 | $358.03 | $2,148.18 | 65 |
| INTC | 84 | $22.34 | $23.16 | $1,945.44 | 60 |
| JNJ | 14 | $155.97 | $164.43 | $2,301.97 | 70 |
| JPM | 8 | $292.14 | $290.06 | $2,320.48 | 70 |
| KO | 30 | $70.97 | $70.44 | $2,113.05 | 65 |
| LLY | 3 | $781.32 | $773.45 | $2,320.34 | 65 |
| MA | 4 | $563.08 | $552.44 | $2,209.76 | 65 |
| META | 3 | $717.12 | $695.59 | $2,086.76 | 70 |
| MRK | 26 | $82.73 | $81.06 | $2,107.55 | 65 |
| MSFT | 5 | $498.84 | $510.73 | $2,553.65 | 75 |
| NFLX | 1 | $1,208.39 | $1,212.42 | $1,212.42 | 65 |
| NKE | 29 | $71.98 | $72.31 | $2,096.99 | 65 |
| NVDA | 14 | $171.88 | $172.08 | $2,409.12 | 70 |
| ORCL | 9 | $232.91 | $246.00 | $2,214.00 | 65 |
| PEP | 15 | $135.89 | $144.73 | $2,170.95 | 65 |
| PFE | 85 | $25.27 | $24.53 | $2,085.18 | 65 |
| PG | 13 | $151.91 | $155.33 | $2,019.29 | 65 |
| PYPL | 29 | $72.18 | $73.77 | $2,139.33 | 65 |
| QCOM | 14 | $153.83 | $154.00 | $2,155.93 | 65 |
| T | 78 | $27.10 | $26.97 | $2,103.66 | 65 |
| TGT | 20 | $104.82 | $103.35 | $2,067.00 | 65 |
| TSLA | 6 | $318.51 | $325.85 | $1,955.10 | 65 |
| UNH | 7 | $298.51 | $284.81 | $1,993.67 | 65 |
| UNP | 9 | $225.02 | $224.76 | $2,022.88 | 65 |
| V | 6 | $355.85 | $348.33 | $2,089.98 | 65 |
| VZ | 51 | $40.87 | $40.94 | $2,087.94 | 65 |
| WFC | 27 | $78.73 | $79.87 | $2,156.49 | 65 |
| WMT | 22 | $97.29 | $95.33 | $2,097.26 | 65 |
| XOM | 20 | $109.90 | $109.86 | $2,197.30 | 70 |

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
| 2025-07-18 14:40:53 | SELL | NVDA | 1 | $172.07 | $0.18 | 70 |
| 2025-07-18 14:40:53 | SELL | BAC | 3 | $47.08 | $2.34 | 65 |
| 2025-07-18 14:40:53 | SELL | KO | 1 | $70.44 | $-0.51 | 65 |
| 2025-07-18 14:40:53 | SELL | MRK | 3 | $81.06 | $-4.49 | 65 |
| 2025-07-18 14:40:53 | BUY | AMD | 1 | $157.83 | N/A | 70 |
| 2025-07-18 14:40:53 | BUY | XOM | 1 | $111.66 | N/A | 70 |
| 2025-07-18 14:40:53 | BUY | PFE | 6 | $24.53 | N/A | 65 |
| 2025-07-18 14:40:53 | BUY | CSCO | 4 | $68.41 | N/A | 75 |
| 2025-07-18 14:40:53 | BUY | CVX | 2 | $151.30 | N/A | 85 |
| 2025-07-18 14:26:10 | SELL | NKE | 1 | $72.27 | $0.28 | 65 |
| 2025-07-18 14:26:10 | SELL | PFE | 6 | $24.58 | $-4.18 | 60 |
| 2025-07-18 14:26:10 | BUY | NVDA | 1 | $173.00 | N/A | 85 |
| 2025-07-18 14:26:10 | BUY | KO | 1 | $70.65 | N/A | 70 |
| 2025-07-18 14:09:21 | SELL | NVDA | 1 | $173.35 | $1.44 | 70 |
| 2025-07-18 14:09:21 | SELL | KO | 1 | $70.61 | $-0.35 | 65 |
| 2025-07-18 14:09:21 | SELL | DIS | 1 | $120.96 | $-1.68 | 65 |
| 2025-07-18 14:09:21 | SELL | NKE | 3 | $72.34 | $0.95 | 65 |
| 2025-07-18 14:09:21 | SELL | CSCO | 2 | $68.51 | $-0.11 | 65 |
| 2025-07-18 14:09:21 | BUY | NFLX | 1 | $1,208.39 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | PFE | 1 | $24.62 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | UNP | 9 | $225.02 | N/A | 65 |
| 2025-07-18 14:09:21 | BUY | TGT | 1 | $103.78 | N/A | 65 |
| 2025-07-18 14:08:57 | SELL | UNP | 9 | $225.04 | $-110.44 | 65 |
| 2025-07-18 14:08:51 | SELL | NFLX | 1 | $1,207.30 | $-71.70 | 65 |
| 2025-07-18 13:49:22 | SELL | WFC | 2 | $79.81 | $2.01 | 65 |

<!--TRADE_LOG_END--> 
