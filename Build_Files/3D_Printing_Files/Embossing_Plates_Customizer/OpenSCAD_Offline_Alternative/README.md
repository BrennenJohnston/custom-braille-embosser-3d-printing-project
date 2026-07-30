# OpenSCAD Offline Alternative - Embossing Plate Customizer

> **This is the *alternative* path.** The **primary recommended workflow** for the Custom Braille Embosser is the web-based customizer at <https://braille-cylinder-stl-generator.vercel.app>. Use this OpenSCAD version only if you need to work offline, want full parametric control, or want to inspect/modify the source. See the [parent README](../README.md) for a side-by-side comparison.

This folder contains a verbatim copy of the OpenSCAD parametric braille-cylinder generator at the time of the v1.0.0 release of the Custom Braille Embosser, vendored here so the embosser project is fully usable without an internet connection. It is the same script demonstrated in **Video Tutorial 1** (alongside the web app).

The upstream repository is [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad). For the latest version, bug fixes, and the full automated test suite, refer to the upstream repository.

> **Note on names.** Upstream was called `braille-stl-generator-openscad` when
> this snapshot was taken, so the copied `.scad` and `docs/` files in this folder
> still say that. Those files are left byte-faithful to the v2.2.1 tree on
> purpose; GitHub redirects the old URLs. Only this wrapper README, which is
> written by the embosser project rather than copied, uses the current name.
> The web app's address moved as well: the copied files point at the old
> `braille-card-and-cylinder-stl-gener.vercel.app` address, which still resolves
> but no longer receives updates. The current address is
> <https://braille-cylinder-stl-generator.vercel.app>. Refreshing this snapshot
> to a newer upstream release is what will correct it inside the copied files.

| Field | Value |
|---|---|
| Vendored from | [`BrennenJohnston/braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) (named `braille-stl-generator-openscad` at the time) |
| Vendored version | 2.2.1 (2026-05-30) — with one project-local modification, see [Project-local modifications](#project-local-modifications) below |
| License | [PolyForm Noncommercial 1.0.0](LICENSE_PolyForm_Noncommercial_1.0.0.md) |
| Maintainer | Brennen Johnston |
| Required software | [OpenSCAD](https://openscad.org/) 2024.x or newer (2026.01.03 or newer recommended) |

> **License note for makers:** The Custom Braille Embosser device itself is released under CERN-OHL-W v2 (hardware) + CC BY-SA 4.0 (documentation) + GPL-3.0-or-later (software). This OpenSCAD generator is a *separately licensed* component, distributed under the **PolyForm Noncommercial 1.0.0** license: free for personal, educational, and non-commercial use; modification and remixing allowed; **no commercial use permitted**. If you intend a commercial use case for the *generator*, contact the upstream maintainer or use the web-based customizer (which is also PolyForm Noncommercial - same constraint).

---

## Files in this folder

| File | Purpose |
|---|---|
| `Braille_Cylinder_STL_Generator.scad` | Main customizer script. Open this in OpenSCAD. |
| `presets.scad` | Preset value tables (0.3 mm and 0.4 mm presets) - included by the main file. |
| `CHANGELOG.md` | Upstream changelog at the time of vendoring. |
| `LICENSE_PolyForm_Noncommercial_1.0.0.md` | License terms for this generator. |
| `docs/PARAMETER_MAPPING.md` | How OpenSCAD parameters correspond to the web UI controls. |
| `docs/WEB_TO_OPENSCAD_PORTING_GUIDE.md` | Comprehensive porting / deep-dive notes. |
| `docs/OPENSCAD_COORDINATE_SYSTEM_SPECIFICATIONS.md` | Coordinate-system reference. |
| `MakerWorld_Upload/` | Single-file, flattened build of the generator for upload to [MakerWorld's Parametric Model Maker](https://makerworld.com/) (which accepts only one `.scad` file and does not support local `include` directives). Use the canonical dual-file version above for everything else. See [`MakerWorld_Upload/README.md`](MakerWorld_Upload/README.md). |

---

## Quick start

### Step 1 - Translate your text to Unicode braille

The OpenSCAD customizer **requires pre-translated Unicode braille input** - it does *not* automatically translate English to braille (the web app does, via Liblouis).

1. Open <https://www.branah.com/braille-translator>.
2. In the options panel, select your desired braille grade:
   - **Grade 2 (contracted)** - recommended for most uses.
   - **Grade 1 (uncontracted)** - for names, emails, or when contractions cause confusion.
3. Make sure **Unicode Braille** is selected (NOT ASCII Braille).
4. Type your English text on the left.
5. Copy the braille output from the right (you'll see Unicode characters like `⠓⠑⠇⠇⠕`).

> **Tip:** for critical content, cross-check the translation with another braille translator or a braille specialist before printing.

### Step 2 - Open the customizer

1. Install OpenSCAD from <https://openscad.org/> if you don't already have it.
2. Open `Braille_Cylinder_STL_Generator.scad` in OpenSCAD.
3. Open the **Customizer panel**: View -> Customizer.

### Step 3 - Configure

In the Customizer panel:

1. **Text Input - Pre-Translated Braille**
   - Paste the Unicode braille from Branah into `Line_1`. Use `Line_2` through `Line_4` for additional lines.
2. **Plate Selection**
   - Set `plate_type` to `Embossing Plate` (the one with raised dots) or `Counter Plate` (the one with cavities).
3. **Paper Thickness Preset**
   - Set `paper_thickness_preset` to `0.4mm` (recommended for typical business-card stock) or `0.3mm` (recommended for thinner card stock).
   - The preset adjusts ~23 parameters at once (spacing, dot dimensions, cylinder settings) to match the web app's "Card Thickness" dropdown. Use `Custom` only if you want to override individual parameters.
4. (Optional) **Expert Mode** sub-menus
   - Shape Selection (rounded vs. cone dots, indicator triangles on/off)
   - Cylinder Dimensions (diameter, height, polygonal cutout)
   - Braille Spacing (cells per row, line / dot spacing, vertical adjustment)
   - Braille Dot Adjustments (per-shape dimensions for embossing dots and counter recesses)
5. **Rendering Quality**
   - `Medium` is a good default. Use `High` only when exporting the final STL.

### Step 4 - Render and export

1. Press **F6** (or Design -> Render) to compute the final mesh. This can take 30 seconds to several minutes depending on rendering quality.
2. **File -> Export -> Export as STL...** and save with a descriptive filename, for example:
   - `Embossing_Plate_<your-message>_0.4mm.stl`
   - `Universal_Counter_Plate_0.4mm.stl`
3. Repeat the configure-render-export cycle for the other plate (the `plate_type` you didn't pick the first time).

### Step 5 - Print and use

Print both STL files on the same FDM printer you used for the device parts (~1.5-3 hours for a plate pair on a Bambu Lab X1C, per Video 1). Then follow the [User Guide](../../../../Documentation/_drafts/Custom_Braille_Embosser_User_Guide.md) to install and use them.

> **Slicer settings recommendation from Video 1 (X1C / Bambu Studio):** start from a *High Quality* (sub-0.2 mm) preset, switch the wall generator from *Classic* to *Arachne*, use *Seam Painting* to place seams only on the indicator letters / triangle area (not on the braille dots), and roughly halve the default speeds. Supports and brim are not needed in the demonstrated workflow.

---

## What the OpenSCAD customizer makes

| Output | When to use it |
|---|---|
| **Cylinder Embossing Plate** (raised dots on outer surface) | The plate that physically forms the braille dots in the card. Must be matched to the card thickness. |
| **Cylinder Counter Plate** (recessed dots on outer surface) | The "anvil" that the embossing plate presses card stock into. Universal across messages of the same card thickness. |

Both plates fit into the holder pairs in the embosser body:

- **Embossing Plate -> Embosser Holder A1 + A2** (plus-marked / X-marked side, embosser's left side)
- **Counter Plate -> Counter Holder B1 + B2** (minus-marked side, embosser's right side)

---

## Default settings

All defaults match the web app's **0.4 mm Paper Thickness Preset** (applied on load):

### Cylinder
- Diameter: 30.8 mm
- Height: 52 mm
- Polygonal cutout: 13 mm radius, 12 sides
- Seam offset: 0 deg

### Braille grid
- Cells per row: 11 (with 2 additional cells reserved when indicators are on)
- Number of rows: 4
- Cell spacing: 6.5 mm
- Line spacing: 10.0 mm
- Dot spacing: 2.5 mm

### Default dot shape
- `dot_shape = "Cone"` (project-local override; see [Project-local modifications](#project-local-modifications) below). Switchable to `"Rounded"` via the Customizer dropdown.

### Cone dot dimensions (0.4 mm preset, default shape)
- Base diameter: 1.5 mm | height: 0.8 mm | flat hat: 0.4 mm

### Counter plate cone recess (0.4 mm preset, default shape)
- Base diameter: 1.9 mm | height: 0.7 mm | flat hat: 1.0 mm

### Rounded dot dimensions (0.4 mm preset, alternative shape)
- Base diameter: 1.5 mm | base height: 0.5 mm
- Dome diameter: 1.0 mm | dome height: 0.5 mm

### Counter plate bowl recess (0.4 mm preset, alternative shape)
- Base diameter: 1.8 mm | depth: 0.8 mm

The full parameter list, including the Cone-shape variants, is documented in [`docs/PARAMETER_MAPPING.md`](docs/PARAMETER_MAPPING.md).

---

## Project-local modifications

This folder is otherwise a verbatim vendored snapshot of upstream [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) v2.2.1, with **one intentional, project-local modification** so the defaults match this embosser project's recommended workflow:

| Parameter | Upstream default | Project-local default | Files affected |
|---|---|---|---|
| `dot_shape` | `"Rounded"` | `"Cone"` | `Braille_Cylinder_STL_Generator.scad` (line ~102), `MakerWorld_Upload/Braille_Cylinder_STL_Generator_MakerWorld.scad` (corresponding line), `docs/PARAMETER_MAPPING.md` ("Default shape" line in the "Default Values Alignment" section) |

### Why

The Cone dot shape is the recommended default for this embosser device because it prints more reliably across the FDM hardware/slicer combinations this project targets (the upstream generator targets a broader audience; "Rounded" remains a valid choice for users who prefer that haptic). The dropdown still exposes both options — only the *initial* selected value changed.

### Maintainer: preserving this change on re-vendor

When pulling a newer upstream snapshot of `Braille_Cylinder_STL_Generator.scad` / `presets.scad`:

1. Copy the new upstream files into this folder.
2. Re-apply this single edit to the new `Braille_Cylinder_STL_Generator.scad`: change `dot_shape = "Rounded";` to `dot_shape = "Cone";` (and keep the `// PROJECT-LOCAL DEFAULT` comment above it so the next maintainer sees it).
3. Re-flatten `MakerWorld_Upload/Braille_Cylinder_STL_Generator_MakerWorld.scad` per [`MakerWorld_Upload/README.md`](MakerWorld_Upload/README.md#maintainer-re-flatten-procedure) — since that procedure starts by copying the (now-edited) desktop main file, the `dot_shape = "Cone"` default flows through automatically.
4. Re-verify the "Default shape" line in `docs/PARAMETER_MAPPING.md` still reads "Cone" after any docs re-vendor.

> The preset *values* (PRESET_04, PRESET_03) are intentionally NOT modified — they have been verified byte-identical to upstream, and that lockstep with the upstream web app's `THICKNESS_PRESETS` is what the upstream's own comments require.

---

## Troubleshooting

### "INVALID CHARACTERS" warning rendered above the cylinder
- You pasted regular English text instead of Unicode braille.
- **Fix:** re-translate at <https://www.branah.com/braille-translator>, ensure **Unicode Braille** (NOT ASCII) is selected, and copy the braille output again.

### "TEXT TOO LONG" warning rendered above the cylinder
- A line is longer than the available cells.
  - Capacity = `grid_columns` when indicators are off
  - Capacity = `grid_columns - 2` when indicators are on (col 0 and col -1 are reserved for the alignment markers).
- **Fix:** shorten the line, increase `grid_columns`, or turn `indicators` off.

### Dots don't align between the two plates
- Confirm both plates were generated at the **same** `paper_thickness_preset`.
- Confirm both plates use the same `dot_shape` (`Rounded` vs `Cone`).
- Confirm both plates use the same `indicators` setting (`On` vs `Off`).
- For minor vertical offset adjustments, use `braille_y_adjust`. For angular offset around the cylinder, use `seam_offset_degrees`.

### Render is taking too long
- Set `render_quality` to `Low` while you're iterating; switch to `Medium` or `High` only for the final export.

### Cylinder is too thick or too thin
- Adjust `cylinder_diameter_mm` (default 30.8 mm) - but note that the embosser's holder pair is dimensioned for 30.8 mm and may not accommodate large changes without recompiling the device CAD.

---

## Going further

- **For an accessible (screen-reader-friendly) browser UI on top of this OpenSCAD generator:** use [`openscad-assistive-forge`](https://github.com/BrennenJohnston/openscad-assistive-forge).
- **For the latest version, automated tests, and additional documentation:** visit the upstream repository [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad).
- **For the web-based version (no install required, automatic translation):** <https://braille-cylinder-stl-generator.vercel.app>.

---

## License recap

This OpenSCAD generator is licensed under **PolyForm Noncommercial 1.0.0**. See [`LICENSE_PolyForm_Noncommercial_1.0.0.md`](LICENSE_PolyForm_Noncommercial_1.0.0.md) for full terms.

- Free for personal, educational, and non-commercial use.
- Modification and remixing allowed.
- No commercial use.

For the rest of the Custom Braille Embosser project (device CAD, build files, documentation), the licenses are CERN-OHL-W v2 (hardware), CC BY-SA 4.0 (documentation), and GPL-3.0-or-later (software). Those terms do *not* extend to this folder; use of files in this folder is governed by the PolyForm Noncommercial license referenced above.
