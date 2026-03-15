# Population Structure Analysis (STRUCTURE)

This module demonstrates the use of the **STRUCTURE** software to determine ancestral components and sub-population assignments in the Maize Diversity Core Panel.

## 🧬 Key Concepts

### 1. Bayesian Clustering
STRUCTURE uses a Bayesian clustering approach to assign individuals to $K$ sub-populations based on multi-locus genotype data. This method assumes that within each sub-population, markers are in Hardy-Weinberg equilibrium and Linkage equilibrium.

### 2. K-Selection (The Delta K Method)
A critical step in population structure analysis is determining the optimal number of sub-populations ($K$). Since $K$ is unknown, multiple values are tested (e.g., $K = 1$ to $K = 10$). We use the **Evanno method** ($\Delta K$) to identify the value of $K$ that represents the most significant level of structure.

### 3. Q-Matrix (Ancestry Proportions)
The output of STRUCTURE is a **Q-matrix**, where each row represents an individual and each column represents a sub-population. The values are the estimated proportions of an individual's genome that originated from each sub-population.

### 4. Application in GWAS
The Q-matrix is a fundamental component of GWAS, as it allows researchers to control for population structure, reducing the risk of false-positive associations caused by ancestry-related phenotypic differences.

## 📊 Outputs
- **Bar Plots:** Visualization of the Q-matrix, where each individual is represented by a vertical bar partitioned into colored segments according to their ancestry proportions.
- **Delta K Plots:** Line graphs used to identify the optimal $K$ value.
- **Population Assignments:** Table of individuals assigned to their most likely sub-population.

## 🖥️ Usage
This analysis requires the [STRUCTURE](https://pritchardlab.stanford.edu/structure.html) software. Detailed workflow instructions can be found in `structure_methodology.md`.
