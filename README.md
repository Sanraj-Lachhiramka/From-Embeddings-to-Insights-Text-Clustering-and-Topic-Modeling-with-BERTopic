
# Advanced NLP Pipeline: ArXiv Research Paper Clustering & Topic Modeling

This project implements a state-of-the-art NLP workflow to analyze and categorize scholarly articles from the **ArXiv Computation and Language** section. It demonstrates a modular approach to text analysis, moving from raw data to interpretable topic discovery using a combination of transformers, dimensionality reduction, and generative AI.

## 🚀 Project Overview
The pipeline processes over 44,000 research abstracts to identify latent thematic clusters and refine them into human-readable topics. 

### 🛠️ Technical Stack
- **Embeddings:** `Sentence-Transformers` (GTE-Small) for high-dimensional semantic representation.
- **Dimensionality Reduction:** `UMAP` for preserving local/global structures in lower-dimensional space.
- **Clustering:** `HDBSCAN` for density-based clustering and noise identification.
- **Topic Modeling:** `BERTopic` using class-based TF-IDF (c-TF-IDF).
- **Generative AI (LLMs):** Topic refinement using **Google Gemini**, **OpenAI GPT-3.5**, and local **Flan-T5** models via custom representation classes.
- **Visualization:** Interative plots using `Plotly` and static visualizations with `Matplotlib`/`Seaborn`.

## 📊 Pipeline Stages
1. **Data Ingestion:** Loading the ArXiv NLP dataset from Hugging Face.
2. **Feature Extraction:** Generating document embeddings.
3. **Clustering Optimization:** Reducing dimensions and identifying clusters.
4. **Topic Discovery:** Extracting keyword-based representations for each cluster.
5. **Representation Refining:** Comparing original c-TF-IDF keywords with LLM-generated labels to ensure high interpretability.
6. **Interactive Visualization:** Mapping documents in 2D space and exploring topic hierarchies.
