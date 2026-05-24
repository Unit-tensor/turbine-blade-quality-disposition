# Turbine Blade Defect Disposition
### GE Aerospace Supply Chain Quality Engineering Simulation

## Overview
This project simulates the role of a supply chain quality engineer at GE Aerospace, 
responsible for dispositioning non-conforming turbine blades on the shop floor.

Three blades (Part No. 65015-40030-007) were flagged by technicians for non-conformance 
at Characteristic 22 (EDM hole). Each blade was evaluated against the engineering drawing 
and GES 251-004 (EDM specification for turbine blades) to determine the appropriate disposition.

---

## Files
| Folder | Contents |
|---|---|
| `drawings/` | Engineering drawing for Blade 65015-40030-007 |
| `specs/` | GES 251-004 — EDM specification for turbine blades |
| `router_notes/` | Technician router notes for each non-conforming blade |
| `output/` | Completed Defect Disposition Forms (Excel) |

---

## Disposition Results

| Serial Number | Non-Conformance | Disposition |
|---|---|---|
| GB31904 | Hole oversized (0.022 in) + out of position toward leading edge | REJECT / SCRAP |
| GB33710 | Hole oversized (0.028 in) | REJECT / SCRAP |
| GB34865 | Hole undersized (0.013 in) | REWORK |

---

## Engineering Logic Applied

- **Drawing spec:** Characteristic 22 calls for 11x holes at Ø0.020 in, with position tolerance of 0.005 in (datum A-B-C)
- **GES 251-004 rules:**
  - Oversized holes → cannot be reworked → scrap
  - Undersized holes → may be reworked to print dimensions → re-inspect after
  - Out-of-position holes → engineering review only if hole is NOT oversized

## Tools Used
- GE Aerospace engineering drawing (ASME Y14.5 GD&T)
- GES 251-004 EDM specification
- Microsoft Excel (defect disposition documentation)
