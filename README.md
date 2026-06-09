# 📰 News Topic Classifier Using BERT

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red)
![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow)
![BERT](https://img.shields.io/badge/BERT-Fine--Tuned-success)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> A Natural Language Processing (NLP) project that classifies news articles into different categories using a fine-tuned BERT model. The project leverages transfer learning from BERT to achieve accurate and efficient news topic classification. BERT-based news classification is a widely used approach for text categorization tasks.

---

# 📌 Table of Contents

* [Overview](#-overview)
* [Dataset](#-dataset)
* [Project Structure](#-project-structure)
* [Model Architecture](#-model-architecture)
* [Workflow](#-workflow)
* [Results](#-results)
* [Installation](#-installation)
* [Usage](#-usage)
* [Technologies Used](#-technologies-used)
* [Future Improvements](#-future-improvements)

---

# 🎯 Overview

News websites publish thousands of articles daily. Automatically classifying articles into topics helps improve content organization, recommendation systems, and information retrieval.

This project uses:

* BERT (Bidirectional Encoder Representations from Transformers)
* Transfer Learning
* Text Classification
* Fine-Tuning
* Deep Learning

The model learns contextual word representations and predicts the most relevant news category for a given article. BERT is commonly used for news classification and text categorization tasks.

---

# 📊 Dataset

The dataset contains news articles/headlines and their corresponding categories.

### Example Categories

| Label | Category      |
| ----- | ------------- |
| 0     | Business      |
| 1     | Sports        |
| 2     | Technology    |
| 3     | Politics      |
| 4     | Entertainment |

### Sample Data

| Text                                          | Category   |
| --------------------------------------------- | ---------- |
| Apple launches new AI-powered iPhone features | Technology |
| Government announces new economic policy      | Politics   |
| Team wins championship after dramatic final   | Sports     |

---

# 📁 Project Structure

```text
News-Topic-Classifier-Using-BERT/
│
├── data/
│   └── news_dataset.csv
│
├── notebooks/
│   └── bert_news_classifier.ipynb
│
├── models/
│   └── bert_news_model.pt
│
├── screenshots/
│   ├── training_loss.png
│   ├── confusion_matrix.png
│
├── requirements.txt
├── README.md
└── LICENSE
```

# 🏗 Model Architecture

```text
Input News Article
        │
        ▼
BERT Tokenizer
        │
        ▼
BERT Encoder
        │
        ▼
Dropout Layer
        │
        ▼
Linear Classification Layer
        │
        ▼
Predicted News Category
```

The project uses a pretrained BERT encoder and fine-tunes it for news topic classification. Fine-tuned BERT models are a standard approach for text classification tasks.

---

# ⚙️ Workflow

### 1. Data Collection

* Load news dataset
* Inspect labels
* Check class distribution

### 2. Text Preprocessing

* Remove missing values
* Tokenization
* Attention masks
* Sequence padding

### 3. Model Training

* Load pretrained BERT
* Add classification head
* Fine-tune on news dataset

### 4. Evaluation

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

### 5. Prediction

Predict category for unseen news articles.

---

# 📈 Results

### Model Performance

| Metric    | Score |
| --------- | ----- |
| Accuracy  | XX%   |
| Precision | XX%   |
| Recall    | XX%   |
| F1-Score  | XX%   |

### Training Loss

![Training Loss](screenshots/training_loss.png)

### Confusion Matrix

![Confusion Matrix](screenshots/confusion_matrix.png)

---

# 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/umm-aiman/News-Topic-Classifier-Using-BERT.git
```

Move into the project directory:

```bash
cd News-Topic-Classifier-Using-BERT
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# ▶️ Usage

Run Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
bert_news_classifier.ipynb
```

Or run training script:

```bash
python train.py
```

---

# 🔍 Example Prediction

```python
text = "Google introduces a new AI model."

prediction = model.predict(text)

print(prediction)
```

Output:

```text
Technology
```

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* PyTorch
* Hugging Face Transformers
* BERT
* Scikit-learn
* Matplotlib

---

# 📚 Skills Demonstrated

* Natural Language Processing (NLP)
* Text Classification
* Transfer Learning
* BERT Fine-Tuning
* Deep Learning
* Model Evaluation
* Data Preprocessing
* Hugging Face Transformers

---

# 🔮 Future Improvements

* RoBERTa Implementation
* DistilBERT Optimization
* Hyperparameter Tuning
* Model Deployment with FastAPI
* Docker Integration
* Streamlit Web App



⭐ If you found this project useful, consider giving it a star on GitHub!




