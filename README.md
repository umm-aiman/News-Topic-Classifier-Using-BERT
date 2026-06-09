📰 News Topic Classifier Using BERT

A Natural Language Processing (NLP) project that fine-tunes BERT (bert-base-uncased) to classify news headlines into topic categories using the AG News dataset.

📌 Table of Contents
Overview
Dataset
Project Structure
Model Architecture
Data Preprocessing
Training
Evaluation Metrics
Results
Installation
Usage
Model Deployment
Future Improvements
Technologies Used
License
📖 Overview

News articles are published every second across the globe. Automatically categorizing them helps news organizations, search engines, and recommendation systems organize content efficiently.

This project uses BERT (Bidirectional Encoder Representations from Transformers) to classify news headlines into four categories:

Label	Category
0	World
1	Sports
2	Business
3	Science/Technology

Example:

Input: "Google launches a new AI model"

Prediction: Science/Technology
📂 Dataset
AG News Dataset

The AG News dataset contains:

120,000 training samples
7,600 testing samples
4 news categories

Dataset Features:

Feature	Description
text	News headline/article
label	Category label
📁 Project Structure
News-Topic-Classifier-BERT/
│
├── News_Topic_Classifier.ipynb
├── app.py
├── requirements.txt
├── README.md
│
├── saved_model/
│   ├── config.json
│   ├── model.safetensors
│   ├── tokenizer.json
│   └── vocab.txt
│
└── results/
🤖 Model Architecture

Model Used:

bert-base-uncased

Architecture:

Input Text
      │
Tokenizer
      │
BERT Encoder
      │
Classification Head
      │
4 Output Classes

The pretrained BERT model is fine-tuned on the AG News dataset for multiclass text classification.

🧹 Data Preprocessing

Steps performed:

1. Load Dataset
from datasets import load_dataset

dataset = load_dataset("ag_news")
2. Tokenization
tokenizer(
    text,
    truncation=True,
    padding="max_length",
    max_length=128
)
3. Convert Labels
label → labels
4. Convert to PyTorch Format
tokenized_dataset.set_format("torch")
🚀 Training

Training Configuration:

Parameter	Value
Model	bert-base-uncased
Epochs	3
Learning Rate	2e-5
Batch Size	16
Max Length	128
Optimizer	AdamW

Training performed using:

Trainer(
    model=model,
    args=training_args,
    train_dataset=train_dataset,
    eval_dataset=test_dataset
)
📊 Evaluation Metrics

The model is evaluated using:

Accuracy
Correct Predictions / Total Predictions
F1 Score
2 × (Precision × Recall)
-------------------------
 Precision + Recall

Metrics calculated using:

evaluate.load("accuracy")
evaluate.load("f1")
📈 Results
Metric	Score
Accuracy	94%+
F1 Score	94%+

The fine-tuned BERT model achieves strong performance on AG News classification tasks.

⚙️ Installation

Clone Repository

git clone <your-repository-url>
cd News-Topic-Classifier-BERT

Install Dependencies

pip install -r requirements.txt
▶️ Usage

Run Training:

python train.py

Run Prediction:

classifier(
    "Tesla unveils new autonomous driving technology"
)

Example Output:

Science/Technology
🌐 Model Deployment

The trained model can be deployed using:

Streamlit
streamlit run app.py
Gradio
import gradio as gr

Possible deployment platforms:

Hugging Face Spaces
Streamlit Cloud
Render
Railway
🔮 Future Improvements
DistilBERT implementation for faster inference
Hyperparameter tuning
Larger news datasets
Real-time news classification API
Multi-language news classification
Docker deployment
🛠️ Technologies Used
Python
Hugging Face Transformers
PyTorch
Datasets Library
Evaluate
NumPy
Scikit-Learn
Streamlit
Jupyter Notebook
📜 License

This project is licensed under the MIT License.



