# Raw Material Budget — Current Save

Secured supply vs. what [`steel-base`](../production-plans/steel-base/) needs.

_Last updated: 2026-09-13_

## Ores

| Resource | Secured | Needed | Delta |
| --- | --- | --- | --- |
| Iron Ore | 2,340/min | 1,710/min | +630 |
| Coal | 930/min | 802.5/min | +127.5 |
| Limestone | 150/min | 90/min | +60 |
| Copper Ore | 300/min | 268/min | +32 |

## Imported intermediates

Supplied by the existing oil factory — not built as part of this plan.

| Item | Needed | Status |
| --- | --- | --- |
| Plastic | 84/min | Supplied |
| Rubber | 75/min | Supplied |

Crude oil extraction, refining, and Heavy Oil Residue disposal are all handled
there. This plan treats plastic and rubber as belt inputs.

## Power

Met by existing infrastructure. Not a constraint on this plan.

## Every requirement is met

Nothing is blocked. Build in tier order:
[`00`](../production-plans/steel-base/00-raw-materials.md) →
[`01`](../production-plans/steel-base/01-smelting.md) →
[`02`](../production-plans/steel-base/02-basic-parts.md) →
[`03`](../production-plans/steel-base/03-assembled-parts.md) →
[`04`](../production-plans/steel-base/04-final-parts.md).

## Secured feeds

| Resource | Feeds | Total |
| --- | --- | --- |
| Iron Ore | 480 + 480 + 480 + 300 + 300 + 300 | 2,340/min |
| Coal | 480 + 240 + 150 + 60 | 930/min |
| Copper Ore | 300 | 300/min |
| Limestone | 150 | 150/min |

TODO: record node purity, miner tier, and clock per feed.

## Surpluses

| Resource | Spare | Notes |
| --- | --- | --- |
| Iron Ore | 630/min | Pairs with spare coal for more steel — see below |
| Coal | 127.5/min | Feeds only steel *in this plan* — see below |
| Limestone | 60/min | Feeds only concrete, which is fully allocated |
| Copper Ore | 32/min | Feeds only wire and copper sheet |

Steel Ingot takes 1 iron ore + 1 coal, so the iron and coal surpluses combine:
**127.5/min of additional steel is available** (coal-limited, with 502.5/min of
iron ore still spare beyond that). Real headroom if the plan is scaled past 100%.

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

TODO: record plastic/rubber capacity at the oil factory, to know whether the
same headroom exists downstream.
