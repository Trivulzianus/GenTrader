# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 18:27:34**

| Metric | Value |
|---|---|
| **Total Value** | **$100,369.23** |
| Cash | $1,781.91 |
| Holdings Value | $98,587.32 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $210.93 | $209.28 | $2,302.08 | 75 |
| ADBE | 5 | $377.60 | $376.01 | $1,880.05 | 65 |
| AMD | 15 | $135.73 | $134.44 | $2,016.57 | 65 |
| AMZN | 12 | $221.79 | $222.57 | $2,670.89 | 85 |
| AVGO | 8 | $275.34 | $273.83 | $2,190.68 | 70 |
| AXP | 7 | $324.46 | $320.70 | $2,244.90 | 70 |
| BA | 10 | $212.15 | $215.85 | $2,158.50 | 70 |
| BAC | 55 | $48.70 | $48.47 | $2,665.58 | 85 |
| C | 25 | $86.37 | $87.23 | $2,180.75 | 70 |
| CAT | 6 | $397.86 | $388.88 | $2,333.28 | 70 |
| COST | 2 | $979.83 | $988.93 | $1,977.86 | 65 |
| CRM | 8 | $268.33 | $268.69 | $2,149.48 | 65 |
| CSCO | 32 | $68.35 | $68.69 | $2,197.92 | 70 |
| CVX | 16 | $146.72 | $145.93 | $2,334.92 | 75 |
| DIS | 18 | $122.86 | $122.75 | $2,209.50 | 70 |
| GOOGL | 13 | $179.38 | $175.88 | $2,286.44 | 75 |
| GS | 3 | $717.52 | $708.01 | $2,124.03 | 75 |
| HD | 6 | $372.64 | $365.10 | $2,190.57 | 65 |
| INTC | 87 | $22.27 | $21.93 | $1,907.48 | 60 |
| JNJ | 13 | $155.80 | $155.09 | $2,016.17 | 65 |
| JPM | 9 | $292.50 | $290.41 | $2,613.69 | 85 |
| KO | 29 | $71.03 | $70.94 | $2,057.26 | 65 |
| LLY | 2 | $776.66 | $765.71 | $1,531.41 | 65 |
| MA | 4 | $563.08 | $561.14 | $2,244.56 | 65 |
| META | 3 | $717.12 | $719.76 | $2,159.28 | 70 |
| MRK | 29 | $82.38 | $80.83 | $2,344.07 | 75 |
| MSFT | 5 | $498.84 | $495.83 | $2,479.17 | 70 |
| NFLX | 1 | $1,279.00 | $1,287.89 | $1,287.89 | 65 |
| NKE | 29 | $75.85 | $76.19 | $2,209.51 | 70 |
| NVDA | 16 | $156.45 | $157.95 | $2,527.20 | 75 |
| PEP | 16 | $136.45 | $134.44 | $2,151.04 | 70 |
| PFE | 88 | $25.29 | $25.17 | $2,214.97 | 70 |
| PG | 13 | $160.77 | $159.94 | $2,079.22 | 65 |
| PYPL | 31 | $76.77 | $75.75 | $2,348.25 | 75 |
| QCOM | 15 | $161.50 | $158.20 | $2,372.99 | 75 |
| T | 73 | $28.54 | $28.29 | $2,065.18 | 65 |
| TGT | 21 | $104.74 | $101.15 | $2,124.15 | 70 |
| TSLA | 7 | $289.38 | $291.79 | $2,042.53 | 60 |
| UNH | 7 | $314.75 | $301.50 | $2,110.50 | 65 |
| UNP | 10 | $236.56 | $234.31 | $2,343.15 | 75 |
| V | 6 | $355.95 | $354.94 | $2,129.64 | 70 |
| VZ | 48 | $43.70 | $42.78 | $2,053.68 | 65 |
| WFC | 29 | $82.26 | $81.60 | $2,366.44 | 75 |
| WMT | 24 | $97.42 | $98.97 | $2,375.40 | 75 |
| XOM | 21 | $109.95 | $110.41 | $2,318.51 | 75 |

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
| 2025-07-07 18:27:28 | SELL | ORCL | 11 | $232.48 | $54.64 | 85 |
| 2025-07-07 18:27:28 | SELL | INTC | 3 | $21.94 | $-0.95 | 60 |
| 2025-07-07 18:27:28 | SELL | T | 2 | $28.30 | $-0.48 | 65 |
| 2025-07-07 18:27:28 | BUY | AAPL | 1 | $209.39 | N/A | 75 |
| 2025-07-07 18:27:28 | BUY | AMZN | 1 | $222.73 | N/A | 85 |
| 2025-07-07 18:27:28 | BUY | BAC | 2 | $48.50 | N/A | 85 |
| 2025-07-07 18:27:28 | BUY | KO | 1 | $70.95 | N/A | 65 |
| 2025-07-07 18:27:28 | BUY | XOM | 1 | $110.39 | N/A | 75 |
| 2025-07-07 18:27:28 | BUY | WMT | 2 | $99.01 | N/A | 75 |
| 2025-07-07 18:27:28 | BUY | PYPL | 2 | $75.78 | N/A | 75 |
| 2025-07-07 18:27:28 | BUY | PFE | 4 | $25.19 | N/A | 70 |
| 2025-07-07 18:27:28 | BUY | VZ | 1 | $42.78 | N/A | 65 |
| 2025-07-07 18:27:28 | BUY | QCOM | 1 | $158.27 | N/A | 75 |
| 2025-07-07 18:27:28 | BUY | AVGO | 1 | $273.97 | N/A | 70 |
| 2025-07-07 18:27:28 | BUY | TGT | 1 | $101.18 | N/A | 70 |
| 2025-07-07 18:27:28 | BUY | PEP | 1 | $134.45 | N/A | 70 |
| 2025-07-07 18:10:56 | SELL | PYPL | 2 | $76.04 | $-1.49 | 70 |
| 2025-07-07 18:10:56 | SELL | C | 5 | $87.66 | $5.36 | 70 |
| 2025-07-07 18:10:56 | SELL | CSCO | 2 | $68.80 | $0.84 | 70 |
| 2025-07-07 18:10:56 | SELL | XOM | 1 | $110.36 | $0.41 | 70 |
| 2025-07-07 18:10:56 | BUY | NVDA | 2 | $158.41 | N/A | 85 |
| 2025-07-07 18:10:56 | BUY | AMZN | 1 | $223.59 | N/A | 85 |
| 2025-07-07 18:10:56 | BUY | INTC | 6 | $22.03 | N/A | 65 |
| 2025-07-07 18:10:56 | BUY | DIS | 1 | $123.00 | N/A | 75 |
| 2025-07-07 18:10:56 | BUY | PFE | 4 | $25.25 | N/A | 70 |

<!--TRADE_LOG_END--> 
