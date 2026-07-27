# Custom Braille Embosser - Maker Guide

> **Document version:** 1.0 | 2026-May-31
> **Designer:** Brennen Johnston
> **For:** makers building the Custom Braille Embosser for themselves or for someone else.

---

## 1. Overview

The Custom Braille Embosser is a fully 3D-printed, hand-operated braille embosser. As the maker you will:

1. Print 10 device parts.
2. Generate one or more pairs of cylindrical embossing/counter plates for the user's chosen text. **The recommended way to do this is the web-based customizer at <https://braille-card-and-cylinder-stl-gener.vercel.app>** (auto-translates English to braille, no install required). An offline OpenSCAD copy is included in this repo at [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative) for makers who need to work offline. See Section 7 for the full workflow.
3. Print the plate pair on the same 3D printer.
4. Snap the parts together by hand. There are no fasteners, no springs, no glue, and no electronics.
5. Test that your assembled embosser produces clean dots on 0.3 mm and 0.4 mm card stock using one of the example plate pairs included in this repository.

Total active maker time: **~10-15 minutes** of assembly. Total print time on a Bambu Lab X1C at 0.2 mm layer height is **~12-18 hours** for the full set of device parts (verify against the slicer's report on the included `.3mf` profile).

### 1.1 Video tutorial set (recommended viewing before starting)

| # | Topic | YouTube | Local mirror |
|---|---|---|---|
| 1 | Customizing braille, downloading STLs, adjusting 3D-print settings | <https://youtu.be/m71VNZq28MI> | `Video_Tutorials/Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/` |
| 2 | Assembling the 3D-printed parts | <https://youtu.be/x-uPNtT2Gqk> | `Video_Tutorials/Video_2_Assembling_Braille_Embosser_3D_Printed_Parts/` |
| 3 | Using the completed Custom Braille Embosser | <https://youtu.be/77iXvJbkXh4> | `Video_Tutorials/Video_3_How_To_Use_Completed_Braille_Embosser/` |

Watch Video 1 before slicing; Video 2 before assembly; Video 3 once your unit is built.

A consolidated written version of those three tutorials, derived from the `.srt` transcript files, is available at `Video_Tutorials/Custom_Braille_Embosser_Written_Tutorial.md`.

## 2. Maker Checklist

Before you start a build, confirm you have:

- [ ] An FDM 3D printer with a build volume of at least **220 x 220 x 200 mm**.
- [ ] A slicer (Bambu Studio recommended; OrcaSlicer, PrusaSlicer, or Cura also work).
- [ ] **At least 200 g** of PLA or PETG filament (covers the device + one plate pair, with margin).
- [ ] Card stock at 0.3 mm and/or 0.4 mm thickness for testing.
- [ ] The recipient's desired braille content - either an English text message (use the browser generator) or pre-generated `.stl` plates.
- [ ] About 1 hour of attended time across the build (to set up prints and to assemble afterwards).

## 3. Items to Hand to the User

When you ship/give the embosser to its recipient, include:

1. The fully assembled Custom Braille Embosser.
2. **At least one** pair of printed embossing + counter plates that contain the message(s) the user requested.
3. A starter pack of card stock (5-10 sheets at the matching thickness).
4. A printed copy of the [User Guide](Custom_Braille_Embosser_User_Guide.pdf) (or the [Quickstart Guide](Custom_Braille_Embosser_Quickstart_Guide.pdf) if the user prefers shorter instructions).
5. (Optional) A soft cloth for cleaning the plates.

## 4. Tool List

| ID | Tool | Purpose | Notes |
|---|---|---|---|
| T01 | FDM 3D printer | Print all 10 device parts and the plate pair | Bambu Lab X1C recommended; pre-sliced `.3mf` profiles included. |
| T02 | Slicer software | Slice STLs if you do not use the included `.3mf` | Bambu Studio recommended. |
| T03 | Spatula / build-plate scraper | Remove parts from the build plate | Often supplied with the printer. |
| T04 | Deburring tool / hobby knife | Clean any seam lines or stringing on snap-fit features | Optional but improves snap fit. |
| T05 | Soft cloth | Clean plates after testing | Microfibre works well. |
| T06 | Calipers (optional) | Verify card-stock thickness | A 0.4 mm card matters; 0.5 mm card will not emboss cleanly. |

## 5. Supplies

| Supply | Specification | Quantity (per device) |
|---|---|---|
| PLA or PETG filament | Any colour, 1.75 mm | **268.81 g for the device** (8 h 44 min on X1C with PLA Basic) + **24.68 g for one plate pair** (3 h 5 min on the same printer/material) = ~293 g total |
| Card stock | 0.3 mm or 0.4 mm | 5-10 sheets for testing |
| Optional: stick-on rubber feet | 8-10 mm dia. | 4 (under the Body Base) |

## 6. PPE

| Item | Why |
|---|---|
| Safety glasses | Recommended when removing parts from the printer build plate. |
| Closed-toe shoes | Standard 3D-printing best practice. |

## 7. Customization Guide - Generating Plates for the User's Message

This section follows the narrated workflow in **Video 1** and should be treated as the most up-to-date plate-generation tutorial. Two officially supported customizer paths are provided; **the web-based customizer is the primary recommended workflow** for almost all makers.

A side-by-side comparison and full quick-start steps for both customizers are also kept up to date in the embedded customizer folder's README at [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/README.md`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/README.md).

### 7.1 Before you type: make the message fit the cylinder
- The customizer workflow is intended for short labels such as business-card information or other compact text.
- The transcript notes that the cylinder holds about **13 braille characters per line**, so most full business cards will not fit without editing.
- When condensing a business card, follow the **BANA-inspired priority order** shown in Video 1:
  1. Name
  2. At least one contact method
  3. Job title
  4. Mailing address
  5. Fax number
- If the app warns that the text exceeds the available space, shorten the content before generating STL files.

### 7.2 Primary path - Web-Based Customizer (recommended for most makers)

The browser-based generator is the **primary recommended workflow** for this project. It is the same tool demonstrated in **Video 1**, runs in any modern browser (no install), generates the STLs locally in your browser (your text is never uploaded), and handles English -> Grade 1 / Grade 2 braille translation automatically (50+ language tables, powered by the open-source [Liblouis](https://liblouis.io/) library).

| Field | Value |
|---|---|
| **Open the web app** | <https://braille-card-and-cylinder-stl-gener.vercel.app> |
| Source repository | [`braille-cylinder-stl-generator`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator) |
| Required software | Any modern browser. No install. |
| License (web app) | PolyForm Noncommercial 1.0.0 |

Step-by-step:
1. Open the web app at <https://braille-card-and-cylinder-stl-gener.vercel.app>.
2. If needed, enable the accessibility options shown at the top of the app:
   - Dark / Light / High Contrast mode
   - Larger / smaller font size
   - 3D preview brightness / contrast controls
3. Paste the user's text into the text area.
4. Leave **Placement Mode** on automatic unless you have a reason to manually place braille.
5. Keep **capitalized letters disabled** unless a capital indicator is important for clarity. Video 1 explains that each capitalized letter consumes an extra braille cell, so disabling capitals saves space.
6. Select the correct **input language / translation table**. The transcript uses **English (UEB) uncontracted** as the default and recommends it for the demonstrated business-card workflow. The web app supports 50+ tables - pick the one that matches the user's language and grade.
7. Set **card thickness** to match the paper the user will emboss:
   - **0.4 mm** for most business cards
   - **0.3 mm** for thinner card stock
8. Keep a note of the chosen thickness. **Both cylinders must be generated at the same thickness.** Mismatching thickness settings can damage the embossing dots or produce poor embossing.
9. Make sure **Embossing Plate** is selected, then click **Generate STL**.
10. After generation completes, review the 3D preview. The transcript points out the built-in **indicator letters** and **indicator triangles**, which help sighted makers identify printed cylinders later and align them during use.
11. Click **Download STL** to save the embossing cylinder.
12. Switch plate selection to **Universal Counter Plate**, then generate and download that STL as well.
13. If you are testing multiple thicknesses, rename the download to include thickness in the filename, such as `counter_cylinder_0.4mm.stl`.
14. When translation accuracy matters, cross-check the braille with another translator or a braille specialist, as recommended in the transcript.

> One useful detail from Video 1: once you have printed a universal counter cylinder for a given thickness, you only need to print a new embossing cylinder when the text changes. The same counter cylinder can be reused for other embossing cylinders of that thickness.

### 7.3 Alternative path - OpenSCAD customizer (offline / power-user, included in this repo)

A copy of the OpenSCAD generator is **included directly in this repository** at [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative). Use this path only if you need to work offline, want full parametric control over every dot/spacing/cylinder dimension, or want to integrate plate generation into an existing OpenSCAD / CAD workflow.

| Field | Value |
|---|---|
| **Local copy** | [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad) |
| Upstream repository | [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) |
| Vendored version | 2.2.1 (2026-05-30) |
| Required software | [OpenSCAD](https://openscad.org/) 2024.x or newer (2026.01.03 or newer recommended) |
| License (this folder only) | PolyForm Noncommercial 1.0.0 (separate from the rest of this repo's licenses) |

Important difference from the web app: **the OpenSCAD customizer does not auto-translate text.** You must paste pre-translated **Unicode braille** (output from <https://www.branah.com/braille-translator>, Unicode mode - not ASCII) into the customizer's `Line_1`..`Line_4` fields.

Step-by-step:
1. Translate your text:
   - Open <https://www.branah.com/braille-translator>.
   - Pick the grade (Grade 2 contracted is recommended for most uses; Grade 1 for names/emails/clarity-critical content).
   - Verify **Unicode Braille** is selected (NOT ASCII Braille).
   - Type the English text and copy the Unicode-braille output (looks like `⠓⠑⠇⠇⠕`).
2. Open `Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/Braille_Cylinder_STL_Generator.scad` in OpenSCAD.
3. Open the **Customizer panel** (View -> Customizer).
4. Paste the Unicode braille into `Line_1`. Use `Line_2`..`Line_4` for additional lines as needed.
5. Set `plate_type` to `Embossing Plate`.
6. Set `paper_thickness_preset` to `0.4mm` or `0.3mm` (matches the same dropdown in the web app).
7. (Optional) Use the **Expert Mode** sub-panels to override individual dot, spacing, or cylinder parameters. Most makers do not need to.
8. Render: press **F6** (or Design -> Render). This can take 30 s to several minutes.
9. Export: **File -> Export -> Export as STL...** with a descriptive filename.
10. Switch `plate_type` to `Counter Plate`, render, and export again. Keep `paper_thickness_preset` the same.
11. Print both STL files.

For the full quick-start, parameter reference, troubleshooting list, and license details, see [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/README.md`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/README.md).

### 7.4 Accessible-UI path (driving the OpenSCAD generator)
For users who prefer a screen-reader-friendly interface, [`openscad-assistive-forge`](https://github.com/BrennenJohnston/openscad-assistive-forge) provides an accessible browser UI on top of the OpenSCAD plate generator. The web-based customizer above is also already screen-reader friendly out of the box.

### 7.5 Offline pre-generated examples
Two pairs are pre-generated and included in this repository in `Build_Files/3D_Printing_Files/Embossing_Plates_Examples/`:
- `Embossing_Plate_Brennen_0.3.stl` + `Universal_Counter_Plate_0.3.stl` (0.3 mm card)
- `Embossing_Plate_Brennen_0.4.stl` + `Universal_Counter_Plate_0.4.stl` (0.4 mm card)

These are useful for first-build verification before generating user-specific plates.

### 7.6 Choosing between the two customizers

| If you... | Use |
|---|---|
| Want the simplest, most beginner-friendly path | **Web-based customizer** (primary, Section 7.2) |
| Don't already have OpenSCAD installed | **Web-based customizer** (primary) |
| Want automatic English -> braille translation | **Web-based customizer** (primary) |
| Use a screen reader | **Web-based customizer** (primary) |
| Need to work fully offline (no internet) | OpenSCAD alternative (Section 7.3) |
| Want full parametric control of every dimension | OpenSCAD alternative |
| Want to inspect, modify, or extend the source code | OpenSCAD alternative |
| Want to batch-generate many plates from a script | OpenSCAD alternative (drives via `openscad -D '...' -o out.stl`) |

## 8. 3D Printing Summary

### 8.1 Recommended profiles (already sliced)
| Printer | File | Layer height | Notes |
|---|---|---|---|
| Bambu Lab X1C | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf` | 0.2 mm | All 10 parts arranged on plate. |
| Bambu Lab X1C | `Build_Files/3D_Printing_Files/Print_Profiles/X1C/Embossing and Counter Cylinder High Quality.3mf` | 0.12 mm (High Quality) | Cylinder pair only, high-quality settings. |

For other printers, slice the per-part STLs in `Build_Files/3D_Printing_Files/STL/` using the per-part settings in Section 8.3.

### 8.2 Per-part summary

| ID  | Part                    | STL filename                                                | QTY | Mass (g) | Print time |
|-----|-------------------------|-------------------------------------------------------------|-----|----------|------------|
| P01 | Body Base               | `P01 - Body Base v1.0 (0.2 Layer Height).stl`               | 1   | TBD      | TBD        |
| P02 | Body Top                | `P02 - Body Top v1.0 (0.2 Layer Height).stl`                | 1   | TBD      | TBD        |
| P03 | Embosser Holder A1      | `P03 - Embosser Holder A1 v1.0 (0.2 Layer Height).stl`      | 1   | TBD      | TBD        |
| P04 | Embosser Holder A2      | `P04 - Embosser Holder A2 v1.0 (0.2 Layer Height).stl`      | 1   | TBD      | TBD        |
| P05 | Counter Holder B1       | `P05 - Counter Holder B1 v1.0 (0.2 Layer Height).stl`       | 1   | TBD      | TBD        |
| P06 | Counter Holder B2       | `P06 - Counter Holder B2 v1.0 (0.2 Layer Height).stl`       | 1   | TBD      | TBD        |
| P07 | Grip Extension Bottom   | `P07 - Grip Extension Bottom v1.0 (0.2 Layer Height).stl`   | 1   | TBD      | TBD        |
| P08 | Grip Extension Top      | `P08 - Grip Extension Top v1.0 (0.2 Layer Height).stl`      | 1   | TBD      | TBD        |
| P09 | Handle Connector        | `P09 - Handle Connector v1.0 (0.2 Layer Height).stl`        | 1   | TBD      | TBD        |
| P10 | Handle Grip             | `P10 - Handle Grip v1.0 (0.2 Layer Height).stl`             | 1   | TBD      | TBD        |
| -   | **Device subtotal (P01-P10, assembly profile, X1C + PLA Basic)** | `Braille Embosser Assembly v1.0 (0.2 Layer Height).3mf` | 1 set | **268.81 g** (258.79 g model + 10.02 g support) | **8 h 44 min** (8 h 35 min printing + 8 min 16 s prep) |
| P11 | Embossing Plate (gen.)  | from companion repo                                         | 1   | TBD      | TBD        |
| P12 | Counter Plate (gen.)    | from companion repo                                         | 1   | TBD      | TBD        |
| -   | **Plate-pair subtotal (P11 + P12, cylinder HQ profile, X1C + PLA Basic)** | `Embossing and Counter Cylinder High Quality.3mf` | 1 pair | **24.68 g** (no supports) | **3 h 5 min** (2 h 55 min printing + 9 min 40 s prep) |

> The two subtotal rows above are the actual Bambu Studio slicer reports for the two included `.3mf` profiles on a Bambu Lab X1C with Bambu Lab PLA Basic. Sources: `Settings Research/Braille Embosser Assembly v1.0/output.png` (device assembly; full breakdown in [`Braille_Embosser_Assembly_Slicer_Settings.md`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Braille_Embosser_Assembly_Slicer_Settings.md#slicing-result-bambu-lab-x1c--pla-basic)) and `Settings Research/Cylinder High Quality profile/output.png` (cylinder pair; full breakdown in [`Embossing_Counter_Cylinder_HQ_Slicer_Settings.md`](../../Build_Files/3D_Printing_Files/Print_Profiles/X1C/Embossing_Counter_Cylinder_HQ_Slicer_Settings.md#slicing-result-bambu-lab-x1c--pla-basic)). Per-part rows P01-P10 and P11-P12 remain TBD because the multi-object profiles do not produce per-part mass / time; slice each STL on its own if you need an individual breakdown. **Complete one-device-with-one-plate-pair total: 293.49 g and ~11 h 49 min** of print time on an X1C with PLA Basic.

### 8.3 Per-part settings

The included `.3mf` profiles already encode these settings; the table below is for makers using a different printer/slicer combination.

| Setting | Value | Why |
|---|---|---|
| Layer height | **0.2 mm** | Used for all parts in v1.0; matches filenames. |
| Wall loops | 3 | Strength at snap-fit features. |
| Top / bottom layers | 4 / 4 | Surface finish. |
| Infill | **30 % gyroid** (PLA) or **20 % gyroid** (PETG) | Stiff enough to handle squeeze force without flexing. |
| Supports | **Tree / organic, only on overhangs >55°** | The Body Top and Body Base have small overhangs around the holder pockets. Other parts print support-free. |
| Print orientation | As laid out in the included `.3mf` files | Hand-tested orientation for strength and dimensional accuracy. |
| Brim | 5 mm on plates with small footprints (Handle Grip, Handle Connector) | Reduces warping. |
| Material | PLA (default) or PETG | PETG is tougher; PLA prints more easily. Either works. |

### 8.4 Plate-specific slicer notes from Video 1

Video 1 shows a tested workflow in **Bambu Studio on a Bambu Lab X1C**. Treat these as proven starting points for the cylinders:

| Setting / action | Transcript-backed recommendation | Why |
|---|---|---|
| Base preset | Start from **High Quality** or another profile below 0.2 mm layer height | Cleaner braille dots |
| Seam control | Use **Seam Painting** and paint the seam onto the **indicator letters / triangle area only** | Keeps seams away from the braille dots and recessed cavities |
| Wall generator | Switch from **Classic** to **Arachne** | More consistent small details and better recessed-dot accuracy |
| Speed | Roughly halve the default speeds; the transcript example uses: initial layer 40, infill 75, outer wall 50, inner wall 75, small perimeters 40, and halved accelerations | Improves dot quality |
| Supports | **None** on the demonstrated X1C setup | Not needed in the shown workflow |
| Brim | **None** on the demonstrated X1C setup | Not needed in the shown workflow |
| Material | Basic PLA was demonstrated; PETG may also work with tuning | PLA was the tested baseline |
| Expected time on X1C | About **3 hours** for both cylinders, or about **1.5 hours** for a replacement embossing cylinder | Helps estimate turnaround for updates |

If your printer already produces clean dots at higher speed, keep the faster settings. If you see dot-quality issues, the transcript recommends slowing the print as the first troubleshooting step.

## 9. Post-processing

1. Remove brim (if used) with a hobby knife.
2. Inspect each snap-fit feature - particularly the Embosser Holder pair, the Counter Holder pair, and the Handle Connector socket - and use a deburring tool to remove any seam lines that might prevent a clean snap.
3. Test-fit the holder pairs around a printed plate before final assembly.

## 10. Examples of Quality Prints

> **TODO for the maker:** add photographs of well-printed parts from your build to this section, captioned with print settings. Reference the photos in `Photos/Custom_Braille_Embosser.jpg` and the additional photo set in the workspace `Braille Embosser Photos/` folder for examples of finished assembled units.

Examples to look for:
- Crisp, layer-aligned dots on the embossing plate (no stringing in the dot caps).
- Clean snap-fit features on Embosser Holder / Counter Holder pairs (no print blobs blocking the snap channel).
- Smooth Handle Grip exterior (no visible Z-banding that would be uncomfortable to squeeze).

## 11. Maker Component List (for reference during assembly)

Use these IDs in your assembly checklist. They match the BOM and Section 8.2.

| ID  | Part                  | Sub-assembly  |
|-----|-----------------------|---------------|
| P01 | Body Base             | Body          |
| P02 | Body Top              | Body          |
| P03 | Embosser Holder A1    | Embosser pair |
| P04 | Embosser Holder A2    | Embosser pair |
| P05 | Counter Holder B1     | Counter pair  |
| P06 | Counter Holder B2     | Counter pair  |
| P07 | Grip Extension Bottom | Grip          |
| P08 | Grip Extension Top    | Grip          |
| P09 | Handle Connector      | Handle        |
| P10 | Handle Grip           | Handle        |
| P11 | Embossing Plate       | Plate pair (printed separately) |
| P12 | Universal Counter Plate | Plate pair (printed separately) |

## 12. Transcript-backed Assembly Tutorial

> The full sequence is shown in the assembly video tutorial: **<https://youtu.be/x-uPNtT2Gqk>** (Video 2 - "Assembling Braille Embosser 3D printed parts"). The local mirror and subtitles live in `Video_Tutorials/Video_2_Assembling_Braille_Embosser_3D_Printed_Parts/`. The steps below are written directly from that transcript and should be treated as the most up-to-date assembly order.

### 12.1 Identify and sort the printed parts
1. Lay out all printed parts where you can identify them easily.
2. Identify the two cylinders:
   - **Embossing cylinder** = raised braille dots on the surface
   - **Counter cylinder** = recessed dots on the surface
3. Identify the matching holder sets:
   - **Plus-marked / X-marked holder side** = used with the embossing cylinder
   - **Minus-marked holder side** = used with the counter cylinder
4. Sort the embossing-cylinder parts and counter-cylinder parts into separate groups so they do not get mixed up.

### 12.2 Fit-check the cylinders to their holder sets
1. Start with the **embossing cylinder** and its **plus-marked** holder set.
2. Line up the triangle indicators before pushing the parts together.
3. Slide the cylinder on only partway first to test the fit.
4. The fit should be snug but removable. It should not be so tight that you cannot pull it back out, and it should not be loose.
5. If the fit is too tight, lightly sand the mating area and test again.
6. Once the fit feels right, complete the assembly for the embossing side.
7. Repeat for the **counter cylinder** using the **minus-marked** holder set.

### 12.3 Confirm cylinder orientation before installation
1. Bring the embossing-cylinder assembly and counter-cylinder assembly together in your hands.
2. Verify the indicator triangles match the orientation shown in Video 2:
   - Top and bottom triangles point directly at each other
   - Side triangles mirror each other
   - Embossing-cylinder side triangles point to the **right**
   - Counter-cylinder side triangles point to the **left**
3. When aligned correctly, the gears should interlock cleanly.

### 12.4 Install the optional grip extension first
1. If you are using the optional grip extension, install it **before** installing the rollers.
2. Place **P08 Grip Extension Top** over the top of the base and slide it down.
3. Set **P07 Grip Extension Bottom** on a solid surface.
4. Line up the base and top piece over the bottom piece.
5. Press until the grip extension clicks into place.

### 12.5 Test the lid fit before adding the rollers
1. Put the lid on and remove it once to make sure it goes on and off cleanly.
2. If the lid is difficult to remove by hand, place the lip of the lid against a solid surface and pull down for leverage, as demonstrated in the transcript.
3. If the lid passes this check, continue.

### 12.6 Install the cylinder assemblies into the body
1. Hold both aligned cylinder assemblies in one hand, palm up, while keeping the lower assembly from shifting.
2. With your other hand, bring the body/base into position.
3. Double-check the transcript's left/right orientation:
   - **Plus-marked / embossing cylinder goes on the left**
   - **Minus-marked / counter cylinder goes on the right**
4. Slide the assemblies carefully into place.
5. At about the halfway point, the rollers should stay in place on their own.
6. Re-check the orientation:
   - Embossing cylinder on the left
   - Counter cylinder on the right
   - Top and bottom triangles point at each other
   - Side triangles mirror each other

### 12.7 Install the handle connector and lid
1. Insert **P09 Handle Connector**.
2. The connector's **X-shaped** end should mate with the embossing-cylinder holder.
3. Snap the lid back on.

### 12.8 Install the handle grip and verify motion
1. Place **P10 Handle Grip** on top of the Handle Connector.
2. Press down until it clicks into place.
3. Rotate the handle a couple of turns.
4. The mechanism should feel **a little stiff, but not difficult to rotate**.
5. If you feel heavy resistance, stop and re-check cylinder alignment and fit.

## 13. Testing

After assembly, run this acceptance test using one of the included example plate pairs and the operating method shown in Video 3:

1. Install the matching example cylinder pair for the card thickness you are testing.
2. Align the indicator triangles to the starting position.
3. Rotate the embosser so the rollers are horizontal.
4. Drop a matching-thickness sheet of card stock into place between the rollers.
5. Rotate the handle forward about a half turn.
6. If desired, inspect the dot formation partway through, then finish rolling the card through.
7. Run a finger across the embossed area. **Pass criteria:**
   - All expected dots are present
   - Dots are uniform in height
   - The card is not punctured
   - The embossing is not visibly skewed from incorrect starting alignment
8. Repeat with the other included thickness set.

If any dots are missing, shallow, or skewed, see Section 14: Troubleshooting.

## 14. Troubleshooting / FAQ

| Symptom | Likely cause | Fix |
|---|---|---|
| Dots too shallow / missing | Card thicker than the plate pair was designed for | Use the matching 0.4 mm plate pair on 0.4 mm card. |
| Dots flat-topped instead of rounded | Cylinder print quality is poor (seam placement, speed, or wall generation) | Reprint the cylinders using the Video 1 settings in Section 8.4: seam painting on the indicator area, Arachne wall generation, and slower high-quality print speeds. |
| Card tears | Card too thin (<0.25 mm) | Use 0.3 mm or thicker card stock. |
| Cylinder fit is too tight during assembly | Minor print swell on the holder/cylinder mating surface | Lightly sand and test-fit again before full assembly. |
| Cylinders rotate with heavy resistance | Embossing/counter cylinders are not aligned per the triangle markers | Remove the lid, re-align triangles, and reinstall with embossing on the left and counter on the right. |
| New cylinders are hard to remove on the first swap | Fresh parts are sticking in the base | Use a small flathead screwdriver carefully to work them loose, as shown in Video 3. |
| Holders rattle | Embosser/Counter Holder snap features under-printed | Increase wall loops to 4 and reprint the holder pair. |
| Handle Grip slides off | Snap feature on P09/P10 under-tolerance | Reprint at +0.05 mm horizontal expansion (slicer setting). |
| Body Top will not close | Foreign material in the body, or holders not seated | Disassemble, clean, re-seat holders and try again. |
| First print flexes during use | Infill too low | Reslice at 30 % gyroid (PLA) and reprint. |
| Plate pair is mismatched (dots fall into wrong cavities) | The two plates are from different generation runs | Always print and use the embossing plate and counter plate from the **same** generator export. |

## 15. After-build Acknowledgements

If you build this for someone else, please consider:
- Logging your build on the [Makers Making Change Maker Wanted](https://makersmakingchange.com/maker-wanted/) page (once the MMC library URL is assigned to this device).
- Filing GitHub issues if you find documentation gaps or improvement ideas.
