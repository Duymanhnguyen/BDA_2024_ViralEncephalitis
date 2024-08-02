# Meta-Analysis of Transcriptomic Profile in Viral Encephalitis

## Overview

This project performs a comprehensive meta-analysis of transcriptomic data from various studies related to viral encephalitis. The goal is to identify common gene expression patterns and pathways associated with viral infections that lead to encephalitis. This repository contains scripts, functions, and analysis results derived from public datasets sourced from the public database of Gemma.

### Project History

The Brain Data Alchemy project was initiated by **Dr. Megan Hagenauer**, who developed the core pipeline available at [Brain Data Alchemy GitHub](https://github.com/hagenaue/BrainDataAlchemy/tree/main). The pipeline was later enhanced by **Duy Nguyen**, a Biological Chemistry and Statistics major at Grinnell College, who participated as a trainee in the first and third cohorts of the project.

### Data Collection

The data collection for this project was performed in June 2022 and included six datasets:
- **GSE30577** - Rabies
- **GSE42264** - Measles
- **GSE44331** - Vesicular Stomatitis Virus
- **GSE51365** - Gammaherpesvirus 68
- **GSE53784** - West Nile Virus & Japanese Encephalitis Virus
- **GSE91074** - Venezuelan Equine Encephalitis Virus

## Analysis Workflow

Here’s the revised Analysis Workflow section, with steps logically grouped and without specific functions and output objects:

---

## Analysis Workflow

### 1. Project Set Up

- Set up the project environment with necessary packages and dependencies.

### 2. Dataset Collection and Initial Assessment

- **Search for Datasets:** Locate relevant datasets in the Gemma database using search terms related to viral encephalitis and specific virus names.
  - Datasets included for meta-analysis:
    - **GSE30577** - Rabies
    - **GSE42264** - Measles
    - **GSE44331** - Vesicular Stomatitis Virus
    - **GSE51365** - Gammaherpesvirus 68
    - **GSE53784** - West Nile Virus & Japanese Encephalitis Virus
    - **GSE91074** - Venezuelan Equine Encephalitis Virus

- **Assess Gene Expression Range:** Check for normalization issues in datasets, especially with Agilent microarray data, and address any necessary re-normalization.

### 3. Differential Expression Analysis

- **Extract Statistical Contrasts:** Retrieve and review statistical contrasts of differential expression analysis to ensure proper subset selection and reference group configuration. Adjust if necessary.

- **Download Differential Expression (DE) Results:** Retrieve and save DE results, focusing on contrasts of interest.

- **Filter DE Results:** Filter results to retain only those with good gene annotation.

- **Extract DE Results for Contrasts of Interest:** Focus on contrasts relevant to the analysis and ensure accurate extraction of Log2FC and T-statistics.

### 4. Data Aggregation and Alignment

- **Collapse DE Results:** Aggregate DE results to one result per gene, calculating standard error and sampling variance.

- **Align DE Results from Same Models:** Integrate DE results from different datasets involving mouse models into a unified dataframe.

- **Align DE Results from Different Models:** Combine DE results from mouse and rat models using an ortholog database to handle cross-species comparisons.

### 5. Meta-Analysis and Statistical Analysis

- **Compare Log2FC Across Datasets:** Generate correlation matrices and hierarchically clustered heatmaps to visualize consistency across datasets.

- **Perform Meta-Analysis:** Conduct a meta-analysis using random effect models on Log2FC and sampling variances to summarize findings across studies.

- **Correct P-Values:** Apply the Benjamini-Hochberg method to correct for false discovery rate (FDR) and identify statistically significant genes.

### 6. Interpretation and Visualization

- **Create Forest Plots:** Generate forest plots for statistically significant genes to visualize effect sizes and confidence intervals.

- **Retrieve Gene Function:** Obtain gene function information from NCBI using Entrez Gene IDs to understand the biological relevance of significant genes.

- **Conduct Gene Set Enrichment Analysis (GSEA):** Perform GSEA using KEGG, GO, Reactome databases, and the Brain.GMT database to identify enriched pathways and biological processes.

## Contributions

Please contact **Dr. Megan Hagenauer** at hagenaue@umich.edu and **Duy Nguyen** at nguyendu@grinnell.edu if you want to make any changes to the original pipeline.