# DBALLSMRDMCMGWSTPMBDKPFP_2023

| Data type     | Analysis goal | Software/Tool  | Notes |
| ------------- |:-------------:| -----:| -----:|
| TCR-seq      | TCR clonality analysis; QC; Filtering | CellRanger v7.1.0 (VDJ alignment) | Reference: refdata-cellranger-vdj-GRCh38-alts-ensembl-5.0.0; QC/Filters: Contigs identified by CellRanger as 'high confidence', 'full length', and 'productive' were included. Only time points with at least 100 cells were included.; Clonotypes were defined by amino acid sequences of the CDR3 for alpha and beta chains. |
| Single-cell RNA-seq      | Alignment; QC; Filtering; Normalization; Clustering |   kallisto v0.46.1; bustools  v0.39.3; kb-python v0.2.3; scanpy v1.9.3; anndata v0.8.0; matplotlib v3.7.2; numpy v1.24.4; pandas v2.0.3; gget v0.27.8 | Reference: Ensembl GRCh38 version 108 modified to include the transgenic CAR sequence (excluding endogenous sequences); QC/Filters: knee plot, cells with >20% mitochondrial counts and <100 genes detected per cell were excluded. Genes detected in less than 3 cells were excluded; Count matrix normalization: log(CP10k +1). Clustering algorithm: Leiden |
| DNA Microarray; Single-cell RNA-seq | Variant calling; Demultiplex cells |    GTCtoVCF v1.2.1; bcftools v1.17; cellsnp-lite v1.2.0; vireo v0.2.3 |  Cells were demultiplexed using genotype files for all donors. |

