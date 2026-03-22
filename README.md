# dm-effect-analysis
Dark Matter SPARC
# Dark Matter Effect – Reproducible Analysis

This repository contains the reproducible data analysis associated with the paper:

**Dunkle-Materie-Effekt**  
Ukshin Q. Rexhepi (2026)

## Contents

- `data/` → CSV files used and generated in the analysis
- `plots/` → generated figures
- `notebook/analysis.ipynb` → reproducible Colab notebook
- `paper/` → manuscript source files

## Main analysis steps

1. Load `q_fit_results.csv`
2. Classify galaxies by filename-derived type
3. Compute regime fractions
4. Generate:
   - q histogram
   - q by galaxy type boxplot
5. Export summary CSV files

## Main results

- Peak regime: q < 1.2
- Diffuse regime: q > 2.5
- Transition regime: 1.2 <= q < 2.5
