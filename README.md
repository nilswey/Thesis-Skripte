# Thesis-Skripte
Automatierungs Skripte für die Methodik zur Bachelor Arbeit: Die Erstellung von Bevölkerungsrastern auf Basis von automatischer Klassifizierung von Gebäudegrundrissen 

Ziel der Arbeit: Gesamtanzahl und Verteilung der Bevölkerung von 4 Landkreisen bestimmen

Python, Packages: Geopandas, Pandas, Seaborn

Zusammenfassung der Methodik:
1. Anreicherung von ALKIS gebäudgrundrissen mit weiteren Merkmalen für RF
2. Automatische Klassifizierung von ALKIS Gebäudegrundrissen mittels Random Forest Algorithmus
3. Berechnung von Bevölkerungskoeffizienten, welcher Bevölkerung jeder Klasse pro Kubikmeter Wohfläche angibt, Datengrundlage sind homogen klassifizierte Zellen des Zensusbevölkerungsraster
4. Zuordnung der Koeffizienten zu den klassifizierten Häusern, Interpolation von Bewohnern des Gebäudes
5. Aggregation in 100m Raster, vergleich mit Zensus Daten zur Validierung
6. Statistische Auswertung mittels RMSE und MAPE, anschließende Visualisierung

Skripte: 
Hausklassifikation statistische Merkmale: Berechnung 15 statistischer und geometrischer Merkmale anhand derer der RF in 7 semantische Häuserklassen einteilt

(Klassifizierung erfolgte nicht in Python)

Bevölkerungsschätzung: Koeffizienten Berechnung aus Zensus-Daten für jede Hausklasse, anschließend werden die Koeeffizienten den klassifizierten Häusern zugewiesen, Interpolation der Hausbevölkerung, Aggregierung in 100m Raster

Statistiken und Visualisierung: Abweichung von Referenzdaten berechnen, RMSE, MAPE und weitere Maße zur Evaluierung der Ergebnisse, Visualisierungen via Seaborn
