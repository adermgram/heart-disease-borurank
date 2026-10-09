# Interpretable Heart Disease Prediction Using BoruRank Feature Selection

This repository contains the code and data for our paper:

**"Interpretable Heart Disease Prediction Using BoruRank Feature Selection and Bagging Ensemble Models with LIME and SHAP Explanations"**

## BoruRank

BoruRank is a two-stage feature selection method that combines:
1. **Boruta** (all-relevant selection) to identify statistically significant features
2. **RFE** (minimal-optimal selection) to rank and reduce to the most compact subset

Applied to the UCI Heart Disease dataset, BoruRank reduces 13 clinical features to 6: `age`, `cp`, `thalach`, `oldpeak`, `ca`, `thal`.

## Results

| Model | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|-------|----------|-----------|--------|----------|---------|
| Bagging Decision Tree | **98.5%** | **1.000** | 0.971 | **0.986** | **1.00** |
| Random Forest | **98.5%** | **1.000** | 0.971 | **0.986** | **1.00** |
| Extra Trees | 98.0% | 0.972 | 0.990 | 0.981 | 0.99 |
| Bagging SVM | 92.2% | 0.949 | 0.895 | 0.922 | 0.98 |
| Bagging KNN | 84.9% | 0.843 | 0.867 | 0.854 | 0.96 |
| Bagging Naive Bayes | 82.4% | 0.817 | 0.848 | 0.832 | 0.89 |

Post-hoc interpretability is provided via **LIME** (local explanations) and **SHAP** (global feature importance).

## Repository Structure

```
.
├── Final_project_maxwell.ipynb   # Full experiment notebook
├── arxiv_paper.tex               # LaTeX source of the paper
├── arxiv_paper.pdf               # Compiled paper
└── README.md
```

## Requirements

- Python 3.8+
- scikit-learn
- boruta
- lime
- shap
- matplotlib, seaborn, pandas, numpy

## Dataset

UCI Heart Disease dataset (Kaggle version, 1,025 records, 13 features).

## Authors

- Dushara Lakmini Dayananda
- Adam Idris
- Kopseb Maxwell Nkeh

Department of Computer Science and Engineering, SRM University AP, India

## Citation

If you use this work, please cite:

```bibtex
@article{dayananda2026borurank,
  title={Interpretable Heart Disease Prediction Using BoruRank Feature Selection and Bagging Ensemble Models with LIME and SHAP Explanations},
  author={Dayananda, Dushara Lakmini and Idris, Adam and Nkeh, Kopseb Maxwell},
  year={2026}
}
```
