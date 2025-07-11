# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-11 15:26:31**

| Metric | Value |
|---|---|
| **Total Value** | **$100,644.18** |
| Cash | $1,559.40 |
| Holdings Value | $99,084.77 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 10 | $211.29 | $210.89 | $2,108.90 | 70 |
| ADBE | 5 | $377.60 | $367.19 | $1,835.97 | 65 |
| AMD | 17 | $136.25 | $144.71 | $2,460.07 | 75 |
| AMZN | 11 | $221.97 | $224.27 | $2,466.97 | 75 |
| AVGO | 8 | $275.34 | $274.34 | $2,194.72 | 70 |
| AXP | 7 | $325.34 | $322.33 | $2,256.31 | 75 |
| BA | 9 | $210.85 | $228.12 | $2,053.08 | 65 |
| BAC | 44 | $48.85 | $46.45 | $2,044.02 | 65 |
| C | 25 | $86.68 | $86.34 | $2,158.62 | 70 |
| CAT | 6 | $397.86 | $404.85 | $2,429.07 | 70 |
| COST | 2 | $979.83 | $968.01 | $1,936.02 | 65 |
| CRM | 7 | $268.68 | $259.27 | $1,814.92 | 65 |
| CSCO | 32 | $68.37 | $68.12 | $2,180.00 | 70 |
| CVX | 17 | $147.16 | $155.10 | $2,636.70 | 85 |
| DIS | 17 | $122.96 | $120.16 | $2,042.77 | 65 |
| GOOGL | 13 | $179.61 | $178.71 | $2,323.25 | 75 |
| GS | 3 | $717.52 | $703.91 | $2,111.74 | 70 |
| HD | 6 | $372.64 | $368.30 | $2,209.77 | 70 |
| INTC | 81 | $22.28 | $23.30 | $1,887.70 | 60 |
| JNJ | 13 | $155.89 | $155.46 | $2,020.98 | 65 |
| JPM | 9 | $291.61 | $286.44 | $2,577.96 | 75 |
| KO | 28 | $71.07 | $69.86 | $1,956.08 | 60 |
| LLY | 3 | $781.32 | $780.18 | $2,340.54 | 70 |
| MA | 4 | $563.08 | $551.97 | $2,207.87 | 65 |
| META | 3 | $717.12 | $716.18 | $2,148.54 | 85 |
| MRK | 25 | $82.30 | $82.35 | $2,058.75 | 65 |
| MSFT | 5 | $498.84 | $502.20 | $2,511.00 | 85 |
| NFLX | 1 | $1,279.00 | $1,239.54 | $1,239.54 | 65 |
| NKE | 30 | $75.88 | $72.72 | $2,181.60 | 70 |
| NVDA | 16 | $157.38 | $166.54 | $2,664.72 | 85 |
| ORCL | 9 | $233.26 | $232.75 | $2,094.75 | 70 |
| PEP | 15 | $136.57 | $134.33 | $2,014.95 | 65 |
| PFE | 81 | $25.18 | $25.48 | $2,064.28 | 65 |
| PG | 14 | $160.52 | $156.78 | $2,194.92 | 65 |
| PYPL | 29 | $76.76 | $74.56 | $2,162.24 | 70 |
| QCOM | 13 | $162.18 | $157.53 | $2,047.95 | 65 |
| T | 76 | $27.10 | $26.83 | $2,039.08 | 65 |
| TGT | 20 | $104.92 | $104.41 | $2,088.25 | 65 |
| TSLA | 6 | $288.62 | $307.62 | $1,845.72 | 65 |
| UNH | 7 | $298.51 | $299.56 | $2,096.90 | 65 |
| UNP | 10 | $236.18 | $234.94 | $2,349.35 | 75 |
| V | 6 | $355.85 | $348.51 | $2,091.06 | 70 |
| VZ | 49 | $43.12 | $41.59 | $2,038.15 | 65 |
| WFC | 29 | $82.28 | $82.33 | $2,387.57 | 75 |
| WMT | 22 | $97.25 | $94.98 | $2,089.56 | 65 |
| XOM | 21 | $109.92 | $115.33 | $2,421.83 | 75 |

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
| 2025-07-11 15:26:26 | SELL | AMD | 1 | $144.69 | $7.97 | 75 |
| 2025-07-11 15:26:26 | SELL | INTC | 6 | $23.31 | $5.73 | 60 |
| 2025-07-11 15:26:26 | SELL | KO | 1 | $69.85 | $-1.19 | 60 |
| 2025-07-11 15:26:26 | SELL | XOM | 2 | $115.29 | $9.81 | 75 |
| 2025-07-11 15:26:26 | SELL | MRK | 1 | $82.43 | $0.13 | 65 |
| 2025-07-11 15:26:26 | BUY | PYPL | 1 | $74.56 | N/A | 70 |
| 2025-07-11 15:26:26 | BUY | NKE | 1 | $72.74 | N/A | 70 |
| 2025-07-11 15:26:26 | BUY | C | 1 | $86.32 | N/A | 70 |
| 2025-07-11 15:08:26 | SELL | BAC | 3 | $46.47 | $-6.67 | 65 |
| 2025-07-11 15:08:26 | SELL | DIS | 1 | $120.31 | $-2.50 | 65 |
| 2025-07-11 15:08:26 | SELL | PFE | 6 | $25.45 | $1.54 | 65 |
| 2025-07-11 15:08:26 | SELL | PYPL | 3 | $74.53 | $-6.25 | 65 |
| 2025-07-11 15:08:26 | SELL | NKE | 2 | $72.54 | $-6.44 | 65 |
| 2025-07-11 15:08:26 | SELL | C | 1 | $86.31 | $-0.37 | 65 |
| 2025-07-11 15:08:26 | BUY | AMD | 2 | $144.16 | N/A | 85 |
| 2025-07-11 15:08:26 | BUY | INTC | 5 | $23.33 | N/A | 65 |
| 2025-07-11 15:08:26 | BUY | XOM | 2 | $115.38 | N/A | 85 |
| 2025-07-11 15:08:26 | BUY | MRK | 1 | $82.32 | N/A | 70 |
| 2025-07-11 15:08:26 | BUY | CSCO | 1 | $68.23 | N/A | 70 |
| 2025-07-11 15:08:26 | BUY | VZ | 3 | $41.64 | N/A | 65 |
| 2025-07-11 14:52:03 | SELL | INTC | 6 | $23.35 | $5.94 | 60 |
| 2025-07-11 14:52:03 | SELL | XOM | 2 | $115.08 | $9.45 | 75 |
| 2025-07-11 14:52:03 | SELL | NKE | 1 | $72.81 | $-2.86 | 70 |
| 2025-07-11 14:52:03 | SELL | CSCO | 3 | $68.11 | $-0.75 | 65 |
| 2025-07-11 14:52:03 | SELL | VZ | 3 | $41.62 | $-4.48 | 60 |

<!--TRADE_LOG_END--> 
