# Sarcasm Detection Model

This project is a **Machine Learning-based Sarcasm Detection System** that predicts whether a given sentence is sarcastic or not. It uses Natural Language Processing (NLP) techniques and the Bernoulli Naive Bayes algorithm trained on a real-world dataset from news headlines.

<div align="center">
  <img src="screenshots/image.png" alt="Sarcasm Detection Screenshot" width="700"/>
</div>

---

## Project Overview

- **Input**: News headlines
- **Output**: Prediction - `Sarcasm` or `Not Sarcasm`
- **Model Used**: Bernoulli Naive Bayes
- **Dataset**: [Sarcasm Headlines Dataset from HuffPost & The Onion](https://www.kaggle.com/datasets/rmisra/news-headlines-dataset-for-sarcasm-detection)
- **Accuracy**: ~84.5%

---

## Technologies Used

- **Python** 🐍
- **Pandas** – Data manipulation
- **NumPy** – Numerical operations
- **Scikit-learn (sklearn)** – Machine learning model and data preprocessing
- **CountVectorizer** – Text vectorization

---

## Dataset Info

The dataset contains three columns:

- `article_link` – URL to the article
- `headline` – News headline text
- `is_sarcastic` – Target variable  
  - `1` = Sarcasm  
  - `0` = Not Sarcasm

We convert this into `"Sarcasm"` and `"Not Sarcasm"` for better readability.

---

## How It Works

1. **Data Loading**: Load `Sarcasm.json` file with `pandas`.
2. **Label Mapping**: Convert binary labels to human-readable strings.
3. **Feature Extraction**: Use `CountVectorizer` to convert text into numerical vectors.
4. **Model Training**: Train a `BernoulliNB` model on 80% of the dataset.
5. **Model Evaluation**: Evaluate on 20% of the data (~84.5% accuracy).
6. **Prediction**: Accepts user input and classifies it as sarcastic or not.
