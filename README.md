# Airfoil Wing Design in CATIA V5
## Overview
This project demonstrates the parametric modeling of an aircraft wing using CATIA V5, where airfoil coordinate data was imported through an Excel-based CATIA macro.
The objective was to design a three-section lofted wing with controlled taper, sweep, and section transitions, essential parameters in preliminary aircraft design.

## Design Parameters
| Section  | Chord Length | Position (mm) | Sweep Offset (mm) | Notes                     |
| -------- | ------------ | ------------- | ----------------- | ------------------------- |
| **Root** | 200 mm       | 0             | 0                 | Base airfoil section      |
| **Mid**  | 150 mm       | 400           | 0                 | Linear taper transition   |
| **Tip**  | 50 mm        | 1200          | 25                | 12.4° swept trailing edge |

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
- The resulting wing geometry was saved as airfoil.CATPart.

## Visual Results
### Preview
<img width="1496" height="673" alt="PREVIEW" src="https://github.com/user-attachments/assets/680f8baa-43c8-4094-8960-dfb85bf8ac79" />

### Root section
<img width="1490" height="321" alt="root" src="https://github.com/user-attachments/assets/36f01e76-025a-46a0-b6cf-f026534e7482" />

### Mid section
<img width="1493" height="323" alt="mid" src="https://github.com/user-attachments/assets/214b7604-7472-40ef-817a-aadcefb3ac13" />

### Tip section
<img width="1246" height="277" alt="tip" src="https://github.com/user-attachments/assets/298cf995-d6af-472a-8f6c-57fbb63bfad0" />

## What I Learned
- Understanding the relationship between taper ratio, sweep angle, and spanwise geometry.
- Handling coordinate-based modeling and precision scaling of airfoil sections.
- Constructing multi-section lofts with smooth aerodynamic surfaces.

## Tools Used
- CATIA V5 for Airfoil and wing 3D modeling
- Excel (VBA) for	CATIA macro execution and spline generation
- AirfoilTools.com for Airfoil coordinate database
- CSV Data for Raw coordinate input for airfoils
