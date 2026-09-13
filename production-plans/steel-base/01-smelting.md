# Tier 1 — Smelting & Refining

| Item | Rate | Building | Count |
| --- | --- | --- | --- |
| Iron Ingot | 907.5/min | Smelter | 30.25 |
| Steel Ingot | 802.5/min | Foundry | 17.83 |
| Copper Ingot | 268/min | Smelter | 8.93 |
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
   factory already needs (coal here is spoken for by steel). ~3.9 Fuel
   Generators at 20 m³/min each. *(Verify generator rate and MW in-game.)*
2. **Petroleum Coke.** 40 HOR → 120 Coke. Useful if there's a coal shortfall
   elsewhere, but this plan doesn't need it.
3. **Package and sink.** Simplest to build, wastes the energy.

Recommendation: option 1 — it's the only one that pays for itself.

## TODO

- [ ] Pick the HOR route and add its machines above
- [ ] Power draw for smelters/foundries/refineries
- [ ] Decide whether steel foundries sit next to the miners or the beam line
