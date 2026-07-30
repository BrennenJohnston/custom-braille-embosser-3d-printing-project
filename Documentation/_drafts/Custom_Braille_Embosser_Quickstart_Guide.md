# Custom Braille Embosser - Quickstart Guide

> **Document version:** 1.0 | 2026-May-31
> **Designer:** Brennen Johnston
> **For:** end users who already have an assembled embosser. **1-2 page condensed version of the full User Guide.**

---

## What you have

A small, hand-operated, fully 3D-printed braille embosser. You squeeze the handle, and a sheet of card is rolled between two plates that press permanent, raised braille dots into it.

## What you need

1. The assembled Custom Braille Embosser (in your hand).
2. A pair of printed cylindrical plates (an *embossing plate* with raised dots + a matching *counter plate*).
3. **Card stock** matching the plate pair: **0.3 mm** for the 0.3 plate set, **0.4 mm** for the 0.4 plate set.

## Five-step use

> **Prefer a video?** Watch Video 3 - "Using the completed Custom Braille Embosser": <https://youtu.be/77iXvJbkXh4>

1. **Align** the indicator triangles on both cylinders so they point directly at each other. This is the starting position.
2. **Rotate** the embosser so the rollers are horizontal, then orient the card so it feeds left-to-right with the printed side facing up in the direction the triangles point.
3. **Insert** the card by dropping it gently between the rollers and checking that it sits level.
4. **Turn** the handle forward about a half turn. If needed, rock it slightly back and forth before the last dot to finish the embossing.
5. **Roll through** the rest of the card and pull it out. The braille is now permanent.

Repeat steps 1-5 to emboss more cards. Do not roll too far past the last dot while checking the embossing or the print may shift out of alignment.

## To get a different message

Generate a new plate pair from text using one of the two officially supported customizers. For most users, the web-based customizer is the easiest:

- **Primary (web-based, recommended):** open <https://braille-cylinder-stl-generator.vercel.app>, type your text, choose a translation table and card thickness, click Generate, and download the STLs. Auto-translates English to Grade 1 / Grade 2 braille; runs entirely in your browser. (Same tool as in [Video 1](https://youtu.be/m71VNZq28MI).)
- **Alternative (OpenSCAD, offline):** included in this repo at [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad`](../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad). Requires [OpenSCAD](https://openscad.org/) and a manual one-time translation step at <https://www.branah.com/braille-translator>. Use this if you need to work offline or want full parametric control.

Print both new plates, or print only a new embossing plate if you are reusing the same card thickness and already have the matching universal counter plate.

## To change cylinders

1. Pull the lid off the embosser. The handle can stay attached.
2. Remove the current cylinder pair and insert the replacement pair.
3. If new cylinders are tight in the base, carefully loosen them with a small flathead screwdriver.
4. Re-align the indicator triangles before embossing.

## Care

- Store at room temperature, out of direct sunlight.
- Wipe plates with a dry, soft cloth between sessions.
- If a part cracks: re-print it from the STL files in `Build_Files/3D_Printing_Files/STL/`.

## When something goes wrong

| Symptom | Quick fix |
|---|---|
| Dots too shallow | Wrong card thickness for these plates - match 0.3 plate pair with 0.3 card, 0.4 with 0.4. |
| Card tears | Card too thin - use 0.3 mm or 0.4 mm card stock. |
| Print is skewed | Re-start with the indicator triangles aligned and stop checking before you pass the last dot. |
| Holders rattle | Snap them back into place; if loose, re-print at higher wall count. |
| Handle slides off | Reprint Handle Grip with +0.05 mm horizontal expansion. |

For more detail, see the [User Guide](Custom_Braille_Embosser_User_Guide.pdf).
