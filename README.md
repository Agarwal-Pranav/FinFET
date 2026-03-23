# Interface Trap Analysis in Multi-Fin FinFET Technology

## Project Overview
This repository contains the research and simulation framework for analyzing **Interface Trap Charges** in modern FinFET architectures. Developed in February 2025 as part of the **Machine Learning Architectures** course, this project bridges the gap between semiconductor device physics and predictive modeling.

The study focuses on **Negative Bias Temperature Instability (NBTI)**, investigating how traps at the $Si/HfO_2$ interface degrade performance in both single-fin and multi-fin configurations.

---

## Key Research Objectives
* **Structure Modeling:** Design and mesh single and multi-fin FinFETs using **Silvaco TCAD**.
* **Reliability Analysis:** Simulate the NBTI effect by introducing density of interface traps ($N_{it}$).
* **Parameter Impact:** Quantify degradation in:
    * **DC Characteristics:** Threshold voltage shift ($\Delta V_{th}$), Drain Current ($I_d$), and Subthreshold Swing (SS).
    * **AC Characteristics:** Gate Capacitance ($C_{gg}$) and Transconductance ($g_m$).
* **Data Generation:** Create a high-fidelity dataset for training ML architectures to predict device reliability.

---

## Technical Specifications

### 1. Device Simulation (Silvaco TCAD)
The simulations utilize the **Atlas** and **Victory Device** modules:
* **Gate Stack:** High-k dielectric ($HfO_2$) with Metal Gate.
* **Physics Models:** * `FERMI` (Fermi-Dirac statistics)
    * `SRH` (Shockley-Read-Hall recombination)
    * `ALBRCT.N` (Inversion layer mobility models)
* **Trap Modeling:** Interface states modeled with donor/acceptor distributions within the bandgap.

### 2. Comparative Analysis: Single vs. Multi-Fin
| Feature | Single-Fin | Multi-Fin |
| :--- | :--- | :--- |
| **Effective Width ($W_{eff}$)** | Lower | Higher (Parallel Fins) |
| **Current Drive** | Standard | Enhanced |
| **Trap Sensitivity** | High local impact | Distributed impact across fins |
| **Thermal Profile** | Faster dissipation | Potential self-heating concerns |

---

## Repository Structure
```text
├── src/
│   ├── single_fin_nbti.in     # Silvaco Input file for Single-Fin
│   └── multi_fin_nbti.in      # Silvaco Input file for Multi-Fin
├── data/
│   ├── dc_characteristics.csv  # Extracted Id-Vg data
│   └── ac_characteristics.csv  # Extracted Capacitance/Frequency data
├── notebooks/
│   └── analysis_plots.ipynb    # Python visualization of degradation
├── docs/
│   └── Project_Report.pdf      # Detailed Feb 2025 Project Report
└── README.md
