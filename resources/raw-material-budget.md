# Resource Budget — Current Save

Delivered lines vs. what [`steel-base`](../production-plans/steel-base/) needs.

_Last updated: 2026-09-13_

## Delivered lines

Everything below already exists in-game and arrives on belts.

| Item | Lines | Total | Plan needs | Spare |
| --- | --- | --- | --- | --- |
| Iron Ingot | 480 + 450 + 450 | 1,380/min | 907.5/min | +472.5 |
| Iron Ore | 480 + 480 | 960/min | 802.5/min | +157.5 |
| Coal | 480 + 300 + 150 | 930/min | 802.5/min | +127.5 |
| Copper Ingot | 300 | 300/min | 268/min | +32 |
| Concrete | 150 | 150/min | 30/min | +120 |
| Plastic | — | 84/min | 84/min | exact |
| Rubber | — | 75/min | 75/min | exact |

**Every input the plan needs is covered.**

Iron ore and coal are dedicated to steel — the foundries are the only consumer
of either. Plastic and rubber come from the existing oil factory.

## What this means for the plan

The delivered lines span three tiers, so the remaining build is smaller than
the tier structure suggests:

| Work | Tier | Status |
| --- | --- | --- |
| Iron ore and coal extraction | 0 | Built |
| Iron and copper smelting | 1 | Built |
| Steel foundries | 1 | **To build** |
| Concrete | 2 | Built |
| All other constructor parts | 2 | **To build** |
| Assembled parts | 3 | **To build** |
| Final parts | 4 | **To build** |

## Surpluses

| Item | Spare | Notes |
| --- | --- | --- |
| Iron Ingot | 472.5/min | A full delivered line goes unused — see tier 2 feed plan |
| Iron Ore | 157.5/min | Only steel consumes it |
| Coal | 127.5/min | Only steel consumes it *in this plan* — see below |
| Concrete | 120/min | Worth routing to storage; concrete is the main hand-build material |
| Copper Ingot | 32/min | Tightest feed in the plan |

### Don't pre-spend the coal surplus

Steel is the only coal consumer in this plan, but four others exist in the game
and will compete for the spare 127.5/min later:

| Consumer | Note |
| --- | --- |
| Coal Generator | Not needed — power is already met |
| Aluminum Scrap | Alumina Solution + Coal in a Refinery; the standard aluminum path |
| Compacted Coal (alt) | Coal + Sulfur; gateway to Turbofuel |
| Black Powder | Coal + Sulfur; Nobelisks and explosives |

Aluminum is the most likely claimant. Check what the aluminum line needs before
committing the surplus to more steel. *(Per-minute rates unverified.)*

## Notes

- Iron ore for steel must stay iron **ore** — the standard Steel Ingot recipe
  takes ore, not ingots. The Solid Steel Ingot alt would take ingots instead,
  but total ingot demand would rise to 1,442.5/min against 1,380 delivered,
  leaving it 62.5/min short.
- TODO: record plastic/rubber capacity at the oil factory, to know whether the
  same headroom exists downstream.
