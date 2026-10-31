---
name: design-review
description: Run Vector-Zero's 10-point engineering design review on an idea or project and write the results to the repo. Use when the owner asks "is this feasible", "review this design", "should I build this", or before turning an idea into a project.
---

# Design review

## Gather context
- Read the idea file or `projects/<name>/` docs if they exist.
- Check `components/inventory.md`, `research/tech-radar.md`, `decisions/README.md` and related `research/` notes.
- If a requirement that would change the answer is missing (budget, power source, range, environment, quantity), ask once, briefly. Otherwise make a stated assumption and continue.

## Review
Answer all 10, concretely and honestly:
1. What problem does it solve, and for whom?
2. Is it technically feasible? Name the hard parts.
3. Is there a simpler approach (including buying something off the shelf)?
4. Biggest risks: technical, safety, cost, schedule, regulatory.
5. Required components: specific models, rough cost, alternatives.
6. What would a prototype look like? (Smallest thing that proves the core idea.)
7. What should be tested first? Make it the riskiest assumption, with a go/no-go criterion.
8. What could cause failure in the field? (Power, environment, RF, mechanical, firmware lockups.)
9. How could it scale later?
10. Is it worth building? Give a clear verdict: build / build a smaller version / park / don't.

For any significant choice, compare the simplest, cheapest, most reliable and most scalable options, and recommend one.

## Write it down
- If the project folder exists: update `projects/<name>/project-brief.md` and `risk-assessment.md` (from `_templates/`).
- If it's still an idea: append a "Design review (YYYY-MM-DD)" section to the idea file and set status `reviewed`.
- Add any new technologies to `research/tech-radar.md` under Assess.
- Reply with the verdict, the top three risks, the first test, and where you wrote it. If the verdict is "build", offer `/new-project`.
