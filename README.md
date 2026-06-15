# Sykes Pennystock Radar

## Home Index
- [中文产品说明](./docs/product-introduction.zh.md)
- [English Product Intro](./docs/product-introduction.en.md)
- [Quick start](#quick-start)
- [Why this exists](#why-this-exists)
- [Case study](#case-study)

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

Most small-cap screens fail in one of two ways:

- they are too vague and give you no decision
- they are too mechanical and miss the actual trade context

This project sits in the middle.
It is designed to turn noisy penny-stock behavior into a simple operating rule:

> catalysts first, liquidity second, stage third, discipline always.

## Case study

The framework is meant to work on names like these:

- `ASTC` as a clean Supernova-style runner
- `PAVS` as a momentum extension with strong sell-into-strength logic
- `INHD` as a high-volatility breakout that needs fast execution
- `EDHL` as an example of a name that can move violently once volume and promotion line up
- `STI` as a squeeze-style setup where shorts become part of the thesis

These are not buy calls.
They are examples of the kind of tape Sykes-style screening is designed to catch.

## How it decides

The default output is built around five things:

1. Verdict
2. Lifecycle stage
3. PREPARE score
4. Entry / invalidation / exit
5. Positioning note

If a ticker does not have a catalyst, does not have enough liquidity, or is already too extended without fresh promotion, the answer should stay conservative.

## License

MIT
