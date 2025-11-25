# 📘 Context2Question  
### Transforming context and answers into meaningful, high-quality questions using NLP.

## 🚀 Overview  
**Context2Question** is an NLP-powered system that automatically generates relevant, natural questions based on a given *context* and *answer*. Unlike template-based generators, it uses a custom **SentencePiece tokenizer** and a trained NLP model to understand semantic relationships and build human-like questions. This project is ideal for educational platforms, AI-driven assessments, learning applications, automated knowledge-checking systems, and NLP research.

## ✨ Features  
- Context-aware question generation  
- Custom-trained **spiece.model** tokenizer  
- Jupyter Notebook for training and inference  
- Subword tokenization for improved performance  
- Handles long, noisy, or domain-specific text  
- Fully reproducible pipeline  

## 📂 Project Structure
Context2Question/
├── Qus_Genrator_NLP_Project.ipynb # Main notebook (training + inference)
├── spiece.model # SentencePiece tokenizer model
├── README.md # Documentation
└── requirements.txt (optional) # Dependency file
## 🔧 Technologies Used  
- Python  
- SentencePiece  
- Transformers / Deep Learning  
- PyTorch or TensorFlow  
- NumPy, Pandas  
- Jupyter Notebook  

## 🧠 How It Works  

### 1. SentencePiece Tokenization  
A custom SentencePiece tokenizer breaks text into subword units for better vocabulary handling, especially rare or domain-specific words.

### 2. Input Format  
Each sample consists of:  
- **Context** → passage  
- **Answer** → extracted phrase  
- **Question** → predicted output  

### 3. Pipeline Steps  
- Load dataset  
- Preprocess text  
- Apply SentencePiece  
- Train NLP model  
- Evaluate & generate questions  



📈 Results
=== SAMPLE 0 ===
Context (truncated): Super Bowl 50 was an American football game to determine the champion of the National Football League (NFL) for the 2015 season. The American Football Conference (AFC) champion Denver Broncos defeated ...
Answer: Denver Broncos
True Question: Which NFL team represented the AFC at Super Bowl 50?
Generated: Who won the Super Bowl?

=== SAMPLE 1 ===
Context (truncated): Super Bowl 50 was an American football game to determine the champion of the National Football League (NFL) for the 2015 season. The American Football Conference (AFC) champion Denver Broncos defeated ...
Answer: Carolina Panthers
True Question: Which NFL team represented the NFC at Super Bowl 50?
Generated: Who did the Denver Broncos defeat?

=== SAMPLE 2 ===
Context (truncated): Super Bowl 50 was an American football game to determine the champion of the National Football League (NFL) for the 2015 season. The American Football Conference (AFC) champion Denver Broncos defeated ...
Answer: Santa Clara, California
True Question: Where did Super Bowl 50 take place?
Generated: Where is the Levi's Stadium located?

🔮 Future Enhancements
Build an API (Flask/FastAPI)

Upgrade model to T5/BART

Add BLEU/ROUGE scores

Support multilingual question generation

Add a UI for interactive use

📜 License
This project is available for educational and research purposes.


