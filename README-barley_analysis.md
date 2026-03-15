# Mixed Model Analysis & BLUP Estimation

This module demonstrates the analysis of an unbalanced breeding dataset for barley. By using **Best Linear Unbiased Predictors (BLUPs)**, we account for experimental variation and phenotypic shrinkage.

## 🧬 Key Concepts

### 1. Unbalanced Designs
In many breeding programs, experimental trials may have missing plots or unequal replication of lines. Mixed linear models (MLM) are the standard for handling such data as they allow for accurate estimation of genetic effects without discarding unbalanced data points.

### 2. Fixed vs. Random Effects
- **Fixed Effects:** Factors with specific levels of interest (e.g., experimental blocks or treatment groups).
- **Random Effects:** Factors sampled from a larger population (e.g., the set of barley lines in a breeding program). This allows us to estimate the genetic variance ($V_G$).

### 3. BLUPs & Shrinkage
BLUPs provide "shrunken" estimates of genetic merit. This is especially useful for lines with limited data; their estimated breeding value (EBV) is pulled (shrunk) toward the population mean based on the reliability (heritability) of the data.
$$BLUP = \mu + h^2(x - \mu)$$
Where:
- $\mu$: Population mean.
- $h^2$: Heritability.
- $x$: Raw phenotypic mean of the line.

### 4. Heritability Estimation
The analysis estimates Broad-sense Heritability ($H^2$), indicating the proportion of total phenotypic variance that can be attributed to genetic factors across the specific trial conditions.

## 📊 Outputs
- **Variance Components:** Breakdown of genetic ($V_G$) and residual ($V_E$) variance.
- **Top Breeders:** Ranking of barley lines based on their genetic merit (BLUPs).
- **Visualization:** Scatter plots demonstrating the shrinkage effect.

## 🖥️ Usage
Open `barley_analysis.Rmd` in RStudio and knit to HTML to view the report.
