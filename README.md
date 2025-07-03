# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-03 16:26:56**

| Metric | Value |
|---|---|
| **Total Value** | **$101,914.32** |
| Cash | $2,529.40 |
| Holdings Value | $99,384.92 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.46 | $213.99 | $2,139.90 | 70 |
| ADBE | 5 | $377.60 | $381.94 | $1,909.70 | 65 |
| AMD | 15 | $135.93 | $137.93 | $2,068.99 | 70 |
| AMZN | 10 | $221.48 | $222.93 | $2,229.30 | 75 |
| AVGO | 8 | $269.90 | $274.50 | $2,196.04 | 65 |
| AXP | 8 | $324.40 | $328.58 | $2,628.64 | 85 |
| BA | 10 | $212.15 | $215.73 | $2,157.26 | 65 |
| BAC | 47 | $48.66 | $48.97 | $2,301.59 | 75 |
| C | 30 | $86.80 | $88.53 | $2,656.05 | 85 |
| CAT | 6 | $396.45 | $398.67 | $2,392.02 | 70 |
| COST | 2 | $979.83 | $985.60 | $1,971.20 | 65 |
| CRM | 8 | $268.33 | $273.37 | $2,186.96 | 65 |
| CSCO | 30 | $68.26 | $69.36 | $2,080.95 | 65 |
| CVX | 16 | $146.55 | $148.50 | $2,376.00 | 75 |
| DIS | 18 | $122.90 | $123.84 | $2,229.21 | 75 |
| GOOGL | 12 | $177.75 | $178.68 | $2,144.16 | 70 |
| GS | 3 | $717.52 | $721.59 | $2,164.77 | 85 |
| HD | 6 | $372.64 | $372.00 | $2,232.00 | 65 |
| INTC | 90 | $22.34 | $22.46 | $2,021.13 | 65 |
| JNJ | 13 | $155.80 | $156.03 | $2,028.39 | 65 |
| JPM | 9 | $292.50 | $295.70 | $2,661.30 | 85 |
| KO | 29 | $71.04 | $71.25 | $2,066.39 | 65 |
| LLY | 2 | $776.66 | $777.41 | $1,554.83 | 65 |
| MA | 3 | $561.03 | $568.80 | $1,706.41 | 65 |
| META | 3 | $717.12 | $719.12 | $2,157.38 | 85 |
| MRK | 25 | $82.46 | $81.34 | $2,033.58 | 65 |
| MSFT | 5 | $491.36 | $499.18 | $2,495.91 | 85 |
| NFLX | 1 | $1,279.00 | $1,300.31 | $1,300.31 | 70 |
| NKE | 27 | $75.71 | $76.34 | $2,061.18 | 65 |
| NVDA | 14 | $155.97 | $159.57 | $2,233.98 | 70 |
| ORCL | 11 | $227.08 | $237.71 | $2,614.81 | 85 |
| PEP | 15 | $136.59 | $135.45 | $2,031.75 | 65 |
| PFE | 80 | $25.30 | $25.50 | $2,040.00 | 65 |
| PG | 12 | $160.76 | $160.72 | $1,928.64 | 65 |
| PYPL | 29 | $76.81 | $76.77 | $2,226.18 | 70 |
| QCOM | 16 | $161.58 | $162.76 | $2,604.16 | 85 |
| T | 77 | $28.52 | $28.34 | $2,181.80 | 70 |
| TGT | 19 | $105.07 | $104.34 | $1,982.45 | 65 |
| TSLA | 6 | $313.02 | $316.84 | $1,901.04 | 55 |
| UNH | 7 | $314.75 | $309.83 | $2,168.81 | 65 |
| UNP | 9 | $236.50 | $237.68 | $2,139.12 | 70 |
| V | 6 | $352.90 | $358.30 | $2,149.80 | 70 |
| VZ | 46 | $43.73 | $43.48 | $2,000.31 | 65 |
| WFC | 29 | $82.23 | $83.44 | $2,419.76 | 80 |
| WMT | 23 | $97.37 | $98.07 | $2,255.69 | 75 |
| XOM | 21 | $109.97 | $112.15 | $2,355.05 | 75 |

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
| 2025-07-03 16:26:50 | SELL | KO | 1 | $71.25 | $0.20 | 65 |
| 2025-07-03 16:26:50 | SELL | NKE | 6 | $76.33 | $3.05 | 65 |
| 2025-07-03 16:26:50 | SELL | PYPL | 1 | $76.76 | $-0.04 | 70 |
| 2025-07-03 16:26:50 | SELL | CSCO | 2 | $69.36 | $2.06 | 65 |
| 2025-07-03 16:26:50 | SELL | PFE | 11 | $25.50 | $1.91 | 65 |
| 2025-07-03 16:26:50 | BUY | BAC | 2 | $48.98 | N/A | 75 |
| 2025-07-03 16:26:50 | BUY | INTC | 1 | $22.45 | N/A | 65 |
| 2025-07-03 16:26:50 | BUY | WMT | 2 | $98.07 | N/A | 75 |
| 2025-07-03 16:26:50 | BUY | WFC | 1 | $83.44 | N/A | 80 |
| 2025-07-03 16:26:50 | BUY | DIS | 1 | $123.83 | N/A | 75 |
| 2025-07-03 16:26:50 | BUY | QCOM | 2 | $162.78 | N/A | 85 |
| 2025-07-03 16:26:50 | BUY | ORCL | 2 | $237.69 | N/A | 85 |
| 2025-07-03 16:26:50 | BUY | T | 1 | $28.31 | N/A | 70 |
| 2025-07-03 16:09:40 | SELL | NVDA | 2 | $159.57 | $6.29 | 70 |
| 2025-07-03 16:09:40 | SELL | BAC | 2 | $48.99 | $0.65 | 70 |
| 2025-07-03 16:09:40 | SELL | XOM | 2 | $112.21 | $4.10 | 75 |
| 2025-07-03 16:09:40 | SELL | NKE | 1 | $76.53 | $0.68 | 80 |
| 2025-07-03 16:09:40 | SELL | WMT | 2 | $98.00 | $1.27 | 65 |
| 2025-07-03 16:09:40 | SELL | DIS | 1 | $123.95 | $1.05 | 65 |
| 2025-07-03 16:09:40 | SELL | WFC | 3 | $83.54 | $3.67 | 75 |
| 2025-07-03 16:09:40 | SELL | CSCO | 1 | $69.42 | $1.05 | 70 |
| 2025-07-03 16:09:40 | BUY | INTC | 1 | $22.54 | N/A | 65 |
| 2025-07-03 16:09:40 | BUY | KO | 1 | $71.22 | N/A | 70 |
| 2025-07-03 16:09:40 | BUY | PFE | 13 | $25.48 | N/A | 75 |
| 2025-07-03 16:09:40 | BUY | T | 1 | $28.35 | N/A | 70 |

<!--TRADE_LOG_END--> 
