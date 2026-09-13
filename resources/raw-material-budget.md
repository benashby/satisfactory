# Raw Material Budget — Current Save

Secured extraction vs. what [`steel-base`](../production-plans/steel-base/) needs.

_Last updated: 2026-09-13_

## Ledger

| Resource | Secured | Needed | Delta | Status |
| --- | --- | --- | --- | --- |
| Iron Ore | 2,340/min | 1,710/min | +630 | Surplus |
| Limestone | 150/min | 90/min | +60 | Surplus |
| Copper Ore | 300/min | 268/min | +32 | Surplus |
| Coal | 780/min | 802.5/min | **−22.5** | **Short** |
| Crude Oil | 0 m³/min | 238.5 m³/min | **−238.5** | **Not secured** |

## Secured feeds

| Resource | Feeds | Total |
| --- | --- | --- |
| Iron Ore | 480 + 480 + 480 + 300 + 300 + 300 | 2,340/min |
| Coal | 480 + 240 + 60 | 780/min |
| Copper Ore | 300 | 300/min |
| Limestone | 150 | 150/min |
| Crude Oil | — | 0 m³/min |

TODO: record node purity, miner tier, and clock per feed.

## Coal shortfall — 22.5/min

Coal feeds only steel, at 1 coal per 1 steel ingot, so 780/min caps steel at
780 against the plan's 802.5 — throttling the factory to 97.2%.

**Fix: one power shard on the 240/min coal miner → 262.5/min (109.4%).**

262.5 still sits under the Mk.3 belt cap of 270, so this needs no re-belting
anywhere. The other candidates are worse:

| Overclock | New rate | Clock | Belt |
| --- | --- | --- | --- |
| 240 feed | 262.5 | 109.4% | Mk.3 still fits (270) |
| 480 feed | 502.5 | 104.7% | Exceeds Mk.4 cap, needs Mk.5 |
| 60 feed | 82.5 | 137.5% | Fits, but a steep clock on a small miner |

The 480 feed is slightly cheaper on power — a gentler clock on the same miner —
but not enough to justify pulling a Mk.5 belt for it.

Alternative: skip the shard and run the plan at 97.2%. Less power, but every
output scales down with it (Adaptive Control Unit lands at 0.97/min).

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
2. Power-shard the 240 coal miner to 262.5/min, closing the 22.5/min gap.
3. Secure one pure oil node → unlocks Adaptive Control Unit and Modular Engine.
4. Decide what the 630/min iron surplus is for.
