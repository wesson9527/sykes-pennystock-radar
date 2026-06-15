---
name: sykes-pennystock-radar
description: Screen and score penny stocks or volatile small caps using the Timothy Sykes framework. Use when the user asks whether a ticker is buyable, wants a stage-based hype-cycle read, asks for a U.S. small-cap scan, or wants a rule-based momentum/dip-buy verdict with entry, invalidation, and position sizing guidance.
---

# Sykes Pennystock Radar

## Overview

Turn the Timothy Sykes framework into a repeatable screen-and-score workflow. For a single ticker, classify its hype-cycle stage and return a buy / watch / avoid verdict. For a market universe, rank candidates with the same filter.

## Use When

- The user gives a ticker and wants a practical tradeability read.
- The user asks for a U.S. penny stock / small-cap scan.
- The user wants a stage-based read on catalyst, float, volume, liquidity, squeeze potential, or dip-buy setup.
- The user wants momentum / panic-dip / sell-into-strength logic rather than fundamental valuation.

## Core Lens

Treat Sykes as a pattern-recognition filter, not a prediction oracle.

Primary beliefs:
- Identify the current stage of the hype cycle.
- Trade catalysts, not stories.
- Favor low float, abnormal volume, and clear liquidity.
- Cut losses quickly.
- Sell into strength.

## Decision Gate

Use this skill only for tradeability, not long-term investing.

Hard fail / downgrade conditions:
- no clear catalyst
- unknown or unusable float
- volume too low to enter and exit cleanly
- setup already too extended without fresh promotion
- poor risk / reward
- user is asking for a fundamental thesis instead of a trading setup

If any hard fail condition is present, return **Avoid** or **Watchlist only** rather than forcing a buy call.

## Workflow

### 1) Classify the setup
First decide whether the ticker is even worth studying.

Check:
- float / share structure
- volume and volatility
- catalyst quality
- social or news promotion intensity
- whether it already looks extended

If the user did not provide enough data to judge float, volume, or catalyst, ask for the minimum missing inputs before forcing a verdict.

### 2) Map to the 7-step lifecycle
Classify the ticker into one of these phases:

1. **Pre-Pump** - early accumulation, early promotion, hard to spot
2. **Ramp** - volume expansion, breakout attempts, momentum building
3. **Supernova** - explosive extension, highest upside and highest risk
4. **Cliff Dive** - abrupt collapse after hype peak
5. **Dip Buy** - panic flush / rebound window
6. **Dead Pump Bounce** - small final bounce, limited edge
7. **Long Kiss Goodnight** - slow death, weak residual action

### 3) Score the PREPARE filter
Use these seven checks:

- **P**: Pattern / Price
- **R**: Reason
- **E**: Ease of Entry / Exit
- **P**: Past Performance
- **A**: Agenda / timing window
- **R**: Risk / Reward
- **E**: Environment

Score each item as strong / medium / weak and translate them into:
- strong = 2
- medium = 1
- weak = 0

Interpretation:
- **10-14**: tradable / high attention
- **6-9**: watchlist / conditional
- **0-5**: avoid

If one of the following is weak, the setup should usually fail:
- catalyst / reason
- liquidity / ease of entry-exit
- risk-reward

### 4) Decide the trade
Return one of:
- **Buyable**
- **Watchlist only**
- **Avoid**

Include:
- likely lifecycle stage
- catalyst thesis
- key risk
- invalidation level
- preferred entry style
- rough position sizing posture
Use plain language and say whether the setup is a momentum chase, dip buy, or no-trade.

Rules for buyability:
- **Buyable**: strong catalyst, workable liquidity, acceptable stage fit, and at least a decent PREPARE score
- **Watchlist only**: interesting setup, but one major input is still missing or the edge is not clean yet
- **Avoid**: no catalyst, dead liquidity, overextended late stage, or weak risk / reward

## Single-Ticker Protocol

When the user gives one ticker:
1. identify the stage
2. score PREPARE
3. decide Buyable / Watchlist only / Avoid
4. give the entry, invalidation, and exit posture
5. state the one thing that would change the verdict

If the setup is ambiguous, stay conservative.

## Screening Rules

When the user asks for a U.S. stock scan, prioritize names that show:

- low float / tight supply
- abnormal volume
- fresh catalyst or promotion
- prior runner behavior
- strong intraday or multi-day extension potential

Rank names by this order:
1. catalyst freshness
2. float / supply tightness
3. volume expansion
4. stage fit
5. risk-reward quality
6. liquidity

Deprioritize names that are:

- too large / too slow
- too illiquid
- already in long-death mode
- missing a real catalyst
- obvious bag-holder traps
- overextended without a fresh catalyst
- too low volume to enter/exit cleanly

If the user gives a watchlist, score each ticker and return the top 3 most tradeable names first.

## Standard Input Template

When possible, ask for or infer these fields:
- ticker / name
- market cap
- float
- avg daily volume
- today / recent volume
- catalyst or news
- recent price action
- social or promotion intensity
- short interest if available
- time horizon

If several fields are missing, ask for the minimum needed to judge tradeability: float, catalyst, and volume.

## Scan Template

For a U.S. scan, rank candidates with this pass order:
1. fresh catalyst
2. low float / supply tightness
3. abnormal volume
4. stage fit
5. risk / reward
6. liquidity

Then separate names into:
- **A tier**: strongest tradable setups
- **B tier**: watchlist / conditional
- **C tier**: ignore

Only include names that have a plausible entry and invalidation.
If the user wants an auto-scan, return the ranked list plus a one-line reason for each candidate.

## Output Format

For a single ticker:
1. Verdict
2. Lifecycle stage
3. PREPARE score
4. Entry / invalidation / exit
5. Positioning note

For a scan:
1. Ranked candidates
2. Why each fits the framework
3. Best stage for each
4. Which names to ignore
5. The one name to study first if the user only wants one
6. Tier labels (A / B / C) if the user asks for a larger universe

Keep the answer tight. Prefer concrete inputs, thresholds, and action over background explanation.

## Hard Rules

- Do not present this as guaranteed profit.
- Do not call a setup buyable if catalyst, liquidity, or risk/reward is weak.
- Do not ignore lifecycle stage.
- Do not give a target without invalidation.
- Do not confuse this with fundamental investing.
- Do not force a verdict when the setup lacks enough data; ask for float / catalyst / volume / market cap if needed.

## Default Response Shape

Use this exact order when possible:

1. Verdict
2. Stage
3. PREPARE score
4. Entry / invalidation / exit
5. Scan ranking or watchlist note

## Reference

- See `references/sykes-framework.md` for the condensed lifecycle map, PREPARE checks, and screening heuristics.
