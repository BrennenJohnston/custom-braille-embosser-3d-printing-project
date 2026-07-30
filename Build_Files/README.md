<!--- Open Source Assistive Technology Template: GitHub Build_Files Readme Version 1.2 (2025-Feb-04) --->
This folder contains the build files for the Custom Braille Embosser. The device has no firmware or PCB; only `3D_Printing_Files` are required.

## Subfolders
- [`3D_Printing_Files/STL/`](3D_Printing_Files/STL) - the 10 part STL files (Body Base, Body Top, Embosser Holder A1/A2, Counter Holder B1/B2, Grip Extension Bottom/Top, Handle Connector, Handle Grip), all v1.0 at 0.2 mm layer height.
- [`3D_Printing_Files/Print_Profiles/X1C/`](3D_Printing_Files/Print_Profiles/X1C) - sliced `.3mf` files for the Bambu Lab X1C printer, with the parts already arranged on the plate, supports configured, and companion markdown notes documenting the exact slicer settings used for this initial posting.
- [`3D_Printing_Files/Embossing_Plates_Examples/`](3D_Printing_Files/Embossing_Plates_Examples) - example pre-generated cylindrical embossing-and-counter-plate pairs for 0.3 mm and 0.4 mm card stock. Print one of these first to verify your printer and embosser before generating user-specific plates.
- [`3D_Printing_Files/Embossing_Plates_Customizer/`](3D_Printing_Files/Embossing_Plates_Customizer) - tools for generating new plates for arbitrary text. Two officially supported customizer paths:
  - **Primary - Web-based customizer** (recommended for most users): <https://braille-cylinder-stl-generator.vercel.app> (auto-translates English to Grade 1 / Grade 2 braille; runs in any browser; no install).
  - **Alternative - OpenSCAD offline customizer**: a vendored copy of [`braille-cylinder-stl-generator-openscad`](https://github.com/BrennenJohnston/braille-cylinder-stl-generator-openscad) at [`3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative/`](3D_Printing_Files/Embossing_Plates_Customizer/OpenSCAD_Offline_Alternative) for offline use and full parametric control.
