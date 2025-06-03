# Estradiol RNA-seq Analysis Directory

This directory contains the analysis results for samples exposed to **17β-estradiol (E2)** at multiple concentrations compared to DMSO vehicle control in **MCF-7 breast cancer cells**.

## Description

Concentrations of E2 studied:
- 10 nM
- 1 nM
- 0.1 nM
- 0.01 nM
- 0.001 nM
- 0.0001 nM

## Directory Structure and File Descriptions

### Counts file
- **`counts_file.csv`**  
  Raw read counts for each gene across all samples, used as input for DESeq2 differential expression analysis.

### Condition and Batch file
- **`condition_file.txt`**  
  Maps each sample to its experimental group (treatment or control) for DESeq2 and GSEA analyses.
- **`batch_file.csv`**  
  Lists batch assignments for each sample to correct for potential batch effects during differential expression modeling.

### CLS and GCT file for GSEA application
- **`CLSforEstra[conc]vsDMSO.cls`**  
  Class file defining sample labels (treatment vs. control) for GSEA input.
- **`deseq_normalized_counts_for_estra[conc]VsDMSO.gct`**  
  Normalized expression matrix (in GCT format) compatible with GSEA.

### Log sorted gene file
- **`log2foldsorted_file_estra[conc]VsDMSO.csv`**  
  Genes sorted by log2 fold change values for the 0.1 nM E2 vs DMSO comparison, often used for enrichment ranking in GSEA.

### DESeq report
- **`DESeq2_report_estra[conc]VsDMSO.pdf`**  
  Full DESeq2 statistical output summarizing differential expression results for 0.1 nM E2 exposure.

### Spearman coefficient heatmaps
- **`heatmap.png`**  
  Spearman correlation heatmaps visualizing sample-to-sample similarity based on gene expression profiles.

### GSEA application results
- **`my_analysis.Gsea.[timestamp]/`**  
  Output from GSEA analyses, including:
  - Enrichment scores
  - Leading edge subsets
  - Enrichment plots
  - Summary reports (HTML, TSV, and PNG images)

### GO subcomponent and Biomarker results and graphs
- **`estradiol10000_GO_`**  
  Contains enrichment results focusing on Gene Ontology (GO) subcomponents and biomarker gene sets, including graphs summarizing key biological themes.
