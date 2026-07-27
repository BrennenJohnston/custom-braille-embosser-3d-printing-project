# Thingiverse Listing - Custom Braille Embosser

> **Derived from:** [`Custom_Braille_Embosser_Publishing_Pack.md`](Custom_Braille_Embosser_Publishing_Pack.md). Edit the master pack first; re-derive this file.
> **Template:** follows Thingiverse's redesigned 2025/26 creation page (Summary → Print Settings → Post-Printing). The description does more work because Thingiverse does not auto-render the same level of structured detail as MakerWorld / Printables.

---

## A. Structured fields (paste into the Thingiverse upload form)

| Field | Value |
|---|---|
| Thing name | `Custom Braille Embosser - Hand-Operated 3D-Printable Braille Card Maker` |
| Designer / account | **Brennen Johnston** |
| Category | Tools (primary) or Education (secondary) |
| License | **Creative Commons - Attribution - NonCommercial - Share Alike (CC BY-NC-SA)** (closest single-pick match; full license split disclosed in the description) |
| Tags (~5-8, trim from baseline) | `braille`, `accessibility`, `assistive-technology`, `embosser`, `vision-impairment`, `business-card`, `educational`, `no-fasteners` |
| License visibility | Public |
| Cover image | `Photos/Custom_Braille_Embosser.jpg` |

**File upload groups:**

- **3D models:** 10 device STLs + 4 example plate STLs.
- **Supplementary downloads (attach in "Thing Files"):** the 2 `.3mf` files plus their companion slicer-settings markdown files, the BOM CSV, and the Maker Guide / User Guide / Quickstart Guide / Design Rationale / Summary (markdown for now; PDFs once exported - Publishing Pack Section 11, G1).

---

## B. Summary (paste into the Summary field)

I built this project because I couldn't find an affordable way to make small batches of custom braille business cards and short labels. Braille card embossers are hard to find, and the usual alternatives, like a slate and stylus, a Perkins-style brailler, or a fully electric embosser, are not ideal for quick, low cost custom runs. So I designed a fully 3D printed, hand operated embosser that just snaps together, with no fasteners, springs, glue, or electronics. I hope this helps someone!

The machine itself is simple. It's fully 3D printed, hand operated, and built from **10 snap fit parts with no fasteners, no springs, no glue, and no electronics**. The message lives on a separate embossing cylinder, paired with a matching counter cylinder. When the text changes, you should only need to print a new embossing cylinder. The recommended way to generate those cylinders is the browser based tool I created as a companion to this project. However, I've also created an OpenSCAD version which is included as the offline and power user backup.

**Who this helps:** blind and vision impaired users, sighted teachers, parents, and caregivers, schools, libraries, and nonprofits without a $1,500+ Perkins Brailler budget, and makers printing one for someone else.

### Generate custom plates (two ways)

**Primary - Web-based customizer (recommended):**

Open <https://braille-card-and-cylinder-stl-gener.vercel.app>, paste your text, pick the card thickness and translation table, click *Generate*, and download both STLs. The web app handles braille translation through [Liblouis](https://liblouis.io/), runs the STL generation **locally in your browser** so your text is not uploaded, and is screen-reader friendly.

**Backup - OpenSCAD offline alternative:**

> **The OpenSCAD customizer is the offline / power-user backup for anyone not wanting to, *or not able to*, use the browser-based tool.** That covers offline use, blocked-internet environments (school / library / corporate / government), screen-reader / accessibility-driven workflows that prefer a desktop application, and locked-down machines that can't run web apps.

A complete copy of the OpenSCAD generator is included as a supplementary download (and in the GitHub source repository) at `Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`. Requires [OpenSCAD](https://openscad.org/) 2024.x or newer. For an accessible browser UI on top of OpenSCAD, see [`openscad-assistive-forge`](https://github.com/BrennenJohnston/openscad-assistive-forge).

Two pre-generated example plate pairs (0.3 mm and 0.4 mm) are included so you can verify your printer before generating your own message.

### Two card-thickness presets

| Plate pair | Card stock | Approx. weight |
|---|---|---|
| `0.3mm` | 0.3 mm | ~110-130 lb / ~250-300 gsm |
| `0.4mm` | 0.4 mm (typical business-card stock) | ~150 lb / ~350 gsm |

> The plate pair **must** match the card-stock thickness. Mismatching produces shallow dots or no dots.

### What's in the download

- **10 device STLs** (Body Base, Body Top, Embosser Holder A1/A2, Counter Holder B1/B2, Grip Extension Bottom/Top, Handle Connector, Handle Grip).
- **4 example plate STLs** (embossing + counter, 0.3 mm and 0.4 mm pairs).
- **2 sliced Bambu `.3mf` profiles** as supplementary downloads (X1C all parts; X1C cylinder pair High Quality), each accompanied by a markdown transcription of its slicer settings.
- **Bill of Materials (CSV)** as a supplementary download.
- **Maker Guide / User Guide / Quickstart Guide / Design Rationale / Summary** in the repo now, with PDF exports planned before final packaging.
- **3 YouTube tutorials** linked below (Thingiverse auto-converts YouTube watch URLs into embeds).

### Source repository

<https://github.com/BrennenJohnston/custom-braille-embosser-3d-printing-project>

### Related earlier braille project

For background on my earlier braille teaching work published through WATAP:

<https://makerworld.com/en/models/254703-better-braille-alphabet-board-no-heading-title>

### Tutorial videos

https://www.youtube.com/watch?v=m71VNZq28MI
*(Tutorial 1 - Customizing braille, downloading STLs, 3D-print settings)*

https://www.youtube.com/watch?v=x-uPNtT2Gqk
*(Tutorial 2 - Assembling the 3D-printed parts)*

https://www.youtube.com/watch?v=77iXvJbkXh4
*(Tutorial 3 - Using the completed Custom Braille Embosser)*

### License (please read - this listing has a license split)

This is an open-hardware project. Multiple licenses apply by component:

- **Hardware**: **CERN-OHL-W v2**.
- **Documentation, photos, videos, written tutorials**: **CC BY-SA 4.0**.
- **Project software / scripts**: **GPL-3.0-or-later**.
- **Customizer software (deployed web app AND vendored OpenSCAD copy)**: **PolyForm Noncommercial 1.0.0** - free for personal, educational, and non-commercial use; commercial use is not permitted.

Thingiverse only allows a single license dropdown per listing. The closest umbrella match is **CC BY-NC-SA**. The per-component licenses above are the authoritative source.

### Credits

- Device designed by **Brennen Johnston**.
- Plate generator code from the companion projects [`braille-cylinder-stl-generator`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator) (web-based, primary) and [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) (OpenSCAD, alternative), also by Brennen Johnston.
- English -> braille translation by the open-source [Liblouis](https://liblouis.io/) library.
- Documentation template by **Makers Making Change / Neil Squire Society** (CC BY-SA 4.0): <https://github.com/makersmakingchange/OpenAT-Template>.

---

## C. Print Settings (paste into the Print Settings field)

**Printer brand / model:** Bambu Lab X1C (primary; sliced `.3mf` provided as supplementary download). Any FDM printer with a build volume ≥ 220 x 220 x 200 mm will work.

**Rafts:** No
**Supports:** Yes (only for overhangs >55° on Body Base / Body Top - tree / organic). **No supports on the cylinder plates.**
**Resolution:** 0.2 mm layer height
**Infill:** 30 % gyroid (PLA) or 20 % gyroid (PETG)
**Filament:** PLA Basic (default) or PETG. **~269 g per device** (8 h 44 min on Bambu Lab X1C with PLA Basic) + **~25 g per plate pair** (3 h 5 min on the same printer/material). Combined: ~293 g and ~11 h 49 min for one device + one plate pair.
**Brim:** 5 mm on Handle Grip + Handle Connector. **None on the cylinder plates.**
**Wall loops:** 3 for device parts. Use the **Arachne** wall generator for the cylinder plates.

### Notes (cylinder plates - tested Bambu Studio + X1C baseline)

```
Cylinder print settings (Bambu Lab X1C / Bambu Studio - tested baseline)

- Base preset: High Quality (or any sub-0.2 mm layer-height profile).
- Wall generator: Arachne (not Classic) - improves recessed-dot accuracy.
- Seam control: use Seam Painting on the indicator-letter / triangle area only,
  to keep the seam off the braille dots.
- Speeds (roughly half of Bambu Studio defaults):
    initial layer 40, infill 75, outer wall 50, inner wall 75, small perimeters 40
    (accelerations also halved).
- Supports: none.
- Brim: none.
- Material: basic PLA tested; PETG should also work with tuning.
- Measured on Bambu Lab X1C with PLA Basic from the included
  `Embossing and Counter Cylinder High Quality.3mf` profile:
    24.68 g, 8.14 m, ~$0.62 at $25/kg PLA, 3 h 5 min total
    (2 h 55 min printing + 9 min 40 s prep).
  ~1.5 h for a replacement embossing cylinder only (slice the
  embossing STL alone to confirm).

If clean dots come out at default speed on your printer, keep the faster settings.
If dots look fuzzy or under-extruded, slow the print as the first troubleshooting
step.

These settings are validated on Bambu Studio + X1C only. Cura / OrcaSlicer /
PrusaSlicer equivalents have not been tuned; adapt layer height, wall generator
(Arachne where supported), and the speed reductions to match.
```

### Tip - use the included `.3mf` files

Two pre-sliced Bambu Lab `.3mf` files are attached as supplementary downloads. Use them directly in Bambu Studio for the closest match to the tested results:

- `Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf` - Bambu X1C, all 10 device parts on one plate.
- `Embossing and Counter Cylinder High Quality.3mf` - Bambu X1C, cylinder pair only, High Quality settings.

A companion markdown file next to each `.3mf` (`Braille_Embosser_Assembly_Slicer_Settings.md` and `Embossing_Counter_Cylinder_HQ_Slicer_Settings.md`) transcribes every slicer setting in the profile for users who slice the STLs themselves.

---

## D. Post-Printing (paste into the Post-Printing field)

### Assembly (10-15 minutes, snap-fit, no tools)

1. Sort the printed parts. Identify each cylinder (embossing = raised dots; counter = recessed dots) and each holder pair by the **plus / X** mark (embossing side) vs the **minus** mark (counter side).
2. Snap each cylinder into its matching holder pair, lining up the triangle indicators. Lightly sand any over-tight surface.
3. Confirm: top and bottom triangles point at each other; side triangles mirror; embossing triangles right; counter triangles left.
4. (Optional) Snap the **Grip Extension** onto the user-side of the Body.
5. Drop both cylinder sub-assemblies into the Body Base. **Embossing-cylinder LEFT; counter-cylinder RIGHT.**
6. Snap on the Body Top.
7. Insert the **Handle Connector** (X-end into the embossing-cylinder holder).
8. Snap the **Handle Grip** over the connector.
9. Turn the handle a few times. It should feel a little stiff but not difficult.

Full walkthrough: [Tutorial 2 on YouTube](https://www.youtube.com/watch?v=x-uPNtT2Gqk).

### Use

1. Align indicator triangles so they point directly at each other (starting position).
2. Rotate the device so the rollers are horizontal.
3. Drop a sheet of **0.3 mm or 0.4 mm** card stock between the rollers (thickness must match the plate pair).
4. Turn the handle forward about a half turn. The braille is now permanent.
5. To change message: pull off the lid, swap in a new embossing cylinder, re-align triangles.

Full walkthrough: [Tutorial 3 on YouTube](https://www.youtube.com/watch?v=77iXvJbkXh4).

### Troubleshooting essentials

- **Dots too shallow** - Card thickness ≠ plate pair. Match 0.3 ↔ 0.3 / 0.4 ↔ 0.4.
- **Dots flat-topped** - Reprint cylinders using the settings block above.
- **Card tears** - Card too thin; use 0.3 mm or thicker.
- **Hard rotation** - Re-align triangles, embossing-left / counter-right.
- **Cylinders hard to swap** - Use a small flathead screwdriver carefully.
- **Holders rattle** - Reprint at 4 wall loops.
- **Handle slides off** - Reprint Handle Grip with +0.05 mm horizontal expansion.

### Card stock

- 0.3 mm card (~110-130 lb / ~250-300 gsm) with the 0.3 plate pair.
- 0.4 mm card (~150 lb / ~350 gsm; typical business-card stock) with the 0.4 plate pair.
- When gifting the embosser, include at least one printed plate pair plus a starter pack of card stock.

### Known limitations

- ~13 braille characters per line on the cylinder; trim long messages.
- Plate pair must match card thickness exactly.
- Print-settings baseline tested on Bambu Studio + X1C only.

### Further reading - attached as supplementary downloads

- `Custom_Braille_Embosser_Maker_Guide.pdf` *(once exported - Publishing Pack G1; markdown source on GitHub in the meantime)* - full build guide, slicer notes, assembly transcript.
- `Custom_Braille_Embosser_User_Guide.pdf` *(once exported)* - end-user manual.
- `Custom_Braille_Embosser_Quickstart_Guide.pdf` *(once exported)* - 1-page condensed user guide.
- `Custom_Braille_Embosser_Design_Rationale.pdf` *(once exported)* - why-the-design-is-this-way write-up.
- `Custom_Braille_Embosser_Summary.pdf` *(once exported)* - project summary.
- `Custom_Braille_Embosser_BOM.csv` - bill of materials (filament + card stock; no electronic parts).
