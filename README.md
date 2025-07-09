# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-09 20:09:08**

| Metric | Value |
|---|---|
| **Total Value** | **$100,967.06** |
| Cash | $1,130.57 |
| Holdings Value | $99,836.49 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $211.14 | $2,111.40 | 70 |
| ADBE | 5 | $377.60 | $373.38 | $1,866.90 | 65 |
| AMD | 15 | $135.39 | $138.41 | $2,076.15 | 65 |
| AMZN | 11 | $221.90 | $222.54 | $2,447.94 | 85 |
| AVGO | 8 | $275.34 | $277.90 | $2,223.20 | 70 |
| AXP | 7 | $325.28 | $317.44 | $2,222.08 | 75 |
| BA | 9 | $210.97 | $226.52 | $2,038.68 | 65 |
| BAC | 46 | $48.73 | $46.83 | $2,154.18 | 70 |
| C | 31 | $86.66 | $85.75 | $2,658.25 | 85 |
| CAT | 6 | $397.86 | $402.30 | $2,413.78 | 70 |
| COST | 2 | $979.83 | $982.09 | $1,964.18 | 65 |
| CRM | 8 | $268.33 | $270.94 | $2,167.54 | 65 |
| CSCO | 33 | $68.35 | $69.27 | $2,285.91 | 75 |
| CVX | 16 | $146.70 | $153.02 | $2,448.32 | 75 |
| DIS | 18 | $122.80 | $120.62 | $2,171.16 | 70 |
| GOOGL | 13 | $179.51 | $176.62 | $2,296.06 | 75 |
| GS | 3 | $717.52 | $696.78 | $2,090.34 | 70 |
| HD | 6 | $372.64 | $371.05 | $2,226.30 | 70 |
| INTC | 85 | $22.29 | $23.44 | $1,992.40 | 65 |
| JNJ | 13 | $155.89 | $156.28 | $2,031.64 | 70 |
| JPM | 9 | $291.61 | $283.06 | $2,547.54 | 75 |
| KO | 29 | $71.03 | $69.48 | $2,014.92 | 65 |
| LLY | 2 | $776.66 | $786.54 | $1,573.09 | 65 |
| MA | 4 | $563.08 | $564.92 | $2,259.68 | 65 |
| META | 3 | $717.12 | $732.78 | $2,198.34 | 85 |
| MRK | 28 | $82.45 | $83.72 | $2,344.02 | 75 |
| MSFT | 5 | $498.84 | $503.51 | $2,517.55 | 85 |
| NFLX | 1 | $1,279.00 | $1,288.28 | $1,288.28 | 70 |
| NKE | 31 | $75.79 | $73.58 | $2,280.98 | 75 |
| NVDA | 16 | $157.22 | $162.88 | $2,606.08 | 85 |
| ORCL | 9 | $233.31 | $235.88 | $2,122.92 | 70 |
| PEP | 15 | $136.57 | $134.48 | $2,017.20 | 65 |
| PFE | 85 | $25.21 | $25.55 | $2,171.75 | 70 |
| PG | 13 | $160.75 | $157.43 | $2,046.59 | 65 |
| PYPL | 31 | $76.62 | $74.83 | $2,319.73 | 75 |
| QCOM | 14 | $161.87 | $159.35 | $2,230.90 | 70 |
| T | 71 | $28.56 | $28.11 | $1,995.65 | 65 |
| TGT | 20 | $104.89 | $102.43 | $2,048.60 | 65 |
| TSLA | 6 | $288.62 | $295.88 | $1,775.28 | 65 |
| UNH | 7 | $314.75 | $302.33 | $2,116.31 | 65 |
| UNP | 9 | $236.60 | $236.46 | $2,128.14 | 75 |
| V | 7 | $356.12 | $357.16 | $2,500.12 | 85 |
| VZ | 47 | $43.16 | $42.62 | $2,003.14 | 65 |
| WFC | 31 | $82.27 | $81.76 | $2,534.56 | 85 |
| WMT | 21 | $97.35 | $96.82 | $2,033.22 | 65 |
| XOM | 20 | $109.83 | $113.78 | $2,275.50 | 75 |

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
| 2025-07-09 20:08:59 | SELL | PFE | 1 | $25.55 | $0.33 | 70 |
| 2025-07-09 20:08:59 | SELL | T | 1 | $28.11 | $-0.45 | 65 |
| 2025-07-09 20:08:59 | SELL | CVX | 1 | $153.02 | $5.95 | 75 |
| 2025-07-09 20:08:59 | SELL | VZ | 1 | $42.62 | $-0.53 | 65 |
| 2025-07-09 20:08:59 | BUY | V | 1 | $357.16 | N/A | 85 |
| 2025-07-09 20:08:59 | BUY | INTC | 4 | $23.44 | N/A | 65 |
| 2025-07-09 20:08:59 | BUY | NKE | 2 | $73.58 | N/A | 75 |
| 2025-07-09 20:08:59 | BUY | WFC | 2 | $81.76 | N/A | 85 |
| 2025-07-09 20:08:59 | BUY | CSCO | 1 | $69.27 | N/A | 75 |
| 2025-07-09 19:50:04 | SELL | INTC | 6 | $23.43 | $6.69 | 60 |
| 2025-07-09 19:50:04 | SELL | CSCO | 1 | $69.21 | $0.87 | 70 |
| 2025-07-09 19:50:04 | BUY | GOOGL | 1 | $176.74 | N/A | 75 |
| 2025-07-09 19:50:04 | BUY | DIS | 1 | $120.89 | N/A | 70 |
| 2025-07-09 19:50:04 | BUY | PYPL | 1 | $74.86 | N/A | 75 |
| 2025-07-09 19:50:04 | BUY | NKE | 1 | $73.72 | N/A | 70 |
| 2025-07-09 19:36:16 | SELL | GOOGL | 1 | $176.47 | $-3.02 | 65 |
| 2025-07-09 19:36:16 | SELL | NKE | 3 | $73.92 | $-5.69 | 65 |
| 2025-07-09 19:36:16 | BUY | CVX | 1 | $153.36 | N/A | 85 |
| 2025-07-09 19:24:35 | SELL | DIS | 1 | $120.95 | $-1.85 | 65 |
| 2025-07-09 19:24:35 | SELL | PYPL | 1 | $74.80 | $-1.82 | 70 |
| 2025-07-09 19:24:35 | SELL | CVX | 1 | $153.29 | $6.23 | 75 |
| 2025-07-09 19:24:35 | BUY | CSCO | 1 | $69.28 | N/A | 75 |
| 2025-07-09 19:08:38 | SELL | CSCO | 1 | $69.25 | $0.91 | 70 |
| 2025-07-09 19:08:38 | BUY | DIS | 1 | $120.63 | N/A | 70 |
| 2025-07-09 19:08:38 | BUY | NKE | 1 | $73.64 | N/A | 75 |

<!--TRADE_LOG_END--> 
