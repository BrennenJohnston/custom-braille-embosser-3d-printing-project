# Embossing and Counter Cylinder High Quality Slicer Settings

This document is a readable transcription of the Bambu Studio slicer profile shown in the screenshots stored in `Settings Research/Cylinder High Quality profile/`.

## Scope

These settings are for the **embossing cylinder** and **counter cylinder** parts only (the two cylindrical parts that actually form the braille dots) and reflect the **Bambu Lab X1C** profile included for the initial project posting.

They are **not** the slicer profile used for the larger Braille Embosser Assembly (body, holders, grips, handle). That profile is documented separately in [`Braille_Embosser_Assembly_Slicer_Settings.md`](Braille_Embosser_Assembly_Slicer_Settings.md).

The companion `.3mf` for this profile is `Embossing and Counter Cylinder High Quality.3mf`.

## Profile Shown in the Screenshots

- Profile name: `0.12mm @BBL X1C - Embosser Cylinder HQ`
- Process mode: `Global`
- View mode: `Advanced`

## Slicing Result (Bambu Lab X1C + PLA Basic)

Source: `Settings Research/Cylinder High Quality profile/output.png` - Bambu Studio "Slicing Result" panel for the included `.3mf` with Bambu Lab PLA Basic on the X1C.

| Quantity | Model | Support | Total |
|---|---|---|---|
| Filament length | 8.14 m | 0 m (none) | **8.14 m** |
| Filament mass | 24.68 g | 0 g (none) | **24.68 g** |

| Other | Value |
|---|---|
| Filament change times | 0 |
| Estimated material cost | **$0.62** (Bambu Studio default `$25/kg` PLA reference) |
| Prepare time | 9 min 40 s |
| Model printing time | 2 h 55 min |
| **Total time** | **3 h 5 min** |

These figures are for the **complete cylinder pair** (P11 embossing + P12 universal counter) sliced together from `Embossing and Counter Cylinder High Quality.3mf` on a Bambu Lab X1C with Bambu Lab PLA Basic. No supports are used (consistent with the "no supports on the cylinders" rule in the published cylinder print-settings block). Per-cylinder figures (embossing only / counter only) are not produced by this multi-object profile; the cylinders are roughly equal in volume, so a replacement-embossing-only print is approximately **half** the totals above (~12 g, ~1.5 h). Slice the embossing STL on its own if you need a more precise per-cylinder figure.

## Quality

### Layer Height

- Layer height: `0.12 mm`
- Initial layer height: `0.2 mm`
- Mixed color sublayer: `Off`

### Line Width

- Default: `0.42 mm`
- Initial layer: `0.5 mm`
- Outer wall: `0.42 mm`
- Inner wall: `0.45 mm`
- Top surface: `0.42 mm`
- Sparse infill: `0.45 mm`
- Internal solid infill: `0.42 mm`
- Support: `0.42 mm`

### Seam

- Seam position: `Aligned`
- Seam placement away from overhangs (experimental): `Off`
- Smart scarf seam application: `On`
- Scarf application angle threshold: `155 deg`
- Scarf around entire wall: `Off`
- Scarf steps: `10`
- Scarf joint for inner walls: `On`
- Override filament scarf seam setting: `Off`
- Role-based wipe speed: `On`

### Precision

- Slice gap closing radius: `0.049 mm`
- Resolution: `0.012 mm`
- Arc fitting: `On`
- X-Y hole compensation: `0 mm`
- X-Y contour compensation: `0 mm`
- Auto circle contour-hole compensation: `Off`
- Elephant foot compensation: `0.15 mm`
- Precise Z height: `Off`

### Ironing

- Ironing type: `No ironing`

### Wall Generator

- Wall generator: `Arachne`
- Wall transitioning threshold angle: `10 deg`
- Wall transitioning filter margin: `25%`
- Wall transition length: `100%`
- Wall distribution count: `1`
- Minimum wall width: `85%`
- Minimum feature size: `25%`

### Advanced

- Order of walls: `inner/outer`
- Print infill first: `Off`
- Bridge flow: `1`
- Thick bridges: `Off`
- Only one wall on top surfaces: `Top surfaces`
- Only one wall on first layer: `Off`
- Smooth speed discontinuity area: `On`
- Smooth coefficient: `150`
- Avoid crossing wall: `Off`
- Smoothing wall speed along Z (experimental): `Off`

## Strength

### Walls

- Wall loops: `4`
- Alternate extra wall: `Off`
- Embedding the wall into the infill: `Off`
- Detect thin wall: `Off`

### Top/Bottom Shells

- Top surface pattern: `Monotonic`
- Top surface density: `100%`
- Top shell layers: `5`
- Top shell thickness: `0.6 mm`
- Top paint penetration layers: `5`
- Bottom surface pattern: `Monotonic`
- Bottom surface density: `100%`
- Bottom shell layers: `5`
- Bottom shell thickness: `0 mm`
- Bottom paint penetration layers: `5`
- Internal solid infill pattern: `Rectilinear`

### Sparse Infill

- Sparse infill density: `15%`
- Fill multiline: `1`
- Sparse infill pattern: `Gyroid`
- Length of sparse infill anchor: `400%`
- Maximum length of sparse infill anchor: `20`

### Advanced

- Infill/Wall overlap: `15%`
- Infill direction: `45 deg`
- Bridge direction: `0 deg`
- Minimum sparse infill threshold: `15 mm^2`
- Infill combination: `Off`
- Detect narrow internal solid infill: `On`
- Ensure vertical shell thickness: `Enabled`
- Detect floating vertical shells: `On`

## Speed

### Initial Layer Speed

- Initial layer: `40 mm/s`
- Initial layer infill: `75 mm/s`

### Other Layers Speed

- Outer wall: `50 mm/s`
- Inner wall: `75 mm/s`
- Small perimeters: `40 mm/s`
- Small perimeter threshold: `0 mm`
- Sparse infill: `90 mm/s`
- Internal solid infill: `90 mm/s`
- Vertical shell speed: `50 mm/s`
- Top surface: `75 mm/s`
- Slow down for overhangs: `On`
- Overhang speed at `10%`: `40 mm/s`
- Overhang speed at `25%`: `15 mm/s`
- Overhang speed at `50%`: `5 mm/s`
- Overhang speed at `75%`: `5 mm/s`
- Overhang speed at `100%`: `5 mm/s`
- Slow down by height: `Off`
- Bridge: `30 mm/s`
- Gap infill: `150 mm/s`
- Support: `75 mm/s`
- Support interface: `50 mm/s`

### Travel Speed

- Travel: `400 mm/s`

### Acceleration

- Normal printing: `3000 mm/s^2`
- Travel: `7500 mm/s^2`
- Initial layer travel: `3000 mm/s^2`
- Initial layer: `400 mm/s^2`
- Outer wall: `1500 mm/s^2`
- Inner wall: `0 mm/s^2`
- Top surface: `1500 mm/s^2`
- Sparse infill: `75 mm/s^2`

## Support

> Support is **disabled** for this profile. The fields below are stored in the profile but are inactive in the slicer UI until "Enable support" is turned on.

### Support

- Enable support: `Off`
- Type: `normal(auto)` (inactive)
- Style: `Default` (inactive)
- Threshold angle: `20 deg` (inactive)
- On build plate only: `Off`
- Remove small overhangs: `On`

### Raft

- Raft layers: `0`

### Filament for Supports

- Support/raft base: `Default` (inactive)
- Support/raft interface: `Default` (inactive)

### Advanced

- Initial layer density: `90%`
- Initial layer expansion: `-1 mm`
- Support wall loops: `-1`
- Top Z distance: `0.12 mm` (inactive)
- Bottom Z distance: `0.12 mm` (inactive)
- Base pattern: `Default` (inactive)
- Base pattern spacing: `2.5 mm` (inactive)
- Pattern angle: `0 deg` (inactive)
- Top interface layers: `2` (inactive)
- Bottom interface layers: `2` (inactive)
- Interface pattern: `Default` (inactive)
- Top interface spacing: `0.5 mm` (inactive)
- Normal support expansion: `0 mm` (inactive)
- Support/object xy distance: `0.35 mm` (inactive)
- Z overrides X/Y: `Off`
- Support/object first layer gap: `0.2 mm` (inactive)
- Don't support bridges: `Off`
- Independent support layer height: `On`

## Others

### Bed Adhesion

- Skirt loops: `0`
- Skirt height: `1 layer`
- Brim type: `Painted`
- Brim width: `5 mm` (applies only to painted regions; field is shown grayed in the UI because painted brim is per-paint, not global)
- Brim-object gap: `0.1 mm`

### Prime Tower

- Enable: `On`
- Skip points: `On`
- Internal ribs: `Off`
- Width: `35 mm`
- Max speed: `90 mm/s`
- Brim width: `3 mm`
- Infill gap: `150%`
- Rib wall: `On`
- Extra rib length: `0 mm`
- Rib width: `8 mm`
- Fillet wall: `On`

### Purge Options

- Purge into objects' infill: `Off`
- Purge into objects' support: `On`

### Special Mode

- Slicing mode: `Regular`
- Print sequence: `By layer`
- Spiral vase: `Off`
- Timelapse: `Traditional`
- Fuzzy skin: `None (Allow Paint)` (the dropdown is rendered truncated in the screenshot as `None(allow...)`; the full Bambu Studio label for this option is `None (Allow Paint)`)
- Fuzzy skin generator mode: `Displacement`
- Fuzzy skin noise type: `Classic`
- Fuzzy skin point distance: `0.8 mm`
- Fuzzy skin thickness: `0.3 mm`
- Apply fuzzy skin to first layer: `Off`

### Advanced

- Use beam interlocking: `Off`
- Interlocking depth of a segmented region: `0 mm`

### G-code Output

- Reduce infill retraction: `Auto`

### Post-Processing Scripts

- Post-processing scripts box: `Empty`

## Notes

- This file is based only on the settings visible in the provided screenshots.
- The values above were checked against the `Settings Research/Cylinder High Quality profile/` screenshots for the X1C profile.
- The high-quality nature of this profile comes primarily from the `0.12 mm` layer height (vs. `0.2 mm` for the Assembly profile) and the `Arachne` wall generator (vs. `Classic` for the Assembly profile), both of which improve curved-surface and small-feature fidelity on the cylinder dots.
- The slicing result block above is taken verbatim from the Bambu Studio Slicing Result panel for this `.3mf` with Bambu Lab PLA Basic on the X1C. If you re-slice with a different filament profile (e.g. PETG) or a custom message that changes the cylinder geometry, the totals will change; re-export `output.png` and update this section before re-publishing.
