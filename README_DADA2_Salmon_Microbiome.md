
# DADA2 Bioinformatic Pipeline  
**2019 Salmon Gut Microbiome Course (V4 region, paired-end)**

## Overview
This repository contains an R-based **DADA2 bioinformatic pipeline** for analysis of the salmon gut microbiome.

- **Pipeline**: DADA2  
- **Original author**: Dr. Benjamin Callahan (NC State University)  
- **Tutorial**: https://benjjneb.github.io/dada2/tutorial.html  
- **Modified by**: Brendan Daisley, Sonja Drosdowech, Samantha Bezner, David Huyben (2025)

> **Note**  
> This workflow is configured for the **V4 region** using paired-end reads.  
> It can be adapted for **V3–V4** or other 16S regions.

---

## Software Requirements

### Install RStudio
Download and install RStudio (Windows or Mac):  
https://posit.co/download/rstudio-desktop/

---

## Install Required Packages

```r
if (!requireNamespace("BiocManager", quietly = TRUE, force = TRUE))
    install.packages("BiocManager")

BiocManager::install("dada2", version = "3.16")
```

Load libraries:

```r
library(dada2)
library(ggplot2)
library(stats)
library(dplyr)
```

---

## Working Directory Setup

```r
setwd("C:/path/201901_salmon")
```

---

## Pipeline Summary

This README documents the full workflow:
1. Quality control
2. Filtering and trimming
3. Error learning
4. Denoising
5. Merging paired reads
6. Chimera removal
7. Taxonomy assignment
8. Data cleanup (chloroplasts & mitochondria)
9. Optional phyloseq analysis

See the full R script in this repository for detailed commands and parameters.

---

## Citation

If you use this pipeline, please cite:

Callahan BJ et al. *DADA2: High-resolution sample inference from Illumina amplicon data*. Nature Methods.

---

## License
For academic and research use.
