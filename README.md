# Thesis-Skripte
Automatierungs Skripte für die Methodik zur Bachelor Arbeit: Die Erstellung von Bevölkerungsrastern auf Basis von automatischer Klassifizierung von Gebäudegrundrissen 

Ziel der Arbeit: Gesamtbevölkerung und Verteilung im UG zu bestimmmen
Python, Packages: Geopandas, Pandas, Seaborn

Zusammenfassung der Methodik:
1. Automatische Klassifizierung von ALKIS Gebäudegrundrissen mittels Random Forest Algorithmus
2. Berechnung von Bevölkerungskoeffizienten, aus Zensus-Bevölkerungsraster für jede Hausklasse in 4 Landkreisen
3. Zuordnung der Koeffizienten zu den klassifizierten Häusern, Interpolation von Bewohnern des Gebäudes
4. aggregieren in 100m Raster, vergleich mit Zensus Daten zur Validierung
5. Statistische Auswertung mittels RMSE und MAPE, anschließende Visualisierung

Skripte: 
Hausklassifikation statistische Merkmale: Berechnung 15 statistischer und geometrischer Merkmale anhand derer der RF in 7 semantische Häuserklassen einteilt

(Klassifizierung erfolgte nicht in Python)

Bevölkerungsschätzung: Koeffizienten Berechnung aus Zensus-Daten für jede Hausklasse, nutzt homogen klassifizierte Zellen, mit bekannter Bevölkerung, um Bevölkerung pro Kubikmeter zu berechnen, 
                       anschließend werden die Koeeffizienten den klassifizierten Häusern zugewiesen, Interpolation der Hausbevölkerung, Aggregierung in 100m Raster

Statistiken und Visualisierung: Abweichung von Referenzdaten berechnen, RMSE und MAPE berechnen auf verschiedenen Ebenen, Visualisierungen via Seaborn
