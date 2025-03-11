# Toward a More Accurate RAG in French: A Lightweight and Open-Source Reranker
🚀 This open-source project aims to improve the accuracy of Retrieval-Augmented Generation (RAG) systems in French through a cross-encoder-based reranker.

## Introduction
This project proposes a lightweight and high-performance Reranker specifically designed to refine document selection in RAG systems. By combining a bi-encoder and a cross-encoder, our solution improves the relevance of retrieved documents, thereby reducing errors and hallucinations in generative models such as GPT or Llama. <br/>
<br/>
📌 Main features: <br/>
📖 Dataset Construction: Prepares data using French QA sources such as PIAF, FQuAD, SQuAD-French, and pandora-s-ragneural-bridge-rag-dataset-12000-google-translated. <br/> 
🏋️ Cross-encoder Fine-tuning: Improves document reranking by training a cross-encoder model. <br/> 
🔍 Benchmarking: Compares performances using Elasticsearch, as well as bi-encoder & cross-encoder models. <br/>


## Structure du projet
```
📂 French-RAG-Reranker <br/>
├── 📜 reranker_prepare_dataset.ipynb    # Data preparation
├── 📜 reranker_fine_tuning.ipynb        # Reranker fine-tuning
├── 📜 benchmark.ipynb                   # Benchmark and model comparison
└── 📜 README.md                         # Project documentation
```

## Usage
Note: The notebooks contain basic implementations, but you may need to adjust the data sources and parameters based on your testing environment.

### Step 1 : Prepare the Data
Run the `reranker_prepare_dataset.ipynb` notebook to build and preprocess the training data.

### Step 2 : Train the Reranker
Launch the `reranker_fine_tuning.ipynb` notebook to fine-tune a cross-encoder model based on BERT or DistilRoBERTa.

### Step 3 : Benchmark and Evaluation
Use `benchmark.ipynb` to compare our model with other open-source and commercial rerankers (e.g., Cohere Rerank).

## Citation
If you use or reference this work in your research or product, you may cite it as follows (example format):
```
@inproceedings{XxxEtAl2025,
title     = {Vers une optimisation de RAG en français : conception d’un reranker open source, fine-tuning et évaluation},
author    = {Xxx, Yyy, and Zzz},
booktitle = {xxx 2025},
year      = {2025},
url       = {x x x},
}
```

## Licence & Utilisation des Données
📢 Our code and models are released under the MIT license: you are free to use, modify, and redistribute them. <br/>
📌 Important: Pay attention to the licenses of the datasets: <br/>
This project uses data from several corpora (PIAF, FQuAD, SQuAD-French, STS-B, pandora-s/neural-bridge-rag-dataset-12000-google-translated). <br/>
➡ If you plan to use the model for commercial purposes, please check the datasets’ licenses and contact the data providers if necessary. Some data may impose restrictions on commercial use. <br/>
Certain datasets are integrated directly into the script, while others are available separately under specific licenses. In all cases, please refer to their official websites for the license terms. <br/>
- PIAF : https://www.data.gouv.fr/fr/datasets/piaf-le-dataset-francophone-de-questions-reponses/ <br/>
- FQuAD : https://fquad.illuin.tech/ <br/>
- SQuAD-French : https://github.com/Alikabbadj/French-SQuAD <br/>
- pandora-s/neural-bridge-rag-dataset-12000-google-translated : https://huggingface.co/datasets/pandora-s/neural-bridge-rag-dataset-12000-google-translated/blob/b85cb4d7b4147595c1c2b9977124bc0d67153eb6/README.md <br/>
- STS Benchmark : https://huggingface.co/datasets/PhilipMay/stsb_multi_mt <br/>
