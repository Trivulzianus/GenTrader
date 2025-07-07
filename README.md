# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 18:56:33**

| Metric | Value |
|---|---|
| **Total Value** | **$100,655.82** |
| Cash | $236.36 |
| Holdings Value | $100,419.46 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $210.93 | $209.65 | $2,306.19 | 70 |
| ADBE | 5 | $377.60 | $376.90 | $1,884.50 | 65 |
| AMD | 15 | $135.73 | $135.00 | $2,025.07 | 65 |
| AMZN | 11 | $221.72 | $223.44 | $2,457.84 | 85 |
| AVGO | 8 | $275.34 | $274.22 | $2,193.76 | 70 |
| AXP | 7 | $324.46 | $321.84 | $2,252.88 | 70 |
| BA | 10 | $212.15 | $217.48 | $2,174.80 | 75 |
| BAC | 54 | $48.70 | $48.55 | $2,621.97 | 85 |
| C | 30 | $86.54 | $87.44 | $2,623.35 | 85 |
| CAT | 6 | $397.86 | $391.19 | $2,347.14 | 75 |
| COST | 2 | $979.83 | $991.11 | $1,982.21 | 65 |
| CRM | 8 | $268.33 | $269.43 | $2,155.44 | 65 |
| CSCO | 32 | $68.35 | $68.86 | $2,203.68 | 70 |
| CVX | 16 | $146.72 | $146.43 | $2,342.88 | 75 |
| DIS | 18 | $122.86 | $122.95 | $2,213.19 | 70 |
| GOOGL | 13 | $179.38 | $176.36 | $2,292.68 | 75 |
| GS | 3 | $717.52 | $709.23 | $2,127.69 | 70 |
| HD | 6 | $372.64 | $366.48 | $2,198.85 | 65 |
| INTC | 84 | $22.28 | $21.93 | $1,842.31 | 60 |
| JNJ | 13 | $155.80 | $155.40 | $2,020.14 | 65 |
| JPM | 9 | $292.50 | $291.00 | $2,619.00 | 85 |
| KO | 29 | $71.03 | $71.03 | $2,059.87 | 65 |
| LLY | 2 | $776.66 | $769.97 | $1,539.93 | 65 |
| MA | 4 | $563.08 | $562.28 | $2,249.12 | 65 |
| META | 3 | $717.12 | $722.60 | $2,167.80 | 70 |
| MRK | 29 | $82.38 | $81.19 | $2,354.65 | 75 |
| MSFT | 5 | $498.84 | $497.00 | $2,485.00 | 85 |
| NFLX | 1 | $1,279.00 | $1,289.70 | $1,289.70 | 70 |
| NKE | 30 | $75.86 | $76.44 | $2,293.05 | 75 |
| NVDA | 16 | $156.47 | $158.58 | $2,537.35 | 85 |
| ORCL | 9 | $233.30 | $233.23 | $2,099.07 | 75 |
| PEP | 15 | $136.57 | $134.72 | $2,020.82 | 70 |
| PFE | 84 | $25.29 | $25.30 | $2,124.78 | 70 |
| PG | 13 | $160.77 | $160.32 | $2,084.16 | 65 |
| PYPL | 31 | $76.77 | $76.11 | $2,359.41 | 75 |
| QCOM | 15 | $161.50 | $158.47 | $2,377.03 | 75 |
| T | 75 | $28.54 | $28.36 | $2,126.62 | 70 |
| TGT | 20 | $104.90 | $101.61 | $2,032.11 | 65 |
| TSLA | 7 | $289.38 | $292.79 | $2,049.56 | 65 |
| UNH | 7 | $314.75 | $302.80 | $2,119.60 | 65 |
| UNP | 10 | $236.56 | $235.09 | $2,350.85 | 75 |
| V | 6 | $355.95 | $355.53 | $2,133.18 | 70 |
| VZ | 47 | $43.72 | $42.84 | $2,013.25 | 65 |
| WFC | 29 | $82.26 | $81.75 | $2,370.75 | 75 |
| WMT | 21 | $97.22 | $99.11 | $2,081.31 | 65 |
| XOM | 20 | $109.91 | $110.75 | $2,214.90 | 70 |

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
| 2025-07-07 18:56:26 | SELL | INTC | 1 | $21.93 | $-0.34 | 60 |
| 2025-07-07 18:56:26 | SELL | XOM | 1 | $110.74 | $0.79 | 70 |
| 2025-07-07 18:56:26 | SELL | WMT | 1 | $98.36 | $1.09 | 65 |
| 2025-07-07 18:56:26 | SELL | BAC | 1 | $48.56 | $-0.14 | 85 |
| 2025-07-07 18:56:26 | SELL | VZ | 1 | $42.83 | $-0.86 | 65 |
| 2025-07-07 18:56:26 | SELL | CSCO | 1 | $68.86 | $0.50 | 70 |
| 2025-07-07 18:56:26 | BUY | AMZN | 1 | $223.43 | N/A | 85 |
| 2025-07-07 18:56:26 | BUY | NVDA | 2 | $158.57 | N/A | 85 |
| 2025-07-07 18:56:26 | BUY | PFE | 4 | $25.30 | N/A | 70 |
| 2025-07-07 18:56:26 | BUY | T | 3 | $28.36 | N/A | 70 |
| 2025-07-07 18:44:29 | SELL | NVDA | 2 | $158.39 | $3.88 | 70 |
| 2025-07-07 18:44:29 | SELL | AMZN | 2 | $223.03 | $2.48 | 70 |
| 2025-07-07 18:44:29 | SELL | INTC | 2 | $21.94 | $-0.64 | 60 |
| 2025-07-07 18:44:29 | SELL | WMT | 2 | $99.03 | $3.23 | 70 |
| 2025-07-07 18:44:29 | SELL | PFE | 8 | $25.27 | $-0.18 | 65 |
| 2025-07-07 18:44:29 | SELL | PEP | 1 | $134.67 | $-1.78 | 65 |
| 2025-07-07 18:44:29 | SELL | T | 1 | $28.36 | $-0.18 | 65 |
| 2025-07-07 18:44:29 | SELL | TGT | 1 | $101.50 | $-3.25 | 65 |
| 2025-07-07 18:44:29 | BUY | NKE | 1 | $76.24 | N/A | 75 |
| 2025-07-07 18:44:29 | BUY | C | 5 | $87.35 | N/A | 85 |
| 2025-07-07 18:44:29 | BUY | CSCO | 1 | $68.79 | N/A | 75 |
| 2025-07-07 18:44:29 | BUY | ORCL | 9 | $233.30 | N/A | 75 |
| 2025-07-07 18:27:28 | SELL | ORCL | 11 | $232.48 | $54.64 | 85 |
| 2025-07-07 18:27:28 | SELL | INTC | 3 | $21.94 | $-0.95 | 60 |
| 2025-07-07 18:27:28 | SELL | T | 2 | $28.30 | $-0.48 | 65 |

<!--TRADE_LOG_END--> 
