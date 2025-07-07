# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 19:25:10**

| Metric | Value |
|---|---|
| **Total Value** | **$100,596.72** |
| Cash | $1,023.46 |
| Holdings Value | $99,573.25 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.08 | $209.40 | $2,094.00 | 65 |
| ADBE | 5 | $377.60 | $376.74 | $1,883.70 | 65 |
| AMD | 15 | $135.73 | $134.88 | $2,023.20 | 65 |
| AMZN | 11 | $221.72 | $223.41 | $2,457.45 | 85 |
| AVGO | 8 | $275.34 | $274.06 | $2,192.44 | 70 |
| AXP | 7 | $324.46 | $321.63 | $2,251.41 | 65 |
| BA | 10 | $212.15 | $217.59 | $2,175.90 | 75 |
| BAC | 54 | $48.70 | $48.51 | $2,619.27 | 85 |
| C | 25 | $86.37 | $87.35 | $2,183.75 | 70 |
| CAT | 6 | $397.86 | $390.59 | $2,343.54 | 75 |
| COST | 2 | $979.83 | $990.26 | $1,980.52 | 65 |
| CRM | 8 | $268.33 | $269.29 | $2,154.32 | 65 |
| CSCO | 32 | $68.36 | $68.71 | $2,198.72 | 70 |
| CVX | 16 | $146.71 | $146.66 | $2,346.48 | 75 |
| DIS | 18 | $122.86 | $122.92 | $2,212.49 | 70 |
| GOOGL | 13 | $179.38 | $176.21 | $2,290.66 | 75 |
| GS | 3 | $717.52 | $708.12 | $2,124.36 | 70 |
| HD | 6 | $372.64 | $366.13 | $2,196.78 | 65 |
| INTC | 85 | $22.27 | $21.92 | $1,863.20 | 60 |
| JNJ | 13 | $155.80 | $155.04 | $2,015.52 | 65 |
| JPM | 9 | $292.50 | $291.14 | $2,620.26 | 85 |
| KO | 29 | $71.03 | $70.83 | $2,054.21 | 65 |
| LLY | 2 | $776.66 | $770.77 | $1,541.54 | 65 |
| MA | 4 | $563.08 | $562.68 | $2,250.72 | 65 |
| META | 3 | $717.12 | $721.21 | $2,163.64 | 75 |
| MRK | 28 | $82.42 | $81.00 | $2,268.00 | 75 |
| MSFT | 5 | $498.84 | $496.70 | $2,483.50 | 85 |
| NFLX | 1 | $1,279.00 | $1,289.00 | $1,289.00 | 65 |
| NKE | 29 | $75.84 | $76.45 | $2,217.20 | 70 |
| NVDA | 14 | $156.20 | $158.36 | $2,217.02 | 70 |
| ORCL | 10 | $233.29 | $233.12 | $2,331.20 | 75 |
| PEP | 15 | $136.57 | $134.49 | $2,017.35 | 65 |
| PFE | 86 | $25.29 | $25.22 | $2,168.92 | 70 |
| PG | 13 | $160.77 | $160.15 | $2,081.95 | 65 |
| PYPL | 31 | $76.77 | $76.03 | $2,357.09 | 75 |
| QCOM | 15 | $161.50 | $158.06 | $2,370.90 | 75 |
| T | 76 | $28.53 | $28.37 | $2,156.29 | 70 |
| TGT | 20 | $104.90 | $101.52 | $2,030.30 | 65 |
| TSLA | 7 | $289.38 | $293.81 | $2,056.70 | 65 |
| UNH | 7 | $314.75 | $303.39 | $2,123.73 | 65 |
| UNP | 10 | $236.54 | $234.88 | $2,348.75 | 75 |
| V | 6 | $355.95 | $355.84 | $2,135.04 | 70 |
| VZ | 47 | $43.72 | $42.86 | $2,014.26 | 65 |
| WFC | 29 | $82.26 | $81.81 | $2,372.49 | 75 |
| WMT | 21 | $97.22 | $99.06 | $2,080.36 | 70 |
| XOM | 20 | $109.91 | $110.75 | $2,215.10 | 70 |

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
| 2025-07-07 19:25:04 | SELL | AAPL | 1 | $209.43 | $-1.49 | 65 |
| 2025-07-07 19:25:04 | SELL | NKE | 1 | $76.50 | $0.64 | 70 |
| 2025-07-07 19:25:04 | SELL | C | 5 | $87.36 | $4.12 | 70 |
| 2025-07-07 19:25:04 | SELL | UNP | 1 | $234.88 | $-1.52 | 75 |
| 2025-07-07 19:25:04 | SELL | CSCO | 1 | $68.71 | $0.34 | 70 |
| 2025-07-07 19:25:04 | SELL | CVX | 1 | $146.66 | $-0.04 | 75 |
| 2025-07-07 19:25:04 | BUY | INTC | 1 | $21.92 | N/A | 60 |
| 2025-07-07 19:25:04 | BUY | MRK | 3 | $81.01 | N/A | 75 |
| 2025-07-07 19:25:04 | BUY | PFE | 2 | $25.23 | N/A | 70 |
| 2025-07-07 19:25:04 | BUY | ORCL | 1 | $233.21 | N/A | 75 |
| 2025-07-07 19:25:04 | BUY | T | 5 | $28.38 | N/A | 70 |
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

<!--TRADE_LOG_END--> 
