# Design, CFD Simulation, and Experimental Validation of a Compact TPMS (Gyroid) Heat Exchanger

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![CFD](https://img.shields.io/badge/Tool-STAR--CCM+-blue)
![CAD](https://img.shields.io/badge/CAD-SolidWorks%20%26%20nTop-orange)
![3D Printing](https://img.shields.io/badge/Manufacturing-SLA%20Resin-red)

## 📖 Overview
This project presents the design and validation of a high-performance compact heat exchanger (CHX) based on a **Triply Periodic Minimal Surface (TPMS) Gyroid lattice**. The goal was to maximize thermal efficiency per unit volume while minimizing solid material usage, targeting air-to-air applications with very low flow rates (`900 NL/h` hot, `200 NL/h` cold).

The work follows a complete engineering workflow:
1. **Analytical Sizing** (Thermodynamic calculations & NTU method).
2. **CAD Modeling** (SolidWorks for casing, nTop for the implicit Gyroid generation).
3. **Numerical Simulation** (Conjugate Heat Transfer analysis in Siemens STAR-CCM+).
4. **Experimental Validation** (SLA 3D printing and lab testing).

## 🔬 Key Features
- **Architecture:** Gyroid TPMS (Unit cell: 10 mm, Wall thickness: 1 mm).
- **Specific Surface Area:** `~291 m²/m³` (extremely compact).
- **Flow Regime:** Strictly laminar (`Re_hot ≈ 94`, `Re_cold ≈ 21`).
- **Manufacturing:** Designed for SLA/DLP resin 3D printing (self-supporting structure).

## 📊 Key Results
| Metric | CFD (Ideal Adiabatic) | Experiment (Real World) |
| :--- | :--- | :--- |
| **Effectiveness (ε)** | ~ **100%** | ~ **35%** |
| **Heat Exchanged** | `1.26 W` | `0.44 W` |
| **Hot Side ΔP** | `29.08 Pa` | *(Validated via CFD)* |
| **Cold Side ΔP** | `2.38 Pa` | *(Validated via CFD)* |

> **⚠️ Note on Discrepancy:** The significant drop in experimental performance is primarily attributed to **environmental heat leakage** (lack of insulation on the casing) and the **thermal buffer effect** caused by the heater's 10s ON/OFF duty cycle interacting with the resin's thermal inertia. The aerodynamic performance (pressure drop) was perfectly validated.

## 🛠️ Technologies & Tools
- **CAD & Geometry:** SolidWorks (Envelope), nTop (Implicit Modeling & Meshing).
- **CFD Solver:** Siemens STAR-CCM+ (Polyhedral mesh, Conjugate Heat Transfer).
- **Manufacturing:** SLA 3D Printing (Standard Photopolymer Resin).
- **Programming/Analysis:** Python / MATLAB (for experimental data post-processing - *recommend you add this if you used it*).

## 📁 Repository Structure
```
.
├── docs/
│   └── TPMS_Gyroid_Heat_Exchanger_Full_Report.pdf   # Complete project thesis/report
├── images/
│   ├── cad_envelope.png
│   ├── cfd_temperature_field.png
│   └── experimental_setup.jpg
└── README.md
```

## 📄 Full Report
For a detailed description of the analytical models, mesh independence study, and transient thermal analysis, please refer to the [Full Project Report](docs/TPMS_Gyroid_Heat_Exchanger_Full_Report.pdf).

---

*Project developed for the "Modeling of Advanced Heat Transfer Problems" course - Politecnico di Torino (Academic Year 2025/2026).*
