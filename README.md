# Dark Matter Effect – Reproducible Analysis

This repository contains the reproducible analysis products associated with the study:

**The Dark Matter Effect as Structured Additional Dynamics**  
*Regimes and Acceleration Relations in SPARC Rotation Curves*

## Current status
 q-regime analysis completed (final version used in paper)     
 BTFR comparison completed     
 acceleration-dependent improvement test completed

 ## Bullet Cluster

This section provides a reproducible analysis of the Bullet Cluster
within the UQSH (Universal Quantum Foam Hypothesis) framework.

### Contents

- Extraction of the right-hand panel from Clowe et al. (2006)
- Calibration using the 200 kpc scale bar
- Measurement of spatial offsets between the gas distribution
  and the effective gravitational (lensing) structure
- Comparison with a structure-dependent UQSH field model

### Method

The analysis is based on the reference X-ray + lensing image.
The gas peak and the lensing peaks are identified using
peak-based localization, avoiding centroid bias from diffuse structures.

Distances are converted to physical units using the
200 kpc scale bar embedded in the original figure.

### Results

The measured offsets between gas and lensing peaks are:

- left: 218.7 kpc  
- right: 227.6 kpc  
- mean: 223.2 kpc  

The UQSH model reproduces the same order of magnitude
and yields a consistent spatial separation.

### Interpretation

The results show that the dominant gravitational structure
does not coincide with the collisional gas component,
but instead follows the galaxy distribution.

Within the UQSH framework, this is interpreted as a consequence
of structure-dependent field coupling:

coherent, dynamically stable structures (galaxies) anchor
the effective gravitational field, while diffuse baryonic matter
(gas) contributes but does not determine the location of the
dominant field maxima.

### Reproducibility

To reproduce the analysis:

1. Upload the Bullet Cluster reference PDF to `/content/`
2. Run the notebook `bullet_cluster_analysis.ipynb`
3. Execute all cells in order

The repository contains:
- processed data (`data/`)
- generated figures (`figures/`)
- the full analysis notebook (`notebooks/`)

## Overview

This repository documents an empirical analysis of SPARC rotation curve data with three main components:

1. q-regime analysis of structurally fitted additional dynamics
2. BTFR comparison between the standard flat velocity `Vflat` and a structurally defined outer velocity `Vout`
3. Acceleration-dependent residual analysis testing whether the improvement of `Vout` depends on dynamical regime

## Main results

- The fitted q-distribution shows two preferred regimes with a weakly populated transition zone.
- The structurally defined velocity `Vout` reproduces the baryonic Tully–Fisher relation (BTFR) with nearly identical slope to the standard `Vflat`.
- `Vout` yields a slightly smaller global scatter than `Vflat`.
- This improvement is acceleration-dependent:
  - stronger in the high-acceleration regime
  - nearly absent in the low-acceleration regime

## Repository structure

- `data/` – processed CSV files used in the analysis
- `figures/` – generated plots
- `notebook/analysis.ipynb` – main reproducible notebook
- `docs/notes.md` – short methodological notes

## Data source

The analysis is based on the SPARC database:

Lelli, F., McGaugh, S. S., & Schombert, J. M. (2016).  
*SPARC: Mass Models for 175 Disk Galaxies with Spitzer Photometry and Accurate Rotation Curves.*  
The Astronomical Journal, 152, 157.

This repository contains processed analysis products and derived tables only. Users should obtain the original SPARC source data from the official SPARC distribution.

## Reproducibility

To reproduce the analysis:

1. Install the required Python packages listed in `requirements.txt`
2. Open `notebook/analysis.ipynb`
3. Run the notebook cells in order
4. Use the processed CSV files in `data/` or obtain the original SPARC files from the official source

## Included files

### Data
- `clean_btfr.csv`
- `merged_btfr.csv`
- `q_fit_results.csv`

### Figures
- `btfr_comparison.png`
- `improvement_vs_acc.png`
- `q_histogram.png`
- `q_by_type.png`

## Notes

This repository is intended to document the empirical analysis and improve reproducibility of the reported results.# Dark Matter Effect – Reproducible Analysis

This repository contains the reproducible analysis products associated with the study:

**The Dark Matter Effect as Structured Additional Dynamics**  
*Regimes and Acceleration Relations in SPARC Rotation Curves*

## Overview

This repository documents an empirical analysis of SPARC rotation curve data with three main components:

1. q-regime analysis of structurally fitted additional dynamics
2. BTFR comparison between the standard flat velocity `Vflat` and a structurally defined outer velocity `Vout`
3. Acceleration-dependent residual analysis testing whether the improvement of `Vout` depends on dynamical regime

## Main results

- The fitted q-distribution shows two preferred regimes with a weakly populated transition zone.
- The structurally defined velocity `Vout` reproduces the baryonic Tully–Fisher relation (BTFR) with nearly identical slope to the standard `Vflat`.
- `Vout` yields a slightly smaller global scatter than `Vflat`.
- This improvement is acceleration-dependent:
  - stronger in the high-acceleration regime
  - nearly absent in the low-acceleration regime

## Repository structure

- `data/` – processed CSV files used in the analysis
- `figures/` – generated plots
- `notebook/analysis.ipynb` – main reproducible notebook
- `docs/notes.md` – short methodological notes

## Data source

The analysis is based on the SPARC database:

Lelli, F., McGaugh, S. S., & Schombert, J. M. (2016).  
*SPARC: Mass Models for 175 Disk Galaxies with Spitzer Photometry and Accurate Rotation Curves.*  
The Astronomical Journal, 152, 157.

This repository contains processed analysis products and derived tables only. Users should obtain the original SPARC source data from the official SPARC distribution.

## Reproducibility

To reproduce the analysis:

1. Install the required Python packages listed in `requirements.txt`
2. Open `notebook/analysis.ipynb`
3. Run the notebook cells in order
4. Use the processed CSV files in `data/` or obtain the original SPARC files from the official source

## Included files

### Data
- `clean_btfr.csv`
- `merged_btfr.csv`
- `q_fit_results.csv`

### Figures
- `btfr_comparison.png`
- `improvement_vs_acc.png`
- `q_histogram.png`
- `q_by_type.png`

## Notes

This repository is intended to document the empirical analysis and improve reproducibility of the reported results.
---
## Notes

The merged dataset is constructed by combining:
- derived outer velocities (Vout)
- SPARC baryonic data

The processed dataset is provided as merged_btfr.csv.
---
### Legacy files

The folder `data/legacy/` contains intermediate results from earlier
analysis stages (preprint v1). These files are preserved for transparency
but are not used in the final results reported in the paper.

# UQSH Project

This repository contains analysis and modeling of:

- Radial Acceleration Relation (RAR)
- Core-Cusp problem
- Bullet Cluster analogue

within the Universal Quantum Foam Hypothesis (UQSH).

## Contents

- notebooks: analysis pipelines
- figures: publication-ready figures
- data: processed datasets

## Key Results

- unified explanation of RAR + core-cusp
- nonlocal field effects reproduce core slopes
- Bullet Cluster-like separation without dark matter

## Author

Ukshin Q. Rexhepi  
Tübingen, Germany  
ORCID: https://orcid.org/0009-0003-4145-5431

---

## Paper

📄 Preprint (Figshare):  
https://doi.org/10.6084/m9.figshare.31830892

📄 Local copy:  
https://github.com/ukshinrexhepi-cloud/dm-effect-analysis/blob/main/paper/Dark_Matter_Effect_22_03_26.pdf
