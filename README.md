# Dark Matter Effect – Reproducible Analysis

This repository contains the reproducible data analysis associated with the paper:

**Dunkle-Materie-Effekt**  
Ukshin Q. Rexhepi (2026)

---

## Overview

This project presents a systematic analysis of 163 galaxy rotation curves from the SPARC database.

The empirical additional term is defined as:

C(r) = v_obs² - v_bar²

After normalization, the resulting profiles reveal a bimodal structure in the scale parameter *q*, indicating two preferred dynamical regimes.

---

## Main Results

The distribution of the parameter *q* shows:

- **Peak regime:** q < 1.2 (~62%)
- **Diffuse regime:** q > 2.5 (~26%)
- **Transition regime:** 1.2 ≤ q < 2.5 (~12%)

These results indicate the presence of two preferred dynamical states with a weakly populated transition region.

---

## Additional Insight

A more detailed analysis shows that the assignment to these regimes is not strictly determined by galaxy type.

Mean q-values by galaxy type:

- Dwarf: ~0.5  
- LSB: ~1.0  
- ESO: ~1.05  
- UGC: ~1.25  
- NGC: ~1.6  
- IC: ~3.0  

This suggests that the observed regimes correspond to **dynamical states** rather than fixed morphological classifications.

---

## Repository Structure

- `data/` → CSV files used and generated in the analysis  
- `plots/` → generated figures (histograms and boxplots)  
- `notebook/analysis.ipynb` → full reproducible Colab notebook  
- `paper/` → manuscript source files  

---

## Reproducibility

All results can be reproduced using the provided notebook:

`notebook/analysis.ipynb`

The workflow includes:

1. Loading the dataset (`q_fit_results.csv`)
2. Classification of galaxies by filename-derived type
3. Computation of regime fractions
4. Generation of plots:
   - q distribution (histogram)
   - q vs galaxy type (boxplot)
5. Export of summary tables

---

## Author

Ukshin Q. Rexhepi  
Tübingen, Germany  
ORCID: https://orcid.org/0009-0003-4145-5431

---

## Paper

📄 Preprint (Figshare):  
https://doi.org/10.6084/m9.figshare.31829263

📄 Local copy:  
paper/paper.pdf
