# AI/ML Engineering Internship — DevelopersHub Corporation

This repository contains my submissions for the AI/ML Engineering Internship tasks at **DevelopersHub Corporation**. Each task explores a different area of the AI/ML workflow — from data exploration and visualization to regression, classification, and LLM-based chatbot development.

**Submission Date:** 26th June, 2026

---

## 📌 Overview

The internship required completing at least 3 out of 6 tasks to build practical, hands-on experience in:

- Data preprocessing and exploratory data analysis (EDA)
- Model training and evaluation
- Time series and regression modeling
- Classification and feature importance analysis
- Prompt engineering and LLM integration
- Fine-tuning language models for conversational use cases

All 6 tasks have been completed and are documented below.

---

## 📂 Repository Structure

```
.
├── task1_iris_dataset_eda/
│   ├── task1_iris_eda.ipynb
│   └── README.md
├── task2_stock_price_prediction/
│   ├── task2_stock_prediction.ipynb
│   └── README.md
├── task3_heart_disease_prediction/
│   ├── task3_heart_disease.ipynb
│   └── README.md
├── task4_health_query_chatbot/
│   ├── task4_health_chatbot.ipynb
│   └── README.md
├── task5_mental_health_chatbot/
│   ├── task5_mental_health_chatbot.ipynb
│   └── README.md
├── task6_house_price_prediction/
│   ├── task6_house_price.ipynb
│   └── README.md
└── README.md
```

---

## ✅ Tasks Summary

| # | Task | Objective | Techniques / Models |
|---|------|-----------|----------------------|
| 1 | [Exploring & Visualizing the Iris Dataset](#task-1--exploring-and-visualizing-a-simple-dataset) | Understand data trends and distributions | pandas, seaborn, matplotlib |
| 2 | [Predicting Short-Term Stock Prices](#task-2--predict-future-stock-prices-short-term) | Predict next-day closing price | Linear Regression, Random Forest, yfinance |
| 3 | [Heart Disease Prediction](#task-3--heart-disease-prediction) | Classify heart disease risk | Logistic Regression, Decision Tree |
| 4 | [General Health Query Chatbot](#task-4--general-health-query-chatbot-prompt-engineering-based) | Answer health questions via LLM | Prompt engineering, OpenAI / Hugging Face APIs |
| 5 | [Mental Health Support Chatbot](#task-5--mental-health-support-chatbot-fine-tuned) | Empathetic conversational responses | Fine-tuned DistilGPT2 / GPT-Neo / Mistral |
| 6 | [House Price Prediction](#task-6--house-price-prediction) | Predict property prices | Linear Regression, Gradient Boosting |

---

## Task 1 — Exploring and Visualizing a Simple Dataset

**Dataset:** Iris Dataset (loaded via `seaborn`)

**Approach:**
- Loaded and inspected the dataset using `pandas` (`.shape`, `.head()`, `.info()`, `.describe()`)
- Visualized feature relationships with scatter plots
- Examined distributions with histograms
- Identified outliers using box plots

**Key Insights:**
- Petal length and petal width show the strongest separation between species.
- *Setosa* is linearly separable from *versicolor* and *virginica*, while the latter two overlap slightly.

**Skills Demonstrated:** Data inspection, descriptive statistics, exploratory visualization

[📓 View Notebook](./task1_iris_dataset_eda/task1_iris_eda.ipynb)

---

## Task 2 — Predict Future Stock Prices (Short-Term)

**Dataset:** Historical stock data via the `yfinance` API

**Approach:**
- Retrieved historical OHLCV data for a selected stock
- Engineered features from Open, High, Low, and Volume
- Trained Linear Regression and Random Forest models to predict next-day closing price
- Compared actual vs. predicted prices visually

**Key Insights:**
- Random Forest captured non-linear patterns slightly better than Linear Regression, though both models track short-term trends reasonably well over erratic single-day jumps.

**Skills Demonstrated:** Time series handling, regression modeling, API-based data fetching

[📓 View Notebook](./task2_stock_price_prediction/task2_stock_prediction.ipynb)

---

## Task 3 — Heart Disease Prediction

**Dataset:** Heart Disease UCI Dataset (Kaggle)

**Approach:**
- Cleaned data and handled missing values
- Performed EDA to identify trends across age, cholesterol, and chest pain type
- Trained Logistic Regression and Decision Tree classifiers
- Evaluated using accuracy, ROC-AUC, and confusion matrix
- Extracted feature importance to identify key risk indicators

**Key Insights:**
- Chest pain type, maximum heart rate, and ST depression were among the most influential features in predicting heart disease risk.

**Skills Demonstrated:** Binary classification, medical data interpretation, model evaluation, feature importance analysis

[📓 View Notebook](./task3_heart_disease_prediction/task3_heart_disease.ipynb)

---

## Task 4 — General Health Query Chatbot (Prompt Engineering Based)

**Tools:** OpenAI GPT-3.5 API / Mistral-7B-Instruct (Hugging Face)

**Approach:**
- Built a Python script to send user health queries to an LLM
- Designed prompts (e.g., *"Act like a helpful medical assistant"*) for friendly, clear responses
- Added safety filters to prevent the bot from giving harmful or definitive medical advice, instead encouraging users to consult a professional for serious concerns

**Example Queries Tested:**
- "What causes a sore throat?"
- "Is paracetamol safe for children?"

**Skills Demonstrated:** Prompt design, LLM API integration, safety handling, conversational agent design

[📓 View Notebook](./task4_health_query_chatbot/task4_health_chatbot.ipynb)

---

## Task 5 — Mental Health Support Chatbot (Fine-Tuned)

**Model Base:** DistilGPT2 / GPT-Neo / Mistral (7B)
**Fine-Tuning Dataset:** EmpatheticDialogues (Facebook AI)

**Approach:**
- Fine-tuned a small LLM using Hugging Face's `Trainer` API
- Trained the model on empathetic, human-style dialogue
- Tuned generation parameters to maintain a gentle, supportive tone
- Built a CLI / Streamlit interface for interactive testing

**Skills Demonstrated:** Model fine-tuning, emotional tone design, conversation modeling, lightweight deployment

> **Note:** This chatbot is intended for educational and supportive purposes only and is not a substitute for professional mental health care.

[📓 View Notebook](./task5_mental_health_chatbot/task5_mental_health_chatbot.ipynb)

---

## Task 6 — House Price Prediction

**Dataset:** House Price Prediction Dataset (Kaggle)

**Approach:**
- Preprocessed features including square footage, bedroom count, and location
- Applied feature scaling and selection
- Trained Linear Regression and Gradient Boosting models
- Evaluated performance using MAE and RMSE
- Visualized predicted vs. actual prices

**Key Insights:**
- Gradient Boosting outperformed Linear Regression in capturing non-linear price relationships, particularly for high-end properties.

**Skills Demonstrated:** Regression modeling, feature scaling/selection, model evaluation, real estate data analysis

[📓 View Notebook](./task6_house_price_prediction/task6_house_price.ipynb)

---

## 🛠️ Tech Stack

- **Languages:** Python
- **Data Handling:** pandas, NumPy
- **Visualization:** matplotlib, seaborn
- **Machine Learning:** scikit-learn
- **Deep Learning / NLP:** Hugging Face Transformers
- **APIs:** yfinance, OpenAI API
- **Deployment:** Streamlit / CLI

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME

# Install dependencies
pip install -r requirements.txt

# Launch a notebook
jupyter notebook task1_iris_dataset_eda/task1_iris_eda.ipynb
```

---

## 📋 Acknowledgements

These tasks were completed as part of the **AI/ML Engineering Internship** at **DevelopersHub Corporation**. Special thanks to the mentors and program coordinators for their guidance throughout the internship.

---

## 📬 Contact

**Author:** Your Name
**LinkedIn:** [your-linkedin-url](https://linkedin.com)
**Email:** your.email@example.com

---

*If you found this repository helpful, consider giving it a ⭐!*
