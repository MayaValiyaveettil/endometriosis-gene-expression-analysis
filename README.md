# Endometriosis Gene Expression & Pain-Associated Pathway Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1E4bsvJIKHegd8hJRCRUU38sY8ZmjJ6r8#scrollTo=948834a7)

**Exploratory bioinformatics analysis | Python · pandas · NumPy · Matplotlib · statsmodels**

## Overview

Endometriosis is a chronic inflammatory condition in which endometrial-like tissue grows outside the uterus. Although many patients experience significant pain, others remain asymptomatic.

This project explores molecular differences between symptomatic and asymptomatic endometriosis using published RNA-sequencing results. The analysis focuses on differential gene expression, biological pathway enrichment, and gene co-expression modules associated with pain.

**Research question:** Which gene expression patterns and biological pathways distinguish symptomatic from asymptomatic endometriosis?

## Dataset

**Source:** Mamillapalli et al. (2026), *Endometriosis Pain: Genes Linked to Inflammation Distinguish Symptomatic from Asymptomatic Disease*

**GEO accession:** [GSE339400](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE339400)

The published study included 27 RNA-seq tissue samples from 19 patients:

- 14 symptomatic samples from 9 patients
- 13 asymptomatic samples from 10 patients

The analysis uses publicly available supplementary differential expression, GSEA, and WGCNA results. The notebook automatically downloads the source workbook from GEO.

## Methods

### 1. Differential Gene Expression

- Processed published differential expression statistics for 19,836 genes.
- Examined log2 fold changes and adjusted p-values.
- Created histograms and volcano plots.
- Identified genes meeting adjusted p-value and fold-change thresholds.
- Explored inflammation-associated genes.

### 2. Gene Set Enrichment Analysis

- Examined published Gene Set Enrichment Analysis (GSEA) results.
- Identified significantly enriched gene sets using FDR q-values.
- Visualized normalized enrichment scores (NES).

### 3. WGCNA Module Analysis

- Examined correlations between published gene co-expression modules and pain.
- Applied Benjamini–Hochberg correction across 40 module-level association tests.
- Identified modules remaining significant after multiple-testing correction.
- Visualized published functional enrichment results for selected modules.

## Key Findings

**Differential expression:** Of 19,836 genes examined, 890 met an adjusted p-value threshold of 0.05. Among these, 262 also exhibited an absolute log2 fold change greater than 1.

**Inflammation-associated genes:** Significant expression differences were observed for IL16, RELT, IL17RA, JAK3, and SMPD3.

**Pathway enrichment:** Four reported gene sets met an FDR threshold of 0.05 in the overall GSEA results, including hormone activity and neuropeptide receptor binding.

**Pain-associated gene modules:** Three WGCNA modules—blue, cyan, and sienna3—remained significant following Benjamini–Hochberg correction.

**Module enrichment:** Published enrichment results highlighted immune activation and cell junction organization in the blue module and RNA splicing in the cyan module.

## Reproducibility

The project is implemented in a Jupyter notebook compatible with Google Colab.

To reproduce the analysis:

1. Open `Endometriosis_Gene_Expression_Analysis.ipynb` in Google Colab.
2. Run all cells in order.
3. The notebook automatically downloads the publicly available supplementary workbook from GEO.
4. The analysis generates summary statistics and visualizations.

Required Python packages: `pandas`, `numpy`, `matplotlib`, `openpyxl`, `statsmodels`.

## Limitations

- The original study included a relatively small cohort of 19 patients.
- Some patients contributed multiple tissue samples.
- Differences in patient age, hormonal status, and technical characteristics may influence gene expression.
- This project reanalyzes published summary statistics rather than raw sequencing data.
- Observed associations do not establish causal mechanisms of endometriosis-related pain.

## Conclusion

This analysis highlights molecular patterns associated with symptomatic endometriosis, including differential expression of inflammation-related genes and enrichment of immune-associated biological processes.

The project demonstrates the application of Python-based data processing, statistical analysis, multiple-testing correction, and biological interpretation to publicly available transcriptomics results.

## Acknowledgments

All original sequencing data and published differential expression, GSEA, and WGCNA results are credited to Mamillapalli et al. (2026). This independent educational project focuses on secondary analysis, visualization, and additional multiple-testing correction of published module–pain associations.
