# Raw Material Budget — Current Save

Secured extraction vs. what [`steel-base`](../production-plans/steel-base/) needs.

_Last updated: 2026-09-13_

## Ledger

| Resource | Secured | Needed | Delta | Status |
| --- | --- | --- | --- | --- |
| Iron Ore | 2,340/min | 1,710/min | +630 | Surplus |
| Limestone | 150/min | 90/min | +60 | Surplus |
| Copper Ore | 300/min | 268/min | +32 | Surplus |
| Coal | 720/min | 802.5/min | **−82.5** | **Short** |
| Crude Oil | 0 m³/min | 238.5 m³/min | **−238.5** | **Not secured** |

## Secured feeds

| Resource | Feeds | Total |
| --- | --- | --- |
| Iron Ore | 480 + 480 + 480 + 300 + 300 + 300 | 2,340/min |
| Coal | 480 + 240 | 720/min |
| Copper Ore | 300 | 300/min |
| Limestone | 150 | 150/min |
| Crude Oil | — | 0 m³/min |

TODO: record node purity, miner tier, and clock per feed.

## Coal shortfall — 82.5/min

Coal feeds only steel, at 1 coal per 1 steel ingot, so 720/min caps steel at
720 against the plan's 802.5 — which throttles the entire factory to 89.7%.

**Fix: one power shard on the 240/min coal miner → 322.5/min (134.4%).**

Put it on the 240 node, not the 480 node. 480/min is exactly the Mk.4 belt cap,
so overclocking that feed forces a Mk.5 re-belt; the 240 feed has headroom.

Alternative: underclock the whole plan to 89.7% and run within current coal.
Cheaper on power, but scales every output down proportionally.

## Crude oil — not secured

Blocks plastic and rubber, and therefore:

- Circuit Board → Computer → **Adaptive Control Unit** (plastic)
- **Modular Engine** (rubber, 75/min)

Two of the plan's three final outputs. The plan needs 238.5 m³/min, which is
0.99 of a pure node — a single pure Oil Extractor at 99.4% covers it exactly.
Securing one pure oil node unlocks both outputs at once.

## Iron surplus — 630/min

Cannot be converted to more steel; there is no spare coal to pair with it.
Options: hold as headroom for the next expansion, or route to a rod/screw/plate
stockpile for hand-building. Undecided.

## Buildable now: the Versatile Framework line

Versatile Framework needs no oil, no copper, and no limestone. Its full chain
fits inside current supply:

| Resource | Consumed | Of secured |
| --- | --- | --- |
| Iron Ore | 900/min | 2,340 |
| Coal | 600/min | 720 |

Chain to 25 VF/min:

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

1. Build the VF line — no new extraction needed.
2. Power-shard the 240 coal miner to close the 82.5/min gap.
3. Secure one pure oil node → unlocks Adaptive Control Unit and Modular Engine.
4. Decide what the 630/min iron surplus is for.
