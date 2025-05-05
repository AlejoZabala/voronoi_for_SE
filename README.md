# Voronoi-Based Substation Zoning for Urban Electricity Planning

This repository demonstrates how **Voronoi polygons** can be used to spatially aggregate and analyze electricity demand in urban areas—particularly useful in cases where **no information about the existing electricity distribution network is available**.

### 🗺 Data & Context

The case study focuses on Bremen, Germany, using spatial data obtained from [FlexiGIS](https://github.com/FlexiGIS/FlexiGIS). Buildings were classified using NACE codes, and residential units were identified separately.

### ⚡ Load Assignment

Each building is assigned a synthetic maximum load (in kVA) using a truncated normal distribution, depending on its type.

### 🔍 Voronoi Segmentation

- Voronoi polygons are generated from clustered building centroids, spaced ~2000m apart.
- Each polygon represents a candidate **substation service area**.
- Loads within each polygon are aggregated to calculate the total maximum demand.

### 📊 Outputs

- Voronoi zones visualized and color-coded by aggregated load.
- Buildings are shaded with lighter tones.
- Summary statistics and per-zone demand profiles displayed interactively.

![image](https://github.com/user-attachments/assets/ad0b2897-ef4a-4ef8-98cd-f0e1ebcad7e2)
