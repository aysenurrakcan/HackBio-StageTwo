# HackBio - Stage Two  
## 🧬 Single-Cell RNA-seq Analysis of Immune Cells

This repository contains a Colab notebook for analyzing single-cell RNA-sequencing (scRNA-seq) data using Scanpy. The goal is to perform clustering and cell type annotation, and to interpret the biological meaning behind the cell populations in the context of infection and tissue origin.

---

### 📁 Files

- `bone_marrow_analysis.ipynb` — Main Colab notebook containing the full analysis pipeline  
- `bone_marrow.h5ad` — Input dataset (**upload manually to Colab**)  
- `README.md` — Project summary and instructions

---

### 🎯 Project Goals

- Identify immune cell types using clustering and marker genes  
- Explain the biological function of each identified cell type  
- Determine whether the sample truly comes from bone marrow  
- Evaluate whether the patient is healthy or shows signs of infection

---

### 🧪 Key Results

**Identified Cell Types:**
- Cluster 0 → Dendritic Cells  
- Cluster 1 → Plasma Cells  
- Cluster 2 → T Cells  

**Is it Bone Marrow?**  
❌ No — The dataset lacks progenitor markers (CD34⁺), erythroid (HBB, GATA1), and neutrophil markers (S100A8). The dominant populations are mature immune cells typically found in **peripheral blood**, not bone marrow.

**Is the Patient Healthy?**  
❌ Unlikely — The high abundance of plasma cells, along with a broad dendritic/monocyte cluster and active T cells, suggests an **ongoing immune response**, consistent with infection.

---

### ▶️ How to Run

1. Open the notebook in [Google Colab](https://colab.research.google.com/)
2. Upload the dataset: `bone_marrow.h5ad`
3. Run each cell step-by-step
4. Review the UMAP, dot plots, and interpretation sections at the end

---

### ⚙️ Technologies Used

- Python 3  
- Scanpy  
- AnnData  
- Matplotlib / Seaborn
