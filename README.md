# Open Source Compliance & Tooling Documentation

**Project:** NASA Space Apps Challenge — NISAR 3D Disaster & Earth Observation Platform  
**Challenge Track:** Earth & Space Science / Satellite Observation  
**Date:** November 2026  
**License Compliance Status:** ✅ **100% Fully Open Source & Open Data Compliant**

---

## 1. Executive Summary & Statement of Compliance

This application was engineered specifically to adhere to the strict **Open Science**, **Open Source**, and **Open Data** mandates established by the **NASA International Space Apps Challenge** and **NASA's Open-Source Science Initiative (OSSI)**.

Every library, visualization framework, tile endpoint, satellite imagery layer, digital elevation model (DEM), and data schema utilized in this project is strictly **free, open-source software (FOSS)** or released under **permissive Open Access / Public Domain** licenses approved by the Open Source Initiative (OSI) or Creative Commons.

---

## 2. Complete Inventory of Visual & Geospatial Tools

The following table provides an exhaustive breakdown of all visual engines, UI libraries, and rendering frameworks utilized:

| Tool / Library | Version | License | Developer / Governance | Repository / Official URL | Role in the Project |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **MapLibre GL JS** | `v6.18.0` | **BSD 3-Clause License** | MapLibre Community & OpenJS Foundation | [maplibre.org](https://maplibre.org/) / [GitHub](https://github.com/maplibre/maplibre-gl-js) | Core interactive 3D Globe renderer, coordinate projection (`globe`), rotation, marker anchoring, and terrain visualization. |
| **Three.js** | `r170` | **MIT License** | Ricardo Cabello (Mr.doob) & Community | [threejs.org](https://threejs.org/) / [GitHub](https://github.com/mrdoob/three.js) | Real-time 3D rendering of the NISAR satellite mesh (12m radar reflector drum, bus, solar panels, and boom arm). |
| **HTML5 Canvas & WebGL** | Web Standard | **W3C / Khronos Group Standard** | Khronos Group & World Wide Web Consortium | [khronos.org/webgl](https://www.khronos.org/webgl/) | GPU-accelerated hardware rendering for the deep space procedural starfield and 3D scenes. |

---

## 3. Geospatial & Satellite Data Sources

All basemaps, satellite textures, and elevation datasets are open and publicly accessible:

| Dataset / Tile Service | Format | License | Provider / Source | Attribution / Citation Notice |
| :--- | :--- | :--- | :--- | :--- |
| **EOX Sentinel-2 Cloudless** | Raster WMTS Tiles (`.jpg`) | **CC BY 4.0** (Creative Commons Attribution 4.0) | EOX IT Services GmbH & European Space Agency (ESA) | `Sentinel-2 cloudless - https://s2maps.eu by EOX IT Services GmbH (Contains modified Copernicus Sentinel data 2020)` |
| **OpenFreeMap** | Vector Tiles (`.pbf`) | **ODbL / BSD** | OpenFreeMap Community | Built upon open-source tile hosting without proprietary API keys. |
| **OpenStreetMap** | Vector Map Data | **ODbL 1.0** (Open Database License) | OpenStreetMap Foundation (OSMF) | `© OpenStreetMap contributors` (https://www.openstreetmap.org/copyright) |
| **Mapterhorn DEM** | Raster-DEM (`Terrarium`) | **Public Domain / CC0 / ODbL** | Mapterhorn (derived from Copernicus GLO-30 & USGS 3DEP) | Global open-access elevation terrain model used for 3D Earth relief. |

---

## 4. Scientific Mission & Reference Data

| Resource | Scope / Origin | Legal Status | Reference |
| :--- | :--- | :--- | :--- |
| **NISAR Satellite Mission** | NASA Jet Propulsion Laboratory (JPL) & ISRO | **Public Domain (US Gov Work) / Open Data Policy** | NASA and ISRO guarantee free and open distribution of all NISAR L-band and S-band synthetic aperture radar (SAR) products. |
| **Global Disaster & Hazard Data** | Curated scenarios (Tsunami, Wildfires, Earthquakes, El Niño, Storms, Floods) | **Public Domain / CC0** | Structured according to international civil protection and disaster response classifications (D01–D06). |

---

## 5. Detailed License Excerpts & Attributions

### 5.1 BSD 3-Clause License (MapLibre GL JS)
```text
Copyright (c) 2020, MapLibre contributors
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.
3. Neither the name of the copyright holder nor the names of its contributors
   may be used to endorse or promote products derived from this software
   without specific prior written permission.
```

### 5.2 MIT License (Three.js)
```text
The MIT License

Copyright © 2010-2026 three.js authors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.
```

### 5.3 Creative Commons Attribution 4.0 International (CC BY 4.0)
Applicable to **EOX Sentinel-2 Cloudless global imagery**:
- **You are free to:** Share (copy and redistribute the material) and Adapt (remix, transform, and build upon the material) for any purpose, even commercially.
- **Under the terms of:** Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made.

### 5.4 Open Database License (ODbL 1.0)
Applicable to **OpenStreetMap** geographic features:
- Any user has the freedom to copy, distribute, transmit, and adapt OpenStreetMap data under the terms of ODbL 1.0, provided attribution is maintained and any modified database is distributed under the same license.

---

## 6. Where and How to Store This Documentation

To ensure complete compliance with competition evaluation criteria:

1. **Repository Root (`/OPEN_SOURCE_COMPLIANCE.md`):**  
   Keep this file at the root level of your Git repository (`GitHub`, `GitLab`, or `Bitbucket`). This is the universal standard for open-source submissions.
2. **Link in the main `README.md`:**  
   Add a direct link in your main project README:
   ```markdown
   ## 📜 Open Source & Licensing
   This project is 100% open source. All libraries, satellite data layers, and 3D visual tools comply with NASA Space Apps Challenge rules. 
   See our detailed [Open Source Compliance Documentation](OPEN_SOURCE_COMPLIANCE.md).
   ```
3. **NASA Space Apps Project Submission Portal:**  
   When submitting your project on the official NASA Space Apps portal:
   - There is a required field: *"What open-source software, data, or APIs did your team use?"*
   - Copy the summary table from **Section 2 and Section 3** of this document directly into that field, or paste the link to your `OPEN_SOURCE_COMPLIANCE.md` on your public repository.
4. **Recommended File Format:**  
   Standard **Markdown (`.md`)**. Markdown is universally rendered by web hosting platforms, code repositories, and documentation viewers without requiring external proprietary software.

---

## 7. Verification Checklist for Space Apps Judges

- [x] No proprietary map tokens (e.g., Mapbox token, Google Maps paid API key) are required.
- [x] All rendering scripts load from public open-source CDNs (`unpkg.com`, `jsdelivr.net`).
- [x] Earth textures are based on European Space Agency (ESA) Copernicus Sentinel-2 open data.
- [x] Real-time 3D engine is powered by Three.js (MIT open source).
- [x] Full source code is open, inspectable, and reproducible locally without closed binaries.

