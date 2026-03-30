# Spatial Econometrics of Unemployment in Poland

## 📌 Overview

This project analyzes determinants of unemployment at the county level (powiaty) in Poland, combining classical econometric modeling with spatial econometric analysis.

The study is divided into two main parts:

* **unemployment_model_ols** – construction and validation of a linear regression model
* **spatial_autocorrelation_analysis** – analysis of spatial autocorrelation in model residuals

---

## 📊 Data

* Source: Bank Danych Lokalnych (GUS)
* Spatial data: powiat boundaries (GIS)
* Year: 2023

---

## 🧠 Methodology

### 1. Classical Econometric Model

* Linear regression model
* Variable selection based on economic reasoning
* Missing data imputation (KNN)
* Outlier treatment (IQR method)
* Multicollinearity analysis (VIF)

### 2. Model Diagnostics

* Normality tests (Shapiro-Wilk, Jarque-Bera, Anderson-Darling)
* Heteroskedasticity (Breusch-Pagan test)
* Spatial autocorrelation (Moran's I)

### 3. Spatial Econometrics

Spatial dependence in residuals was analyzed using different spatial weight matrices:

* Contiguity (Queen)
* k-nearest neighbors (k=7)
* Distance threshold (50 km)
* Inverse distance
* Squared inverse distance

---

## 📈 Key Results

* The model explains approx. **34% of unemployment variation (R² ≈ 0.34)**
* All variables are statistically significant
* Significant **spatial autocorrelation** detected in residuals
* Strongest spatial dependence observed for contiguity matrix
* Log transformation improved model properties:

  * removed heteroskedasticity
  * removed spatial autocorrelation

---

## 📄 Reports

* unemployment_model_ols: `paper/unemployment_model_ols.pdf`
* spatial_autocorrelation_analysis: `paper/spatial_autocorrelation_analysis.pdf`

---

## 👥 Informations

Developed as part of a group project at AGH University of Science and Technology.
