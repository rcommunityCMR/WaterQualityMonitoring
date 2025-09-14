# 💧 WaterQuality-SatR — Guide Contributeurs

## 🎯 Objectif
Ce projet vise à **apprécier la qualité de l’eau** à partir d’images satellitaires (Sentinel, Landsat) en R.  
Les contributeurs doivent suivre une structure simple : importer les données, préparer la donnée géographique, et produire un rapport automatique en R Markdown.

---

## 📂 Organisation du dépôt

---
```
WaterQuality-SatR/
├─ R/ # Scripts principaux
│ ├─ import_data.R # Import AOI + rasters
│ ├─ preprocess.R # Recadrage, harmonisation CRS
│ ├─ indices.R # Calcul NDWI/MNDWI
│ └─ render_report.R # Génération rapport Rmd
│
├─ data-raw/ # Données brutes
│ ├─ aois/region.geojson # Zone d’étude
│ └─ sat/stack.tif # Rasters satellites
│
├─ outputs/ # Résultats
│ ├─ maps/ # Cartes
│ ├─ tables/ # Indicateurs
│ └─ report/ # Rapports Rmd rendus
│
└─ rmarkdown/
└─ report_water_quality.Rmd # Template du rapport
```

---

## 🗂️ Tâches des contributeurs

1. **Importer les données**
   - Placer l’AOI (`region.geojson`) dans `data-raw/aois/`
   - Placer les images satellites (`stack.tif`) dans `data-raw/sat/`

2. **Préparer la donnée géographique**
   - Vérifier projection/CRS
   - Recadrer le raster sur l’AOI
   - Sauvegarder les fichiers propres dans `data/`

3. **Calculer les indices**
   - NDWI / MNDWI (qualité/préservation de l’eau)
   - Sauvegarder résultats dans `outputs/maps/`

4. **Générer le rapport**
   - Utiliser `rmarkdown/report_water_quality.Rmd`
   - Inclure : contexte, méthodologie, cartes, statistiques simples
   - Rapport final rendu dans `outputs/report/`

---

## ✅ Definition of Done

- AOI + raster bien importés et alignés  
- Indices (NDWI/MNDWI) générés sans erreur  
- Rapport Rmd rendu en HTML ou PDF dans `outputs/report/`  
- Contexte et sources documentés  

---

## 📜 Licence

MIT — libre et ouvert.  
Les données doivent être utilisées en respectant les licences Copernicus/USGS.  
