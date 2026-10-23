# Secondary Genomic & Phenotypic AMR Analysis in *Klebsiella pneumoniae*

## 📌 Overview
This repository contains the dataset and computational R code for a secondary genomic and phenotypic antimicrobial resistance (AMR) analysis of 27 reconciled *Klebsiella pneumoniae* isolates from Egyptian hospital settings.

---

## 📥 Project Inputs
* **Dataset File:** `Klebsiella_Source_Matched_Verified_Analysis.xlsx`
  * **Description:** Contains paired genomic profiles (72 AMR markers) and phenotypic resistance phenotypes across multiple antimicrobial classes for $N=27$ reconciled isolates (derived from Gamaleldin et al., 2024).

---

## 💻 Code & Analysis
* **Script File:** `Klebsiella_Statistical_Analysis.R`
  * **Language:** R (version >= 4.0)
  * **Methodology:** 
    1. Overall correlation testing (Pearson $r$ & Spearman $\rho$).
    2. Pairwise gene-drug contingency analysis (Fisher's Exact Test).
    3. Benjamini–Hochberg False Discovery Rate (FDR) multiple testing adjustment.

---

## 📤 Project Outputs
* **Overall Correlation:** Strong positive linear correlation between total AMR marker count and total phenotypic resistance count ($r = 0.6935$, nominal $p < 0.001$; Spearman $\rho = 0.5639$, $p = 0.002$).
* **Pairwise Associations & FDR Adjustment:** 
  * Initial exploratory analysis showed a nominal association between *blaNDM-1* and Meropenem resistance ($OR = 16.0$, nominal $p = 0.009$).
  * After applying Benjamini–Hochberg FDR correction across 21 gene-drug pairs, the adjusted $p$-value was $p_{adj} = 0.13391$ (non-significant after correction).
* **Key Conclusion:** Simple genomic marker counting reflects overall resistance burden but cannot replace direct Phenotypic Antimicrobial Susceptibility Testing (AST) for clinical decision-making.
