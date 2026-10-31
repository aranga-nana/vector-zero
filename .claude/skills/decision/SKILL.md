---
name: decision
description: Record an engineering decision as a numbered decision record in Vector-Zero's decisions/ folder, comparing the simplest, cheapest, most reliable and most scalable options. Use when a significant choice is made or needs making (MCU, radio, flight stack, power system, protocol, architecture).
---

# Decision record

1. Read `decisions/README.md`. Check whether an accepted decision already covers this. If so, either stay consistent with it or write a new one that supersedes it, and mark the old one `superseded by NNNN`.
2. Take the next free number (four digits). File it as `decisions/NNNN-kebab-title.md` from `_templates/decision-record.md`.
3. Fill in the context, then compare at least the simplest, cheapest, most reliable and most scalable options on cost, complexity, reliability, maintainability, scalability, availability and repairability. Prefer parts in `components/inventory.md` and Adopt/Trial entries on `research/tech-radar.md`.
4. State the decision, what it gives up, and what would trigger a revisit.
5. Status is `proposed` unless the owner has agreed, in which case it's `accepted`.
6. Add the row to `decisions/README.md`. Link the record from the project README if it's project-specific. Move the chosen tech's ring on the tech radar if appropriate.
7. Reply with the recommendation in two or three sentences and the file link.
