---
title: Satellite-Based Conservation Agriculture Monitoring Using Sentinel-1 SAR and Sentinel-2 in Pavia Rice Fields
date: 2025-02-16
weight: 1
share: false
show_related: false
external_link: "/projects/conservag-pavia-rice/"
build:
  render: never
  list: always
links:
  - name: View on GitHub
    url: 'https://github.com/prashanthreddy47/conservag-pavia-rice'
tags:
  - Remote Sensing
  - SAR
  - Sentinel-1
  - Sentinel-2
  - Conservation Agriculture
  - Machine Learning
  - Random Forest
  - SHAP Explainability
  - Google Earth Engine
  - Carbon Estimation
  - Agriculture
---

A proof-of-concept study classifying post-harvest conservation agriculture practices in 75 rice fields (382 ha) across Pavia Province, Italy, using Sentinel-1 SAR and Sentinel-2 optical time series. The SAR-only Random Forest model achieved **F1 = 0.85** (weighted), outperforming optical-only (F1 = 0.70) — demonstrating that SAR backscatter captures crop residue detection, winter flooding, and cover crop signals more reliably than optical indices, especially during cloud-prone winter months when December 2020 had zero usable Sentinel-2 scenes due to Po Valley fog.

---

### Key Findings

| Configuration | F1 (weighted) | Accuracy |
|---------------|---------------|----------|
| **SAR-only RF** | **0.85** | 0.87 |
| Fusion RF | 0.84 | 0.85 |
| Optical-only RF | 0.70 | 0.71 |

---

### Methodology

1. **Field Selection** — DUSAF 2021 + SIARL 2020 cross-validation, area stratification, 500 m grid spacing → 75 fields
2. **Feature Engineering** — 151 features from 5 temporal windows (harvest through recovery) extracted via Google Earth Engine
3. **Pseudo-Labeling** — Unsupervised clustering (K-Means, GMM, DBSCAN) with physical signature interpretation → 4 management classes
4. **Classification** — Random Forest, XGBoost, SVM across SAR-only, Optical-only, and Fusion feature sets
5. **Spatial Block CV** — 4 geographic quadrants to prevent spatial autocorrelation leakage
6. **SHAP Explainability** — VH/VV polarization ratio confirmed as top feature; each management class detected through distinct SAR scattering mechanisms

---

### Classification Results

| Management Practice | Fields | Area (ha) | Detection Mechanism |
|-------------------|--------|-----------|-------------------|
| Residue Retention | 35 | 169 | High NDTI, elevated VH/VV ratio |
| Winter Flooding | 23 | 132 | Low VH backscatter, specular reflection |
| Conventional Tillage | 15 | 71 | Bare soil BSI signal |
| Cover Crop | 2 | 10 | Strong winter NDVI recovery |

---

### Carbon Impact (IPCC Tier 1 Estimates)

Conservation practices across the study area correspond to an estimated **333 tCO₂eq/yr** reduction and **42 tC/yr** soil organic carbon gain — based on published IPCC literature values, not field measurements.

---

### Limitations

This is a proof-of-concept with important caveats: pseudo-labels from unsupervised clustering carry circular validation risk, the sample is small (75 fields, single season), cover crop is severely underrepresented (n=2), and carbon estimates use literature factors rather than site-specific measurements.

---

### Tools

Google Earth Engine · Python · scikit-learn · XGBoost · SHAP · Sentinel-1 SAR · Sentinel-2 MSI · Spatial Block Cross-Validation · IPCC Carbon Accounting
