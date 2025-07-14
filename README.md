# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-14 13:48:26**

| Metric | Value |
|---|---|
| **Total Value** | **$100,749.98** |
| Cash | $739.31 |
| Holdings Value | $100,010.67 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $208.14 | $2,081.40 | 65 |
| ADBE | 6 | $375.23 | $363.12 | $2,178.72 | 65 |
| AMD | 15 | $134.63 | $142.84 | $2,142.60 | 65 |
| AMZN | 12 | $222.22 | $225.33 | $2,703.96 | 85 |
| AVGO | 8 | $275.34 | $270.75 | $2,166.00 | 65 |
| AXP | 7 | $325.34 | $319.23 | $2,234.61 | 65 |
| BA | 10 | $212.59 | $230.71 | $2,307.08 | 70 |
| BAC | 47 | $48.70 | $46.78 | $2,198.89 | 70 |
| C | 26 | $86.65 | $86.80 | $2,256.80 | 70 |
| CAT | 5 | $396.39 | $406.67 | $2,033.35 | 70 |
| COST | 2 | $979.83 | $974.93 | $1,949.86 | 70 |
| CRM | 7 | $268.68 | $261.70 | $1,831.90 | 65 |
| CSCO | 33 | $68.40 | $67.74 | $2,235.42 | 70 |
| CVX | 17 | $147.16 | $154.12 | $2,620.04 | 85 |
| DIS | 18 | $122.80 | $120.45 | $2,168.10 | 65 |
| GOOGL | 14 | $179.65 | $180.59 | $2,528.26 | 75 |
| GS | 3 | $717.52 | $706.49 | $2,119.47 | 70 |
| HD | 6 | $372.64 | $371.08 | $2,226.48 | 65 |
| INTC | 88 | $22.38 | $23.08 | $2,031.04 | 65 |
| JNJ | 14 | $155.99 | $157.34 | $2,202.83 | 70 |
| JPM | 9 | $291.63 | $287.68 | $2,589.12 | 85 |
| KO | 29 | $71.03 | $70.00 | $2,030.00 | 65 |
| LLY | 3 | $781.32 | $795.19 | $2,385.57 | 70 |
| MA | 4 | $563.08 | $558.07 | $2,232.28 | 60 |
| META | 3 | $717.12 | $719.83 | $2,159.49 | 70 |
| MRK | 28 | $82.49 | $84.09 | $2,354.66 | 75 |
| MSFT | 5 | $498.84 | $502.15 | $2,510.77 | 75 |
| NFLX | 1 | $1,279.00 | $1,255.96 | $1,255.96 | 65 |
| NKE | 28 | $72.10 | $72.12 | $2,019.50 | 65 |
| NVDA | 13 | $156.17 | $162.74 | $2,115.62 | 65 |
| ORCL | 9 | $233.26 | $226.44 | $2,037.96 | 65 |
| PEP | 15 | $136.57 | $134.96 | $2,024.40 | 65 |
| PFE | 86 | $25.21 | $25.63 | $2,204.18 | 70 |
| PG | 13 | $160.78 | $155.43 | $2,020.59 | 65 |
| PYPL | 32 | $72.29 | $74.20 | $2,374.40 | 75 |
| QCOM | 14 | $162.09 | $154.06 | $2,156.84 | 65 |
| T | 76 | $27.11 | $27.41 | $2,083.17 | 65 |
| TGT | 20 | $104.91 | $104.14 | $2,082.80 | 65 |
| TSLA | 6 | $288.62 | $316.69 | $1,900.11 | 65 |
| UNH | 7 | $298.51 | $303.72 | $2,126.05 | 65 |
| UNP | 10 | $236.18 | $234.40 | $2,344.00 | 75 |
| V | 6 | $355.85 | $350.69 | $2,104.11 | 65 |
| VZ | 49 | $43.12 | $41.77 | $2,046.73 | 65 |
| WFC | 27 | $82.25 | $82.78 | $2,234.98 | 70 |
| WMT | 21 | $97.38 | $94.95 | $1,993.95 | 65 |
| XOM | 21 | $109.99 | $114.60 | $2,406.60 | 75 |

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
| 2025-07-14 13:48:21 | SELL | NVDA | 3 | $162.65 | $15.79 | 65 |
| 2025-07-14 13:48:21 | SELL | WFC | 1 | $82.75 | $0.48 | 70 |
| 2025-07-14 13:48:21 | SELL | CSCO | 1 | $67.74 | $-0.64 | 70 |
| 2025-07-14 13:48:21 | SELL | QCOM | 1 | $154.02 | $-7.52 | 65 |
| 2025-07-14 13:48:21 | BUY | JNJ | 1 | $157.31 | N/A | 70 |
| 2025-07-14 13:48:21 | BUY | AMZN | 1 | $225.02 | N/A | 85 |
| 2025-07-14 13:48:21 | BUY | INTC | 1 | $23.43 | N/A | 65 |
| 2025-07-14 13:48:21 | BUY | NKE | 28 | $72.10 | N/A | 65 |
| 2025-07-14 13:48:21 | BUY | PYPL | 3 | $74.08 | N/A | 75 |
| 2025-07-14 13:48:21 | BUY | MRK | 3 | $84.08 | N/A | 75 |
| 2025-07-14 13:48:21 | BUY | T | 1 | $26.97 | N/A | 65 |
| 2025-07-14 13:48:02 | SELL | NKE | 29 | $72.07 | $-113.39 | 65 |
| 2025-07-14 13:29:35 | SELL | NKE | 1 | $72.63 | $-3.24 | 65 |
| 2025-07-14 13:29:35 | SELL | C | 1 | $86.73 | $0.08 | 70 |
| 2025-07-14 13:29:35 | SELL | BA | 1 | $226.84 | $12.95 | 65 |
| 2025-07-14 13:29:35 | BUY | GOOGL | 1 | $180.19 | N/A | 85 |
| 2025-07-14 13:29:35 | BUY | AMD | 1 | $146.42 | N/A | 70 |
| 2025-07-14 13:29:35 | BUY | PFE | 7 | $25.65 | N/A | 70 |
| 2025-07-14 13:29:35 | BUY | CSCO | 2 | $67.95 | N/A | 75 |
| 2025-07-14 13:04:14 | SELL | XOM | 1 | $115.43 | $5.19 | 75 |
| 2025-07-14 13:04:14 | BUY | DIS | 1 | $119.87 | N/A | 70 |
| 2025-07-14 13:04:14 | BUY | NKE | 1 | $72.63 | N/A | 70 |
| 2025-07-14 13:04:14 | BUY | C | 1 | $86.73 | N/A | 75 |
| 2025-07-14 13:04:14 | BUY | T | 1 | $26.97 | N/A | 65 |
| 2025-07-14 12:32:17 | SELL | PFE | 7 | $25.65 | $3.08 | 65 |

<!--TRADE_LOG_END--> 
