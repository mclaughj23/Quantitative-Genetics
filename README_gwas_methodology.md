# GWAS Analysis & Fusarium Ear Rot Resistance

This module demonstrates a Genome-Wide Association Study (GWAS) to identify SNPs associated with Fusarium ear rot resistance in the Maize Diversity Core Panel. The analysis is conducted using **TASSEL** and mixed linear models.

## 🧬 Key Concepts

### 1. Genome-Wide Association Study (GWAS)
GWAS identifies associations between genetic markers (SNPs) and phenotypes by scanning the entire genome of diverse populations. Unlike linkage mapping, GWAS utilizes ancestral recombination events to provide higher resolution.

### 2. Population Structure (Q-Matrix)
Diverse populations often exhibit structure due to breeding history or geographic origin. If not accounted for, this structure can lead to **false positive associations**. We use a Q-matrix (calculated from STRUCTURE or PCA) to adjust for these effects.

### 3. Kinship (K-Matrix)
Cryptic relatedness between individuals can also bias GWAS results. A Kinship matrix represents the genetic similarity between every pair of individuals in the panel, acting as a random effect in a **Mixed Linear Model (MLM)**.

### 4. MLM vs. GLM
- **General Linear Model (GLM):** Accounts for population structure (Q).
- **Mixed Linear Model (MLM):** Accounts for both structure (Q) and kinship (K). MLM is the "gold standard" for GWAS as it significantly reduces the genomic inflation of p-values.

## 📊 Outputs
- **Manhattan Plot:** Visual representation of p-values across all chromosomes. Significant SNPs appear as peaks.
- **QQ Plot:** Evaluates the fit of the GWAS model. Deviation from the expected diagonal suggests true associations or systematic bias.
- **Top SNPs:** Identification of genomic coordinates and p-values for the most significant markers.

## 🖥️ Usage
This analysis requires the [TASSEL](https://www.maizegenetics.net/tassel) software. Detailed workflow instructions can be found in `gwas_methodology.md`.
