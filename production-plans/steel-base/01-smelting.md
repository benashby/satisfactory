# Tier 1 — Smelting & Refining

## Ingots

| Ingot | Rate | Building | Machines | Practical build | Uniform alternative |
| --- | --- | --- | --- | --- | --- |
| Iron Ingot | 907.5/min | Smelter | 30.25 | 30 @ 100% + 1 @ 25% | 31 @ 97.58% |
| Steel Ingot | 802.5/min | Foundry | 17.83 | 17 @ 100% + 1 @ 83.33% | 18 @ 99.07% |
| Copper Ingot | 268/min | Smelter | 8.93 | 8 @ 100% + 1 @ 93.33% | 9 @ 99.26% |

39 smelters, 18 foundries. The uniform-clock builds cost marginally less power
and are easier to clone as a blueprint.

### Ore in

| Ingot | Ore | Rate |
| --- | --- | --- |
| Iron Ingot | Iron Ore | 907.5/min |
| Steel Ingot | Iron Ore | 802.5/min |
| | Coal | 802.5/min |
| Copper Ingot | Copper Ore | 268/min |

### Ingots out

| Ingot | Consumer | Rate |
| --- | --- | --- |
| Iron Ingot (907.5) | Iron Rod | 581.25/min |
| | Iron Plate | 326.25/min |
| Steel Ingot (802.5) | Steel Beam | 660/min |
| | Steel Pipe | 142.5/min |
| Copper Ingot (268) | Wire | 216/min |
| | Copper Sheet | 52/min |

### Output belts

| Ingot | Rate | Belt |
| --- | --- | --- |
| Iron Ingot | 907.5/min | 2 × Mk.5 or 1 × Mk.6 |
| Steel Ingot | 802.5/min | 2 × Mk.5 or 1 × Mk.6 |
| Copper Ingot | 268/min | 1 × Mk.3 (270 cap — only 2/min of headroom) |

Consider running copper on Mk.4 anyway: at 268 of a 270 cap, any later overclock
forces a belt upgrade.

### Power

Smelter 4 MW, Foundry 16 MW *(verify in-game)*.

| Group | Machines | Draw |
| --- | --- | --- |
| Iron smelters | 30.25 | ~121 MW |
| Copper smelters | 8.93 | ~36 MW |
| Foundries | 17.83 | ~285 MW |
| **Total** | | **~442 MW** |

Steel dominates: the foundries draw nearly twice what all 39 smelters draw
together. Underclocked builds come in slightly under these figures, since power
scales super-linearly with clock speed.

## Refining

| Item | Rate | Building | Count |
| --- | --- | --- | --- |
| Plastic | 84/min | Refinery | 4.2 |
| Rubber | 75/min | Refinery | 3.75 |

## Heavy Oil Residue — 117 m³/min, unhandled

Standard Plastic (30 crude → 20 plastic + 10 HOR) and Rubber (30 crude → 20
rubber + 20 HOR) produce HOR as a byproduct:

- Plastic line → 42 m³/min
- Rubber line → 75 m³/min

**Nothing in this plan consumes it.** A refinery whose byproduct output backs up
stops entirely, so unhandled HOR stalls plastic and rubber, which stalls circuit
boards, computers, and the Adaptive Control Unit. It needs a destination.

Options, roughly in order of preference:

1. **Residual Fuel → Fuel Generators.** 60 HOR → 40 Fuel, so 117 HOR/min needs
   1.95 refineries and yields 78 Fuel/min. Turns the waste into power the
   factory badly needs — see the ~442 MW smelting draw above. ~3.9 Fuel
   Generators at 20 m³/min each. *(Verify generator rate and MW in-game.)*
2. **Petroleum Coke.** 40 HOR → 120 Coke. Useful if there's a coal shortfall
   elsewhere, but this plan has 127.5/min of spare coal.
3. **Package and sink.** Simplest to build, wastes the energy.

Recommendation: option 1 — it's the only one that pays for itself.

## TODO

- [ ] Pick the HOR route and add its machines above
- [ ] Verify smelter/foundry power figures in-game
- [ ] Decide whether steel foundries sit next to the miners or the beam line
