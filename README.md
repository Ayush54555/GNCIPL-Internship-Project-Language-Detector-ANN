# 📝 Language Detector using Character-level ANN (Week 5 Internship Project)

This project was completed as part of my **AI-ML Internship (Week 5 Project)**.  
The goal of this project is to build a simple **Language Detection system** that can identify the language of an input sentence using a **character-level Artificial Neural Network (ANN)**.

---

## 📌 Project Overview
- **Project Title:** Language Detector  
- **Internship Organization:** Global Next Consulting India Pvt. Ltd. (GNCIPL)  
- **Domain:** Natural Language Processing (NLP)  
- **Objective:** Detect the language from a given text input using a neural network trained on character sequences.  
- **ML Technique:** Supervised Learning (Classification) with ANN in Keras  

---

## 📂 Dataset
- **Source:** [Language Detection Dataset on Kaggle](https://www.kaggle.com/datasets/basilb2s/language-detection)  
- **Description:** The dataset contains text samples in multiple languages with corresponding language labels.  
- **File Used:** `Language Detection.csv`

---

## ⚙️ Steps Followed
1. **Data Collection & Cleaning**  
   - Loaded dataset (text and language labels).  
   - Lowercased text and removed extra spaces.  

2. **Preprocessing**  
   - Used **Keras Tokenizer** with `char_level=True` to convert characters into integer IDs.  
   - Applied `pad_sequences` to make all sequences the same length.  
   - Encoded labels using `LabelEncoder`.  

3. **Model Building**  
   - Built a simple ANN using Keras:  
     - **Embedding Layer** → converts characters into vectors.  
     - **GlobalAveragePooling1D** → averages sequence into one vector.  
     - **Dense Layer (ReLU)** → learns hidden patterns.  
     - **Dense Layer (Softmax)** → outputs probabilities for each language.  

4. **Model Training**  
   - Optimizer: **Adam**  
   - Loss: **Sparse Categorical Crossentropy**  
   - Epochs: 8  
   - Batch Size: 64  

5. **Evaluation**  
   - Calculated **Accuracy, Precision, Recall, F1-Score**.  
   - Visualized **Confusion Matrix**.  

6. **Testing**  
   - Tried custom sentences like:  
     - `"Bonjour, comment allez-vous?"` → French  
     - `"Hola, ¿cómo estás?"` → Spanish  
     - `"This is an English sentence."` → English  

---

## 📊 Results
- Achieved good accuracy on test data.  
- Model was able to correctly classify different languages.  
- Simple ANN worked well even with character-level features.  

---

## 🚀 Tools & Libraries
- Python  
- pandas, numpy, matplotlib, seaborn  
- scikit-learn  
- TensorFlow / Keras   
