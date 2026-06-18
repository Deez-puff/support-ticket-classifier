# 🎫 Support Ticket Classification & Prioritization System

An AI-powered Support Ticket Classification & Prioritization System that automatically categorizes IT support tickets and assigns priority levels using Machine Learning and Natural Language Processing (NLP).

## 📌 Overview

Organizations receive thousands of support tickets daily. Manually categorizing and prioritizing them is inefficient and time-consuming.

This project automates the process by:

* Classifying support tickets into predefined categories
* Assigning ticket priorities (High, Medium, Low)
* Evaluating model performance using ML metrics
* Providing an interactive Streamlit web interface

---

## 🚀 Features

### 📂 Ticket Classification

The model predicts support ticket categories such as:

* Hardware
* Access
* HR Support
* Storage
* Purchase
* Administrative Rights
* Internal Project
* Miscellaneous

### ⚡ Priority Prediction

Rule-based priority assignment using urgency keywords.

| Priority | Example Keywords                         |
| -------- | ---------------------------------------- |
| High     | urgent, critical, down, failure, blocked |
| Medium   | issue, problem, error, warning           |
| Low      | request, inquiry, information            |

### 🧠 NLP Processing

* Text Cleaning
* Stopword Removal
* Lemmatization
* TF-IDF Feature Extraction

### 📊 Model Evaluation

* Accuracy
* Precision
* Recall
* F1-Score
* Classification Report
* Confusion Matrix

### 🌐 Streamlit Web App

* Train new models
* Upload datasets
* Predict ticket categories
* Assign priorities
* Visualize performance metrics

---

## 🛠️ Tech Stack

* Python
* Scikit-Learn
* NLTK
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Streamlit
* Joblib

---

## 📂 Project Structure

```text
support-ticket-classifier/
│
├── data/
│   ├── all_tickets_processed_improved_v3.csv
│   ├── category_model.pkl
│   ├── category_vectorizer.pkl
│   └── confusion_matrix.png
│
├── src/
│   ├── preprocessor.py
│   ├── feature_extractor.py
│   ├── classifier.py
│   └── evaluator.py
│
├── app.py
├── main.py
├── requirements.txt
└── README.md
```

---

## 📊 Dataset Information

### Dataset Used

IT Service Ticket Classification Dataset

### Dataset Statistics

* Total Tickets: 47,837
* Categories: 8
* Text Column: Document
* Target Column: Topic_group

### Categories

* Hardware
* HR Support
* Access
* Miscellaneous
* Storage
* Purchase
* Internal Project
* Administrative Rights

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/support-ticket-classifier.git
cd support-ticket-classifier
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

Windows:

```bash
venv\Scripts\activate
```

Linux / Mac:

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run Training

```bash
python main.py
```

This will:

* Load the dataset
* Clean ticket text
* Generate TF-IDF features
* Train Logistic Regression classifier
* Evaluate model performance
* Save trained model files
* Generate confusion matrix

---

## 🌐 Run Web Application

```bash
streamlit run app.py
```

Open:

```text
http://localhost:8501
```

---

## 🧠 Machine Learning Pipeline

### Step 1: Text Preprocessing

* Lowercase conversion
* Special character removal
* Stopword removal
* Lemmatization

### Step 2: Feature Extraction

```python
TfidfVectorizer(
    max_features=3000,
    ngram_range=(1,2)
)
```

### Step 3: Model Training

```python
LogisticRegression(
    max_iter=1000,
    random_state=42
)
```

### Step 4: Evaluation

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## 📈 Results

| Metric            | Score  |
| ----------------- | ------ |
| Training Accuracy | 88.58% |
| Testing Accuracy  | 85.43% |
| Precision         | 85.79% |
| Recall            | 85.43% |
| F1-Score          | 85.43% |

### Key Findings

* Strong model generalization
* Low overfitting (~3% train-test gap)
* Purchase and Storage categories perform best
* Miscellaneous and Administrative Rights are more challenging due to overlapping vocabulary

---

## 🔍 Sample Predictions

### Example 1

Input:

```text
My laptop screen is broken and won't turn on.
```

Output:

```text
Category: Hardware
Priority: High
```

### Example 2

Input:

```text
The storage server mailbox is almost full.
```

Output:

```text
Category: Storage
Priority: Medium
```

### Example 3

Input:

```text
I would like access to the shared HR drive.
```

Output:

```text
Category: Access
Priority: Low
```

---

## 📸 Screenshots

Add screenshots after running the application:

```text
screenshots/home.png
screenshots/model_metrics.png
screenshots/confusion_matrix.png
screenshots/prediction.png
```

---

## 🔮 Future Improvements

* BERT-based Classification
* LSTM & Transformer Models
* FastAPI Integration
* Automated Ticket Routing
* Email Integration
* Cloud Deployment
* Database Support
* User Authentication

---

## 👨‍💻 Author

**Deepak Rajesh**

Support Ticket Classification & Prioritization System

Built using Machine Learning, NLP, and Streamlit.

---

## ⭐ Support

If you found this project useful:

* Star the repository ⭐
* Fork the project 🍴
* Contribute improvements 🚀
