# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-17 16:56:49**

| Metric | Value |
|---|---|
| **Total Value** | **$101,214.74** |
| Cash | $234.70 |
| Holdings Value | $100,980.04 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.28 | $211.15 | $2,111.50 | 65 |
| ADBE | 6 | $375.23 | $365.51 | $2,193.06 | 65 |
| AMD | 14 | $160.03 | $159.88 | $2,238.32 | 70 |
| AMZN | 10 | $221.65 | $223.74 | $2,237.40 | 75 |
| AVGO | 8 | $275.34 | $287.44 | $2,299.52 | 65 |
| AXP | 7 | $309.18 | $313.69 | $2,195.83 | 65 |
| BA | 9 | $210.81 | $227.76 | $2,049.84 | 70 |
| BAC | 45 | $46.25 | $46.60 | $2,097.00 | 65 |
| C | 30 | $86.85 | $92.47 | $2,774.25 | 85 |
| CAT | 6 | $397.74 | $416.50 | $2,499.03 | 75 |
| COST | 2 | $979.83 | $952.26 | $1,904.52 | 65 |
| CRM | 8 | $267.44 | $258.97 | $2,071.76 | 65 |
| CSCO | 31 | $68.58 | $68.28 | $2,116.53 | 65 |
| CVX | 16 | $146.82 | $150.22 | $2,403.60 | 75 |
| DIS | 22 | $122.51 | $121.41 | $2,671.02 | 85 |
| GOOGL | 13 | $179.34 | $182.75 | $2,375.75 | 75 |
| GS | 3 | $717.52 | $708.90 | $2,126.70 | 75 |
| HD | 6 | $354.18 | $356.56 | $2,139.36 | 65 |
| INTC | 84 | $22.34 | $22.98 | $1,930.74 | 60 |
| JNJ | 13 | $155.43 | $163.03 | $2,119.33 | 65 |
| JPM | 9 | $291.90 | $287.43 | $2,586.87 | 75 |
| KO | 30 | $70.97 | $69.67 | $2,090.25 | 65 |
| LLY | 3 | $781.32 | $767.36 | $2,302.08 | 65 |
| MA | 4 | $563.08 | $552.96 | $2,211.84 | 65 |
| META | 3 | $717.12 | $702.52 | $2,107.56 | 70 |
| MRK | 29 | $82.56 | $81.45 | $2,362.05 | 75 |
| MSFT | 5 | $498.84 | $512.63 | $2,563.15 | 70 |
| NFLX | 1 | $1,279.00 | $1,261.73 | $1,261.73 | 65 |
| NKE | 30 | $71.91 | $73.00 | $2,189.85 | 70 |
| NVDA | 15 | $171.83 | $173.61 | $2,604.15 | 85 |
| ORCL | 9 | $232.91 | $247.21 | $2,224.89 | 70 |
| PEP | 16 | $136.49 | $144.33 | $2,309.28 | 70 |
| PFE | 84 | $25.28 | $24.54 | $2,061.23 | 65 |
| PG | 14 | $152.18 | $154.50 | $2,162.93 | 65 |
| PYPL | 28 | $72.12 | $73.54 | $2,059.08 | 65 |
| QCOM | 14 | $153.83 | $153.10 | $2,143.40 | 70 |
| T | 83 | $27.08 | $26.84 | $2,227.31 | 70 |
| TGT | 20 | $104.83 | $103.33 | $2,066.60 | 65 |
| TSLA | 6 | $318.51 | $321.33 | $1,928.00 | 60 |
| UNH | 7 | $298.51 | $288.85 | $2,021.92 | 65 |
| UNP | 10 | $236.33 | $227.68 | $2,276.80 | 65 |
| V | 6 | $355.85 | $349.59 | $2,097.54 | 65 |
| VZ | 50 | $40.87 | $40.86 | $2,043.00 | 65 |
| WFC | 26 | $78.69 | $80.11 | $2,082.73 | 65 |
| WMT | 22 | $97.29 | $95.10 | $2,092.20 | 65 |
| XOM | 21 | $109.97 | $111.83 | $2,348.53 | 75 |

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
| 2025-07-17 16:56:39 | SELL | INTC | 6 | $22.99 | $3.60 | 60 |
| 2025-07-17 16:56:39 | SELL | CSCO | 1 | $68.29 | $-0.29 | 65 |
| 2025-07-17 16:56:39 | BUY | NVDA | 2 | $173.66 | N/A | 85 |
| 2025-07-17 16:56:39 | BUY | NKE | 1 | $73.01 | N/A | 70 |
| 2025-07-17 16:56:39 | BUY | VZ | 50 | $40.87 | N/A | 65 |
| 2025-07-17 16:56:39 | BUY | T | 6 | $26.84 | N/A | 70 |
| 2025-07-17 16:56:16 | SELL | VZ | 51 | $40.86 | $-111.01 | 65 |
| 2025-07-17 16:44:33 | SELL | NKE | 2 | $73.14 | $2.38 | 65 |
| 2025-07-17 16:44:33 | SELL | WFC | 2 | $80.17 | $2.74 | 65 |
| 2025-07-17 16:44:33 | BUY | XOM | 2 | $111.66 | N/A | 75 |
| 2025-07-17 16:44:33 | BUY | INTC | 6 | $22.92 | N/A | 65 |
| 2025-07-17 16:27:10 | SELL | NVDA | 2 | $174.01 | $4.26 | 70 |
| 2025-07-17 16:27:10 | SELL | BAC | 3 | $46.61 | $1.01 | 65 |
| 2025-07-17 16:27:10 | SELL | INTC | 6 | $22.94 | $3.32 | 60 |
| 2025-07-17 16:27:10 | SELL | XOM | 2 | $111.70 | $3.44 | 65 |
| 2025-07-17 16:27:10 | SELL | NKE | 1 | $72.97 | $0.98 | 70 |
| 2025-07-17 16:27:10 | SELL | WFC | 1 | $80.18 | $1.33 | 70 |
| 2025-07-17 16:27:10 | BUY | DIS | 3 | $121.40 | N/A | 85 |
| 2025-07-17 16:27:10 | BUY | CSCO | 1 | $68.29 | N/A | 70 |
| 2025-07-17 16:10:07 | SELL | CSCO | 1 | $68.43 | $-0.15 | 65 |
| 2025-07-17 16:10:07 | BUY | NVDA | 2 | $173.51 | N/A | 85 |
| 2025-07-17 16:10:07 | BUY | NKE | 3 | $72.90 | N/A | 75 |
| 2025-07-17 16:10:07 | BUY | WFC | 1 | $80.31 | N/A | 75 |
| 2025-07-17 15:52:40 | SELL | NVDA | 2 | $173.43 | $3.11 | 70 |
| 2025-07-17 15:52:40 | SELL | NKE | 3 | $72.80 | $2.46 | 65 |

<!--TRADE_LOG_END--> 
