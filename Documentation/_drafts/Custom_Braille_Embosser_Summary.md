# Custom Braille Embosser - Summary

> **Document version:** 1.0 | 2026-May-31
> **Designer:** Brennen Johnston
> **Repository:** https://github.com/BrennenJohnston/custom-braille-embosser-3d-printing-project

---

## Product Information

| Field | Value |
|---|---|
| Device name | Custom Braille Embosser |
| Version | V1.0.0 |
| Designer | Brennen Johnston |
| Release date | 2026-May-31 |
| Source license (hardware) | CERN-OHL-W v2 |
| Documentation license | CC BY-SA 4.0 |
| Software license | GPL-3.0-or-later |
| Repository | https://github.com/BrennenJohnston/custom-braille-embosser-3d-printing-project |
| MMC Library URL | *(to be assigned by MMC; placeholder `<MMCWebLink>`)* |

## Device Categories
- **Communication** ✓ (primary - written communication via braille)
- Mobility - no
- Recreation - no (could be used for recreational labelling, but not the primary use)

## Disability Types Served
- **Vision Impairment**
- **Blindness**

The Custom Braille Embosser also benefits sighted teachers, parents, and caregivers who need to produce braille labels and short braille messages without owning a $1,500+ commercial Perkins Brailler.

## User Value Statement
The Custom Braille Embosser gives a blind user, a vision-impaired user, or anyone supporting them, a way to produce permanent, raised, Grade-1 or Grade-2 braille on card stock for the price of a few grams of 3D-printer filament. The device:

- Is **fully 3D-printed** - no fasteners, no springs, no glue, no electronics, no PCB.
- Is **content-agnostic**: any message can be embossed by swapping in a different cylindrical embossing plate. Plates are produced from text by either of two officially supported customizers (see "How to Generate Plates", below).
- Costs about **$3-$6 USD of filament per device**, vs. $300-$1,500+ for commercial slate-and-stylus, hand-frame, or Perkins-style braille writers.
- Is **maker-friendly**: 10 STL parts, two pre-sliced `.3mf` profiles for the most common Bambu Lab printers, and three step-by-step video tutorials (hosted on YouTube and mirrored in this repo) covering customization, assembly, and use:
  - Video 1 - Customizing braille / downloading STLs / 3D-print settings: <https://youtu.be/m71VNZq28MI>
  - Video 2 - Assembling the 3D-printed parts: <https://youtu.be/x-uPNtT2Gqk>
  - Video 3 - Using the completed embosser: <https://youtu.be/77iXvJbkXh4>
- Is **repairable and remixable**: every parametric design file (`.f3z`, `.step`, `.obj`) is included, plus an offline copy of the OpenSCAD source for the plate generator vendored directly into this repo at `Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`.

## How to Generate Plates - Two Customizer Options

| Path | Best for | Where |
|---|---|---|
| **Primary - Web-based customizer** | Most users; auto-translates English to Grade 1 / Grade 2 braille (50+ languages); runs in any browser; screen-reader friendly; no install. | <https://braille-card-and-cylinder-stl-gener.vercel.app> |
| **Alternative - OpenSCAD (offline)** | Offline use; full parametric control; existing OpenSCAD/CAD workflows. Vendored in this repo. | [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative) |

A side-by-side comparison and full quick-start steps for both options are kept in [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/README.md`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/README.md).

## How to Use (Short)
1. Generate the embossing-plate / counter-plate pair for the message you want to emboss (web-based customizer recommended; OpenSCAD alternative available - see "How to Generate Plates" above), or use one of the included pre-generated example pairs in `Build_Files/3D_Printing_Files/Embossing_Plates_Examples/`.
2. Print the 10 device parts and the 2 plate parts on any FDM 3D printer.
3. Snap the device together (no tools, no fasteners).
4. Insert the embossing plate into the Body Base (held by Embosser Holder A1/A2) and the counter plate into the Body Top (held by Counter Holder B1/B2).
5. Insert a sheet of card stock (0.3 mm or 0.4 mm) between the plates.
6. Squeeze the handle to roll the plates over the card. The dots are now permanent.
7. Remove the card. Re-feed for additional lines if needed.

Detailed step-by-step instructions are in the [User Guide](Custom_Braille_Embosser_User_Guide.pdf), and a 1-page summary is in the [Quickstart Guide](Custom_Braille_Embosser_Quickstart_Guide.pdf).

## Estimated Cost
| Cost component | Estimate (USD) |
|---|---|
| Filament for the device (10 parts, **268.81 g** measured from the included X1C + PLA Basic profile) | **~$6.72** |
| Filament for one pair of plates (Embossing + Counter, **24.68 g** measured from the included cylinder HQ profile, X1C + PLA Basic) | **~$0.62** |
| Card stock (per sheet, 0.3 mm or 0.4 mm) | **~$0.15 - $0.20** |
| Off-the-shelf parts | **$0.00 (none)** |
| **Total per device + one plate pair** | **~$7.34** |

> Device and plate-pair mass / time figures are taken from the Bambu Studio slicer reports for the two included `.3mf` profiles on a Bambu Lab X1C with Bambu Lab PLA Basic: `Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf` (258.79 g model + 10.02 g support = 268.81 g, 8 h 44 min total) and `Embossing and Counter Cylinder High Quality.3mf` (24.68 g, no supports, 3 h 5 min total). All cost figures use the Bambu Studio default $25/kg PLA reference.

## Attribution
- Device designed by **Brennen Johnston**.
- Cylindrical embossing-plate and counter-plate generator code (used to produce the example plates included in this repo, and vendored locally at `Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`) is from the companion projects [`braille-cylinder-stl-generator`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator) (web-based, primary) and [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) (OpenSCAD, alternative), also by Brennen Johnston. The web app's English -> braille translation is powered by the open-source [Liblouis](https://liblouis.io/) library.
- Documentation template by **Makers Making Change / Neil Squire Society**, used under CC BY-SA 4.0: https://github.com/makersmakingchange/OpenAT-Template

## Maker Information
| Field | Value |
|---|---|
| Total estimated print time | ~12-18 h on a Bambu Lab X1C at 0.2 mm layer height (verify against final slicer report) |
| Total assembly time | ~10-15 minutes (snap-fit, no fasteners) |
| Skills required | Beginner-level FDM 3D printing; ability to remove parts from a build plate |
| Tools required | FDM printer, slicer (Bambu Studio recommended). Optional: deburring tool / hobby knife. |
| Off-the-shelf parts required | None |
| Soldering / wiring required | None |
