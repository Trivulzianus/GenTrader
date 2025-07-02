# AI Trading Agent

This project is an AI-powered day trading agent that uses OpenAI's GPT models to analyze market data and make trading decisions.

## Portfolio Status

<!--PORTFOLIO_STATUS_START-->
**Last Updated: 2025-07-02 12:13:14**

| Metric | Value |
|---|---|
| **Total Value** | **$101,079.66** |
| Cash | $101,079.66 |
| Holdings Value | $0.00 |

### Holdings
| Symbol | Shares | Avg Cost | Current Price | Current Value | Confidence |
|---|---|---|---|---|---|
| *No holdings* | - | - | - | - | - |

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
| 2025-07-01 22:16:21 | SELL | INTC | 82 | $22.85 | $51.01 | 0 |
| 2025-07-01 22:16:21 | SELL | AMZN | 11 | $220.46 | $-73.43 | 0 |
| 2025-07-01 22:16:21 | SELL | HD | 7 | $373.16 | $22.80 | 0 |
| 2025-07-01 22:16:21 | SELL | WMT | 25 | $98.24 | $29.13 | 0 |
| 2025-07-01 22:16:21 | SELL | C | 22 | $86.27 | $48.76 | 0 |
| 2025-07-01 22:16:21 | SELL | BA | 9 | $209.79 | $-49.58 | 0 |
| 2025-07-01 22:16:21 | SELL | UNP | 11 | $235.57 | $36.86 | 0 |
| 2025-07-01 22:16:21 | SELL | CAT | 5 | $390.92 | $48.60 | 0 |
| 2025-07-01 22:16:21 | SELL | CRM | 7 | $271.91 | $-24.13 | 0 |
| 2025-07-01 22:16:21 | SELL | WFC | 30 | $81.49 | $49.18 | 0 |
| 2025-07-01 22:16:21 | SELL | T | 84 | $28.88 | $29.96 | 0 |
| 2025-07-01 22:16:21 | SELL | TGT | 23 | $103.85 | $113.16 | 0 |
| 2025-07-01 22:16:21 | SELL | UNH | 8 | $326.14 | $156.09 | 0 |
| 2025-07-01 22:16:21 | SELL | PYPL | 32 | $75.29 | $45.79 | 0 |
| 2025-07-01 22:16:21 | SELL | V | 6 | $355.47 | $63.14 | 0 |
| 2025-07-01 22:16:21 | SELL | META | 3 | $719.22 | $19.54 | 0 |
| 2025-07-01 22:16:21 | SELL | NVDA | 16 | $153.30 | $-0.25 | 0 |
| 2025-07-01 22:16:21 | SELL | MSFT | 4 | $492.05 | $-3.37 | 0 |
| 2025-07-01 22:16:21 | SELL | JPM | 7 | $290.41 | $37.71 | 0 |
| 2025-07-01 22:16:21 | SELL | ADBE | 5 | $392.10 | $31.72 | 0 |
| 2025-07-01 22:16:21 | SELL | MA | 4 | $564.61 | $106.96 | 0 |
| 2025-07-01 22:16:21 | SELL | BAC | 50 | $48.15 | $43.54 | 0 |
| 2025-07-01 22:16:21 | SELL | XOM | 22 | $109.24 | $-2.85 | 0 |
| 2025-07-01 22:16:21 | SELL | DIS | 16 | $123.49 | $9.87 | 0 |
| 2025-07-01 22:16:21 | SELL | PFE | 97 | $25.04 | $72.72 | 0 |

<!--TRADE_LOG_END--> 
