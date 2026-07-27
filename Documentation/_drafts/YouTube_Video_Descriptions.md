# Custom Braille Embosser - YouTube Titles & Descriptions

> **Purpose:** copy-paste-ready titles and descriptions for the three Custom Braille Embosser tutorials on YouTube.
> **Source transcripts:** the `.srt` files in [`Video_Tutorials/Video_1_*`](../../Video_Tutorials/Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings), [`Video_2_*`](../../Video_Tutorials/Video_2_Assembling_Braille_Embosser_3D_Printed_Parts), and [`Video_3_*`](../../Video_Tutorials/Video_3_How_To_Use_Completed_Braille_Embosser).
> **Master publishing pack:** [`Custom_Braille_Embosser_Publishing_Pack.md`](Custom_Braille_Embosser_Publishing_Pack.md).
>
> **YouTube hard limit:** description fields are capped at **5,000 characters** (newlines count). The blocks in section 2 are sized so the longest description (Video 1) lands at ~4,950 characters with the trimmed block set, and Videos 2 and 3 have room for the series links and hashtag line on top of that. See section 2.6 for the per-video budget. YouTube descriptions also render as **plain text only** (no Markdown), so any backticks, asterisks, or `[label](url)` syntax will display literally.
>
> If you rename a video or rewrite a description on YouTube, update this file first so the videos and the rest of the documentation stay in sync.

---

## 1. Quick reference

| # | Short URL | Long URL | Local mirror |
|---|---|---|---|
| 1 | <https://youtu.be/m71VNZq28MI> | `https://www.youtube.com/watch?v=m71VNZq28MI` | `Video_Tutorials/Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/` |
| 2 | <https://youtu.be/x-uPNtT2Gqk> | `https://www.youtube.com/watch?v=x-uPNtT2Gqk` | `Video_Tutorials/Video_2_Assembling_Braille_Embosser_3D_Printed_Parts/` |
| 3 | <https://youtu.be/77iXvJbkXh4> | `https://www.youtube.com/watch?v=77iXvJbkXh4` | `Video_Tutorials/Video_3_How_To_Use_Completed_Braille_Embosser/` |

---

## 2. Shared blocks (reused at the bottom of each video description)

> The wording for the project summary, links, series, acknowledgments, and hashtags is shared across the videos. Because of YouTube's 5,000-character description cap, **not every block fits in every video** - the longest description (Video 1) can only fit blocks 2.1, 2.2, and 2.4. See section 2.6 below for the per-video budget and section 3 / 4 / 5 for the exact set to paste for each video.
>
> Edit the canonical wording in this section first, then re-paste into each YouTube description.

### 2.1 About the project (one paragraph)

```text
About the Custom Braille Embosser:

The Custom Braille Embosser is a fully 3D printed, hand operated device for embossing braille onto card stock. I designed it to stay simple, so there's no fasteners, no springs, no glue, and no electronics. The whole device snaps together from 10 printed parts, and the braille message comes from interchangeable embossing and counter cylinders that you generate from text. Once the base device is printed, changing the message usually just means printing a new embossing cylinder, so the overall cost and time stays low.
```

### 2.2 Project & customizer links

```text
Project links:

- Main GitHub repository (this project): https://github.com/BrennenJohnston/custom-braille-embosser-3d-printing-project
- Web-based braille customizer (no install, runs in your browser):
- App: https://braille-card-and-cylinder-stl-gener.vercel.app
- Source: https://github.com/BrennenJohnston/braille-cylinder-stl-generator
- Offline OpenSCAD alternative customizer (for anyone not wanting to, or not able to, use the browser-based tool):
- Source: https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad
- Accessible browser UI on top of the OpenSCAD generator: https://github.com/BrennenJohnston/openscad-assistive-forge
- Braille translation engine used by the web customizer: https://liblouis.io/
```

### 2.3 The full 3-part tutorial series

```text
Full tutorial series:
- Part 1 of 3 - Customize Braille, Download STLs, and 3D-Print Settings: https://youtu.be/m71VNZq28MI
- Part 2 of 3 - Assembling the 3D-Printed Parts: https://youtu.be/x-uPNtT2Gqk
- Part 3 of 3 - How to Use the Completed Embosser: https://youtu.be/77iXvJbkXh4
```

### 2.4 Acknowledgments (WATAP & UW CREATE)

```text
Acknowledgments:

This project was made possible with support from:
- The Washington Assistive Technology Act Program (WATAP) - a statewide program that helps Washingtonians of all ages and abilities make informed decisions about, and gain access to, assistive technology. Learn more: https://watap.org/

- The University of Washington Center for Research and Education on Accessible Technology and Experiences (UW CREATE) - an interdisciplinary research center whose mission is to make technology accessible and to make the world accessible through technology. Learn more: https://create.uw.edu/
```

### 2.5 Hashtags

```text
#Braille #Accessibility #3DPrinting #AssistiveTechnology #OpenSourceHardware #BrailleEmbosser #WATAP #UWCREATE #DisabilityInclusion #DIY
```

> The full CC BY-SA 4.0 / CERN-OHL-W v2 / PolyForm Noncommercial 1.0.0 license text used to live in this block, but the combined description plus license body exceeds the 5,000-character YouTube cap for every video. The canonical license wording now lives only in the repository's [`LICENSE.md`](../../LICENSE.md), [`Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/LICENSE_PolyForm_Noncommercial_1.0.0.md`](../../Build_Files/3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/LICENSE_PolyForm_Noncommercial_1.0.0.md), and the project [`README.md`](../../README.md) §Licensing. The repository link in block 2.2 is what points YouTube viewers at the full terms.

### 2.6 Per-video character budget

YouTube's description field is capped at **5,000 characters**, including newlines. Character counts below assume the wording in §2.1 - §2.5 above is pasted verbatim, with a single blank line between blocks. (Counts can shift by a few characters depending on whether your clipboard uses LF or CRLF line endings; the YouTube editor shows a live count once you paste.)

| Video | Specific copy (intro + bullets + chapters) | Blocks that fit | Final description length | Headroom |
|---|---|---|---|---|
| 1 | ~3,055 | 2.1 + 2.2 + 2.4 | **~4,950** (no room for 2.3 or 2.5) | ~50 |
| 2 | ~2,545 | 2.1 + 2.2 + 2.3 + 2.4 + 2.5 | **~4,870** | ~130 |
| 3 | ~2,155 | 2.1 + 2.2 + 2.3 + 2.4 + 2.5 | **~4,485** | ~515 |

If you edit any of the video-specific copy in sections 3 - 5, re-check the totals; Video 1 has only ~50 characters of headroom, so even short additions there will push it over the 5,000 cap.

---

## 3. Video 1 - Customizing Braille, Downloading STLs, 3D-Print Settings

### 3.1 Title (paste into the YouTube "Title" field)

```text
Custom Braille Embosser - Part 1 of 3: Customize Braille, Download STLs & 3D-Print Settings
```

> 92 characters - inside YouTube's 100-character title cap. Alternate shorter title if the platform truncates: `Custom Braille Embosser (1/3): Customize Braille, Download STLs, 3D-Print Settings`.

### 3.2 Full description (paste into the YouTube "Description" field)

```text
This is part 1 of 3 in the Custom Braille Embosser tutorial series.

In this video, we're going to create a custom braille embossing cylinder from start to finish in the browser-based Braille Customizer. Then we'll download both STL files: the embossing cylinder and the matching universal counter cylinder. After that, I'll go over the 3D-printer slicer settings that worked best for me, so by the end you'll have two printable STL files and a solid starting point for printing them.

A few important points from the video
- The cylinder only holds about 13 braille characters per line, so most full business cards have to be shortened first. In the video I follow the Braille Authority of North America (BANA) priority order: name, at least one contact method, then job title, then mailing address, then fax number.
- Card thickness controls the embossing depth. `0.4 mm` is right for most business cards, and `0.3 mm` is there for thinner card stock. Whichever one you choose, keep a note of it, because the embossing cylinder and the counter cylinder both need to be generated at the same thickness.
- This program uses Liblouis for braille translation. It is one of the most reputable freely available braille translation tools, but for important content I still recommend cross-checking the result with another translator or a braille specialist.
- In my experience, seam painting makes a significant difference in braille dot quality. I recommend painting the seam over the indicator letters and triangles so the seam stays away from the braille dots.
- On my Bambu Lab X1C, what worked best for me was starting from the High Quality preset, switching the wall generator from Classic to Arachne, cutting the default speeds and accelerations roughly in half, and printing with no supports and no brim. These are just my starting points, so if your printer is already giving you clean results at a higher speed, you should keep your settings.
- Once you have a counter cylinder for one thickness, you can reuse it for as many custom embossing cylinders as you'd like at that same thickness. So if you need to update the message later, you usually only need to print a new embossing cylinder.

Chapters
0:00 Introduction
0:28 Tour of the Braille Customizer app
0:53 Accessibility controls (dark mode, high contrast, font size, preview brightness)
1:12 Deciding what to emboss (13 chars per line, BANA priority list)
2:33 Auto placement and capital letters
3:19 Liblouis - the translation library
3:46 Choosing the input language (50+ supported)
4:15 Setting card thickness (0.4 mm vs 0.3 mm)
4:42 Generate and download the embossing cylinder
5:13 Indicator letters and triangles in the 3D preview
5:56 Generate and download the universal counter cylinder
6:41 Expert Mode (advanced control over dot shape and spacing)
6:54 3D-printer slicer settings on Bambu Studio + X1C
7:30 Seam painting on the indicator area
8:00 Arachne wall generator and halved print speeds
8:55 Estimated print times and the "print one new cylinder per message" workflow

(Insert About / Project links / Acknowledgments blocks 2.1, 2.2, 2.4 here - in that order. The series block 2.3 and hashtags block 2.5 do NOT fit in this description's 5,000-character budget; viewers find the other two videos through the YouTube playlist and channel.)
```

> **Action when pasting into YouTube:** replace the parenthetical at the bottom with the verbatim contents of [section 2.1](#21-about-the-project-one-paragraph), then [section 2.2](#22-project--customizer-links), then [section 2.4](#24-acknowledgments-watap--uw-create) of this file, with a single blank line between each block. Skip 2.3 and 2.5 for this video.

---

## 4. Video 2 - Assembling the 3D-Printed Parts

### 4.1 Title

```text
Custom Braille Embosser - Part 2 of 3: Assembling the 3D-Printed Parts
```

> 70 characters.

### 4.2 Full description

```text
This is part 2 of 3 in the Custom Braille Embosser tutorial series.

In this video, we're going to assemble the 3D printed Braille Embosser. Once everything has been fully 3D printed, I'll walk through how I sort the parts, test the fit, line up the indicator triangles, and snap the whole device together. There are no fasteners, no springs, no glue, and no electronics, and the active assembly time is only about 10 to 15 minutes.

A few important points from the video
- Sort the parts into two groups by the plus / X versus minus markings on the holders. The plus-marked holder goes with the embossing cylinder, and the minus-marked holder goes with the counter cylinder. I recommend keeping them in separate groups so they don't get mixed up.
- I recommend test-fitting each cylinder by sliding it onto the holder only partway first. It should go on without too much resistance. It shouldn't be too tight or too loose. If it feels too tight, a little sanding might be needed.
- The indicator triangles are the main guide during assembly. Every holder has a top triangle, three side triangles, and a bottom triangle. When the two cylinder assemblies are lined up correctly, the top and bottom triangles point directly at each other, and the side triangles mirror each other.
- If you're using the optional grip extension, it needs to be installed before the rollers. The grip comes in two pieces. It does take a little bit of effort, but it should click into place.
- The technique that works best for me is to hold both aligned cylinder assemblies in one hand, then bring the base in with the other hand. Double check that the plus side is going into the left side, the minus side is going into the right side, the embossing cylinder is on the left, and the counter cylinder is on the right.
- Once everything is assembled, the handle should feel a little stiff, but not too difficult to rotate. If you're getting a lot of resistance, double check that everything is aligned correctly.

Chapters
0:00 Introduction
0:09 Identifying the parts (embossing cylinder, counter cylinder, plus and minus holders)
0:44 Test-fitting the embossing cylinder into the plus holder
1:30 Test-fitting the counter cylinder into the minus holder
1:45 Aligning the indicator triangles between the two cylinder assemblies
2:06 Optional grip extension
2:37 Lid fit check
2:59 Installing the cylinder assemblies into the body
3:47 Installing the Handle Connector
3:56 Snapping the lid back on
4:05 Attaching the Handle Grip
4:13 Testing the assembled mechanism

(Insert blocks 2.1, 2.2, 2.3, 2.4, then 2.5 here - in that order, with a single blank line between blocks. All five fit within the 5,000-character cap for this video.)
```

> **Action when pasting into YouTube:** replace the parenthetical with the verbatim contents of [section 2.1](#21-about-the-project-one-paragraph) through [section 2.5](#25-hashtags), in numerical order, with a single blank line between each block.

---

## 5. Video 3 - How to Use the Completed Embosser

### 5.1 Title

```text
Custom Braille Embosser - Part 3 of 3: How to Use the Completed Embosser
```

> 72 characters.

### 5.2 Full description

```text
This is part 3 of 3 in the Custom Braille Embosser tutorial series.

In this video, I'm going to walk you through how to use the 3D printed Braille Embosser. I'll show the starting position, how I line up the card, how far to turn the handle, and how to swap in a different cylinder when you want to change the message.

A few important points from the video
- You want to start by aligning the indicator triangles so the triangles on both cylinders are directly on top of each other. Once they're aligned, rotate the whole embosser so the rollers are horizontal. That's the starting position.
- Use the indicator triangles as your guide for card orientation. The card should roll from left to right, with the printed information facing up in the direction the triangles are pointing.
- I find it helpful to use gravity to level the card by dropping it into place between the rollers, then double checking that it seems level before embossing.
- Rotate the handle forward about a half turn. Another technique I found helpful is to flip the embosser partway through so I can watch the dots forming. Just make sure you stop before going over the last dot, or you may end up with a misaligned print.
- A quick note on settings: the embosser shown in the video is using the `0.4 mm` cardstock setting. If you have thinner business cards, make sure you use the `0.3 mm` cylinder preset instead.
- If you want to change out the cylinders, you can pull the lid off and leave the handle attached. If a fresh print is stuck in the base on the first swap, I recommend using a small flathead screwdriver carefully to help work it loose.
- If you run into any issues or want to contribute to the project, the GitHub link is in the description below.

Chapters
0:00 Introduction
0:05 Aligning the indicator triangles to the starting position
0:25 Lining up the embossing dots with the printed information
0:38 Orienting and dropping in the card
0:56 Embossing the card (half turn + the "flip and inspect" trick)
1:28 Quick note on 0.3 mm vs 0.4 mm card thickness
1:41 Swapping out the cylinders for a new message
2:02 Where to find the GitHub repository and report issues

(Insert blocks 2.1, 2.2, 2.3, 2.4, then 2.5 here - in that order, with a single blank line between blocks. All five fit within the 5,000-character cap for this video.)
```

> **Action when pasting into YouTube:** replace the parenthetical with the verbatim contents of [section 2.1](#21-about-the-project-one-paragraph) through [section 2.5](#25-hashtags), in numerical order, with a single blank line between each block.

---

## 6. Captions / subtitles to upload alongside each video

Each YouTube video should have its captions uploaded from the matching `.srt` file in this repo so that closed captions are available immediately (rather than waiting for YouTube's auto-captioning):

| # | Caption file |
|---|---|
| 1 | [`Video_Tutorials/Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/Custom_Braille_Embosser_3d_Printing_Step1.srt`](../../Video_Tutorials/Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/Custom_Braille_Embosser_3d_Printing_Step1.srt) |
| 2 | [`Video_Tutorials/Video_2_Assembling_Braille_Embosser_3D_Printed_Parts/Custom_Braille_Embosser_3d_Printing_Step2.srt`](../../Video_Tutorials/Video_2_Assembling_Braille_Embosser_3D_Printed_Parts/Custom_Braille_Embosser_3d_Printing_Step2.srt) |
| 3 | [`Video_Tutorials/Video_3_How_To_Use_Completed_Braille_Embosser/Custom_Braille_Embosser_3d_Printing_Step3.srt`](../../Video_Tutorials/Video_3_How_To_Use_Completed_Braille_Embosser/Custom_Braille_Embosser_3d_Printing_Step3.srt) |

Upload on YouTube: Studio → Subtitles → select the video → ADD LANGUAGE (English) → Upload file → "Without timing" off (the `.srt` files have timing) → publish.

---

## 7. Pre-publish checklist (per video)

Before saving the new title + description on YouTube, confirm:

- [ ] Title matches section 3.1 / 4.1 / 5.1 exactly (including the "Part X of 3" prefix).
- [ ] Description has the video-specific summary + key takeaways + chapters at the top.
- [ ] **Video 1** has blocks 2.1 (About), 2.2 (Project links), and 2.4 (Acknowledgments - **WATAP and UW CREATE**) pasted in below, in that order. Blocks 2.3 and 2.5 are intentionally omitted because the total would exceed the 5,000-character cap.
- [ ] **Videos 2 and 3** have blocks 2.1, 2.2, 2.3 (Series), 2.4, and 2.5 (Hashtags) pasted in below, in that order.
- [ ] Total description length is at or below YouTube's **5,000-character** limit (paste into YouTube's editor to confirm - the character count is shown live).
- [ ] The first chapter line is `0:00` and at least three chapters are listed (required for YouTube's auto-chapters UI).
- [ ] The matching `.srt` from [section 6](#6-captions--subtitles-to-upload-alongside-each-video) has been uploaded under Subtitles → English.
- [ ] Video is set to **Public** (or **Unlisted** during review), language **English**, category **Howto & Style** (or **Education**), audience **No, it's not made for kids**.
- [ ] The video's URL has been re-confirmed in [`Video_Tutorials/README.md`](../../Video_Tutorials/README.md) and [`README.md`](../../README.md) (if the URL changed for any reason, update both files).

---

## 8. Maintenance plan

- If any of the three videos is re-uploaded with a new URL, update the URL columns in [section 1](#1-quick-reference) of this file, then in [`Video_Tutorials/README.md`](../../Video_Tutorials/README.md), then in the root [`README.md`](../../README.md), and finally in [`Custom_Braille_Embosser_Publishing_Pack.md`](Custom_Braille_Embosser_Publishing_Pack.md) §12.
- If the title is changed, update sections 3.1 / 4.1 / 5.1 above first, then propagate to the iframe `title="..."` attributes in [`Video_Tutorials/README.md`](../../Video_Tutorials/README.md).
- The shared blocks 2.1 - 2.5 are the canonical wording for the WATAP and UW CREATE credit. Edit them here first, then re-paste into each YouTube description.
- If any of the video-specific copy (sections 3.2 / 4.2 / 5.2) is rewritten, re-run the character count against the 5,000-char cap. Video 1 has only ~55 characters of headroom in the current layout, so even short additions there will push it over.
