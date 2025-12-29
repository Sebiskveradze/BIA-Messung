# BIA-Messung & Trainingsanalyse

Dieses Projekt dient der Analyse und Visualisierung von Daten aus der Bioelektrischen Impedanzanalyse (BIA) sowie sportlichen Aktivitäten aus Strava. Es berechnet Körperzusammensetzungswerte und stellt diese grafisch dar, um Veränderungen über einen Trainingszeitraum (z. B. 4 Wochen Lauftraining) zu verdeutlichen.

## Projektstruktur

* **`Script/BIA_Messung.R`**: Das zentrale R-Skript für die Datenverarbeitung, Berechnung von Kennzahlen und Erstellung der Plots.
* **`Data/activities.csv`**: Enthält die Rohdaten der sportlichen Aktivitäten (ID, Datum, Typ, Distanz etc.).
* **`Plots/`**: Verzeichnis, in dem die generierten Visualisierungen gespeichert werden:
    * `Plot_BIA.png`: Stapeldiagramm der Körperzusammensetzung (FFM, ASMM, FM).
    * `Plot_BMI.png`: Vergleich des Body-Mass-Index zwischen Baseline und Follow-up.
    * `Plot_Runs.png`: Wöchentliche Zusammenfassung der Laufdistanzen und Anzahl der Einheiten.
* **`renv/` & `renv.lock`**: Dateien zur Verwaltung der Paketabhängigkeiten und Sicherstellung der Reproduzierbarkeit.

## Funktionen des Skripts

### 1. Berechnung der Körperzusammensetzung
Das Skript nutzt spezifische Formeln zur Ermittlung folgender Werte aus den BIA-Rohdaten (Widerstand $R_z$ und Reaktanz $X_c$):
* **FFM (Fettfreie Masse)**
* **ASMM (Appendikuläre Skelettmuskelmasse)**
* **FM (Fettmasse)**
* **BMI (Body Mass Index)**

### 2. Strava-Aktivitätsanalyse
Das Skript filtert automatisch nach Lauftrainings innerhalb eines definierten Zeitraums (Februar bis März 2025), gruppiert diese in Trainingswochen und berechnet die Gesamtdistanz sowie die Anzahl der Läufe.

*Letzte Aktualisierung: 26.02.2025*
