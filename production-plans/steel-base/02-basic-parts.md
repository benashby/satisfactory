# Tier 2 — Basic Parts (Constructors)

All nine items are Constructors. ~121 machines total, the largest tier in the
plan by machine count.

| Item | Rate | Machines | Practical build | Uniform alternative |
| --- | --- | --- | --- | --- |
| Iron Rod | 581.25/min | 38.75 | 38 @ 100% + 1 @ 75% | 39 @ 99.36% |
| Screws | 1,305/min | 32.63 | 32 @ 100% + 1 @ 62.5% | 33 @ 98.86% |
| Wire | 432/min | 14.4 | 14 @ 100% + 1 @ 40% | 15 @ 96% |
| **Steel Beam** | 165/min | **11 exactly** | 11 @ 100% | — |
| Iron Plate | 217.5/min | 10.88 | 10 @ 100% + 1 @ 87.5% | 11 @ 98.86% |
| Steel Pipe | 95/min | 4.75 | 4 @ 100% + 1 @ 75% | 5 @ 95% |
| Cable | 116/min | 3.87 | 3 @ 100% + 1 @ 86.67% | 4 @ 96.67% |
| Copper Sheet | 26/min | 2.6 | 2 @ 100% + 1 @ 60% | 3 @ 86.67% |
| **Concrete** | 30/min | **2 exactly** | 2 @ 100% | — |

Steel Beam and Concrete land on whole numbers — build those at 100% and forget
about them.

## Inputs

| Item | Input | Rate |
| --- | --- | --- |
| Iron Rod | Iron Ingot | 581.25/min |
| Screws | Iron Rod | 326.25/min |
| Iron Plate | Iron Ingot | 326.25/min |
| Wire | Copper Ingot | 216/min |
| Cable | Wire | 232/min |
| Copper Sheet | Copper Ingot | 52/min |
| Steel Beam | Steel Ingot | 660/min |
| Steel Pipe | Steel Ingot | 142.5/min |
| Concrete | Limestone | 90/min |

## Outputs

| Item | Rate | Goes to | Belt |
| --- | --- | --- | --- |
| Screws | 1,305/min | Rotor 750, Reinforced Iron Plate 435, Heavy Modular Frame 120 | 2 × Mk.5 |
| Iron Rod | 581.25/min | Screws 326.25, Rotor 150, Modular Frame 105 | 1 × Mk.5 |
| Wire | 432/min | Cable 232, Stator 200 | 1 × Mk.4 |
| Iron Plate | 217.5/min | Reinforced Iron Plate (all) | 1 × Mk.3 |
| Steel Beam | 165/min | Versatile Framework 150, Encased Industrial Beam 15 | 1 × Mk.3 |
| Cable | 116/min | Automated Wiring 100, Computer 16 | 1 × Mk.2 (120 cap — tight) |
| Steel Pipe | 95/min | Stator 75, Heavy Modular Frame 20 | 1 × Mk.2 |
| Concrete | 30/min | Encased Industrial Beam (all) | 1 × Mk.1 |
| Copper Sheet | 26/min | Circuit Board (all) | 1 × Mk.1 |

## Layout notes

- **Screws are the dominant flow at 1,305/min** — more than one Mk.6 belt can
  carry. Don't build one central screw bank and belt it out. Split the 33
  constructors into three groups sited next to their consumers (750 at the
  rotors, 435 at the reinforced plates, 120 at the heavy modular frames) and
  belt Iron Rod to them instead. Rod is 581.25/min, less than half the volume.
- **Cable at 116/min sits just under the Mk.2 cap of 120.** Same situation as
  copper ingot on Mk.3. Run it on Mk.3 if a later overclock is plausible.
- Iron Rod feeds three different consumers including screws; a manifold with
  correct priority matters more here than anywhere else in the plan.

## Power

Constructor 4 MW *(verify in-game)* → ~484 MW across the tier. Reference only;
power is already met.
