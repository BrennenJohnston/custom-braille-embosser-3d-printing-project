# MakerWorld Upload — Single-File OpenSCAD Build

This subfolder contains a **single-file, flattened** copy of the braille cylinder generator, prepared specifically for upload to **[MakerWorld's Parametric Model Maker](https://makerworld.com/)**. It exists for one reason only: MakerWorld accepts exactly one `.scad` file per parametric model and does **not** support local `include <...>` directives.

> **If you are not uploading to MakerWorld, use the [canonical dual-file desktop version](../) one folder up instead.** The dual-file version is easier to maintain and is what the project's documentation and tutorial videos refer to.

| Field | Value |
|---|---|
| Files in this folder | `Braille_Cylinder_STL_Generator_MakerWorld.scad`, `README.md` |
| Source of truth | [`../Braille_Cylinder_STL_Generator.scad`](../Braille_Cylinder_STL_Generator.scad) + [`../presets.scad`](../presets.scad) |
| License | [PolyForm Noncommercial 1.0.0](../LICENSE_PolyForm_Noncommercial_1.0.0.md) (unchanged) |
| Required software (desktop preview) | [OpenSCAD](https://openscad.org/) 2021.x or newer |
| Target platform | [MakerWorld Parametric Model Maker](https://makerworld.com/) |

---

## Why this file exists (background)

The desktop main file [`../Braille_Cylinder_STL_Generator.scad`](../Braille_Cylinder_STL_Generator.scad) pulls in `../presets.scad` via:

```
include <presets.scad>;
```

`presets.scad` defines the `PRESET_04` and `PRESET_03` lookup tables plus the `preset_lookup(...)` / `preset_value(...)` helper functions used by every `_preset_*` variable at the top of the main script. MakerWorld's Parametric Model Maker only receives the one file you upload, so any reference to `presets.scad` resolves to "unknown function" / "undefined variable" errors *before* the customizer UI can render — which the upload UI surfaces as "not compatible".

To work around this, `Braille_Cylinder_STL_Generator_MakerWorld.scad` is a **byte-identical** copy of the desktop main file with one targeted edit: the `include <presets.scad>;` line has been replaced inline with the body of `presets.scad`. The inlined content lives inside the *existing* `/* [Hidden] */` block, so MakerWorld's customizer UI renders exactly the same set of controls (and only the same set of controls) as desktop OpenSCAD does.

The inlined region is clearly delimited:

```
// ==== BEGIN inlined from presets.scad (MakerWorld single-file requirement) ====
... (lines 38..147 of presets.scad: /* [Hidden] */, PRESET_04, PRESET_03, preset_lookup, preset_value) ...
// ==== END inlined from presets.scad ====
```

---

## How to upload to MakerWorld

1. Sign in to <https://makerworld.com/> and open the **Parametric Model Maker** ("Create" → "Parametric Model" / "Custom Model").
2. Upload `Braille_Cylinder_STL_Generator_MakerWorld.scad`. MakerWorld auto-detects it as a parametric OpenSCAD model and exposes a **Customize** button.
3. In the Customizer panel that appears, use the same parameter sections you would in desktop OpenSCAD:
   - **Text Input - Pre-Translated Braille** — paste Unicode braille from <https://www.branah.com/braille-translator> (the OpenSCAD build does **not** translate English to braille; see the [parent README](../README.md#step-1---translate-your-text-to-unicode-braille) for the full Branah workflow).
   - **Plate Selection** — `Embossing Plate` (raised dots) or `Counter Plate` (recesses).
   - **Paper Thickness Preset** — `0.4mm`, `0.3mm`, or `Custom`.
   - **Expert Mode** sub-sections (shape, cylinder dimensions, spacing, dot adjustments).
   - **Rendering Quality** — leave on `Medium` while iterating; switch to `High` for the final render.
4. Click **Render** / **Generate** to produce the STL inside MakerWorld, then publish or download as you would for any other parametric model.

> For everything else (translating text, choosing card thickness, slicer settings for printing the resulting plates), follow the [parent README](../README.md) — it applies in full.

---

## Maintainer: re-flatten procedure

When [`../Braille_Cylinder_STL_Generator.scad`](../Braille_Cylinder_STL_Generator.scad) and/or [`../presets.scad`](../presets.scad) are re-vendored from the upstream repository [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad), regenerate this file with a simple manual flatten — no scripts required:

1. **Copy** `../Braille_Cylinder_STL_Generator.scad` over `./Braille_Cylinder_STL_Generator_MakerWorld.scad`.
2. **Restore the header note** at the top of the file documenting that this is the MakerWorld single-file build and pointing back to the dual-file canonical version (see the existing `// MAKERWORLD SINGLE-FILE BUILD` section near the top).
3. **Find** the one `include <presets.scad>;` line (currently around line 163 of the desktop main file, inside the `/* [Hidden] */` block).
4. **Replace** that single line with everything from line 38 through line 147 of the new `../presets.scad` (the `/* [Hidden] */` marker, the `PRESET_04` table, the `PRESET_03` table, and the `preset_lookup` / `preset_value` function definitions), wrapped in the sentinel comments:

   ```
   // ==== BEGIN inlined from presets.scad (MakerWorld single-file requirement) ====
   ... (paste presets.scad lines 38..147 here) ...
   // ==== END inlined from presets.scad ====
   ```

5. **Verify** in desktop OpenSCAD: open `Braille_Cylinder_STL_Generator_MakerWorld.scad`, press **F5** for preview — the geometry should render identically to the dual-file version. Toggle `paper_thickness_preset` between `0.4mm`, `0.3mm`, and `Custom` and confirm dot sizes change in preview.
6. **Verify** on MakerWorld: upload the file, open the Customizer, confirm all dropdowns and sliders appear in the same sections as desktop OpenSCAD (`Text Input - Pre-Translated Braille`, `Plate Selection`, `Paper Thickness Preset`, the four `Expert Mode - *` sections, `Rendering Quality`).

### Why no flatten script?

The re-flatten step is a single search-and-replace of one line, only needed when upstream `presets.scad` changes (rarely). A Python flatten script would add tooling overhead disproportionate to the benefit for the vendored-snapshot model this project uses. The procedure above is the maintained one.

### Known project-local divergence from upstream (preserve, don't revert)

The desktop main file has one intentional project-local modification relative to the upstream `braille-cylinder-stl-generator-openscad` snapshot: the default value of `dot_shape` has been changed from `"Rounded"` (upstream) to `"Cone"` (this project). Because the re-flatten procedure above starts by copying the desktop main file, this default automatically flows into the MakerWorld build — so as long as you do **not** revert the desktop file's `dot_shape` default during a re-vendor, the MakerWorld file will stay in sync. See the parent README's [Project-local modifications](../README.md#project-local-modifications) section for the full rationale and re-vendor procedure.

### What must NOT diverge from the desktop main file

Anything other than the one targeted edit:
- Every `/* [Section] */` block header (these drive MakerWorld's Customizer UI grouping; renaming or reordering them breaks parity with the web app and desktop OpenSCAD).
- Every parameter declaration and its inline magic comment (e.g. `// [10:0.1:100] ...`, `// [Embossing Plate, Counter Plate]`).
- Every `/* [Hidden] */` marker — the second one (around the `combined_shape` / `indicator_shapes` test-system block) keeps those four variables out of the Customizer panel.
- Every geometry module (`braille_dot_centered`, `counter_recess`, `cylinder_shell`, `cylinder_emboss_plate`, `cylinder_counter_plate`).
- The final `if (is_emboss_plate) { ... } else { ... }` dispatch.

---

## Cross-links

- [Parent README — full quick-start, parameter reference, troubleshooting, slicer notes](../README.md)
- [Desktop main file (canonical, dual-file)](../Braille_Cylinder_STL_Generator.scad)
- [Presets file (canonical)](../presets.scad)
- [License — PolyForm Noncommercial 1.0.0](../LICENSE_PolyForm_Noncommercial_1.0.0.md)
- [Upstream repository — `braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad)
- [Web-based generator (alternative to OpenSCAD entirely)](https://braille-cylinder-stl-generator.vercel.app)

---

## License recap

This file inherits **PolyForm Noncommercial 1.0.0** from the parent folder (see [`../LICENSE_PolyForm_Noncommercial_1.0.0.md`](../LICENSE_PolyForm_Noncommercial_1.0.0.md)) — unchanged by the flattening. Free for personal, educational, and non-commercial use; modification and remixing allowed; **no commercial use permitted**. If you need a commercial license for the generator, contact the upstream maintainer.
