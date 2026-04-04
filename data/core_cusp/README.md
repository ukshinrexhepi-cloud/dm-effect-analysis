# Core Cusp UQSH Final

## Zweck
Finale reproduzierbare Analyse des Core-Cusp Problems
im Rahmen der Universellen Quanten-Schaum-Hypothese (UQSH).

## Hauptbefund
Drei empirisch unterscheidbare Regime der Core-Cusp Dynamik
in 175 SPARC-Galaxien:

Klein (r_max < 16 kpc, n=107):
  - Systemgröße kein signifikanter Treiber (r=-0.078, p=0.42)
  - Gamma-Sättigungsterm aktiv: 93-99% core-bildend
  - Feld hat noch Toleranz

Übergang (16-30 kpc, n=32):
  - Beide Mechanismen gleichwertig
  - Median alpha=1.94, nahe NFW
  - Ablösungspunkt der zwei Regime

Groß (r >= 30 kpc, n=36):
  - Systemgröße dominiert (r=-0.383, p=0.02)
  - 81% core-artig
  - Großskalige Feldspannung überdeckt Gamma-Term

Gesamt: r=-0.461, p<0.0001
Kruskal-Wallis: H=33.1, p<0.0001

## Verwendete Daten
- SPARC ROTMOD: Rotmod_LTG.zip (Lelli et al. 2016)
- q-Fit Ergebnisse: q_fit_results.csv

## Ausführung
1. Rotmod_LTG.zip und q_fit_results.csv in Colab hochladen
2. core_cusp_uqsh_final.ipynb öffnen
3. Alle Zellen ausführen
4. Ergebnisse in ergebnisse_csv/ und abbildungen/

## Referenzen
- de Blok (2009): The Core-Cusp Problem, arXiv:0910.3538
- Lelli et al. (2016): SPARC, AJ 152, 157
- Rexhepi (2026): Fundamente der UQSH
- Rexhepi (2026): Black Holes - The Immortal Life-Givers
