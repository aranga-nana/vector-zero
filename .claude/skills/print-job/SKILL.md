---
name: print-job
description: Help with any 3D printing task in Vector-Zero: review a part's design for printability, choose material and slicer settings, diagnose a failed print, calibrate a printer or filament, or record what was printed. Use when the owner mentions printing, STLs, 3MF, slicers, filament, warping, stringing, layer adhesion, supports, enclosures, or a printer.
---

# Print job

## Gather context
- Printer: `fabrication/printers/` (if none is recorded, ask once which printer they have, then create the file from `_templates/printer.md`).
- Materials: `fabrication/filaments.md` and the filament stock in `components/inventory.md`.
- Earlier prints of this part: `cad/<project>/print-settings.md`. Earlier calibrations: `fabrication/calibration/`.
- Design rules: `docs/design-for-printing.md`.

## Pick the mode

**Design review (before printing)**
Check the part against `docs/design-for-printing.md`: orientation against load, wall thickness, tolerances for mating parts, overhangs and supports, fasteners and inserts, and material fit for heat, UV and load. Australian sun and car interiors rule out PLA. Give concrete changes (e.g. "add 1 mm chamfer on bottom edge", "split here and print flat"), not general advice.

**Settings**
Recommend material, layer height, walls, infill, orientation, supports and brim, with a reason for each. Prefer calibrated values from `fabrication/` over generic ones, and say which you're using.

**Failure diagnosis**
Ask for (or look at) a photo if it would settle the cause. Rank likely causes from most to least likely, each with a single check or fix. Common culprits: first layer and bed adhesion, wet filament, wrong temperature, flow or pressure advance, cooling, belts or eccentric nuts, partial nozzle clogs, and the wrong material for an enclosure. Change one variable at a time.

**Calibration**
Guide the test (temperature tower, flow, pressure advance, retraction, tolerance coupon, shrinkage). Record the result in `fabrication/calibration/<printer>-<filament>-YYYY-MM-DD.md`, and update the filament library row and the slicer profile.

## Write it down
- Per-part settings and history: `cad/<project>/print-settings.md` from `_templates/print-settings.md`. CAD source goes in `cad/<project>/source/`, print files (`.3mf`/`.stl`) in `cad/<project>/print/`. Don't commit `.gcode`; regenerate it from the 3MF.
- Lasting lessons (what fixed a failure, a new tolerance number): update `fabrication/filaments.md`, `docs/design-for-printing.md` or the printer file.
- New printers, slicers or materials: add them to the tech radar.

## Safety
- Don't leave a print unattended for long without a smoke alarm nearby. Thermal runaway protection must be on.
- ABS, ASA, PC and nylon give off fumes: use an enclosure and ventilate.
- Resin printers: nitrile gloves, ventilation, and cured waste only in the bin.
- Never print propellers or safety-critical load paths for anything that flies over people.
