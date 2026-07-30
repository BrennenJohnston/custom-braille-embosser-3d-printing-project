<!--- Open Source Assistive Technology Template: GitHub Build_Files/3D_Printing_Files/Embossing_Plates_Customizer Readme Version 1.2 (2025-Feb-04) --->

# Embossing Plates Customizer - Generate Your Own Braille

The Custom Braille Embosser is **content-agnostic**: the device itself does not encode any braille text. Each braille message is supplied by a matching pair of cylindrical 3D-printed plates - an **embossing plate** with raised dots and a **universal counter plate** with cavities. This folder contains everything you need to create those plates from your own text.

The companion folder [`Embossing_Plates_Examples/`](../Embossing_Plates_Examples) contains pre-generated 0.3 mm and 0.4 mm plate pairs that you can print before generating your own, to verify that the embosser and your printer are working correctly.

---

## Two ways to generate plates

There are two officially supported customizers. Use the **web-based customizer** unless you specifically need offline operation or to inspect/modify the OpenSCAD source.

### 1. Web-Based Customizer (PRIMARY - recommended for most users)

The browser-based generator is the **primary recommended workflow** for this project. It is the same tool demonstrated in **Video Tutorial 1** and gives you:

- **Automatic English -> Grade 1 / Grade 2 braille translation** (powered by the open-source [Liblouis](https://liblouis.io/) library, with 50+ language tables).
- **Live in-browser 3D preview** before you download.
- **Screen-reader-friendly UI** with adjustable font size, dark/light/high-contrast modes, and accessible controls. (For an even more accessible OpenSCAD experience, see [`openscad-assistive-forge`](https://github.com/BrennenJohnston/openscad-assistive-forge).)
- **No software install required** - works on any modern browser, including Chromebooks and tablets.
- **All STL generation runs locally in your browser** - your text is never uploaded to a server.

| Step | Action |
|---|---|
| 1. Open the web app | <https://braille-cylinder-stl-generator.vercel.app> |
| 2. Source repository | <https://github.com/BrennenJohnston/braille-cylinder-stl-generator> |
| 3. License (web app) | PolyForm Noncommercial 1.0.0 (free for personal, educational, and non-commercial use) |
| 4. Type your text, pick a translation table and grade, set card thickness | (see Video 1 walkthrough) |
| 5. Click **Generate**, preview, then **Download STL** | Repeat for **Embossing Plate** then **Universal Counter Plate** |

> **Detailed step-by-step walkthrough:** see Section 7.2 of the [Maker Guide](../../../Documentation/_drafts/Custom_Braille_Embosser_Maker_Guide.md), the transcript-backed write-up at [`Video_Tutorials/Custom_Braille_Embosser_Written_Tutorial.md`](../../../Video_Tutorials/Custom_Braille_Embosser_Written_Tutorial.md), or watch [Video 1 on YouTube](https://youtu.be/m71VNZq28MI).

### 2. OpenSCAD Customizer (ALTERNATIVE - offline / power-user)

If you need to work fully offline, want full parametric control over every dot dimension, or want to integrate plate generation into an existing OpenSCAD / CAD workflow, a copy of the OpenSCAD generator is included in [`OpenSCAD_Offline_Alternative/`](OpenSCAD_Offline_Alternative). See its [README](OpenSCAD_Offline_Alternative/README.md) for the full quick-start.

| Step | Action |
|---|---|
| 1. Translate your text to **Unicode braille** | <https://www.branah.com/braille-translator> (Grade 1 or Grade 2; output must be Unicode, not ASCII) |
| 2. Open the customizer in OpenSCAD | [`OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad`](OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad) |
| 3. Open the Customizer panel | View -> Customizer |
| 4. Paste braille into `Line_1`, `Line_2`, etc. | Pick `plate_type` (`Embossing Plate` or `Counter Plate`) and `paper_thickness_preset` (`0.4mm` or `0.3mm`) |
| 5. Render (F6) and export STL | File -> Export -> Export as STL. Repeat for the other plate. |
| 6. License (OpenSCAD customizer) | PolyForm Noncommercial 1.0.0 - see [`OpenSCAD_Offline_Alternative/LICENSE_PolyForm_Noncommercial_1.0.0.md`](OpenSCAD_Offline_Alternative/LICENSE_PolyForm_Noncommercial_1.0.0.md) |

The OpenSCAD copy in this folder mirrors version **2.2.1 (2026-05-30)** of the upstream repository [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) at the time of the v1.0.0 release of the embosser. For the latest version, see the upstream repo.

---

## Choosing between the two

| If you... | Use |
|---|---|
| Want the simplest, most beginner-friendly path | **Web-based customizer** (primary) |
| Don't already have OpenSCAD installed | **Web-based customizer** (primary) |
| Want automatic English->braille translation | **Web-based customizer** (primary) |
| Use a screen reader | **Web-based customizer** (primary) - or pair the OpenSCAD copy with [`openscad-assistive-forge`](https://github.com/BrennenJohnston/openscad-assistive-forge) |
| Need to work fully offline (no internet) | OpenSCAD alternative |
| Want full parametric control of every dot/spacing/cylinder dimension | OpenSCAD alternative |
| Want to inspect, modify, or extend the source code | OpenSCAD alternative |
| Already have an existing OpenSCAD / CAD workflow you want to integrate into | OpenSCAD alternative |
| Want to batch-generate many plates from a script | OpenSCAD alternative (drives via `openscad -D '...' -o out.stl`) |

Both customizers produce STL files that drop directly into the same Embosser Holder A1/A2 and Counter Holder B1/B2 sockets in the device body.

---

## Critical: match the card-stock thickness

Whichever customizer you use, **the embossing plate and the counter plate must be generated at the same paper-thickness setting** as the card stock you intend to emboss. Mismatching produces shallow, ill-formed dots or no dots at all.

| Plate-pair preset | Card stock | Approx. weight |
|---|---|---|
| `0.3mm` | 0.3 mm | ~110-130 lb / ~250-300 gsm |
| `0.4mm` | 0.4 mm | ~150 lb / ~350 gsm (typical business-card stock) |

> **Useful reuse tip from Video 1:** once you have printed a *universal counter plate* for a given thickness, you only need to print a new *embossing plate* when the text changes. The same counter plate can be reused with future embossing plates of the same thickness.

---

## Cross-references

- [Maker Guide - Section 7: Customization Guide](../../../Documentation/_drafts/Custom_Braille_Embosser_Maker_Guide.md) - full plate-generation workflow.
- [User Guide - Section 4: Compatibility](../../../Documentation/_drafts/Custom_Braille_Embosser_User_Guide.md) - swap plates after device is built.
- [Quickstart Guide - "To get a different message"](../../../Documentation/_drafts/Custom_Braille_Embosser_Quickstart_Guide.md) - 1-page condensed version.
- [Embossing_Plates_Examples/](../Embossing_Plates_Examples) - pre-generated 0.3 mm and 0.4 mm plate pairs to verify your printer.
- Companion repositories:
  - [`braille-cylinder-stl-generator`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator) - source of the web-based customizer (primary).
  - [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) - source of the OpenSCAD customizer (alternative).
  - [`openscad-assistive-forge`](https://github.com/BrennenJohnston/openscad-assistive-forge) - accessible browser UI for driving the OpenSCAD customizer.
