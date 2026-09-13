# Tier 1 — Smelting

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

Reference only — power needs are already met, so this is for layout and
substation sizing rather than a constraint. Smelter 4 MW, Foundry 16 MW
*(verify in-game)*.

| Group | Machines | Draw |
| --- | --- | --- |
| Iron smelters | 30.25 | ~121 MW |
| Copper smelters | 8.93 | ~36 MW |
| Foundries | 17.83 | ~285 MW |
| **Total** | | **~442 MW** |

Steel dominates: the foundries draw nearly twice what all 39 smelters draw
together. Underclocked builds come in slightly under these figures, since power
scales super-linearly with clock speed.

## Plastic and Rubber — external

Already built. The existing oil factory supplies both as belt inputs:

| Item | Rate |
| --- | --- |
| Plastic | 84/min |
| Rubber | 75/min |

Crude oil extraction, refining, and Heavy Oil Residue disposal (117 m³/min, a
byproduct of the standard plastic and rubber recipes) are all handled there.
Nothing in this plan needs to build or dispose of them.

## TODO

- [ ] Verify smelter/foundry power figures in-game
- [ ] Decide whether steel foundries sit next to the miners or the beam line
