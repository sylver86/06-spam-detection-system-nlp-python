# Spam Detection System — NLP Pipeline

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![spaCy](https://img.shields.io/badge/spaCy-3.x-09A3D5?logo=spacy&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-3.x-green)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-F37626?logo=jupyter&logoColor=white)

## Overview

End-to-end **NLP pipeline** for email spam detection, combining classical machine learning, topic modelling, and named entity recognition.
The system goes beyond binary classification: it extracts the dominant themes hidden in spam traffic and identifies organisations mentioned in legitimate emails — skills directly applicable to text analytics in compliance, fraud detection, and enterprise content monitoring.

---

## Results

| Task | Method | Score |
|------|--------|-------|
| Spam/Ham classification | Naive Bayes + SVM | Accuracy ~97%, F1 ~0.96 |
| Topic modelling (spam) | LDA (5 topics) | Coherence score evaluated |
| Semantic distance between topics | Cosine similarity | Topics show clear separation |
| Organisation extraction (ham) | spaCy NER | Precision ~0.89 on ORG entities |

---

## Pipeline

```
Raw email dataset (CSV)
        │
        ▼
  Text Preprocessing
  • Tokenisation, stop-word removal
  • Lemmatisation & stemming (NLTK)
        │
        ▼
  Spam Classifier
  • Naive Bayes / SVM
  • Evaluated: accuracy, precision, recall, F1
        │
        ├──── Spam emails ────▶ LDA Topic Modelling
        │                        • 5 dominant topics extracted
        │                        • Cosine similarity between topics
        │
        └──── Ham emails  ────▶ Named Entity Recognition (spaCy)
                                 • Organisation names extracted
```

---

## Key Techniques

- **Text classification**: Naive Bayes and SVM with TF-IDF vectorisation
- **Topic modelling**: LDA (Latent Dirichlet Allocation) on spam corpus
- **Semantic distance**: Cosine similarity matrix between LDA topic vectors
- **NER**: spaCy `en_core_web_sm` model for ORG entity extraction on ham emails

---

## Dataset

Large email corpus with spam/ham labels. Features include raw email text.
Preprocessing reduces vocabulary by ~60% via stop-word removal and lemmatisation.

---

## Setup

```bash
git clone https://github.com/sylver86/06-spam-detection-system-nlp-python.git
cd 06-spam-detection-system-nlp-python
pip install spacy nltk scikit-learn pandas jupyter
python -m spacy download en_core_web_sm
jupyter notebook
```

Open `Progetto_Spam_Filter.ipynb` and run all cells.

---

## Technologies

`Python` · `spaCy` · `NLTK` · `Scikit-learn` · `LDA` · `TF-IDF` · `Pandas` · `Jupyter`
