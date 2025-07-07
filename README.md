# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-07 15:39:22**

| Metric | Value |
|---|---|
| **Total Value** | **$100,865.36** |
| Cash | $2,138.63 |
| Holdings Value | $98,726.74 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.35 | $212.03 | $2,120.35 | 65 |
| ADBE | 5 | $377.60 | $378.56 | $1,892.80 | 65 |
| AMD | 16 | $135.69 | $134.20 | $2,147.20 | 70 |
| AMZN | 11 | $221.66 | $224.17 | $2,465.87 | 80 |
| AVGO | 8 | $269.90 | $276.52 | $2,212.20 | 70 |
| AXP | 8 | $324.34 | $323.71 | $2,589.72 | 75 |
| BA | 10 | $212.15 | $215.30 | $2,153.00 | 70 |
| BAC | 54 | $48.71 | $48.87 | $2,638.99 | 85 |
| C | 30 | $86.68 | $87.89 | $2,636.55 | 85 |
| CAT | 6 | $397.86 | $392.19 | $2,353.11 | 85 |
| COST | 2 | $979.83 | $984.80 | $1,969.60 | 65 |
| CRM | 8 | $268.33 | $270.75 | $2,166.04 | 65 |
| CSCO | 32 | $68.34 | $69.00 | $2,207.84 | 70 |
| CVX | 16 | $146.70 | $146.61 | $2,345.76 | 75 |
| DIS | 17 | $122.86 | $123.33 | $2,096.53 | 65 |
| GOOGL | 13 | $179.44 | $177.65 | $2,309.43 | 75 |
| GS | 3 | $717.52 | $715.37 | $2,146.10 | 70 |
| HD | 6 | $372.64 | $368.03 | $2,208.18 | 65 |
| INTC | 93 | $22.25 | $22.01 | $2,046.93 | 65 |
| JNJ | 13 | $155.80 | $155.79 | $2,025.27 | 65 |
| JPM | 9 | $292.50 | $292.73 | $2,634.57 | 85 |
| KO | 28 | $71.03 | $71.11 | $1,991.08 | 65 |
| LLY | 2 | $776.66 | $771.56 | $1,543.12 | 65 |
| MA | 4 | $563.08 | $564.52 | $2,258.10 | 65 |
| META | 3 | $717.12 | $724.85 | $2,174.55 | 70 |
| MRK | 29 | $82.38 | $81.33 | $2,358.71 | 75 |
| MSFT | 5 | $498.84 | $498.05 | $2,490.25 | 85 |
| NFLX | 1 | $1,279.00 | $1,285.35 | $1,285.35 | 65 |
| NKE | 31 | $75.89 | $76.06 | $2,357.86 | 75 |
| NVDA | 14 | $156.19 | $157.91 | $2,210.74 | 70 |
| ORCL | 10 | $226.85 | $234.16 | $2,341.60 | 75 |
| PEP | 15 | $136.59 | $134.70 | $2,020.50 | 65 |
| PFE | 87 | $25.31 | $25.32 | $2,202.41 | 70 |
| PG | 13 | $160.77 | $160.17 | $2,082.21 | 65 |
| PYPL | 29 | $76.83 | $76.31 | $2,212.99 | 70 |
| QCOM | 14 | $161.69 | $158.66 | $2,221.24 | 75 |
| T | 77 | $28.52 | $28.34 | $2,182.57 | 70 |
| TGT | 20 | $104.92 | $101.18 | $2,023.68 | 65 |
| TSLA | 6 | $288.90 | $293.20 | $1,759.19 | 60 |
| UNH | 7 | $314.75 | $304.48 | $2,131.36 | 65 |
| UNP | 11 | $236.46 | $236.25 | $2,598.75 | 85 |
| VZ | 47 | $43.72 | $42.90 | $2,016.30 | 65 |
| WFC | 29 | $82.25 | $82.34 | $2,388.01 | 75 |
| WMT | 21 | $97.28 | $98.19 | $2,061.99 | 65 |
| XOM | 22 | $110.04 | $111.28 | $2,448.16 | 80 |

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
| 2025-07-07 15:39:15 | SELL | V | 6 | $356.17 | $19.60 | 65 |
| 2025-07-07 15:39:15 | SELL | DIS | 1 | $123.32 | $0.44 | 65 |
| 2025-07-07 15:39:15 | SELL | WMT | 2 | $98.19 | $1.67 | 65 |
| 2025-07-07 15:39:15 | SELL | PYPL | 1 | $76.31 | $-0.50 | 70 |
| 2025-07-07 15:39:15 | BUY | GOOGL | 1 | $177.71 | N/A | 75 |
| 2025-07-07 15:39:15 | BUY | AMD | 1 | $134.20 | N/A | 70 |
| 2025-07-07 15:39:15 | BUY | INTC | 8 | $22.01 | N/A | 65 |
| 2025-07-07 15:39:15 | BUY | NKE | 3 | $76.06 | N/A | 75 |
| 2025-07-07 15:39:15 | BUY | XOM | 2 | $111.28 | N/A | 80 |
| 2025-07-07 15:39:15 | BUY | PFE | 7 | $25.31 | N/A | 70 |
| 2025-07-07 15:39:15 | BUY | MRK | 4 | $81.38 | N/A | 75 |
| 2025-07-07 15:39:15 | BUY | C | 1 | $87.90 | N/A | 85 |
| 2025-07-07 15:39:15 | BUY | UNP | 1 | $236.27 | N/A | 85 |
| 2025-07-07 15:39:15 | BUY | ORCL | 1 | $234.18 | N/A | 75 |
| 2025-07-07 15:39:15 | BUY | T | 5 | $28.34 | N/A | 70 |
| 2025-07-07 15:26:23 | SELL | GOOGL | 1 | $177.19 | $-2.21 | 65 |
| 2025-07-07 15:26:23 | SELL | PFE | 6 | $25.31 | $0.00 | 65 |
| 2025-07-07 15:26:23 | SELL | MRK | 4 | $81.06 | $-5.11 | 65 |
| 2025-07-07 15:26:23 | SELL | WFC | 1 | $82.57 | $0.31 | 75 |
| 2025-07-07 15:26:23 | BUY | NKE | 1 | $76.03 | N/A | 70 |
| 2025-07-07 15:26:23 | BUY | C | 3 | $87.99 | N/A | 85 |
| 2025-07-07 15:07:46 | SELL | NVDA | 2 | $157.80 | $2.81 | 70 |
| 2025-07-07 15:07:46 | SELL | INTC | 1 | $22.05 | $-0.22 | 60 |
| 2025-07-07 15:07:46 | SELL | XOM | 1 | $111.52 | $1.53 | 70 |
| 2025-07-07 15:07:46 | SELL | NKE | 3 | $76.06 | $0.53 | 65 |

<!--TRADE_LOG_END--> 
