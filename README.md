# De Novo Transcriptomics Analysis Pipeline

This repository contains tools and pipelines for RNA-Seq data analysis, specifically focusing on de novo transcriptome assembly, quality control, and functional annotation.




## Pipeline Steps

1. **Sample Collection**: Collect tissues or cells based on your research objective.
2. **RNA Extraction**: Extract RNA from collected samples.
3. **RNA Integrity Check**: Use tools like Bioanalyzer or TapeStation for RNA integrity assessment (RIN score).
4. **RNA Quantification**: Quantify RNA concentration using spectrophotometers or fluorometers (e.g., NanoDrop, Qubit).
5. **Quality Control (FastQC)**: Perform initial quality checks using **FastQC** to examine raw RNA-Seq data quality.
6. **MultiQC**: Consolidate FastQC results using **MultiQC** for an overview of the overall data quality.
7. **Data Preprocessing (Fastp)**: Use **Fastp** to trim adapters and filter out low-quality sequences.
8. **Assembly (Trinity)**: Assemble the cleaned RNA data using **Trinity** to generate transcript sequences.
9. **Assembly Clustering (CD-HIT)**: Cluster transcripts using **CD-HIT** to remove redundancies.
10. **Functional Prediction (TransDecoder)**: Predict Open Reading Frames (ORFs) using **TransDecoder**.
11. **Annotation**:
   - **BLAST**: Use **BLAST** for functional annotation by comparing sequences against a reference database.
   - **GO**: Classify genes based on their functions using **Gene Ontology (GO)** terms.
   - **KEGG/Reactome**: Map genes to metabolic or signaling pathways via **KEGG** and **Reactome**.
   - **InterPro**: Identify protein domains and motifs using **InterPro** for structural and functional predictions.

## Tools and Dependencies

### Software
- **Trinity**: For de novo transcriptome assembly.
- **CD-HIT**: For clustering identical or similar sequences.
- **TransDecoder**: For prediction of coding regions (ORFs) in transcript data.
- **BLAST**: For homology search and functional annotation.
- **FastQC**: For quality assessment of raw RNA-Seq data.
- **Fastp**: For high-speed, quality control of RNA-Seq data (adapter trimming, quality filtering, etc.).
- **MultiQC**: For summarizing and visualizing FastQC reports.
- **Gene Ontology (GO)**: For functional annotation and categorization of gene functions.
- **KEGG**: For mapping genes to metabolic pathways.
- **Reactome**: For pathway-based analysis.
- **InterPro**: For protein domain and functional analysis.

### Installation

You can install the required tools by following these steps:

1. **Install Trinity**:
   ```bash
   git clone https://github.com/trinityrnaseq/trinityrnaseq.git
   cd trinityrnaseq
   make
