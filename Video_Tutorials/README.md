# Custom Braille Embosser - Video Tutorials

Three step-by-step tutorial videos cover the full lifecycle of the device:

1. **Customizing the braille content, downloading STLs, and adjusting 3D-print settings**
2. **Assembling the 3D-printed parts into a working embosser**
3. **Using the completed embosser to emboss card stock**

The videos are hosted on YouTube, so they can be embedded in [MakerWorld](https://makerworld.com/), [Printables](https://www.printables.com/), [Thingiverse](https://www.thingiverse.com/), or any external listing.

> **The `.mp4` files are not in this repository.** Each recording is 368-705 MB,
> past GitHub's 100 MB per-file limit, and Git LFS's free tier is 1 GB total —
> mirroring 1.5 GB of video here would cost money and make every clone enormous.
> The `.mp4` files stay in the maintainer's local copy of this folder (they are
> gitignored), and the videos are published on YouTube, which is where people
> actually watch them.
>
> **What is published here:** the `.srt` captions, the per-step assembly
> screenshots in [`Video_2_Screen_Shots/`](Video_2_Screen_Shots), the thumbnails,
> and the transcript-derived
> [written tutorial](Custom_Braille_Embosser_Written_Tutorial.md). Anyone without
> internet access, or who prefers reading, gets the whole procedure in text and
> images. The [Maker Guide](../Documentation/Custom_Braille_Embosser_Maker_Guide.pdf)
> covers the same ground.
>
> If you want the source `.mp4` files for re-hosting under the project's
> CC BY-SA 4.0 license, [open an issue](https://github.com/BrennenJohnston/custom-braille-embosser-3d-printing-project/issues)
> and they can be attached to a GitHub release.

Companion content elsewhere in the repo:

- The transcript-backed written tutorial: [`Custom_Braille_Embosser_Written_Tutorial.md`](Custom_Braille_Embosser_Written_Tutorial.md). This file is derived from the `.srt` sources in this folder and should be kept in sync with them.
- The canonical YouTube titles and descriptions (with WATAP / UW CREATE acknowledgments and project links): [`Documentation/_drafts/YouTube_Video_Descriptions.md`](../Documentation/_drafts/YouTube_Video_Descriptions.md). Edit that file first if you change a title or description on YouTube.

## Canonical YouTube titles

Use these titles on YouTube and anywhere a title is needed (iframe `title=` attributes, social posts, etc.):

1. **Custom Braille Embosser - Part 1 of 3: Customize Braille, Download STLs & 3D-Print Settings**
2. **Custom Braille Embosser - Part 2 of 3: Assembling the 3D-Printed Parts**
3. **Custom Braille Embosser - Part 3 of 3: How to Use the Completed Embosser**

## Quick links

| # | Topic | YouTube | Captions in this repo |
|---|---|---|---|
| 1 | Customize braille, download STLs, 3D-print settings | <https://youtu.be/m71VNZq28MI> | [`.srt`](Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/Custom_Braille_Embosser_3d_Printing_Step1.srt) |
| 2 | Assembling the 3D-printed parts | <https://youtu.be/x-uPNtT2Gqk> | [`.srt`](Video_2_Assembling_Braille_Embosser_3D_Printed_Parts/Custom_Braille_Embosser_3d_Printing_Step2.srt) + [screenshots](Video_2_Screen_Shots) |
| 3 | How to use the completed Custom Braille Embosser | <https://youtu.be/77iXvJbkXh4> | [`.srt`](Video_3_How_To_Use_Completed_Braille_Embosser/Custom_Braille_Embosser_3d_Printing_Step3.srt) |

## Snippets to copy/paste into MakerWorld / Printables / blog posts

### Markdown links (works on Printables, GitHub, MakerWorld description fields, generic blogs)

```markdown
**Custom Braille Embosser - Tutorial videos:**

1. [Part 1 of 3 - Customize Braille, Download STLs & 3D-Print Settings (YouTube)](https://youtu.be/m71VNZq28MI)
2. [Part 2 of 3 - Assembling the 3D-Printed Parts (YouTube)](https://youtu.be/x-uPNtT2Gqk)
3. [Part 3 of 3 - How to Use the Completed Embosser (YouTube)](https://youtu.be/77iXvJbkXh4)
```

### Long-form YouTube URLs (for "Add Video" fields that require `youtube.com/watch?v=…`)

| # | Long URL |
|---|---|
| 1 | `https://www.youtube.com/watch?v=m71VNZq28MI` |
| 2 | `https://www.youtube.com/watch?v=x-uPNtT2Gqk` |
| 3 | `https://www.youtube.com/watch?v=77iXvJbkXh4` |

### HTML iframe embeds (for sites that allow embed code)

```html
<!-- Video 1 - Customize braille, download STLs, 3D-print settings -->
<iframe width="560" height="315"
  src="https://www.youtube.com/embed/m71VNZq28MI"
  title="Custom Braille Embosser - Part 1 of 3: Customize Braille, Download STLs & 3D-Print Settings"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen></iframe>

<!-- Video 2 - Assembling the 3D-printed parts -->
<iframe width="560" height="315"
  src="https://www.youtube.com/embed/x-uPNtT2Gqk"
  title="Custom Braille Embosser - Part 2 of 3: Assembling the 3D-Printed Parts"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen></iframe>

<!-- Video 3 - How to use the completed embosser -->
<iframe width="560" height="315"
  src="https://www.youtube.com/embed/77iXvJbkXh4"
  title="Custom Braille Embosser - Part 3 of 3: How to Use the Completed Embosser"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen></iframe>
```

### Thumbnail-style markdown (Printables / blog)

Each video's auto-generated YouTube thumbnail can be linked back to the watch page:

```markdown
[![Video 1 thumbnail](https://img.youtube.com/vi/m71VNZq28MI/hqdefault.jpg)](https://youtu.be/m71VNZq28MI)
[![Video 2 thumbnail](https://img.youtube.com/vi/x-uPNtT2Gqk/hqdefault.jpg)](https://youtu.be/x-uPNtT2Gqk)
[![Video 3 thumbnail](https://img.youtube.com/vi/77iXvJbkXh4/hqdefault.jpg)](https://youtu.be/77iXvJbkXh4)
```

## Other media (maintainer's local copy only)

For reference / archival, the maintainer's copy of this folder also contains the
following. Like the tutorial recordings, these are gitignored rather than
published — they are supplementary renders, not the primary tutorials, and are
not uploaded to YouTube.

| File | Description |
|---|---|
| `Braille_Embosser_Assembly_v1_0_Animation.avi` | Original CAD-driven assembly animation rendered out of Fusion 360 (no narration). |
| `Braille_Embosser_Assembly_Video_Simulation_1.mp4` | Earlier simulation render of the assembly sequence. |
| `Braille_Embosser_Assembly_Video_Simulation_2.mp4` | Updated simulation render. |

Animated GIFs of the same simulation and of the device in use **are** published,
in [`../Photos/Gif/`](../Photos/Gif).

## Captions / subtitles

Each YouTube video has its captions auto-uploaded from the matching `.srt` files in this folder. If you re-upload elsewhere, you can attach the same `.srt` for built-in captions support:

- Video 1 captions: `Video_1_Customizing_Braille_Downloading_STL_3D_Print_Settings/Custom_Braille_Embosser_3d_Printing_Step1.srt`
- Video 2 captions: `Video_2_Assembling_Braille_Embosser_3D_Printed_Parts/Custom_Braille_Embosser_3d_Printing_Step2.srt`
- Video 3 captions: `Video_3_How_To_Use_Completed_Braille_Embosser/Custom_Braille_Embosser_3d_Printing_Step3.srt`

## License

The videos are part of the Custom Braille Embosser project's "accompanying material" and are released under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). You may redistribute, re-host, re-mix, or re-caption them as long as you (a) attribute Brennen Johnston, (b) license your derivative under the same CC BY-SA 4.0 terms, and (c) link back to this repository: <https://github.com/BrennenJohnston/custom-braille-embosser-3d-printing-project>.
