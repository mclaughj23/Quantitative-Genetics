# Quantitative Genetics & Bioinformatics Portfolio

This repository showcases a comprehensive suite of quantitative genetic analyses, ranging from classical breeding designs to modern genomic selection and association mapping. The projects were developed as part of a graduate-level curriculum in Bioinformatics and Plant Breeding.

## 🚀 Key Skills Demonstrated
- **Mixed Linear Models (MLM):** Estimation of BLUPs, GCA/SCA effects, and variance components using the `sommer` and `lme4` R packages.
- **Linkage Mapping (QTL):** High-resolution mapping of quantitative trait loci using `R/qtl`, including permutation-based significance thresholds.
- **Genome-Wide Association Studies (GWAS):** Analysis of population structure and kinship using TASSEL and mixed models.
- **Population Genetics:** Sub-population assignment and allele frequency analysis using STRUCTURE.
- **Data Visualization:** Creating professional-grade Manhattan plots, QQ plots, and genetic maps.

---

## 📂 Project Modules

### [01. Diallel Analysis & Mixed Models](./01-Diallel-Analysis-Sommer)
**Tools:** `R`, `sommer`
**Analysis:** Evaluation of a half-diallel dataset to estimate General Combining Ability (GCA) and Specific Combining Ability (SCA). Focuses on heritability estimation and ranking parents by genetic merit (BLUPs).

### [02. BLUP Estimation in Unbalanced Breeding Data](./02-Mixed-Model-BLUPs-Barley)
**Tools:** `R`, `lme4`
**Analysis:** Mixed model analysis of Double Haploid (DH) barley lines. Handles unbalanced experimental designs to extract reliable breeding values (BLUPs) and estimate broad-sense heritability.

### [03. QTL Mapping of Maize Architecture](./03-QTL-Mapping-Maize-Rqtl)
**Tools:** `R`, `R/qtl`
**Analysis:** Linkage mapping of plant height in a Maize Recombinant Inbred Line (RIL) population. Includes LOD score profiling, epistasis detection, and multiple-QTL model fitting.

### [04. GWAS & Fusarium Ear Rot Resistance](./04-GWAS-Maize-TASSEL)
**Tools:** `TASSEL`, `R`
**Analysis:** Association mapping using the Maize Diversity Core Panel. Accounting for population structure (Q-matrix) and kinship (K-matrix) to identify SNPs associated with disease resistance.

### [05. Population Structure Analysis](./05-PopStructure-Maize-STRUCTURE)
**Tools:** `STRUCTURE`, `CLUMPP`
**Analysis:** Determining ancestral components and optimal sub-population counts (K) for the maize diversity panel.

---

## 🛠️ Installation & Requirements
Most analyses are written in R. To replicate these results, you will need:
```r
install.packages(c("sommer", "qtl", "lme4", "ggplot2", "dplyr"))
```
For the GWAS and Population Structure modules, standalone installations of [TASSEL](https://www.maizegenetics.net/tassel) and [STRUCTURE](https://pritchardlab.stanford.edu/structure.html) are required.

---
**Contact:** [Your Name] - [Your Email/LinkedIn]
