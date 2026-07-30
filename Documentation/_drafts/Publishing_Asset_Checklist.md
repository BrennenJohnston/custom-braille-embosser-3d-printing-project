# Custom Braille Embosser - Publishing Asset Checklist

> **Derived from:** [`Custom_Braille_Embosser_Publishing_Pack.md`](Custom_Braille_Embosser_Publishing_Pack.md).
> **Purpose:** capture what strong MakerWorld / Printables / Thingiverse listings include, and mark which of those assets are already in the repo vs. still missing.
> **Use:** work top-to-bottom; nothing under "must-have to publish" should be left blank when copy is pasted into the live platforms.

---

## Status legend

- DONE - asset is already in the repo at the cited path and is good enough to publish.
- USE-EXISTING - asset exists, but the maker should pick which of several candidates to use (e.g. choose from `Photos/DSC_*.jpg`).
- RESHOOT - asset is **missing or weak**; capture a new one before publishing.
- DECIDE - editorial decision required from the maker (not a missing file).
- PDF-PENDING - the underlying markdown content is complete; only a `.docx` → `.pdf` export pass is needed.

---

## 1. Photos (highest-impact for marketplace ranking)

### 1.1 Must-have to publish

| Slot | Where it shows | Status | Source / target |
|---|---|---|---|
| Lead cover photo (1000 px wide, real printed object) | All 3 platform cover thumbnails | DONE | [`Photos/Custom_Braille_Embosser.jpg`](../../Photos/Custom_Braille_Embosser.jpg) (1000x563, 122 KB) |
| Real printed photo for **MakerWorld Print Profile 1 (X1C all parts)** *(MakerWorld 2026-Feb-05 rule)* | MakerWorld Print Profile 1 cover | USE-EXISTING | Audit `Photos/DSC_8524.jpg`, `DSC_8542.jpg`, `DSC_8561.jpg`-`DSC_8590.jpg` for "assembled finished device" shot. If none reads as the *fully assembled, all-parts-printed* unit at thumbnail scale, RESHOOT. |
| Real printed photo for **MakerWorld Print Profile 2 (X1C cylinder pair, High Quality)** | MakerWorld Print Profile 2 cover | RESHOOT (likely) | Need a clean shot of the cylinder pair on its own (preferably next to a freshly embossed card). |
| Embossed-output close-up on a card | All 3 platform galleries | RESHOOT (likely) | Almost certainly a gap. A clear photo of a finished embossed card (raking light works best for visible dots). |
| Parts-spread / exploded-layout photo | All 3 platform galleries | RESHOOT or RENDER | Either reshoot a real "parts laid out on a table" photo, or render a labelled exploded view from [`Design_Files/CAD_Design_Files/Fusion/Braille Embosser Assembly v1.0.f3z`](../../Design_Files/CAD_Design_Files/Fusion/Braille%20Embosser%20Assembly%20v1.0.f3z). |

### 1.2 Strong-to-have (improves ranking and conversion)

| Slot | Where it shows | Status | Source / target |
|---|---|---|---|
| In-use shot (someone embossing a card) | All 3 platform galleries | USE-EXISTING or RESHOOT | Try `Photos/DSC_8569.jpg`, `DSC_8570.jpg`, `DSC_8572.jpg`, `DSC_8575.jpg` first; reshoot if no clean in-use frame exists. |
| Multiple-card / multi-message demo | MakerWorld + Printables galleries | RESHOOT | Lay out 2-4 cards each embossed with a different message. Demonstrates the "content-agnostic" angle. |
| Customizer screenshot (browser app) | Printables description; MakerWorld Print Profile 2 | RESHOOT | Browser screenshot of <https://braille-cylinder-stl-generator.vercel.app> showing the text input and the live 3D preview. |
| OpenSCAD customizer screenshot | Printables description | RESHOOT (optional) | Screenshot of the OpenSCAD Customizer panel for makers who pick the OpenSCAD path. |
| Open-graph banner (GitHub social preview, 1280x640) | GitHub repo only | USE-EXISTING | Template at [`Photos/repository-open-graph-template.png`](../../Photos/repository-open-graph-template.png). Optional - replace with a Custom Braille Embosser banner before configuring as GitHub social-preview. |

### 1.3 Photo audit against the 15 raw `DSC_*.jpg` files

> Action: open each of these once, then tag in the table below.

| File | Size | Likely-good for | Maker's pick |
|---|---|---|---|
| `DSC_8524.jpg` | 9.2 MB | Source of the resized `Custom_Braille_Embosser.jpg` lead photo - reuse as the hi-res variant. | [TODO] |
| `DSC_8542.jpg` | 5.4 MB | Hi-res candidate for the assembled-device alt angle. | [TODO] |
| `DSC_8561.jpg` | 1.4 MB | Audit | [TODO] |
| `DSC_8562.jpg` | 1.5 MB | Audit | [TODO] |
| `DSC_8566.jpg` | 1.4 MB | Audit | [TODO] |
| `DSC_8567.jpg` | 1.4 MB | Audit | [TODO] |
| `DSC_8569.jpg` | 1.5 MB | Likely an in-use / hand-on-handle shot. | [TODO] |
| `DSC_8570.jpg` | 1.3 MB | Audit | [TODO] |
| `DSC_8572.jpg` | 0.9 MB | Audit | [TODO] |
| `DSC_8575.jpg` | 2.6 MB | Audit | [TODO] |
| `DSC_8578.jpg` | 1.9 MB | Audit | [TODO] |
| `DSC_8582.jpg` | 1.9 MB | Audit | [TODO] |
| `DSC_8583.jpg` | 2.2 MB | Audit | [TODO] |
| `DSC_8586-2.jpg` | 2.8 MB | Audit | [TODO] |
| `DSC_8590.jpg` | 8.1 MB | Hi-res candidate. | [TODO] |

---

## 2. File package (downloads listed on each platform)

| Asset | Status | Path / source |
|---|---|---|
| 10 device STLs | DONE | [`Build_Files/3D_Printing_Files/STL/`](../../Build_Files/3D_Printing_Files/STL/) |
| 4 example plate STLs (0.3 + 0.4 pairs) | DONE | [`Build_Files/3D_Printing_Files/Embossing_Plates_Examples/`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Examples/) |
| `.3mf` - Bambu X1C, all parts | DONE | [`Build_Files/3D_Printing_Files/Print_Profiles/X1C/Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Braille%20Embosser%20Assembly%20v1.0%20%280.2%20Layer%20Height%29.3mf) |
| `.3mf` - Bambu X1C, cylinder pair HQ | DONE | [`Build_Files/3D_Printing_Files/Print_Profiles/X1C/Embossing and Counter Cylinder High Quality.3mf`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Embossing%20and%20Counter%20Cylinder%20High%20Quality.3mf) |
| Slicer settings markdown - X1C assembly profile | DONE | [`Build_Files/3D_Printing_Files/Print_Profiles/X1C/Braille_Embosser_Assembly_Slicer_Settings.md`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Braille_Embosser_Assembly_Slicer_Settings.md) |
| Slicer settings markdown - X1C cylinder HQ profile | DONE | [`Build_Files/3D_Printing_Files/Print_Profiles/X1C/Embossing_Counter_Cylinder_HQ_Slicer_Settings.md`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Embossing_Counter_Cylinder_HQ_Slicer_Settings.md) |
| CAD source - Fusion `.f3z` | DONE | [`Design_Files/CAD_Design_Files/Fusion/Braille Embosser Assembly v1.0.f3z`](../../Design_Files/CAD_Design_Files/Fusion/Braille%20Embosser%20Assembly%20v1.0.f3z) |
| CAD source - STEP (5 files) | DONE | [`Design_Files/CAD_Design_Files/STEP/`](../../Design_Files/CAD_Design_Files/STEP/) |
| CAD source - OBJ + MTL (10 parts) | DONE | [`Design_Files/CAD_Design_Files/OBJ/`](../../Design_Files/CAD_Design_Files/OBJ/) |
| Bill of Materials (CSV) | DONE (both `.3mf` profiles sliced on X1C + PLA Basic: device 268.81 g / 8 h 44 min, plate pair 24.68 g / 3 h 5 min, combined 293.49 g / ~11 h 49 min / ~$7.34. Per-part rows P01-P10 and P11-P12 individually remain TBD - only needed for a per-part breakdown) | [`Documentation/Custom_Braille_Embosser_BOM.csv`](../Custom_Braille_Embosser_BOM.csv) |
| Maker Guide PDF | PDF-PENDING (markdown done) | Source: [`Documentation/_drafts/Custom_Braille_Embosser_Maker_Guide.md`](Custom_Braille_Embosser_Maker_Guide.md) → target `Documentation/Custom_Braille_Embosser_Maker_Guide.pdf` |
| User Guide PDF | PDF-PENDING | [`Documentation/_drafts/Custom_Braille_Embosser_User_Guide.md`](Custom_Braille_Embosser_User_Guide.md) → `Documentation/Custom_Braille_Embosser_User_Guide.pdf` |
| Quickstart Guide PDF | PDF-PENDING | [`Documentation/_drafts/Custom_Braille_Embosser_Quickstart_Guide.md`](Custom_Braille_Embosser_Quickstart_Guide.md) → `Documentation/Custom_Braille_Embosser_Quickstart_Guide.pdf` |
| Design Rationale PDF | PDF-PENDING | [`Documentation/_drafts/Custom_Braille_Embosser_Design_Rationale.md`](Custom_Braille_Embosser_Design_Rationale.md) → `Documentation/Custom_Braille_Embosser_Design_Rationale.pdf` |
| Summary PDF | PDF-PENDING | [`Documentation/_drafts/Custom_Braille_Embosser_Summary.md`](Custom_Braille_Embosser_Summary.md) → `Documentation/Custom_Braille_Embosser_Summary.pdf` |
| 3 YouTube tutorials | DONE | <https://youtu.be/m71VNZq28MI>, <https://youtu.be/x-uPNtT2Gqk>, <https://youtu.be/77iXvJbkXh4> |
| Local `.mp4` + `.srt` mirrors of all 3 tutorials | DONE | [`Video_Tutorials/Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/`](../../Video_Tutorials/Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/), `Video_2_...`, `Video_3_...` |
| Bonus CAD assembly simulation (no narration) | DONE | [`Video_Tutorials/Braille_Embosser_Assembly_Video_Simulation_2.mp4`](../../Video_Tutorials/Braille_Embosser_Assembly_Video_Simulation_2.mp4) (~10 MB) |
| Web customizer link | DONE | <https://braille-cylinder-stl-generator.vercel.app> |
| OpenSCAD customizer source (vendored locally) | DONE | [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/) |
| Accessible OpenSCAD UI link | DONE | <https://github.com/BrennenJohnston/openscad-assistive-forge> |

---

## 3. Listing metadata

| Item | Status | Notes |
|---|---|---|
| Title (`Custom Braille Embosser - Hand-Operated 3D-Printable Braille Card Maker`) | DONE | Trim to each platform's character cap. |
| Tagline / Summary (1-sentence) | DONE | Verbatim from Publishing Pack §1.3. |
| Tag baseline (15 tags) | DONE | Trim to platform cap (~15 / ~10 / ~5-8 for MW / PR / TV respectively). |
| Category proposal per platform | DONE | MakerWorld: Education > Other Education Models. Printables: Education. Thingiverse: Tools or Education. |
| License (per-platform single dropdown) | DONE | CC BY-NC-SA per platform; full license split disclosed in description. |
| Designer / account decision | DONE | Use **Brennen Johnston** in formal listing fields. Use **Brennen** in prose where it reads better. Keep WATAP only as background or cross-link context. |

---

## 4. Print Settings (structured-form fields)

> Same values on all three platforms. Populate the platform's structured "Print Settings" / "Filaments" widget in addition to writing them in the description.

| Field | Value |
|---|---|
| Layer height | 0.2 mm |
| Wall loops | 3 for device parts; switch to **Arachne** for the cylinders |
| Infill | 30 % gyroid (PLA) or 20 % gyroid (PETG) |
| Supports | Tree / organic, only on overhangs >55° on Body Base / Body Top. **None on the cylinders.** |
| Brim | 5 mm on Handle Grip + Handle Connector. **None on the cylinders.** |
| Filament | PLA (default) or PETG; **~269 g per device** (8 h 44 min on Bambu Lab X1C with PLA Basic) + **~25 g per plate pair** (3 h 5 min on the same printer/material). Combined: ~293 g and ~11 h 49 min for one device + one plate pair. |
| Recommended printer | Bambu Lab X1C (`.3mf` provided); any FDM ≥ 220x220x200 mm |
| **Cylinder block (Bambu Studio + X1C tested baseline)** | See Publishing Pack §8 - paste verbatim |

---

## 5. Card-stock / use guidance

| Item | Status |
|---|---|
| Supported card thicknesses **0.3 mm** and **0.4 mm** | DONE |
| Plate pair **must** match card thickness | DONE - emphasised in every variant |
| Recommend shipping at least one printed plate pair + a starter pack of card stock | DONE - in Publishing Pack §6 and each platform variant |

---

## 6. Video embed strategy per platform

| Platform | How videos are added | Status |
|---|---|---|
| MakerWorld | Long YouTube URL via the dedicated "Add Video" field (3 entries) | DONE - URLs ready in Publishing Pack §12 |
| Printables | "Add Video" field (auto-embeds YouTube URL) + markdown thumbnail fallback in the description | DONE - thumbnail block in Publishing Pack §12.3 |
| Thingiverse | Paste long YouTube watch URLs directly into the description (Thingiverse auto-converts) | DONE - long URLs in Publishing Pack §12.1 |

---

## 7. `.3mf` strategy per platform

| Platform | Strategy | Status |
|---|---|---|
| MakerWorld | 2 separate Print Profiles, each with its own description + photos + structured settings | Copy ready in [`MakerWorld_Post_Copy.md`](MakerWorld_Post_Copy.md) §C/D |
| Printables | 2 `.3mf` files attached as "Print profiles" group + STLs available individually | Copy ready in [`Printables_Post_Copy.md`](Printables_Post_Copy.md) |
| Thingiverse | `.3mf` files attached as supplementary downloads; users slice STLs individually | Copy ready in [`Thingiverse_Post_Copy.md`](Thingiverse_Post_Copy.md) |

---

## 8. Hard blockers consolidated (from Publishing Pack §11.1)

| # | Blocker | Status | Resolution path |
|---|---|---|---|
| G1 | Documentation PDFs not yet exported | OPEN | `.docx` → Save As PDF for Maker / User / Quickstart / Design Rationale / Summary (per [Compliance Checklist items 3-7](../../_template_reference/COMPLIANCE_CHECKLIST.md)). |
| G2 | BOM mass / time TBDs | DONE (per-`.3mf`-profile level) | Both included profiles sliced on X1C + PLA Basic. Assembly: **268.81 g / 8 h 44 min** ([`Braille_Embosser_Assembly_Slicer_Settings.md`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Braille_Embosser_Assembly_Slicer_Settings.md#slicing-result-bambu-lab-x1c--pla-basic)). Cylinder pair: **24.68 g / 3 h 5 min** ([`Embossing_Counter_Cylinder_HQ_Slicer_Settings.md`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Embossing_Counter_Cylinder_HQ_Slicer_Settings.md#slicing-result-bambu-lab-x1c--pla-basic)). Per-part rows P01-P10 and P11-P12 individually remain TBD - not needed for platform copy. |
| G3 | Per-Print-Profile real printed photo (MakerWorld 2026-Feb-05 rule) | OPEN | Audit `Photos/DSC_*.jpg` and reshoot the (a) assembled device, (b) cylinder pair, (c) embossed-output close-up, (d) parts-spread shots not covered. |
| G4 | Embossed-output close-up photo | OPEN | Reshoot with raking light on a freshly embossed card. |
| G5 | Photo / diagram TODOs inside docs | OPEN | Resolve before linking Maker Guide §10 / User Guide §2 verbatim, or skip linking those sections from platform copy. |

---

## 9. Editorial decisions consolidated (from Publishing Pack §11.2)

| # | Decision | Default | Status |
|---|---|---|---|
| E1 | Listing identity | Use **Brennen Johnston** in formal fields and **Brennen** in body copy where it reads better | DONE |
| E2 | Cross-slicer wording | Stay Bambu-only | DONE in pack and platform copies |
| E3 | PolyForm Noncommercial visibility | Disclose explicitly | DONE in pack and platform copies |
| E4 | Customizer framing - "for anyone not wanting to, *or not able to*, use the browser-based tool" | Use verbatim | DONE - verbatim in pack and all 3 platform copies |
| E5 | MMC wording while no device URL exists | Omit direct MMC listing references from the marketplace copy until the official URL exists | DONE |
| E6 | Cross-link to existing WATAP listing | Add a short cross-link for context | DONE |
| E7 | Boost / commercial-incentive eligibility on MakerWorld | Not planning to use Boost or similar incentive programs for this listing | DONE |

---

## 10. Final consistency pass (run before pasting into any live platform)

- [ ] All three platform copies use the same title (modulo platform character cap).
- [ ] All three platform copies use the same file inventory and file names.
- [ ] All three platform copies use the same external links (web customizer URL, GitHub repo URL, all 3 YouTube URLs, OpenSCAD upstream).
- [ ] All three platform copies mention both supported card thicknesses (0.3 mm and 0.4 mm) and the plate-pair-must-match rule.
- [ ] All three platform copies disclose the full license split (CERN-OHL-W v2 / CC BY-SA 4.0 / GPL-3.0-or-later / PolyForm Noncommercial 1.0.0) even when the dropdown is a single CC option.
- [ ] All three platform copies present the OpenSCAD customizer with the verbatim *"for anyone not wanting to, or not able to, use the browser-based tool"* framing.
- [ ] All three platform copies present the cylinder print-settings block verbatim and clearly tagged as a Bambu Studio + X1C tested baseline.
- [ ] All three platform copies match the [`Publishing_Upload_Manifest.md`](Publishing_Upload_Manifest.md) - **the description does not promise files that are not actually attached**.
