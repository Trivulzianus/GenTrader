# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 18:45:29**

| Metric | Value |
|---|---|
| **Total Value** | **$100,848.78** |
| Cash | $2,010.52 |
| Holdings Value | $98,838.27 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.66 | $2,096.64 | 65 |
| ADBE | 5 | $377.60 | $372.51 | $1,862.55 | 65 |
| AMD | 15 | $135.39 | $139.01 | $2,085.08 | 70 |
| AMZN | 11 | $221.90 | $222.54 | $2,447.94 | 85 |
| AVGO | 8 | $275.34 | $277.26 | $2,218.12 | 70 |
| AXP | 7 | $325.28 | $317.85 | $2,224.95 | 75 |
| BA | 9 | $210.97 | $226.53 | $2,038.77 | 65 |
| BAC | 44 | $48.81 | $46.84 | $2,060.74 | 65 |
| C | 31 | $86.66 | $85.61 | $2,653.76 | 85 |
| CAT | 6 | $397.86 | $403.22 | $2,419.32 | 70 |
| COST | 2 | $979.83 | $975.08 | $1,950.16 | 65 |
| CRM | 8 | $268.33 | $271.01 | $2,168.08 | 65 |
| CSCO | 31 | $68.29 | $69.22 | $2,145.66 | 70 |
| CVX | 15 | $146.26 | $153.11 | $2,296.65 | 70 |
| DIS | 17 | $122.93 | $120.73 | $2,052.41 | 65 |
| GOOGL | 13 | $179.49 | $176.16 | $2,290.08 | 75 |
| GS | 3 | $717.52 | $696.79 | $2,090.37 | 70 |
| HD | 6 | $372.64 | $369.17 | $2,215.01 | 70 |
| INTC | 88 | $22.33 | $23.35 | $2,054.80 | 65 |
| JNJ | 13 | $155.89 | $155.64 | $2,023.32 | 65 |
| JPM | 9 | $291.61 | $282.76 | $2,544.88 | 75 |
| KO | 29 | $71.03 | $69.26 | $2,008.54 | 65 |
| LLY | 2 | $776.66 | $785.26 | $1,570.52 | 70 |
| MA | 4 | $563.08 | $562.34 | $2,249.34 | 65 |
| META | 3 | $717.12 | $734.80 | $2,204.40 | 85 |
| MRK | 28 | $82.45 | $83.84 | $2,347.66 | 75 |
| MSFT | 5 | $498.84 | $502.51 | $2,512.55 | 85 |
| NFLX | 1 | $1,279.00 | $1,279.29 | $1,279.29 | 65 |
| NKE | 30 | $75.89 | $73.63 | $2,208.90 | 70 |
| NVDA | 16 | $157.22 | $162.77 | $2,604.32 | 85 |
| ORCL | 9 | $233.31 | $235.03 | $2,115.27 | 70 |
| PEP | 15 | $136.57 | $133.99 | $2,009.79 | 65 |
| PFE | 87 | $25.22 | $25.42 | $2,211.54 | 70 |
| PG | 13 | $160.75 | $157.02 | $2,041.26 | 65 |
| PYPL | 31 | $76.62 | $74.62 | $2,313.38 | 75 |
| QCOM | 14 | $161.87 | $159.09 | $2,227.26 | 70 |
| T | 73 | $28.55 | $28.16 | $2,055.32 | 65 |
| TGT | 20 | $104.89 | $102.27 | $2,045.30 | 65 |
| TSLA | 6 | $288.62 | $296.42 | $1,778.49 | 65 |
| UNH | 7 | $314.75 | $302.62 | $2,118.34 | 65 |
| UNP | 9 | $236.60 | $237.43 | $2,136.87 | 65 |
| V | 6 | $355.95 | $355.99 | $2,135.94 | 65 |
| VZ | 48 | $43.15 | $42.70 | $2,049.60 | 65 |
| WFC | 29 | $82.30 | $81.70 | $2,369.30 | 75 |
| WMT | 21 | $97.35 | $96.81 | $2,032.91 | 65 |
| XOM | 20 | $109.83 | $113.64 | $2,272.90 | 75 |

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
| 2025-07-09 18:45:21 | SELL | DIS | 1 | $120.70 | $-2.11 | 65 |
| 2025-07-09 18:45:21 | SELL | WFC | 1 | $81.69 | $-0.59 | 75 |
| 2025-07-09 18:45:21 | SELL | BA | 1 | $226.55 | $14.02 | 65 |
| 2025-07-09 18:45:21 | BUY | AMZN | 1 | $222.52 | N/A | 85 |
| 2025-07-09 18:45:21 | BUY | GOOGL | 1 | $176.15 | N/A | 75 |
| 2025-07-09 18:45:21 | BUY | PYPL | 2 | $74.62 | N/A | 75 |
| 2025-07-09 18:45:21 | BUY | CSCO | 1 | $69.21 | N/A | 70 |
| 2025-07-09 18:27:27 | SELL | GOOGL | 1 | $176.27 | $-3.23 | 65 |
| 2025-07-09 18:27:27 | SELL | BAC | 3 | $46.96 | $-5.20 | 65 |
| 2025-07-09 18:27:27 | SELL | WFC | 2 | $81.72 | $-1.05 | 75 |
| 2025-07-09 18:27:27 | SELL | CSCO | 4 | $69.18 | $3.26 | 65 |
| 2025-07-09 18:27:27 | SELL | CVX | 1 | $152.91 | $6.24 | 70 |
| 2025-07-09 18:27:27 | BUY | INTC | 1 | $23.33 | N/A | 65 |
| 2025-07-09 18:27:27 | BUY | NKE | 2 | $73.62 | N/A | 70 |
| 2025-07-09 18:27:27 | BUY | PYPL | 1 | $74.72 | N/A | 70 |
| 2025-07-09 18:27:27 | BUY | PFE | 7 | $25.39 | N/A | 70 |
| 2025-07-09 18:27:27 | BUY | T | 1 | $28.14 | N/A | 65 |
| 2025-07-09 18:11:03 | SELL | PYPL | 3 | $74.79 | $-5.53 | 65 |
| 2025-07-09 18:11:03 | SELL | PFE | 6 | $25.45 | $1.38 | 65 |
| 2025-07-09 18:11:03 | SELL | NKE | 1 | $73.82 | $-2.15 | 65 |
| 2025-07-09 18:11:03 | BUY | WFC | 2 | $81.94 | N/A | 85 |
| 2025-07-09 17:51:26 | BUY | INTC | 1 | $23.35 | N/A | 65 |
| 2025-07-09 17:51:26 | BUY | PYPL | 1 | $74.97 | N/A | 75 |
| 2025-07-09 17:51:26 | BUY | NKE | 1 | $73.70 | N/A | 70 |
| 2025-07-09 17:51:26 | BUY | PFE | 1 | $25.45 | N/A | 70 |

<!--TRADE_LOG_END--> 
