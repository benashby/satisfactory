# Tier 1 — Smelting

## Delivered

Iron and copper smelting are built. Both arrive as lines:

| Item | Lines | Total | Plan needs |
| --- | --- | --- | --- |
| Iron Ingot | 3 × (480, 450, 450) | 1,380/min | 907.5/min |
| Copper Ingot | 1 × 300 | 300/min | 268/min |

## Steel foundries — to build

The only tier 1 work remaining. 12 foundries, overclocked:

| | Rate |
| --- | --- |
| Iron Ore in | 802.5/min |
| Coal in | 802.5/min |
| Steel Ingot out | 802.5/min |
| Clock | 148.6111% |

12 × 45 × 1.486111 = 802.5. One power shard per foundry — 148.61% fits under the
150% ceiling a single shard gives. Twelve shards total.

A 100% build would use 17.83 foundries instead.

### Feeds

Coal and iron ore are 1:1 in the standard recipe, so both are 802.5/min.

| Item | Delivered | Needed | Spare |
| --- | --- | --- | --- |
| Iron Ore | 2 × 480 = 960/min | 802.5/min | +157.5 |
| Coal | 480 + 300 + 150 = 930/min | 802.5/min | +127.5 |

Both feeds are oversupplied, so the foundries will never starve. Do not raise
them to 960/min: that would need 960 coal against 930 secured, and 177.78% on
the foundries.

Steel must be made from iron **ore**. The standard recipe does not take ingots;
the Solid Steel Ingot alt does, but would push total ingot demand to 1,442.5/min
against 1,380 delivered.

## Ingot allocation

| Ingot | Consumer | Rate |
| --- | --- | --- |
| Iron Ingot (907.5 used) | Iron Rod | 581.25/min |
| | Iron Plate | 326.25/min |
| Steel Ingot (802.5) | Steel Beam | 660/min |
| | Steel Pipe | 142.5/min |
| Copper Ingot (268 used) | Wire | 216/min |
| | Copper Sheet | 52/min |

## Steel output belts

802.5/min needs 2 × Mk.4. A single Mk.5 cannot carry it — 780 falls just short.

| Line | Feeds | Load |
| --- | --- | --- |
| Steel A | Steel Beam ×1 bank + Steel Pipe ×1 bank | 472.5 / 480 |
| Steel B | Steel Beam ×1 bank | 330 / 480 |

## Plastic and Rubber — external

Supplied by the existing oil factory at 84/min and 75/min. Crude oil extraction,
refining, and Heavy Oil Residue disposal (117 m³/min) are all handled there.

## Power

Reference only — power needs are already met. Foundry 16 MW *(verify in-game)*,
so 12 foundries at 148.61% draw well above their 192 MW nameplate; overclocking
scales draw with clock^1.32.
