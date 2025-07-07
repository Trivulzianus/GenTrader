# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 19:07:53**

| Metric | Value |
|---|---|
| **Total Value** | **$100,575.94** |
| Cash | $541.00 |
| Holdings Value | $100,034.94 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $210.93 | $209.65 | $2,306.15 | 75 |
| ADBE | 5 | $377.60 | $376.97 | $1,884.85 | 65 |
| AMD | 15 | $135.73 | $134.69 | $2,020.28 | 70 |
| AMZN | 11 | $221.72 | $223.28 | $2,456.08 | 85 |
| AVGO | 8 | $275.34 | $273.74 | $2,189.94 | 70 |
| AXP | 7 | $324.46 | $321.74 | $2,252.18 | 70 |
| BA | 10 | $212.15 | $216.99 | $2,169.85 | 75 |
| BAC | 54 | $48.70 | $48.50 | $2,619.13 | 85 |
| C | 30 | $86.54 | $87.33 | $2,619.90 | 85 |
| CAT | 6 | $397.86 | $390.57 | $2,343.39 | 75 |
| COST | 2 | $979.83 | $990.84 | $1,981.68 | 65 |
| CRM | 8 | $268.33 | $269.13 | $2,153.04 | 65 |
| CSCO | 33 | $68.37 | $68.82 | $2,271.06 | 75 |
| CVX | 17 | $146.70 | $146.46 | $2,489.74 | 85 |
| DIS | 18 | $122.86 | $122.86 | $2,211.49 | 70 |
| GOOGL | 13 | $179.38 | $176.19 | $2,290.47 | 75 |
| GS | 3 | $717.52 | $707.94 | $2,123.82 | 70 |
| HD | 6 | $372.64 | $366.37 | $2,198.22 | 65 |
| INTC | 84 | $22.28 | $21.91 | $1,840.02 | 60 |
| JNJ | 13 | $155.80 | $155.20 | $2,017.60 | 65 |
| JPM | 9 | $292.50 | $290.86 | $2,617.74 | 85 |
| KO | 29 | $71.03 | $70.96 | $2,057.84 | 65 |
| LLY | 2 | $776.66 | $769.85 | $1,539.70 | 65 |
| MA | 4 | $563.08 | $562.29 | $2,249.16 | 65 |
| META | 3 | $717.12 | $721.65 | $2,164.95 | 70 |
| MRK | 25 | $82.58 | $81.08 | $2,026.88 | 65 |
| MSFT | 5 | $498.84 | $496.62 | $2,483.10 | 85 |
| NFLX | 1 | $1,279.00 | $1,289.86 | $1,289.86 | 70 |
| NKE | 30 | $75.86 | $76.44 | $2,293.20 | 75 |
| NVDA | 14 | $156.20 | $158.37 | $2,217.11 | 70 |
| ORCL | 9 | $233.30 | $232.86 | $2,095.74 | 65 |
| PEP | 15 | $136.57 | $134.61 | $2,019.15 | 65 |
| PFE | 84 | $25.29 | $25.27 | $2,122.26 | 70 |
| PG | 13 | $160.77 | $160.21 | $2,082.66 | 65 |
| PYPL | 31 | $76.77 | $75.95 | $2,354.40 | 75 |
| QCOM | 15 | $161.50 | $158.02 | $2,370.31 | 75 |
| T | 71 | $28.54 | $28.39 | $2,015.76 | 65 |
| TGT | 20 | $104.90 | $101.62 | $2,032.40 | 65 |
| TSLA | 7 | $289.38 | $293.08 | $2,051.56 | 65 |
| UNH | 7 | $314.75 | $302.95 | $2,120.65 | 65 |
| UNP | 11 | $236.39 | $234.75 | $2,582.20 | 85 |
| V | 6 | $355.95 | $355.56 | $2,133.36 | 70 |
| VZ | 47 | $43.72 | $42.88 | $2,015.20 | 65 |
| WFC | 29 | $82.26 | $81.67 | $2,368.29 | 75 |
| WMT | 21 | $97.22 | $99.08 | $2,080.78 | 70 |
| XOM | 20 | $109.91 | $110.59 | $2,211.80 | 75 |

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
| 2025-07-07 19:07:47 | SELL | NVDA | 2 | $158.38 | $3.82 | 70 |
| 2025-07-07 19:07:47 | SELL | MRK | 4 | $81.07 | $-5.20 | 65 |
| 2025-07-07 19:07:47 | SELL | T | 4 | $28.39 | $-0.58 | 65 |
| 2025-07-07 19:07:47 | BUY | UNP | 1 | $234.74 | N/A | 85 |
| 2025-07-07 19:07:47 | BUY | CSCO | 1 | $68.82 | N/A | 75 |
| 2025-07-07 19:07:47 | BUY | CVX | 1 | $146.43 | N/A | 85 |
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

<!--TRADE_LOG_END--> 
