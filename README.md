# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-10 13:47:26**

| Metric | Value |
|---|---|
| **Total Value** | **$101,040.27** |
| Cash | $1,591.49 |
| Holdings Value | $99,448.78 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 11 | $211.08 | $210.93 | $2,320.23 | 70 |
| ADBE | 5 | $377.60 | $366.29 | $1,831.45 | 65 |
| AMD | 15 | $135.39 | $143.47 | $2,151.97 | 65 |
| AMZN | 11 | $221.90 | $221.04 | $2,431.44 | 75 |
| AVGO | 8 | $275.34 | $279.41 | $2,235.28 | 70 |
| AXP | 7 | $325.28 | $320.58 | $2,244.06 | 75 |
| BA | 9 | $210.97 | $227.59 | $2,048.32 | 65 |
| BAC | 50 | $48.57 | $46.98 | $2,348.75 | 75 |
| C | 26 | $86.83 | $86.20 | $2,241.20 | 70 |
| CAT | 6 | $397.86 | $406.96 | $2,441.76 | 75 |
| COST | 2 | $979.83 | $976.80 | $1,953.60 | 65 |
| CRM | 8 | $268.33 | $265.10 | $2,120.80 | 65 |
| CSCO | 34 | $68.38 | $69.30 | $2,356.20 | 75 |
| CVX | 15 | $146.28 | $151.90 | $2,278.50 | 75 |
| DIS | 18 | $122.80 | $121.20 | $2,181.60 | 70 |
| GOOGL | 12 | $179.86 | $175.43 | $2,105.16 | 65 |
| GS | 3 | $717.52 | $699.50 | $2,098.51 | 65 |
| HD | 6 | $372.64 | $371.70 | $2,230.20 | 65 |
| INTC | 86 | $22.31 | $23.82 | $2,048.53 | 65 |
| JNJ | 13 | $155.89 | $156.97 | $2,040.61 | 65 |
| JPM | 9 | $291.61 | $284.58 | $2,561.22 | 85 |
| KO | 29 | $71.03 | $69.33 | $2,010.71 | 65 |
| LLY | 2 | $776.66 | $788.28 | $1,576.57 | 65 |
| MA | 4 | $563.08 | $563.42 | $2,253.68 | 65 |
| META | 3 | $717.12 | $728.69 | $2,186.07 | 85 |
| MRK | 29 | $82.51 | $83.40 | $2,418.60 | 75 |
| MSFT | 5 | $498.84 | $501.63 | $2,508.18 | 75 |
| NFLX | 1 | $1,279.00 | $1,282.83 | $1,282.83 | 65 |
| NKE | 32 | $75.73 | $73.73 | $2,359.36 | 75 |
| NVDA | 16 | $157.35 | $163.82 | $2,621.12 | 85 |
| ORCL | 9 | $233.31 | $238.34 | $2,145.06 | 70 |
| PEP | 15 | $136.57 | $134.50 | $2,017.50 | 65 |
| PFE | 86 | $25.21 | $25.70 | $2,210.05 | 70 |
| PG | 13 | $160.75 | $157.42 | $2,046.46 | 65 |
| PYPL | 30 | $76.69 | $74.66 | $2,239.80 | 70 |
| QCOM | 13 | $162.06 | $158.73 | $2,063.49 | 70 |
| T | 73 | $28.55 | $27.73 | $2,024.65 | 65 |
| TGT | 20 | $104.89 | $102.90 | $2,058.00 | 65 |
| TSLA | 6 | $288.62 | $305.80 | $1,834.77 | 60 |
| UNH | 6 | $298.34 | $298.58 | $1,791.49 | 65 |
| UNP | 10 | $236.59 | $237.06 | $2,370.60 | 70 |
| V | 6 | $355.85 | $356.56 | $2,139.36 | 65 |
| VZ | 48 | $43.15 | $41.97 | $2,014.32 | 65 |
| WFC | 29 | $82.30 | $81.85 | $2,373.65 | 75 |
| WMT | 21 | $97.35 | $96.29 | $2,022.09 | 65 |
| XOM | 23 | $110.31 | $113.52 | $2,610.96 | 85 |

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
| 2025-07-10 13:47:19 | SELL | GOOGL | 1 | $175.33 | $-4.18 | 65 |
| 2025-07-10 13:47:19 | SELL | MRK | 2 | $83.42 | $1.68 | 75 |
| 2025-07-10 13:47:19 | SELL | PYPL | 1 | $74.64 | $-1.98 | 70 |
| 2025-07-10 13:47:19 | SELL | PFE | 5 | $25.68 | $2.24 | 70 |
| 2025-07-10 13:47:19 | BUY | NVDA | 2 | $163.90 | N/A | 85 |
| 2025-07-10 13:47:19 | BUY | UNH | 6 | $298.34 | N/A | 65 |
| 2025-07-10 13:47:19 | BUY | XOM | 3 | $113.46 | N/A | 85 |
| 2025-07-10 13:47:19 | BUY | NKE | 1 | $73.76 | N/A | 75 |
| 2025-07-10 13:47:19 | BUY | T | 1 | $27.73 | N/A | 65 |
| 2025-07-10 13:46:52 | SELL | UNH | 7 | $298.55 | $-113.40 | 65 |
| 2025-07-10 13:03:45 | SELL | NVDA | 2 | $162.88 | $11.32 | 70 |
| 2025-07-10 13:03:45 | SELL | C | 1 | $85.79 | $-1.00 | 70 |
| 2025-07-10 13:03:45 | BUY | BAC | 3 | $46.84 | N/A | 75 |
| 2025-07-10 13:03:45 | BUY | INTC | 1 | $23.44 | N/A | 65 |
| 2025-07-10 13:03:45 | BUY | PFE | 1 | $25.56 | N/A | 75 |
| 2025-07-10 12:32:03 | SELL | BAC | 2 | $46.84 | $-3.54 | 70 |
| 2025-07-10 12:32:03 | SELL | T | 5 | $28.10 | $-2.13 | 65 |
| 2025-07-10 12:32:03 | BUY | PFE | 5 | $25.56 | N/A | 75 |
| 2025-07-10 12:13:46 | SELL | PFE | 6 | $25.56 | $1.94 | 70 |
| 2025-07-10 12:13:46 | SELL | VZ | 2 | $42.61 | $-1.03 | 65 |
| 2025-07-10 12:13:46 | BUY | INTC | 5 | $23.44 | N/A | 65 |
| 2025-07-10 12:13:46 | BUY | MRK | 3 | $83.71 | N/A | 85 |
| 2025-07-10 12:13:46 | BUY | T | 5 | $28.10 | N/A | 70 |
| 2025-07-10 11:50:29 | SELL | INTC | 6 | $23.44 | $6.79 | 60 |
| 2025-07-10 11:50:29 | SELL | MRK | 3 | $83.71 | $3.41 | 75 |

<!--TRADE_LOG_END--> 
