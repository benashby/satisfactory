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
- **Much of the plan already exists as delivered lines**: iron ingot
  (1,380/min), copper ingot (300/min), concrete (150/min), plus plastic
  (84/min) and rubber (75/min) from the oil factory. What remains to build is
  the steel foundries and tiers 2-4. See
  [`raw-material-budget.md`](../../resources/raw-material-budget.md).

## Tiers

| File | Contents |
| --- | --- |
| [`00-raw-materials.md`](00-raw-materials.md) | Iron ore and coal feeds (built) |
| [`01-smelting.md`](01-smelting.md) | Steel foundries (iron and copper ingots delivered) |
| [`02-basic-parts.md`](02-basic-parts.md) | Rods, screws, plates, wire, cable, sheets, beams, pipes (concrete delivered) |
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
| Crude Oil | 238.5 m³ | handled externally |
| Limestone | 90 | 0 (concrete delivered) |
| Iron Ingot | 907.5 | 1 |
| Steel Ingot | 802.5 | 1 |
| Copper Ingot | 268 | 1 |
| Plastic | 84 | 1 (imported) |
| Rubber | 75 | 1 (imported) |
| Heavy Oil Residue | 117 m³ | handled externally |
| Screws | 1,305 | 2 |
| Iron Rod | 581.25 | 2 |
| Wire | 432 | 2 |
| Iron Plate | 217.5 | 2 |
| Steel Beam | 165 | 2 |
| Cable | 116 | 2 |
| Steel Pipe | 95 | 2 |
| Copper Sheet | 26 | 2 |
| Concrete | 30 | 2 (delivered) |
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

- [x] Raw material budget solved — all requirements met
- [ ] Machine counts per tier (tier 1 done)
- [x] Heavy Oil Residue — handled by the existing oil factory
- [x] Power — met by existing infrastructure
- [x] Node allocation for current save (see [`resources/raw-material-budget.md`](../../resources/raw-material-budget.md))
- [x] Tier 0 extraction built
- [x] Iron and copper ingots built and delivered
- [x] Concrete built and delivered
- [ ] Steel foundries built
- [ ] Tiers 2-4 built in-game
