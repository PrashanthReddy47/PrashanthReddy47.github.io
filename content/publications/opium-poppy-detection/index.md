---
title: "Phenology-Informed Identification of Opium Poppy Cultivation: Explainable Feature Extraction from Multispectral Time Series Data"
authors:
  - me
  - fabio-dellacqua
  - shafi-miakhil
date: "2026-01-15"
share: false
show_related: false
doi: ""

publication_types: ["article-journal"]

publication: "*Remote Sensing Applications: Society and Environment* (under review)"
publication_short: "RSASE (under review)"

abstract: "Opium poppy cultivation monitoring in fragile and hard-to-access regions faces major operational challenges, as field surveys are difficult due to remoteness, access limitations, and the sensitive nature of illicit crop cultivation. Machine learning classification of freely available multispectral data offers potential for scalable surveillance, but published accuracy assessments suffer from spatial autocorrelation bias when validation uses nearby pixels rather than independent fields. This study addresses these methodological gaps through phenology-informed classification with rigorous spatial validation and model interpretability analysis, applied to Nangarhar Province, Afghanistan. Random Forest and XGBoost models achieved 98.7% and 98.1% F1-scores respectively, with zero false positives among 43 non-poppy fields. SHAP analysis revealed January features dominated discrimination, contradicting conventional flowering-focused approaches."

summary: "Machine learning classification achieving 98.7% F1-score for opium poppy detection with rigorous spatial cross-validation and explainable AI analysis."

tags:
  - Remote Sensing
  - Machine Learning
  - Crop Classification
  - Explainable AI

featured: false

links:
  - name: "Under Review"
    url: ""

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''
---

## Key Achievements

- **98.7% F1-score** using Random Forest (100% precision, 97.4% recall)
- **98.1% F1-score** using XGBoost (100% precision, 96.3% recall)
- **Zero false positives** among 43 non-poppy fields
- **Leave-One-Field-Out cross-validation** preventing spatial autocorrelation bias
- **Temporal validation** on 2020 imagery maintained 97.5% F1-score

## Methodology Innovation

- Multi-temporal Sentinel-2 imagery across 6 phenological dates (January-June 2021)
- 90 features from 9 spectral bands and 6 vegetation indices
- SHAP interpretability analysis revealing January as most discriminative stage
- Rigorous three-axis validation: spatial LOFO, temporal testing, interpretability

## Research Significance

This work advances remote sensing methodology through rigorous spatial validation that prevents common accuracy inflation from spatial autocorrelation. The explainable AI approach provides insights into phenological discrimination patterns that can inform operational monitoring systems.

**Status:** Manuscript under editorial review at *Remote Sensing Applications: Society and Environment*
