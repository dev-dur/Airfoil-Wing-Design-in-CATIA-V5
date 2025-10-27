# Airfoil Wing Design in CATIA V5
## Overview

This project demonstrates the parametric 3D modeling of an aircraft wing using CATIA V5, where airfoil data from AirfoilTools is imported through an Excel-driven CATIA macro.
The Excel file automates point generation and spline plotting in CATIA to form three airfoil sections (root, mid, and tip), which are later lofted into a complete wing geometry.

## Design Parameters
- Section	Chord Length	Position (mm)	Sweep Offset	Notes
- Root	200 mm	0 mm	0 mm	Base airfoil section
- Mid	150 mm	400 mm	0 mm	Linear taper
- Tip	50 mm	1200 mm	25 mm	12.4° sweep

- Taper Ratio: 0.25
- Sweep Angle: 12.4°

## Design Process
### 1. Airfoil Data Extraction
- Airfoil coordinate data downloaded as .csv from AirfoilTools.com
- Three spanwise sections defined:
    - airfoil_root.csv
    - airfoil_mid.csv
    - airfoil_tip.csv
- Each .csv file contains X–Y coordinate pairs representing the airfoil surface.

### 2. Excel Macro Automation
- The Excel workbook GSD_PointSplineLoftFromExcel.xlsm includes a built-in CATIA macro (VBA).
- The macro automates:
   - Import of .csv data into Excel.
   - Communication with CATIA via CATIA API.
   - Creation of 3D points and splines from the airfoil data directly inside CATIA.
- The macro was executed for all three airfoil sections (root, mid, and tip).
Result: Each section appears in CATIA as a clean spline curve representing its airfoil profile.

### 3. Wing Construction in CATIA
- Each spline was:
    - Scaled according to the chord length (200, 150, and 50 mm).
    - Positioned at the correct spanwise location:
      - Root at 0 mm
      - Mid at 400 mm
      - Tip at 1200 mm
    - Tip airfoil translated 25 mm aft to introduce 12.4° sweep.
- The Multi-Section Surface (Loft) tool was used in the Generative Shape Design (GSD) module to connect the three airfoil profiles into a smooth 3D wing surface.

### 4. Lofting and Verification
- The lofted surface was checked for:
    - Smoothness and continuity.
    - Proper alignment of section edges.
    - Correct geometric scaling and sweep.
- The resulting wing geometry was saved as Airfoil_Wing.CATPart.

## Visual Results
[Uploading wing_design.bmp…]()
![root](https://github.com/user-attachments/assets/b7da433e-cb29-47b7-993b-cb46199cdcca)
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg width="212.02mm" height="45.31mm" viewBox="0 0 212.02 45.31" xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:xlink="http://www.w3.org/1999/xlink">
<title>Airfoil plot (user-000) NACA 2412 Airfoil M=2.0% P=40.0% T=12.0% by AirfoilTools.com</title>
<g transform="translate(206,21.8396)"><g transform="scale(1,-1)"><line fill="none" stroke="green" stroke-width="0.1" x1="-10" x2="-10" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-20" x2="-20" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-30" x2="-30" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-40" x2="-40" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-50" x2="-50" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-60" x2="-60" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-70" x2="-70" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-80" x2="-80" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-90" x2="-90" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-100" x2="-100" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-110" x2="-110" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-120" x2="-120" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-130" x2="-130" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-140" x2="-140" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-150" x2="-150" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-160" x2="-160" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-170" x2="-170" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-180" x2="-180" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-190" x2="-190" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-200" x2="-200" y1="-14.47" y2="21.84"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-206" x2="6.02" y1="10" y2="10"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-206" x2="6.02" y1="20" y2="20"></line><line fill="none" stroke="green" stroke-width="0.1" x1="-206" x2="6.02" y1="-10" y2="-10"></line>
<path fill="none" stroke="red" stroke-width="0.2" d="M 0.02 0.25 L -0.29 0.32 L -1.2 0.5 L -2.72 0.82 L -4.83 1.25 L -7.53 1.78 L -10.79 2.42 L -14.61 3.15 L -18.94 3.95 L -23.78 4.82 L -29.09 5.73 L -34.83 6.68 L -40.99 7.65 L -47.51 8.63 L -54.35 9.6 L -61.49 10.55 L -68.87 11.46 L -76.44 12.32 L -84.17 13.12 L -92 13.84 L -99.88 14.48 L -107.77 15.01 L -115.62 15.42 L -123.39 15.71 L -131.06 15.84 L -138.54 15.79 L -145.78 15.56 L -152.73 15.16 L -159.34 14.59 L -165.57 13.86 L -171.38 12.99 L -176.74 11.98 L -181.6 10.87 L -185.94 9.65 L -189.74 8.36 L -192.96 7.02 L -195.59 5.63 L -197.62 4.22 L -199.03 2.81 L -199.83 1.4 L -200 0 L -199.56 -1.34 L -198.5 -2.57 L -196.86 -3.68 L -194.62 -4.68 L -191.82 -5.57 L -188.47 -6.33 L -184.59 -6.98 L -180.2 -7.5 L -175.34 -7.91 L -170.04 -8.2 L -164.32 -8.39 L -158.22 -8.47 L -151.77 -8.46 L -145.02 -8.37 L -137.99 -8.21 L -130.74 -7.99 L -123.3 -7.73 L -115.67 -7.43 L -107.92 -7.09 L -100.12 -6.7 L -92.31 -6.27 L -84.54 -5.83 L -76.87 -5.37 L -69.33 -4.9 L -61.97 -4.43 L -54.85 -3.98 L -47.99 -3.53 L -41.46 -3.1 L -35.28 -2.69 L -29.49 -2.3 L -24.14 -1.94 L -19.25 -1.61 L -14.87 -1.3 L -11 -1.03 L -7.69 -0.8 L -4.95 -0.61 L -2.8 -0.45 L -1.26 -0.34 L -0.33 -0.27 L -0.02 -0.25 "></path>
<path fill="none" stroke="blue" stroke-width="0.2" d="M -200 0 L 0 0 "></path>
<line fill="none" stroke="black" stroke-width="0.2" x1="-206" x2="6.02" y1="0" y2="0"></line>
<line fill="none" stroke="black" stroke-width="0.2" x1="0" x2="0" y1="-14.47" y2="21.84"></line>
</g>
</g>
<g transform="translate(0,36.3088)"><g transform="scale(2,2)"><text fill="rgb(48,48,144)" font-size="1.8" style="font-family:Arial,Helvetica,sans-serif;" x="1" y="2">Name = NACA 2412 Airfoil M=2.0% P=40.0% T=12.0%</text><text fill="rgb(48,48,144)" font-size="1.8" style="font-family:Arial,Helvetica,sans-serif;" x="1" y="4">Chord = 200mm  Radius = 0mm  Thickness = 100%  Origin = 100%  Pitch = 0&#176; </text></g></g></svg>

## What I Learned
- How to automate airfoil plotting in CATIA using Excel VBA macros and the CATIA API.
- Understanding the relationship between taper ratio, sweep angle, and spanwise geometry.
- Handling coordinate-based modeling and precision scaling of airfoil sections.
- Creating parametric lofted surfaces with smooth continuity between multiple profiles.
- Structuring aerospace CAD projects for traceability and reproducibility.

## Tools Used
- CATIA V5 for Airfoil and wing 3D modeling
- Excel (VBA) for	CATIA macro execution and spline generation
- AirfoilTools.com for Airfoil coordinate database
- CSV Data for Raw coordinate input for airfoils

(Replace these with your own CATIA screenshots)
![Lofted Wing Render](assets/final_render.png)
