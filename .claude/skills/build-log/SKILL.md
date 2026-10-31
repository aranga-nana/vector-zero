---
name: build-log
description: Log a build or debugging session for a Vector-Zero project as a dated entry in build-logs/. Use when the owner reports what they did at the bench ("today I soldered...", "got the motor spinning", "it keeps resetting").
---

# Build log

1. Identify the project. Use today's date unless the owner gives another.
2. Write `build-logs/<project>/YYYY-MM-DD.md` from `_templates/build-log.md`. If that file already exists, append a new session section.
3. Record what they did, what worked, what broke, and the parts used, in their own words and tightened up.
4. If something broke, add a short "Likely causes" list with the next debug step for each. Common culprits: power, grounding, brownout, logic levels, wiring and pin mapping.
5. If stock changed, update `components/inventory.md`. If measurements were taken, offer `/test-report`. If the project status changed, update the project README and `projects/README.md`.
6. Reply with the next-session plan.
