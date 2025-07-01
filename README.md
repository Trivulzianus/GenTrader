# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-01 14:55:26**

| Metric | Value |
|---|---|
| **Total Value** | **$100,638.20** |
| Cash | $158.19 |
| Holdings Value | $100,480.02 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| AAPL | 12 | $201.29 | $208.40 | $2,500.80 | 85 |
| ADBE | 5 | $385.76 | $389.19 | $1,945.92 | 65 |
| AMD | 18 | $141.35 | $136.49 | $2,456.82 | 85 |
| AMZN | 11 | $226.80 | $219.30 | $2,412.30 | 85 |
| AVGO | 9 | $275.08 | $266.77 | $2,400.93 | 85 |
| AXP | 6 | $315.94 | $318.67 | $1,912.02 | 65 |
| BA | 10 | $214.55 | $208.03 | $2,080.30 | 65 |
| BAC | 40 | $47.18 | $47.53 | $1,901.34 | 65 |
| C | 23 | $84.14 | $84.92 | $1,953.05 | 65 |
| CAT | 5 | $381.20 | $387.88 | $1,939.38 | 65 |
| COST | 2 | $991.47 | $991.48 | $1,982.96 | 65 |
| CRM | 9 | $274.67 | $272.89 | $2,456.01 | 85 |
| CSCO | 32 | $68.91 | $68.99 | $2,207.68 | 75 |
| CVX | 13 | $143.34 | $144.44 | $1,877.72 | 85 |
| DIS | 16 | $122.90 | $122.93 | $1,966.88 | 65 |
| GOOGL | 14 | $175.62 | $174.92 | $2,448.88 | 85 |
| GS | 3 | $706.65 | $704.37 | $2,113.11 | 65 |
| HD | 7 | $369.90 | $373.45 | $2,614.15 | 85 |
| INTC | 84 | $22.33 | $22.61 | $1,899.66 | 65 |
| JNJ | 12 | $151.53 | $156.33 | $1,875.96 | 65 |
| JPM | 7 | $285.02 | $288.22 | $2,017.54 | 65 |
| KO | 27 | $70.44 | $71.97 | $1,943.32 | 65 |
| LLY | 3 | $767.33 | $784.36 | $2,353.08 | 65 |
| MA | 4 | $537.87 | $562.97 | $2,251.88 | 65 |
| META | 3 | $712.71 | $725.88 | $2,177.62 | 85 |
| MRK | 30 | $79.35 | $81.00 | $2,430.00 | 85 |
| MSFT | 4 | $492.89 | $496.54 | $1,986.16 | 65 |
| NFLX | 1 | $1,334.07 | $1,310.21 | $1,310.21 | 85 |
| NKE | 33 | $71.01 | $73.54 | $2,426.82 | 85 |
| NVDA | 16 | $156.03 | $152.99 | $2,447.81 | 85 |
| ORCL | 9 | $219.56 | $218.44 | $1,965.96 | 65 |
| PEP | 17 | $131.85 | $134.90 | $2,293.30 | 75 |
| PFE | 89 | $24.24 | $24.82 | $2,208.54 | 75 |
| PG | 12 | $159.73 | $161.13 | $1,933.56 | 65 |
| PYPL | 33 | $73.91 | $74.59 | $2,461.47 | 85 |
| QCOM | 16 | $159.24 | $158.91 | $2,542.56 | 85 |
| T | 85 | $28.52 | $28.98 | $2,462.88 | 85 |
| TGT | 21 | $98.42 | $103.27 | $2,168.67 | 75 |
| TSLA | 6 | $290.36 | $298.62 | $1,791.72 | 65 |
| UNH | 8 | $306.63 | $322.08 | $2,576.64 | 85 |
| UNP | 11 | $232.22 | $233.60 | $2,569.60 | 85 |
| V | 6 | $344.95 | $354.04 | $2,124.24 | 65 |
| VZ | 50 | $42.73 | $43.56 | $2,178.25 | 75 |
| WFC | 31 | $79.89 | $80.39 | $2,492.24 | 85 |
| WMT | 25 | $97.07 | $99.05 | $2,476.25 | 85 |
| XOM | 18 | $109.40 | $107.99 | $1,943.82 | 65 |

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
| 2025-07-01 14:55:20 | SELL | TSLA | 1 | $317.66 | $23.40 | 65 |
| 2025-07-01 14:55:20 | SELL | PFE | 10 | $24.80 | $4.99 | 75 |
| 2025-07-01 14:55:20 | SELL | CSCO | 4 | $68.99 | $0.27 | 75 |
| 2025-07-01 14:55:20 | BUY | NVDA | 1 | $152.99 | N/A | 85 |
| 2025-07-01 14:55:20 | BUY | INTC | 1 | $22.64 | N/A | 65 |
| 2025-07-01 14:55:20 | BUY | AMD | 2 | $136.55 | N/A | 85 |
| 2025-07-01 14:55:20 | BUY | T | 9 | $28.98 | N/A | 85 |
| 2025-07-01 14:48:45 | SELL | JNJ | 1 | $156.44 | $4.53 | 65 |
| 2025-07-01 14:48:45 | SELL | INTC | 2 | $22.64 | $0.60 | 65 |
| 2025-07-01 14:48:45 | SELL | PYPL | 1 | $74.48 | $0.56 | 85 |
| 2025-07-01 14:48:45 | SELL | WMT | 1 | $99.08 | $1.93 | 85 |
| 2025-07-01 14:48:45 | SELL | PFE | 1 | $24.85 | $0.55 | 85 |
| 2025-07-01 14:48:45 | SELL | CSCO | 1 | $68.95 | $0.03 | 85 |
| 2025-07-01 14:48:45 | SELL | TGT | 1 | $103.21 | $4.57 | 75 |
| 2025-07-01 14:48:45 | BUY | NVDA | 2 | $153.41 | N/A | 85 |
| 2025-07-01 14:48:45 | BUY | MRK | 5 | $81.01 | N/A | 85 |
| 2025-07-01 14:40:14 | SELL | NVDA | 3 | $157.99 | $3.24 | 65 |
| 2025-07-01 14:40:14 | SELL | JNJ | 1 | $156.26 | $4.04 | 65 |
| 2025-07-01 14:40:14 | SELL | BAC | 1 | $47.57 | $0.37 | 65 |
| 2025-07-01 14:40:14 | SELL | INTC | 3 | $22.52 | $0.55 | 65 |
| 2025-07-01 14:40:14 | SELL | AXP | 1 | $318.68 | $2.35 | 65 |
| 2025-07-01 14:40:14 | SELL | WFC | 1 | $80.59 | $0.68 | 85 |
| 2025-07-01 14:40:14 | SELL | TGT | 1 | $102.93 | $4.11 | 75 |
| 2025-07-01 14:40:14 | SELL | T | 12 | $28.99 | $5.35 | 75 |
| 2025-07-01 14:40:14 | BUY | AMZN | 2 | $219.61 | N/A | 85 |

<!--TRADE_LOG_END--> 
