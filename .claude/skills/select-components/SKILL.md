---
name: select-components
description: Choose specific hardware parts for a Vector-Zero project (MCU, sensors, radios, motors, ESCs, batteries, BMS, regulators, cameras, frames) and write the comparison and BOM. Use when the owner asks "what should I use for...", "which sensor/board/battery", or needs a parts list.
---

# Component selection

1. Pin down the requirements for this function: interfaces, voltage, power budget, size and weight, environment, accuracy, quantity, budget. Ask once only if a missing fact would change the pick.
2. Check `components/inventory.md` (parts on hand win ties), `components/<part>.md` evaluations, and `research/tech-radar.md`.
3. Compare 3–5 specific models (exact part numbers or modules, not generic categories). For each: why consider it, key specs, rough cost in USD, worldwide availability (AliExpress, Digi-Key/Mouser, LCSC, Amazon), whether it's already owned, and concerns.
4. Name the simplest, cheapest, most reliable and most scalable options, then pick one for the stated goals. Give a fallback if it's out of stock.
5. Call out compatibility gotchas: logic levels, current draw, I2C address clashes, library support, footprints, connector types, and battery C-rating against motor draw.
6. If current prices or availability matter and could have changed, verify them with a web search, and say what you checked.
7. Write `projects/<name>/component-selection.md` (from `_templates/component-selection.md`, one section per function). Add or update rows in `bom/<name>.csv`. For a reusable part, also add `components/<part>.md`.
8. If the pick is significant, record it with the `/decision` steps. Update the tech radar.
9. Reply with the picks, the BOM total, and the main compatibility risks.
