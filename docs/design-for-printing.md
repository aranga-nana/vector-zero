# Design for 3D printing (FDM)

Practical rules for parts that print first time and survive real use. Replace the generic numbers here with ones measured on our printers (see `fabrication/calibration/`).

## Strength and orientation
- Parts are weakest **between layers**. Orient so the main load runs along the layers, not across them. Example: print a bracket on its side so the bending load doesn't peel layers apart.
- Walls beat infill for strength: 3–4 walls with 15–25 % infill is a good functional default. Raise walls before raising infill.
- Add fillets (≥1 mm) at inside corners that carry load.

## Tolerances (starting points, 0.4 mm nozzle)
| Fit | Clearance per side |
|---|---|
| Press / tight | 0.05–0.1 mm |
| Snug sliding | 0.15–0.2 mm |
| Free / loose | 0.3–0.4 mm |
| Holes | Print 0.1–0.2 mm oversize; small holes shrink. Drill or ream when it must be exact. |

Print a tolerance test coupon on each new printer + filament combination and record the result.

## Overhangs, bridges, supports
- Overhangs up to about 45° print without support. Chamfer instead of filleting downward-facing edges.
- Bridges up to about 10–20 mm are fine on a tuned printer.
- Design supports out: teardrop holes for horizontal holes, split parts, or flat-on-bed faces.

## Hardware
- **Heat-set inserts** (brass M2/M2.5/M3) for anything assembled more than once. Use the insert vendor's recommended hole size.
- Captive hex-nut pockets: about 0.2 mm clearance across flats.
- Screw directly into plastic only for low-cycle assemblies. Use a self-tapping screw for plastic.
- M3 is the default fastener for electronics enclosures and drone parts.

## Electronics enclosures
- Leave cable entry, USB access and a way to reach reset/boot buttons.
- Ventilation for regulators and MCUs. Linear regulators and ESP32s get warm in a sealed PLA box in summer.
- Use standoffs for PCBs (M2.5 for Raspberry Pi, M3 common elsewhere). Check the board's mounting-hole drawing.
- Outdoor: ASA or PETG, gasket groove for TPU seal or O-ring, drip loop, and cable glands. Face the vents downward.
- RF: plastic is transparent to Wi-Fi/LoRa, but keep antennas clear of metal, batteries and carbon-fibre filament (it's conductive and blocks RF).

## Drone and robot parts
- PLA is brittle and softens in the sun; avoid it for flying parts. TPU suits camera mounts, antenna holders and guards. PA-CF / PET-CF suits stiff structural parts.
- Never print props.
- Keep carbon-filled parts away from GPS and antennas.

## Before you print
- [ ] Wall thickness ≥ 2 × nozzle width
- [ ] Orientation chosen for strength and minimum supports
- [ ] Tolerances set for mating parts
- [ ] Material suits heat/UV/load (see `fabrication/filaments.md`)
- [ ] Fastener plan (inserts / nuts)
- [ ] Source CAD saved in `cad/<project>/source/`, print file in `cad/<project>/print/`
