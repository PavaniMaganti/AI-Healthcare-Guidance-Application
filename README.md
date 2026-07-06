# 🩺 AI-Healthcare-Guidance-Application

An AI-powered healthcare guidance application that predicts possible health conditions from selected symptoms and provides basic care guidance using machine learning.

## 📌 Project Overview

This project is a symptom-based healthcare AI prototype built to demonstrate a complete machine learning workflow, from dataset preparation and model training to future API deployment.

The application allows users to select symptoms and receive a predicted possible condition, confidence-based output, basic care guidance, risk level, and a recommendation on whether to seek professional medical support.

This project is designed as an educational AI/ML prototype and does not provide medical diagnosis or prescription advice.

## 🎯 Project Objective

The main goal of this project is to build an interactive healthcare guidance system that can:

* Predict possible conditions based on selected symptoms
* Compare multiple machine learning models
* Select the best-performing model using proper evaluation metrics
* Provide simple care guidance without suggesting specific medicines or dosages
* Prepare the model for deployment using FastAPI

## 🧠 Machine Learning Models Tested

Three supervised machine learning models were trained and compared:

* Support Vector Machine
* Naive Bayes
* Random Forest

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Cross-validation
* Class-wise classification report

## 📊 Dataset Summary

The dataset contains symptom-based records for disease prediction.

| Detail                 |               Value |
| ---------------------- | ------------------: |
| Disease classes        |                  41 |
| Symptom features       |                 130 |
| Original rows          |                 861 |
| Duplicate rows removed |                 231 |
| Final cleaned rows     |                 630 |
| Missing values         |                   0 |
| Feature format         | Binary 0/1 symptoms |

Each symptom column represents whether a symptom is present or absent.

## 🧹 Data Cleaning Steps

Before training the models, the dataset was cleaned and prepared by:

* Checking for missing values
* Removing exact duplicate rows
* Verifying that symptom columns contain only binary values
* Cleaning spelling issues in disease labels
* Separating symptom features and target disease labels
* Encoding disease names using label encoding
* Splitting the dataset into training and testing sets

Duplicate rows were removed to reduce data leakage and make the model evaluation more reliable.

## 🏆 Final Model Selection

After testing all three models, **Naive Bayes** was selected as the final model.

Final Naive Bayes performance:

| Metric    |  Score |
| --------- | -----: |
| Accuracy  | 0.9841 |
| Precision | 0.9877 |
| Recall    | 0.9841 |
| F1 Score  | 0.9812 |

## ✅ Why Naive Bayes Was Selected

Naive Bayes was selected because it achieved the strongest holdout test performance and performed very closely to Random Forest during cross-validation.

Although Random Forest had a slightly higher cross-validation F1 score, the difference was very small. Naive Bayes performed better on the final test set and is also simple, fast, and suitable for binary symptom-based data.

Since the dataset uses symptom features represented as 0 or 1, Naive Bayes was a strong choice for this type of classification problem.

## 🏥 Application Features

The final application is planned to include:

* Symptom selection interface
* Disease prediction
* Top possible conditions
* Confidence score
* Risk level
* Simple care guidance
* Doctor consultation recommendation
* Medical safety disclaimer

## 🚀 Future Improvements

Future versions of the project may include:

* FastAPI backend deployment
* Clean interactive frontend
* Top 3 condition prediction display
* Doctor search feature
* Appointment booking feature
* Teleconsultation support
* Model explainability
* Larger and more clinically reliable dataset
* User-friendly dashboard design

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* SVM
* Naive Bayes
* Random Forest
* Google Colab
* Joblib
* FastAPI
* GitHub
* Render

## 📁 Project Status

Current progress:

* Dataset cleaned
* Duplicate rows removed
* Three ML models trained
* Model comparison completed
* Final model selected
* Final model saved for deployment

Next step:

* Build FastAPI backend and connect the trained model to an interactive app.

## ⚠️ Medical Disclaimer

This project is an educational AI prototype. It does not provide medical diagnosis, prescription advice, emergency care, or treatment decisions. Users should consult a qualified healthcare professional for medical concerns, urgent symptoms, or worsening conditions.

## 👩‍💻 Author

Pavani Maganti
