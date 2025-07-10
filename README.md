# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 16:57:31**

| Metric | Value |
|---|---|
| **Total Value** | **$101,484.22** |
| Cash | $1,964.88 |
| Holdings Value | $99,519.34 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.04 | $212.05 | $2,120.50 | 65 |
| ADBE | 5 | $377.60 | $372.71 | $1,863.57 | 65 |
| AMD | 15 | $134.94 | $144.50 | $2,167.50 | 70 |
| AMZN | 10 | $221.91 | $222.19 | $2,221.95 | 75 |
| AVGO | 8 | $275.34 | $273.85 | $2,190.76 | 70 |
| AXP | 7 | $325.28 | $323.71 | $2,265.96 | 75 |
| BA | 9 | $210.97 | $224.47 | $2,020.18 | 70 |
| BAC | 46 | $48.71 | $47.07 | $2,165.22 | 70 |
| C | 30 | $86.81 | $86.77 | $2,603.10 | 85 |
| CAT | 6 | $397.86 | $409.57 | $2,457.42 | 85 |
| COST | 2 | $979.83 | $976.37 | $1,952.73 | 65 |
| CRM | 8 | $268.33 | $266.91 | $2,135.27 | 65 |
| CSCO | 34 | $68.39 | $68.85 | $2,340.74 | 75 |
| CVX | 17 | $147.16 | $153.83 | $2,615.11 | 85 |
| DIS | 18 | $122.80 | $121.28 | $2,183.13 | 70 |
| GOOGL | 13 | $179.61 | $177.00 | $2,301.00 | 75 |
| GS | 3 | $717.52 | $707.32 | $2,121.96 | 75 |
| HD | 6 | $372.64 | $376.54 | $2,259.21 | 70 |
| INTC | 84 | $22.26 | $23.72 | $1,992.09 | 65 |
| JNJ | 13 | $155.89 | $157.90 | $2,052.64 | 70 |
| JPM | 9 | $291.61 | $287.46 | $2,587.14 | 85 |
| KO | 29 | $71.03 | $69.54 | $2,016.71 | 65 |
| LLY | 2 | $776.66 | $791.50 | $1,583.00 | 65 |
| MA | 4 | $563.08 | $563.88 | $2,255.52 | 65 |
| META | 3 | $717.12 | $725.85 | $2,177.54 | 85 |
| MRK | 28 | $82.46 | $84.52 | $2,366.68 | 75 |
| MSFT | 5 | $498.84 | $500.48 | $2,502.40 | 75 |
| NFLX | 1 | $1,279.00 | $1,255.63 | $1,255.63 | 65 |
| NKE | 29 | $75.83 | $75.31 | $2,183.85 | 70 |
| NVDA | 14 | $156.61 | $163.34 | $2,286.83 | 70 |
| ORCL | 9 | $233.31 | $236.29 | $2,126.61 | 70 |
| PEP | 15 | $136.57 | $136.25 | $2,043.77 | 70 |
| PFE | 83 | $25.20 | $25.80 | $2,141.82 | 70 |
| PG | 13 | $160.77 | $159.38 | $2,071.94 | 65 |
| PYPL | 31 | $76.64 | $76.03 | $2,357.09 | 75 |
| QCOM | 15 | $161.71 | $159.78 | $2,396.70 | 75 |
| T | 73 | $28.55 | $27.61 | $2,015.53 | 65 |
| TGT | 19 | $104.85 | $105.88 | $2,011.72 | 65 |
| TSLA | 6 | $288.62 | $303.22 | $1,819.32 | 65 |
| UNH | 6 | $298.34 | $302.49 | $1,814.95 | 65 |
| UNP | 9 | $236.20 | $238.54 | $2,146.90 | 75 |
| V | 6 | $355.85 | $356.44 | $2,138.67 | 65 |
| VZ | 48 | $43.15 | $42.00 | $2,016.00 | 65 |
| WFC | 32 | $82.33 | $82.53 | $2,641.12 | 85 |
| WMT | 21 | $97.36 | $95.83 | $2,012.43 | 65 |
| XOM | 22 | $110.12 | $114.52 | $2,519.44 | 85 |

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
| 2025-07-10 16:44:03 | SELL | QCOM | 1 | $159.93 | $-1.67 | 75 |
| 2025-07-10 16:44:03 | BUY | PFE | 1 | $25.82 | N/A | 65 |
| 2025-07-10 16:27:11 | SELL | BAC | 1 | $47.10 | $-1.58 | 70 |
| 2025-07-10 16:27:11 | SELL | PFE | 2 | $25.82 | $1.31 | 65 |
| 2025-07-10 16:27:11 | SELL | MRK | 3 | $84.41 | $5.29 | 75 |
| 2025-07-10 16:27:11 | SELL | VZ | 1 | $41.99 | $-1.13 | 65 |
| 2025-07-10 16:27:11 | SELL | T | 1 | $27.58 | $-0.96 | 65 |
| 2025-07-10 16:27:11 | BUY | NVDA | 1 | $163.26 | N/A | 85 |
| 2025-07-10 16:27:11 | BUY | INTC | 3 | $23.72 | N/A | 65 |
| 2025-07-10 16:27:11 | BUY | NKE | 1 | $75.41 | N/A | 75 |
| 2025-07-10 16:27:11 | BUY | QCOM | 1 | $159.70 | N/A | 85 |
| 2025-07-10 16:09:41 | SELL | NVDA | 2 | $162.90 | $10.99 | 70 |
| 2025-07-10 16:09:41 | SELL | INTC | 6 | $23.75 | $8.66 | 60 |
| 2025-07-10 16:09:41 | BUY | MRK | 3 | $84.54 | N/A | 85 |
| 2025-07-10 16:09:41 | BUY | WFC | 3 | $82.56 | N/A | 85 |

<!--TRADE_LOG_END--> 
