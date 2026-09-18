# Tier 3 — Assembled Parts

| Item | Rate | Building | Machines | Goes to |
| --- | --- | --- | --- | --- |
| Reinforced Iron Plate | 36.25/min | Assembler | 7.25 | Modular Frame 26.25, Smart Plating 10 |
| Rotor | 30/min | Assembler | 7.5 | Motor 20, Smart Plating 10 |
| Stator | 25/min | Assembler | 5 | Motor 20, Automated Wiring 5 |
| **Versatile Framework** | **25/min** | Assembler | 5 | **Final output** |
| Modular Frame | 17.5/min | Assembler | 8.75 | Versatile Framework 12.5, Heavy Modular Frame 5 |
| Circuit Board | 13/min | Assembler | 1.73 | Computer 8, Adaptive Control Unit 5 |
| Motor | 10/min | Assembler | 2 | Modular Engine (all) |
| Smart Plating | 10/min | Assembler | 5 | Modular Engine (all) |
| Automated Wiring | 5/min | Assembler | 5 | Adaptive Control Unit (all) |
| Encased Industrial Beam | 5/min | Assembler | 0.83 | Heavy Modular Frame (all) |

*(Machine counts derived from standard recipe rates — verify in-game.)*

Smart Plating and Automated Wiring are consumed internally; they are not
outputs of this plan.

## Siting the screw banks

Screws are made at their consumers, not belted. Iron rod splits into four
branches that each fit a single belt and sum to the full 581.25/min output:

| Site | Rod in | Belt | Contains |
| --- | --- | --- | --- |
| Rotor | 337.5/min | Mk.4 | 2 screw banks + 7.5 Rotor assemblers |
| Reinforced Iron Plate | 108.75/min | Mk.2 | 2 screw banks + 7.25 RIP assemblers |
| Modular Frame | 105/min | Mk.2 | 8.75 assemblers (no screws) |
| Heavy Modular Frame | 30/min | Mk.1 | 1 screw bank + 1 Manufacturer |

### Rotor — 750 screws

The rod belt does double duty: 187.5 to the two screw banks, 150 straight to
the assemblers. A Rotor takes 5 rod **and** 25 screws, so rod is the only
input this site needs delivered.

Out: 30 Rotor/min → Motor 20, Smart Plating 10.

### Reinforced Iron Plate — 435 screws

Two deliveries: rod 108.75 for the screw banks, and **Iron Plate 217.5/min**
(Mk.3) — the entire tier 2 plate output lands here.

Out: 36.25/min → Modular Frame 26.25, Smart Plating 10.

### Modular Frame — no screws

Not a screw consumer, but sits next to Reinforced Iron Plate: it eats 26.25 of
that output plus its own 105 rod.

Out: 17.5/min → Versatile Framework 12.5, Heavy Modular Frame 5.

### Heavy Modular Frame — 120 screws

Only 1/min, but the most input-hungry building in the plan: 5 Modular Frame,
20 Steel Pipe, 5 Encased Industrial Beam, 120 Screws. Put it downstream of
Modular Frame and near wherever steel lands.

## Adjacency constraints

- **Smart Plating pulls from both Rotor and Reinforced Iron Plate** (10 each).
  Site it between them or run two medium belts across the factory.
- **Reinforced Iron Plate → Modular Frame → Heavy Modular Frame is a chain.**
  Lay them in a line and the connections stay short.
- **Rotor is the odd one out** — rod in, Motor and Smart Plating out. It can sit
  anywhere the rod trunk reaches.

## TODO

- [ ] Verify assembler counts in-game
- [ ] Bank/blueprint layout for assemblers
- [ ] Power draw
