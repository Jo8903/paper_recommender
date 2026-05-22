# paper_recommender

Research Paper Analysis and Recommendation System for COMP8420 Assignment 3, Use Case 3.

The notebook builds a practical arXiv paper recommender that combines basic NLP baselines with advanced LLM/RAG techniques.

## Dataset

Use the Kaggle arXiv Dataset:

https://www.kaggle.com/datasets/Cornell-University/arxiv

Recommended setup:

1. Download `arxiv-metadata-oai-snapshot.json` from Kaggle.
2. Place it in this project root.
3. Run `main.ipynb` from top to bottom.

The notebook also includes a `kagglehub` fallback download if the local file is missing.

## Implemented Techniques

### 2. Basic

- 2.1 Text preprocessing: normalization, tokenization, stop-word removal.
- 2.2 TF-IDF keyword extraction.
- 2.3 Rule-based metadata extraction / NER-style author and institution extraction.
- 2.4 Traditional research-domain classification with TF-IDF + Logistic Regression.
- 2.5 Dense embedding similarity for semantic recommendation.

### 3. Advanced

- 3.1 Retrieval-Augmented Generation (RAG) for paper search and related-work discovery.
- 3.2 Fine-tuning setup using LoRA.
- 3.3 Prompt Engineerring

## Run

```bash
pip install -r requirements.txt
jupyter notebook main.ipynb
```

The first full run may take time because the arXiv dataset is large and embedding/LLM models may need to download.
