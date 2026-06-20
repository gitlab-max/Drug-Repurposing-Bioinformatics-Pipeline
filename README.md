# Schizophrenia BA46 Meta-Analysis & Drug Repurposing

## Overview

This project presents a complete bioinformatics pipeline for identifying therapeutic targets in schizophrenia using post-mortem BA46 brain transcriptomic datasets. The workflow integrates differential expression analysis, meta-analysis, functional enrichment, network biology, and drug repurposing via molecular docking.

---

## Objectives

* Identify consistently dysregulated genes in schizophrenia BA46 cortex
* Perform robust meta-analysis across multiple GEO datasets
* Identify biological pathways and mechanisms involved in disease
* Construct protein-protein interaction networks
* Prioritize hub genes and therapeutic targets
* Evaluate drug repurposing candidates using molecular docking

---

## Datasets

The following publicly available GEO datasets were used:

* GSE12649
* GSE21138
* GSE53987

All datasets represent BA46 (prefrontal cortex) tissue samples from schizophrenia patients and controls.

---

## Workflow

The analysis pipeline includes:

1. Differential Expression Analysis (limma)
2. Probe annotation and gene mapping
3. Robust Rank Aggregation (RRA) meta-analysis
4. GO enrichment analysis (biological processes)
5. KEGG pathway enrichment analysis
6. Protein-protein interaction (PPI) network construction (STRING)
7. Hub gene identification (Cytoscape / cytoHubba)
8. Target prioritization
9. Molecular docking and drug repurposing

---

## Key Results

### Differential Expression

* Thousands of DEGs identified across datasets
* Consistent transcriptional dysregulation in neuronal and glial pathways

### Meta-analysis

* **2,568 significant consistently dysregulated genes**

### Biological Insights (GO)

* Response to hypoxia
* Gliogenesis
* Axonogenesis
* Regulation of cell growth
* Neurodevelopmental processes

### KEGG Pathways

* Neuroactive ligand-receptor interaction
* Dopaminergic synapse
* PI3K-AKT signaling pathway
* Synaptic signaling pathways

### Hub Genes

Key network hubs identified:

* HIF1A
* MAPK1
* FOXO1
* PIK3CB
* GNB1
* CDK1

---

## Target Prioritization

Based on multi-layer evidence (DEG + GO + KEGG + PPI + literature):

### Final candidate target:

* **PDE4B**

Rationale:

* Involved in cAMP signaling
* Highly expressed in brain tissue
* Druggable enzyme class
* Linked to psychiatric disorders

---

## Molecular Docking Results

Drug repurposing screening against PDE4B identified:

| Ligand       | Docking Score |
| ------------ | ------------- |
| Cilomilast   | -9.506        |
| Perphenazine | -9.459        |
| Haloperidol  | -8.877        |
| Roflumilast  | -8.874        |
| Thioridazine | -8.579        |

---

## Biological Interpretation

The results suggest that schizophrenia involves:

* Dysfunction of inhibitory interneurons
* Astrocyte dysregulation
* Synaptic signaling alterations
* Neurodevelopmental disruption
* cAMP signaling pathway involvement (PDE4B axis)

---

## Tools & Software

* R / Bioconductor
* limma
* GEOquery
* RobustRankAggreg
* clusterProfiler
* STRING database
* Cytoscape
* Schrödinger Glide (or AutoDock Vina)

---

## Repository Structure

```
data/           Raw GEO datasets
metadata/       Sample annotations
scripts/        Analysis pipeline scripts
results/        Output tables and DEG lists
figures/        Plots and network visualizations
```

---

## Reproducibility

All scripts are written in R and are fully reproducible. Each step of the pipeline is modular and can be executed independently.

---

## Future Work

* RNA-seq validation
* Single-cell transcriptomics integration
* Experimental validation (PDE4B inhibition assays)
* Expanded drug repurposing screening
* Machine learning-based biomarker discovery

---

## Author

Independent Bioinformatics Researcher

Expertise:

* Transcriptomics
* RNA-seq analysis
* Meta-analysis
* Network biology
* Drug repurposing
* Molecular docking

---

## Contact

GitHub: [your-profile]
LinkedIn: [your-link]
Email: [your-email]
