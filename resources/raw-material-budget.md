# Raw Material Budget — Current Save

Secured extraction vs. what [`steel-base`](../production-plans/steel-base/) needs.

_Last updated: 2026-09-13_

## Ledger

| Resource | Secured | Needed | Delta | Status |
| --- | --- | --- | --- | --- |
| Iron Ore | 2,340/min | 1,710/min | +630 | Surplus |
| Coal | 930/min | 802.5/min | +127.5 | Surplus |
| Limestone | 150/min | 90/min | +60 | Surplus |
| Copper Ore | 300/min | 268/min | +32 | Surplus |
| Crude Oil | 0 m³/min | 238.5 m³/min | **−238.5** | **Not secured** |

**Crude oil is the only remaining gap.** Every ore feed now covers the plan.

## Secured feeds

| Resource | Feeds | Total |
| --- | --- | --- |
| Iron Ore | 480 + 480 + 480 + 300 + 300 + 300 | 2,340/min |
| Coal | 480 + 240 + 150 + 60 | 930/min |
| Copper Ore | 300 | 300/min |
| Limestone | 150 | 150/min |
| Crude Oil | — | 0 m³/min |

TODO: record node purity, miner tier, and clock per feed.

## Crude oil — not secured

Blocks plastic and rubber, and therefore:

- Circuit Board → Computer → **Adaptive Control Unit** (plastic)
- **Modular Engine** (rubber, 75/min)

Two of the plan's three final outputs. The plan needs 238.5 m³/min, which is
0.99 of a pure node — a single pure Oil Extractor at 99.4% covers it exactly,
on one Mk.1 pipe. Two normal nodes also work, same clock each.

Securing one pure oil node completes the plan.

## Surpluses

| Resource | Spare | Notes |
| --- | --- | --- |
| Iron Ore | 630/min | Pairs with spare coal for more steel — see below |
| Coal | 127.5/min | Feeds only steel |
| Limestone | 60/min | Feeds only concrete, which is fully allocated |
| Copper Ore | 32/min | Feeds only wire and copper sheet |

Steel Ingot takes 1 iron ore + 1 coal, so the iron and coal surpluses combine:
**127.5/min of additional steel is available** (coal-limited, with 502.5/min of
iron ore still spare beyond that). That is real expansion headroom if the plan
is ever scaled past 100%.

None of these substitute for crude oil.

## Buildable now: the Versatile Framework line

Versatile Framework needs no oil, no copper, and no limestone. Its full chain
fits inside current supply:

| Resource | Consumed | Of secured |
| --- | --- | --- |
| Iron Ore | 900/min | 2,340 |
| Coal | 600/min | 930 |

Chain to 25 Versatile Framework/min:

| Step | Rate |
| --- | --- |
| Steel Ingot | 600/min |
| Steel Beam | 150/min |
| Iron Ingot | 300/min |
| Iron Rod | 131.25/min (75 to frames, 56.25 to screws) |
| Screws | 225/min |
| Iron Plate | 112.5/min |
| Reinforced Iron Plate | 18.75/min |
| Modular Frame | 12.5/min |
| **Versatile Framework** | **25/min** |

That is 25 of the plan's 31 total output units/min, with no new nodes required.

## Suggested order

1. Build the Versatile Framework line — no new extraction needed.
2. Secure one pure oil node → unlocks Adaptive Control Unit and Modular Engine,
   and completes the plan.
3. Decide what the surpluses are for.
