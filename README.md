# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 17:26:01**

| Metric | Value |
|---|---|
| **Total Value** | **$101,534.62** |
| Cash | $1,906.39 |
| Holdings Value | $99,628.23 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.59 | $2,125.90 | 75 |
| ADBE | 5 | $377.60 | $373.30 | $1,866.50 | 65 |
| AMD | 18 | $136.48 | $144.15 | $2,594.70 | 85 |
| AMZN | 10 | $221.91 | $222.36 | $2,223.60 | 75 |
| AVGO | 8 | $275.34 | $273.79 | $2,190.28 | 65 |
| AXP | 7 | $325.28 | $324.22 | $2,269.52 | 75 |
| BA | 9 | $210.97 | $224.80 | $2,023.20 | 70 |
| BAC | 48 | $48.64 | $47.09 | $2,260.32 | 75 |
| C | 30 | $86.81 | $86.80 | $2,604.00 | 85 |
| CAT | 6 | $397.86 | $410.14 | $2,460.84 | 70 |
| COST | 2 | $979.83 | $972.95 | $1,945.90 | 65 |
| CRM | 8 | $268.33 | $266.58 | $2,132.68 | 65 |
| CSCO | 34 | $68.39 | $68.86 | $2,341.41 | 75 |
| CVX | 15 | $146.27 | $153.83 | $2,307.45 | 75 |
| DIS | 18 | $122.80 | $121.47 | $2,186.55 | 70 |
| GOOGL | 13 | $179.61 | $178.11 | $2,315.41 | 75 |
| GS | 3 | $717.52 | $708.38 | $2,125.12 | 75 |
| HD | 6 | $372.64 | $376.90 | $2,261.40 | 70 |
| INTC | 84 | $22.27 | $23.73 | $1,993.74 | 65 |
| JNJ | 13 | $155.89 | $157.80 | $2,051.38 | 65 |
| JPM | 9 | $291.61 | $287.70 | $2,589.30 | 85 |
| KO | 29 | $71.03 | $69.54 | $2,016.66 | 65 |
| LLY | 2 | $776.66 | $793.94 | $1,587.87 | 70 |
| MA | 4 | $563.08 | $564.12 | $2,256.46 | 70 |
| META | 3 | $717.12 | $725.25 | $2,175.74 | 85 |
| MRK | 28 | $82.46 | $84.63 | $2,369.64 | 75 |
| MSFT | 5 | $498.84 | $500.71 | $2,503.57 | 85 |
| NFLX | 1 | $1,279.00 | $1,250.27 | $1,250.27 | 65 |
| NKE | 29 | $75.83 | $75.38 | $2,186.02 | 70 |
| NVDA | 14 | $156.61 | $163.44 | $2,288.09 | 70 |
| ORCL | 9 | $233.31 | $236.42 | $2,127.78 | 75 |
| PEP | 15 | $136.57 | $136.29 | $2,044.35 | 65 |
| PFE | 83 | $25.20 | $25.88 | $2,148.04 | 70 |
| PG | 13 | $160.77 | $159.44 | $2,072.72 | 65 |
| PYPL | 29 | $76.68 | $76.08 | $2,206.18 | 70 |
| QCOM | 15 | $161.71 | $159.88 | $2,398.20 | 75 |
| T | 73 | $28.55 | $27.62 | $2,016.26 | 65 |
| TGT | 20 | $104.91 | $106.11 | $2,122.10 | 70 |
| TSLA | 6 | $288.62 | $302.40 | $1,814.40 | 65 |
| UNH | 6 | $298.34 | $303.23 | $1,819.38 | 65 |
| UNP | 9 | $236.20 | $238.74 | $2,148.66 | 75 |
| V | 6 | $355.85 | $357.02 | $2,142.12 | 70 |
| VZ | 48 | $43.15 | $42.02 | $2,016.72 | 65 |
| WFC | 32 | $82.33 | $82.52 | $2,640.64 | 85 |
| WMT | 21 | $97.36 | $95.35 | $2,002.35 | 65 |
| XOM | 21 | $109.91 | $114.52 | $2,404.82 | 75 |

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
| 2025-07-10 17:25:53 | SELL | NVDA | 2 | $163.37 | $11.84 | 70 |
| 2025-07-10 17:25:53 | SELL | XOM | 1 | $114.53 | $4.41 | 75 |
| 2025-07-10 17:25:53 | SELL | PYPL | 2 | $76.08 | $-1.11 | 70 |
| 2025-07-10 17:25:53 | SELL | CVX | 2 | $153.84 | $13.36 | 75 |
| 2025-07-10 17:25:53 | BUY | INTC | 5 | $23.72 | N/A | 65 |
| 2025-07-10 17:25:53 | BUY | BAC | 2 | $47.10 | N/A | 75 |
| 2025-07-10 17:25:53 | BUY | AMD | 2 | $144.12 | N/A | 85 |
| 2025-07-10 17:25:53 | BUY | PFE | 5 | $25.88 | N/A | 70 |
| 2025-07-10 17:25:53 | BUY | C | 3 | $86.80 | N/A | 85 |
| 2025-07-10 17:25:53 | BUY | TGT | 1 | $106.11 | N/A | 70 |
| 2025-07-10 17:10:42 | SELL | INTC | 5 | $23.69 | $7.15 | 60 |
| 2025-07-10 17:10:42 | SELL | PFE | 5 | $25.88 | $3.42 | 65 |
| 2025-07-10 17:10:42 | SELL | C | 3 | $86.82 | $0.04 | 75 |
| 2025-07-10 17:10:42 | BUY | NVDA | 2 | $163.36 | N/A | 85 |
| 2025-07-10 17:10:42 | BUY | AMD | 1 | $144.26 | N/A | 75 |
| 2025-07-10 16:57:22 | SELL | NKE | 1 | $75.32 | $-0.49 | 70 |
| 2025-07-10 16:57:22 | SELL | TGT | 1 | $105.94 | $1.03 | 65 |
| 2025-07-10 16:57:22 | BUY | INTC | 5 | $23.72 | N/A | 65 |
| 2025-07-10 16:57:22 | BUY | XOM | 1 | $114.52 | N/A | 85 |
| 2025-07-10 16:57:22 | BUY | PFE | 5 | $25.81 | N/A | 70 |
| 2025-07-10 16:57:22 | BUY | C | 4 | $86.77 | N/A | 85 |
| 2025-07-10 16:44:03 | SELL | NVDA | 1 | $163.45 | $6.38 | 70 |
| 2025-07-10 16:44:03 | SELL | INTC | 4 | $23.73 | $5.91 | 60 |
| 2025-07-10 16:44:03 | SELL | XOM | 2 | $114.51 | $8.41 | 75 |
| 2025-07-10 16:44:03 | SELL | C | 4 | $86.78 | $-0.13 | 70 |

<!--TRADE_LOG_END--> 
