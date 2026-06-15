# Sykes Pennystock Radar

## Home Index
- [中文产品说明](./docs/product-introduction.zh.md)
- [English Product Intro](./docs/product-introduction.en.md)
- [Quick start](#quick-start)

> Screen and score penny stocks or volatile small caps with the Timothy Sykes framework.

## Quick start

```bash
npm test
```

## What it does

This project turns the Timothy Sykes framework into a repeatable screen-and-score workflow.

For a single ticker, it classifies the hype-cycle stage and returns a Buyable / Watchlist only / Avoid verdict.
For a market universe, it ranks candidates using the same filter.

## Core output

- Verdict
- Lifecycle stage
- PREPARE score
- Entry / invalidation / exit
- Positioning note

## Scan mode

Use it to rank U.S. penny stocks or volatile small caps by:

1. catalyst freshness
2. float / supply tightness
3. abnormal volume
4. stage fit
5. risk / reward
6. liquidity

## Why this exists

The point is not prediction.
The point is to identify where a ticker sits in the hype cycle and react with discipline.

## License

MIT
