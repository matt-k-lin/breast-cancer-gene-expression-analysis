# Breast Cancer Gene Expression Analysis in R 

## Overview 

This project uses RNA-seq expression data and cell motility measurements from the Physical Sciences in Oncology (PS-ON) Cell Line Characterization Study to explore differences between two breast cancer cell lines grown on a Hyaluronic Acid Collagen substrate. The analysis compares a slower, epithelial-like breast cancer cell line, T-47D, with a faster, more motile line, MDA-MB-231. The workflow includes data import, TPM verification, log transformation, differential gene expression analysis, visualization, and biological interpretation.

## Dataset The analysis uses two data sources: 

- `PSON.RData`: gene expression and cell speed data
- Image assets used for interpretation and context

The project focuses on the breast cancer cell lines:
- T-47D
- MDA-MB-231

## Methods 
- Load and inspect gene expression data
- Convert expression values to a matrix with gene symbols as row names
- Verify transcript-per-million structure - Apply `log2(1 + x)` transformation
- Filter motility data for HyaluronicAcid Collagen
- Compare breast cancer cell lines by motility 
- Compute differential gene expression
- Rank genes by expression difference
- Visualize the distribution of DGE values
- Interpret top-ranked genes in a biological context

## Key Findings

MDA-MB-231 showed substantially higher expression of genes associated with motility and aggressive behavior, including: 
- `VIM`
- `SERPINE1`
- `MSN`
- `AXL`
- `PLAU`

T-47D showed higher expression of epithelial-associated genes, including:
- `CDH1`
- `KRT23`
- `FOXA1`
- `IGFBP5`

These patterns are consistent with differences in cell morphology and migration behavior.

## Skills Demonstrated
- R programming 
- R Markdown
- Data wrangling
- Matrix manipulation
- Exploratory data analysis
- Differential gene expression
- Biological interpretation
- Reproducible research

## Files

- `analysis.Rmd` — complete analysis
- `analysis.html` — knitted report
- `figures/` — exported plots and images
- `fast_genes.csv` — top genes upregulated in the faster cell line
- `slow_genes.csv` — top genes upregulated in the slower cell line

## How to Run

1. Open `analysis.Rmd` in RStudio.
2. Make sure the data files are available in the directory referenced by `data_dir`.
3. Click **Knit** to generate the HTML report.
