# Peltier-Wrist-Cooler
Battery-powered wearable Peltier cooling band for the inner wrist. Custom 3D-printed enclosure, CAD source and full build documentation. Inspired by Tolga Özuygur's personal air conditioner project.

# WristChill — Wearable Peltier Wrist Cooler

A self-contained, battery-powered thermoelectric cooling band worn on the inner wrist.
Fully custom mechanical design, 3D-printed enclosure, and assembly documentation.

> **Attribution / Inspiration**
> The concept of a wrist-worn Peltier cooling band comes from the Turkish maker and YouTuber
> **Tolga Özuygur** ([@tolgaozuygur](https://github.com/tolgaozuygur)) and his "personal air
> conditioner" build. This repository is **not** a copy, fork, or re-upload of his work:
> every CAD part, dimension, mounting scheme and assembly step here was designed from
> scratch by me. Credit for the original idea belongs to him.
> Original video: <!-- TODO: paste the YouTube link here -->

---

## Why it works

Cooling the inner wrist cools blood passing close to the skin surface and triggers a
disproportionately strong *perceived* whole-body cooling effect — the same reason a cold
compress goes on the wrists and forehead. This device does **not** cool the room; it
changes how cold the wearer feels.

A Peltier (thermoelectric) module is the core: apply DC current and one face drops below
ambient while the opposite face heats up. The cold face contacts the wrist; the hot face
is bonded to a heatsink and force-cooled by a 5 V axial fan. If the hot side is not
removed effectively, the cold side stops being cold — heat rejection is the whole
engineering problem here.

## Hardware

| Part | Spec | Notes |
|---|---|---|
| Thermoelectric module | <!-- TODO: e.g. TEC1-12706, 40×40 mm --> | Cold face toward wrist |
| Heatsink | <!-- TODO: dimensions --> | Bonded with thermal paste |
| Fan | 5 V DC, 40×40 mm axial | Exhausts hot-side air |
| Battery | <!-- TODO: chemistry, cells, mAh --> | Housed in left enclosure |
| Switch | Rocker SPST | Main power cutoff |
| Secondary switch | <!-- TODO: what does it control? --> | |
| Strap | Velcro, <!-- TODO: width --> mm | |
| Fasteners | M3 screws + heat-set inserts | |

### Wiring

<!-- TODO: add a simple schematic or a wiring description.
     State the supply voltage, whether the TEC and fan share a rail,
     and any current limiting / protection used. -->

## Mechanical design

The enclosure is a three-body split: two side boxes (battery and switching) flanking a
central TEC/heatsink/fan stack, joined by hinge-style pin bosses so the assembly conforms
to the curvature of the wrist instead of sitting flat on it.

- Printed grille over the fan intake — finger and cable protection, minimal airflow loss
- Heat-set insert bosses rather than self-tapping screws into plastic
- Cold-face window on the underside for direct skin contact

**CAD:** designed in Shapr3D. Source and export files in [`/cad`](./cad).

### Printing

| Setting | Value |
|---|---|
| Material | <!-- TODO: PLA / PETG? --> |
| Layer height | <!-- TODO --> |
| Walls / infill | <!-- TODO --> |
| Supports | <!-- TODO --> |

> **Material note:** the hot side of a TEC can reach temperatures where PLA softens.
> If the heatsink mount is printed in PLA, monitor it — PETG or ABS is the safer choice
> for any part in the hot-side thermal path.

## Repository layout

```
/cad        Shapr3D source + STEP exports
/stl        Print-ready meshes
/docs       Assembly photos and notes
/bom        Bill of materials
```

## Assembly

<!-- TODO: numbered steps. Cover at minimum:
     1. Heat-set inserts into the enclosure bosses
     2. Thermal paste + TEC-to-heatsink bonding, correct polarity/orientation
     3. Fan mounting and airflow direction
     4. Wiring and switch installation
     5. Battery placement and closing the shells -->

## Safety and limitations

- **This is a prototype, not a medical or safety device.** Do not use it to treat heat
  exhaustion, fever, or any medical condition.
- Prolonged skin contact with a sub-ambient surface can cause cold injury. Limit
  continuous wear and remove the device if the skin becomes numb or painful.
- The hot side gets genuinely hot. Do not obstruct the fan or the exhaust path.
- Peltier modules are electrically inefficient — expect short runtimes relative to
  battery size. Measured runtime: <!-- TODO -->
- Measured wrist-side surface temperature vs. ambient: <!-- TODO -->

## Status

<!-- TODO: e.g. "v1 assembled and functional; v2 planned with temperature feedback." -->

## License

Hardware designs (CAD, STL): [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
Any code in this repository: MIT

## Credits

- Original concept: **Tolga Özuygur**
- Mechanical design, CAD, build and documentation: **Ali** <!-- TODO: GitHub handle -->
