# Belt Cart Mod

A removable belt cartridge for Baby Panda. The whole belt assembly — rollers, rods,
bearings and drive motors — lifts out of the printer as one unit, so belt and bed
maintenance no longer means dismantling the machine.

Designed by **Chad Deitrich** ([@3DCreationsByChad](https://github.com/3DCreationsByChad)).

## Why

Two things it fixes:

1. **Tool-less service.** The roller holders stay tight to the belt, so the cartridge
   slides out without disassembly. Bed maintenance is four bolts a side.
2. **It fixes the bed sag** present in the original design.

## Printed parts

All eight are new. Print one of each — the left and right files are true mirrors,
not copies.

| Part | Qty | Size (mm) | Volume |
|---|---|---|---|
| `belt_cart_mod_adjustable_belt_motor_mount` L + R | 2 | 38 × 68.6 × 52 | 28.9 cm³ ea |
| `front_roller_arm_toolless_frame-side_part_1_front` L + R | 2 | 60 × 74.2 × 58.3 | 150.4 cm³ ea |
| `front_roller_arm_toolless_roller-side_part_2_front` L + R | 2 | 60 × 168.1 × 50.2 | 158.3 cm³ ea |
| `rear_bearing_holder_tool-less` L + R | 2 | 20 × 121.8 × 52 | 49.1 cm³ ea |
| `Baby_Panda_cart_mod_drill_jig` (tool, not part of the printer) | 1 | 55 × 80 × 55.8 | 101.8 cm³ |

**Material: roughly 442 g** for the eight parts at a typical 4-wall / 25% infill
(982 g if printed solid), plus ~130 g for the jig.

**Print settings: Voron standard.**

### Reused from the original design

The mod does **not** replace these — keep the ones you have:

- Front bearing holders (old style, L + R)
- Front and rear rollers

## Hardware

| Item | Spec |
|---|---|
| Front arms | 4 × M3×15 socket head screws + 4 × M3 heat-set inserts |
| Motor mounts | 4 screws with shims per mount |
| Frame / bed rail bolts | **M6 socket head cap screws** |
| Rods, front and rear | Ø8 × 300 mm |
| Rollers, front and rear | Ø57 × 230 mm |
| Bearings | 608 skateboard bearings (8 mm bore) |
| Drive motors | 2 × NEMA 17, **32 mm body** |
| Bed rails | **2 × 4040 × 350 mm extrusion** (4020/2040 works, 4040 is better) |
| Drive belt | GT2 closed loop, **200 mm × 6 mm** — 2 needed |
| Motor pulley | GT2 **20 tooth** — 2 needed |
| Roller pulley | GT2 **60 tooth** — 2 needed (3:1 reduction) |

Pulleys and belts come as one kit — e.g. a *GT2 20 & 60 tooth, 8 mm bore aluminium
set with 200 mm × 6 mm belts*. **You need two of each size**, one per side.

The 200 mm belt is corroborated by the CAD: measured centre distance between the motor
and roller pulleys is **56.87 mm**, which with 20T (Ø12.73 pitch) and 60T (Ø38.20 pitch)
gives a required belt of **196.6 mm**. The 3.4 mm difference is taken up by the
*adjustable* motor mount as tension.

⚠️ **Check your motor shaft diameter before ordering pulleys.** The common kit is
**8 mm bore**, while a standard NEMA 17 shaft is **5 mm**. Confirm which you have and
order the matching bore.

## Frame preparation

⚠️ **This mod requires drilling new through-holes in the sides of the frame** to mount
the dual bed rails.

Hole spec, from the counterbore drill used:

- **Through-hole: 6.5 mm**
- **Counterbore: 10 mm diameter × 13 mm deep**, to seat the M6 socket head

A printable drill jig is included (`Baby_Panda_cart_mod_drill_jig`). Measured features:

| Feature | Axis | Pattern |
|---|---|---|
| Ø9.60 × 4 | X | 20.00 × 19.80 mm rectangle |
| Ø5.20 × 2 (with Ø11.40 counterbore) | Z | 20.00 mm apart |
| Ø6.00 × 2 | Y | 50.80 mm apart |
| Ø6.40 × 2 | Y | 49.40 mm apart |

A step drill of the `HSS 10×6.5×13` type with a depth-stop collar cuts the through-hole
and the head cavity in one operation. ⚠️ The jig and that drill are **untested together**
— the original holes were marked and drilled freehand on a drill press.

## ⚠️ Compatibility

- **Not compatible with the old bed shield.**
- Requires new through-holes in the frame sides (above).
- Bed rails must be 4020/2040 minimum; 4040 recommended.

## Files

- `STEP/` — source geometry, one file per part
- `STLs/` — ready to slice

All eight printed parts and the jig were verified as single valid solids
(`BRepCheck_Analyzer`), and each left/right pair matches its mirror exactly in
bounding box and volume.
