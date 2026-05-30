# WGA_regel v.3 – Gründach-Analyse Wilhelmsburg

## Rohdaten (Google Drive)
Große Geodateien (>100 MB) liegen auf Google Drive:
https://drive.google.com/drive/folders/1tIGcuM_AwGdYkVez77xnPdh3Ytc9GqvP

Enthält:
- dachflaechen_WHB.geojson (180 MB) – alle Dachflächen Wilhelmsburg
- dachflaechen_WHB_gefiltert.geojson – gefiltert: slope <30°, area >10m²
- dachflaechen_WHB_solar.geojson – Solar-Potenzial-Daten
- dachflaechen_WHB_NDVI.geojson – NDVI-Begrünungsscore
- truedop_WHB.tif – TrueDOP 2024 (RGBI, 10cm)

## Pipeline
1. Clip auf Wilhelmsburg-Umring (gdalwarp)
2. Filter: slope <30°, area >10m²
3. Centroid-Join Solar-Daten (Schatten, Ausrichtung)
4. NDVI-Begrünungsscore aus TrueDOP

## Repo-Inhalt
- WHB_Umring_WGS84.geojson – Gebietsgrenze
- potentialflaechen_solar.geojson – Potenzialflächen mit Eignungsklassen
- v.3.qgz – QGIS-Projektdatei
