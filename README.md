# Fake-and-Real-news-Detection-using-RNN
Fake and Real news Detection using RNN
# 📰 Fake and Real News Detection using RNN

## 📌 Project Overview

This project focuses on detecting whether a news article is **Fake or Real** using a **Recurrent Neural Network (RNN)**.

The project uses Natural Language Processing (NLP) techniques to clean and preprocess news text, convert words into numerical sequences, and train an RNN model to classify news articles.

## 🎯 Project Objective

The objective of this project is to develop an RNN-based deep learning model that can classify a given news article as:

* **Fake News**
* **Real News**

The project also evaluates the model using accuracy, precision, recall, F1-score, and confusion matrix.

## 📂 Dataset

The project uses two datasets:

* `Fake.csv`
* `True.csv`

A target variable is created:

```text
Fake News → 0
Real News → 1
```

The title and news text are combined to create a single content field for classification.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Regular Expressions
* Scikit-learn
* TensorFlow / Keras
* Matplotlib
* Seaborn

## 🔄 Project Workflow

```text
Load Fake & Real News Data
          ↓
Understand Dataset
          ↓
Create Target Variable
          ↓
Combine Title + News Text
          ↓
Exploratory Data Analysis
          ↓
Data Cleaning
          ↓
Remove Empty Text
          ↓
Train-Test Split
          ↓
Tokenization
          ↓
Padding
          ↓
Build RNN Model
          ↓
Train Model
          ↓
Evaluate Model
          ↓
Classification Report
          ↓
Confusion Matrix
          ↓
Predict Unseen News
```

## 🧹 Data Preprocessing

The news content is cleaned by:

* Converting text to lowercase
* Removing URLs
* Removing special characters
* Removing extra spaces
* Removing empty text records

The cleaned text is then converted into numerical sequences using **Tokenization**.

### Tokenization

The tokenizer uses:

* Maximum vocabulary size: **15,000 words**
* OOV token: `<OOV>`

### Padding

Since news articles have different lengths, padding is applied to make all sequences the same length.

* Maximum sequence length: **150**
* Padding: `post`
* Truncating: `post`

## 🧠 RNN Model Architecture

The model uses the following architecture:

```text
Embedding Layer
      ↓
SimpleRNN (64 units)
      ↓
Dropout (0.3)
      ↓
Dense (32 units, ReLU)
      ↓
Dense (1 unit, Sigmoid)
```

### Model Configuration

* Optimizer: **Adam**
* Loss Function: **Binary Crossentropy**
* Metric: **Accuracy**
* Epochs: **3**
* Batch Size: **64**
* Validation Split: **20%**

## 📊 Model Evaluation

The model is evaluated on the test dataset using:

* Test Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

The classification report evaluates performance separately for **Fake** and **Real** news.

## 🔮 Prediction on New News

A prediction function is created to classify new and unseen news.

The new article goes through the same:

```text
Cleaning
   ↓
Tokenization
   ↓
Padding
   ↓
RNN Prediction
   ↓
Fake News / Real News
```

The model uses a probability threshold of **0.5**:

```text
Probability ≥ 0.5 → Real News
Probability < 0.5 → Fake News
```

## 💡 Key Learning Outcomes

This project helped demonstrate:

* NLP text preprocessing
* Tokenization
* Sequence padding
* RNN-based text classification
* Deep learning model building
* Binary classification
* Model evaluation
* Prediction on unseen text

## 🎯 Business / Real-World Use

A fake news detection system can help:

* Identify potentially misleading news content
* Support content verification systems
* Analyze large volumes of news articles
* Reduce manual effort in initial news screening

The model should be treated as a **classification aid**, since determining whether a news claim is factually true can require additional context and human verification.

## 📁 Project Structure

```text
Fake-and-Real-News-Detection/
│
├── Fake and Real News Detection using RNN.ipynb
├── Fake.csv
├── True.csv
└── README.md
```

## 👩‍💻 Author

**Reena Shri**


## 📌 Conclusion

An **RNN-based deep learning model** was developed to classify news articles as Fake or Real. The project covered text preprocessing, tokenization, padding, sequence modeling, model training, evaluation, and prediction on new unseen news.

The project demonstrates how **RNNs can be applied to NLP-based text classification and fake news detection**.
