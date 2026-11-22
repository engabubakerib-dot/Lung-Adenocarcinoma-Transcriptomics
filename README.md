# Cross-Cohort Transcriptomic Analysis of Lung Adenocarcinoma

## Overview

This repository contains the results of a cross-cohort transcriptomic analysis investigating gene-expression alterations associated with lung adenocarcinoma (LUAD), with particular emphasis on vascular and endothelial-associated genes.

The study uses two independent GEO datasets to identify differentially expressed genes, evaluate the reproducibility of expression changes, and explore the potential discriminatory ability of selected genes.

## Datasets

| Dataset | Platform | Samples | Study design |
|---|---|---:|---|
| GSE10072 | GPL96 – Affymetrix Human Genome U133A | 107 | 58 tumor, 49 normal |
| GSE75037 | GPL6884 – Illumina HumanWG-6 v3 | 166 | 83 paired tumor-normal patients |

Both datasets were analyzed using paired tumor-versus-normal comparisons.

Original datasets are available through the NCBI Gene Expression Omnibus (GEO):

- [GSE10072](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE10072)
- [GSE75037](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE75037)

## Analytical Workflow

1. Data acquisition and sample metadata processing.
2. Expression matrix and platform annotation quality control.
3. Paired differential expression analysis using the limma framework.
4. Identification of candidate genes associated with vascular and endothelial-related biological processes.
5. Independent cross-cohort validation using GSE75037.
6. Gene-level aggregation of probe-level results using the Simes method.
7. Cross-cohort effect-size comparison.
8. Exploratory ROC curve and AUC analysis.

## Main Findings

- The discovery analysis identified substantial transcriptomic differences between tumor and normal tissues.
- Enrichment analysis highlighted vascular development, angiogenesis, cell adhesion, and extracellular matrix-related biological processes.
- A 31-gene vascular/endothelial-associated candidate panel was evaluated across the two cohorts.
- Twenty-four genes showed strong directional validation.
- Twenty-eight of the 29 genes assessable in the validation cohort showed significant downregulation in gene-level Simes analysis.
- Exploratory ROC analysis showed high discrimination for several genes, including AGER, JAM2, ADAMTS8, PTPRB, and CDH5.

## Repository Contents

- `Lung_Transcriptomics_Final_Results.zip`: Consolidated analysis outputs.
- `Results/`: Differential expression, cross-cohort validation, gene-level, and ROC results.
- `Figures/`: Volcano plots, heatmaps, correlation plots, and ROC visualizations.

*The exact contents of the Results and Figures folders depend on the files uploaded to the repository.*

## Important Limitations

The ROC analyses were performed in the same validation cohort used for assessing candidate-gene reproducibility. Therefore, the reported AUC values should be considered exploratory and should not be interpreted as unbiased estimates of clinical diagnostic performance.

Further independent validation, ideally in larger and clinically characterized cohorts, is required.

Bulk-tissue transcriptomic measurements also cannot independently establish whether observed expression changes arise from altered gene regulation within cells or differences in tissue cellular composition.

## Reproducibility

The repository provides processed results and analysis outputs. Complete computational reproducibility requires access to the corresponding scripts, software versions, and preprocessing specifications.

## Data Availability

All original expression datasets are publicly available through NCBI GEO under accession numbers GSE10072 and GSE75037.


MIT License

Copyright (c) 2026 Abubaker Izz

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE
