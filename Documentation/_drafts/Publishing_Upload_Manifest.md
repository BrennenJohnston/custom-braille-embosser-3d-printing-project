# Custom Braille Embosser - Publishing Upload Manifest

> **Derived from:** [`Custom_Braille_Embosser_Publishing_Pack.md`](Custom_Braille_Embosser_Publishing_Pack.md).
> **Purpose:** the exact list of files, structured-field values, tags, categories, license tagging, and external links to upload for each platform. The platform descriptions never reference a file that is not also listed here.

---

## 1. Shared baseline (applies to all three platforms)

### 1.1 Common metadata

| Field | Value |
|---|---|
| Canonical title | `Custom Braille Embosser - Hand-Operated 3D-Printable Braille Card Maker` |
| Tagline / 1-sentence summary | `A fully 3D-printed, hand-operated braille embosser for business cards and short labels, with snap-fit parts and no fasteners, springs, or electronics.` |
| Cover image | `Photos/Custom_Braille_Embosser.jpg` |
| Source repo | <https://github.com/BrennenJohnston/custom-braille-embosser-3d-printing-project> |
| OKH manifest | [`okh.yml`](../../okh.yml) |
| Designer | **Brennen Johnston** |

### 1.2 Common external links

| Link | URL |
|---|---|
| Web-based customizer (deployed) | <https://braille-cylinder-stl-generator.vercel.app> |
| Web customizer source repo | <https://github.com/BrennenJohnston/braille-cylinder-stl-generator> |
| OpenSCAD customizer upstream | <https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad> |
| Accessible OpenSCAD UI | <https://github.com/BrennenJohnston/openscad-assistive-forge> |
| Liblouis (translation library) | <https://liblouis.io/> |
| Branah translator (for OpenSCAD path) | <https://www.branah.com/braille-translator> |
| OpenAT template (attribution) | <https://github.com/makersmakingchange/OpenAT-Template> |
| Earlier WATAP braille board listing (cross-link context) | <https://makerworld.com/en/models/254703-better-braille-alphabet-board-no-heading-title> |

### 1.3 Common video URLs

| # | Topic | Short | Long |
|---|---|---|---|
| 1 | Customizing / downloading / print settings | <https://youtu.be/m71VNZq28MI> | `https://www.youtube.com/watch?v=m71VNZq28MI` |
| 2 | Assembly | <https://youtu.be/x-uPNtT2Gqk> | `https://www.youtube.com/watch?v=x-uPNtT2Gqk` |
| 3 | Using the completed device | <https://youtu.be/77iXvJbkXh4> | `https://www.youtube.com/watch?v=77iXvJbkXh4` |

### 1.4 Common structured Print Settings values

| Field | Value |
|---|---|
| Layer height | 0.2 mm |
| Wall loops | 3 (device parts); Arachne wall generator for the cylinders |
| Infill | 30 % gyroid (PLA) / 20 % gyroid (PETG) |
| Supports | Tree / organic, overhangs >55° on Body Base / Body Top. None on cylinders. |
| Brim | 5 mm on Handle Grip + Handle Connector. None on cylinders. |
| Filament | PLA Basic (default), PETG (alternate). **~269 g per device** (8 h 44 min on Bambu Lab X1C with PLA Basic) + **~25 g per plate pair** (3 h 5 min on the same printer/material). Combined: ~293 g and ~11 h 49 min for one device + one plate pair. |
| Recommended printer | Bambu Lab X1C; any FDM ≥ 220 x 220 x 200 mm |
| Cylinder block (verbatim) | See Publishing Pack §8 |

### 1.5 Common tag baseline (15 - trim per platform)

`braille`, `accessibility`, `assistive-technology`, `embosser`, `vision-impairment`, `blindness`, `business-card`, `educational`, `openat`, `no-fasteners`, `customizable`, `hand-operated`, `3d-printable`, `openscad`, `braille-embosser`.

### 1.6 Common license disclosure (paste in every Description; the dropdown is separate)

- **Hardware:** CERN-OHL-W v2.
- **Documentation / photos / videos / written tutorials:** CC BY-SA 4.0.
- **Project software / scripts:** GPL-3.0-or-later.
- **Customizer software (deployed web app AND vendored OpenSCAD copy):** PolyForm Noncommercial 1.0.0 - free for personal, educational, and non-commercial use; commercial use not permitted.

---

## 2. MakerWorld manifest

### 2.1 Model-level structured fields

| Field | Value |
|---|---|
| Title | `Custom Braille Embosser - Hand-Operated 3D-Printable Braille Card Maker` |
| Category | Education > Other Education Models |
| License (dropdown) | CC BY-NC-SA 4.0 |
| Cover image | `Photos/Custom_Braille_Embosser.jpg` |
| Tags (use the full baseline of 15) | from §1.5 |
| Add Video (×3, long URLs) | from §1.3 |
| External link 1 | Web customizer URL |
| External link 2 | Source repo URL |
| Description body | from [`MakerWorld_Post_Copy.md`](MakerWorld_Post_Copy.md) §B |

### 2.2 Files to upload at the model level

> Bundle all STLs at the model level; Print-Profile pages share these files.

| File | Local path |
|---|---|
| P01 - Body Base v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P02 - Body Top v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P03 - Embosser Holder A1 v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P04 - Embosser Holder A2 v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P05 - Counter Holder B1 v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P06 - Counter Holder B2 v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P07 - Grip Extension Bottom v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P08 - Grip Extension Top v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P09 - Handle Connector v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| P10 - Handle Grip v1.0 (0.2 Layer Height).stl | `Build_Files/3D_Printing_Files/STL/` |
| Embossing_Plate_Brennen_0.3.stl | `Build_Files/3D_Printing_Files/Embossing_Plates_Examples/` |
| Embossing_Plate_Brennen_0.4.stl | `Build_Files/3D_Printing_Files/Embossing_Plates_Examples/` |
| Universal_Counter_Plate_0.3.stl | `Build_Files/3D_Printing_Files/Embossing_Plates_Examples/` |
| Universal_Counter_Plate_0.4.stl | `Build_Files/3D_Printing_Files/Embossing_Plates_Examples/` |

### 2.3 Print Profiles (2)

| # | Profile title | `.3mf` file | Local path | Real printed photo (REQUIRED) | Structured fields |
|---|---|---|---|---|---|
| 1 | `Bambu X1C - All 10 device parts (0.2 mm Layer Height)` | `Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf` | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/` | Assembled finished device (see Asset Checklist §1.1) | X1C / PLA / 0.2 mm / 30 % gyroid / supports tree >55° / 5 mm brim on small parts |
| 2 | `Bambu X1C - Cylinder Pair, High Quality (Embossing + Counter)` | `Embossing and Counter Cylinder High Quality.3mf` | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/` | Cylinder pair on its own, ideally next to embossed card | X1C / PLA / 0.12 mm / Arachne / **no supports** / **no brim** / seam painted on indicator area |

### 2.4 Photos for the model gallery (in addition to per-Print-Profile covers)

1. Lead cover - `Photos/Custom_Braille_Embosser.jpg`
2. Assembled-device alt angle - from `Photos/DSC_8542.jpg` or `DSC_8590.jpg`
3. In-use shot (hand on handle, embossing in progress) - from `Photos/DSC_8569.jpg` / `DSC_8570.jpg` / `DSC_8572.jpg` / `DSC_8575.jpg`
4. Embossed-card close-up - **RESHOOT** (see Asset Checklist §1.1)
5. Parts-spread / exploded view - **RESHOOT or RENDER** (see Asset Checklist §1.1)
6. (Optional) Web-customizer browser screenshot

### 2.5 Document attachments

> MakerWorld doesn't have a first-class "attach PDF" slot for documentation; link from the description.

- Description links to: Maker Guide, User Guide, Quickstart Guide, Design Rationale, Summary, BOM CSV. While PDFs are pending (Publishing Pack G1), link directly to the markdown files on GitHub.

---

## 3. Printables manifest

### 3.1 Structured fields

| Field | Value |
|---|---|
| Title (Model name) | `Custom Braille Card Embosser - Hand Operated` *(title as published on the live listing)* |
| Summary | `A fully 3D printed, hand operated braille embosser for cards and labels. Fully snap fit, no fasteners or electronics.` *(as published)* |
| Category (Main) | Tools *(as published; Education is the secondary candidate)* |
| License | CC BY-NC-SA 4.0 |
| Cover image | `Photos/Custom_Braille_Embosser.jpg` |
| Tags (as published) | `educational`, `customizable`, `accessibility`, `blind`, `embosser`, `customized`, `braille`, `assistivetechnology`, `businesscard`, `visionimpaired`, `buinesscardembosser` |
| Filaments | PLA Basic (primary); PETG (alternate) |
| Printer brand / model | Bambu Lab X1C (primary), Any FDM ≥ 220 x 220 x 200 mm |
| Print Settings (structured) | from §1.4 |
| Add Video (×3) | from §1.3 long URLs |
| Description body | from [`Printables_Post_Copy.md`](Printables_Post_Copy.md) §B |

### 3.2 Files to upload

#### 3D models (STL)

All 10 device STLs + 4 example plate STLs (same list as MakerWorld §2.2).

#### Print profiles (`.3mf`)

| File | Local path |
|---|---|
| Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/` |
| Embossing and Counter Cylinder High Quality.3mf | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/` |
| Braille_Embosser_Assembly_Slicer_Settings.md (companion settings transcription) | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/` |
| Embossing_Counter_Cylinder_HQ_Slicer_Settings.md (companion settings transcription) | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/` |

#### Supplementary documents

| File | Local path | Status |
|---|---|---|
| `Custom_Braille_Embosser_BOM.csv` | `Documentation/` | DONE (both `.3mf` profiles sliced on X1C + PLA Basic: device 268.81 g / 8 h 44 min, plate pair 24.68 g / 3 h 5 min, combined 293.49 g / ~11 h 49 min / ~$7.34. Per-part P01-P10 and P11-P12 individually remain TBD - not needed for platform copy. Publishing Pack G2.) |
| `Custom_Braille_Embosser_Maker_Guide.pdf` | `Documentation/` | PDF-PENDING (link to markdown on GitHub in the meantime) |
| `Custom_Braille_Embosser_User_Guide.pdf` | `Documentation/` | PDF-PENDING |
| `Custom_Braille_Embosser_Quickstart_Guide.pdf` | `Documentation/` | PDF-PENDING |
| `Custom_Braille_Embosser_Design_Rationale.pdf` | `Documentation/` | PDF-PENDING |
| `Custom_Braille_Embosser_Summary.pdf` | `Documentation/` | PDF-PENDING |

### 3.3 Photos for the gallery

Same set as MakerWorld §2.4 (lead, alt-angle, in-use, embossed-card close-up [RESHOOT], parts-spread [RESHOOT/RENDER], optional customizer screenshot). Per-Print-Profile photos are not separately required on Printables but improve conversion.

---

## 4. Thingiverse manifest

### 4.1 Structured fields

| Field | Value |
|---|---|
| Thing name | `Custom Braille Embosser - Hand-Operated 3D-Printable Braille Card Maker` |
| Summary | from [`Thingiverse_Post_Copy.md`](Thingiverse_Post_Copy.md) §B |
| Print Settings | from [`Thingiverse_Post_Copy.md`](Thingiverse_Post_Copy.md) §C |
| Post-Printing | from [`Thingiverse_Post_Copy.md`](Thingiverse_Post_Copy.md) §D |
| Category | Tools (primary) or Education (secondary) |
| License | CC BY-NC-SA |
| Cover image | `Photos/Custom_Braille_Embosser.jpg` |
| Tags (trim baseline to ~5-8) | `braille`, `accessibility`, `assistive-technology`, `embosser`, `vision-impairment`, `business-card`, `educational`, `no-fasteners` |
| Videos | YouTube watch URLs pasted directly into the description (Thingiverse auto-converts) |

### 4.2 Files to upload (Thing Files)

> Thingiverse doesn't have a separate "Print Profiles" group; `.3mf`s go in alongside STLs.

| File | Local path |
|---|---|
| All 10 device STLs | `Build_Files/3D_Printing_Files/STL/` |
| 4 example plate STLs | `Build_Files/3D_Printing_Files/Embossing_Plates_Examples/` |
| 2 `.3mf` profiles | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/` |
| `Custom_Braille_Embosser_BOM.csv` | `Documentation/` |
| `Custom_Braille_Embosser_Maker_Guide.pdf` (once exported) | `Documentation/` |
| `Custom_Braille_Embosser_User_Guide.pdf` (once exported) | `Documentation/` |
| `Custom_Braille_Embosser_Quickstart_Guide.pdf` (once exported) | `Documentation/` |
| `Custom_Braille_Embosser_Design_Rationale.pdf` (once exported) | `Documentation/` |
| `Custom_Braille_Embosser_Summary.pdf` (once exported) | `Documentation/` |

### 4.3 Photos for the Thing gallery

Same set as the other platforms (lead, alt-angle, in-use, embossed-card close-up [RESHOOT], parts-spread [RESHOOT/RENDER]).

---

## 5. Cross-platform sanity check

Before pasting:

| Check | MW | PR | TV |
|---|---|---|---|
| Title is the canonical title from §1.1 (modulo character cap) | [ ] | [ ] | [ ] |
| Summary / tagline = §1.1 | [ ] | [ ] | [ ] |
| Cover image = `Photos/Custom_Braille_Embosser.jpg` | [ ] | [ ] | [ ] |
| File inventory matches §2.2 / §3.2 / §4.2 | [ ] | [ ] | [ ] |
| All 3 YouTube URLs present | [ ] | [ ] | [ ] |
| Web customizer URL present | [ ] | [ ] | [ ] |
| Source-repo URL present | [ ] | [ ] | [ ] |
| Cylinder print-settings block pasted verbatim from Publishing Pack §8 | [ ] | [ ] | [ ] |
| OpenSCAD framing pasted verbatim ("for anyone not wanting to, or not able to, use the browser-based tool") | [ ] | [ ] | [ ] |
| Full license split disclosed in description (CERN-OHL-W v2 / CC BY-SA 4.0 / GPL-3.0 / PolyForm NC 1.0.0) | [ ] | [ ] | [ ] |
| Card-thickness rule (0.3 mm / 0.4 mm; plate-pair must match) called out | [ ] | [ ] | [ ] |
| Tag count within the platform's cap | [ ] | [ ] | [ ] |
| Real printed cover photo per Print Profile (MakerWorld 2026 rule) | [ ] | N/A | N/A |
| **No file referenced in copy that is not also in the upload list** | [ ] | [ ] | [ ] |
| Formal fields use `Brennen Johnston`; body copy can use `Brennen` where it reads better | [ ] | [ ] | [ ] |
| BOM mass / time TBDs replaced with slicer-reported values (G2) | [ ] | [ ] | [ ] |
| PDFs exported (G1) - or temporary markdown-on-GitHub links noted | [ ] | [ ] | [ ] |

When every row above is checked for the platform you are publishing to, paste and publish.
