---
name: stocks
description: Stock quotes, history, search, compare, crypto via Yahoo.
version: 0.1.0
author: Mibay (Mibayy), Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [Stocks, Finance, Market, Crypto, Investing]
    category: finance
    related_skills: [dcf-model, comps-analysis, lbo-model]
---

# Stocks Skill

Read-only market data via Yahoo Finance. Five commands: `quote`, `search`, `history`, `compare`, `crypto`. Python stdlib only — no API key, no pip installs. Yahoo's endpoint is unofficial and may rate-limit or change.

## When to Use

- User asks for a current stock price
- User wants to look up a ticker by company name
- User wants OHLCV history or performance over a date range
- User wants to compare several tickers side by side
- User asks for a crypto price

## Prerequisites

Python 3.8+ stdlib only. Optional: set `ALPHA_VANTAGE_KEY` to enrich market data. This skill is read-only and does not place orders or connect to brokerage accounts.

## Quick Reference

```text
quote SYMBOL [SYMBOL2 ...]
search QUERY
history SYMBOL --range 1mo|3mo|6mo|1y|5y
compare SYMBOL1 SYMBOL2 [...]
crypto SYMBOL
```

## Pitfalls

- Yahoo Finance's API is unofficial and may be delayed, rate-limited, or change.
- Treat all returned prices as time-stamped market data, not guaranteed real-time quotes.
- Verify ticker, exchange, currency, and data date before analysis.
- This skill provides data only; it does not by itself justify buy/sell conclusions.

## Installed Source

Adapted from: https://github.com/NousResearch/hermes-agent/tree/main/optional-skills/finance/stocks
Pinned source commit: 057dcdf236f8a6a26721c10fcc6ccb72726e272a
