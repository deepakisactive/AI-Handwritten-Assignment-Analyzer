# 🧠 AI Handwritten Assignment Analyzer (Deep Learning)

## 📌 Overview
This project presents an end-to-end deep learning system that converts handwritten assignments into machine-readable text and evaluates similarity using transformer-based models. The system combines computer vision and natural language processing to analyze both exact and semantic similarity between assignments.

---

## 🚀 Features
- ✍️ Handwritten text recognition using deep learning (CRNN)
- 🧠 Semantic understanding using transformer models
- 📊 Dual similarity scoring:
  - Semantic similarity (meaning-based)
  - Exact similarity (text-based)
- 📄 End-to-end pipeline from image → text → analysis
- 📈 Scalable and extensible for academic evaluation systems

---

## 🧩 System Architecture

```
Handwritten Image
      ↓
CNN (Feature Extraction)
      ↓
RNN / Transformer (Sequence Modeling)
      ↓
Recognized Text
      ↓
Transformer Encoder (BERT / Sentence-BERT)
      ↓
Embedding Vectors
      ↓
Similarity Computation
      ↓
Final Scores
```

---

## 🧠 Methodology

### 1. Handwriting Recognition (CRNN)

The system uses a **Convolutional Recurrent Neural Network (CRNN)**:

- **CNN**: Extracts spatial features from handwritten images  
- **RNN (LSTM/GRU)**: Models sequential dependencies in text  
- **CTC Loss**: Enables training without character-level alignment  

**CTC Loss Function:**
```
L_CTC = -log P(y | x)
```

---

### 2. Text Representation (Transformers)

Extracted text is processed using transformer-based models:

- BERT  
- Sentence-BERT  

These models generate contextual embeddings that capture semantic meaning rather than just keyword overlap.

---

### 3. Similarity Computation

#### 🔹 Semantic Similarity
- Sentence embeddings are generated  
- Cosine similarity is computed:

```
Similarity = (A · B) / (||A|| ||B||)
```

#### 🔹 Exact Similarity (Optional)
- Levenshtein Distance  
- Jaccard Similarity  

---

## 📊 Output

The system provides:

- Extracted text from handwritten input  
- Semantic similarity score  
- Exact similarity score  
- (Optional) Highlighted differences  

---

## 🛠️ Tech Stack

- **Languages**: Python  
- **Deep Learning**: TensorFlow / PyTorch  
- **Computer Vision**: OpenCV  
- **NLP Models**: HuggingFace Transformers  
- **Libraries**:
  - NumPy  
  - Pandas  
  - Scikit-learn  

---

## 📁 Project Structure

```
├── data/
├── models/
│   ├── crnn_model.py
│   ├── transformer_model.py
├── utils/
│   ├── preprocessing.py
│   ├── similarity.py
├── app/
│   ├── main.py
├── notebooks/
├── README.md
```

---

## ⚙️ Installation

```bash
git clone https://github.com/your-username/ai-handwritten-analyzer.git
cd ai-handwritten-analyzer
pip install -r requirements.txt
```

---

## ▶️ Usage

```bash
python app/main.py --input path_to_image
```

---

## 📈 Future Improvements

- Improve OCR accuracy for noisy handwriting  
- Add multilingual support  
- Integrate grading system  
- Build web-based dashboard  
- Real-time evaluation system  

---

## 🎯 Applications

- Academic plagiarism detection  
- Automated assignment evaluation  
- Digital archiving of handwritten documents  
- Educational tools for assessment  

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

Deepak