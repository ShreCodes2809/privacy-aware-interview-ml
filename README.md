# **Privacy Enhancing Machine Learning for Job Interview Analysis**
This project explores privacy-preserving machine learning techniques to assess communication quality in job interviews. Using the VetTrain dataset, the study classifies responses into four levels: under-explained, succinct, comprehensive, and over-explained. The focus is on developing fair, ethical, and privacy-enhancing models for automated job interview evaluations.

---

## **Project Overview**
The primary objective of this project is to:
- Analyze the quality of responses in job interviews.
- Mitigate speaker-identity-based biases in machine learning models.
- Balance privacy, fairness, and transparency while maintaining model performance.

The study employs advanced linguistic feature extraction techniques and implements tree-based, deep learning, and transformer-based models.

---

## **Dataset**
- **Name**: VetTrain Dataset
- **Description**: Annotated transcripts from 38 participants, capturing interview responses.
- **Features**:
  - Behavioral labels: under-explained, succinct, comprehensive, over-explained.
  - Linguistic features: TF-IDF, POS tagging, sentiment scores, and word embeddings.
- **Structure**:
  - Question-response pairs with participant IDs.
  - Behavioral annotations as ground truth for classification.

---

## **Key Features**
### 1. **Feature Engineering**
- **TF-IDF**: Represents text importance in a document relative to a collection.
- **Part-of-Speech (POS) Tagging**: Captures syntactic structure.
- **Sentiment Analysis**: Quantifies emotional tone using metrics like positive, neutral, negative, and compound scores.
- **Word Embeddings**: Encodes semantic richness and context using Sentence Transformers.

### 2. **Classification Tasks**
- **Speaker Identification**: Predicts speaker identity while reducing bias.
- **Degree of Explanation**:
  - Binary classification tasks: Under-explained vs. Succinct, Over-explained vs. Comprehensive.

### 3. **Bias Mitigation**
- Feature selection using **mutual information** to remove speaker-dependent features.
- Balanced sample weights for equitable performance across speakers.

---

## **Models Used**
### 1. **Tree-Based Models**
- **Decision Tree**, **Random Forest**, and **Gradient Boosting**.
- Feature selection with hyperparameter tuning.

### 2. **Deep Learning Models**
- **LSTM**: Captures temporal patterns in sequential data.
- **Conv1D**: Extracts local feature dependencies.

### 3. **Transformer-Based Models**
- **Sentence Transformers (MiniLM)**: Explores zero-shot classification for response evaluation.

---

## **Results**
- **Speaker Identification**:
  - Best balanced accuracy: **Random Forest** (47.90% with 200 features).
- **Classification Tasks**:
  - **Under-explained vs. Succinct**:
    - Conv1D achieved highest balanced accuracy: **66.67%**.
  - **Over-explained vs. Comprehensive**:
    - Random Forest achieved best balanced accuracy: **79.00%**.
- **Bias Mitigation**:
  - Comparable model performance with reduced speaker dependencies.
- **Transformer Performance**:
  - Limited effectiveness due to tokenization constraints; future work on prompt engineering suggested.

---

## **Setup and Usage**
1. **Clone the repository**:
   ```bash
   git clone https://github.com/ShreCodes2809/privacy-aware-interview-ml.git
   cd privacy-aware-interview-ml
   ```

2. **View Results**:
   - Output files include accuracy, balanced accuracy, and confusion matrices for each model.

---

## **Future Enhancements**
- Refine transformer-based models with **prompt engineering** and **few-shot learning**.
- Expand analysis to include additional linguistic features and larger datasets.
- Apply findings to real-world automated interview evaluation systems.

---

This project was completed as part of the **CSCI 5622 - Machine Learning** coursework by **Team 9**:
- Ayushi S
- Amulya A
- Shreyash S
- Yuanyuan W
