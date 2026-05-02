# SpamGuard — Sistema di Rilevamento Spam con NLP

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![spaCy](https://img.shields.io/badge/spaCy-NLP-09A3D5)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Classification-F7931E?logo=scikitlearn&logoColor=white)
![Accuracy](https://img.shields.io/badge/Accuracy-~97%25-brightgreen)

## Panoramica

Sistema NLP per la classificazione automatica di messaggi spam/ham con accuracy ~97% e F1-score ~0.96. Pipeline completa: preprocessing testuale con spaCy e NLTK, estrazione feature TF-IDF, confronto di classificatori e valutazione con metriche enterprise.

Tecniche direttamente trasferibili a sistemi di content moderation, classificazione automatica di email e ticket, fraud detection su testo e governance dei contenuti in ambito enterprise.

## Valore Enterprise

| Settore / Azienda | Rilevanza |
|-------------------|-----------|
| Difesa & Sicurezza (Leonardo) | Content moderation, rilevamento comunicazioni anomale |
| IT Consulting (NTT Data, Accenture) | NLP pipelines per classificazione automatica documenti |
| Banking & Insurance | Fraud detection testuale, analisi comunicazioni clienti |
| Engineering Informatica | Integrazione NLP in applicazioni enterprise |

## Risultati

| Metrica | Valore |
|---------|--------|
| Accuracy | ~97% |
| F1-Score | ~0.96 |
| spaCy NER Precision | ~0.89 |
| Dataset | SMS spam/ham reale |

## Pipeline NLP

```
Testo grezzo
     │
     ▼
Preprocessing (spaCy + NLTK)
tokenizzazione · lemmatizzazione · rimozione stopwords · NER
     │
     ▼
Feature Extraction → TF-IDF Vectorizer
     │
     ▼
Classificatori (confronto): Naive Bayes · SVM · Logistic Regression · Random Forest
     │
     ▼
Valutazione: Accuracy · Precision · Recall · F1 · Confusion Matrix · AUC-ROC
```

## Setup

```bash
git clone https://github.com/sylver86/06-spam-detection-system-nlp-python.git
cd 06-spam-detection-system-nlp-python
pip install -r requirements.txt
python -m spacy download en_core_web_sm
jupyter notebook notebooks/Progetto_Spam_Filter.ipynb
```

## Struttura Repository

```
06-spam-detection-system-nlp-python/
├── notebooks/
│   └── Progetto_Spam_Filter.ipynb
├── data/
│   ├── spam_dataset.csv
│   └── spam_dataset_.csv
├── requirements.txt
└── README.md
```

## Stack Tecnologico

`Python 3.8+` · `spaCy` · `NLTK` · `scikit-learn` · `TF-IDF` · `pandas` · `Matplotlib` · `Seaborn`

---

---

# SpamGuard — NLP-Based Spam Detection System 🇬🇧

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)
![Accuracy](https://img.shields.io/badge/Accuracy-~97%25-brightgreen)

## Overview

NLP system for automatic spam/ham classification achieving ~97% accuracy and F1-score ~0.96. Full pipeline: text preprocessing with spaCy and NLTK, TF-IDF feature extraction, multi-classifier comparison, and enterprise evaluation metrics.

Techniques directly applicable to enterprise content moderation, email/ticket classification, text-based fraud detection, and digital content governance.

## Results

| Metric | Value |
|--------|-------|
| Accuracy | ~97% |
| F1-Score | ~0.96 |
| spaCy NER Precision | ~0.89 |
| Dataset | Real SMS spam/ham |

## NLP Pipeline

```
Raw text  →  Preprocessing (spaCy + NLTK)  →  TF-IDF
    →  Classifiers (NB · SVM · LR · RF)  →  Accuracy · F1 · AUC-ROC
```

## Setup

```bash
git clone https://github.com/sylver86/06-spam-detection-system-nlp-python.git
cd 06-spam-detection-system-nlp-python
pip install -r requirements.txt
python -m spacy download en_core_web_sm
jupyter notebook notebooks/Progetto_Spam_Filter.ipynb
```

## Technologies

`Python 3.8+` · `spaCy` · `NLTK` · `scikit-learn` · `TF-IDF` · `pandas` · `Matplotlib`
