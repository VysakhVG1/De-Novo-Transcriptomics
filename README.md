# De Novo Transcriptomics Analysis Pipeline

This repository contains bioinformatics tools and pipelines for de novo transcriptome assembly, quality control, and annotation.

## Tools & Dependencies
- Trinity
- Fastp
- FastQC
- BUSCO


## Usage
1. **Preprocessing**: `bash scripts/fastp_preprocessing.sh raw_data/input.fastq processed_data/`
2. **Assembly**: `bash scripts/trinity_assembly.sh processed_data/input.fastq processed_data/assembly/`

## License
MIT License (or any applicable license)

## Citation
Please cite as:
[Your Paper or Citation Info]
