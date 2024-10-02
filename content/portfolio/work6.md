+++
date = "2024-02-15T19:41:01+05:30"
title = "Paddy Field Mapping using NDVI Thresholding and Machine Learning"
draft = false
image = "img/portfolio/paddy-mapping.png"
showonlyimage = false
weight = 1
+++

#### Links:
- [Live Application](https://prashanthreddyputta.users.earthengine.app/view/paddy-field-mapping-with-ndvi-rf-svm)

In this project, I developed a comprehensive methodology for accurate and efficient mapping of paddy fields in the Nalgonda District, India, using multi-temporal Sentinel-2 imagery. The study employed three different approaches: NDVI thresholding, Random Forest classification, and Support Vector Machine (SVM) classification. The research focused on the Rabi season from December 2019 to May 2020, analyzing the unique phenological patterns of paddy growth to improve classification accuracy.

#### Methodology Overview:

![Methodology Flowchart](/img/portfolio/paddy-mapping-methodology.png)
---
---
#### Key Components:

1. **Data Acquisition and Preprocessing**
   - Utilized Google Earth Engine for cloud-free Sentinel-2 imagery acquisition
   - Implemented atmospheric corrections and cloud masking (<20% cloud cover)
   - Created 10-day composites for consistent temporal coverage (18 images total)

2. **NDVI Threshold Approach**
   - Established optimal threshold (0.65) for paddy field identification
   - Analyzed phenological stages:
     - Plantation start: December
     - Peak growth: March
     - Harvest: June/July
   - Generated binary mask for paddy pixels

3. **Machine Learning Classifications**
   - Random Forest (RF) and Support Vector Machine (SVM) classifiers
   - Training data: 700 paddy points, 300 non-paddy points
   - Features: multi-temporal NDVI values and spectral bands

---

4. **Time Series Analysis**
![Time Series Analysis Workflow](/img/portfolio/paddy-time-series-analysis.png)
---

5. **Accuracy Assessment**
   - Confusion matrices for RF and SVM classifications
   - Comparison with ground truth data
   - McNemar's test for statistical comparison of methods

#### Technologies Used:
- Google Earth Engine (JavaScript API)
- Python for data analysis and machine learning
- Remote sensing techniques (NDVI, spectral indices)
- Machine learning algorithms (Random Forest, SVM)

#### Results and Visualizations:
![Paddy Mapping Results](/img/portfolio/paddy-mapping.png)

- NDVI Threshold Method: Efficiently captured paddy growth cycle
- Random Forest: 97% accuracy
- SVM: 90% accuracy
- Interactive Earth Engine App for result visualization
- Time series charts of NDVI values
- Area statistics for different land cover classes

#### Impact and Applications:
This study demonstrates that the NDVI threshold method can be as effective as complex machine learning approaches while being more time and resource-efficient. The methodology developed can be adapted for mapping other crops with distinct phenological patterns, potentially revolutionizing large-scale crop monitoring practices.

The project contributes to:
- Improved agricultural monitoring systems
- Enhanced decision-making in crop management
- Food security assessments
- Agricultural policy-making support

By providing a cost-effective and accurate method for paddy field mapping, this approach is particularly valuable in regions with limited resources for extensive ground surveys.