# Custom Braille Embosser - Publishing Pack (Master Source of Truth)

> **Document version:** 1.0 | 2026-Jun-01
> **Designer:** Brennen Johnston
> **Repository:** <https://github.com/BrennenJohnston/custom-braille-embosser-3d-printing-project>
> **Status:** Draft - hold for the open items listed in [Section 11: Outstanding Gaps Before Publishing](#11-outstanding-gaps-before-publishing).

This document is the single source of truth for the public listing copy of the Custom Braille Embosser on **MakerWorld**, **Printables**, and **Thingiverse**. Edit this file first; then re-derive the three platform-specific copies in this folder:

- [`MakerWorld_Post_Copy.md`](MakerWorld_Post_Copy.md)
- [`Printables_Post_Copy.md`](Printables_Post_Copy.md)
- [`Thingiverse_Post_Copy.md`](Thingiverse_Post_Copy.md)

The companion docs in this same folder are also derived from this pack:

- [`Publishing_Asset_Checklist.md`](Publishing_Asset_Checklist.md) - what strong listings include and what is still missing.
- [`Publishing_Upload_Manifest.md`](Publishing_Upload_Manifest.md) - per-platform list of files, structured-field values, tags, categories, license tagging, and external links.

---

## Table of contents

1. [Titles and tagline](#1-titles-and-tagline)
2. [Long-form description](#2-long-form-description)
3. [Why this project exists](#3-why-this-project-exists)
4. [Who this helps](#4-who-this-helps)
5. [How the embosser works (plain-language)](#5-how-the-embosser-works-plain-language)
6. [What is included in the download package](#6-what-is-included-in-the-download-package)
7. [Customizer paths - browser-first, OpenSCAD as backup](#7-customizer-paths---browser-first-openscad-as-backup)
8. [Cylinder print-settings block (copy-paste verbatim)](#8-cylinder-print-settings-block-copy-paste-verbatim)
9. [Assembly, use, troubleshooting, limitations](#9-assembly-use-troubleshooting-limitations)
10. [Attribution, licensing, tags, categories](#10-attribution-licensing-tags-categories)
11. [Outstanding gaps before publishing](#11-outstanding-gaps-before-publishing)
12. [Video embed snippets](#12-video-embed-snippets)
13. [Per-platform deviation summary](#13-per-platform-deviation-summary)
14. [Maintenance plan after first publish](#14-maintenance-plan-after-first-publish)

---

## 1. Titles and tagline

### 1.1 Recommended title (use everywhere if length allows)
**Custom Braille Embosser - Hand-Operated 3D-Printable Braille Card Maker**

### 1.2 Alternates (use when a platform forces a shorter title or wants a different angle)
- *Custom Braille Embosser - 3D-Printable Braille Business-Card Embosser (No Fasteners, No Electronics)*
- *Custom Braille Embosser - Open-Source Hand Brailler for Cards and Labels*

### 1.3 One-sentence summary (use in the Summary / tagline field on every platform)
> A fully 3D-printed, hand-operated braille embosser for business cards and short labels, with snap-fit parts and no fasteners, springs, or electronics.

### 1.4 Short pitch (1-2 sentences, for thumbnails / search snippets)
> I built this project because I couldn't find an affordable way to make small batches of custom braille business cards and short labels. So I designed a fully 3D printed, hand operated embosser that just snaps together, with no fasteners, springs, glue, or electronics. I hope this helps someone!

---

## 2. Long-form description

> *3-5 paragraphs. Paste verbatim into every platform's main description, then trim to fit length limits.*

I built this project because I couldn't find an affordable way to make small batches of custom braille business cards and short labels. Braille card embossers are hard to find, and the usual alternatives, like a slate and stylus, a Perkins-style brailler, or a fully electric embosser, are not ideal for quick, low cost custom runs. So I designed a fully 3D printed, hand operated embosser that just snaps together, with no fasteners, springs, glue, or electronics. I hope this helps someone!

The machine itself is simple. It's fully 3D printed, hand operated, and built from **10 snap fit parts with no fasteners, no springs, no glue, and no electronics**. The message lives on a separate embossing cylinder, paired with a matching counter cylinder. When the text changes, you should only need to print a new embossing cylinder. The recommended way to generate those cylinders is the browser based tool I created as a companion to this project. However, I've also created an OpenSCAD version which is included as the offline and power user backup.

**Who this helps:** blind and vision impaired users, sighted teachers, parents, and caregivers, schools, libraries, and nonprofits without a $1,500+ Perkins Brailler budget, and makers printing one for someone else.

The repo includes the 10 device STLs, three Bambu `.3mf` profiles, four example plate STLs, CAD source files, the BOM, written guides, and three tutorial videos. It is meant to be practical for blind and low-vision users, teachers, parents, caregivers, schools, nonprofits, and makers building one for someone else. The base device uses under $10 of filament, and most updates only require reprinting the embossing cylinder.

The hardware is released under **CERN-OHL-W v2**, with documentation under **CC BY-SA 4.0** and project software under **GPL-3.0-or-later**. The deployed web customizer and the vendored OpenSCAD copy are separate **PolyForm Noncommercial 1.0.0** software. That license split matters, so it should stay visible in every platform version.

---

## 3. Why this project exists

The standard tools for making tactile braille fall into three rough cost tiers (USD, 2026):

| Tier | Tool | Approx. unit cost | Notes |
|---|---|---|---|
| Low | Slate and stylus | $10 - $30 | Slow, requires reverse / mirror typing, mostly for very short labels. |
| Mid | Manual hand-frame braillers (Perkins-style) | $700 - $1,500 | Heavy, mechanically complex, hard to ship internationally. |
| High | Electronic embossers (Index, ViewPlus, ...) | $2,000 - $5,000+ | Fast, but out of reach for individuals and most schools outside well-funded districts. |

Existing DIY designs (various MMC braille labellers, Hot Dots tape, hand-rolled "Braille Buddy" prototypes) usually emboss one fixed message per device or one character at a time, and do not include a parametric pipeline for arbitrary text. **Custom business-card braille embossers are no longer commercially available**, so a blind professional who wants a tactile business card cannot simply buy a custom embosser the way you can buy a custom stamp.

The Custom Braille Embosser was designed to fit a missing **fourth tier**:

- **Cost:** under $10 USD per device in raw filament.
- **Manufacturing:** any FDM printer; no fasteners, no electronics, no PCB.
- **Customisation:** any text, any supported language, Grade-1 or Grade-2 braille, generated parametrically.
- **Repair:** every part is reprintable.

This is the **why** for the listing description. Keep it short and explicit on every platform.

---

## 4. Who this helps

- **Blind and vision-impaired users** who want custom tactile braille on cards, labels, file dividers, name tags, signage, or instructional handouts.
- **Sighted teachers, parents, caregivers, and rehabilitation professionals** who need a small batch of braille labels without a $1,500+ Perkins Brailler budget.
- **Schools, libraries, and nonprofits** that want to give every student or every signpost a braille label.
- **Makers building it for someone else** who want a practical project that can be printed, assembled, and updated without specialized hardware.
- **Researchers and translators** building tools for under-served braille language tables (Liblouis covers 50+).

---

## 5. How the embosser works (plain-language)

The device is a **two-cylinder hand roller**. One cylinder has braille dots sticking out (the *embossing plate*); the other has matching dimples (the *universal counter plate*). When you turn the handle, the two cylinders rotate together and squeeze a sheet of card stock between them. The dots punch upward through the card and into the matching cavities, leaving the braille permanently raised on the card.

There is no electronic switch, no battery, no spring, no fastener, and no glue. The whole device is held together by **snap-fit features printed directly into each part**:

- The **Body Base** and **Body Top** clamshell snap around the two plate sub-assemblies.
- Each cylindrical plate is held by a **two-part snap-fit holder** (Embosser Holder A1/A2 for the embossing plate; Counter Holder B1/B2 for the counter plate).
- The **Handle Connector** snaps into the body and drives the embossing cylinder; the **Handle Grip** snaps over the connector.
- An optional **Grip Extension** snaps onto the user-side of the body for a longer purchase.

To swap the braille content you pop the lid off the body, lift the embossing cylinder out, and drop in a new one. Universal counter plates can be reused as long as the card thickness stays the same, so a typical re-print is a single 1.5-hour embossing cylinder.

---

## 6. What is included in the download package

> *Use this exact inventory in every platform listing. Do not promise files that are not in the actual upload manifest.*

| # | Group | Contents | Path in repo |
|---|---|---|---|
| A | **Printable device parts (10 STLs)** | P01 Body Base, P02 Body Top, P03 Embosser Holder A1, P04 Embosser Holder A2, P05 Counter Holder B1, P06 Counter Holder B2, P07 Grip Extension Bottom, P08 Grip Extension Top, P09 Handle Connector, P10 Handle Grip - all `P0X - <part> v1.0 (0.2 Layer Height).stl`. | [`Build_Files/3D_Printing_Files/STL/`](../../Build_Files/3D_Printing_Files/STL/) |
| B | **Sliced print profiles (2 `.3mf` files)** | Bambu X1C - all 10 device parts on plate; Bambu X1C - cylinder pair only, High Quality. Each profile is accompanied by a markdown transcription of its slicer settings. | [`Build_Files/3D_Printing_Files/Print_Profiles/X1C/`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/) |
| C | **Example plate pairs (4 STLs)** | Pre-generated embossing + universal counter plate pairs for 0.3 mm and 0.4 mm card stock, useful for first-build verification. | [`Build_Files/3D_Printing_Files/Embossing_Plates_Examples/`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Examples/) |
| D | **CAD source (Fusion + STEP + OBJ)** | Fusion `.f3z` archive of the full assembly, 5 STEP files (full assembly + 4 sub-assemblies), 10 per-part `.obj` + matching `.mtl`. | [`Design_Files/CAD_Design_Files/`](../../Design_Files/CAD_Design_Files/) |
| E | **Documentation set** | Maker Guide, User Guide, Quickstart Guide, Design Rationale, Summary, BOM. Markdown drafts and `.docx` working copies in the repo; PDF exports pending (see [Section 11](#11-outstanding-gaps-before-publishing)). | [`Documentation/`](../) |
| F | **Bill of Materials** | CSV (final) plus `.xlsx` working copy. No off-the-shelf electronics, no fasteners; only filament and card stock. | [`Documentation/Custom_Braille_Embosser_BOM.csv`](../Custom_Braille_Embosser_BOM.csv) |
| G | **Video tutorials (3 YouTube + local mirrors)** | Tutorial 1: customizing braille / downloading STLs / 3D-print settings. Tutorial 2: snap-fit assembly. Tutorial 3: using the completed device. Each as a YouTube link and a local `.mp4` + `.srt`. | [`Video_Tutorials/`](../../Video_Tutorials/) |
| H | **Bonus CAD-driven assembly simulation** | `Braille_Embosser_Assembly_Video_Simulation_2.mp4` (~10 MB, no narration) - usable as a supplemental marketing clip. | [`Video_Tutorials/Braille_Embosser_Assembly_Video_Simulation_2.mp4`](../../Video_Tutorials/Braille_Embosser_Assembly_Video_Simulation_2.mp4) |
| I | **Companion-tool links (not bundled files; external)** | Web-based customizer (deployed): <https://braille-cylinder-stl-generator.vercel.app>. Source: `braille-cylinder-stl-generator`. OpenSCAD copy vendored in the repo. Accessible OpenSCAD UI: `openscad-assistive-forge`. | See [Section 7](#7-customizer-paths---browser-first-openscad-as-backup) |

---

## 7. Customizer paths - browser-first, OpenSCAD as backup

Plate generation is intentionally **decoupled** from the device. The device is content-agnostic; the customizer is a separate, parameterised pipeline.

### 7.1 Primary - Web-based customizer (recommended for almost everyone)

| Field | Value |
|---|---|
| Open the web app | <https://braille-cylinder-stl-generator.vercel.app> |
| Source repo | <https://github.com/BrennenJohnston/braille-cylinder-stl-generator> |
| Translation | Automatic braille translation via [Liblouis](https://liblouis.io/). The documented workflow centers on English Grade 1 / Grade 2, with 50+ language tables available. |
| Install required | None. Works in a modern browser, including Chromebooks and tablets. |
| Where STL generation runs | **Locally in your browser**. Your text is never uploaded. |
| Accessibility | Screen-reader friendly UI; dark / light / high-contrast modes; adjustable font size |
| License (web app) | PolyForm Noncommercial 1.0.0 |
| Walkthrough | [Video Tutorial 1 on YouTube](https://youtu.be/m71VNZq28MI) |

Typical workflow: open the web app, paste your text, pick a translation table, set the card thickness to **0.3 mm** or **0.4 mm**, click *Generate*, preview, then click *Download STL*. Switch the plate selector to *Universal Counter Plate* and repeat. Print both at the **same** card thickness.

### 7.2 Backup - OpenSCAD offline alternative (vendored directly in this repo)

The OpenSCAD customizer is the project's official offline / power-user backup. Frame it exactly this way in every listing:

> **The OpenSCAD customizer is the offline / power-user backup for anyone not wanting to, *or not able to*, use the browser-based tool.**

The *"or not able to"* half of that sentence is intentional. It covers:

- **Offline use** - no internet at all (camping, fieldwork, build parties without WiFi, areas with poor connectivity).
- **Blocked-internet environments** - school / library / corporate / government networks that block the deployed Vercel app or block arbitrary third-party web apps.
- **Screen-reader and accessibility-driven workflows** that prefer a desktop application over a browser app (pair the OpenSCAD copy with [`openscad-assistive-forge`](https://github.com/BrennenJohnston/openscad-assistive-forge) for an accessible browser front-end on top of the OpenSCAD generator).
- **Locked-down corporate / school / library machines** that can't run web apps but can run installed software like OpenSCAD.

| Field | Value |
|---|---|
| Local copy | [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad) |
| Upstream repo | <https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad> |
| Vendored version | 2.2.1 (2026-05-30) |
| Required software | [OpenSCAD](https://openscad.org/) 2024.x or newer (2026.01.03 or newer recommended) |
| Translation | **Manual** - paste pre-translated Unicode braille from a third-party translator such as <https://www.branah.com/braille-translator> (Unicode mode, not ASCII). This extra paste step (and the OpenSCAD learning curve) is the main tradeoff vs. the browser tool, and is called out explicitly in the live Printables listing. |
| Accessibility | Pair with [`openscad-assistive-forge`](https://github.com/BrennenJohnston/openscad-assistive-forge) for an accessible browser UI |
| License (OpenSCAD copy) | PolyForm Noncommercial 1.0.0 - separate from the rest of the repository |

Files generated by either path drop directly into the same Embosser Holder A1/A2 and Counter Holder B1/B2 sockets.

### 7.3 Pre-generated example plates (verify your printer first)

Two pre-generated example pairs are included so you can verify your printer before generating user-specific plates:

- `Embossing_Plate_Brennen_0.3.stl` + `Universal_Counter_Plate_0.3.stl` (0.3 mm card)
- `Embossing_Plate_Brennen_0.4.stl` + `Universal_Counter_Plate_0.4.stl` (0.4 mm card)

---

## 8. Cylinder print-settings block (copy-paste verbatim)

> Source: `Video_Tutorials/Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/Custom_Braille_Embosser_3d_Printing_Step1.srt`, also captured in [Maker Guide Section 8.4](Custom_Braille_Embosser_Maker_Guide.md) and [Written Tutorial Section 2.7](../../Video_Tutorials/Custom_Braille_Embosser_Written_Tutorial.md).
>
> Treat this block as the **tested Bambu Studio + Bambu Lab X1C baseline only**. Cura / OrcaSlicer / PrusaSlicer equivalents have not been tuned and should not be presented as a generalised cross-slicer recipe.

This block should appear verbatim in **all three** platform variants, both inside the description and as the basis for each platform's structured *Print Settings* form fields.

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

### 8.1 Device-part print settings (use the `.3mf` profiles when possible)

For makers slicing the per-part STLs on a non-Bambu printer, the included `.3mf` profiles already encode these settings:

| Setting | Value | Why |
|---|---|---|
| Layer height | **0.2 mm** | Used for all parts in v1.0; matches filenames. |
| Wall loops | 3 (device parts); switch to **Arachne** for the cylinders | Strength at snap-fit features; recessed-dot accuracy on cylinders. |
| Top / bottom layers | 4 / 4 | Surface finish. |
| Infill | **30 % gyroid** (PLA) or **20 % gyroid** (PETG) | Stiff enough to handle squeeze force without flexing. |
| Supports | **Tree / organic, only on overhangs >55°** on Body Base / Body Top. **None on the cylinders.** | Most parts print support-free. |
| Brim | **5 mm** on small-footprint parts (Handle Grip, Handle Connector). **None on the cylinders.** | Reduces warping. |
| Material | PLA (default) or PETG | PETG is tougher; PLA prints more easily. |
| Recommended printer | Bambu Lab X1C (`.3mf` profiles provided); any FDM with build volume ≥ 220 x 220 x 200 mm | Pre-sliced profiles included. |
| Filament budget | **~269 g per device** (8 h 44 min total print time on Bambu Lab X1C with PLA Basic) + **~25 g per plate pair** (3 h 5 min total print time on the same printer/material). Combined: ~293 g and ~11 h 49 min for one device + one plate pair. |

---

## 9. Assembly, use, troubleshooting, limitations

### 9.1 Assembly (one-paragraph summary, expand from Maker Guide Section 12)

Sort the parts into two groups by the **plus / X** vs **minus** markings on the holder pairs. Snap each cylinder into its matching holder pair (plus = embossing, minus = counter), lining up the triangle indicators. Snap the Grip Extension onto the body if you want the longer grip. Drop both cylinder sub-assemblies into the Body Base with the **embossing cylinder on the left** and the **counter cylinder on the right**, indicator triangles mirrored. Snap on the Body Top, insert the Handle Connector (X-end into the embossing-cylinder holder), and snap the Handle Grip over the connector. Total active time: ~10-15 minutes. The full step-by-step is in [Maker Guide Section 12](Custom_Braille_Embosser_Maker_Guide.md#12-transcript-backed-assembly-tutorial) and [Video 2 on YouTube](https://youtu.be/x-uPNtT2Gqk).

### 9.2 Use (one-paragraph summary, expand from User Guide)

Align the indicator triangles on both cylinders so they point directly at each other (starting position). Rotate the device so the rollers are horizontal. Drop a sheet of 0.3 mm or 0.4 mm card stock between the rollers - the thickness **must match** the plate pair you have installed. Turn the handle forward about a half turn. The braille is now permanent. To change the message, swap in a new embossing cylinder (the same universal counter plate can be reused for any embossing cylinder at the same card thickness). The full step-by-step is in [User Guide Section 5](Custom_Braille_Embosser_User_Guide.md#5-how-to-use) and [Video 3 on YouTube](https://youtu.be/77iXvJbkXh4).

### 9.3 Troubleshooting (verbatim into every platform)

| Symptom | Likely cause | Fix |
|---|---|---|
| Dots too shallow / missing | Card thicker than the plate pair was designed for | Use the matching 0.4 mm plate pair on 0.4 mm card. |
| Dots flat-topped instead of rounded | Cylinder print quality is poor | Reprint the cylinders using the [Section 8](#8-cylinder-print-settings-block-copy-paste-verbatim) block: seam painting on the indicator area, Arachne wall generation, halved speeds. |
| Card tears | Card too thin (<0.25 mm) | Use 0.3 mm or thicker card stock. |
| Cylinder fit is too tight during assembly | Minor print swell on the mating surface | Lightly sand and test-fit again. |
| Cylinders rotate with heavy resistance | Cylinders not aligned per the triangle markers | Remove the lid, re-align triangles, embossing on the left and counter on the right. |
| Fresh cylinders are hard to remove on the first swap | Tight first-fit | Work them loose with a small flathead screwdriver (as shown in Video 3). |
| Holders rattle | Snap features under-printed | Reprint at 4 wall loops. |
| Handle Grip slides off | Snap rib under-tolerance | Reprint at +0.05 mm horizontal expansion. |
| Print is skewed across the card | Start position off, or rolled too far past the last dot while checking | Re-align indicator triangles, finish the print before flipping to inspect. |
| Plate pair mismatched (dots fall into wrong cavities) | Two plates are from different generation runs | Print and use the embossing plate and counter plate from the **same** generator export. |

### 9.4 Known limitations (call out, don't hide)

- **About 13 braille characters per line** on the cylinder. Most full business cards must be trimmed before they will fit. Recommended priority order: Name → at least one contact method → job title → mailing address → fax number.
- **Card-thickness rule:** the plate pair must match the card thickness exactly (0.3 mm or 0.4 mm). A 0.3 mm counter plate with 0.4 mm card produces shallow dots; a 0.4 mm counter plate with 0.3 mm card may not contact at all.
- **Slicer baseline only:** the cylinder print settings in [Section 8](#8-cylinder-print-settings-block-copy-paste-verbatim) are tested on **Bambu Studio + Bambu Lab X1C**. Other slicers will need equivalent tuning.
- **No quantitative dot-height measurement yet** - V1.0 was verified by reading; a feeler-gauge / micrometer pass is on the V1.1 roadmap.
- **No motorised drive** - this is intentionally a hand-operated device; users with very limited grip strength may need a longer Handle Connector (V1.1+) or an alternative tool.

---

## 10. Attribution, licensing, tags, categories

### 10.1 Attribution

- **Device designed by Brennen Johnston.**
- **Plate generator code** (used to produce the example plates included in this repo, and vendored locally at [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative)) is from the companion projects [`braille-cylinder-stl-generator`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator) (web-based, primary) and [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) (OpenSCAD, alternative), also by Brennen Johnston.
- **Braille translation** in the web app is powered by the open-source [Liblouis](https://liblouis.io/) library.
- **Documentation template** by Makers Making Change / Neil Squire Society, used under CC BY-SA 4.0: <https://github.com/makersmakingchange/OpenAT-Template>.

### 10.2 Licensing (verbatim block; disclose all four in the description on every platform)

> **This is an open-hardware project. Multiple licenses apply by component:**
>
> - **Hardware (everything needed to design, make, test, or prepare the device):** [CERN-OHL-W v2](https://cern.ch/cern-ohl).
> - **Documentation, photos, videos, written tutorials (accompanying material):** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
> - **Project software / scripts (where applicable):** [GPL-3.0-or-later](https://www.gnu.org/licenses/gpl.html).
> - **Customizer software (deployed web app *and* the vendored OpenSCAD copy in this repo):** [PolyForm Noncommercial 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0) - free for personal, educational, and non-commercial use; commercial use is not permitted.
>
> Each marketplace only lets you pick one CC-style license per listing. The closest umbrella match is **CC BY-NC-SA** (matching the maker's existing WATAP marketplace style); the disclosure above clarifies the exact per-component licenses.

### 10.3 Tag baseline (trim per platform's tag limit)

`braille`, `accessibility`, `assistive-technology`, `embosser`, `vision-impairment`, `blindness`, `business-card`, `educational`, `openat`, `no-fasteners`, `customizable`, `hand-operated`, `3d-printable`, `openscad`, `braille-embosser`.

### 10.4 Category proposals

- **MakerWorld:** Education > Other Education Models (matches the maker's existing WATAP listing).
- **Printables:** Tools (single-pick; as published on the live listing). Secondary candidate: Education.
- **Thingiverse:** Tools or Education (single-pick).

### 10.5 Designer / account attribution

> Use **Brennen Johnston** in formal listing fields and metadata. In body copy, **Brennen** is fine when a more natural voice reads better. Keep **WATAP** as background context or cross-link context, not as the primary listing identity for this release.

---

## 11. Outstanding gaps before publishing

> The major binary assets (10 device STLs, 2 sliced X1C `.3mf` profiles plus their companion slicer-settings markdown files, 4 example plate STLs, lead photo, 15 raw `DSC_*.jpg` photos, 3 YouTube tutorial mirrors + `.srt`, CAD source, CSV BOM) are **already present**. The actual remaining gaps are smaller and listed below. Do not let the published platform copy promise files or numbers that are not yet finished.

### 11.1 Hard blockers (must be closed before pasting into live platforms)

| # | Gap | Where to fix | Owner |
|---|---|---|---|
| G1 | **Documentation PDFs not yet exported.** Markdown drafts and `.docx` working copies exist for the Maker Guide, User Guide, Quickstart Guide, Summary, Design Rationale, and BOM, but `.pdf` versions referenced from [README.md](../../README.md), [okh.yml](../../okh.yml), and the platform posts still need a Save-As-PDF pass per [`_template_reference/COMPLIANCE_CHECKLIST.md`](../../_template_reference/COMPLIANCE_CHECKLIST.md) items 3-7. Until the PDFs exist, the platform posts should link to the markdown source on GitHub or temporarily attach the `.docx` working copies where the platform allows it. | `Documentation/` | Maker |
| G2 | **BOM mass / time TBDs - DONE for the included profiles.** Both included `.3mf` profiles have been sliced on a Bambu Lab X1C with Bambu Lab PLA Basic and the figures are now reflected in the BOM, Maker Guide §8.2, Summary cost table, User Guide §3, and all three platform copies. Assembly profile (`Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf`): **268.81 g**, **8 h 44 min** - see [`Braille_Embosser_Assembly_Slicer_Settings.md`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Braille_Embosser_Assembly_Slicer_Settings.md#slicing-result-bambu-lab-x1c--pla-basic). Cylinder HQ profile (`Embossing and Counter Cylinder High Quality.3mf`): **24.68 g**, **3 h 5 min** - see [`Embossing_Counter_Cylinder_HQ_Slicer_Settings.md`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Embossing_Counter_Cylinder_HQ_Slicer_Settings.md#slicing-result-bambu-lab-x1c--pla-basic). **Combined per device + one plate pair: 293.49 g / ~11 h 49 min / ~$7.34.** Only remaining TBDs are the per-part rows P01-P10 and P11-P12 in the BOM and Maker Guide §8.2, which are not needed for the platform copy because the multi-object profiles do not produce per-part figures; slice individual STLs only if you want a per-part breakdown. | `.3mf` files | Maker |
| G3 | **Real printed-result cover photo per Print Profile (MakerWorld 2026-Feb-05 rule).** A lead photo exists at `Photos/Custom_Braille_Embosser.jpg`. Audit the 15 raw `Photos/DSC_*.jpg` files and decide which ones cover (a) the assembled device, (b) the cylinder pair on its own, (c) an embossed-output close-up, and (d) a parts-spread / exploded view. Reshoot any of those four shots that are not already covered. | `Photos/` | Maker |
| G4 | **Embossed-output close-up.** Almost certainly a gap in the current `Photos/` set. Required for the MakerWorld 2026 rule and for credibility on every platform. | `Photos/` | Maker |
| G5 | **Photo / diagram TODOs inside the docs.** [Maker Guide Section 10](Custom_Braille_Embosser_Maker_Guide.md#10-examples-of-quality-prints) and [User Guide Section 2](Custom_Braille_Embosser_User_Guide.md#2-labelled-features) currently flag user-action TODOs to insert labelled photos. Either resolve before linking these sections verbatim from the platform copy, or skip linking those sections. | `Documentation/_drafts/` | Maker |

### 11.2 Editorial decisions and current defaults

| # | Question | Default | Where it matters |
|---|---|---|---|
| E1 | **Listing identity** | Use **Brennen Johnston** in formal fields. Use **Brennen** in body copy where a more natural voice reads better. | Byline on every listing; credit wording; cross-link placement. |
| E2 | **Cross-slicer wording.** Should the Section 8 block stay framed as the *Bambu Studio + X1C tested baseline only*, or should the listing add equivalent Cura / OrcaSlicer / PrusaSlicer wording? | Stay framed as Bambu-only. Do not generalise without testing. | Section 8 of this pack and every platform variant. |
| E3 | **PolyForm Noncommercial visibility.** The deployed web customizer and the vendored OpenSCAD copy are PolyForm Noncommercial 1.0.0. Make this visible in every platform's description so the licensing split is not lost in shorter copy. | Disclose explicitly in every Description body, even if the platform's License tag is a CC option. | Section 10.2 of this pack. |
| E4 | **Customizer framing.** Keep the browser customizer as the default recommendation in every listing. Present the OpenSCAD customizer as the offline / power-user backup, framed verbatim as *"for anyone not wanting to, or not able to, use the browser-based tool"*. The "or not able to" clause is intentional and **should not be edited out**. | Use the framing verbatim. | Section 7 of this pack. |
| E5 | **MMC wording while no device URL exists.** | Omit direct MMC listing references from the marketplace copy until the official URL exists. | README follow-up, future MMC-specific copy, and any live marketplace text. |
| E6 | **Cross-link strategy.** | Yes. Add a short cross-link to the existing WATAP *"Better Braille Alphabet Board (No Heading Title)"* listing for context. | MakerWorld and any platform where external context links make sense. |
| E7 | **Boost / commercial-incentive eligibility.** | Not applicable for this listing. Do not plan around Boost or similar incentive programs. | MakerWorld upload manifest and publish checklist. |

### 11.3 Once everything in 11.1 and 11.2 is resolved

1. Edit this pack with the resolved values (mass, time, photo filenames, account, license tag, cross-links).
2. Re-derive the three platform copies (`MakerWorld_Post_Copy.md`, `Printables_Post_Copy.md`, `Thingiverse_Post_Copy.md`).
3. Run a final consistency pass across titles, file names, links, supported card thicknesses, license tagging, customizer recommendations, and the "OpenSCAD as backup for anyone not wanting to or not able to use the browser tool" framing across the three platform variants.
4. Paste each platform copy into the live platform, attach the files per the upload manifest, and publish.

---

## 12. Video embed snippets

> The full source for these snippets lives in [`Video_Tutorials/README.md`](../../Video_Tutorials/README.md). Reuse the snippets there verbatim instead of rewriting.

### 12.1 Quick reference (YouTube)

| # | Topic | YouTube short URL | Long URL (use for "Add Video" form fields) |
|---|---|---|---|
| 1 | Customizing braille / downloading STLs / 3D-print settings | <https://youtu.be/m71VNZq28MI> | `https://www.youtube.com/watch?v=m71VNZq28MI` |
| 2 | Assembling the 3D-printed parts | <https://youtu.be/x-uPNtT2Gqk> | `https://www.youtube.com/watch?v=x-uPNtT2Gqk` |
| 3 | Using the completed Custom Braille Embosser | <https://youtu.be/77iXvJbkXh4> | `https://www.youtube.com/watch?v=77iXvJbkXh4` |

### 12.2 Markdown link block (paste into Printables / GitHub / MakerWorld description / Thingiverse)

```markdown
**Tutorial videos:**

1. [Customizing braille, downloading STLs, 3D-print settings (YouTube)](https://youtu.be/m71VNZq28MI)
2. [Assembling the 3D-printed parts (YouTube)](https://youtu.be/x-uPNtT2Gqk)
3. [Using the completed Custom Braille Embosser (YouTube)](https://youtu.be/77iXvJbkXh4)
```

### 12.3 Thumbnail-style markdown (Printables / blogs - falls back gracefully if the auto-embed fails)

```markdown
[![Video 1 thumbnail](https://img.youtube.com/vi/m71VNZq28MI/hqdefault.jpg)](https://youtu.be/m71VNZq28MI)
[![Video 2 thumbnail](https://img.youtube.com/vi/x-uPNtT2Gqk/hqdefault.jpg)](https://youtu.be/x-uPNtT2Gqk)
[![Video 3 thumbnail](https://img.youtube.com/vi/77iXvJbkXh4/hqdefault.jpg)](https://youtu.be/77iXvJbkXh4)
```

### 12.4 Bonus CAD-driven assembly simulation (no narration)

A no-narration `Braille_Embosser_Assembly_Video_Simulation_2.mp4` (~10 MB) is available as a supplemental marketing clip - usable as an extra video upload on MakerWorld / Printables, or as an animated GIF / loop on social media.

---

## 13. Per-platform deviation summary

> For full per-platform copy and the upload manifest, see the four derived files in this folder. This section is a quick "what's different per platform" cheat-sheet so the master pack stays the canonical source.

| Aspect | MakerWorld | Printables | Thingiverse |
|---|---|---|---|
| Description length | Long-form (story-driven) | Sectioned per Printables template | Tighter; description does more work |
| Print Profile structure | 2 separate Print Profiles, each with its own description + photos + structured settings | 2 `.3mf` files attached together as a "Print profiles" group alongside STLs | `.3mf` files as supplementary downloads; users pick STLs to slice individually |
| Print-Profile photo rule | **Per-Profile real printed photo required (effective 2026-Feb-05)** | Encouraged, not strictly required | Encouraged, not strictly required |
| Video embed method | Dedicated "Add Video" field, long YouTube URL | "Add Video" field (auto-embeds YouTube URL) + thumbnail markdown fallback in description | Paste YouTube watch URLs directly into the description (Thingiverse auto-converts) |
| Tag count cap | Generous; use the full baseline set | Moderate; trim to ~10 most relevant | Tighter; trim to ~5-8 most relevant |
| License picker | Single CC option in dropdown; disclose the full split in description | Single license in dropdown; disclose split in description | Single CC option in dropdown; disclose split in description; attach BOM + Guides as supplementary documents |
| BOM / Guide attachment | Markdown links in description; attach PDFs when ready | Attach PDFs as supplementary downloads when ready | **Attach BOM CSV and User/Maker Guide PDFs** in the supplementary-document slot - Thingiverse doesn't auto-render the same structured detail, so the description and attachments do more work |

---

## 14. Maintenance plan after first publish

- Whenever [`CHANGES.txt`](../../CHANGES.txt) gets a new entry (e.g. a V1.1 release), update this master pack first, then re-derive the three platform-specific docs in this folder, then push the updated copy to each platform.
- Treat this pack as the **only** place you edit description content. The three platform-specific docs and the asset checklist / upload manifest are **derived** files.
- Re-run the photo audit before each major version (V1.1+) so the lead-photo / per-Print-Profile-photo rule still holds with the latest device.
