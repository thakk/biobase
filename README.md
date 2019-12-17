# Singularity containers for bioinformatics tools

Bioinformatics related singularity container recipies. 

Base is CentOS 8.

Currently two containers are implemented: 
- basic tools:
  - Samtools
  - BEDTools
  - FastQC
  - Bowtie2
  - MultiQC
  - Cutadapt
  - STAR
  - Hisat2
  - Picard
  - Trimmomatic
  - Samblaster
  - VarScan
  - Vcfanno
  - Plink
  - MACS2
  - Homer
  - NextFlow
  - nf-core
  - MAGeCK
  - TrimGalore
  - Bismark
  - UCSC tools
- methylKit (built from basic):
  - R + Bioconductor 
  - methylkit
- samtools (built from Alpine Linux 3.10.3)
  - Note, automated Singularity Hub build does not seem to work correctly as this recipe uses multistage build to minimize container size

## Availability

Basic tools container is available at Singularity hub: shub://thakk/biobase
