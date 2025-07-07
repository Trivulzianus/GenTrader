# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 18:44:34**

| Metric | Value |
|---|---|
| **Total Value** | **$100,572.00** |
| Cash | $571.90 |
| Holdings Value | $100,000.10 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $210.93 | $209.37 | $2,303.07 | 75 |
| ADBE | 5 | $377.60 | $376.62 | $1,883.12 | 65 |
| AMD | 15 | $135.73 | $134.71 | $2,020.65 | 65 |
| AMZN | 10 | $221.54 | $223.03 | $2,230.27 | 70 |
| AVGO | 8 | $275.34 | $273.85 | $2,190.80 | 70 |
| AXP | 7 | $324.46 | $321.49 | $2,250.39 | 65 |
| BA | 10 | $212.15 | $216.94 | $2,169.35 | 75 |
| BAC | 55 | $48.70 | $48.53 | $2,669.15 | 85 |
| C | 30 | $86.54 | $87.34 | $2,620.20 | 85 |
| CAT | 6 | $397.86 | $390.52 | $2,343.12 | 70 |
| COST | 2 | $979.83 | $990.81 | $1,981.61 | 65 |
| CRM | 8 | $268.33 | $269.00 | $2,151.96 | 65 |
| CSCO | 33 | $68.37 | $68.80 | $2,270.24 | 75 |
| CVX | 16 | $146.72 | $146.47 | $2,343.60 | 75 |
| DIS | 18 | $122.86 | $122.86 | $2,211.39 | 70 |
| GOOGL | 13 | $179.38 | $176.26 | $2,291.38 | 75 |
| GS | 3 | $717.52 | $709.10 | $2,127.28 | 70 |
| HD | 6 | $372.64 | $366.20 | $2,197.23 | 65 |
| INTC | 85 | $22.27 | $21.96 | $1,867.03 | 60 |
| JNJ | 13 | $155.80 | $155.31 | $2,019.03 | 65 |
| JPM | 9 | $292.50 | $290.97 | $2,618.72 | 85 |
| KO | 29 | $71.03 | $70.97 | $2,058.27 | 65 |
| LLY | 2 | $776.66 | $768.30 | $1,536.60 | 65 |
| MA | 4 | $563.08 | $561.83 | $2,247.32 | 65 |
| META | 3 | $717.12 | $721.31 | $2,163.93 | 70 |
| MRK | 29 | $82.38 | $81.12 | $2,352.48 | 75 |
| MSFT | 5 | $498.84 | $496.33 | $2,481.65 | 85 |
| NFLX | 1 | $1,279.00 | $1,287.80 | $1,287.80 | 65 |
| NKE | 30 | $75.86 | $76.27 | $2,288.10 | 75 |
| NVDA | 14 | $156.17 | $158.42 | $2,217.88 | 70 |
| ORCL | 9 | $233.30 | $233.43 | $2,100.83 | 75 |
| PEP | 15 | $136.57 | $134.68 | $2,020.13 | 65 |
| PFE | 80 | $25.29 | $25.27 | $2,021.59 | 65 |
| PG | 13 | $160.77 | $160.24 | $2,083.14 | 65 |
| PYPL | 31 | $76.77 | $75.93 | $2,353.83 | 75 |
| QCOM | 15 | $161.50 | $158.41 | $2,376.22 | 75 |
| T | 72 | $28.54 | $28.35 | $2,041.20 | 65 |
| TGT | 20 | $104.90 | $101.50 | $2,029.90 | 65 |
| TSLA | 7 | $289.38 | $292.57 | $2,048.02 | 65 |
| UNH | 7 | $314.75 | $302.38 | $2,116.65 | 65 |
| UNP | 10 | $236.56 | $234.88 | $2,348.80 | 75 |
| V | 6 | $355.95 | $355.38 | $2,132.25 | 70 |
| VZ | 48 | $43.70 | $42.88 | $2,058.00 | 65 |
| WFC | 29 | $82.26 | $81.70 | $2,369.38 | 75 |
| WMT | 22 | $97.27 | $99.06 | $2,179.21 | 70 |
| XOM | 21 | $109.95 | $110.83 | $2,327.33 | 75 |

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

<!--TRADE_LOG_END--> 
