# Fabrication

Shared knowledge about how we make things: printers, slicer profiles, calibration and materials. Files for a specific part live in `cad/<project>/`. This folder holds what's true across projects.

| Path | What goes here |
|---|---|
| `printers/<printer>.md` | One file per machine: model, mods, nozzle, firmware, config, maintenance log (from `_templates/printer.md`) |
| `printers/<printer>/` | Machine config files (e.g. Klipper `printer.cfg`, macros) when there are any |
| `slicer-profiles/` | Exported printer, filament and process profiles (OrcaSlicer / Bambu Studio / PrusaSlicer). Name them `<printer>-<material>-<purpose>`. |
| `calibration/` | Calibration results per printer + filament (`<printer>-<filament>-YYYY-MM-DD.md`): temperature tower, flow, pressure advance, retraction, shrinkage |
| `filaments.md` | The filament library: what works, at what settings, and drying needs |

Related:
- Design rules: [../docs/design-for-printing.md](../docs/design-for-printing.md)
- Filament stock: [../components/inventory.md](../components/inventory.md)
- Per-part print settings: `cad/<project>/print-settings.md` (from `_templates/print-settings.md`)
