# Psychiatric Disorder Classification using GWAS-Derived Genetic Variants

## Published Research
**IEEE Conference — IIT Guwahati (Accepted, 2026)**

## Overview
A machine learning pipeline to classify three psychiatric disorders — 
Schizophrenia, Bipolar Disorder, and Depression — using SNP–gene 
association data derived from Genome-Wide Association Studies (GWAS).

## Objective
To identify genetic variants (SNPs) most predictive of psychiatric 
disorders and build interpretable ML models that bridge bioinformatics 
and machine learning.

## Dataset
- Source: GWAS Catalog
- 4,237 SNP-gene association records
- Features: CHR_ID, CHR_POS, Risk Allele Frequency, OR/BETA, 
  PVALUE_MLOG, Gene mappings
- Classes: Schizophrenia (2706), Depression (1015), Bipolar (516)

## Models Trained
| Model | Accuracy | Best AUC |
|---|---|---|
| Logistic Regression | 73% | 0.824 |
| Random Forest | 90% | 0.994 |
| Gradient Boosting | 87% | 0.993 |
| XGBoost | 92% | 0.997 |
| CatBoost (Best) | 93% | 0.998 |

## Methodology
- One-vs-Rest (OvR) multiclass classification strategy
- Stratified K-Fold Cross Validation (5 folds)
- SHAP TreeExplainer for model interpretability
- ROC curves and Confusion Matrix analysis
- Feature importance via SHAP beeswarm plots

## Best Results (CatBoost)
- Overall Accuracy: 93%
- Depression AUC: 0.998
- Schizophrenia AUC: 0.984
- Bipolar AUC: 0.969

## Technologies
Python · Pandas · NumPy · Scikit-learn · CatBoost · XGBoost · 
SHAP · Matplotlib · Seaborn

## Files
- `psychiatric_disorder_classification.ipynb` — Complete ML pipeline 
  with all models, SHAP analysis, ROC curves, and visualizations
