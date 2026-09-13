# Satisfactory Notes

Personal notes, production plans, and factory designs for
[Satisfactory](https://www.satisfactorygame.com/) (Coffee Stain Studios).

This is a scratchpad-turned-reference: everything I work out in-game — ratios,
build layouts, logistics routes, to-do lists — gets written down here so I stop
re-deriving the same math every save.

## Contents

| Directory | What lives there |
| --- | --- |
| [`production-plans/`](production-plans/) | Ratio math and line plans for specific items (machine counts, inputs/outputs, byproducts) |
| [`factories/`](factories/) | Per-factory build notes: location, layout, what it makes, what it needs |
| [`resources/`](resources/) | Node surveys, purity/allocation tracking, power and pipe budgets |
| [`reference/`](reference/) | Cheat sheets: belt/pipe throughput, alt recipes worth chasing, milestone checklists |
| [`saves-notes/`](saves-notes/) | Per-save logs — current goals, what's half-built, screenshots |

## Conventions

- One Markdown file per topic, named in `kebab-case.md`.
- Every production plan states the **target output rate** up front (items/min),
  then the machine counts needed to hit it.
- Note the **recipe variant** used (standard vs. alternate) — alt recipes change
  ratios completely, and a plan without one is unreproducible.
- Record numbers as items per minute (`/min`), the unit the game's UI uses.
- Mark anything not yet verified in-game with `TODO` or `(unverified)`.

## Production plan template

```markdown
# <Item> — <N>/min

**Recipes:** <standard / alternate recipe names used>
**Power:** ~<N> MW
**Location:** <factory or "unplaced">

## Inputs
| Item | Rate (/min) | Source |
| --- | --- | --- |

## Machines
| Building | Recipe | Count | Clock |
| --- | --- | --- | --- |

## Outputs & byproducts
| Item | Rate (/min) | Destination |
| --- | --- | --- |

## Notes
- <gotchas, overflow handling, sink routing>
```

## Tools I use alongside these notes

- [Satisfactory Tools](https://www.satisfactorytools.com/) — production chain solver
- [Satisfactory Calculator](https://satisfactory-calculator.com/) — interactive map, save editor
- [Official wiki](https://satisfactory.wiki.gg/)

## Status

Early days — structure first, content as I play.
