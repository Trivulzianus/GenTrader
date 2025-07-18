# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 14:53:30**

| Metric | Value |
|---|---|
| **Total Value** | **$101,112.35** |
| Cash | $967.80 |
| Holdings Value | $100,144.55 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $210.66 | $2,106.60 | 70 |
| ADBE | 6 | $375.23 | $364.80 | $2,188.77 | 65 |
| AMD | 14 | $159.84 | $157.98 | $2,211.72 | 65 |
| AMZN | 11 | $221.89 | $223.74 | $2,461.14 | 75 |
| AVGO | 8 | $275.34 | $283.03 | $2,264.24 | 70 |
| AXP | 7 | $309.18 | $304.80 | $2,133.60 | 65 |
| BA | 10 | $232.01 | $229.20 | $2,292.00 | 70 |
| BAC | 47 | $46.28 | $47.14 | $2,215.58 | 70 |
| C | 29 | $86.64 | $93.26 | $2,704.54 | 85 |
| CAT | 6 | $397.74 | $415.53 | $2,493.18 | 85 |
| COST | 2 | $979.83 | $956.90 | $1,913.80 | 65 |
| CRM | 8 | $267.44 | $260.30 | $2,082.40 | 65 |
| CSCO | 33 | $68.56 | $68.38 | $2,256.38 | 70 |
| CVX | 18 | $147.33 | $151.48 | $2,726.64 | 85 |
| DIS | 18 | $122.74 | $120.56 | $2,170.08 | 65 |
| GOOGL | 13 | $179.34 | $184.65 | $2,400.45 | 70 |
| GS | 3 | $717.52 | $704.81 | $2,114.43 | 70 |
| HD | 6 | $354.18 | $358.82 | $2,152.92 | 65 |
| INTC | 89 | $22.40 | $23.30 | $2,073.26 | 65 |
| JNJ | 14 | $155.97 | $163.93 | $2,295.03 | 70 |
| JPM | 8 | $292.14 | $290.84 | $2,326.72 | 70 |
| KO | 30 | $70.97 | $70.27 | $2,107.95 | 65 |
| LLY | 3 | $781.32 | $773.34 | $2,320.02 | 65 |
| MA | 4 | $563.08 | $552.49 | $2,209.96 | 65 |
| META | 3 | $717.12 | $696.60 | $2,089.80 | 70 |
| MRK | 26 | $82.73 | $80.90 | $2,103.40 | 65 |
| MSFT | 5 | $498.84 | $511.08 | $2,555.42 | 85 |
| NFLX | 1 | $1,208.39 | $1,204.22 | $1,204.22 | 65 |
| NKE | 29 | $71.98 | $72.39 | $2,099.16 | 65 |
| NVDA | 13 | $171.84 | $172.34 | $2,240.49 | 70 |
| ORCL | 9 | $232.91 | $246.87 | $2,221.83 | 75 |
| PEP | 15 | $135.89 | $144.32 | $2,164.80 | 65 |
| PFE | 85 | $25.27 | $24.55 | $2,086.33 | 65 |
| PG | 13 | $151.91 | $154.85 | $2,013.05 | 65 |
| PYPL | 29 | $72.18 | $73.87 | $2,142.23 | 65 |
| QCOM | 14 | $153.83 | $154.53 | $2,163.42 | 65 |
| T | 78 | $27.10 | $26.93 | $2,100.15 | 65 |
| TGT | 20 | $104.82 | $102.98 | $2,059.60 | 65 |
| TSLA | 6 | $318.51 | $327.48 | $1,964.85 | 65 |
| UNH | 7 | $298.51 | $284.57 | $1,991.99 | 65 |
| UNP | 9 | $225.02 | $223.81 | $2,014.29 | 65 |
| V | 6 | $355.85 | $347.93 | $2,087.58 | 70 |
| VZ | 51 | $40.87 | $40.87 | $2,084.12 | 65 |
| WFC | 28 | $78.77 | $79.94 | $2,238.32 | 70 |
| WMT | 22 | $97.29 | $95.05 | $2,091.10 | 65 |
| XOM | 20 | $109.90 | $110.35 | $2,207.00 | 70 |

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
| 2025-07-18 14:53:25 | SELL | NVDA | 1 | $172.34 | $0.46 | 70 |
| 2025-07-18 14:53:25 | SELL | CSCO | 2 | $68.38 | $-0.35 | 70 |
| 2025-07-18 14:53:25 | BUY | BAC | 2 | $47.15 | N/A | 70 |
| 2025-07-18 14:53:25 | BUY | INTC | 5 | $23.30 | N/A | 65 |
| 2025-07-18 14:53:25 | BUY | WFC | 1 | $79.94 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
