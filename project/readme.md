# Spatio-Temporal Drought Assessment & Trend Analysis 🌍💧

An automated data engineering and statistical modeling pipeline to assess 45 years (1981–2025) of meteorological and hydrological drought patterns across 23 districts of integrated Andhra Pradesh.

## 📌 Project Overview
Understanding shifting precipitation patterns is critical for water resource management and infrastructure planning. This project utilizes high-resolution satellite precipitation data to compute drought severity indices, track long-term climatic shifts, and generate automated geospatial heatmaps.

## 🛠️ Tech Stack & Libraries
* **Data Extraction:** Google Earth Engine (GEE), JavaScript
* **Data Engineering & Analysis:** Python, Pandas, NumPy
* **Statistical Modeling:** SciPy (Gamma Distributions), PyMannKendall
* **Geospatial Visualization:** GeoPandas, Matplotlib

## 📊 Methodology
1. **Data Acquisition:** Clipped 45 years of CHIRPS v2.0 satellite precipitation data (0.05° resolution) to the 2011 India District shapefile using Google Earth Engine.
2. **Index Computation:** Modeled raw rainfall data against a Gamma distribution to calculate multi-scalar Standardized Precipitation Indices (SPI-1, SPI-3, SPI-12).
3. **Trend Analysis:** Applied the non-parametric **Mann-Kendall** test for statistical significance (Z-scores) and **Sen’s Slope** estimator for trend magnitude.
4. **Spatial Mapping:** Programmatically mapped statistical outputs back to the geographic shapefile to generate localized drought heatmaps.

## 🚀 Key Results
* Engineered an automated pipeline capable of processing 540 months of continuous spatial data without manual intervention.
* Successfully mapped statistically significant drying trends, isolating highly vulnerable geographic clusters to aid in actionable risk assessment.

## 📂 Repository Structure
* `/scripts`: Python pipelines and Colab notebooks for SPI and Trend computation.
* `/data`: Sample time-series datasets.
* `/maps_and_plots`: Generated geospatial heatmaps and multi-scalar time-series charts.