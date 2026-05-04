# alzheimer-penetrance-modeling
Custom survival analysis pipeline for Alzheimer's disease penetrance. Includes conditional likelihood estimation for SORL1 variants and Monte-Carlo simulations to quantify selection bias.

# Alzheimer's Disease: Penetrance Estimation & Bias Simulation 

**Context:** Advanced Biostatistics Project - Université Paris Cité (2025).  
**Objective:** Estimate the penetrance of SORL1 "loss of function" variants while accounting for APOE ε4 stratification and selection bias.

---

## Technical Highlights

### 1. Custom Statistical Modeling
*   **Conditional Likelihood:** Developed a custom estimation engine for $\beta$ because standard R functions were insufficient for this specific family-based design.
*   **Model Selection (BIC):** Compared constant effect vs. time-varying effect ($\beta(t)$) models. 
    *   *Result:* The time-varying model was preferred (BIC: 636.6 vs 714.3), suggesting a non-constant genetic influence across the lifespan.

### 2. Monte-Carlo Simulations
*   **Bias Quantification:** Conducted a simulation study (500 iterations) on 50-family cohorts to assess the "Index Case" bias.
*   **Findings:** Demonstrated that including the index case leads to significant overestimation of the risk parameter ($\theta$), whereas excluding it leads to underestimation.

---

##  Key Visualizations
The analysis provides multi-level penetrance curves showing the cumulative risk based on:
1.  **SORL1 status** (Carrier vs. WT).
2.  **APOE genotype** (0, 1, or 2 ε4 alleles).

---

## 📁 Repository Structure
*   `Projet2025_TL_SB.html`: Full technical report with R code and interpretations.
*   `/docs`: Official project specifications and biological context.
