# TASSEL GWAS Workflow: Fusarium Ear Rot

This guide details the procedure for conducting a Genome-Wide Association Study (GWAS) using the **TASSEL** software and the Maize Diversity Core Panel.

## 1. Data Preparation
To conduct the analysis, ensure the following files are loaded:
- **Genotype File (`mdp_genotype.hmp.txt`):** HapMap format containing SNPs for 281 maize lines.
- **Phenotype File (`FusariumEarRot.txt`):** Phenotypic scores for Fusarium ear rot resistance.
- **Structure Matrix (`mdp_population_structure.txt`):** Population assignment probabilities (Q-matrix) from STRUCTURE.

## 2. Calculating Kinship (K-Matrix)
Cryptic relatedness must be accounted for to minimize false positives.
1. Select the genotype file in TASSEL.
2. Go to **Analysis > Kinship**.
3. Choose the **Scaled IBS** method.
4. Export the resulting file as `mdp_kinship.txt`.

## 3. Data Intersection (Join)
Before running the GWAS, all data must be aligned by individual ID.
1. Select the genotype, phenotype, kinship, and structure matrices.
2. Go to **Data > Intersect Join**.
3. Verify that all datasets share a common set of taxons.

## 4. Model Selection (GLM vs. MLM)

### GLM Analysis
1. Select the joined dataset.
2. Go to **Analysis > GLM**.
3. Select the Q-matrix as a fixed covariate.
4. Run the analysis and export the p-values.

### MLM Analysis (Recommended)
1. Select the joined dataset.
2. Go to **Analysis > MLM**.
3. Select the kinship matrix as a random effect and the Q-matrix as a fixed effect.
4. Ensure the **EMMA** (Efficient Mixed-Model Association) algorithm is selected.
5. Run the analysis.

## 5. Visualizing Results
Interpret the association results using the built-in TASSEL viewers or R:
- **Manhattan Plots:** Use the **Results > Manhattan Plot** option to visualize significant loci across the genome.
- **QQ Plots:** Use the **Results > QQ Plot** to check for p-value inflation and ensure the model has correctly accounted for population structure.

## 6. Interpreting Significance
Apply a **Bonferroni correction** (e.g., $0.05 / n\_snps$) or use the **FDR (False Discovery Rate)** to identify the most significant markers associated with Fusarium resistance.
