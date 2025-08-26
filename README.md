# Ultrasound_microglia_project — Analysis Code

This repository contains the code used to analyze single-cell and spatial data in the study:  
“Ultrasound-mediated BBB disruption promotes microglial reprogramming and enhanced endothelial crosstalk in the human brain.”

The analyses integrate scRNA-seq, single-cell ATAC+RNA (multiome), and gene regulatory network inference to characterize how ultrasound-mediated blood–brain barrier (BBB) opening reprograms microglia and reshapes vascular–immune interactions.

## Repository structure
code/scRNA-seq/  
R Markdown and Python scripts for preprocessing, integration, quality control, differential gene expression, pathway enrichment, and cell–cell communication analyses of the single-cell RNA-seq dataset (paired sonicated and non-sonicated brain biopsies from 7 patients).

code/multiome-atac-rna/  
Scripts for processing and integrating the multiome dataset (RNA + ATAC) from paired sonicated and non-sonicated samples (2 patients). Includes steps for quality control, dimensionality reduction, clustering, motif analysis, and differential chromatin accessibility.

code/gene-regulatory-networks/  
Scripts to construct condition-specific gene regulatory networks, using matched RNA and ATAC data to infer transcription factor activity and network rewiring (e.g., AP-1 complex and downstream targets).

code/scripts/modified_azimuth_for_cell_annotation.R  
Custom R script extending the Azimuth pipeline for cell annotation using reference atlases.

code/resources/homologs.rds  
Lookup table for gene name homolog mapping, used during integration and annotation.

## Usage
Each subfolder contains scripts organized in run order (e.g., preprocessing → integration → analysis → figures).  
Start with `scRNA-seq/` for transcriptomic analyses.  
Use `multiome-atac-rna/` for chromatin accessibility integration.  
Run `gene-regulatory-networks/` for GRN inference.  
Custom annotation and gene mapping resources are in `scripts/` and `resources/`.

All scripts assume that raw and processed data are available locally in the expected directory structure (update paths in each script as needed).
