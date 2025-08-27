# Bulk-RNAseq-Analysis
## Introduction 
Bulk RNA sequencing provides a powerful way to analyze transcriptomic changes across large groups of cells. By quantifying gene expression under various experimental or clinical conditions, it helps detect differentially expressed genes (DEGs) and interpret biological differences between groups. These insights contribute to understanding disease biology, molecular pathways, and the discovery of new therapeutic strategies.
### About This Project 
This repository provides a reproducible pipeline for Bulk RNA-seq analysis, covering the complete workflow from raw sequencing data to biological interpretation. The goal is to create an easy-to-follow framework that can be applied to various datasets, including disease studies, drug response analysis, and basic transcriptomic research.

### Workflow 
Quality Control (QC): Raw read quality check using FastQC and report aggregation with MultiQC.

Alignment: Mapping reads to a reference genome using  HISAT2.

Quantification: Gene expression quantification using featureCounts.

Differential Expression Analysis (DEA): Identifying DEGs with DESeq2.

Functional Enrichment: Pathway and gene ontology analysis using tool like clusterProfiler.

Visualization: PCA plots, heatmaps, volcano plots, and pathway enrichment graphs.
