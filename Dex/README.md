# Dexamethasone RNA-seq Analysis Directory

This directory contains the analysis results for samples exposed to **Dexamethasone (Dex)**\* at multiple concentrations compared to DMSO vehicle control in **MCF-7 breast cancer cells**.

## Description

Concentrations of Dexamethasone studied:
- 0.0001 μM
- 0.001 μM
- 0.01 μM
- 0.1 μM
- 1 μM

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
- **`CLSforDex[conc]vsDMSO.cls`**  
  Class file defining sample labels (treatment vs. control) for GSEA input.
- **`deseq_normalized_counts_for_Dex[conc]VsDMSO.gct`**  
  Normalized expression matrix (in GCT format) compatible with GSEA.

### Log sorted gene file
- **`log2foldsorted_file_Dex[conc]VsDMSO.csv`**  
  Genes sorted by log2 fold change values for the 0.1 nM Dexamethasone vs DMSO comparison, often used for enrichment ranking in GSEA.

### DESeq report
- **`DESeq2_report_Dex[conc]VsDMSO.pdf`**  
  Full DESeq2 statistical output summarizing differential expression results for 0.1 nM Dexamethasone exposure.

### Spearman coefficient heatmaps
- **`heatmap.png`**  
  Spearman correlation heatmaps visualizing sample-to-sample similarity based on gene expression profiles.

### GSEA application results
- **`gsea_report_for_[control/treatment]`**  
  Output from GSEA analyses, including:
  - Enrichment scores
  - Leading edge subsets
  - Enrichment plots
  - Summary reports (HTML, TSV, and PNG images)

### GO subcomponent and Biomarker results and graphs
- **`Dex[Conc]_GO_`**  
  Contains enrichment results focusing on Gene Ontology (GO) subcomponents and biomarker gene sets, including graphs summarizing key biological themes.

### Heatmap of Normalized Gene Expression and Log2 Fold Change
- **`normCountsheatmapDex`** 
Heatmap displays normalized expression (Z-scores) of selected estrogen-responsive genes across control and Dex-treated MCF-7 samples. The side annotations indicate log2 fold change and average expression values, highlighting genes consistently up- or downregulated in response to Dex exposure.

\* Samples that were associated with Plate 1B index G were excluded from the analysis as showed low intra-group correlation.
