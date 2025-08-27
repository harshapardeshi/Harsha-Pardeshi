# Bulk-RNAseq-Analysis
## Introduction 
Bulk RNA sequencing provides a powerful way to analyze transcriptomic changes across large groups of cells. By quantifying gene expression under various experimental or clinical conditions, it helps detect differentially expressed genes (DEGs) and interpret biological differences between groups. These insights contribute to understanding disease biology, molecular pathways, and the discovery of new therapeutic strategies.
### About This Project 
This repository provides a reproducible pipeline for Bulk RNA-seq analysis, covering the complete workflow from raw sequencing data to biological interpretation. The goal is to create an easy-to-follow framework that can be applied to various datasets, including disease studies, drug response analysis, and basic transcriptomic research.

## Workflow  
- **Quality Control (QC):** Raw read quality check using FastQC and report aggregation with MultiQC.  
- **Alignment:** Mapping reads to a reference genome using HISAT2.  
- **Quantification:** Gene expression quantification using featureCounts.  
- **Differential Expression Analysis (DEA):** Identifying DEGs with DESeq2.  
- **Functional Enrichment:** Pathway and gene ontology analysis using tools like clusterProfiler.  
- **Visualization:** PCA plots, heatmaps, volcano plots, and pathway enrichment graphs.  

### 📖 Dataset / Study Background  
This project uses bulk RNA-seq data comparing **Normoxia (normal oxygen conditions)** with **Hypoxia (low oxygen conditions)**.  
The goal is to identify differentially expressed genes (DEGs) that respond to oxygen deprivation and understand the molecular  
pathways involved, such as HIF signaling, metabolic reprogramming, and stress response.  

This dataset is taken from the study by *[Guo H, Ci X, Ahmed M, et al. (2019)]*, where bulk RNA-seq was applied to investigate transcriptional  
changes under normoxic vs hypoxic conditions.  

### Reference  
- Guo H, Ci X, Ahmed M, et al. (2019). *ONECUT2 is a driver of neuroendocrine prostate cancer.*  
  **Nature Communications**, 10:278. https://doi.org/10.1038/s41467-018-08133-6  
 
**1. Install SRA Toolkit**  
```bash
sudo apt install sra-toolkit 
## Check Installation 
fastq-dump --version

### 2. Insatlling Core Tools using Conda 
# Create new environment
conda create -n rnaseq_env
conda activate rnaseq_env

### 3. Install core tools
conda install -c bioconda  fastqc multiqc hisat2

✅ After completing the installation, you are ready to download RNA-seq data from SRA.  
Go to the **Download Data** section for instructions on fetching and converting `.sra` files into `.fastq.gz` format.  


