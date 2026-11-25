# BRCA1-Breast-Cancer-Survival-Analysis
Exploratory bioinformatics analysis of BRCA1 mRNA expression and patient survival in TCGA breast cancer data
# BRCA1 Expression and Overall Survival in Breast Cancer (TCGA)

## Overview
A bioinformatics project that looks into whether BRCA1 mRNA concentration varies across breast cancer subtypes and also whether it correlates with the patient's overall survival rate

## Dataset
* **Source:** [cBioPortal](https://cbioportal.org) — *Breast Invasive Carcinoma (TCGA, PanCancer Atlas)* (~1,082 patient samples).
* **Files Used:** `data_mrna_seq_v2_rsem.txt` (RNA-seq gene expression) and `data_clinical_patient.txt` (clinical metadata & survival outcomes).

## Key Findings
* **Differential Subtype Expression:** BRCA1 mRNA expression differs significantly across molecular subtypes, with the highest median expression observed in **Luminal B (`BRCA_LumB`)** compared to **Luminal A (`BRCA_LumA`)** (*Mann-Whitney U test, p = 1.43e-29*).
* **Overall Survival Analysis:** Dividing patients into High vs. Low BRCA1 expression groups (by median `log2` expression) shows **no statistically significant difference** in overall survival (*Kaplan-Meier log-rank test, p = 0.4329*).
* **Biological Interpretation:** Having a high or low BRCA1 mRNA concentration doesn't correlate with patient survival rate if grouped up with other subtypes. Predicting patient survival rate requires checking for faulty BRCA1 DNA mutations or analyzing specific subtypes individually

## Tools & Libraries Used
* **Language:** Python (Google Colab)
* **Data Wrangling & Statistics:** `pandas`, `numpy`, `scipy`
* **Survival Analysis & Visualization:** `lifelines`, `seaborn`, `matplotlib`
