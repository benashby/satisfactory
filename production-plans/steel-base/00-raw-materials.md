# Tier 0 — Raw Materials

> **Built.** Extraction is complete. What the factory actually receives:
>
> | Item | Lines | Total | Needed |
> | --- | --- | --- | --- |
> | Iron Ore | 2 × 480 | 960/min | 802.5/min |
> | Coal | 480 + 300 + 150 | 930/min | 802.5/min |
>
> Both go to the steel foundries and nothing else. Copper ore and limestone no
> longer appear here — copper ingot and concrete arrive already made. The
> extractor sizing below is kept as reference for future expansions.

Everything the plan needs out of the ground. These five feeds are the entire
input side; nothing else enters the factory.

| Resource | Required | Extractor | Feed belt/pipe |
| --- | --- | --- | --- |
| Iron Ore | 1,710/min | 3.56 pure-node Miner Mk.3 | 3 × Mk.5 (2,340 cap) or 2 × Mk.6 |
| Coal | 802.5/min | 1.67 pure-node Miner Mk.3 | 2 × Mk.5 or 1 × Mk.6 (1,200 cap) |
| Copper Ore | 268/min | 0.56 pure-node Miner Mk.3 | 1 × Mk.3 (270 cap — 2/min of headroom) |
| Crude Oil | 238.5 m³/min | 0.99 pure-node Oil Extractor | 1 × Mk.1 pipe (300 cap) |
| Limestone | 90/min | 0.38 normal-node Miner Mk.3 | 1 × Mk.2 (120 cap) |

**Crude oil is almost exactly one pure node** (238.5 of 240 — a pure Oil
Extractor at 99.4%). Site the factory to reach one, and the whole oil branch is
a single extractor and a single Mk.1 pipe.

## Where the ore goes

| Resource | Consumer | Rate |
| --- | --- | --- |
| Iron Ore | Iron Ingot | 907.5/min |
| | Steel Ingot (with coal) | 802.5/min |
| Coal | Steel Ingot | 802.5/min |
| Copper Ore | Copper Ingot | 268/min |
| Crude Oil | Plastic | 126 m³/min |
| | Rubber | 112.5 m³/min |
| Limestone | Concrete | 90/min |

Coal is used **only** for steel — there is no coal power in this plan, so the
factory needs an external power source.

## Extractor options

Node purity and miner tier trade off; pick whatever the save actually has.

### Iron Ore — 1,710/min

| Setup | Nodes | Clock |
| --- | --- | --- |
| Miner Mk.3, pure | 4 | 89.06% |
| Miner Mk.3, 3 pure + 1 normal | 4 | 101.8% |
| Miner Mk.2, pure | 8 | 89.06% |
| Miner Mk.2, normal | 15 | 95% |

A Miner Mk.3 on a pure node outputs 480/min, which is exactly the Mk.4 belt
cap — so every pure-node miner needs a Mk.4 or better belt with no margin.
Prefer Mk.5 so an overclock later doesn't require re-belting.

### Coal — 802.5/min

| Setup | Nodes | Clock |
| --- | --- | --- |
| Miner Mk.3, pure | 2 | 83.6% |
| Miner Mk.3, 1 pure + 2 normal | 3 | 83.6% |
| Miner Mk.2, pure | 4 | 83.6% |

### Copper Ore — 268/min

| Setup | Nodes | Clock |
| --- | --- | --- |
| Miner Mk.3, pure | 1 | 55.8% |
| Miner Mk.3, normal | 1 | 111.7% (1 power shard) |
| Miner Mk.2, pure | 2 | 55.8% |

### Crude Oil — 238.5 m³/min

| Setup | Nodes | Clock |
| --- | --- | --- |
| Oil Extractor, pure | 1 | 99.4% |
| Oil Extractor, normal | 2 | 99.4% |

### Limestone — 90/min

| Setup | Nodes | Clock |
| --- | --- | --- |
| Miner Mk.3, normal | 1 | 37.5% |
| Miner Mk.2, normal | 1 | 75% |
| Miner Mk.1, normal | 1 | 150% (2 power shards) |

Limestone is the one trivial feed — a single underclocked miner covers it.

## Notes

- Underclocking is strongly preferred over overclocking here: power draw scales
  super-linearly with clock speed, and every one of these targets sits *below* a
  whole number of pure nodes.
- Node assignments for a specific save do **not** belong in this file — they go
  in `resources/` so this plan stays portable between saves.

## TODO

- [ ] Power draw for the extractor bank
- [ ] Decide Mk.5 vs Mk.6 belts for iron (Mk.6 halves the belt count but needs Tier 9)
- [ ] Assign real nodes in the current save
