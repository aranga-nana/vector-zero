---
name: vz-status
description: Audit the Vector-Zero repo and report project status, missing or stale docs, broken indexes and misfiled content, then fix what's safe to fix. Use when the owner asks "where are we", "what's the status", "review the repo", or at the start of a working session.
---

# Vector-Zero status

1. Scan the tree, ignoring `.gitkeep` files and `archive/`.
2. For each project, check:
   - It has a row in `projects/README.md`, and the status there matches the project README.
   - It has `README.md`, `project-brief.md` and `risk-assessment.md`, plus a BOM if there's hardware.
   - Its type folders (`firmware/<name>/` and so on) are linked from its README.
   - Its last build log or test report date. Flag a project as stale if nothing has happened in 30+ days and it isn't done or shelved.
3. Check that `decisions/README.md` matches the files in `decisions/` and that numbering has no gaps or duplicates.
4. Check `ideas/` for ideas promoted without a link, or reviewed but never decided.
5. Look for misfiled content: code outside `firmware/` or `software/`, project docs at the repo root, and names that aren't kebab-case.
6. Check `research/tech-radar.md` for entries older than 60 days, and suggest `/tech-watch` if there are many.
7. Fix the safe things directly: index rows, links, and status mismatches. List anything that needs the owner's call, such as moving files or archiving a project. Don't delete anything.
8. Reply with:
   - a status table (project, status, last activity, next step)
   - what you fixed
   - what needs the owner's decision
   - the single most valuable next action
