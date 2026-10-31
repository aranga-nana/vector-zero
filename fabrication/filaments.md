# Filament library

What works on our printers. Starting ranges are typical datasheet values. **Replace them with calibrated numbers** from `calibration/` as we prove them.

| Material | Brand / colour | Nozzle °C | Bed °C | Enclosure | Dry before use | Calibrated on | Good for | Notes |
|---|---|---|---|---|---|---|---|---|
| PLA | _generic starting point_ | 200–220 | 55–65 | No (door open) | Rarely | | Prototypes, jigs, fit tests | Softens around 55–60 °C: **not for cars, outdoors or near motors in Australian summer** |
| PETG | _generic_ | 230–250 | 70–85 | Optional | Yes, 65 °C for 4–6 h | | Functional parts, mild outdoor use | Stringy; sticks too well to PEI (use glue stick as a release layer) |
| ASA | _generic_ | 240–260 | 90–110 | **Yes** | Yes | | **Outdoor / UV parts, enclosures in the sun** | Fumes (styrene): ventilate. Better than ABS outdoors. |
| ABS | _generic_ | 240–260 | 95–110 | **Yes** | Yes | | Heat-resistant indoor parts | Fumes, warps; prefer ASA |
| TPU 95A | _generic_ | 220–240 | 40–60 | No | **Yes** | | Bumpers, gaskets, drone arm guards, antenna mounts | Slow (direct drive preferred); can jam in an AMS |
| PA-CF / PET-CF | _generic_ | 260–300 | 80–100 | Yes | **Always** | | Stiff, heat-resistant drone and robot parts | **Needs a hardened nozzle**; abrasive; very hygroscopic |
| PC | _generic_ | 260–300 | 100–120 | Yes | Yes | | High heat, tough | Hard to print; warps |

## Rules of thumb
- Australian heat: anything that lives in a car, outdoors or in direct sun gets **ASA, PETG or PC**, never PLA.
- Wet filament causes stringing, popping and weak parts. If in doubt, dry it.
- Carbon- and glass-filled filaments wear brass nozzles in hours. Use hardened steel or ruby.
