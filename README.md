# Resume Gap Analyzer

An NLP pipeline that compares a resume against a job description to identify skill gaps and score overall alignment.

## What it does
- Extracts skills from resume and job description using keyword matching
- Identifies matched skills, missing skills, and extra skills
- Scores overall text similarity using TF-IDF + cosine similarity
- Visualizes the gap with a bar chart

## Tech stack
- Python
- spaCy — text preprocessing and lemmatization
- scikit-learn — TF-IDF vectorization and cosine similarity
- pandas — results table
- matplotlib — visualization

## How it works
1. Raw text is cleaned — lowercased, stopwords removed, lemmatized
2. Skills are extracted by matching against a curated skill dictionary
3. Both texts are converted to TF-IDF vectors
4. Cosine similarity measures overall alignment (0 = no match, 1 = perfect)

## How to run

### Option 1 — Kaggle (easiest)
Open the notebook directly on Kaggle: [https://www.kaggle.com/code/nagasaiparaksh/resume-gap-analyzer]

### Option 2 — Local
```bash
pip install spacy scikit-learn pandas matplotlib
python -m spacy download en_core_web_sm
jupyter notebook resume_gap_analyzer.ipynb
```
