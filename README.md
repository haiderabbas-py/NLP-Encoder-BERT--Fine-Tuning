BERT-Based Customer Feedback Sentiment Classification

This repository contains the implementation for **Task 1** of Project 03: Fine-Tuning Transformer Architectures for Real-Time NLP Applications.
Here, we fine-tune a **BERT (Encoder-Only Transformer)** model to perform **sentiment classification** on customer feedback.

---

## 🎯 Objective

The goal of this task is to classify customer feedback into **Positive**, **Negative**, or **Neutral** categories using a fine-tuned **BERT** model from HuggingFace.

---

## 📂 Repository Structure

```
Task1-BERT/
│
├── README.md                 # Project documentation
├── preprocessing.py          # Text cleaning + tokenization
├── train.py                  # Fine-tuning BERT
├── evaluate.py               # Accuracy, F1-score, confusion matrix
├── app.py                    # Streamlit/Gradio interface for predictions
├── requirements.txt          # Dependencies
└── sample_predictions.txt    # Example outputs
```

---

## 📊 Dataset

**Customer Feedback Sentiment Dataset** (Kaggle)
Contains customer reviews labeled as:

* Positive
* Negative
* Neutral

Dataset link (as provided in assignment):
Used for training/validation/testing.

---

## 🔧 Steps Performed

### **1. Preprocessing & Tokenization**

* Cleaning text
* Removing special symbols
* Lowercasing
* BERT WordPiece tokenization
* Padding & attention masks

### **2. Training BERT**

Model: `bert-base-uncased`
We fine-tune it using:

* Cross-entropy loss
* AdamW optimizer
* Learning rate scheduling
* GPU acceleration (if available)

### **3. Evaluation Metrics**

After training, the model is evaluated using:

* **Accuracy**
* **F1-score (macro & weighted)**
* **Confusion Matrix**

### **4. Example Predictions**

Example outputs are included in `sample_predictions.txt`.

---

### **Run the UI (Streamlit/Gradio)**

```bash
streamlit run app.py
```

The interface will allow you to input customer feedback and see the predicted sentiment.

---

## 📈 Results (Expected)

A fine-tuned BERT model typically achieves:

* High accuracy
* Strong F1-score
* Clear class separation in confusion matrix

Exact metrics depend on training time and environment.

---
