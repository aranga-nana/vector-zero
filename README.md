# Vector-Zero

Engineering HQ: ideas, projects, research, designs, firmware, and the reasoning behind decisions.

## Layout

| Folder | What goes here |
|---|---|
| `ideas/` | Raw ideas, one file each, before they earn a project |
| `projects/` | One folder per active project (brief, plans, risks, links) |
| `research/` | Notes on parts, protocols, techniques, datasheet summaries |
| `decisions/` | Numbered decision records (`0001-title.md`), cross-project |
| `architecture/` | System architecture docs and diagrams |
| `components/` | Reusable part notes and evaluations |
| `electronics/` | Schematics, circuits, breadboard notes |
| `pcbs/` | KiCad / EasyEDA projects, gerbers |
| `firmware/` | Microcontroller code |
| `software/` | Host-side, cloud, and tooling code |
| `ai-ml/` | TinyML / vision / model experiments |
| `drones/` | Airframes, FC configs, PX4/ArduPilot params, flight logs |
| `cad/` | Per-project CAD source and print files (`cad/<project>/source/`, `print/`) |
| `fabrication/` | 3D printers, slicer profiles, calibration results, filament library |
| `bom/` | Bills of materials |
| `test-results/` | Measurements, benchmarks, test reports |
| `build-logs/` | Dated build diaries |
| `photos/` | Build and test photos |
| `docs/` | Cross-cutting documentation |
| `archive/` | Shelved or finished work |
| `_templates/` | Starter docs: decision record, project brief, risk assessment, BOM |

## Working with Claude

[CLAUDE.md](CLAUDE.md) tells Claude who to be, how to evaluate decisions, and which folder each kind of content belongs in. Start a Claude session in this folder and it picks that up automatically.

Project skills in `.claude/skills/`:

| Skill | Use it to |
|---|---|
| `/new-idea` | Capture an idea |
| `/design-review` | Run the 10-point review |
| `/new-project` | Start a project with its full folder set |
| `/decision` | Record a decision |
| `/select-components` | Pick parts and build the BOM |
| `/build-log` | Log a bench session |
| `/test-report` | Record a test |
| `/print-job` | Get help with 3D printing: design review, settings, failed prints, calibration |
| `/tech-watch` | Refresh the tech radar from the web |
| `/vz-status` | Audit the repo and get a status report |

Key living docs: [projects/README.md](projects/README.md), [decisions/README.md](decisions/README.md), [components/inventory.md](components/inventory.md), [research/tech-radar.md](research/tech-radar.md), [fabrication/filaments.md](fabrication/filaments.md), [docs/design-for-printing.md](docs/design-for-printing.md).

## Conventions

- New project: `projects/<name>/`, start from `_templates/project-brief.md`.
- Decisions that outlive one project go in `decisions/`, numbered sequentially.
- Record why, not just what.
- Large binaries (CAD, photos, logs) should go through Git LFS once the repo is initialised.
