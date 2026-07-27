# Braille Embosser Assembly Slicer Settings

This document is a readable transcription of the Bambu Studio slicer profile shown in the screenshots stored in `Settings Research/Braille Embosser Assembly v1.0/`.

## Scope

These settings are for the **Braille Embosser Assembly** 3D printed parts only and reflect the **Bambu Lab X1C** profile included for the initial project posting.

They are **not** the separate high-quality settings mentioned in the tutorial video for the **embossing cylinder** and **counter cylinder**. Those are documented separately in [`Embossing_Counter_Cylinder_HQ_Slicer_Settings.md`](Embossing_Counter_Cylinder_HQ_Slicer_Settings.md).

The companion `.3mf` for this profile is `Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf`.

## Profile Shown in the Screenshots

- Profile name: `0.20mm Strength @BBL X1C - v1.3`
- Process mode: `Global`
- View mode: `Advanced`

## Slicing Result (Bambu Lab X1C + PLA Basic)

Source: `Settings Research/Braille Embosser Assembly v1.0/output.png` - Bambu Studio "Slicing Result" panel for the included `.3mf` with Bambu Lab PLA Basic on the X1C.

| Quantity | Model | Support | Total |
|---|---|---|---|
| Filament length | 85.39 m | 3.31 m | **88.70 m** |
| Filament mass | 258.79 g | 10.02 g | **268.81 g** |

| Other | Value |
|---|---|
| Filament change times | 0 |
| Estimated material cost | **$6.72** (Bambu Studio default `$25/kg` PLA reference) |
| Prepare time | 8 min 16 s |
| Model printing time | **8 h 35 min** |
| **Total time** | **8 h 44 min** |

These figures are the **whole-assembly** total for all 10 device parts (P01-P10) printed together on one X1C plate from `Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf`. They do **not** include the embossing or counter cylinders, which are sliced separately from the High Quality profile in [`Embossing_Counter_Cylinder_HQ_Slicer_Settings.md`](Embossing_Counter_Cylinder_HQ_Slicer_Settings.md). Per-part mass / time figures (P01-P10 individually) are not produced by this multi-object profile; if a per-part breakdown is required, slice each STL on its own and copy the values into [`Documentation/Custom_Braille_Embosser_BOM.csv`](../../../../Documentation/Custom_Braille_Embosser_BOM.csv) and [Maker Guide §8.2](../../../../Documentation/_drafts/Custom_Braille_Embosser_Maker_Guide.md#82-per-part-summary).

## Quality

### Layer Height

- Layer height: `0.2 mm`
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

- Wall generator: `Classic`

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

- Wall loops: `6`
- Alternate extra wall: `Off`
- Embedding the wall into the infill: `Off`
- Detect thin wall: `Off`

### Top/Bottom Shells

- Top surface pattern: `Monotonic`
- Top surface density: `100%`
- Top shell layers: `5`
- Top shell thickness: `1 mm`
- Top paint penetration layers: `5`
- Bottom surface pattern: `Monotonic`
- Bottom surface density: `100%`
- Bottom shell layers: `3`
- Bottom shell thickness: `0 mm`
- Bottom paint penetration layers: `3`
- Internal solid infill pattern: `Rectilinear`

### Sparse Infill

- Sparse infill density: `25%`
- Fill multiline: `1`
- Sparse infill pattern: `Grid`
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

- Initial layer: `50 mm/s`
- Initial layer infill: `105 mm/s`

### Other Layers Speed

- Outer wall: `60 mm/s`
- Inner wall: `300 mm/s`
- Small perimeters: `50%`
- Small perimeter threshold: `0 mm`
- Sparse infill: `270 mm/s`
- Internal solid infill: `250 mm/s`
- Vertical shell speed: `80%`
- Top surface: `200 mm/s`
- Slow down for overhangs: `On`
- Overhang speed at `10%`: `0 mm/s`
- Overhang speed at `25%`: `50 mm/s`
- Overhang speed at `50%`: `30 mm/s`
- Overhang speed at `75%`: `10 mm/s`
- Overhang speed at `100%`: `10 mm/s`
- Slow down by height: `Off`
- Bridge: `50 mm/s`
- Gap infill: `250 mm/s`
- Support: `150 mm/s`
- Support interface: `80 mm/s`

### Travel Speed

- Travel: `500 mm/s`

### Acceleration

- Normal printing: `10000 mm/s^2`
- Travel: `10000 mm/s^2`
- Initial layer travel: `6000 mm/s^2`
- Initial layer: `500 mm/s^2`
- Outer wall: `5000 mm/s^2`
- Inner wall: `0 mm/s^2`
- Top surface: `2000 mm/s^2`
- Sparse infill: `100%`

## Support

### Support

- Enable support: `On`
- Type: `normal(manual)`
- Style: `Default`
- Threshold angle: `35 deg`
- On build plate only: `Off`
- Remove small overhangs: `On`

### Raft

- Raft layers: `0`

### Filament for Supports

- Support/raft base: `Default`
- Support/raft interface: `Default`

### Advanced

- Initial layer density: `90%`
- Initial layer expansion: `-1 mm`
- Support wall loops: `-1`
- Top Z distance: `0.2 mm`
- Bottom Z distance: `0.2 mm`
- Base pattern: `Default`
- Base pattern spacing: `2.5 mm`
- Pattern angle: `0 deg`
- Top interface layers: `2`
- Bottom interface layers: `2`
- Interface pattern: `Default`
- Top interface spacing: `0.5 mm`
- Normal support expansion: `0 mm`
- Support/object xy distance: `0.35 mm`
- Z overrides X/Y: `Off`
- Support/object first layer gap: `0.2 mm`
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
- The values above were checked against the `Settings Research/Braille Embosser Assembly v1.0/` screenshots for the X1C profile.
- The slicing result block above is taken verbatim from the Bambu Studio Slicing Result panel for this `.3mf` with Bambu Lab PLA Basic on the X1C. If you re-slice with a different filament profile (e.g. PETG) the totals will change; re-export `output.png` and update this section before re-publishing.
