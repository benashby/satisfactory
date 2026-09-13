# Tier 2 — Basic Parts (Constructors)

Concrete is already built and arrives as 1 × 150/min line, so eight items
remain. All are Constructors — ~119 machines, the largest tier by machine count.

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

Steel Beam lands on a whole number — build 11 at 100% and forget about it.

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
| Copper Sheet | 26/min | Circuit Board (all) | 1 × Mk.1 |

## Blueprint banks — 10 constructors each

Bank counts rounded up so every machine runs below 100%.

| Item | Machines needed | Banks | Constructors | Clock |
| --- | --- | --- | --- | --- |
| Iron Rod | 38.75 | 4 | 40 | 96.875% |
| Screws | 32.63 | 4 | 40 | 81.5625% |
| Wire | 14.4 | 2 | 20 | 72% |
| Steel Beam | 11 | 2 | 20 | 55% |
| Iron Plate | 10.88 | 2 | 20 | 54.375% |
| Steel Pipe | 4.75 | 1 | 10 | 47.5% |
| Cable | 3.87 | 1 | 10 | 38.6667% |
| Copper Sheet | 2.6 | 1 | 10 | 26% |
| **Total** | **118.87** | **17** | **170** | |

Cable is the only non-terminating clock: 116/300 = 38.666…%. Enter 38.6667%,
which yields 116.0001/min — rounding slightly over target rather than under.

### Screws sited at their consumers

Per the layout note above, building screws beside their consumers instead of as
one central bank costs one extra bank and avoids running two Mk.5 belts of
screws across the factory:

| Screw group | Rate | Banks | Constructors | Clock |
| --- | --- | --- | --- | --- |
| At the rotors | 750/min | 2 | 20 | 93.75% |
| At the reinforced plates | 435/min | 2 | 20 | 54.375% |
| At the heavy modular frames | 120/min | 1 | 10 | 30% |

18 banks total instead of 17. Worth the trade.

### Power

~432 MW across all 17 banks, against ~476 MW for a tight 119-constructor build
at 100%. Underclocking more machines costs less power than running fewer at
full speed, because draw scales with clock^1.32. *(Approximate — verify the
exponent and constructor base draw in-game.)*

## Feeding the banks — Mk.4 (480/min) lines

No bank needs more than one 480 line. The hungriest is Steel Beam at 330/min.

| Item | Banks | Input | Per bank | Banks per 480 line |
| --- | --- | --- | --- | --- |
| Steel Beam | 2 | 660 steel ingot | 330 | 1 only |
| Iron Plate | 2 | 326.25 iron ingot | 163.13 | 2 |
| Iron Rod | 4 | 581.25 iron ingot | 145.31 | 3 |
| Steel Pipe | 1 | 142.5 steel ingot | 142.5 | 3 |
| Wire | 2 | 216 copper ingot | 108 | 4 |
| Copper Sheet | 1 | 52 copper ingot | 52 | 9 |

Two banks can share a line everywhere **except Steel Beam**, where two banks
draw 660/min and overrun the belt. Those two get separate feeds.

### Assignment to the delivered lines

| Line | Feeds | Load |
| --- | --- | --- |
| Iron Ingot 480 | Iron Plate ×2 banks + Iron Rod ×1 bank | 471.56 / 480 |
| Iron Ingot 450 (first) | Iron Rod ×3 banks | 435.94 / 480 |
| Iron Ingot 450 (second) | — spare | 0 |
| Copper Ingot 300 | Wire ×2 banks + Copper Sheet ×1 bank | 268 / 300 |
| Steel A (built here) | Steel Beam ×1 bank + Steel Pipe ×1 bank | 472.5 / 480 |
| Steel B (built here) | Steel Beam ×1 bank | 330 / 480 |

**Two of the three delivered iron ingot lines cover the plan**, with 22.5/min to
spare. The third is entirely surplus — route it to storage or leave it for a
later expansion.

All copper fits on the single delivered 300 line, with 32/min spare. This is the
tightest feed in the plan.

The Iron Ingot 480 and Steel A lines run at ~98% of belt capacity — slow to
prime on startup, and no buffer against an upstream hiccup. Fine in steady state.

### Concrete

Delivered at 150/min against 30/min needed. Goes straight to Encased Industrial
Beam; no constructors required here.

### Internal feed

326.25/min of Iron Rod goes to the screw constructors — one more 480 line.

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
