# Sykes Pennystock Radar

## 1. What it is

Sykes Pennystock Radar is a practical due-diligence skill for penny stocks and volatile small caps.

Give it a ticker, watchlist, or a U.S. small-cap universe, and it will classify the hype-cycle stage, score the PREPARE filter, and return a rule-based verdict.

It is not a prediction engine.
It is a trading filter.

## 2. What it solves

Most small-cap screens are either too vague or too mechanical.

This project sits in the middle:

- it is not a fundamental valuation model
- it is not a blind momentum bot
- it is not a vibe-based hot stock list
- it is a tradeability filter

## 3. Why it matters

Timothy Sykes is not trying to find great companies.
He is trying to find great tape.

That means the real questions are:

- is there a catalyst
- is the float tight
- is volume expanding
- is the name getting promoted
- is the setup still tradable

If those conditions are not there, the story does not matter much.

## 4. Core framework

The system uses:

- the 7-step lifecycle
- the PREPARE filter
- stop conditions for weak setups

The two most useful places in the cycle are:

1. `Supernova` - highest upside, highest risk
2. `Dip Buy` - panic flush / rebound window

## 5. Output

For one ticker:

- verdict
- stage
- PREPARE score
- entry / invalidation / exit
- positioning note

For a scan:

- ranked candidates
- best stage for each
- ignore list
- A / B / C tiers if needed

## 6. Best fit

- U.S. penny stocks
- volatile small caps
- catalyst-driven runners
- panic-dip and sell-into-strength setups

## 7. Not for

- long-term investing
- fundamentals-first analysis
- no-catalyst names
- low-liquidity names you cannot exit cleanly

## 8. Simple mental model

Think of it like a trading gate:

- first check if the setup deserves attention
- then check whether the stage is right
- then decide whether to act

It does not promise easy money.
It helps you avoid obvious bad entries.
