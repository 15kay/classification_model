
# 📨 SMS Spam Classifier

This project implements a machine learning pipeline to classify SMS messages as **Spam** or **Ham (Not Spam)**. It includes a Jupyter notebook for training and tuning multiple classification models, a JSON configuration file with hyperparameters, and an interactive Streamlit web application for real-time prediction.

![Uploading image.png…]()



## 📁 Repository Structure

```
├── SMS_Spam_Classifier.ipynb         # Notebook for data exploration, vectorization, training, and evaluation
├── classification_param_settings.json # Parameter settings for multiple ML models (GridSearch-ready)
├── sms_spam_app.py                   # Streamlit app for classifying new messages
├── spam_classifier_pipeline.pkl      # Trained model saved as a pipeline (expected to be generated by notebook)
└── spam_predictions_results.xlsx     # (Optional) Automatically generated by app for saving predictions
```

## ✅ Features

- Cleans and processes text using **TF-IDF Vectorization**
- Compares 8 classifiers: Logistic Regression, Naive Bayes, Random Forest, SVM, Gradient Boosting, AdaBoost, KNN, and Decision Tree
- Hyperparameter tuning using `GridSearchCV`
- Saves best model using `joblib`
- Interactive prediction interface built with **Streamlit**
- Saves user predictions and messages to an Excel file

## 🧪 Models Tuned

Model tuning parameters are configured in [`classification_param_settings.json`](classification_param_settings.json). Models include:

- Logistic Regression
- Multinomial Naive Bayes
- Random Forest
- Linear SVC
- Gradient Boosting
- AdaBoost
- K-Nearest Neighbors
- Decision Tree

Each model is evaluated using **Accuracy** and **F1 Score**.

## 🚀 Running the Streamlit App

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

**Example `requirements.txt`:**

```text
pandas
scikit-learn
streamlit
joblib
openpyxl
```

### 2. Run the App

Make sure you have the trained model file `spam_classifier_pipeline.pkl` in the same folder.

```bash
streamlit run sms_spam_app.py
```

## 📊 Training Notebook

The notebook `SMS_Spam_Classifier.ipynb` includes:

- Loading and preprocessing of SMS data
- TF-IDF vectorization
- Model training and comparison
- Hyperparameter tuning using `GridSearchCV`
- Saving the best model for deployment

## 📂 Prediction Output

When using the Streamlit app, every classification is saved in `spam_predictions_results.xlsx`, with the message, timestamp, and prediction label.

## 💡 Example Prediction

> **Message**: *"Congratulations! You've won a free ticket to Bahamas!"*  
> **Prediction**: 📢 Spam

> **Message**: *"Hey, are we still meeting at 6 PM?"*  
> **Prediction**: ✅ Ham (Not Spam)

## 🛠️ Future Improvements

- Add evaluation metrics (confusion matrix, ROC curve) to app
- Extend dataset for higher accuracy
- Deploy the app on platforms like **Streamlit Cloud** or **Heroku**

## 👨‍🏫 Author

**Kgaugelo Mmakola**  
Educational Material 
