# Custom Braille Embosser - Design Rationale

> **Document version:** 1.0 | 2026-May-31
> **Designer:** Brennen Johnston
> **Status:** Released, V1.0.0

---

## 1. Introduction

### 1.1 Purpose
This document records *why* the Custom Braille Embosser is designed the way it is, what alternatives were considered, and what the design's known limitations are. It is the long-form companion to the BOM, Maker Guide, and User Guide.

### 1.2 Background
Producing tactile braille is a routine but expensive task for the global blind and vision-impaired community. The standard tools fall into three rough cost tiers:

| Tier | Tool | Approx. unit cost (USD, 2026) | Notes |
|---|---|---|---|
| Low | Slate and stylus | $10 - $30 | Slow, requires reverse-mirror typing, mostly for short labels. |
| Mid | Manual hand-frame braillers (Perkins-style) | $700 - $1,500 | Mechanically complex, heavy, hard to ship internationally, expensive. |
| High | Electronic embossers (Index, ViewPlus, etc.) | $2,000 - $5,000+ | Fastest; price puts them out of reach for individuals and most schools outside well-funded districts. |

Existing community / DIY projects (e.g. various MMC braille labellers, Hot Dots adhesive systems, hand-rolled "Braille Buddy" prototypes) generally produce one fixed message per device, or one character at a time, and do not include a parametric pipeline for arbitrary text.

The Custom Braille Embosser was designed to fit a fourth tier:

- **Cost:** under $10 USD per device in raw filament.
- **Manufacturing:** any FDM printer; no fasteners, no electronics, no PCB.
- **Customisation:** any text, in Grade-1 or Grade-2 braille, generated parametrically.
- **Repair:** every part is reprintable.

## 2. Requirements

### 2.1 Functional requirements

| ID | Requirement |
|---|---|
| F1 | The device shall emboss legible, permanent, raised braille onto card stock by hand operation only. |
| F2 | The braille content shall be interchangeable: a different message can be embossed by swapping the embossing plate. |
| F3 | The device shall support at least two card-stock thicknesses (0.3 mm and 0.4 mm). |
| F4 | The braille produced shall conform to standard braille cell geometry (dot diameter, dot height, cell spacing) for at least one common standard (e.g. North American). |
| F5 | The device shall be operable with one hand on the handle and one hand stabilising the body. |

### 2.2 Non-functional requirements

| ID | Requirement |
|---|---|
| N1 | Cost: total filament cost per device shall be under **$10 USD** at $25/kg PLA. |
| N2 | Print volume: every part shall fit within a **220 x 220 x 200 mm** build volume. |
| N3 | Manufacturing complexity: assembly shall require **no fasteners, glue, springs, or solder**. |
| N4 | Operating force: shall be comfortable for a typical adult user (no hard maximum specified for v1.0; see opportunities for improvement). |
| N5 | Source format: design shall be released in an editable parametric format (Fusion 360 `.f3z`) plus a neutral STEP. |

### 2.3 Constraints

| ID | Constraint |
|---|---|
| C1 | The device must be reproducible from this repository alone, plus a companion repository for plate generation. No proprietary or paywalled software shall be required. |
| C2 | All printable parts must be free of overhangs requiring large support structures (Fusion 360 part orientation in the included `.3mf` profiles satisfies this). |
| C3 | Assembly must be possible without a workbench (i.e. on a tabletop, by hand). |

## 3. Research Summary

### 3.1 Commercial reference devices
- **Perkins Brailler (1951-present):** the de-facto standard hand-cranked brailler. Mature, heavy (~5 kg), expensive, hard to repair, dependent on machined-steel internals. Inspirational for the per-cell positive/negative-die concept, but not directly reproducible by FDM printing.
- **Slate and stylus:** simplest possible braille writing tool; inexpensive, but requires the user to type in mirror and right-to-left. Not a model the Custom Braille Embosser tries to imitate.
- **Hot Dots / 3M heat-activated braille tape:** thermally-activated raised dots; ergonomically simple but consumable-driven and language-dependent.

### 3.2 DIY / community reference designs
- Several MMC-style and Thingiverse-style "braille labellers" using laser-cut plates or stamped Lego-like dies.
- DIY hand-frames using nuts and bolts.
- None known (at the time of v1.0) provide a fully parametric, FDM-printable, content-agnostic plate-driven embosser with a parametric plate generator. **This design fills that gap.**

### 3.3 Reference braille standards
The plate generator is parameterised on dot diameter, dot height, dot-to-dot spacing within a cell, and cell-to-cell spacing. The included example plates use parameters consistent with common North American braille (cell pitch ~6.0-6.4 mm). Other standards (UEB, Marburg Medium, Japanese tenji) can be supported by adjusting the generator parameters - see "Opportunities for Improvement", below.

## 4. Ideation

### 4.1 Concept directions considered
1. **Stamp-and-anvil per cell** - one cell at a time, like a hand stamp.
2. **Roller-die ("rolling pin")** - a continuous pair of cylinders rolling across the card. ✓ chosen
3. **Stack-of-fixed-dots** - a long flat embosser plate; press straight down.
4. **Heat-activated raised material** - print a "stamp" that lays a dot of UV resin or hot melt.

### 4.2 Selection
The roller-die approach (option 2) was chosen because:
- It allows arbitrary-length messages (limited by cylinder length, not by stack height).
- The user-applied force at any instant is small (only one cell-pair is in contact at a time), so the device can be hand-operated comfortably.
- It is mechanically simple - **no springs, no detents, no ratchet** - and the force is limited by the stiffness of the printed parts.
- It is fully producible by FDM printing (no machined cylinders).

## 5. Conceptual Designs

### 5.1 Sub-assembly breakdown
The chosen architecture decomposes into four sub-assemblies, each independently printable and replaceable:

| Sub-assembly | Parts (from BOM) | Function |
|---|---|---|
| **Body** | P01 Body Base + P02 Body Top | Encloses the plate-holder sub-assemblies; defines the card slot. |
| **Embosser pair (Cylinder Roller Holder, embossing side)** | P03 Embosser Holder A1 + P04 Embosser Holder A2 + P11 Embossing Plate (printed separately) | Holds and rotates the embossing-plate cylinder. |
| **Counter pair (Cylinder Roller Holder, counter side)** | P05 Counter Holder B1 + P06 Counter Holder B2 + P12 Universal Counter Plate (printed separately) | Holds and rotates the counter-plate cylinder. |
| **Grip Extension** | P07 Grip Extension Bottom + P08 Grip Extension Top | Provides ergonomic grip on the body side. |
| **Handle** | P09 Handle Connector + P10 Handle Grip | Lever the user squeezes; transfers force to roll the cylinders. |

This decomposition matches the four neutral STEP files included (`Body…`, `Cylinder Roller Holder…`, `Grip Extension…`, `Handle Connector and Handle Grip…`) and makes targeted future revisions tractable - a redesigned Handle, for example, does not change the Body geometry.

## 6. Prototyping Log (Summary)

> The Fusion 360 file at `Design_Files/CAD_Design_Files/Fusion/Braille Embosser Assembly v1.0.f3z` is the canonical V1.0 design and represents the result of multiple unreleased prototype iterations. Key prototype lessons that drove V1.0:

| Iteration outcome | What it taught the V1.0 design |
|---|---|
| Single-piece monolithic body | Hard to print without supports; replaced by the **two-half (Base + Top) snap-fit body** in V1.0. |
| Plates pressed directly into round holes in the body | Could not be replaced without disassembly; replaced by **two-piece snap-fit holder pairs** that can be removed with the plate. |
| Single embosser holder ring | Insufficient axial location; replaced by the **A1 + A2 / B1 + B2** mirrored-pair design. |
| Solid Handle Grip | Uncomfortable for long sessions; replaced by the **two-part Connector + Grip** design that allows alternative ergonomic grips to be drop-in replacements without changing the Body. |

## 7. Testing

| Test | Method | V1.0 result |
|---|---|---|
| Embossing legibility (0.3 mm card) | Emboss, then ask a sighted reader (with reference card) and a fluent braille reader to identify the cell pattern. | Pass: full-cell test pattern read correctly. |
| Embossing legibility (0.4 mm card) | As above with the 0.4 mm plate pair. | Pass. |
| Dot height vs. standard | Measure with feeler-style depth gauge or compare against a Perkins Brailler output. | Verified visually; quantitative measurement is an item for V1.1. |
| Snap-fit retention | Squeeze handle 100 times; check holders do not loosen. | Pass at 100 cycles; long-term cycle test is an item for V1.1. |
| Print reproducibility | Re-print and re-assemble on a different X1C unit using the included `.3mf`. | Pass. |

## 8. Detailed Design

### 8.1 Body (P01 + P02)
- Two-half, snap-fit clamshell.
- Each half includes a half-pocket that locates the corresponding plate-holder sub-assembly.
- Card slot is defined by the gap between the closed halves (0.3 mm or 0.4 mm depending on the loaded plate pair).
- Designed at 0.2 mm layer height with a 3-perimeter wall to ensure snap-fit features print accurately.

### 8.2 Cylinder Roller Holders (P03+P04 / P05+P06)
- Mirrored two-piece sleeves that snap around each end of a cylindrical plate.
- The pair locates rotationally in the Body, but the plate can spin freely within the holder.
- Designed so that the *holder* is generic (same STL across the embosser side and counter side could be considered for V1.1, currently distinct A/B pairs to avoid fit confusion).

### 8.3 Grip Extension (P07 + P08)
- Two-half snap-fit, attached to the user-side of the Body.
- Provides a longer purchase for the non-handle hand.
- Hollow internal volume keeps mass low.

### 8.4 Handle Connector + Handle Grip (P09 + P10)
- The Connector (P09) is a stub that snaps into the Body's handle socket and provides the structural lever.
- The Grip (P10) is a sleeve that slides over the Connector and locks via a snap rib. The Grip is the user-replaceable surface.
- Splitting the lever into Connector + Grip lets a maker print alternative ergonomic grips (textured, oversized, child-sized, etc.) without re-printing the whole handle.

### 8.5 Embossing & Counter Plates (P11 / P12)
Generated separately by the customizer (web-based primary, OpenSCAD alternative - see Section 8.6). The plate cylinders are designed so:
- The embossing plate has raised dots conforming to the chosen braille standard.
- The counter plate has matching cavities **plus** a thickness offset equal to the target card thickness, so that the active dot height equals the plate-pair gap minus the card thickness.

This is why **the plate pair must match the card thickness** - using a 0.3 mm counter plate with 0.4 mm card produces shallow dots; using a 0.4 mm counter plate with 0.3 mm card may not contact the card at all in some dots.

### 8.6 Customizer architecture - two officially supported paths

The plate generator is intentionally **decoupled** from the device: the device is content-agnostic, and the generator is a separate, parameterised pipeline. Two officially supported implementations of the same parameter set are provided so users can pick the path that fits their workflow without changing any device geometry.

| Path | Source repo | Local copy in this repo | Best for | Translation |
|---|---|---|---|---|
| **Primary - Web-based** | [`braille-cylinder-stl-generator`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator) | n/a (deployed at <https://braille-card-and-cylinder-stl-gener.vercel.app>) | Most users; auto-translates English to Grade 1 / Grade 2 braille across 50+ language tables; runs in any browser; STL generation runs locally in browser; screen-reader friendly. | Automatic via [Liblouis](https://liblouis.io/) |
| **Alternative - OpenSCAD** | [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) | [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative) | Offline use; full parametric control; existing OpenSCAD/CAD pipelines; batch processing. | Manual via <https://www.branah.com/braille-translator> (Unicode mode) |

Both paths are intentionally kept in **parameter parity**: the OpenSCAD `paper_thickness_preset` matches the web app's *Card Thickness* dropdown, and the same dot, spacing, and cylinder parameters are exposed in both. Files generated by either path are interchangeable in the device.

Why two paths instead of one:
- The web app meets the most common need (a sighted maker entering English text, or a screen-reader user entering text) with the smallest barrier to entry. It is the right default and the project documentation is structured around it.
- The OpenSCAD path is essential for offline use, for makers who want to inspect or extend the generator code, and for downstream automation (CI pipelines, batch generation, parameter sweeps). Vendoring a copy of the OpenSCAD code into this repo at `Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/` (PolyForm Noncommercial 1.0.0) makes the embosser project fully usable even without internet access.

## 9. Opportunities for Improvement (V1.1+)

| Idea | Why it would help | Difficulty |
|---|---|---|
| **Quantitative dot-height measurement** | Confirm conformance to North American / UEB standards. | Low (one trip to a depth gauge or a CT scan). |
| **Heavier card stock support (>0.5 mm)** | Adds use-cases (signage, durable labels). | Medium - needs a longer Handle Connector for more leverage and a stiffer Body. |
| **Multi-line registration aid** | Today the user eyeballs row-to-row alignment; a snap-in registration jig would help. | Low - additional accessory part. |
| **Alternate braille standards (UEB, Marburg, Japanese tenji)** | Internationalisation. | Low at the plate generator; no device-side changes. |
| **Motorised drive** | Higher throughput; accessibility for users with reduced grip strength. | High - introduces electronics, removes "no electronics" constraint. |
| **Identical A/B holder pairs** | Reduces SKU count from 4 holders to 1. | Medium - geometry refactor; needs to retain rotational keying. |
| **Optional rubber-feet variant of Body Base** | Improved desktop stability. | Trivial. |

## 10. References

1. **Open Know-How Specification** (2022). Internet of Production Alliance. https://standards.internetofproduction.org/pub/okh
2. **OpenAT-Template** (Makers Making Change / Neil Squire Society, v1.2 2025-Feb-04). https://github.com/makersmakingchange/OpenAT-Template
3. **CERN Open Hardware Licence Version 2 - Weakly Reciprocal** (CERN-OHL-W v2). https://cern.ch/cern-ohl
4. **Web-based plate generator (primary, deployed):** https://braille-card-and-cylinder-stl-gener.vercel.app
5. **Companion repository - Web-based plate generator (source):** https://github.com/BrennenJohnston/braille-cylinder-stl-generator
6. **Companion repository - OpenSCAD plate generator (alternative; vendored locally at `Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`):** https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad
7. **Companion repository - Accessible OpenSCAD UI:** https://github.com/BrennenJohnston/openscad-assistive-forge
8. **Liblouis braille translation library** (powering the web app's automatic translation): https://liblouis.io/
9. **Branah braille translator** (used to translate text for the OpenSCAD alternative): https://www.branah.com/braille-translator
10. **PolyForm Noncommercial 1.0.0 license** (governs both customizers): https://polyformproject.org/licenses/noncommercial/1.0.0
