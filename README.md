# scGPT Classifier

This project involves using scGPT, a foundation model for single-cell genomics, to generate cell embeddings from single-cell RNA-seq (scRNA-seq) data.

🎯 **Goal**: Build a classifier capable of annotating **unknown liver endothelial cells** by mapping them to an annotated reference dataset.

---

## 📓 Notebooks Overview

This repository contains several Jupyter notebooks designed for preprocessing, embedding generation, and visualization of single-cell data using **scGPT**. Below is a brief description of each:

---

### 1️⃣ `scGPT_zero_shot_embedding_ramachandran.ipynb`

🔍 **Goal**: Explore scGPT’s ability to annotate unknown cell labels in the endothelial zone of the human liver.

* Uses [Ramachandran dataset (GSE136103)](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE136103) as **query**.
* Uses [MacParland dataset (GSE115469)](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE115469) as **reference**.
* Based on the official [scGPT zero-shot tutorial](https://github.com/bowang-lab/scGPT/blob/main/tutorials/zero-shot/Tutorial_ZeroShot_Reference_Mapping.ipynb/).

---

### 2️⃣ `preprocess_ramachandran.ipynb`

⚙️ **Goal**: Preprocess raw liver samples into usable H5AD format.

* Input: `Raw.TAR` file with healthy + diseased liver samples.
* Output: Processed **H5AD** files, ready for scGPT embedding generation.
* Dataset: [Ramachandran (GSE136103)](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE136103).

---

### 3️⃣ `scGPT_reference_embedding.ipynb`

🧬 **Goal**: Generate embeddings and evaluate clustering performance.

* Dataset: [MacParland (GSE115469)](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE115469).
* Uses cell annotations as labels.
* Tests how well **scGPT** groups similar cells without fine-tuning.

---

### 4️⃣ `scGPT_UMAPs.ipynb`

🗺 **Goal**: Visualize embeddings.

* Produces **UMAP plots** for the MacParland dataset embeddings.

---

### 5️⃣ `Rds_to_h5ad.ipynb`

🔄 **Goal**: Convert data formats.

* Converts **Seurat `.Rds` objects** → **H5AD format** (required for scGPT).

---


