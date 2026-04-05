# dm-effect-analysis

Reproducible analysis of the Dark Matter Effect within the UQSH 
(Universal Quantum Foam Hypothesis) framework.

**Author:** Ukshin Q. Rexhepi | Independent Researcher, Tübingen, Germany  
**ORCID:** [0009-0003-4145-5431](https://orcid.org/0009-0003-4145-5431)  
**GitHub:** [Universal-Quantum-Foam-Hypothesis-UQSH-](https://github.com/ukshinrexhepi-cloud/Universal-Quantum-Foam-Hypothesis-UQSH-)

---

## Published Preprint (v1)

**Title:** Bimodal Regime Structure in Galactic Rotation Curves: 
Evidence for Distinct Dynamical States and a Field-Based 
Interpretation of the Dark Matter Effect  
**Preprints.org ID:** 206674  
**Date:** April 2026  
**Status:** Pending Check

---

## Repository Structure
---

## Repository Structure

dm-effect-analysis/
├── data/
│   ├── btfr/
│   │   ├── clean_btfr.csv         ← 102 core sample galaxies
│   │   └── merged_btfr.csv        ← full merged dataset
│   ├── bullet_cluster/        ← Bullet Cluster analysis data
│   ├── core_cusp/                 ← inner slope data
│   ├── derived/
│   │   └── rar_analysis_v1.ipynb  ← legacy notebook
│   ├── mdar/                      ← MDAR data
│   └── rar/                       ← q-fit results (164 galaxies)
│
├── notebook/
│   ├── rar_analysis.ipynb         ← RAR + regime analysis
│   ├── btfr_analysis.ipynb        ← BTFR comparison
│   ├── core_cusp_uqsh_final.ipynb ← Core-Cusp analysis
│   ├── mdar_analysis.ipynb        ← MDAR analysis
│   └── bullet_cluster_analysis.ipynb
│
├── figures/                       ← all output figures
├── plots/rar/                     ← RAR specific plots
└── docs/                          ← notes and documentation

---

---

## Analysis Overview

### RAR — Radial Acceleration Relation
- 164 SPARC galaxies
- Individual q-fits per galaxy
- Bimodal regime structure discovered:
  - Peak (q < 1.2): 102 galaxies, 62.2%
  - Transition: 20 galaxies, 12.2%
  - Diffuse (q > 2.5): 42 galaxies, 25.6%
- Systematic dependence on galaxy type confirmed

### BTFR — Baryonic Tully-Fisher Relation
- 102 core sample galaxies
- Vout (median of last 3 points) vs. standard Vflat
- Global scatter: σ_flat = 0.222, σ_out = 0.220
- Improvement acceleration-dependent

### Core-Cusp
- 175 galaxies, inner logarithmic slopes α
- Median α = 2.09, range 0.60–3.81
- Strong correlation with galaxy size (r = −0.476, p < 0.0001)
- Consistent with field saturation limit (UQSH)

### Bullet Cluster
- Reference: Clowe et al. (2006)
- Measured offsets: 218.7 kpc / 227.6 kpc (mean: 223.15 kpc)
- UQSH model reproduces separation without dark matter particles

---

## Data Source

All analyses are based on the SPARC database:

Lelli, F., McGaugh, S. S., & Schombert, J. M. (2016).  
*SPARC: Mass Models for 175 Disk Galaxies with Spitzer Photometry 
and Accurate Rotation Curves.*  
The Astronomical Journal, 152, 157.

Original SPARC data: [astroweb.cwru.edu/SPARC](http://astroweb.cwru.edu/SPARC/)


```
