# Custom Braille Embosser - Written Tutorial

> This document is the transcript-backed written version of the tutorial videos in `Video_Tutorials/`. If the videos and any other written instructions ever disagree, update this file from the `.srt` sources and treat the transcript-backed flow as the newest tutorial.

## Source transcripts

- `Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/Custom_Braille_Embosser_3d_Printing_Step1.srt`
- `Video_2_Assembling_Braille_Embosser_3D_Printed_Parts/Custom_Braille_Embosser_3d_Printing_Step2.srt`
- `Video_3_How_To_Use_Completed_Braille_Embosser/Custom_Braille_Embosser_3d_Printing_Step3.srt`

## 1. Overview

The Custom Braille Embosser workflow has three stages:

1. Generate and print the braille cylinders.
2. Assemble the printed embosser.
3. Use the finished device to emboss card stock.

This tutorial follows those same three stages.

## 2. Stage 1 - Generate and print the cylinders

### 2.1 Decide what text to emboss

The browser customizer shown in Video 1 is best for short text such as business-card information. The tutorial notes that the cylinder holds about **13 braille characters per line**, so you usually need to shorten a full business card before it will fit.

For business cards, the video recommends this priority order:

1. Name
2. At least one contact method
3. Job title
4. Mailing address
5. Fax number

If the app warns that your text is too long, trim the message before generating STL files.

### 2.2 Open the browser customizer

1. Open the Braille Customizer app from the `braille-cylinder-stl-generator` project.
2. If needed, use the accessibility controls at the top of the page:
   - Dark mode / Light mode / High Contrast mode
   - Larger or smaller font size
   - Preview brightness and contrast
3. Paste the text into the text entry area.

### 2.3 Choose the important settings

1. Leave **auto placement** enabled unless you need manual control.
2. Leave **capital letters disabled** unless a capital indicator is needed for clarity. The tutorial explains that each capitalized letter uses an extra braille cell, so turning capitals off saves space.
3. Select the correct **input language**. The example uses **English (UEB) uncontracted**.
4. Choose the correct **card thickness**:
   - `0.4 mm` for most business cards
   - `0.3 mm` for thinner card stock

Keep a note of the thickness you selected. The embossing cylinder and the universal counter cylinder must both use the same thickness.

### 2.4 Generate and download the embossing cylinder

1. Make sure **Embossing Plate** is selected.
2. Click **Generate STL**.
3. Wait for the preview to update.
4. Review the generated cylinder in the preview. The video points out two useful visual markers:
   - **Indicator letters** for quick sighted identification
   - **Indicator triangles** used later during assembly and operation
5. Click **Download STL**.

### 2.5 Generate and download the universal counter cylinder

1. Change plate selection to **Universal Counter Plate**.
2. Click **Generate STL** again.
3. Download that STL as well.

The transcript makes an important point here: once you have a universal counter cylinder for a given thickness, you can reuse it with other embossing cylinders made for that same thickness. If the message changes, you often only need to print a new embossing cylinder.

If you experiment with more than one thickness, rename the files so the thickness is obvious later, for example:

- `embossing_cylinder_name_0.4mm.stl`
- `counter_cylinder_0.4mm.stl`

### 2.6 Expert mode and translation accuracy

Video 1 notes that the app also has an **Expert Mode** for advanced control over dot shape, dot spacing, and other details. Use it only if you need to tune the geometry.

For critical braille content, cross-check the translation with another braille translator or a braille specialist.

### 2.7 Slicer settings shown in the tutorial

The demonstrated slicer workflow uses **Bambu Studio** on a **Bambu Lab X1C**.

Recommended changes from the transcript:

1. Start from a **High Quality** style preset or another profile below `0.2 mm`.
2. Use **Seam Painting** and place seams only on the **indicator letters / triangle area**, away from the braille dots.
3. Change the wall generator from **Classic** to **Arachne**.
4. Slow the print down significantly. The transcript example reduces speeds to roughly half of default values.
5. No supports were needed in the demonstrated workflow.
6. No brim was needed in the demonstrated workflow.

Approximate print times from the transcript on an X1C:

- Both cylinders together: about **3 hours**
- Replacement embossing cylinder only: about **1.5 hours**

## 3. Stage 2 - Assemble the embosser

### 3.1 Sort the parts

1. Lay out all printed parts so they are easy to identify.
2. Identify the two cylinders:
   - **Embossing cylinder** = raised dots
   - **Counter cylinder** = recessed dots
3. Identify the matching holder sides:
   - **Plus-marked / X-marked side** = embossing cylinder
   - **Minus-marked side** = counter cylinder

Keep the embossing-side parts and counter-side parts separated so they do not get mixed up.

### 3.2 Test-fit the cylinders

1. Start with the embossing cylinder and the plus-marked holder side.
2. Line up the triangle indicators before pushing the parts together.
3. Slide the cylinder on only partway first.
4. The fit should be snug but removable.
5. If it is too tight, sand the mating area lightly and try again.
6. Repeat for the counter cylinder using the minus-marked side.

### 3.3 Confirm the alignment before installing

Before placing the assemblies into the body:

- The top and bottom triangles should point directly at each other.
- The side triangles should mirror each other.
- The embossing cylinder's side triangles should point to the **right**.
- The counter cylinder's side triangles should point to the **left**.

When aligned correctly, the gears should interlock cleanly.

### 3.4 Install the optional grip extension first

If you are using the optional grip extension:

1. Place the **top** grip-extension piece over the top of the base and slide it down.
2. Set the **bottom** grip-extension piece on a solid surface.
3. Line up the base and top piece over it.
4. Press until it clicks into place.

The transcript installs the grip extension before the rollers.

### 3.5 Check the lid fit

1. Put the lid on once and remove it again before installing the rollers.
2. If the lid is hard to remove, place the lip of the lid against a solid surface and pull down to pop it off.

### 3.6 Install the cylinder assemblies

1. Hold both aligned cylinder assemblies in one hand.
2. Bring the base/body in with your other hand.
3. Double-check the orientation:
   - **Embossing cylinder on the left**
   - **Counter cylinder on the right**
   - **Plus-marked side on the left**
   - **Minus-marked side on the right**
4. Slide the assemblies into place carefully.
5. Re-check that the top and bottom triangles still point at each other.

### 3.7 Install the handle connector and handle grip

1. Insert the **Handle Connector**. Its X-shaped end mates with the embossing-cylinder side.
2. Snap the lid back on.
3. Place the **Handle Grip** on top of the Handle Connector.
4. Press down until it clicks into place.

### 3.8 Test the completed mechanism

Turn the handle a couple of times.

- It should feel a little stiff.
- It should not feel jammed or extremely hard to rotate.

If rotation feels wrong, stop and re-check the cylinder alignment.

## 4. Stage 3 - Use the completed embosser

### 4.1 Set the starting position

1. Turn the handle until the indicator triangles on both cylinders are directly on top of each other.
2. Rotate the whole embosser so the rollers are horizontal.

This is the starting position shown in Video 3.

### 4.2 Orient the card

1. Use the indicator triangles to understand which direction the braille will emboss.
2. Feed the card from **left to right**.
3. Keep the card's printed side **facing up** in the direction the triangles point.
4. Drop the card into place between the rollers and make sure it sits level.

### 4.3 Emboss the card

1. Rotate the handle forward about a **half turn**.
2. If helpful, flip the embosser partway through so you can watch the dots forming.
3. You can move the handle back and forth slightly to finish the dots.
4. Do **not** go too far past the last dot while checking the embossing, or the print can shift out of alignment.
5. Once the dots look right, roll the card all the way through.

### 4.4 Thickness reminder

The example operation video uses the **0.4 mm** cardstock setting. If your card is thinner, use the **0.3 mm** cylinder preset instead.

### 4.5 Change to a different message

1. Pull the lid off.
2. Leave the handle attached.
3. Remove the current cylinders.
4. Install the replacement cylinders.
5. Re-align the indicator triangles before embossing again.

If fresh cylinders feel stuck in the base, the transcript recommends using a **small flathead screwdriver** carefully to work them loose.

## 5. Quick troubleshooting

| Problem | Likely cause | What to try |
|---|---|---|
| Dots are too shallow | Wrong thickness pair for the card | Match `0.3 mm` cylinders to `0.3 mm` card, and `0.4 mm` cylinders to `0.4 mm` card |
| Print looks skewed | Start position or travel distance was off | Re-align the indicator triangles and avoid rolling too far while checking the dots |
| Assembly is too tight | Mating surfaces need cleanup | Sand lightly and test-fit again |
| Rotation is hard | Cylinders are misaligned | Reinstall with embossing on the left, counter on the right, and triangles mirrored correctly |
| Cylinders are stuck during swapping | Fresh print fit is tight | Use a small flathead screwdriver carefully |

## 6. Related written docs

For the MMC documentation set, this tutorial is also reflected in:

- `Documentation/_drafts/Custom_Braille_Embosser_Maker_Guide.md`
- `Documentation/_drafts/Custom_Braille_Embosser_User_Guide.md`
- `Documentation/_drafts/Custom_Braille_Embosser_Quickstart_Guide.md`
