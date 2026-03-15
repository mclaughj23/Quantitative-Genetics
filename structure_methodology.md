# STRUCTURE Workflow: Population Analysis

This guide details the procedure for conducting a population structure analysis using the **STRUCTURE** software and the Maize Diversity Core Panel.

## 1. Input Data
- **Genotype File:** Multi-locus genotype data for individuals. SNPs should be coded appropriately (e.g., 1, 2 for alleles).
- **Taxon Labels:** Unique identifiers for each individual.

## 2. Model Parameters
To ensure accurate clustering, configure the following parameters in STRUCTURE:
- **Burn-in Period:** 10,000 to 100,000 iterations (to discard early, non-equilibrated samples).
- **MCMC Iterations:** 10,000 to 100,000 iterations (for the actual analysis).
- **Ancestry Model:** **Admixture** (allows individuals to have mixed ancestry).
- **Allele Frequency Model:** **Correlated Allele Frequencies** (more sensitive to subtle structure).

## 3. Running multiple K values
Since the true number of sub-populations ($K$) is unknown, run the simulation for multiple $K$ values (e.g., $K=1$ through $K=10$).
- Perform **multiple iterations** per $K$ (e.g., 5-10 iterations) to ensure results are consistent.

## 4. Estimating Optimal K (The Evanno Method)
After the simulations are complete, use the **Evanno Method** to identify the optimal $K$:
1. Calculate the mean log-likelihood $L(K)$ for each $K$.
2. Calculate $L'(K)$ (first derivative) and $L''(K)$ (second derivative).
3. Calculate $\Delta K = |L''(K)| / SD(L(K))$.
4. The value of $K$ with the highest $\Delta K$ is typically the most significant level of structure.

## 5. Visualizing the Q-Matrix
Use the STRUCTURE output or tools like **CLUMPP** and **distruct** to generate ancestry bar plots:
- Each bar represents one individual.
- Colors within the bar represent the proportion of the genome assigned to each sub-population.
- Groups of individuals with similar color patterns indicate sub-populations (e.g., Stiff Stalk, Non-Stiff Stalk, Tropical).

## 6. Integration with GWAS
Export the final Q-matrix for $K=optimal\_k$ as a text file. This file will be used as a covariate in GWAS analyses (e.g., in TASSEL or GAPIT) to control for population structure.
