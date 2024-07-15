# Thesis-Skripte
Automatierungs Skripte für die Methodik zur Bachelor Arbeit: Die Erstellung von Bevölkerungsrastern auf Basis von automatischer Klassifizierung von Gebäudegrundrissen 

Ziel der Arbeit: Gesamtzahl und Verteilung der Bevölkerung für vier Landkreise zu bestimmmen

Python Packages: Geopandas, Pandas, Seaborn

Zusammenfassung der Methodik:
1. Anreicherung von ALKIS Gebäudegrundrissen mit Merkmalen für Klassifizierung
2. Automatische Klassifizierung von ALKIS Gebäudegrundrissen mittels Random Forest Algorithmus
3. Berechnung von Bevölkerungskoeffizienten welcher die zu erwartende Bevölkerung pro Kubikmeter für jede Häuserklasse enthält, Datengrundlage bilden die Bevölkerungszahlen von homogen klassifizierten Rasterzellen des Zensus 2022
4. Zuordnung der Koeffizienten zu den klassifizierten Häusern, Interpolation von Bewohnern des Gebäudes
5. Aggregation in 100m Raster, vergleich mit Zensus Daten zur Validierung
6. Statistische Auswertung mittels RMSE und MAPE, anschließende Visualisierung

Skripte: 
Hausklassifikation statistische Merkmale: Berechnung 15 statistischer und geometrischer Merkmale anhand derer der RF in 7 semantische Häuserklassen einteilt

(Klassifizierung erfolgte nicht in Python)

Bevölkerungsschätzung: Koeffizienten Berechnung aus Zensus-Daten für jede Hausklasse, nutzt homogen klassifizierte Zellen, mit bekannter Bevölkerung, um Bevölkerung pro Kubikmeter Koeffizient für jede Hausklasse zu berechnen, anhand dessen soll die Bevölkerung eines Hauses geschätzt werden
                       anschließend werden die Koeeffizienten den klassifizierten Häusern zugewiesen und deren Bevölkerung geschätzt

Statistiken und Visualisierung: Abweichung von Referenzdaten berechnen, RMSE, MAPE und weitere Maße für die Validation der Ergebnisse, Visualisierungen via Seaborn
