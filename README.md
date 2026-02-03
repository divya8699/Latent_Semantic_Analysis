# Latent_Semantic_Analysis

# Latent Semantic Indexing (LSI) on Classic Literature

This project applies **Latent Semantic Indexing (LSI)** to a corpus of classic literary texts to uncover **latent semantic structures**, **thematic relationships**, and **document similarities** across genres. Using **Singular Value Decomposition (SVD)** and a comparative **Non-Negative Matrix Factorization (NMF)** analysis, the project demonstrates how dimensionality reduction techniques can reveal hidden semantic patterns beyond traditional word-frequency analysis.

The analysis is performed on **10 public-domain novels** sourced from Project Gutenberg, spanning fantasy, science fiction, adventure, comedy, and historical genres.

📄 Full technical report: *Latent Semantic Indexing* :contentReference[oaicite:0]{index=0}

---

## Objectives

- Identify **latent topics and semantic dimensions** within classic literature
- Analyze **semantic similarity between books** using cosine similarity
- Compare **SVD-based LSI** with **NMF** for interpretability and performance
- Demonstrate the effectiveness of LSI in handling **synonymy and polysemy**
- Provide visual insights through **word clouds**, **heatmaps**, and **topic distributions**

---

## Dataset

- **Source**: Project Gutenberg (public domain)
- **Corpus size**: 10 books (~600,000+ words)
- **Genres**:
  - Fantasy
  - Science Fiction
  - Adventure
  - Comedy
  - History

### Sample Books
- *Alice’s Adventures in Wonderland* — Lewis Carroll  
- *Frankenstein* — Mary Shelley  
- *The Time Machine* — H.G. Wells  
- *The Art of War* — Sun Tzu  
- *Gulliver’s Travels* — Jonathan Swift  
- *Life on the Mississippi* — Mark Twain  

---

## Methodology

### 1. Text Preprocessing
- PDF text extraction
- Sentence tokenization
- Word tokenization
- Stop-word removal
- Lemmatization

### 2. Feature Engineering
- Construction of **Term-Document Matrix (TDM)**
- TF-IDF weighting to emphasize informative terms

### 3. Latent Semantic Indexing
- Truncated **Singular Value Decomposition (SVD)**
- Projection of documents into lower-dimensional semantic space
- Cosine similarity computation between documents

### 4. Comparative Analysis
- **Non-Negative Matrix Factorization (NMF)** for interpretability comparison
- Analysis of trade-offs between reconstruction accuracy and semantic clarity

---

## Analysis & Visualizations

- 📊 **Cosine similarity heatmaps** across books
- ☁️ **Word clouds** highlighting dominant themes per book
- 🔥 **Topic heatmaps** showing top weighted words per latent topic
- 📈 **Query-based semantic matching** (e.g., *Politics & War*, *Comedy & Drama*)
- 📉 Dimensionality reduction insights across genres

Key findings include:
- Strong semantic similarity between **science fiction and adventure** novels
- Clear separation between **comedy and historical texts**
- LSI successfully groups conceptually related terms beyond surface-level frequency

---

## Notebooks Overview

| Notebook | Description |
|--------|-------------|
| `LSI_Matrix_mavericks.ipynb` | End-to-end LSI pipeline: preprocessing, SVD, similarity analysis, and visualizations |
| `lsqt_and_nmf.ipynb` | Comparative study of **SVD vs NMF** for dimensionality reduction and topic interpretability |

---

## Tech Stack

- **Language**: Python
- **NLP**: NLTK, Gensim
- **Machine Learning**: scikit-learn
- **Linear Algebra**: NumPy, SciPy
- **Visualization**: Matplotlib, Seaborn
- **Data Handling**: Pandas

---

## Results Summary

- Successfully reduced high-dimensional text data while preserving semantic structure
- Revealed latent thematic groupings across diverse literary genres
- Demonstrated that **LSI captures contextual meaning** better than raw word counts
- Highlighted interpretability vs accuracy trade-offs between **SVD and NMF**

---

## Limitations & Future Work

- Small corpus size (10 books)
- Future extensions could include:
  - Larger and more diverse datasets
  - Topic modeling (LDA)
  - Transformer-based embeddings (BERT, sentence transformers)
  - Temporal or author-centric semantic analysis

---

## How to Run

```bash
pip install numpy pandas nltk scikit-learn gensim matplotlib seaborn



Then open and run the notebooks in order:

LSI_Matrix_mavericks.ipynb

lsqt_and_nmf.ipynb
