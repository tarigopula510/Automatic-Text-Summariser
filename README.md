# 📰 Automatic Text Summariser

An NLP-based application that automatically generates concise summaries from lengthy news articles. The project implements both **extractive summarisation using TextRank** and **abstractive summarisation using a pre-trained T5 model**, and compares their performance using ROUGE evaluation metrics.

---

## 📌 Project Overview

Reading long news articles can be time-consuming when users only need the key information. This project aims to automatically reduce lengthy news articles into short, meaningful summaries while preserving the most important information.

The project uses two different summarisation approaches:

- **Extractive Summarisation** – TextRank with Sumy selects the most important sentences from the original article.
- **Abstractive Summarisation** – A pre-trained T5 model from Hugging Face generates a new summary based on the meaning and context of the article.

The generated summaries are evaluated and compared using **ROUGE-1, ROUGE-2, and ROUGE-L** metrics.

---

## 🎯 Objectives

- To automatically summarise lengthy news articles.
- To implement extractive summarisation using TextRank.
- To implement abstractive summarisation using T5.
- To compare extractive and abstractive summarisation approaches.
- To evaluate generated summaries using ROUGE metrics.
- To provide a simple and interactive user interface.
- To reduce the time required to read lengthy news articles.

---

## 🔄 Project Workflow

```text
                 News Article
                      │
                      ▼
             Text Preprocessing
                      │
              ┌───────┴───────┐
              ▼               ▼
          TextRank            T5
         Extractive       Abstractive
              │               │
              ▼               ▼
       Extractive        Abstractive
         Summary            Summary
              │               │
              └───────┬───────┘
                      ▼
               ROUGE Evaluation
                      │
                      ▼
             Model Comparison
                      │
                      ▼
               Final Results
✨ Key Features
📝 Accepts lengthy news articles as input.
📌 Extractive summarisation using TextRank.
🤖 Abstractive summarisation using T5.
📊 ROUGE-based summary evaluation.
🔍 Comparison between TextRank and T5.
📏 Configurable summary length.
💻 Interactive Streamlit interface.
⚡ Faster access to important information from news articles.
🧠 Techniques Used
1. Extractive Summarisation

Extractive summarisation selects important sentences directly from the original article.

The project uses the TextRank algorithm, which represents sentences as nodes in a graph and ranks them based on their importance and similarity to other sentences.

Article
   ↓
Sentence Splitting
   ↓
Sentence Similarity
   ↓
TextRank
   ↓
Sentence Ranking
   ↓
Important Sentences
   ↓
Extractive Summary
2. Abstractive Summarisation

Abstractive summarisation generates new sentences instead of simply selecting existing sentences.

The project uses a pre-trained T5 (Text-to-Text Transfer Transformer) model through Hugging Face Transformers.

Article
   ↓
Tokenisation
   ↓
T5 Model
   ↓
Context Understanding
   ↓
Text Generation
   ↓
Abstractive Summary
📊 Evaluation

The generated summaries are evaluated using ROUGE (Recall-Oriented Understudy for Gisting Evaluation).

The project uses:

ROUGE-1 – Measures overlap of individual words.
ROUGE-2 – Measures overlap of two-word sequences.
ROUGE-L – Measures similarity based on the longest common subsequence.

Example result format:

Method	ROUGE-1	ROUGE-2	ROUGE-L
TextRank	0.XX	0.XX	0.XX
T5	0.XX	0.XX	0.XX

The actual values will be obtained after running the models on the selected test dataset.

📚 Dataset

The project can use the following datasets:

CNN/DailyMail

The CNN/DailyMail dataset contains news articles along with human-written reference summaries. It is useful for testing and evaluating automatic summarisation models.

Inshorts

The Inshorts dataset contains news articles and short summaries and can be used for experimenting with news summarisation.

🛠️ Technologies Used
Technology	Purpose
Python	Main programming language
NLTK	Natural language processing and preprocessing
Sumy	Extractive summarisation
TextRank	Extractive summarisation algorithm
Hugging Face Transformers	T5 model implementation
T5	Abstractive summarisation
PyTorch	Deep learning framework
Pandas	Dataset processing
NumPy	Numerical operations
ROUGE	Evaluation
Streamlit	User interface
Jupyter Notebook / Google Colab	Development and experimentation
Git & GitHub	Version control
📁 Project Structure
Automatic_Text_Summariser/
│
├── app.py
├── requirements.txt
├── README.md
│
├── data/
│   ├── cnn_dailymail/
│   └── inshorts/
│
├── models/
│   ├── text_rank.py
│   └── t5_model.py
│
├── preprocessing/
│   └── preprocess.py
│
├── evaluation/
│   └── rouge.py
│
└── notebooks/
    └── experiments.ipynb
⚙️ Installation
Step 1: Clone the Repository
git clone https://github.com/your-username/Automatic_Text_Summariser.git
Step 2: Navigate to the Project
cd Automatic_Text_Summariser
Step 3: Create a Virtual Environment
python -m venv venv
Step 4: Activate the Environment

For Windows:

venv\Scripts\activate

For Linux/macOS:

source venv/bin/activate
Step 5: Install Dependencies
pip install -r requirements.txt
▶️ How to Run

Run the Streamlit application using:

streamlit run app.py

The application will open in your browser.

🖥️ Application Usage
Open the Automatic Text Summariser application.
Enter or paste a news article.
Click Generate Summary.
The application generates an Extractive Summary using TextRank.
It generates an Abstractive Summary using T5.
The generated results can be compared.
ROUGE scores can be used to evaluate the summaries when a reference summary is available.
