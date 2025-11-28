# Single-Cell RNA-seq Analysis of Human Bone Marrow

This repository presents a single-cell RNA sequencing (scRNA-seq) analysis of human bone marrow immune cells. The workflow was implemented in Python using **Scanpy** for data preprocessing, dimensionality reduction, clustering, and visualization, and **CellTypist** for automated immune cell annotation. The aim of this project is to characterize the cellular composition of bone marrow and evaluate transcriptional heterogeneity across major immune populations.

---

## Objectives

- Perform rigorous quality control and filtering of single-cell transcriptomes  
- Normalize and log-transform gene expression data  
- Identify highly variable genes informative for downstream analysis  
- Apply PCA, neighborhood graph construction, and UMAP embedding  
- Resolve cellular heterogeneity through Leiden clustering  
- Annotate immune cell types using reference-based prediction models  
- Interpret cell populations in the context of known bone marrow biology  

---

## Methods

### Quality Control  
Quality assessment included examination of:  
- total UMI counts,  
- number of detected genes,  
- mitochondrial gene expression percentage.  

Cells falling outside acceptable biological ranges (e.g., high mitochondrial content indicative of stress or apoptosis) were excluded to ensure analytical reliability.

### Preprocessing  
Data were normalized to account for sequencing depth and log-transformed. Highly variable genes were selected to capture transcriptional variance relevant for lineage and functional differences.

### Dimensionality Reduction  
Principal component analysis (PCA) was used to summarize global transcriptional variation. The top PCs were used to compute a neighborhood graph and construct a two-dimensional **UMAP** embedding, enabling visualization of cell–cell relationships.

### Clustering  
Graph-based **Leiden clustering** identified transcriptionally distinct groups. These clusters formed the basis for exploring immune subsets and potential progenitor states.

### Cell Type Annotation  
**CellTypist** models were applied to assign putative cell identities. Predicted populations included:  
- neutrophils,  
- classical and non-classical monocytes,  
- dendritic cells,  
- NK cells,  
- naïve and mature B cells,  
- T cell subsets (helper, cytotoxic),  
- progenitor-like populations.  

Marker gene inspection was used to support the computational annotations.

---

## Results Overview

The analysis revealed well-defined myeloid and lymphoid clusters, consistent with the expected cellular architecture of bone marrow. Cytotoxic lymphocytes expressed canonical effector genes, while B cell clusters showed immunoglobulin and MS4A1 expression. Progenitor-like groups displayed early hematopoietic signatures, suggesting developmental intermediates within the dataset.

---

## Tools and Libraries

- Python 3  
- Scanpy  
- Anndata  
- CellTypist  
- NumPy  
- Pandas  
- Matplotlib  

---

## Conclusion

This workflow provides a reproducible framework for analyzing human bone marrow scRNA-seq data. By integrating quality control filtering, graph-based clustering, and reference-guided annotation, the analysis highlights the transcriptional diversity of bone marrow immune populations and supports further investigation of hematopoietic dynamics.

