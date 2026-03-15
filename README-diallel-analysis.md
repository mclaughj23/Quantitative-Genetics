# Diallel Analysis & Mixed Model Equations

This module focuses on the quantitative genetic analysis of a half-diallel mating design. Using the **`sommer`** package in R, we partition phenotypic variance into genetic components and estimate breeding values.

## 🧬 Key Concepts

### 1. Mating Design: Half-Diallel
In a half-diallel, $p$ parents are crossed in all possible combinations without reciprocals or selfs. This design is highly efficient for:
- Estimating the importance of **General Combining Ability (GCA)**.
- Identifying specific crosses with superior **Specific Combining Ability (SCA)**.

### 2. General Combining Ability (GCA)
GCA represents the average performance of a parent in all its cross combinations. It is directly related to the additive genetic variance ($V_A$) and reflects the breeding value of the parent.

### 3. Specific Combining Ability (SCA)
SCA represents cases where certain cross combinations perform better or worse than expected based on the GCA of the parents. It is related to non-additive genetic variance, such as dominance and epistasis.

### 4. Mixed Model Equations (MME)
The analysis utilizes Restricted Maximum Likelihood (REML) to solve the mixed model:
$$y = X\beta + Z u + \epsilon$$
Where:
- $X\beta$: Fixed effects (e.g., experimental blocks).
- $Zu$: Random effects (Parental GCA and Cross SCA).
- $\epsilon$: Residual error.

## 📊 Outputs
- **Variance Components:** Estimation of $V_A$, $V_{D+I}$, and $V_E$.
- **Heritability:** Calculation of Narrow-sense ($h^2$) and Broad-sense ($H^2$) heritability.
- **BLUPs:** Ranking parents and crosses by their Best Linear Unbiased Predictors to inform selection decisions.

## 🖥️ Usage
Open `diallel_analysis.Rmd` in RStudio and knit to HTML to view the full report.
