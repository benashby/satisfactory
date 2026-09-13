# Steel Base — Overview

The generic all-purpose steel factory. Everything else builds from this.

**Final outputs**

| Item | Rate |
| --- | --- |
| Versatile Framework | 25/min |
| Modular Engine | 5/min |
| Adaptive Control Unit | 1/min |

Every other item on this page is an intermediate consumed inside the plan.

## Key facts

- **All standard recipes. No alternates.** Verified: every listed rate reconciles
  exactly against the standard recipe ratios, with zero slack anywhere.
- **Because there is zero slack, any alternate recipe you swap in invalidates
  this entire sheet.** Re-solve from scratch rather than patching one tier.
- **Heavy Oil Residue (117 m³/min) is a byproduct, not an input.** Nothing in
  this plan consumes it. It must be given a destination or the refineries back
  up and the whole plastic branch stalls. See [`01-smelting.md`](01-smelting.md).

## Tiers

| File | Contents |
| --- | --- |
| [`00-raw-materials.md`](00-raw-materials.md) | Iron ore, coal, copper ore, limestone, crude oil |
| [`01-smelting.md`](01-smelting.md) | Iron/steel/copper ingots, plastic, rubber, HOR disposal |
| [`02-basic-parts.md`](02-basic-parts.md) | Rods, screws, plates, wire, cable, sheets, beams, pipes, concrete |
| [`03-assembled-parts.md`](03-assembled-parts.md) | Reinforced plates, rotors, stators, circuit boards, motors, frames |
| [`04-final-parts.md`](04-final-parts.md) | Computers, heavy modular frames, and the three final outputs |

## Full requirements

<details>
<summary>All items, per minute</summary>

| Item | Rate | Tier |
| --- | --- | --- |
| Iron Ore | 1,710 | 0 |
| Coal | 802.5 | 0 |
| Copper Ore | 268 | 0 |
| Crude Oil | 238.5 m³ | 0 |
| Limestone | 90 | 0 |
| Iron Ingot | 907.5 | 1 |
| Steel Ingot | 802.5 | 1 |
| Copper Ingot | 268 | 1 |
| Plastic | 84 | 1 |
| Rubber | 75 | 1 |
| Heavy Oil Residue | 117 m³ | 1 (byproduct) |
| Screws | 1,305 | 2 |
| Iron Rod | 581.25 | 2 |
| Wire | 432 | 2 |
| Iron Plate | 217.5 | 2 |
| Steel Beam | 165 | 2 |
| Cable | 116 | 2 |
| Steel Pipe | 95 | 2 |
| Copper Sheet | 26 | 2 |
| Concrete | 30 | 2 |
| Reinforced Iron Plate | 36.25 | 3 |
| Rotor | 30 | 3 |
| Stator | 25 | 3 |
| Versatile Framework | 25 | 3 |
| Modular Frame | 17.5 | 3 |
| Circuit Board | 13 | 3 |
| Motor | 10 | 3 |
| Smart Plating | 10 | 3 |
| Automated Wiring | 5 | 3 |
| Encased Industrial Beam | 5 | 3 |
| Modular Engine | 5 | 4 |
| Computer | 2 | 4 |
| Adaptive Control Unit | 1 | 4 |
| Heavy Modular Frame | 1 | 4 |

</details>

## Status

- [x] Raw material budget solved
- [ ] Machine counts per tier (tier 1 done)
- [ ] HOR disposal decided
- [ ] Power budget
- [x] Node allocation for current save (see [`resources/raw-material-budget.md`](../../resources/raw-material-budget.md))
- [ ] Built in-game
