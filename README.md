# Large-scale-Multi-omic-Analysis-of-COVID-19-Severity
Large-scale Multi-omic Analysis of COVID-19 Severity
# COVID-19 Multi-Omic Analysis: Differentially Expressed Genes (GSE157103) 🦠🧬

## Overview

This repository contains the key visualization and summary files resulting from a differential gene expression analysis conducted on the public domain dataset **GSE157103** (Large-scale Multi-omic Analysis of COVID-19 Severity).

The analysis compares the gene expression profiles between hospitalized **COVID-19 patients** and **NON-COVID-19 patients** to identify genes significantly affected by the disease. This is a crucial step in understanding the molecular pathology and identifying potential therapeutic targets for COVID-19.

### Methodology
The analysis was performed using standard bioinformatics tools (likely **GEO2R** and associated differential expression methods like DESeq2 or limma) with a focus on identifying genes with a significant difference in expression (low P-adjusted value) and a notable change in magnitude (log2 Fold Change).

---

## Repository Contents

The files represent key steps and visualizations from the differential expression pipeline:

| File Name | Analysis Type | Purpose/Insight |
| :--- | :--- | :--- |
| **SUMMARY FILE.pdf** | Study Summary | Contains the GEO accession (GSE157103), study title, design, and citation details. |
| **TOTAL FILE.pdf** | Differential Expression Table | The full table of results, including **GeneID**, **padj** (adjusted P-value), **log2FC** (Fold Change), and gene annotations. |
| **VOLCANO PLOT.pdf** | Statistical Visualization | Plots the significance (-log10(P-value)) vs. the magnitude (log2FC) of gene expression changes, highlighting the most differentially expressed genes. |
| **MEANDIFF PLOT.pdf** | Mean-Difference Plot | Visualizes the relationship between the average expression signal (log10 base Mean) and the log2 Fold Change (log2FC). |
| **GEO2R Venn diagram.pdf** | Overlap Analysis | Shows the number of significant genes (e.g., using a threshold like $Padj<0.03$) and their overlap across different contrasts. |
| **UMAP PLOT.png** | Clustering/Dimensionality Reduction | A UMAP plot showing how samples cluster based on their global expression profiles (ideally separating COVID-19 from non-COVID-19 groups). |
| **P-VALUE HISTOGRAM.png** | Quality Control | Checks the distribution of raw P-values, which is a key diagnostic for well-behaved statistical tests. |
| **BOX PLOT.png** | Expression Distribution | Shows the distribution of expression values (e.g., normalized counts) across samples or groups. |
| **MEAN VARIANCE TREND PLOT.png** | Quality Control | Used to check the relationship between mean expression and variance, crucial for differential expression methods. |
| **TAKING ONE GENE EXPRESSION VALUE.pdf** | Individual Gene Profile | Example of a profile graph showing the expression level of a specific gene (e.g., GUCY2D) across individual samples/groups. |

---

## Key Findings (Based on GSE157103)

* **Dataset:** Large-scale Multi-omic Analysis of COVID-19 Severity (Homo sapiens).
* **Comparison:** **COVID-19 vs. NON COVID-19** (likely hospitalized patients).
* **Significant Genes:** The analysis identified a large number of genes with $Padj < 0.03$, confirming significant transcriptional changes related to the disease.
* **Visualization Insights:** The **Volcano Plot** clearly identifies numerous genes that are both highly statistically significant and strongly up- or down-regulated. The **UMAP Plot** visually confirms a separation between the patient groups based on their overall gene expression.

---

## Setup and Interpretation

To interpret these results:

1.  **Examine the Volcano Plot:** Genes in the upper-left and upper-right corners are the most interesting candidates for further research.
2.  **Review the TOTAL FILE.pdf:** Use the `padj` and `log2FC` columns to filter the most reliable differentially expressed genes.
3.  **Cross-Reference:** The genes identified as significant can be used as input for further functional analysis (e.g., Pathway Enrichment Analysis using DAVID or GO).

### Reproducibility
The data and primary analysis tools are available via the NCBI GEO website: `GSE157103`. The results can be replicated using the GEO2R tool with the specified contrast (`COVID-19 vs NON COVID-19`) and Padj threshold.
