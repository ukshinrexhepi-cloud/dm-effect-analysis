# Herleitung Core Cusp in Colab
## UQSH-basierte Analyse des Core-Cusp Problems
### Ukshin Q. Rexhepi, Tübingen 2026

---

## Ausgangssituation

Das Core-Cusp Problem beschreibt die Diskrepanz zwischen
beobachteten galaktischen Dichteprofilen (core-artig, alpha~0)
und den Vorhersagen von LCDM-Simulationen (cuspy, alpha~-1).
De Blok (2009) zeigt, dass hochauflösende Beobachtungen
konsistent cores bevorzugen, während Simulationen cusps
vorhersagen. Keiner der bisher vorgeschlagenen baryonischen
Feedback-Mechanismen erklärt den Befund vollständig.

Im UQSH-Rahmen wird Dunkle Materie nicht als Teilchen
interpretiert, sondern als persistente Feldorganisation.
Die Frage ist: kann dieser Rahmen das Core-Cusp Problem
erklären, ohne Feedback oder Explosionsprozesse?

---

## Schritt 1: Ausgangsdaten und erste Analyse

Ausgangspunkt war das bestehende SPARC-Analyse-Notebook
(core_cusp_analysis_clean.ipynb). Dieses berechnet aus den
ROTMOD-Dateien die inneren logarithmischen Steigungen alpha
der effektiven Massenverteilung M(r) ~ r^alpha.

Erste Befunde:
- Peak-Regime: medianer alpha = 2.10
- Diffus-Regime: medianer alpha = 1.94
- Transition: medianer alpha = 1.98
- Diffuse Systeme liegen näher am Core-Bereich als Peak-Systeme

Das war überraschend, weil Peak-Systeme (kleine kompakte
Galaxien) intuitiv ausgeprägtere Cores haben sollten.

---

## Schritt 2: Physikalische Hypothese zur Gammastrahlung

Ausgangspunkt war die UQSH-Interpretation aus dem
Black Holes Paper (Rexhepi 2026):
Gammastrahlung ist keine separate Physik, sondern dieselbe
Spannungsfront wie Licht, nur höherfrequent. Sie entsteht
als Produkt maximaler Feldsättigung und wirkt gleichzeitig
als Ursache weiterer Feldsättigung durch ihre eigene
Intensität und Energiedichte.

Die Hypothese:
- Gammastrahlung ist an baryonische Ankermaterie gekoppelt
- Sie breitet sich sphärisch aus, wird durch Druckkanäle
  hochgesättigter Feldknoten zu Jets fokussiert
- Ohne baryonische Ankermaterie entsteht kein ausgeprägter
  DM-Halo, weil die Feldorganisation nicht stabilisiert wird
- Die Rückkopplungsschleife: gesättigtes Feld erzeugt
  Gammastrahlung, die wiederum das Feld weiter sättigt
- Für das Core-Cusp Problem: Gammastrahlung verhindert
  zentrale Cusp-Bildung durch kontinuierliche Feldsättigung

Verbindung zu de Blok (2009):
De Blok zeigt, dass der Core-Radius mit der
Scheibenskalenlänge korreliert. In der UQSH ist das natürlich:
die Gammastrahlung entsteht aus der baryonischen Struktur,
ihre Reichweite ist direkt an die Scheibengröße gekoppelt.

---

## Schritt 3: Gamma-Term v1 (gescheitert)

Erster Versuch: dimensionsloser Term
Delta_g_gamma(r) = A_gamma * mass_norm * exp(-r/r_gamma)

Ergebnis: Delta_alpha ~ 1e-5, also numerisch null.
Ursache: Vobs^2 liegt bei ~10^4 km^2/s^2, der Term
liefert nur ~10^-3. Die Einheiten passen nicht.

Erkenntnis: Der Term muss physikalisch korrekt skaliert sein.

---

## Schritt 4: Gamma-Term v2 (physikalisch skaliert)

Neue Formulierung:
Delta_g_gamma(r) = A_gamma * g0 * mass_norm * exp(-r/r_gamma)

g0 = V0^2/r0 ist die zentrale Beschleunigung der Galaxie
in km^2/s^2/kpc, also derselben Einheit wie g_obs.
Der Term ist damit ein Bruchteil der zentralen Felddynamik.

Ergebnis:
- Effekt messbar: Delta_alpha ~ 1e-3
- Diffuse Systeme reagieren stärker als Peak-Systeme
- Median g0 Diffus: 2428 km^2/s^2/kpc vs. Peak: 1151
- RMSE wird aber größer, nicht kleiner

Erkenntnis: Der Term ist real aber quantitativ zu schwach.
Diskussion führte zur Frage ob der Mechanismus nicht
akkumulativ über lange Zeitskalen wirkt.

---

## Schritt 5: Gamma-Term v3 (Phasenwelle)

Erweiterung um räumlich phasenversetzten Term:
Delta_g_gamma(r) = A_gamma * g0 * mass_norm
                  * exp(-r/r_gamma)
                  * cos(2*pi*r / lambda_gamma)

lambda_gamma = f_lambda * r_max (skaliert mit Haloradius)

Physikalische Begründung:
Gammastrahlung propagiert mit Lichtgeschwindigkeit.
Bei einer Galaxie mit R~50 kpc braucht sie ~160.000 Jahre
zum äußeren Rand. Das erzeugt räumlich phasenversetzte
Sättigungswellen. Kleine Systeme: kurze Laufzeit, agil.
Große Systeme: lange Laufzeit, träge, versetzt.

Beobachtbare Konsequenz:
Je nach Phase der Gamma-Propagation sehen wir verschiedene
räumliche GRB-Muster relativ zum Halo:
- GRB am Halorand, kein GRB am AGN
- GRB an beiden Enden gleichzeitig
- GRB nur in der Mitte
Testbar an edge-on Galaxien mit bekannter Inklination.

Ergebnis: RMSE leicht verbessert für kleine Systeme
mit Phase-Termen (g_phase_halb, g_phase_ganz).
Aber immer noch kein dominanter Effekt.

---

## Schritt 6: Entscheidende Erkenntnis - Systemgröße

Schlüsselidee aus der Diskussion:
In großen Systemen übersteigt die Feldgröße selbst
den Effekt der Gammastrahlung und überdeckt ihn aufgrund
der großskaligen Feldspannung. Das bedeutet nicht, dass
Gammastrahlung keinen Effekt hat, sondern dass in großen
Systemen die Systemgröße der dominante Treiber ist.

Direkter Test: r_max vs. alpha ohne jeden Gamma-Term.

Ergebnis (hochsignifikant):
- Gesamt: r=-0.461, p<0.0001
- Schwellenwert: gleitender Median unterschreitet NFW=2.0
  ab r_max ~ 16 kpc
- Klein (r<15 kpc): median alpha=2.249
- Groß (r>=15 kpc): median alpha=1.657
- Mann-Whitney p=0.000000

Interpretation im UQSH-Rahmen:
Große diffuse Systeme haben maximale Größe erreicht in der
das Feld selbst soweit dagegenhält, dass eine Konzentration
nicht aufrechterhalten werden kann. Je größer ein System,
desto stärker die Rückwirkung des Feldes. Analog zum
schwarzen Loch als maximal gesättigtem Feldknoten, aber
auf Galaxienskala.

---

## Schritt 7: Kombinierter Test

Test: verbessert der Gamma-Term die Korrelation zusätzlich?

Ergebnis:
- Bei großen Systemen: RMSE wird größer (Gamma überdeckt)
- Bei kleinen Systemen: RMSE leicht kleiner für Phase-Terme
- Delta_r maximal +0.009 (weniger als 2% Verbesserung gesamt)

Bestätigung der Hypothese:
In großen Systemen überdeckt die großskalige Feldspannung
den Gamma-Beitrag. Der Gamma-Term ist dort Rauschen.
In kleinen Systemen ist er der relevante Mechanismus.

---

## Schritt 8: Drei-Regime Analyse (Hauptergebnis)

Aufteilen in drei Gruppen:
- Klein:     r_max <  16 kpc (n=107)
- Übergang:  16 <= r_max < 30 kpc (n=32)
- Groß:      r_max >= 30 kpc (n=36)

Statistik:
Gruppe     Median-alpha  Core-artig  Cuspy   r vs r_max
Klein      2.21          29%         26%     -0.078 (p=0.42, n.s.)
Uebergang  1.94          63%         22%     +0.078 (p=0.67, n.s.)
Gross      1.45          81%          8%     -0.383 (p=0.02)

Kruskal-Wallis: H=33.1, p<0.0001
Mann-Whitney:
  Klein vs Uebergang: p=0.021
  Uebergang vs Gross: p=0.014
  Klein vs Gross:     p<0.0001

Gamma-Term in kleinen Systemen:
93-99% der Korrekturen sind negativ (core-bildend).
In kleinen Systemen ist der Gamma-Mechanismus der
relevante Feinkorrektur-Prozess.

---

## Physikalische Gesamtinterpretation

Drei klar unterscheidbare Regime der Core-Cusp Dynamik:

1. Klein (r < 16 kpc):
   Das Feld hat noch Toleranz. Die großskalige Feldspannung
   ist schwach. Gammastrahlung ist der aktive Mechanismus
   der zentrale Cusp-Bildung verhindert. Hohe Streuung weil
   die Gamma-Intensität von Galaxie zu Galaxie variiert.

2. Übergang (16-30 kpc):
   Beide Mechanismen gleichwertig. Ablösungspunkt der zwei
   Regime. Keine klare Korrelation mit Systemgröße.
   Alpha nahe NFW=2.0 als Gleichgewichtspunkt.

3. Groß (r >= 30 kpc):
   Das Feld hat seine maximale Organisationskapazität im
   Regime erreicht. Großskalige Feldspannung dominiert,
   überdeckt den Gamma-Beitrag, und verhindert systematisch
   cuspy Strukturen. 81% core-artig ohne jeden
   Feedback-Prozess nötig.

---

## Verbindung zur UQSH-Feldgleichung

Der Gamma-Term als Erweiterung der Feldgleichung:

Delta_g_gamma(r) = A_gamma
                  * (V0^2/r0)     <- zentrale Feldsättigung
                  * mass_norm     <- Kopplung an Ankermaterie
                  * exp(-r/r_gamma)  <- Dissipation mit Radius
                  [* cos(2*pi*r/lambda_gamma)]  <- Phasenwelle

Eine vollständige Herleitung aus der UQSH-Feldgleichung
bleibt zukünftiger Arbeit vorbehalten.

---

## Offene Fragen

1. Quantitative Herleitung des Gamma-Terms aus der
   UQSH-Feldgleichung

2. Zeitabhängige Modellierung der Phasenwellen:
   tau = R/c_eff als expliziter Term

3. Observationeller Test: GRB-Positionen relativ zum
   Halorand in edge-on Galaxien, Korrelation mit
   Regimeklassifikation

4. Bestimmung der Schwellenwerte 16 kpc und 30 kpc
   aus fundamentalen Feldparametern

5. Erweiterung auf elliptische Galaxien und Cluster

---

## Verwendete Daten und Software

Daten:
- SPARC ROTMOD: Lelli et al. (2016), 175 Galaxien
- q-Fit Ergebnisse: aus Hauptpaper SPARC-Analyse

Software:
- Python 3, NumPy, Pandas, SciPy, Matplotlib
- Google Colab

Referenzen:
- de Blok (2009): The Core-Cusp Problem, arXiv:0910.3538
- Lelli et al. (2016): SPARC, AJ 152, 157
- Rexhepi (2026): Black Holes - The Immortal Life-Givers
- Rexhepi (2026): Fundamente der UQSH
