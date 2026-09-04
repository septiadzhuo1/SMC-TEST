# SMC Chart

A zero-dependency, single-file TradingView-style crypto chart with a **Smart Money Concept** strategy engine — live data, backtesting, and an adjustable risk model. No build step, no framework: open `index.html` in a browser.

Strategy logic is based on the eBook *"Smart Money Concept"* by **De Gus Trader**.

## Features

- **Live data** — streams candles + ticker over WebSocket from Binance's public market-data host (`data-stream.binance.vision`), with automatic fallback to REST polling.
- **Multi-coin / multi-timeframe** — 22 popular pairs plus free-text search for any USDT pair; timeframes 1m → 1w.
- **Chart** — candles or line, volume, MA25/MA99, crosshair with OHLC legend, price/time axis, pan / wheel-zoom / drag-to-scale, right-scroll margin, dark/light theme.
- **SMC engine** (toggle):
  - **Structure** — swing pivots → BOS (continuation) and MSS (reversal).
  - **Order Blocks** — last opposite candle before a structure-breaking impulse, validated by a following imbalance.
  - **Imbalance (FVG)** — 3-candle gaps, drawn until filled.
  - **Liquidity** — unswept swing highs (BSL) / lows (SSL).
  - **Live setup** — Entry / SL / TP with risk–reward shading and a HUD.
- **Two entry models** — Order Block, and Fibonacci OTE (entry 71.5%, SL 100%).
- **Adjustable Risk:Reward** — target = RR × stop distance, live across setup, on-chart trades, and the report.
- **Backtest** — walk-forward the strategy since 2020-01-01: win rate, expectancy (R), profit factor, equity curve, per-year breakdown, and on-chart trade markers.

## Usage

Just open `index.html` in any modern browser — it needs an internet connection for live prices. No server or install required.

## Disclaimer

For research and education only. Backtests repaint (structure confirms a few bars late) and assume no fees/slippage. Nothing here is financial advice.
