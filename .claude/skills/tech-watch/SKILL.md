---
name: tech-watch
description: Sweep the web for news on technologies in Vector-Zero's tech radar (new chip and board releases, PX4/ArduPilot/Betaflight/ESP-IDF versions, deprecations, end-of-life notices, notable new hobbyist parts) and update research/tech-radar.md. Use when the owner asks "what's new", "keep me up to date", "any new tech for...", or wants the radar refreshed.
---

# Tech watch

1. Read `research/tech-radar.md`. Focus on entries whose "Last checked" date is blank or older than about 60 days. If the owner named an area (e.g. "drones"), only check that area.
2. For each entry, search for the latest stable release or version, any end-of-life or not-recommended-for-new-designs notices, and major problems (supply shortages, critical bugs). Prefer primary sources: vendor sites, GitHub releases, official docs.
3. Look for new options worth adding under Assess in areas the owner works in: MCUs and SBCs, radios, flight controllers and stacks, sensors, edge ML accelerators, battery tech, PCB/CAD tools. Only add things a hobbyist can actually buy or use now.
4. Update the radar: version or status, Last checked (today), and a source link in Notes. Don't move an entry's ring on news alone; suggest the move and give the reason. Rings move when Vector-Zero projects prove or disprove something, or the owner agrees.
5. If an update affects an active project (a part going end-of-life, a breaking firmware release), say so and add a note to that project's risk assessment.
6. Reply with a short digest: what changed, what's new and worth a look, and any action needed on current projects. Every claim needs a source, and don't guess versions.
