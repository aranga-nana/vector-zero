---
name: new-project
description: Start a new Vector-Zero project, or promote an idea to a project, creating the project folder, brief, risk assessment, BOM and the project-named subfolders. Use when the owner says "let's build X", "start a project", or approves an idea.
---

# New project

1. Choose a kebab-case project name. Confirm it only if it's ambiguous. Use the same name everywhere.
2. If an idea file exists, read it and any design review in it.
3. Create:
   - `projects/<name>/README.md` from `_templates/project-readme.md`
   - `projects/<name>/project-brief.md` from `_templates/project-brief.md`, filled in from what's known
   - `projects/<name>/risk-assessment.md` from `_templates/risk-assessment.md`, with at least the top risks
   - `bom/<name>.csv` from `_templates/bom.csv`, with known parts
4. Only create type folders the project actually needs, for example `firmware/<name>/`, `software/<name>/`, `cad/<name>/`, `pcbs/<name>/`, `electronics/<name>/`, `ai-ml/<name>/`, `drones/<craft>/`, `test-results/<name>/`, `build-logs/<name>/`, `photos/<name>/`. Link each one from the project README.
5. Add a row to `projects/README.md` and set the status.
6. If promoted from an idea, set the idea's status to `promoted → projects/<name>/`.
7. If no design review has been done, run the `/design-review` steps now.
8. Reply with the folder tree you created and the first concrete step (usually the riskiest bench test).
