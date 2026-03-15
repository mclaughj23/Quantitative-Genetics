# QTL Mapping of Maize Architecture

This module demonstrates a linkage mapping study to identify Quantitative Trait Loci (QTL) associated with plant height in Maize. The analysis uses a Recombinant Inbred Line (RIL) population.

## 🧬 Key Concepts

### 1. Linkage Mapping
Linkage mapping uses recombination frequencies between genetic markers to identify genomic regions (QTLs) that contribute to a quantitative trait. In this study, we analyze a Maize RIL population, which is ideal for high-resolution mapping.

### 2. Logarithm of Odds (LOD) Score
The LOD score measures the likelihood that a QTL exists at a specific genomic location versus the null hypothesis of no QTL.
- **LOD > 3:** Often considered a standard threshold for significance.
- **Peak Identification:** The location with the highest LOD score is the most likely candidate for the QTL.

### 3. Significance Thresholding (Permutations)
To account for multiple testing across the genome, we use **permutation tests**. By shuffling the relationship between phenotypes and genotypes 1,000 times, we establish an empirical LOD threshold that represents a 5% genome-wide false positive rate.

### 4. Epistasis (Locus Interaction)
Using `scantwo`, we evaluate whether pairs of loci interact to influence the trait (epistasis). This is crucial for understanding the complex genetic architecture of traits like plant height.

### 5. Multiple-QTL Model (MQM)
Single QTL scans are combined into a multi-locus model to estimate the total proportion of phenotypic variance ($R^2$) explained by the identified loci.

## 📊 Outputs
- **Genetic Map:** Visualization of marker density across chromosomes.
- **LOD Profiles:** Plots demonstrating the significance of genomic regions.
- **QTL Estimates:** Effect sizes and genomic coordinates for the identified loci.

## 🖥️ Usage
Open `maize_qtl_analysis.Rmd` in RStudio and knit to HTML to view the report.
