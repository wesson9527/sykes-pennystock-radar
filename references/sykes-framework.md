# Sykes Framework Reference

## 1. Core Belief

Sykes treats penny stocks as hype-cycle systems, not valuation systems. The goal is to identify where a name sits in the cycle and react with discipline.

## 2. 7-Step Lifecycle

1. **Pre-Pump** - early accumulation or promotion
2. **Ramp** - volume builds, breakout attempts begin
3. **Supernova** - explosive move, highest opportunity and risk
4. **Cliff Dive** - hype collapses
5. **Dip Buy** - panic flush and rebound window
6. **Dead Pump Bounce** - weak final bounce
7. **Long Kiss Goodnight** - slow decline, low edge

## 3. PREPARE Filter

- **P** Pattern / Price
- **R** Reason
- **E** Ease of Entry / Exit
- **P** Past Performance
- **A** Agenda / timing window
- **R** Risk / Reward
- **E** Environment

Translate each into strong / medium / weak and treat the total as a tradeability filter.

Suggested scoring:
- strong = 2
- medium = 1
- weak = 0

Interpretation:
- 10-14: tradable / high attention
- 6-9: watchlist / conditional
- 0-5: avoid

## 4. Screening Heuristics

Good signs:
- low float
- abnormal volume
- fresh catalyst
- promotion or social buzz
- prior runner behavior
- clear liquidity

Bad signs:
- no catalyst
- too large / too slow
- weak liquidity
- overextended late-stage move
- obvious bag-holder supply

## 5. Output Logic

Return:
- verdict
- lifecycle stage
- PREPARE score
- entry
- invalidation
- exit posture
- scan ranking if multiple names are provided

## 6. Stop Conditions

Skip or downgrade the setup if:
- no clear catalyst exists
- float is unknown and cannot be inferred
- volume is too low to enter/exit cleanly
- the name is already too extended without fresh promotion
- the user is asking for a long-term fundamental thesis instead of a trading setup

## 7. Ranking Rules

For scans, rank by:
1. catalyst freshness
2. float / supply tightness
3. abnormal volume
4. stage fit
5. risk / reward
6. liquidity

Group names into:
- A: best tradable setups
- B: watchlist only
- C: ignore
