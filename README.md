# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-18 16:58:29**

| Metric | Value |
|---|---|
| **Total Value** | **$100,978.06** |
| Cash | $758.83 |
| Holdings Value | $100,219.24 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.31 | $2,113.05 | 65 |
| ADBE | 6 | $375.23 | $365.48 | $2,192.88 | 65 |
| AMD | 14 | $159.84 | $157.80 | $2,209.15 | 70 |
| AMZN | 10 | $221.57 | $225.80 | $2,258.00 | 75 |
| AVGO | 8 | $275.34 | $282.89 | $2,263.12 | 70 |
| AXP | 7 | $309.18 | $306.43 | $2,145.01 | 65 |
| BA | 10 | $232.01 | $228.10 | $2,281.00 | 65 |
| BAC | 51 | $46.35 | $47.23 | $2,408.99 | 75 |
| C | 29 | $86.64 | $93.44 | $2,709.62 | 85 |
| CAT | 6 | $397.74 | $414.00 | $2,484.03 | 70 |
| COST | 2 | $979.83 | $954.13 | $1,908.26 | 65 |
| CRM | 8 | $267.44 | $259.75 | $2,078.04 | 65 |
| CSCO | 35 | $68.54 | $68.23 | $2,388.22 | 75 |
| CVX | 16 | $147.08 | $149.38 | $2,390.08 | 75 |
| DIS | 18 | $122.74 | $121.33 | $2,183.94 | 65 |
| GOOGL | 12 | $178.88 | $185.00 | $2,220.00 | 65 |
| GS | 3 | $717.52 | $706.61 | $2,119.83 | 70 |
| HD | 6 | $354.18 | $357.58 | $2,145.51 | 65 |
| INTC | 90 | $22.39 | $23.20 | $2,088.45 | 65 |
| JNJ | 14 | $155.97 | $164.13 | $2,297.82 | 70 |
| JPM | 8 | $292.14 | $291.83 | $2,334.64 | 70 |
| KO | 30 | $70.96 | $70.18 | $2,105.40 | 65 |
| LLY | 3 | $781.32 | $770.62 | $2,311.88 | 65 |
| MA | 4 | $563.08 | $551.67 | $2,206.68 | 65 |
| META | 3 | $717.12 | $698.69 | $2,096.07 | 70 |
| MRK | 26 | $82.73 | $80.28 | $2,087.28 | 65 |
| MSFT | 5 | $498.84 | $509.61 | $2,548.05 | 75 |
| NFLX | 1 | $1,208.39 | $1,205.96 | $1,205.96 | 65 |
| NKE | 31 | $72.02 | $72.54 | $2,248.74 | 70 |
| NVDA | 15 | $171.94 | $172.13 | $2,581.95 | 85 |
| ORCL | 9 | $232.91 | $245.58 | $2,210.22 | 70 |
| PEP | 15 | $135.89 | $143.54 | $2,153.10 | 65 |
| PFE | 85 | $25.27 | $24.43 | $2,076.83 | 65 |
| PG | 13 | $151.91 | $154.99 | $2,014.87 | 65 |
| PYPL | 29 | $72.18 | $73.98 | $2,145.42 | 65 |
| QCOM | 14 | $153.83 | $154.12 | $2,157.68 | 65 |
| T | 78 | $27.10 | $26.95 | $2,102.49 | 65 |
| TGT | 20 | $104.82 | $102.44 | $2,048.80 | 65 |
| TSLA | 6 | $318.51 | $325.38 | $1,952.28 | 60 |
| UNH | 7 | $283.57 | $281.94 | $1,973.58 | 65 |
| UNP | 9 | $225.02 | $224.07 | $2,016.63 | 65 |
| V | 6 | $355.85 | $348.16 | $2,088.96 | 65 |
| VZ | 51 | $40.87 | $40.83 | $2,082.08 | 65 |
| WFC | 29 | $78.84 | $80.44 | $2,332.76 | 70 |
| WMT | 22 | $97.29 | $95.05 | $2,091.10 | 65 |
| XOM | 20 | $109.90 | $108.04 | $2,160.80 | 65 |

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
| 2025-07-18 16:58:19 | SELL | GOOGL | 1 | $184.97 | $5.63 | 65 |
| 2025-07-18 16:58:19 | SELL | WFC | 1 | $80.44 | $1.54 | 70 |
| 2025-07-18 16:58:19 | BUY | NVDA | 1 | $172.14 | N/A | 85 |
| 2025-07-18 16:58:19 | BUY | INTC | 6 | $23.21 | N/A | 65 |
| 2025-07-18 16:58:19 | BUY | CSCO | 2 | $68.24 | N/A | 75 |
| 2025-07-18 16:58:19 | BUY | CVX | 1 | $149.43 | N/A | 75 |
| 2025-07-18 16:44:31 | SELL | INTC | 6 | $23.25 | $5.17 | 60 |
| 2025-07-18 16:44:31 | SELL | KO | 2 | $70.26 | $-1.31 | 65 |
| 2025-07-18 16:44:31 | SELL | CVX | 2 | $148.85 | $3.40 | 65 |
| 2025-07-18 16:44:31 | BUY | PFE | 5 | $24.48 | N/A | 65 |
| 2025-07-18 16:44:31 | BUY | WFC | 2 | $80.48 | N/A | 75 |
| 2025-07-18 16:44:31 | BUY | NKE | 2 | $72.54 | N/A | 70 |
| 2025-07-18 16:27:10 | SELL | NVDA | 1 | $172.01 | $0.08 | 70 |
| 2025-07-18 16:27:10 | SELL | PFE | 5 | $24.42 | $-4.21 | 60 |
| 2025-07-18 16:27:10 | BUY | KO | 2 | $70.18 | N/A | 70 |
| 2025-07-18 16:27:10 | BUY | INTC | 7 | $23.18 | N/A | 65 |
| 2025-07-18 16:27:10 | BUY | WFC | 2 | $80.35 | N/A | 70 |
| 2025-07-18 16:27:10 | BUY | VZ | 3 | $40.83 | N/A | 65 |
| 2025-07-18 16:10:58 | SELL | AMZN | 1 | $225.05 | $3.16 | 70 |
| 2025-07-18 16:10:58 | SELL | NKE | 2 | $72.50 | $0.98 | 65 |
| 2025-07-18 16:10:58 | SELL | WFC | 1 | $80.27 | $1.55 | 65 |
| 2025-07-18 16:10:58 | SELL | VZ | 3 | $40.84 | $-0.08 | 60 |
| 2025-07-18 15:53:05 | SELL | INTC | 7 | $23.44 | $7.19 | 60 |
| 2025-07-18 15:53:05 | SELL | CVX | 1 | $150.71 | $3.36 | 75 |
| 2025-07-18 15:53:05 | BUY | NVDA | 2 | $172.51 | N/A | 85 |

<!--TRADE_LOG_END--> 
