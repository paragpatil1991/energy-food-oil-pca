# Dynamic Coupling Between Energy, Fertilizer, and Food Markets Using Rolling PCA

## Overview

This project studies the dynamic coupling between energy, fertilizer, and food markets using Principal Component Analysis (PCA) and Rolling PCA. The goal is to understand how shocks in energy markets propagate to fertilizer and food markets and how these relationships evolve over time.

This analysis focuses on identifying system-wide coupling, time-varying relationships, and transmission mechanisms between energy and agricultural markets.

---

## Data

Monthly time-series data used in this study:

- Brent Crude Oil Price  
- Global Natural Gas Spot Price (FRED)  
- Fertilizer Cost Index (Nitrogen Fertilizer PPI)  
- Food Price Index  

### Data Processing

- Converted all data to monthly frequency  
- Aligned time periods across datasets  
- Computed first differences (returns)  
- Standardized variables before PCA  
- Removed missing values  

Returns were used instead of raw levels to avoid spurious correlations due to trends and to focus on dynamic co-movements.

---

## Methodology

### 1. Static PCA

Principal Component Analysis was first applied to the full dataset to identify overall system coupling.

Findings:
- First principal component (PC1) explained approximately 83% of total variance
- Strong coupling observed between oil, gas, fertilizer, and food markets

This indicates that the four markets behave as an integrated system.

---

### 2. Rolling PCA

Rolling PCA was performed to examine time-varying coupling.

Rolling windows used:
- 30 months  
- 60 months  
- 84 months  

Findings:
- Coupling varies over time
- Strong coupling observed around:
  - 2008 Financial Crisis
  - 2014 Oil Price Shock
  - 2022 Energy Crisis

This suggests that global shocks increase system-wide coupling.

---

### 3. Rolling PCA Loadings

Rolling PCA loadings were computed to analyze variable contributions over time:

Variables analyzed:
- Oil
- Gas
- Fertilizer
- Food

Findings:
- Gas contributed more strongly in early 2000s
- Oil contribution increased during commodity boom
- Fertilizer contribution increased around 2022
- Food contribution increased post-2022

This indicates structural evolution in system dynamics.

---

### 4. Lag Analysis

Lag relationships were analyzed using cross-correlation.

Results:
- Oil → Fertilizer ≈ 3-month lag
- Oil → Food ≈ 1-month lag
- Fertilizer → Food weak / near simultaneous

Interpretation:
- Energy shocks propagate quickly to food markets
- Fertilizer acts as a secondary transmission channel

---

### 5. Rolling Correlation Analysis

Rolling correlations were computed for:

- Oil vs Food  
- Gas vs Fertilizer  
- Fertilizer vs Food  

Findings:
- Weak coupling before 2008
- Strong coupling during 2008 crisis
- Moderate coupling post-2014
- Strong coupling again around 2022

This confirms time-varying market integration.

---

### 6. Rolling PC1 Variance Explained

Rolling PC1 variance was computed to measure system-wide coupling strength.

Findings:
- PC1 variance ranged between approximately 0.55 and 0.92
- Strong coupling observed during crisis periods
- Temporary decoupling observed during transitional periods

This provides a system-wide coupling index.

---

## Key Findings

- Strong coupling exists between energy, fertilizer, and food markets
- PC1 explains approximately 83% of total variance
- Coupling varies over time
- Crisis-driven coupling observed
- Energy shocks propagate to food markets
- Structural evolution observed in system dynamics

---

## Repository Structure

energy-fertilizer-food-pca/
│
├── notebooks/
│   ├── data_preparation.ipynb
│   ├── static_pca.ipynb
│   ├── rolling_pca.ipynb
│   ├── lag_analysis.ipynb
│   ├── rolling_correlation.ipynb
│
├── data/
├── figures/
├── README.md
├── requirements.txt

---

## Requirements

Install dependencies:

pip install -r requirements.txt

Required packages:

- pandas
- numpy
- matplotlib
- scikit-learn
- seaborn
- scipy
- jupyter

---

## Motivation

Understanding the energy–fertilizer–food nexus is important for:

- Food price inflation analysis
- Agricultural policy
- Energy market shocks
- Supply chain risk analysis

This study provides a dynamic and data-driven analysis of these relationships.

---

## Future Work

Possible extensions:

- Granger causality analysis
- Additional commodity inclusion
- Forecasting models
- Regime-switching models
- Multi-country analysis

---

## Author

Parag Patil

Research Project: Dynamic Coupling Between Energy, Fertilizer, and Food Markets