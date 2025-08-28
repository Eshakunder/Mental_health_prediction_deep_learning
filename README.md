#  Mental Health Text Classification using Deep Learning

##  Overview
This project focuses on **mental health text classification** using **deep learning models** with different **embedding techniques**. The goal was to investigate how **Word2Vec** and **Text Vectorization** embeddings influence classification performance, and whether **Bayesian Optimization** for hyperparameter tuning can offset weaker embeddings.  

The experiments clearly show that **embedding choice is more critical than optimization alone** — Word2Vec consistently outperformed Text Vectorization, even with the same models and tuning strategies.

---

##  Project Workflow
1. **Dataset Preparation**
   - Dataset link - https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health/code
   - Preprocessed textual dataset of mental health-related statements.
   - Text cleaning: lowercasing, stopword removal, tokenization.

3. **Embedding Techniques**
   - **Word2Vec (100-dimensional pre-trained embeddings)**
   - **Text Vectorization (frequency-based representation)**

4. **Deep Learning Models**
   - **BiLSTM**
   - **BiGRU**
   - **CNN**

5. **Hyperparameter Tuning**
   - Used **Bayesian Optimization** for hyperparameter search.  
   - **15 trials**, each trained for **20 epochs** to evaluate performance.  
   - The **best configuration** from Bayesian Optimization was then used to train each model for **50 epochs** with both embedding techniques.

---

##  Experimental Setup
- **Optimization Method:** Bayesian Optimization  
- **Hyperparameter Search:** 15 trials × 20 epochs  
- **Final Training:** 50 epochs with best hyperparameters  
- **Embeddings Compared:** Word2Vec vs Text Vectorization  
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-Score  

---

##  Results & Findings
- **Word2Vec-based models outperformed Text Vectorization models** in all metrics.
- **Bayesian Optimization improved results**, but it could not overcome the limitations of poor embedding representations.
- **Best performing models (Word2Vec + BiLSTM / BiGRU)** achieved the highest accuracy and F1-scores.

### Key Takeaways
- Word2Vec embeddings captured semantic relationships better, improving classification.
- Text Vectorization produced **poor results even after optimization**, proving that embedding choice is fundamental.

---

## 📂 Project Structure
