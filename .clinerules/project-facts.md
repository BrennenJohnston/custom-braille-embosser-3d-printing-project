# Project Facts — custom-braille-embosser-3d-printing-project (always active)

Fully 3D-printed hand braille embosser (no fasteners, no electronics).
Working branch: main.

1. The OpenSCAD customizer lives at Build_Files\3D_Printing_Files\
   Embossing_Plates_Customizer\OpenSCAD_Offline_Alternative\ — the scad-check
   script sits IN that folder and must be run FROM that folder:
   powershell -ExecutionPolicy Bypass -File scad-check.ps1
2. That folder holds TWO copies of Braille_Cylinder_STL_Generator.scad: the
   main one, and MakerWorld_Upload\ (upload mirror). Edit the main copy, then
   mirror the change to MakerWorld_Upload deliberately — never let them drift.
3. Canonical braille constants (do not change without my approval): dot
   spacing 2.5 / cell 6.5 / line 10.0 mm; dot map [[0,0],[1,0],[2,0],[0,1],
   [1,1],[2,1]] = dots 1–6. Full geometry specs live in
   braille-cylinder-stl-generator\docs\specifications\.
4. Embossing force and lever geometry are the accessibility features of the
   assembled device — changes to plate thickness or dot recess depths affect
   embossing quality; propose with trade-offs, I decide.
