# Predicting Bacterial Essential Genes Solely on the Protein Sequences

## Introduction
This repository provides the source code and example test datasets used to reproduce the test environments for each model introduced in our paper, *"Predicting Bacterial Essential Genes Solely on the Protein Sequences"* Additionally, it includes gene essentiality datasets of individual strains. Users can utilize the example code and data to replicate the processes of protein sequence embedding and essential gene classification. Furthermore, with minor modifications to the provided examples, users can test the models and make predictions using their own data.

## Key Features

- **Protein Sequence Only**: Predict essential genes using only their protein sequences without complex feature data integration.
- **Extended Bacterial Essential Gene Dataset**: Experimental essentiality data of approximately *280,000 bacterial genes* collected from 79 studies ('essentiality', 'protein_seq', 'dna_seq', 'genome_id', 'locus_tag', etc.).

## Performance

![performance](performance.png)

## Repository Structure

- **`data/raw_data/`**: Essential gene datasets (include non-essential genes) of each strain.
- **`data/test_exam/`**: Example test datasets consisting of genes from *E. coli* Keio collection.
- **`models/`**: Models to predict essential genes ('classifier_~') or encode protein sequences (embed_custom).
- **`results/`**: Model evaluation, prediction results and model training history.
- **`sources/`**: Jupyter notebook codes for sequence embedding ('emb ~') or model test and prediction ('test ~').

## How to Use

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sblabkribb/deessgene.git
   cd deessgene
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set options (data_path, etc.) in each source code**:
   ```python
   # Set options
   embed_ver = ["clstm", "esm2", "bert", "t5"]
   data_path = "../data/test_exam/"
   model_path = f"../models/classifier_indiv/"
   result_path = f"../results/"
   ```
4. **Run the source code**


## Citation

To cite this work, please reference:
```
Seongbo Heo et al. "Predicting Bacterial Essential Genes Solely on the Protein Sequences" Synthetic Biology Research Center, KRIBB.
```

## Acknowledgments

This project was supported by the **Korea Research Institute of Bioscience and Biotechnology (KRIBB)** and the **National Research Foundation of Korea**.

