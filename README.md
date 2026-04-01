# dm-effect-analysis

Reproducible analysis of the Dark Matter Effect within the UQSH (Universal Quantum Foam Hypothesis) framework.

**Author:** Ukshin Q. Rexhepi | ORCID: [0009-0003-4145-5431](https://orcid.org/0009-0003-4145-5431)  
**Tübingen, Germany**

---

## Published Preprint (v1)

**Title:** Dunkle-Materie-Effekt — Eine feldbasierte Interpretation des Dunkle-Materie-Effekts als Folge nicht-kopplungsfähiger Strukturen in einem kontinuierlichen Medium  
**DOI:** https://doi.org/10.6084/m9.figshare.31829263  
**Date:** March 2026

> ⚠️ The analyses in this repository correspond to the published preprint (v1).  
> An extended v2 analysis with g_bar, g_obs, regime_q and D-factor is in preparation.

---

## Repository Structure

```
dm-effect-analysis/
├── RAR/
│   ├── data/
│   │   ├── Rotmod_LTG.zip         ← SPARC rotmod source files
│   │   └── q_fit_results.csv      ← individual q-fits (164 galaxies)
│   ├── figures/
│   │   ├── q_histogram.png        ← used in preprint (v1)
│   │   └── q_by_type.png          ← used in preprint (v1)
│   └── notebooks/
│       ├── rar_analysis_v1.ipynb  ← reproduces preprint figures
│       └── rar_analysis_v2.ipynb  ← extended analysis (in preparation)
│
├── MDAR/
│
├── BTFR/
│   ├── data/
│   │   ├── clean_btfr.csv
│   │   ├── merged_btfr.csv
│   │   └── q_fit_results.csv
│   ├── figures/
│   │   ├── btfr_comparison.png
│   │   └── improvement_vs_acc.png
│   └── notebooks/
│
├── Core-Cusp/
│   ├── data/
│   │   ├── core_slopes.csv
│   │   ├── core_vs_q.csv
│   │   └── core_summary.csv
│   ├── figures/
│   │   ├── fig_core_q_relation.png
│   │   └── fig_core_model_comparison.png
│   └── notebooks/
│       └── core_cusp_analysis.ipynb
│
└── Bullet-Cluster/
    ├── data/
    │   └── bullet_cluster_comparison.csv
    ├── figures/
    └── notebooks/
        └── bullet_cluster_analysis.ipynb
```

---

## Analysis Overview

### RAR — Radial Acceleration Relation
- 163–175 SPARC galaxies
- Individual q-fits per galaxy
- Bimodal regime structure: Peak (q < 1.2), Transition, Diffus (q > 2.5)
- Regime fractions: ~62% Peak, ~12% Transition, ~26% Diffus
- Systematic dependence on galaxy type confirmed

### BTFR — Baryonic Tully-Fisher Relation
- Comparison of standard `Vflat` vs. structurally defined `Vout`
- `Vout` yields slightly smaller global scatter
- Improvement is acceleration-dependent: stronger in high-acceleration regime, nearly absent in low-acceleration regime

### Core-Cusp
- Inner logarithmic slopes: α ≈ 1.7–1.9
- Systematically below NFW expectation (α = 2)
- No classical cuspy or flat-core profiles observed
- Consistent with structured field dynamics (UQSH)

### Bullet Cluster
- Reference: Clowe et al. (2006)
- Measured offsets between gas and lensing peaks: ~219 kpc / ~228 kpc (mean: ~223 kpc)
- UQSH model reproduces spatial separation without additional particle component
- 2D toy model (proof-of-concept; full 3D modelling is future work)

---

## Reproducibility

### RAR (v1)
```
1. Place Rotmod_LTG.zip and q_fit_results.csv in /content/
2. Open RAR/notebooks/rar_analysis_v1.ipynb in Colab
3. Run all cells
→ Reproduces: q_histogram.png, q_by_type.png
```

### Bullet Cluster
```
1. Upload Bullet Cluster reference image to /content/
2. Open Bullet-Cluster/notebooks/bullet_cluster_analysis.ipynb
3. Run all cells
```

---

## Data Source

All analyses are based on the SPARC database:

Lelli, F., McGaugh, S. S., & Schombert, J. M. (2016).  
*SPARC: Mass Models for 175 Disk Galaxies with Spitzer Photometry and Accurate Rotation Curves.*  
The Astronomical Journal, 152, 157.

This repository contains processed analysis products and derived tables only.  
Original SPARC source data should be obtained from the [official SPARC distribution](http://astroweb.cwru.edu/SPARC/).

---

## Citation

```
Rexhepi, U. Q. (2026). Dunkle-Materie-Effekt.
Independent Researcher. Tübingen, Germany.
ORCID: https://orcid.org/0009-0003-4145-5431
DOI: https://doi.org/10.6084/m9.figshare.31829263
GitHub: https://github.com/ukshinrexhepi-cloud/dm-effect-analysis
```
