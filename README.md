#  Molecular Properties for Drug Discovery — Solubility Prediction Project

## Overview

This project applies **machine learning techniques** to predict **aqueous solubility (logS)** of drug-like molecules using the **Delaney (ESOL)** dataset.  
The study demonstrates how **molecular descriptors** can be used to estimate a key pharmacokinetic property — solubility — which plays a critical role in **drug absorption, distribution, and bioavailability**.

The notebook — `Molecular_Properties_for_Drug_Discovery.ipynb` — walks through the full data science workflow:
1. Data loading and preprocessing  
2. Exploratory data analysis (EDA) and visualization  
3. Feature selection and correlation analysis  
4. Model training and evaluation  
5. Insights and interpretation of results  

---

## Dataset Description

**Dataset name:** Delaney ESOL Dataset (preprocessed version)  
**Source:** John S. Delaney, *Journal of Chemical Information and Computer Sciences* (2004).  
**Target variable:** `measured logS` — aqueous solubility in mol/L.  

###  Key Molecular Features
| Descriptor | Meaning |
|-------------|----------|
| Molecular Weight | Total mass of the molecule |
| Number of Hydrogen Bond Donors | Count of hydrogen atoms that can participate in hydrogen bonding |
| Number of Rotatable Bonds | Flexibility measure of a molecule |
| Number of Rings | Structural cyclic features |
| Polar Surface Area | Surface area contributed by polar atoms |
| ESOL Predicted logS | Empirical solubility estimate from structure |

---

## Methodology

### Tools and Libraries
- **Data Processing:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn`
- **Environment:** Google Colab / Jupyter Notebook

###  Models Applied
| Model | Type | Purpose |
|--------|------|----------|
| Linear Regression | Baseline | Understand linear relation between descriptors and solubility |
| Random Forest Regressor | Ensemble | Capture non-linear molecular relationships |

### Evaluation Metrics
- **RMSE (Root Mean Squared Error)** — Measures prediction error magnitude  
- **R² Score (Coefficient of Determination)** — Measures goodness of fit  

---

## Results Summary

| Model | RMSE | R² |
|--------|------|----|
| Linear Regression | ~0.90 | ~0.75 |
| Random Forest | ~0.60 | ~0.88 |

>  **Interpretation:**  
> Random Forest performed significantly better, capturing complex molecular interactions that affect solubility.  
>  
> Key influential features include:  
> - Molecular Weight  
> - Polar Surface Area  
> - Hydrogen Bond Donors  

---

##  Visualization Highlights

The notebook includes:
- **Heatmap** of descriptor correlations  
- **Actual vs Predicted Solubility plot**  
- **Feature importance ranking** for Random Forest  
- **Distribution plots** of molecular weight and solubility  

---

##  Key Takeaways

- Physicochemical descriptors can effectively model solubility trends.  
- Random Forests offer strong generalization and interpretability in QSAR models.  
- The workflow can easily extend to predict other ADMET properties.

---

## Future Work

- Integrate **molecular fingerprints** (e.g., ECFP, Morgan)  
- Compare with **advanced models** (XGBoost, LightGBM, or deep learning)  
- Include **3D descriptors** and **quantum-chemical features** for better accuracy  
- Deploy the model via a **web app** (e.g., Streamlit or Flask)

---

##  Repository Structure

